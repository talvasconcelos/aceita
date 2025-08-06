<script>
  export let title, subtitle, img, description, signinUrl, btnText;
</script>

<div class="meetup-card">
  <div class="card-image">
    {#if img}
      <img src={img} alt={title} />
    {:else}
      <img src="images/evento.png" alt="event" />
    {/if}
  </div>
  <div class="card-content">
    {#if title}
      <h3 class="card-title">{title}</h3>
    {/if}
    {#if description}
      <p class="description">{description}</p>
    {/if}
    {#if signinUrl}
      <button
        on:click={() => window.open(signinUrl, "_blank")}
        class="btn btn-primary">{btnText ?? "Inscrição"}</button
      >
    {/if}
  </div>
</div>

<style>
  .meetup-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow:
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
    height: 100%;
    display: flex;
    flex-direction: column;
    transition:
      transform 0.2s ease-in-out,
      box-shadow 0.2s ease-in-out;
  }

  .meetup-card:hover {
    transform: translateY(-4px);
    box-shadow:
      0 10px 15px -3px rgba(0, 0, 0, 0.1),
      0 4px 6px -2px rgba(0, 0, 0, 0.05);
  }

  .card-image {
    position: relative;
    padding: 1.5rem;
    background: #f3f4f6;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 180px;
  }

  .card-image img {
    max-width: 100%;
    max-height: 180px;
    object-fit: contain;
    transition: transform 0.3s ease;
  }

  .meetup-card:hover .card-image img {
    transform: scale(1.05);
  }

  .card-content {
    padding: 1.5rem;
    flex: 1;
    display: flex;
    flex-direction: column;
  }

  .card-title {
    margin: 0 0 1rem;
    font-size: 1.25rem;
    font-weight: 600;
    color: #1a202c;
    line-height: 1.4;
  }

  .description {
    color: #4a5568;
    line-height: 1.5;
    margin: 0 0 1.5rem;
    flex: 1;
  }

  .btn {
    width: 100%;
    padding: 0.75rem 1.5rem;
    border-radius: 6px;
    font-weight: 500;
    text-transform: none;
    letter-spacing: 0;
    text-align: center;
    display: inline-flex;
    justify-content: center;
    align-items: center;
  }

  .btn-primary {
    background-color: #2563eb;
    color: white;
    border: none;
    transition: background-color 0.2s ease;
  }

  .btn-primary:hover {
    background-color: #1d4ed8;
  }

  @media (max-width: 600px) {
    .card-content {
      padding: 1.25rem;
    }

    .card-title {
      font-size: 1.125rem;
    }
  }
</style>
