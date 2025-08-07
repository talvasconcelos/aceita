<script>
  import { onMount } from "svelte";
  import MeetupCard from "../components/MeetupCard.svelte";

  let meetups = [];

  async function fetchMeetups() {
    const url = `https://raw.githubusercontent.com/talvasconcelos/aceita/main/meetups.json`;
    try {
      const response = await fetch(url);
      if (!response.ok) throw new Error("Meetups not found");
      return await response.json();
    } catch (error) {
      console.error(`Error fetching Meetups:`, error);
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

  // Fetch on component initialization
  onMount(async () => {
    const fetchedMeetups = await fetchMeetups();
    if (fetchedMeetups && fetchedMeetups.meetups) {
      meetups = await Promise.all(
        fetchedMeetups.meetups.map(async (meetup) => {
          meetup.img = await fetchImage(meetup.img);
          return meetup;
        })
      );
    }
  });
</script>

<section class="meetups-section">
  <div class="container grid-lg">
    <header class="section-header">
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
          img={meetup.img}
          description={meetup.description}
          signinUrl={meetup.link}
          btnText="Saber Mais"
        />
      {/each}
    </div>
  </div>
</section>

<style>
  .meetups-section {
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

  .card-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
  }

  @media (min-width: 640px) {
    .card-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 639px) {
    .meetups-section {
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
</style>
