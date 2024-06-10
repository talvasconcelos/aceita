<script>
    import PatronCard from "../components/PatronCard.svelte";
    const mockPatrons = [
        {
            patronName: "Choppork",
            patronService: "Ervaboca",
            contact: "ervaboca@proton.me",
            website: "https://www.ervaboca.pt",
            img: "images/patrons/carne.jpeg",
            serviceDescription: "Organic Grass Fed Barrosã",
        },
        {
            patronName: "Ojeda",
            patronService: "Residencia Paraguai",
            contact: "ojeda@service.com",
            website: "https://www.offshorePara.com",
            img: "images/patrons/segundaresidencia.jpg",
            serviceDescription: "Serviço de Obtenção de Residência Paraguai",
        },
        {
            patronName: "Chico",
            patronService: "Bitcoin Consulting",
            contact: "chico@advisor.com",
            website: "https://www.chicoconsulting.com",
            img: "images/patrons/consultor.jpeg",
            serviceDescription: "Serviço de Consultoria Bitcoiner",
        },
        {
            patronName: "LocalP2P",
            patronService: "Buy and Sell P2P",
            contact: "local@p2p.com",
            website: "https://www.p2p-pt.com",
            img: "images/patrons/p2pbitcoin.png",
            serviceDescription: "Serviço de Compra e Venda de Bitcoin P2P",
        },
    ];

    let patrons = [];

    async function fetchPatrons() {
        const url = `https://raw.githubusercontent.com/talvasconcelos/aceita/main/patrons.json`;
        try {
            const response = await fetch(url);
            if (!response.ok) throw new Error("Patrons not found");
            return response.json();
        } catch (error) {
            console.error(`Error fetching Patrons:`, error);
            return mockPatrons;
        }
    }

    // Fetch and order meetups on component initialization
    fetchPatrons().then((fetchedPatrons) => {
        patrons = fetchedPatrons;
        console.log(patrons);
    });
</script>

<section class="container grid-lg">
    <header>
        <h2>Apoiantes</h2>
        <div class="subtitle">
            <p>Descubra as pessoas que apoiam o nosso trabalho</p>
        </div>
    </header>
    <section class="container grid-lg">
        <div cl>
            {#each patrons as patron, i}
                <PatronCard
                    patronName={patron.patronName}
                    patronService={patron.patronService}
                    contact={patron.contact}
                    description={patron.serviceDescription}
                    img={patron.img}
                    buttonURL={patron.website}
                    buttonText="Saber Mais"
                    img_right
                />
            {/each}
        </div>
    </section>
</section>

<style>
    .quote {
        text-align: center;
        width: 100%;
        font-size: 1.2rem;
        font-weight: 300;
        padding: 1rem 0;
    }
    @media (min-width: 600px) {
        .quote {
            font-size: 1.5rem;
        }
    }
</style>
