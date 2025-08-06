<script>
  import { Link } from "svelte-navigator";
  export let patronName,
    patronService,
    contact,
    description,
    img,
    buttonText,
    buttonURL;
</script>

<article class="patron-card">
  <figure class="patron-image">
    <img src={img} alt={patronService} />
  </figure>
  <div class="patron-content">
    <h3 class="patron-title">{patronService}</h3>
    <div class="patron-details">
      <p class="description">
        {description}
      </p>
      <p class="patron-name"><strong>Nome:</strong> {patronName}</p>
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
  .patron-card {
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

  .patron-image {
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

  .patron-content {
    padding: 1.5rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }

  .patron-title {
    margin: 0 0 1rem;
    font-size: 1.5rem;
    color: #1a202c;
  }

  .patron-details {
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
    .patron-card {
      text-align: center;
    }

    .patron-image img {
      max-width: 150px;
    }
  }
</style>
