<script>
    import { Link } from "svelte-navigator";
    export let img_right;
    export let patronName,
        patronService,
        contact,
        description,
        img,
        buttonText,
        buttonURL;
</script>

<article class="columns {img_right ? 'right' : ''}">
    <figure class="column col-6 col-sm-12">
        <img class="img-responsive" src={img} alt="" />
    </figure>
    <div class="copy column col-6 col-sm-12">
        <h1>{patronService}</h1>
        <p class="text-dark">
            Descrição: {description}
        </p>
        <p class="text-dark">Nome do Patrono: {patronName}</p>
        <p class="text-dark">Contacto: {contact}</p>
        <div class="card-footer">
            {#if buttonURL}
                <button
                    on:click={() => window.open(buttonURL, "_blank")}
                    class="btn btn-primary">{buttonText}</button
                >
            {/if}
        </div>
    </div>
</article>

<style lang="scss">
    article {
        display: flex;
        align-items: center;
        margin-bottom: 2.5rem;
    }
    article.right {
        flex-direction: row-reverse;
    }
    figure {
        margin: 0;
        padding: 3rem;
    }

    @media (max-width: 600px) {
        article {
            margin-bottom: 2rem;
        }
        figure {
            display: flex;
            justify-content: center;
            width: 100%;
            padding-bottom: 3rem;
            overflow: hidden;
        }

        figure img {
            max-width: 60%;
        }
        .copy {
            text-align: center;
        }
    }
</style>
