<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="o-que-e-um-bloco" title="O que é um bloco?">
  <p>Um bloco é um conjunto de transacções que foi adicionado à Blockchain.</p>
</Section>
<Section hashtag="como-se-formam-blocos" title="Como se formam os blocos?">
  <p>Blocos são criados pelos mineiros.</p>
  <p>
    Quando se faz uma transacção de bitcoin, esta não é imediatamente adicionada
    à blockchain. Em vez disso, é mantido num pool de transacções (ou mempool).
  </p>
  <p>
    Se for um mineiro, o seu trabalho é recolher transacções do pool de
    transacções para um "candidato a bloco", e tentar adicionar esse bloco à
    blockchain.
  </p>
  <p>
    <strong>Cabeçalho do bloco</strong>
    <br />
    Também se pode dar a cada bloco candidato um cabeçalho, que é basicamente um
    monte de metadados sobre o bloco.
    <br />
    Os mineiros utilizam estes metadados quando tentam adicionar um bloco à blockchain.
  </p>
  <p>
    Os detalhes destes campos não são importantes para agora, mas aqui está uma
    rápida análise de qualquer maneira:
  </p>
  <ul>
    <li>
      Versão: descreve a estrutura dos dados no interior do bloco. É utilizada
      para que os computadores possam ler correctamente o conteúdo de cada
      bloco.
    </li>
    <li>
      Último bloco um número de identificação para o bloco anterior. Estamos a
      tentar obter um destes para o actual bloco candidato.
    </li>
    <li>
      Merkle Root: todas as transacções no interior do bloco se precipitaram
      para formar uma única linha de texto. Todos os campos são únicos, mas
      seria justo pensar nisto como a parte mais significativa do cabeçalho do
      bloco.
    </li>
    <li>Tempo (timestamp): a "hora" actual.</li>
    <li>
      Alvo: um valor com o qual os mineiros trabalham para tentar adicionar o
      bloco candidato à blockchain. É estabelecido pela rede de bitcoin, e fará
      mais sentido dentro de momentos.
    </li>
  </ul>
</Section>
<Section
  hashtag="adicionar-bloco-blockchain"
  title="como são os blocos adicionados à Blockchain?"
>
  <p>
    Para adicionar um bloco candidato à blockchain, tem que fazer um hash dos
    dados no cabeçalho do bloco e esperar que o resultado esteja abaixo de um
    determinado valor-alvo.
  </p>
  <p>
    O valor-alvo é calculado a partir da dificuldade, que é um valor
    estabelecido pela rede de Bitcoin para regular a dificuldade de adicionar um
    bloco de transacções à blockchain.
  </p>
  <p>
    Pense no alvo como o trave no limbo (a dança) dos blocos candidatos - quanto
    maior a dificuldade, mais baixo o alvo, e mais difícil é encontrar um hash
    de bloco que esteja abaixo deste valor.
  </p>
  <p>
    O <i>target</i> e a dificuldade são um pouco confusos de entender ao início,
    mas fará mais sentido com o tempo.
  </p>
  <p class="note tip">
    Dificuldade: um valor estabelecido pela rede Bitcoin que foi concebido para
    regular a rapidez com que os blocos são resolvidos. Ajusta-se a cada 2016
    blocos para tentar criar uma média de 10 minutos entre blocos.
  </p>
</Section>
