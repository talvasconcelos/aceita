<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';
  import QRCode from 'qrcode';

  let data;
  let amount;
  let activeTabValue = 'offchain';
  let fiatPrice;
  let converted;
  let loading = false;
  let LNURL =
    'LNURL1DP68GURN8GHJ7AMPD3KX2APWWDCXZUNTWPSHJTNSWSHKCMN4WFK8QTMPWP5J7A339AKXUATJDSHNWSJ3UK6';

  $: if (fiatPrice && amount && amount > 0) {
    converted = (amount / 100000000) * fiatPrice;
  }

  onMount(() => getPrice());

  const handleClick = (tabValue) => (e) => (activeTabValue = tabValue);

  const makeQR = async (string) => {
    try {
      return await QRCode.toDataURL(string, { margin: 1, width: 500 });
    } catch (err) {
      console.error(err);
    }
  };

  const getPrice = () => {
    fetch(
      'https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=eur'
    )
      .then((res) => res.json())
      .then((r) => {
        fiatPrice = r.bitcoin.eur;
      })
      .catch((e) => console.error(e));
  };

  const getData = (amount) => {
    const API_KEY = '312c2d9dda2942d9aa50ce87f7158714';
    loading = true;
    const rootUrl = 'https://wallet.sparkpay.pt';
    const invoice = fetch(`${rootUrl}/api/v1/payments`, {
      method: 'POST',
      headers: {
        'Content-type': 'application/json',
        'X-Api-Key': API_KEY,
      },
      body: JSON.stringify({
        out: false,
        amount: amount,
        memo: 'Donativo',
      }),
    }).then((res) => res.json());
    const address = fetch(
      `${rootUrl}/watchonly/api/v1/address/5CidegfVYQsNwyan6fZJW4`,
      {
        headers: {
          'Content-type': 'application/json',
          'X-Api-Key': API_KEY,
        },
      }
    ).then((res) => res.json());

    Promise.all([invoice, amount >= 25000 ? address : null]).then((res) => {
      console.log(res.filter((v) => v));
      data = { ...res[0] };
      if (res[1]) {
        let x = res[1][0];
        data.onchainaddress = x.address;
        if (amount > 100000) {
          activeTabValue = 'onchain';
        }
      }
      loading = false;
    });
  };
</script>

<section class="container grid-lg">
  <header>
    <h2>Donativo</h2>
    <div class="subtitle">
      <p>Apoiar o projecto</p>
    </div>
  </header>
  <div class="columns">
    <div class="column col-5 col-mr-auto col-sm-12">
      <header>
        <p class="title">Criar um pagamento</p>
      </header>
      <div class="form-group">
        <label class="form-label" for="amount">Quantia (em satoshis)</label>
        <input
          class="form-input"
          type="number"
          id="amount"
          bind:value={amount}
          placeholder="100"
          min="10"
        />
        {#if fiatPrice}<small>1 BTC ~ €{fiatPrice}</small>{/if}
        {#if converted}
          <br />
          <small>Aprox. €{converted.toFixed(2)}</small>
        {/if}
      </div>
      <button
        class="btn btn-primary float-right"
        class:loading
        on:click={() => {
          getData(parseInt(amount));
          amount = null;
        }}>Doar</button
      >
    </div>
    <div class="column col-6 col-sm-12">
      {#if !data}
        <div transition:fade={{ duration: 350 }}>
          <header>
            <p class="title">Outras opções</p>
          </header>
          <dl class="list list_custom">
            <dd><strong>LN Address: </strong>geral@aceitabitcoin.pt</dd>
            <dd>
              <strong>LNURL: </strong><span>{LNURL}</span>
              <div class="qr-code">
                {#await makeQR(LNURL)}
                  <p>Wait...</p>
                {:then qr}
                  <figure class="shadowed">
                    <a href={`lightning:${LNURL}`}>
                      <img class="img-responsive" src={qr} alt={LNURL} />
                    </a>
                  </figure>
                {:catch error}
                  <p>Oh no! Something went wrong!</p>
                {/await}
              </div>
            </dd>
          </dl>
        </div>
      {:else}
        <div transition:fade={{ duration: 350 }}>
          <ul class="tab tab-block">
            {#if data.onchainaddress}
              <li class="tab-item" class:active={activeTabValue === 'onchain'}>
                <a href="#void" on:click={handleClick('onchain')}
                  >BTC (Onchain)</a
                >
              </li>
            {/if}
            <li class="tab-item" class:active={activeTabValue === 'offchain'}>
              <a href="#void" on:click={handleClick('offchain')}
                >LN (Offchain)</a
              >
            </li>
          </ul>
          <div class="qr-code">
            {#if activeTabValue === 'onchain'}
              {#await makeQR(data.onchainaddress)}
                <p>Wait...</p>
              {:then qr}
                <figure>
                  <a href={`bitcoin:${data.onchainaddress}`}>
                    <img
                      class="img-responsive"
                      src={qr}
                      alt={data.onchainaddress}
                    />
                  </a>
                  <figcaption>{data.onchainaddress}</figcaption>
                </figure>
              {:catch error}
                <p>Oh no! Something went wrong!</p>
              {/await}
            {/if}
            {#if activeTabValue === 'offchain'}
              {#await makeQR(data.payment_request)}
                <p>Wait...</p>
              {:then qr}
                <figure>
                  <a href={`lightning:${data.payment_request}`}>
                    <img
                      class="img-responsive"
                      src={qr}
                      alt={data.payment_request}
                    />
                  </a>
                  <figcaption>{data.payment_request}</figcaption>
                </figure>
              {:catch error}
                <p>Oh no! Something went wrong!</p>
              {/await}
            {/if}
          </div>
          <button
            class="btn btn-success p-centered"
            on:click={() => (data = null)}>Fechar</button
          >
        </div>
      {/if}
    </div>
  </div>
</section>

<style>
  dd span {
    word-break: break-all;
    text-transform: lowercase;
  }
  .title {
    font-size: 1.1rem;
  }
  .qr-code {
    position: relative;
    width: 100%;
    max-width: 350px;
    margin: 2rem auto;
  }
  .qr-code figure.shadowed {
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px,
      rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
  }
  .qr-code img {
    width: 100%;
  }
  .qr-code figcaption {
    margin-top: 2em;
    text-align: center;
    font-size: 75%;
    word-break: break-all;
  }
</style>
