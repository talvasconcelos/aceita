<script>
  export let title, image, type, description, url;
  if (!type) {
    type = 'website';
  }
</script>

<svelte:head>
  <!-- TITLE -->
  {#if title}
    <meta property="og:title" content={title} />
    <meta name="twitter:title" content={title} />
  {/if}
  <!-- DESCRIPTION -->
  {#if description}
    <meta property="og:description" content={description} />
    <meta name="twitter:description" content={description} />
  {/if}
  <!-- URL -->
  {#if url}
    <meta property="og:url" content={url} />
    <meta property="twitter:url" content={url} />
    <meta property="twitter:domain" content={url.split('://')[1]} />
  {/if}
  <!-- IMAGE -->
  <!-- {#if image}
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:image" content={image} />
    <meta property="og:image" content={image} />
    <meta property="og:image:width" content="1200" />
    <meta property="og:image:height" content="630" />
  {/if} -->
  <!-- TYPE -->
  <meta property="og:type" content="website" />
</svelte:head>
