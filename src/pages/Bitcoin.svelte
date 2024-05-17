<script>
  import { Tabs, Tab, TabList, TabPanel } from 'svelte-tabs';
  import GuideHome from '../components/GuideHome.svelte';
  import GuideBeginner from '../components/GuideBeginner.svelte';
</script>

<section class="container grid-lg">
  <header>
    <h2>Como Funciona Bitcoin</h2>
  </header>
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
</section>
