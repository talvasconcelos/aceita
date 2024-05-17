<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="rede-bitcoin" title="O que é a Rede Bitcoin?">
  <p>
    A Rede Bitcoin é composta por todos os que executam o software bitcoin (mais
    conhecido como "clientes bitcoin").
  </p>
</Section>
<Section hashtag="o-que-faz-a-rede" title="O que faz a Rede Bitcoin?">
  <p>
    As pessoas (ou melhor, os clientes bitcoin) da rede falam umas com as
    outras.
  </p>
  <p>
    E por "falar uns com os outros" quero dizer transmitir informação sobre o
    que se passa noutras partes da rede. Isto é feito através do envio de
    mensagens uns aos outros.
  </p>
  <p>
    Por exemplo, uma mensagem pode ser informação sobre uma nova transacção.
  </p>
  <p>
    Esta partilha de informação (por exemplo, transacções) é o que permite a
    todos na rede manterem-se actualizados, o que é bastante importante se
    quiserem gerir uma moeda digital na Internet.
  </p>
  <div class="note tip">
    <p>
      A Rede Bitcoin é descrita como uma rede ponto a ponto (peer-to-peer, ou
      P2P), porque:
    </p>

    <ul>
      <li>Todos estão ligados uns aos outros, por isso é uma rede</li>
      <li>Todos na rede são iguais, por isso são pares</li>
    </ul>
  </div>
</Section>
<Section hashtag="constituicao-rede-bitcoin" title="O que constitui a rede?">
  <p>
    Como mencionado, qualquer pessoa com uma ligação activa à Internet e a gerir
    um cliente bitcoin.
  </p>
  <p>
    <strong>Qualquer pessoa pode aderir à rede bitcoin.</strong> Só precisa de uma
    ligação à Internet e de um cliente Bitcoin, que é uma peça de software como qualquer
    outro.
  </p>
  <p>
    E assim que estiver instalado e a funcionar, será referido como um nó na
    rede Bitcoin.
  </p>
  <p class="note tip">
    O "<strong>certo número de zeros</strong>" provém da dificuldade. Isto é
    estabelecido pela rede e muda com base no volume dos mineiros - quanto mais
    pessoas mineram, mais poder de processamento, maior a dificuldade e mais
    zeros são necessários no início (o que torna mais difícil encontrar um
    resultado vencedor).
  </p>
  <p>
    Esta é uma versão bastante simplificada de como os blocos são adicionados à
    blockchain. Para um pouco mais de detalhe, consulte a parte de Blocos.
  </p>
</Section>
<Section hashtag="para-que-mineracao" title="Porquê a mineração é necessária?">
  <p>
    Boa pergunta. Porque não adicionar transacções directamente à blockchain?
    Porque a mineração permite que toda a rede Bitcoin chegue a acordo sobre que
    transacções são "arquivadas", e é assim que se evita a fraude numa moeda
    digital.
  </p>
  <p>
    Quando se faz uma transacção de bitcoin, os nós da rede não ouvem falar dela
    instantaneamente. Em vez disso, as transacções viajam através da rede de
    bitcoin ao serem passadas de um nó para o outro.
  </p>
  <p>
    No entanto, é possível fazer outra transacção usando esse mesmo bitcoin (ou
    melhor, esses mesmos outputs) e inserir essa transacção também na rede. Por
    exemplo, poderia comprar uma cerveja com algum bitcoin, depois tentar
    comprar rapidamente uma fatia de pizza com esse mesmo bitcoin. Por outras
    palavras, fraude.
  </p>
  <p>
    Alguns nós obteriam primeiro a transacção da pizza (e ignorariam a
    transacção da cerveja), enquanto outros obteriam primeiro a transacção da
    cerveja (e ignorariam a transacção da pizza). No entanto, mesmo que se faça
    a transacção da pizza após a transacção da cerveja, devido à forma como as
    transacções viajam através da rede Bitcoin, a rede ficaria em desacordo
    sobre se se deve obter a cerveja ou a pizza.
  </p>
  <p>
    <strong>Como é que a rede decide qual q transacção correcta?</strong>
    Mineração, claro. Se um nó na rede completar o desafio, então são as transacções
    no seu mempool que são adicionadas à blockchain.
  </p>
  <p class="note tip">
    Se um nó com a transacção da pizza mina com sucesso um bloco, então é essa a
    transacção que é adicionada à blockchain, e a transacção da cerveja
    evapora-se da rede.
  </p>
  <p>
    Parece uma forma pouco ortodoxa de seleccionar transacções mas, esta é a
    solução que a rede Bitcoin utiliza para chegar a um consenso quando se lida
    com informações contraditórias.
  </p>
  <p>
    Pelo lado positivo, demora apenas cerca de 10 minutos para que cada novo
    bloco de transacções seja adicionado à blockchain, pelo que só é preciso
    esperar 10 minutos por uma confirmação de que as bitcoins "chegaram" a um
    novo endereço (e não foram enviadas para um endereço alternativo).
  </p>
</Section>
<Section
  hashtag="outro-beneficio-mineracao"
  title="Outro benefício da mineração"
>
  <p>
    Se quiser tentar controlar os blocos (ou seja, as transacções) que são
    adicionados à blockchain, tem de competir para resolver os puzzles de blocos
    com todos os outros nós mineiros da rede bitcoin.
  </p>
  <p>
    Por outras palavras, é preciso ter um computador com poder de processamento
    suficiente que seja capaz de ultrapassar o poder de processamento combinado
    de qualquer outro mineiro de bitcoin.
  </p>
  <p>
    O que é inteiramente possível - basta gastar alguns milhares de milhões de
    euros em hardware e está pronto para começar (embora este número aumente com
    cada novo mineiro que se junte à rede).
  </p>
</Section>
