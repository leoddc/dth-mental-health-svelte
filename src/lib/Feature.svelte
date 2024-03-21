<script>
    import Article from "./Article.svelte";

    export let img;
    export let textLeft = true;
    export let invertColors = false;
    export let size = 90;
    export let imgSize = "75%";
    export let normalImg = true;
</script>

<div
    class="container"
    style="color: {invertColors
        ? 'var(--white)'
        : 'var(--black)'}; --size: {size}vh;"
>
    {#if textLeft}
        <div class="text">
            <slot name="text" />
        </div>
        <img
            src={img}
            style:width={imgSize}
            alt=""
            class={normalImg ? `normal-img` : ""}
        />
    {:else}
        <img
            src={img}
            style:width={imgSize}
            alt=""
            class={normalImg ? `normal-img` : ""}
        />
        <div class="text">
            <slot name="text" />
        </div>
    {/if}
</div>

<style>
    .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        width: 90%;
        margin: auto;
        height: var(--size);
    }
    .text,
    img {
        margin: auto;
        text-align: center;
    }

    .normal-img {
        aspect-ratio: 3/2;
        object-fit: cover;
    }

    @media (max-width: 800px) {
        .container {
            grid-template-columns: 1fr;
            height: fit-content;
            padding: 60px 0;
        }
        .text,
        img {
            width: 90%;
        }
    }
</style>
