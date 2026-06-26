<script>
  import { onMount } from "svelte";
  import ProjectCard from "../components/ProjectCard.svelte";

  let projects = [];

  async function fetchProjects() {
    const url = `https://raw.githubusercontent.com/talvasconcelos/aceita/main/projects.json`;
    try {
      const response = await fetch(url);
      if (!response.ok) throw new Error("Projects not found");
      return await response.json();
    } catch (error) {
      console.error(`Error fetching Projects:`, error);
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

  // Fetch projects on component initialization
  onMount(async () => {
    const fetchedProjects = await fetchProjects();
    if (fetchedProjects && fetchedProjects.projects) {
      projects = await Promise.all(
        fetchedProjects.projects.map(async (project) => {
          project.img = await fetchImage(project.img);
          return project;
        }),
      );
    }
  });
</script>

<section class="projects-section">
  <div class="container grid-lg">
    <header class="section-header">
      <h2>Projetos</h2>
      <div class="subtitle">
        <p>Descubra os projetos que estamos desenvolvendo</p>
      </div>
    </header>
    <div class="project-grid">
      {#each projects as project, i}
        <ProjectCard
          projectName={project.projectName}
          projectService={project.projectService}
          contact={project.contact}
          description={project.serviceDescription}
          img={project.img}
          buttonURL={project.website}
          buttonText="Saber Mais"
        />
      {/each}
    </div>
  </div>
</section>

<style>
  .projects-section {
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

  .project-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
  }

  @media (min-width: 768px) {
    .project-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 639px) {
    .projects-section {
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

  .project-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
  }

  @media (min-width: 768px) {
    .project-grid {
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
