<article>
  <p>
    Bitcoin é um sistema de pagamento electrónico criado em 2009. Permite-lhe
    enviar dinheiro para qualquer pessoa no mundo, e não precisa de pedir
    permissão a ninguém para criar uma conta. Foi criado como uma solução para o
    sistema financeiro moderno, onde temos um pequeno número de grandes bancos
    que controlam quem obtém uma conta e quais as transacções que são
    processadas. Isto significa que o controlo do dinheiro é centralizado, e
    temos de confiar nos bancos para agir de forma responsável.
  </p>
  <p>
    A centralização da banca e a consequente crise financeira de 2007 inspiraram
    o desenvolvimento de Bitcoin. É um sistema de pagamento, e funciona sem um
    ponto central de controlo. Foi concebido de forma anónima por Satoshi
    Nakamoto, e foi <a
      href="https://www.metzdowd.com/pipermail/cryptography/2009-January/014994.html"
      target="_blank">lançado em Janeiro de 2009</a
    >. Qualquer pessoa pode executar o programa ou utilizar o sistema.
  </p>
  <h5 id="o-que-e-bitcoin">O que é Bitcoin</h5>
  <p>
    Bitcoin é simplesmente um programa de computador. Você pode fazer o download
    e instalar no seu computador.
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
    Quando executar o programa, este ligar-se-á a outros computadores que também
    estejam a executar este programa, e eles começarão a partilhar um ficheiro
    consigo. Este ficheiro chama-se blockchain, e é basicamente uma grande lista
    de transacções.
  </p>
  <p>
    Quando uma nova transacção entra na rede, é propagada de computador para
    computador até que todos tenham uma cópia da transacção. Em intervalos de
    aproximadamente 10 minutos, um computador (nó ou node) aleatório na rede
    adicionará as últimas transacções recebidas à blockchain, e partilhará as
    actualizações com todas as outras pessoas, ou melhor todos os outros nós, na
    rede.
  </p>
  <p>
    Como resultado, o programa Bitcoin cria uma grande rede de computadores que
    comunicam uns com os outros para partilhar um ficheiro e actualizá-lo com
    novas transacções.
  </p>
  <h5 id="o-que-bitcoin-resolve">
    Para que precisamos de Bitcoin? O que resolve?
  </h5>
  <p>
    Era possível retransmitir transacções através de uma rede de computadores
    antes do Bitcoin. No entanto, o problema é que é possível inserir
    transacções conflituosas numa rede de computadores. Por exemplo, pode criar
    duas transacções separadas que gastam a mesma moeda digital, e enviar ambas
    as transacções para a rede ao mesmo tempo. Isto é conhecido como um "gasto
    duplo".
  </p>
  <p>
    Assim, criar um sistema de pagamento electrónico sem um ponto central de
    controlo, tem o problema de descobrir qual destas transacções veio
    "primeiro", e isto é uma coisa difícil de fazer quando se tem uma rede de
    computadores todos a agir independentemente. Alguns computadores receberão
    primeiro a transacção A, e alguns computadores receberão primeiro a
    transacção B. Quem decidirá qual deles veio "primeiro" e deverá ser o único
    a ser escrito no ficheiro? Bitcoin resolve este problema forçando os nós a
    manter todas as transacções que recebem na memória antes de as escreverem
    num ficheiro. Depois, a intervalos de 10 minutos, um nó aleatório na rede
    adicionará as transacções da sua memória ao ficheiro.
  </p>
  <p>
    Este ficheiro actualizado é então partilhado com a rede, e os nós aceitarão
    as transacções no ficheiro actualizado como "correctas", removendo quaisquer
    transacções conflituosas da sua memória. Como resultado, nenhuma transacção
    de duplicação de despesas será jamais escrita no ficheiro, e todos os nós
    podem actualizar os seus ficheiros de acordo uns com os outros.
  </p>
  <p>
    O processo de adicionar transacções ao ficheiro chama-se mineração, e é
    basicamente uma concorrência a nível da rede que não pode ser controlada por
    um único nó na rede.
  </p>
  <h5 id="como-funciona-mineracao">Como funciona a mineração</h5>
  <p>
    Para começar, cada nó armazena as últimas transacções que recebeu na sua
    reserva de memória (mempool), que é apenas memória temporária no seu
    computador. Qualquer nó pode então tentar extrair as transacções do seu
    mempool para o ficheiro (a blockchain). Para o fazer, um nó reunirá as
    transacções do seu mempool num recipiente chamado bloco, e depois utilizará
    o poder de processamento para tentar adicionar este bloco de transacções à
    blockchain.
  </p>
  <p>
    Então, onde é que entra o poder de processamento? Bem, para adicionar este
    bloco à blockchain, é necessário alimentar o seu bloco de transacções com
    algo chamado função hash. Uma função hash é basicamente um miniprograma de
    computador que irá receber qualquer quantidade de dados, codificá-los, e
    devolver um número completamente aleatório (mas único). Uma impressão
    digital daqueles dados.
  </p>
  <p>
    Para que o seu bloco seja adicionado com sucesso à blockchain, este número
    (o hash do bloco) deve estar abaixo do alvo, que é um número limite com o
    qual todos na rede concordam.
  </p>
  <p>
    Se o seu hash de bloco resultante não estiver abaixo do alvo, pode fazer um
    pequeno ajuste aos dados dentro do bloco e colocá-lo novamente através da
    função de hash. Isto produzirá um número completamente diferente que se
    espera que esteja abaixo do alvo. Caso contrário, ajustará o bloco e tentará
    de novo.
  </p>
  <p>
    Em resumo, o processo de mineração utiliza o poder de processamento para
    realizar cálculos de hash o mais rápido possível para tentar ser o primeiro
    computador na rede a obter um hash de bloco abaixo do alvo. Se tiver
    sucesso, pode adicionar o seu bloco de transacções à blockchain e
    partilhá-lo com o resto da rede.
  </p>
  <p>
    <small
      >Nota: Embora ainda seja possível a qualquer pessoa tentar a mineração, já
      não é competitivo fazê-lo num computador doméstico. Existe agora hardware
      especializado que foi concebido para efectuar cálculos de hash o mais
      rápido (e eficientemente) possível, o que significa que a exploração
      mineira é agora maioritariamente executada por quem tem acesso a hardware
      especializado e electricidade barata.</small
    >
  </p>
  <h5 id="onde-vem-bitcoin">De onde vêm os bitcoins?</h5>
  <p>
    Como incentivo à utilização do poder de processamento para tentar adicionar
    novos blocos de transacções à blockchain, cada novo bloco disponibiliza uma
    quantidade fixa de bitcoins que não existia anteriormente. Portanto, se for
    capaz de "extrair" com sucesso um bloco, poderá "enviar" a si próprio estas
    novas bitcoins como recompensa pelo seu esforço.
  </p>
  <p>
    Esta recompensa de novas bitcoins é chamada a <strong
      >recompensa do bloco</strong
    >, e é a razão pela qual o processo é chamado de "mineração".
  </p>
  <h5 id="blockchain">
    Porque o ficheiro se chama cadeia de blocos, ou blockchain?
  </h5>
  <p>
    Como já vimos, as transacções não são adicionadas ao ficheiro
    individualmente - são recolhidas em conjunto e adicionadas em blocos. Cada
    um destes novos blocos constrói-se sobre um já existente, pelo que o
    ficheiro é constituído por uma cadeia de blocos; daí, a cadeia de blocos.
  </p>
  <p>
    Além disso, cada nó da rede adoptará sempre a cadeia mais longa de blocos
    que receber como a versão "oficial" da cadeia de blocos. Isto significa que
    os mineiros tentarão sempre construir em cima da "ponta" da blockchain mais
    longa conhecida, pois quaisquer blocos que não façam parte da cadeia mais
    longa não serão considerados válidos por outros nós.
  </p>
  <p>
    Portanto, se alguém quisesse reescrever a história das transacções, teria de
    reconstruir uma cadeia mais longa de blocos para criar uma <strong
      >nova</strong
    > cadeia mais longa para que outros nós a adoptassem. No entanto, para o conseguir,
    um único mineiro precisaria de ter mais poder de processamento informático do
    que o resto da rede combinada.
  </p>
  <p>
    Como resultado, o esforço combinado da rede torna difícil para qualquer
    indivíduo "ultrapassar" a rede e reescrever a blockchain.
  </p>
  <h5 id="transaccoes">Como funcionam as transacções</h5>
  <p>
    Pode pensar-se na blockchain como sendo um depósito para cofres, a que
    chamamos <strong>outputs</strong> . Estes outputs são apenas contentores que
    contêm várias quantidades de bitcoin.
  </p>
  <p>
    Quando efectua uma transacção de bitcoin, selecciona alguns outputs e
    desbloqueia-os, depois cria novos outputs e coloca-lhes novos bloqueios.
  </p>
  <p>
    Portanto, quando se "envia" bitcoins a alguém, está-se na realidade a
    colocar uma quantidade de bitcoins num novo cofre, e a colocar-lhe um
    cadeado que só a pessoa quem está a "enviar" os bitcoins pode desbloquear.
    <br />
    Por exemplo, se eu quisesse enviar-lhe algumas bitcoins, seleccionaria alguns
    outputs na blockchain que eu posso desbloquear, e criaria um novo output a partir
    deles que só você pode desbloquear. Além disso, se eu não quisesse enviar todas
    as bitcoins que eu tinha desbloqueado, criaria um output extra como o meu troco
    e trancava-o para mim próprio.
  </p>
  <p>
    Posteriormente, se quiser enviar as suas bitcoins para outra pessoa,
    repetiria o processo de selecção dos outputs existentes (que pode
    desbloquear) e de criação de novos outputs a partir deles. Como resultado,
    as transacções de bitcoins formam uma estrutura gráfica, onde o movimento
    das bitcoins está ligado por uma série de transacções.
  </p>
  <p>
    Finalmente, quando uma transacção é adicionada, ou minada, na blockchain, os
    outputs que foram usados (gastos) na transacção não podem ser utilizados
    noutra transacção, e os resultados recentemente criados estarão disponíveis
    para serem transferidos para uma transacção futura.
  </p>
  <h5 id="como-ter-bitcoin">Como se possuem as bitcoins?</h5>
  <p>
    Para poder "receber" bitcoins, precisa de ter o seu próprio conjunto de
    chaves. Este conjunto de chaves é como o seu número de conta e senha,
    excepto que em Bitcoin são chamadas a sua chave pública e a sua chave
    privada. Por exemplo, se eu quisesse enviar-lhe algumas bitcoins, precisaria
    primeiro de dar-me a sua chave pública. Quando crio a transacção, coloco a
    vossa chave pública dentro da fechadura no output (o cofre de depósito).
    Você depois, utilizaria a sua chave privada para desbloquear este output
    quando quisesse enviar as bitcoins para outra pessoa.
  </p>
  <p>
    Então onde se pode obter uma chave pública e privada? Bem, com a ajuda da
    criptografia pode, e deve, na verdade gerá-las você mesmo. Em suma, a sua
    chave privada é apenas um grande número aleatório, e a sua chave pública é
    um número calculado a partir desta chave privada. Mas a parte inteligente é
    que pode dar a sua chave pública a outra pessoa, mas esta não pode obter a
    chave privada a partir dela.
  </p>
  <p>
    Agora, quando pretende desbloquear moedas que são atribuídas à sua chave
    pública, utiliza a sua chave privada para criar aquilo a que se chama uma
    assinatura digital. Esta assinatura digital prova que é o proprietário da
    chave pública (e por isso pode desbloquear as bitcoins), sem ter de revelar
    a sua chave privada. Esta assinatura digital também só é válida para a
    transacção para a qual foi criada, pelo que não pode ser utilizada para
    desbloquear outras bitcoins bloqueadas à mesma chave pública.
  </p>
  <p>
    Este sistema é conhecido como <a
      href="https://pt.wikipedia.org/wiki/Criptografia_de_chave_p%C3%BAblica"
      target="_blank"
      rel="noopener noreferrer">"Criptografia de Chave Pública"</a
    >, e está disponível desde 1978. Bitcoin faz uso deste sistema para permitir
    a qualquer pessoa criar chaves para enviar e receber bitcoins com segurança,
    sem necessidade de uma autoridade central para emitir contas e passwords.
  </p>
  <h5 id="juntando-as-pecas">Juntando as peças</h5>
  <p>
    Para começar com o bitcoin, gera a sua própria chave privada e a chave
    pública. A sua chave privada é apenas um número aleatório muito grande, e a
    sua chave pública é calculada a partir dela. Estas chaves podem ser
    facilmente geradas no seu computador, ou mesmo em algo tão simples como uma
    calculadora. A maioria das pessoas usa uma carteira bitcoin para ajudar a
    gerar e gerir as suas chaves.
  </p>
  <p>
    Para receber bitcoins, teria de dar a sua chave pública a alguém que lhe
    quisesse enviar alguns. Esta pessoa criaria uma transacção onde desbloqueia
    as bitcoins que possui, e criaria um novo "cofre" de bitcoins e colocaria a
    sua chave pública dentro da fechadura.
  </p>
  <p>
    Esta transacção é então enviada para qualquer nó da rede Bitcoin, onde é
    retransmitida de computador para computador até que cada nó da rede tenha
    uma cópia da transacção. A partir daqui, cada nó tem a oportunidade de
    tentar minerar as últimas transacções que recebeu para a blockchain.
  </p>
  <p>
    Este processo de mineração envolve um nó que recolhe transacções do seu
    mempool para um bloco, e coloca repetidamente esses dados através de uma
    função hash (com um pequeno ajuste de cada vez) para tentar obter um hash de
    bloco abaixo do valor alvo.
  </p>
  <p>
    O primeiro mineiro a encontrar um hash de bloco abaixo do alvo adicionará o
    bloco à sua cópia da blockchain, e transmitirá este bloco para os outros nós
    da rede. Cada nó adicionará também este bloco à sua blockchain (garantindo
    que o novo bloco segue as regras da rede e removendo quaisquer transacções
    conflituosas do seu mempool), e reiniciará o processo de mineração para
    tentar construir em cima deste novo bloco na cadeia.
  </p>
  <p>
    Finalmente, o mineiro que extraiu este bloco terá colocado a sua própria
    transacção especial dentro do bloco, o que lhe permite desbloquear uma
    quantidade definida de bitcoins que ainda não existia. Esta recompensa de
    bloco funciona como um incentivo para os nós continuarem a construir a
    blockchain, ao mesmo tempo que distribui novas moedas pela rede Bitcoin.
  </p>
  <h5 id="resumo">Resumindo</h5>
  <p>
    Bitcoin é um programa de computador que partilha um ficheiro seguro com
    outros computadores em todo o mundo. Este ficheiro seguro é constituído por
    transacções, e estas transacções utilizam criptografia para permitir às
    pessoas enviar e receber cofres de depósito digitais. Como resultado, isto
    cria um sistema de pagamento electrónico que pode ser utilizado por qualquer
    pessoa, e funciona sem um ponto central de controlo.
  </p>
  <p>
    A rede Bitcoin tem funcionado ininterruptamente desde o seu lançamento em
    Janeiro de 2009. Em 2019 a rede Bitcoin processou mais de 112 milhões de
    transacções, movimentando um total de $15.577.763.114.629,34 ($15 biliões de
    dólares)
  </p>
  <p>
    O próprio programa Bitcoin está também em desenvolvimento activo, com mais
    de 600 indivíduos a contribuir para o código desde o seu lançamento3. Isto
    deve-se ao facto de o software ser "open source", o que significa que
    qualquer pessoa pode ver o código e contribuir para a sua melhoria.
  </p>

  <ul>
    <li>
      <a
        href="https://bitcoin.org/bitcoin.pdf"
        target="_blank"
        rel="noopener noreferrer">Whitepaper Bitcoin</a
      >
    </li>
    <li>
      <a
        href="https://blog.sparkpay.pt/whitepaper-bitcoin-portugal/"
        target="_blank"
        rel="noopener noreferrer">Whitepaper em Português</a
      >
    </li>
    <li>
      <a
        href="https://github.com/bitcoin/bitcoin/"
        target="_blank"
        rel="noopener noreferrer">Código fonte</a
      >
    </li>
  </ul>
</article>
