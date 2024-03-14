<script>
    import Article from "./Article.svelte";

    export let articleData = [];
    export let header = "";
    export let sideCar = true;
    export let sizePct = 85;
    export let invertColors = false;
</script>

{#if header}
    <h2>{header}</h2>
{/if}
<div class="grid-container" style:width={`${sizePct}%`}>
    {#each articleData as { header, text, author, img }}
        <Article {img} headline={header} summary={text} author={author} sideCar={sideCar} invertColors={invertColors} />
    {/each}
</div>

<style>
    .grid-container {
        display: grid;
        grid-template-columns: auto auto auto;
        gap: 40px;
        margin: auto;
    }
</style>
