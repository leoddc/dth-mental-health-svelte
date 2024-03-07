<script>
    import Article from "./Article.svelte";

    export let img;
    export let headline;
    export let summary = "";
    export let author;
    export let textLeft = true;
</script>

<div class="container">
    {#if textLeft}
        <div class="text">
            <Article headline={headline} summary={summary} author={author} headerSize={26} summarySize={20}/>
        </div>
        <img src="{img}" alt="">
    {:else}
        <img src="{img}" alt="">
        <div class="text">
            <Article headline={headline} summary={summary} author={author}/>
        </div>
    {/if}
</div>

<style>
    .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        width: 90%;
        margin: 240px auto;
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