<script>
    import MeetupCard from "../components/MeetupCard.svelte";
    const mockMeetups = [
        {
            name: "Portugal Norte - Bitcoin Meetup",
            location: {
                place: "French Fries Factory",
                address: "Rua do Bonjardim 302",
                city: "Porto",
            },
            time: "2024-05-25 18:00:00Z",
            img: "images/meetups/meetupNorte.jpeg",
            description:
                "Toxic Maxis Only - No Shitcoins Allowed; Lightning Payments Accepted",
            link: "https://t.me/btcnortept",
        },
        {
            name: "Portugal Oeste - Bitcoin Meetup",
            location: {
                place: "Pizzaria Papadoc",
                address: "R. Ilha do Corvo 1",
                city: "Marinha Grande",
            },
            time: "2024-05-22T19:30:00Z",
            img: "images/meetups/meetupOeste.jpeg",
            description: "Traz um amigo - shitcoins not welcome",
            link: "https://t.me/OesteBitcoinMeetUp",
        },
        {
            name: "Lisbon Bitcoin Maxis",
            location: {
                place: "Carnalentejana",
                address: "Campo Pequeno D",
                city: "Lisboa",
            },
            time: "2024-05-27T17:00:00Z",
            img: "images/meetups/meetupLisboa.jpeg",
            description: "The Genesis Book, by Aaron Van Wirdum",
            link: "https://www.meetup.com/lisbon-bitcoin-maximalists/",
        },
        {
            name: "Bitcoin Tribe Algarve",
            location: {
                place: "Default Place",
                address: "Somewhere in Algarve",
                city: "Faro",
            },
            time: "2024-05-27T17:00:00Z",
            img: "images/meetups/meetupAlgarve.jpeg",
            description: "No shitcoining - Ln Accepted",
            link: "https://t.me/BitcoinAlgarve",
        },
        {
            name: "FREE Madeira Bitcoin Meetup",
            location: {
                place: "Pizzaria Papadoc",
                address: "CCIF",
                city: "Funchal",
            },
            time: "2024-05-30T17:00:00Z",
            img: "images/meetups/meetupMadeira.jpeg",
            description: "No shitcoining - Ln Accepted",
            link: "https://t.me/freemadeira",
        },
    ];

    let meetups = [];

    async function fetchMeetups() {
        const url = `https://raw.githubusercontent.com/talvasconcelos/aceita/main/meetups.json`;
        try {
            const response = await fetch(url);
            if (!response.ok) throw new Error("Meetups not found");
            return response.json();
        } catch (error) {
            console.error(`Error fetching Meetups:`, error);
            return mockMeetups;
        }
    }

    function orderMeetups(meetups) {
        return meetups.sort((a, b) => {
            const dateA = new Date(a.time).getTime();
            const dateB = new Date(b.time).getTime();
            a.newDate = new Date(a.time).toLocaleDateString("pt-pt", {
                weekday: "long",
                year: "numeric",
                month: "short",
                day: "numeric",
            });
            a.newTime = new Date(a.time).toLocaleTimeString();
            b.newDate = new Date(b.time).toLocaleDateString("pt-pt", {
                weekday: "long",
                year: "numeric",
                month: "short",
                day: "numeric",
            });
            b.newTime = new Date(b.time).toLocaleTimeString();
            return dateA - dateB;
        });
    }

    // Fetch and order meetups on component initialization
    fetchMeetups().then((fetchedMeetups) => {
        meetups = orderMeetups(fetchedMeetups);
        console.log(meetups);
    });
</script>

<section class="container grid-lg">
    <header>
        <h2>Encontros</h2>
        <div class="subtitle">
            <p>Descubra os encontros que decorrem perto de si</p>
        </div>
    </header>
    <div class="card-grid">
        {#each meetups as meetup, i}
            <MeetupCard
                title={meetup.name}
                subtitle={""}
                place={meetup.location.place}
                address={meetup.location.address}
                city={meetup.location.city}
                date={meetup.newDate}
                time={meetup.newTime}
                img={meetup.img}
                description={meetup.description}
                signinUrl={meetup.link}
                btnText="Saber Mais"
            />
        {/each}
    </div>
</section>

<style>
    header {
        margin-bottom: 3rem;
    }
    .event-list {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    .card-grid {
        display: block;
    }
    @media (min-width: 600px) {
        .card-grid {
            display: grid;
            gap: 1rem;
            grid-template-columns: repeat(auto-fill, minmax(35%, 1fr));
        }
    }
    @media (min-width: 1280px) {
        .card-grid {
            display: grid;
            gap: 1rem;
            grid-template-columns: repeat(auto-fill, minmax(25%, 1fr));
        }
    }
</style>
