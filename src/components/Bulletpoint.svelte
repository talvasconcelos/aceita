<script>
  export let bullet;
</script>

<p>
  <strong>{bullet}</strong>
  <slot />
</p>

<style>
  strong::after {
    content: ' - ';
  }
</style>
