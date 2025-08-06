<script>
  export let bullet;
</script>

<div class="bullet-point">
  <h4 class="bullet-title">{bullet}</h4>
  <p class="bullet-content">
    <slot />
  </p>
</div>

<style>
  .bullet-point {
    margin-bottom: 2rem;
    padding: 1.5rem;
    background: white;
    border-radius: 8px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    transition:
      transform 0.2s ease,
      box-shadow 0.2s ease;
  }

  .bullet-point:hover {
    transform: translateY(-2px);
    box-shadow:
      0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }

  .bullet-title {
    color: #2563eb;
    font-size: 1.25rem;
    margin: 0 0 0.75rem 0;
    font-weight: 600;
  }

  .bullet-content {
    color: #4a5568;
    line-height: 1.6;
    margin: 0;
  }

  @media (max-width: 640px) {
    .bullet-point {
      padding: 1.25rem;
    }

    .bullet-title {
      font-size: 1.125rem;
    }
  }
</style>
