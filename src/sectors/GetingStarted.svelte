<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="bitcoin-core" title="Bitcoin Core">
  <p>
    A melhor maneira de começar com Bitcoin é instalar o Bitcoin Core. Bitcoin
    Core é o programa original criado por Satoshi Nakamoto em 2009.
  </p>
  <div>
    <a
      class="btn btn-primary btn-large"
      href="https://bitcoin.org/en/download"
      target="_blank"
      rel="noopener noreferrer">Download Bitcoin</a
    >
  </div>
  <br />
  <p>
    Ao executar o programa, este ligar-se-á a outras pessoas que executem o
    mesmo programa, criando uma rede de computadores que comunicam uns com os
    outros.
  </p>
  <p>
    A primeira vez que executar o Bitcoin Core, começará a descarregar um
    ficheiro a partir dos outros nós da rede. Este ficheiro chama-se <strong
      ><a href="#">blockchain</a></strong
    >, e é um grande ficheiro de transacções.
  </p>
  <p>
    Uma vez descarregada e verificada a blockchain completa (actualmente cerca
    de 500 GB), pode começar a fazer as suas próprias transacções, que se
    propagam na rede e são escritas na blockchain no computador de todos. Isto é
    o básico de Bitcoin!
  </p>
</Section>
<Section hashtag="carteiras-bitcoin" title="Carteiras Bitcoin">
  <p>
    O requisito de executar o Bitcoin Core é que é necessário descarregar e
    armazenar a blockchain completa. Isto é uma coisa boa, porque cria uma cópia
    extra da blockchain, e está a ajudar a retransmitir as transacções para
    outros computadores também.
  </p>
  <p>
    No entanto, nem todos têm espaço no disco rígido para armazenar a sua
    própria cópia da blockchain.
  </p>
  <p>
    Assim, em vez de correr o Bitcoin Core, pode usar algo chamado "carteira" de
    bitcoin. As carteiras permitem-lhe enviar e receber "bitcoins", mas sem
    precisar da sua própria cópia da blockchain.
  </p>
  <p>
    Se preferir não correr um nó completo (full node), uma carteira de bitcoin é
    a forma mais fácil de começar com Bitcoin.
  </p>
  <p>
    <strong
      >Qual a desvantagem de usar uma carteira em vez de correr o Bitcoin Core?</strong
    >
    <br />
  </p>
  <ul>
    <li>
      <strong>Bitcoin Core: </strong>Tem uma cópia de todas as transacções
      alguma vez feitas. Portanto, pode verificar cada transacção que recebe e
      visualizá-las no seu próprio computador, sem a necessidade de confiar em
      mais ninguém.
    </li>
    <li>
      <strong>Carteira Bitcoin: </strong>A carteira precisa de se ligar a um nó
      para obter informações sobre a transacção. Assim, confia na carteira para
      se ligar a um nó honesto a fim de obter os detalhes correctos da
      transacção.
    </li>
  </ul>
  <p>
    Usar uma carteira é a forma mais conveniente de usar o bitcoin, mas correr
    um nó completo é a forma de usar o bitcoin sem ter de confiar em ninguém.
    Ou, se preferir, pode utilizar os dois métodos... A escolha é sua.
  </p>
</Section>
<Section hashtag="qual-carteiras-bitcoin" title="Que carteira devo usar?">
  <p>
    Bitcoin é um programa de código aberto, por isso qualquer pessoa pode criar
    a sua própria carteira. Deixo aqui algumas recomendações para começar:
  </p>
  <ul>
    <li>
      <strong>Desktop: </strong>
      <span
        ><a
          href="https://electrum.org/"
          target="_blank"
          rel="noopener noreferrer">Electrum</a
        ></span
      >
    </li>
    <li>
      <strong>Android: </strong>
      <span
        ><a
          href="https://samouraiwallet.com/"
          target="_blank"
          rel="noopener noreferrer">Samourai</a
        ></span
      >
    </li>
    <li>
      <strong>iOS: </strong>
      <span
        ><a
          href="https://blockstream.com/green/"
          target="_blank"
          rel="noopener noreferrer">Green</a
        ></span
      >
    </li>
  </ul>
  <p>
    Mas, qualquer um pode criar uma carteira de bitcoin, por isso certifique-se
    de que a que usa é fiável (e não apenas a mais bonita).
  </p>
</Section>
<Section hashtag="o-faz-a-carteira" title="O que faz uma carteira?">
  <p>
    Quando se começa a usar pela primeira vez uma carteira de bitcoin, esta
    dar-lhe-á uma semente (seed). Esta semente é uma lista gerada aleatoriamente
    de 12-24 palavras que mais ninguém no mundo alguma vez viu.
  </p>
  <p>
    A sua seed é única, e é utilizada para criar todos os endereço na sua
    carteira.
  </p>
  <ul>
    <li>
      Um endereço é o que se dá às pessoas para que possam receber bitcoins.
    </li>
    <li>
      Cada endereço tem a sua própria chave privada, que é utilizada quando
      envia as suas moedas para outra pessoa.
    </li>
  </ul>
  <p>
    Em suma, uma carteira de bitcoin gere as suas chaves e endereços para que
    possa enviar e receber bitcoins.
  </p>
  <p class="note tip">
    <strong>Dica: </strong>Se perder a carteira, pode recuperar todas as suas
    chaves (e todo seu bitcoin) apenas com a sua semente.
  </p>
  <p class="note warning">
    <strong>Aviso: </strong>Mantenha a sua semente segura, e não a mostre a
    ninguém. Se alguém tiver a sua seed, pode aceder às suas moedas.
  </p>
</Section>
<Section hashtag="como-funciona-bitcoin" title="Como funciona o Bitcoin?">
  <p>
    Bitcoin é uma rede de computadores, e todos eles trabalham em conjunto para
    partilhar um ficheiro chamado blockchain. Pode-se pensar na blockchain como
    sendo um cofre gigante de caixas de segurança, onde cada uma destas caixas
    contém uma quantidade de bitcoin e um cadeado.
  </p>
  <p>
    Quando faz uma transacção, a sua carteira selecciona uma caixa de bitcoins
    da blockchain que lhe pertence, e cria uma nova caixa de bitcoins para a
    pessoa a quem quer enviar bitcoin. A sua carteira coloca o endereço da outra
    pessoa como cadeado da nova caixa, e utiliza a chave privada necessária para
    desbloquear a caixa de bitcoins que está actualmente bloqueada ao seu
    endereço.
  </p>
  <p>
    Por outras palavras, está a desbloquear o seu cofre de segurança, e a criar
    um novo cofre de segurança para outra pessoa. De qualquer modo, esta
    transacção (que é apenas um monte de dados) é enviada para um dos
    computadores da rede, onde é propagada de computador para computador até que
    todos na rede tenham uma cópia da sua transacção.
  </p>
  <p>
    Eventualmente, essa transacção chegará às blockchains de todos. Isto
    acontece porque um dos nós da rede recolhe as últimas transacções que
    recebeu para um bloco, e depois mina este bloco para o adicionar à
    blockchain (o que usa energia). Partilham então este novo bloco minado com
    os outros nós da rede, que o adicionam também à sua cópia da blockchain.
  </p>
  <p>
    Assim, a intervalos regulares, cada nó da rede irá actualizar a sua
    blockchain com as últimas transacções que foram enviadas para a rede. Este
    processo repete-se uma e outra vez, pelo que a blockchain está
    constantemente a crescer com novas transacções. De qualquer modo, uma vez
    que uma transacção chega à blockchain, esta não pode ser removida, o que
    significa que a transacção está completa, e os bitcoins mudaram de mãos. E é
    assim que Bitcoin funciona.
  </p>
  <p class="note tip">
    <strong>Nota: </strong>Reparou que uso <strong>B</strong>itcoin e
    <strong>b</strong>itcoin? Bitcoin (com B maiúsculo), significa a rede, o
    protocolo e bitcoin (com b minúsculo), refere-se à moeda ou token que é
    usado dentro da rede.
  </p>
</Section>
