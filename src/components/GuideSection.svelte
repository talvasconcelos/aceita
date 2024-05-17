<script>
  export let hashtag, title;
</script>

<div>
  <h5><a class="anchor" href={`#${hashtag}`}>{title}</a></h5>
  <slot />
</div>

<style>
  .anchor {
    color: inherit;
    text-decoration: none;
  }
</style>
