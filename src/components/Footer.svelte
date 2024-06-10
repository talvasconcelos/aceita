<script>
  import { Link } from "svelte-navigator";
</script>

<footer>
  <div class="hero bg-gray">
    <div class="hero-body container grid-lg">
      <div class="columns">
        <div class="column col-6 col-sm-12">
          <h3 class="text-secondary">Aceita Bitcoin</h3>
          <p>
            Bitcoin é uma rede que funciona de forma consensual onde foi
            possível criar uma nova forma de pagamento e também uma nova moeda
            completamente digital.
          </p>
        </div>
        <div class="column col-3 col-sm-6 col-xs-12 links">
          <h5>Links</h5>
          <dl class="list list_custom">
            <dd><Link to="/">Home</Link></dd>
            <dd><Link to="/encontros">Encontros</Link></dd>
            <dd><Link to="/eventos">Eventos</Link></dd>
            <dd><Link to="/podcast">Podcast</Link></dd>
            <dd><Link to="/donate">Donativos</Link></dd>
            <dd><Link to="/apoiantes">Apoiantes</Link></dd>
            <dd>
              <a
                href="https://drive.google.com/drive/folders/1mMUwPTEKuXz5D3DX4IwbnJLoh3rd-J5g?usp=sharing"
                target="_blank">Recursos</a
              >
            </dd>
            <!-- <dd>
              <a
                class="tooltip"
                data-tooltip="Para onchain contacte-nos"
                href="https://wallet.sparkpay.pt/lnurlp/5"
                target="_blank">Donativos</a
              >
            </dd> -->
          </dl>
        </div>
        <div class="column col-3 col-sm-6 col-xs-12 links">
          <h5>Contactos</h5>
          <dl class="list list_custom">
            <dd>
              <a
                class="tooltip"
                data-tooltip="geral@aceitabitcoin.pt"
                href="mailto:geral@aceitabitcoin.pt">Email</a
              >
            </dd>
            <dd>
              <a href="https://twitter.com/aceitabitcoinpt" target="_blank"
                >Twitter</a
              >
            </dd>
            <dd>
              <a href="https://t.me/aceitabitcoin" target="_blank">Telegram</a>
            </dd>
            <dd>
              <a
                href="https://youtube.com/channel/UCfBge76eIh41EcvGkd3ZgjQ"
                target="_blank">Youtube</a
              >
            </dd>
            <dd>
              <a
                href="https://amboss.space/node/028873425462e0addf3ad8a2f3ae72ef23b4ea4165d9739134b3ff1a86a0a8eb00"
                target="_blank">LN Node</a
              >
            </dd>
          </dl>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container grid-lg">
        <span>2021 aceitabitcoin.pt</span>
        <span class="float-right"
          >Made by <a href="https://twitter.com/talvasconcelos" target="_blank"
            >talvasconcelos</a
          >
          and
          <a href="https://twitter.com/Arminduhh" target="_blank">abjecto</a>
        </span>
      </div>
    </div>
  </div>
</footer>

<style>
  footer {
    margin-top: 4rem;
  }
  .hero {
    padding-bottom: 0;
  }
  h3 {
    font-size: 1.15rem;
    font-weight: bold;
  }
  .links {
    text-align: center;
    margin-top: 1rem;
  }
  .footer-bottom {
    width: 100%;
    font-size: 0.75rem;
    margin-top: 1rem;
    padding: 1rem 0;
  }
  @media (min-width: 480px) {
    .links {
      text-align: left;
      margin-top: 0;
    }
  }
</style>
