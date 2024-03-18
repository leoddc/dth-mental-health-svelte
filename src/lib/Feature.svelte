<script>
    import Article from "./Article.svelte";

    export let img;
    export let summary = "";
    export let author = "";
    export let textLeft = true;
    export let invertColors = false;
    export let headerSize = 26;
    export let size = 90;
</script>

<div class="container" style="color: {invertColors ? 'var(--white)' : 'var(--black)'}; --size: {size}vh;">
    {#if textLeft}
        <div class="text">
            <slot name="text"/>
        </div>
        <img src="{img}" alt="">
    {:else}
        <img src="{img}" alt="">
        <div class="text">
            <slot name="text"/>
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
    .text, img {
        width: 75%;
        margin: auto;
        text-align: center;
    }
    @media (max-width: 800px) {
        .container {
            grid-template-columns: 1fr;
            height: fit-content;
            padding: 60px 0;
        }
        .text, img {
            width: 90%;
        }
    }
</style>
