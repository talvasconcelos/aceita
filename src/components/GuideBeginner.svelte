<script>
  import GetingStarted from '../sectors/GetingStarted.svelte';
  import Mining from '../sectors/Mining.svelte';
  import Nodes from '../sectors/Nodes.svelte';
  import Network from '../sectors/Network.svelte';
  import Blockchain from '../sectors/Blockchain.svelte';
  import Blocks from '../sectors/Blocks.svelte';

  let activeSector = null;

  const changeSector = (id) => {
    activeSector = id;
    console.log(activeSector);
  };
</script>

<article>
  <p>
    Ouviu falar sobre Bitcoin e quer entrar na toca do coelho? Vamos começar...
  </p>
  <ul class="clickable">
    <li on:click={() => changeSector('intro')}>Introdução</li>
    <li on:click={() => changeSector('network')}>Rede Bitcoin</li>
    <li>
      <ul>
        <li on:click={() => changeSector('nodes')}>Nós</li>
      </ul>
    </li>
    <li on:click={() => changeSector('mining')}>Mineração</li>
    <li>
      <ul>
        <li on:click={() => changeSector('blockchain')}>Blockchain</li>
        <li on:click={() => changeSector('blocks')}>Blockchain</li>
      </ul>
    </li>
  </ul>
  {#if activeSector == 'intro'}
    <GetingStarted />
  {:else if activeSector == 'network'}
    <Network />
  {:else if activeSector == 'nodes'}
    <Nodes />
  {:else if activeSector == 'mining'}
    <Mining />
  {:else if activeSector == 'blockchain'}
    <Blockchain />
  {:else if activeSector == 'blocks'}
    <Blocks />
  {/if}
</article>

<style lang="scss">
  ul.clickable {
    list-style-type: none;
    margin-bottom: 2rem;

    & li {
      width: fit-content;
      text-decoration: underline;
      font-size: 1.1rem;
      font-weight: 400;
      cursor: pointer;

      & ul {
        list-style-type: circle;
      }
    }
  }
</style>
