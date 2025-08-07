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

  // Fetch patrons on component initialization
  onMount(async () => {
    const fetchedPatrons = await fetchPatrons();
    if (fetchedPatrons && fetchedPatrons.patrons) {
      patrons = await Promise.all(
        fetchedPatrons.patrons.map(async (patron) => {
          patron.img = await fetchImage(patron.img);
          return patron;
        })
      );
    }
  });
</script>

<section class="patrons-section">
  <div class="container grid-lg">
    <header class="section-header">
      <h2>Parceiros</h2>
      <div class="subtitle">
        <p>Descubra as pessoas que apoiam o nosso trabalho</p>
      </div>
    </header>
    <div class="patron-grid">
      {#each patrons as patron, i}
        <PatronCard
          patronName={patron.patronName}
          patronService={patron.patronService}
          contact={patron.contact}
          description={patron.serviceDescription}
          img={patron.img}
          buttonURL={patron.website}
          buttonText="Saber Mais"
        />
      {/each}
    </div>
  </div>
</section>

<style>
  .patrons-section {
    padding: 4rem 0;
    background-color: #f8fafc;
  }

  .section-header {
    text-align: center;
    margin-bottom: 3.5rem;
  }

  .section-header h2 {
    font-size: 2.5rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 1rem;
  }

  .subtitle {
    max-width: 600px;
    margin: 0 auto;
  }

  .subtitle p {
    font-size: 1.125rem;
    color: #64748b;
    line-height: 1.6;
  }

  .patron-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
  }

  @media (min-width: 768px) {
    .patron-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 639px) {
    .patrons-section {
      padding: 3rem 0;
    }

    .section-header {
      margin-bottom: 2.5rem;
    }

    .section-header h2 {
      font-size: 2rem;
    }

    .subtitle p {
      font-size: 1rem;
    }
  }

  .patron-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
  }

  @media (min-width: 768px) {
    .patron-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

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
