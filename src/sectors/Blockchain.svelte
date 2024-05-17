<script>
  import Section from '../components/GuideSection.svelte';
</script>

<Section hashtag="blockchain-bitcoin" title="O que é a Blockchain?">
  <p>
    A blockchain é um ficheiro que contém uma lista de cada transacção de
    bitcoin alguma vez feita.
    <br />
    Todos na rede Bitcoin partilham uma cópia deste ficheiro, e este é actualizado
    regularmente com as últimas transacções.
  </p>
</Section>
<Section
  hashtag="para-que-serve-blockchain"
  title="Porque a blockchain é importante?"
>
  <p>A blockchain diz-lhe quanto bitcoin cada pessoa possui.</p>
  <p>
    Isto porque ter uma lista completa de transacções permite-lhe saber quantas
    bitcoin estão localizadas em cada morada. Portanto, é possível descobrir
    quantos bitcoin cada pessoa (mais correctamente, cada endereço) tem.
  </p>
  <p>A blockchain é como um livro de registo, ou um livro-razão.</p>
  <p class="note tip">
    Livro razão, razão geral, ficha razão, extrato da conta - um livro em que as
    transacções monetárias de uma empresa são afixadas sob a forma de débitos e
    créditos.
  </p>
</Section>
<Section
  hashtag="porque-se-chama-blockchain"
  title="Porque se chama Blockchain?"
>
  <p>
    Porque as transacções não são adicionadas ao ficheiro individualmente. Em
    vez disso, são agrupadas e adicionadas em blocos. Por isso, uma cadeia de
    blocos.
  </p>
  <p>
    Além disso, estes blocos são ligados entre si, pelo que quaisquer alterações
    feitas a um bloco mais abaixo na cadeia irão alterar os blocos acima dele.
    Assim, os blocos ligados, ou cadeia de blocos.
  </p>
  <p>
    O agrupamento das transacções em blocos facilita a todos a partilha de uma
    cópia da blockchain. Com as velocidades de ligação à Internet que temos, é
    muito mais fácil partilhar um ficheiro que se actualiza uma vez a cada 10
    minutos, do que um que se actualiza várias vezes por segundo.
  </p>
  <p>
    O encadeamento das transacções é uma característica de segurança. Torna
    difícil manipular a cadeia de blocos sem que ninguém repare.
  </p>
</Section>
