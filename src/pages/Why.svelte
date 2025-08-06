<script>
  import Bullet from "../components/Bulletpoint.svelte";
</script>

<section class="why-section">
  <div class="container grid-lg">
    <header class="section-header">
      <h2>Porquê aceitar Bitcoin</h2>
      <div class="subtitle">
        <p>Porque devo aceitar Bitcoin no meu negócio?</p>
      </div>
    </header>

    <div class="content-section">
      <div class="intro-section">
        <h3>Adopção de Bitcoin</h3>
        <p class="intro-text">
          Desde a sua criação, Bitcoin tem vindo a captar a atenção de milhões
          de pessoas em todo o mundo. A adopção desta nova forma de dinheiro
          está longe de estar a abrandar. Pelo contrário, a rede Bitcoin tem
          vindo a crescer a um ritmo incrível e muitos salientam que a sua curva
          de adopção pode ser comparada à curva de adopção da Internet.
        </p>
        <p class="intro-text">
          A Internet proporcionou-nos uma forma de transferir informação
          globalmente e a Bitcoin é simplesmente uma forma de transferir valor
          globalmente sem a necessidade de intermediários. O Bitcoin está aqui
          para ficar, não fique para trás!
        </p>
      </div>

      <div class="reasons-section">
        <h3>Porque devo então aceitar pagamentos em bitcoin?</h3>
        <Bullet bullet="Maior Segurança">
          A rede Bitcoin existe há 13 anos, período durante o qual nunca foi
          pirateada com sucesso. Ouviu correctamente, nunca foi pirateada. Pode
          ter ouvido falar de hacks neste espaço, mas estes não estão associados
          à rede Bitcoin, são muito provavelmente outras moedas criptográficas
          que tentam replicar a Bitcoin. A rede é a tecnologia mais segura que
          temos para transacções a nível mundial.
        </Bullet>
        <Bullet bullet="Maior Rapidez">
          Com a adição da Lightning Network, uma nova tecnologia de 2ª camada
          (Layer 2) que facilita pagamentos instantâneos em Bitcoin e fiat,
          comerciantes e clientes podem aceder a pagamentos seguros e sem
          fricções de todo o mundo em segundos.
        </Bullet>
        <Bullet bullet="Mais Barato">
          Como comerciante, o incentivo para fazer a transição dos seus clientes
          para pagamentos Bitcoin é enorme. Ao contrário das empresas de cartões
          de crédito, que cobram taxas de 2-3% por cada transacção pela qual o
          comerciante é responsável e que demoram vários dias a serem
          liquidadas, a Lightning Network está a permitir que os comerciantes
          liquidem transacções instantaneamente por quase nada (por vezes menos
          de um cêntimo).
        </Bullet>
        <Bullet bullet="Mais Global">
          Bitcoin não tem fronteiras, permitindo-lhe aceitar pagamentos de
          clientes de todo o mundo com hipótese de converter instantaneamente
          esses pagamentos na sua moeda local sem necessidade de guardar
          qualquer Bitcoin. Mais clientes, menos custos. Todos ganham, excepto
          os bancos.
        </Bullet>
        <Bullet bullet="Mais Cool">
          Por último, mas não menos importante, Bitcoin é "fixe". À medida que
          mais e mais pessoas adoptam Bitcoin, elas procuram vendedores que lhes
          permitam utilizar Bitcoin como método de pagamento e evitar que tenham
          de converter a sua Bitcoin em moedas normais (fiat). Seja esse
          fornecedor. Aceitar pagamentos com Bitcoin permite-lhe promover o seu
          negócio como "Bitcoin friendly", atrair um segmento crescente de
          clientes e mostrar o seu negócio como orientado para o futuro, global
          e para o cliente.
        </Bullet>
        <p>
          Existem muitas formas de começar a aceitar Bitcoin no seu negócio.
          Quer seja um negócio online, uma loja fisíca, uma banca na praça, na
          feira, etc... Contacte-nos se precisar de ajuda!
        </p>
      </div>
    </div>
  </div>
</section>

<style>
  .why-section {
    padding: 4rem 0;
    background-color: #f8fafc;
  }

  .section-header {
    text-align: center;
    margin-bottom: 3rem;
  }

  .section-header h2 {
    font-size: 2.5rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 1rem;
  }

  .subtitle {
    max-width: 600px;
    margin: 0 auto;
  }

  .subtitle p {
    font-size: 1.25rem;
    color: #64748b;
    line-height: 1.6;
  }

  .content-section {
    max-width: 800px;
    margin: 0 auto;
  }

  .intro-section {
    margin-bottom: 3rem;
    padding: 2rem;
    background: white;
    border-radius: 12px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  }

  .intro-section h3 {
    color: #1a202c;
    font-size: 1.75rem;
    font-weight: 600;
    margin-bottom: 1.5rem;
  }

  .intro-text {
    color: #4a5568;
    line-height: 1.8;
    margin-bottom: 1.5rem;
    font-size: 1.125rem;
  }

  .intro-text:last-child {
    margin-bottom: 0;
  }

  .reasons-section {
    margin-top: 3rem;
  }

  .reasons-section h3 {
    color: #1a202c;
    font-size: 1.75rem;
    font-weight: 600;
    margin-bottom: 2rem;
  }

  @media (max-width: 640px) {
    .why-section {
      padding: 3rem 0;
    }

    .section-header {
      margin-bottom: 2rem;
    }

    .section-header h2 {
      font-size: 2rem;
    }

    .subtitle p {
      font-size: 1.125rem;
    }

    .intro-section {
      padding: 1.5rem;
      margin-bottom: 2rem;
    }

    .intro-section h3,
    .reasons-section h3 {
      font-size: 1.5rem;
    }

    .intro-text {
      font-size: 1rem;
    }
  }
</style>
