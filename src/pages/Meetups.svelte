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
  onMount(async () => {
    const fetchedMeetups = await fetchMeetups();
    if (fetchedMeetups && fetchedMeetups.meetups) {
      const orderedMeetups = orderMeetups(fetchedMeetups.meetups);
      meetups = await Promise.all(
        orderedMeetups.map(async (meetup) => {
          meetup.img = await fetchImage(meetup.img);
          return meetup;
        }),
      );
    }
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
