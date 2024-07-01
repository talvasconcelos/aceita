<script>
  import EventCard from "../components/EventCard.svelte";
</script>

<section class="container grid-lg">
  <header>
    <h2>Eventos</h2>
    <div class="subtitle">
      <p>Descubra os eventos perto de si</p>
    </div>
  </header>
  <div class="card-grid">
    <EventCard
      title="Peniche - A.E.F.C.R.P."
      subtitle="Workshop Bitcoin para comércio local"
      address="A.E.F.C.R.P., Av. das Escolas, 2520-294 Peniche"
      date="Maio"
      time="17h - 19h"
      img={null}
      description="Workshop para explicar os fundamentos de Bitcoin e como este novo sistema monetário pode fazer mais por Peniche."
      signinUrl={null}
      btnText="Saber Mais"
    />
    <EventCard
      title="Óbidos"
      subtitle="Bitcoin - Moeda Universal"
      address="Parque Tecnológico Óbidos, Edifícios Centrais, Rua da Criatividade, 2510-216 Óbidos"
      date="28 Abril 2022"
      time="11h - 13h"
      img={null}
      description="Sessão/debate, em formato híbrido, para explicar os fundamentos de Bitcoin: o que é o dinheiro, como funciona esta moeda digital e como se transacciona, por que razão é tão interessante e que dimensões resolve."
      signinUrl={null}
      btnText="Saber Mais"
    />
    <EventCard
      title="Caldas da Rainha"
      subtitle="Workshop Bitcoin e Prontos."
      address="Avenida Primeiro de Maio, 20 A, 2500-081 Caldas da Rainha"
      date="23 Março"
      time="18h - 20h"
      img="images/events/ev_04.jpg"
      description="Workshop Bitcoin na Prontos em Caldas da Rainha. Metade do valor da inscrição é reembolsada em bitcoin no dia do evento. Venha conhecer Bitcoin e a Lightning Network!"
      signinUrl="https://forms.gle/djycWjpaeUsip6ot8"
      btnText="Saber Mais"
    />
    <EventCard
      title="Viseu"
      subtitle="Workshop Bitcoin & Lightning Network"
      date="27 Novembro"
      time="14h - 19h"
      img="images/events/workshop_viseu_2021.jpg"
      description="Venha conhecer o que é Bitcoin, como funciona e como pode começar a usar, para fazer e receber pagamentos"
      signinUrl="https://docs.google.com/forms/d/12OEC3sFbmnPR6XwABOPJUQvVTMrfrXKv4i8U_e-qamI"
    />
    <EventCard
      title="Madeira"
      subtitle="Bitcoin Atlantis - Bem-vindo ao Bitcoin"
      date="29 Fevereiro"
      time="9h - 17h"
      img="images/events/CCIF.jpg"
      description="Descobre o fascinante universo do Bitcoin no evento “Bem-vindo ao Bitcoin”, uma iniciativa da F.R.E.E. Madeira, em parceria com o grupo Aceita Bitcoin."
      signinUrl="https://bitcoinatlantis.com/bem-vindo-ao-bitcoin"
      btnText="Saber Mais"
    />
  </div>
</section>

<style>
  header {
    margin-bottom: 3rem;
  }
  .card-grid {
    display: block;
  }
  @media (min-width: 600px) {
    .card-grid {
      display: grid;
      gap: 1rem;
      grid-template-columns: repeat(auto-fill, minmax(35%, 1fr));
    }
  }
  @media (min-width: 1280px) {
    .card-grid {
      display: grid;
      gap: 1rem;
      grid-template-columns: repeat(auto-fill, minmax(25%, 1fr));
    }
  }
</style>
