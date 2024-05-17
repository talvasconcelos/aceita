<script>
  export let title, subtitle, date, time, address, img, description, signinUrl, btnText;
</script>

<div class="card">
  <div class="card-header">
    {#if title}
      <div class="card-title h5">{title}</div>
    {/if}
    {#if subtitle}
      <div class="card-subtitle">
        <p>
          {subtitle}
          <br />
          {#if address}
            <small>{address}</small>
            <br />
          {/if}
          <small>{date}</small>
          <br />
          <small>{time}</small>
        </p>
      </div>
    {/if}
  </div>
    <div class="card-image">
    {#if img}
      <img src={img} alt="event" class="img-responsive" />
      {:else}
      <img src="images/evento.png" alt="event" class="img-responsive" />
      {/if}
    </div>
  {#if description}
    <div class="card-body">
      {description}
    </div>
  {/if}
  <div class="card-footer">
    {#if signinUrl}
      <button
        on:click={() => window.open(signinUrl, "_blank")}
        class="btn btn-primary">{btnText ?? 'Inscrição'}</button
      >
    {/if}
  </div>
</div>

<style>
  .card {
    border: none;
    margin-bottom: 1rem;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px,
      rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
  }

  @media (min-width: 600px) {
    .card {
      margin-bottom: 0;
    }
  }
</style>
