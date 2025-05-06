<script>
  import { Link } from "svelte-navigator";
</script>

<nav class="navbar container grid-xl">
  <section class="navbar-section">
    <Link to="/" class="navbar-brand mr-2 text-secondary"
      >Aceita <img
        class="bitcoin-logo"
        src="../../images/btc_logo.png"
        alt="aceita bitcoin"
      /><span class="bitcoin-word">Bitcoin</span></Link
    >
  </section>
  <section class="navbar-section">
    <Link to="/encontros" class="btn btn-link">Encontros</Link>
    <Link to="/eventos" class="btn btn-link">Eventos</Link>
    <Link to="/porque-bitcoin" class="btn btn-link">Porquê Bitcoin</Link>
    <Link to="/parceiros" class="btn btn-link">Parceiros</Link>
  </section>
</nav>

<style>
  .navbar {
    height: 90px;
  }
  .bitcoin-word {
    opacity: 0;
    width: 0;
  }
  .bitcoin-logo {
    width: auto;
    height: 1.15rem;
    margin-left: 5px;
    align-self: center;
    margin-bottom: 2px;
    opacity: 1;
    transition: all 0.3s linear;
  }
  @media (min-width: 600px) {
    .bitcoin-logo {
      width: 0;
      opacity: 0;
    }
    .bitcoin-word {
      width: auto;
      opacity: 1;
      transition: all 0.3s linear;
    }
  }
</style>
