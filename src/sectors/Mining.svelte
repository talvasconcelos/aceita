<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="o-que-mineracao-bitcoin" title="O que é a Mineração?">
  <p>
    Mineração é simplesmente o processo de adicionar transacções à blockchain.
  </p>
</Section>
<Section hashtag="como-funciona-mining" title="Como funciona?">
  <p>
    Cada nó da rede Bitcoin partilha informação sobre novas transacções.
    Armazenam estas transacções na sua mempool.
  </p>
  <p>
    Cada nó tem também a opção de tentar "minar" as transacções no seu mempool
    para um ficheiro. Este ficheiro é um livro-razão de cada transacção de
    bitcoin, e é chamado de blockchain.
  </p>
  <p class="note tip">
    Pode pensar-se no mempool como transacções "em espera" e a blockchain como
    transacções "arquivadas".
  </p>
  <p>
    No entanto, para adicionar transacções do mempool à blockchain, um nó tem de
    usar muito poder de processamento informático. Este poder de processamento é
    forçado através da existência de um <i>desafio</i> no mempool.
  </p>
</Section>
<Section hashtag="desafio-mempool" title="Que desafio é esse?">
  <p>
    Ok, imagine que é um nó. A qualquer momento, pode condensar as transacções
    no mempool numa única "sequência" de números e letras, um hash.
  </p>
  <p>
    Agora, o seu objectivo é criar um hash desta sequência com um outro número
    para tentar obter uma nova sequência que comece com um <strong
      >certo número de zeros</strong
    >.
  </p>
  <p>
    Isto parece suficientemente fácil, mas na realidade é difícil. É totalmente
    aleatório, e só se pode esperar encontrar um resultado vencedor através de
    tentativa e erro. E é isso que a Mineração é - muito "hashing" (usando muito
    do poder de processamento do seu computador) e esperança de ter sorte. Mas
    se tiver a sorte de encontrar um resultado de hash bem sucedido, as
    transacções na sua mempool são adicionadas à blockchain, e cada outro nó da
    rede adiciona o seu bloco de transacções à sua blockchain.
    <br />
    Receberá também uma recompensa de 6.25 BTC (à data deste guia) pelo seu esforço,
    bem como quaisquer taxas que tenham sido aplicadas às transacções que acabou
    de adicionar à blockchain.
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
