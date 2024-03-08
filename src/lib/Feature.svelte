<script>
    import Article from "./Article.svelte";

    export let img;
    export let headline;
    export let summary = "";
    export let author = "";
    export let textLeft = true;
    export let invertColors = false;
    export let headerSize = 26;
    export let size = 240;
</script>

<div class="container" style:color={invertColors ? "#fff" : "#000"} style:padding={`${size}px 0px`} >
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
    }
    .text {
        width: 75%;
        text-align: center;
        margin: auto;
    }
    img {
        margin: auto;
        width: 75%;
    }
</style>