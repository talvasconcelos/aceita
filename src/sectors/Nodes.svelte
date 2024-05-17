<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="full-node" title="O que é um nó (node)?">
  <p>
    Um nó é apenas um computador que está a executar o programa Bitcoin. Mais
    importante ainda, está ligado a outros computadores (executando o mesmo
    programa) para criar uma Rede.
  </p>
</Section>
<Section hashtag="o-que-faz-node" title="O que faz um nó?">
  <p>O nó tem 3 funções:</p>
  <ul>
    <li>garantir o cumprimento das regras</li>
    <li>partilhar informação</li>
    <li>manter uma cópia das transacções confirmadas</li>
  </ul>
  <p>
    <strong>1. Garantir o cumprimento das regras</strong>
    <br />
    Cada nó (cliente bitcoin) foi programado para seguir um conjunto de regras. Seguindo
    estas regras, um nó é capaz de verificar as transacções que recebe e só as retransmite
    se tudo estiver bem. Se houver algum problema, a transacção não é transmitida.
  </p>
  <p>
    Por exemplo, uma regra é que uma pessoa deve possuir uma quantidade igual ou
    maior de bitcoin do que aquele que está a tentar enviar. Assim, se o seu nó
    receber uma transacção em que alguém tenha tentado enviar mais bitcoin do
    que aquele que possui, a transacção não será transmitida a outros nós.
  </p>
  <p>
    <strong>2. Partilhar informação</strong>
    <br />
    A principal função de um nó é partilhar informação com outros nós, e a informação
    quintessencial que um nó partilha são as transacções.
    <br />
    Agora, há dois tipos de transacções que os nós partilham:
  </p>
  <ul>
    <li>transacções novas - transacções que entraram recentemente na rede.</li>
    <li>
      transacções confirmadas - transacções que tenham sido "confirmadas" e
      escritas num ficheiro. Estas são partilhadas em blocos de transacções, e
      não individualmente.
    </li>
  </ul>
  <p>
    Não se preocupe com a diferença entre as duas, por agora. Mais à frente
    falaremos sobre a Mineração e sobre os Blocos.
  </p>
  <p>
    <strong>3. Manter uma cópia das transacções confirmadas</strong>
    <br />
    Como mencionado, cada nó também mantém blocos de transacções confirmadas. Estes
    são mantidos juntos num ficheiro chamado a Blockchain.
  </p>
  <p>
    Transacções recentes são propagadas pela rede até serem adicionadas à
    blockchain, que é um livro-razão de transacções confirmadas. Cada nó tem uma
    cópia da blockchain em segurança, e partilha-a com outros nós se a sua cópia
    não estiver actualizada.
    <br />
    Ao processo de adicionar novas transacções à blockchain, chama-se Mineração.
  </p>
  <p>
    De mencionar que cada nó é autónomo. Isto quer dizer que quando se gere um
    cliente bitcoin, a rede não "lhe diz o que fazer". Em vez disso, o seu
    cliente bitcoin já sabe o que fazer, e toma as suas próprias decisões.
    Assim, toda a rede de bitcoin é constituída por nós que tomam as suas
    próprias decisões, mas cada um deles toma as mesmas decisões que o outro, o
    que faz dela uma rede completamente descentralizada mas poderosa. Se todos
    os outros nós ficassem offline, o seu nó estaria a sustentar toda a rede de
    bitcoin.
  </p>
</Section>
<Section
  hashtag="tenho-que-ter-no"
  title="Tenho que ter/ser um nó para usar Bitcoin?"
>
  <p>
    Não. Pode enviar e receber bitcoin sem ter de ser um nó. Só precisa de
    enviar a transacção para a rede Bitcoin.
    <br />
    Se estiver a utilizar uma carteira web, por exemplo, eles irão enviar para a
    rede as transacções feitas por si.
  </p>
</Section>
