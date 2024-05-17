<script>
  import { onMount } from 'svelte';
  import QRious from 'qrious';

  export let items = [];
  export let activeTabValue;
  export let data;

  onMount(() => {
    // Set default tab value
    if (Array.isArray(items) && items.length && items[0].value) {
      activeTabValue = items[0].value;
    }
  });

  const handleClick = (tabValue) => () => (activeTabValue = tabValue);
</script>

<ul class="tab tab-block">
  {#if Array.isArray(items)}
    {#each items as item}
      <li class="tab-item" class:active={activeTabValue === item.value}>
        <a href="#" on:click={handleClick(item.value)}>{item.label}</a>
        <Tab />
      </li>
    {/each}
  {/if}
</ul>
