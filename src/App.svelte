<script>
  import { Router, Route } from "svelte-navigator";
  import Navbar from "./components/Navbar.svelte";
  import Footer from "./components/Footer.svelte";
  import Home from "./pages/Home.svelte";
  import Events from "./pages/Events.svelte";
  import Meetups from "./pages/Meetups.svelte";
  import Donate from "./pages/Donate.svelte";
  import Podcast from "./pages/Podcast.svelte";
  import Patrons from "./pages/Patrons.svelte";
  import Why from "./pages/Why.svelte";
  import Bitcoin from "./pages/Bitcoin.svelte";
</script>

<Router>
  <Navbar />
  <main>
    <Route path="/">
      <Home />
    </Route>
    <Route path="/encontros">
      <Meetups />
    </Route>
    <Route path="/eventos">
      <Events />
    </Route>
    <Route path="/donate">
      <Donate />
    </Route>
    <Route path="/podcast">
      <Podcast />
    </Route>
    <Route path="/porque-bitcoin">
      <Why />
    </Route>
    <Route path="/parceiros">
      <Patrons />
    </Route>
    <Route path="/como-funciona-bitcoin">
      <Bitcoin />
    </Route>
  </main>
  <Footer />
</Router>
