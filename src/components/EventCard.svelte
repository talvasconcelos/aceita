<script>
  export let title,
    subtitle,
    date,
    time,
    address,
    img,
    description,
    signinUrl,
    btnText;
</script>

<div class="event-card">
  <div class="card-image">
    {#if img}
      <img src={img} alt={title} />
    {:else}
      <img src="images/evento.png" alt="event" />
    {/if}
  </div>
  <div class="card-content">
    <div class="card-header">
      {#if title}
        <h3 class="card-title">{title}</h3>
      {/if}
      {#if subtitle}
        <h4 class="card-subtitle">{subtitle}</h4>
      {/if}
    </div>

    <div class="event-details">
      <div class="datetime">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          ><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line
            x1="16"
            y1="2"
            x2="16"
            y2="6"
          ></line><line x1="8" y1="2" x2="8" y2="6"></line><line
            x1="3"
            y1="10"
            x2="21"
            y2="10"
          ></line></svg
        >
        <span>{date} · {time}</span>
      </div>
      {#if address}
        <div class="location">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            ><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"
            ></path><circle cx="12" cy="10" r="3"></circle></svg
          >
          <span>{address}</span>
        </div>
      {/if}
    </div>

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
  .event-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    height: 100%;
    display: flex;
    flex-direction: column;
    box-shadow:
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
    transition:
      transform 0.2s ease-in-out,
      box-shadow 0.2s ease-in-out;
  }

  .event-card:hover {
    transform: translateY(-4px);
    box-shadow:
      0 10px 15px -3px rgba(0, 0, 0, 0.1),
      0 4px 6px -2px rgba(0, 0, 0, 0.05);
  }

  .card-image {
    position: relative;
    padding-top: 56.25%;
    background: #f3f4f6;
    overflow: hidden;
  }

  .card-image img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .card-content {
    padding: 1.5rem;
    flex: 1;
    display: flex;
    flex-direction: column;
  }

  .card-header {
    margin-bottom: 1rem;
  }

  .card-title {
    font-size: 1.25rem;
    font-weight: 600;
    color: #1a202c;
    margin: 0 0 0.5rem;
  }

  .card-subtitle {
    font-size: 1rem;
    font-weight: 500;
    color: #2563eb;
    margin: 0;
  }

  .event-details {
    margin-bottom: 1rem;
    font-size: 0.875rem;
    color: #64748b;
  }

  .datetime,
  .location {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-bottom: 0.5rem;
  }

  .location {
    margin-bottom: 0;
  }

  .datetime svg,
  .location svg {
    flex-shrink: 0;
    color: #2563eb;
  }

  .description {
    color: #4a5568;
    line-height: 1.6;
    margin: 0 0 1.5rem;
    flex: 1;
  }

  .btn {
    width: 100%;
    padding: 0.75rem 1.5rem;
    border-radius: 6px;
    font-weight: 500;
    border: none;
    cursor: pointer;
    text-align: center;
    display: inline-flex;
    justify-content: center;
    align-items: center;
  }

  .btn-primary {
    background-color: #2563eb;
    color: white;
    transition: background-color 0.2s ease;
  }

  .btn-primary:hover {
    background-color: #1d4ed8;
  }

  @media (max-width: 640px) {
    .card-content {
      padding: 1.25rem;
    }

    .card-title {
      font-size: 1.125rem;
    }
  }
</style>
