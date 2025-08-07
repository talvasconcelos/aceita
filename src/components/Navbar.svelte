<script>
  import { Link } from "svelte-navigator";
</script>

<nav class="navbar">
  <div class="navbar-container container grid-xl">
    <Link to="/" class="navbar-brand mr-2 text-primary">
      Aceita
      <img
        class="bitcoin-logo"
        src="../../images/btc_logo.png"
        alt="aceita bitcoin"
      />
      <span class="bitcoin-word">Bitcoin</span>
    </Link>

    <div class="navbar-links">
      <Link to="/encontros" class="nav-link">Encontros</Link>
      <Link to="/eventos" class="nav-link">Eventos</Link>
      <Link to="/porque-bitcoin" class="nav-link">Porquê Bitcoin</Link>
      <Link to="/parceiros" class="nav-link">Parceiros</Link>
    </div>
  </div>
</nav>

<style>
  .navbar {
    height: 70px;
    background: white;
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  }

  .navbar-container {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .navbar-brand {
    display: flex;
    align-items: center;
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--bitcoin-orange);
    text-decoration: none;
    transition: color 0.2s ease;
  }

  .navbar-brand:hover {
    color: var(--bitcoin-orange-dark);
  }

  .bitcoin-word {
    opacity: 0;
    width: 0;
    overflow: hidden;
    transition: all 0.3s ease;
  }

  .bitcoin-logo {
    width: auto;
    height: 1.25rem;
    margin-left: 5px;
    opacity: 1;
    transition: all 0.3s ease;
  }

  .navbar-links {
    display: flex;
    gap: 1.5rem;
    align-items: center;
  }

  .nav-link {
    color: var(--button-blue);
    text-decoration: none;
    font-weight: 500;
    font-size: 1rem;
    padding: 0.5rem;
    border-radius: 6px;
    transition: all 0.2s ease;
    position: relative;
  }

  .nav-link:hover {
    color: var(--button-blue-light);
  }

  .nav-link::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 50%;
    width: 0;
    height: 2px;
    background: var(--button-blue);
    transition: all 0.2s ease;
    transform: translateX(-50%);
  }

  .nav-link:hover::after {
    width: calc(100% - 1rem);
  }

  @media (min-width: 600px) {
    .bitcoin-logo {
      width: 0;
      opacity: 0;
    }
    .bitcoin-word {
      width: auto;
      opacity: 1;
      margin-left: 5px;
    }
  }

  @media (max-width: 639px) {
    .navbar {
      height: 60px;
    }

    .navbar-links {
      gap: 1rem;
    }

    .nav-link {
      font-size: 0.875rem;
      padding: 0.375rem;
    }
  }
</style>
