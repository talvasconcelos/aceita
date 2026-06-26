<script>
  import { Link } from "svelte-navigator";
  export let projectName,
    projectService,
    contact,
    description,
    img,
    buttonText,
    buttonURL;
</script>

<article class="project-card">
  <figure class="project-image">
    <img src={img} alt={projectService} />
  </figure>
  <div class="project-content">
    <h3 class="project-title">{projectService}</h3>
    <div class="project-details">
      <p class="description">
        {description}
      </p>
      <p class="project-name"><strong>Nome:</strong> {projectName}</p>
      <p class="contact"><strong>Contacto:</strong> {contact}</p>
    </div>
    {#if buttonURL}
      <button
        on:click={() => window.open(buttonURL, "_blank")}
        class="btn btn-primary">{buttonText}</button
      >
    {/if}
  </div>
</article>

<style lang="scss">
  .project-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow:
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
    transition:
      transform 0.2s ease-in-out,
      box-shadow 0.2s ease-in-out;
    height: 100%;
    display: flex;
    flex-direction: column;

    &:hover {
      transform: translateY(-4px);
      box-shadow:
        0 10px 15px -3px rgba(0, 0, 0, 0.1),
        0 4px 6px -2px rgba(0, 0, 0, 0.05);
    }
  }

  .project-image {
    margin: 0;
    padding: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #f9fafb;

    img {
      max-width: 200px;
      height: auto;
      object-fit: contain;
    }
  }

  .project-content {
    padding: 1.5rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }

  .project-title {
    margin: 0 0 1rem;
    font-size: 1.5rem;
    color: #1a202c;
  }

  .project-details {
    flex-grow: 1;

    p {
      margin: 0.75rem 0;
      color: #4a5568;
      line-height: 1.5;
    }

    .description {
      margin-bottom: 1rem;
    }
  }

  .btn {
    margin-top: 1rem;
    width: 100%;
    text-align: center;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    background-color: var(--button-blue);
    color: white;
    border: none;
    border-radius: 8px;
    transition: all 0.2s ease;
  }

  .btn:hover {
    background-color: var(--button-blue-light);
    transform: translateY(-1px);
  }

  @media (max-width: 600px) {
    .project-card {
      text-align: center;
    }

    .project-image img {
      max-width: 150px;
    }
  }
</style>
