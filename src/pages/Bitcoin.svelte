<script>
  import { Tabs, Tab, TabList, TabPanel } from "svelte-tabs";
  import GuideHome from "../components/GuideHome.svelte";
  import GuideBeginner from "../components/GuideBeginner.svelte";
</script>

<section class="bitcoin-guide">
  <div class="hero">
    <div class="container grid-lg">
      <header>
        <h2>Como Funciona Bitcoin</h2>
        <div class="bitcoin-decoration">₿</div>
      </header>
    </div>
  </div>

  <div class="container grid-lg content-section">
    <Tabs>
      <TabList>
        <Tab>Home</Tab>
        <Tab>Iniciantes</Tab>
        <!-- <Tab>...</Tab> -->
      </TabList>

      <!-- Home -->
      <TabPanel>
        <GuideHome />
      </TabPanel>

      <TabPanel>
        <GuideBeginner />
      </TabPanel>

      <!-- <TabPanel>
        <h2>Panel Three</h2>
      </TabPanel> -->
    </Tabs>
  </div>
</section>

<style>
  .bitcoin-guide {
    background: linear-gradient(
      to bottom,
      var(--bg-dark) 0%,
      var(--bg-dark) 30%,
      var(--bg-light) 30%,
      var(--bg-light) 100%
    );
  }

  .hero {
    padding: 5rem 0 8rem;
    position: relative;
    overflow: hidden;
  }

  header {
    text-align: center;
    position: relative;
    z-index: 1;
  }

  h2 {
    font-size: 3.2rem;
    font-weight: 800;
    color: var(--bg-light);
    margin-bottom: 1rem;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }

  .bitcoin-decoration {
    font-size: 12rem;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgba(247, 147, 26, 0.1);
    z-index: 0;
  }

  .content-section {
    margin-top: -4rem;
    position: relative;
    z-index: 2;
  }

  :global(.svelte-tabs) {
    background: var(--bg-light);
    border-radius: 12px;
    box-shadow: 0 4px 24px rgba(0, 0, 0, 0.1);
    padding: 2.5rem;
  }

  :global(.svelte-tabs__tab-list) {
    border-bottom: 2px solid rgba(247, 147, 26, 0.1);
    margin-bottom: 2.5rem;
    display: flex;
    justify-content: center;
    gap: 2rem;
  }

  :global(.svelte-tabs__tab) {
    border: none;
    color: var(--secondary-color);
    font-weight: 600;
    font-size: 1.1rem;
    padding: 0.75rem 1.5rem;
    transition: all 0.3s ease;
    position: relative;
  }

  :global(.svelte-tabs__tab:hover) {
    color: var(--bg-dark);
  }

  :global(.svelte-tabs__tab--selected) {
    color: var(--bg-dark);
  }

  :global(.svelte-tabs__tab--selected::after) {
    content: "";
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 100%;
    height: 3px;
    background: linear-gradient(
      90deg,
      var(--bitcoin-orange) 0%,
      var(--bitcoin-orange-light) 100%
    );
    border-radius: 3px 3px 0 0;
  }

  :global(.svelte-tabs__panel) {
    padding: 1.5rem 0;
  }

  @media (max-width: 768px) {
    .hero {
      padding: 4rem 0 6rem;
    }

    h2 {
      font-size: 2.4rem;
    }

    .bitcoin-decoration {
      font-size: 8rem;
    }

    :global(.svelte-tabs__tab-list) {
      gap: 1rem;
    }

    :global(.svelte-tabs__tab) {
      font-size: 1rem;
      padding: 0.5rem 1rem;
    }
  }
</style>
