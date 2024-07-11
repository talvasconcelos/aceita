<script>
  import { onMount } from "svelte";
  import PatronCard from "../components/PatronCard.svelte";

  let patrons = [];

  async function fetchPatrons() {
    const url = `https://raw.githubusercontent.com/talvasconcelos/aceita/main/patrons.json`;
    try {
      const response = await fetch(url);
      if (!response.ok) throw new Error("Patrons not found");
      return await response.json();
    } catch (error) {
      console.error(`Error fetching Patrons:`, error);
    }
  }

  async function fetchImage(imageUrl) {
    const url = imageUrl;
    try {
      const response = await fetch(url);
      if (!response.ok) throw new Error("Image not found");
      const blob = await response.blob();
      return URL.createObjectURL(blob);
    } catch (error) {
      console.error(`Error fetching image:`, error);
      return ""; // Return empty string if image fetch fails
    }
  }

  // Fetch and order meetups on component initialization
  fetchPatrons().then((fetchedPatrons) => {
    patrons = fetchedPatrons.patrons;
  });

  onMount(async () => {
    const fetchedPatrons = await fetchPatrons();
    if (fetchedPatrons && fetchedPatrons.patrons) {
      patrons = await Promise.all(
        fetchedPatrons.map(async (patron) => {
          patron.img = await fetchImage(patron.img);
          return patron;
        }),
      );
    }
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
