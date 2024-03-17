<script>
    import Article from "./Article.svelte";

    export let img;
    export let headline;
    export let summary = "";
    export let author = "";
    export let textLeft = true;
    export let invertColors = false;
    export let headerSize = 26;
    export let size = 100;
</script>

<div class="container" style="color: {invertColors ? 'var(--white)' : 'var(--black)'}; --size: {size}vh;">
    {#if textLeft}
        <div class="text">
            <Article invertColors={invertColors} headline={headline} summary={summary} author={author} headerSize={headerSize} summarySize={20}/>
        </div>
        <img src="{img}" alt="">
    {:else}
        <img src="{img}" alt="">
        <div class="text">
            <Article invertColors={invertColors} headline={headline} summary={summary} author={author} headerSize={headerSize} summarySize={20}/>
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
