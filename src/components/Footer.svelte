<script>
  import { Link } from "svelte-navigator";
</script>

<footer class="footer-section">
  <div class="footer-content container grid-lg">
    <div class="footer-main">
      <div class="footer-brand">
        <h3>Aceita Bitcoin</h3>
        <p>
          Bitcoin é uma rede que funciona de forma consensual onde foi possível
          criar uma nova forma de pagamento e também uma nova moeda
          completamente digital.
        </p>
        <div class="social-links">
          <a
            href="mailto:geral@aceitabitcoin.pt"
            class="social-link"
            title="Email"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              ><path
                d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
              ></path><polyline points="22,6 12,13 2,6"></polyline></svg
            >
          </a>
          <a
            href="https://twitter.com/aceitabitcoinpt"
            target="_blank"
            class="social-link"
            title="Twitter"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              ><path
                d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
              ></path></svg
            >
          </a>
          <a
            href="https://t.me/aceitabitcoin"
            target="_blank"
            class="social-link"
            title="Telegram"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              ><path
                d="M21.198 2.433a2.242 2.242 0 0 0-1.022.215l-16.5 7.666c-.509.236-.842.505-.842.505s1.842 5.001 2.128 5.523a.429.429 0 0 0 .286.126c.121-.044 6.147-4.34 6.147-4.34s4.018 5.667 6.23 8.092c.098.114 2.172-.685 2.172-.685l4.8-13.638c.162-.47.165-1.214-.203-1.68a2.204 2.204 0 0 0-1.197-.683z"
              /></svg
            >
          </a>
          <a
            href="https://youtube.com/channel/UCfBge76eIh41EcvGkd3ZgjQ"
            target="_blank"
            class="social-link"
            title="YouTube"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              ><path
                d="M22.54 6.42a2.78 2.78 0 0 0-1.94-2C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 0 0-1.94 2A29 29 0 0 0 1 11.75a29 29 0 0 0 .46 5.33A2.78 2.78 0 0 0 3.4 19c1.72.46 8.6.46 8.6.46s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-2 29 29 0 0 0 .46-5.25 29 29 0 0 0-.46-5.33z"
              ></path><polygon
                points="9.75 15.02 15.5 11.75 9.75 8.48 9.75 15.02"
              ></polygon></svg
            >
          </a>
        </div>
      </div>

      <nav class="footer-nav">
        <div class="footer-links">
          <h4>Links</h4>
          <ul>
            <li><Link to="/">Home</Link></li>
            <li><Link to="/encontros">Encontros</Link></li>
            <li><Link to="/eventos">Eventos</Link></li>
            <li><Link to="/podcast">Podcast</Link></li>
            <li><Link to="/donate">Donativos</Link></li>
            <li><Link to="/parceiros">Parceiros</Link></li>
            <li>
              <a
                href="https://drive.google.com/drive/folders/1mMUwPTEKuXz5D3DX4IwbnJLoh3rd-J5g?usp=sharing"
                target="_blank">Recursos</a
              >
            </li>
          </ul>
        </div>

        <div class="footer-connect">
          <h4>Conecte-se</h4>
          <ul>
            <li>
              <a
                href="https://amboss.space/node/028873425462e0addf3ad8a2f3ae72ef23b4ea4165d9739134b3ff1a86a0a8eb00"
                target="_blank"
                class="node-link"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  ><path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" /></svg
                >
                LN Node
              </a>
            </li>
          </ul>
        </div>
      </nav>
    </div>

    <div class="footer-bottom">
      <div class="copyright">
        <span>© {new Date().getFullYear()} aceitabitcoin.pt</span>
      </div>
      <div class="credits">
        Made with ♥ by
        <a href="https://twitter.com/talvasconcelos" target="_blank"
          >talvasconcelos</a
        >
        and
        <a href="https://twitter.com/Arminduhh" target="_blank">abjecto</a>
      </div>
    </div>
  </div>
</footer>

<style>
  .footer-section {
    margin-top: 4rem;
    background: #f8f9fa;
    color: #4a5568;
    padding: 4rem 0 0;
  }

  .footer-content {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .footer-main {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 4rem;
  }

  .footer-brand h3 {
    color: #1a202c;
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
  }

  .footer-brand p {
    color: #4a5568;
    line-height: 1.6;
    margin-bottom: 2rem;
  }

  .social-links {
    display: flex;
    gap: 1rem;
  }

  .social-link {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 8px;
    background: rgba(0, 0, 0, 0.05);
    color: #4a5568;
    transition: all 0.2s ease;
  }

  .social-link:hover {
    background: #2563eb;
    color: white;
    transform: translateY(-2px);
  }

  .footer-nav {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }

  .footer-nav h4 {
    color: #1a202c;
    font-size: 1.125rem;
    font-weight: 600;
    margin-bottom: 1.25rem;
  }

  .footer-nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .footer-nav li {
    margin-bottom: 0.75rem;
  }

  .footer-nav a {
    color: #4a5568;
    text-decoration: none;
    transition: color 0.2s ease;
  }

  .footer-nav a:hover {
    color: #2563eb;
  }

  .node-link {
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .node-link svg {
    color: #2563eb;
  }

  .footer-bottom {
    border-top: 1px solid rgba(0, 0, 0, 0.1);
    padding: 2rem 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #718096;
    font-size: 0.875rem;
  }

  .footer-bottom a {
    color: #2563eb;
    text-decoration: none;
    transition: color 0.2s ease;
  }

  .footer-bottom a:hover {
    color: #1d4ed8;
  }

  @media (max-width: 768px) {
    .footer-main {
      grid-template-columns: 1fr;
      gap: 3rem;
    }

    .footer-nav {
      grid-template-columns: 1fr;
    }

    .footer-bottom {
      flex-direction: column;
      text-align: center;
      gap: 1rem;
    }
  }

  @media (max-width: 640px) {
    .footer-section {
      padding: 3rem 0 0;
    }

    .social-links {
      justify-content: center;
    }

    .footer-brand {
      text-align: center;
    }
  }
</style>
