<script>
  import Header from "../components/Header.svelte";
  import Feature from "../components/Feature.svelte";
</script>

<Header />
<section class="quote bg-gray">
  <div class="container grid-lg">
    <quote
      >A iniciativa <strong>Aceita Bitcoin</strong>, é um esforço conjunto, sem
      fins lucrativos, de um grupo de entusiastas e voluntários que pretendem um
      futuro melhor para <strong>Portugal</strong></quote
    >
  </div>
</section>
<section class="container grid-lg">
  <Feature
    title="Educação e Suporte"
    text="Os voluntários da iniciativa oferecem às comunidades locais as ferramentas e formação necessárias para transaccionar com Bitcoin, como criar e usar uma carteira, etc..."
    img="../images/suporte.svg"
    buttonText="Saber mais..."
    buttonURL="/como-funciona-bitcoin"
  />
  <Feature
    title="Adopção e Poupança"
    text="Promovemos a adopção de Bitcoin como sistema monetário alternativo. Bitcoin não só oferece uma excelente forma de pagamento como é uma poderosa tecnologia de poupança!"
    img="../images/adoption.svg"
    img_right
  />
  <Feature
    title="Eventos e Workshops"
    text="Estamos a organizar eventos e workshops por todo o país para dar a conhecer Bitcoin à população. O objectivo é desmistificar e informar sobre a tecnologia e como pode permitir uma economia mais inclusiva e sustentada na poupança e no crescimento."
    img="../images/educa_bitcoin.svg"
    buttonText="Ver Eventos"
    buttonURL="/eventos"
  />
</section>

<style>
  .quote {
    text-align: center;
    width: 100%;
    font-size: 1.2rem;
    font-weight: 300;
    padding: 1rem 0;
  }
  @media (min-width: 600px) {
    .quote {
      font-size: 1.5rem;
    }
  }
</style>
