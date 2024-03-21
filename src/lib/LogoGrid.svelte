<script>
    export let logoList;
</script>

<div class="logo-grid">
    {#each logoList as { img, url }}
        <a target="_parent" href={url}><img src={img} alt="Masthead" /></a>
    {/each}
</div>

<style>
    .logo-grid {
        display: grid;
        grid-template-columns: auto auto auto;
        gap: 60px;
    }

    img {
        width: 200px;
        filter: grayscale(1);
        opacity: 0.7;
        transition: 750ms ease-in-out;
    }

    a {
        align-self: center;
    }

    img:hover {
        filter: grayscale(0);
        opacity: 1;
        transform: scale(1.03);
    }

    @media only screen and (max-width: 900px) {
        .logo-grid {
            grid-template-columns: 1fr 1fr;
        }
    }

    @media only screen and (max-width: 600px) {
        .logo-grid {
            grid-template-columns: auto;
        }
    }
</style>
