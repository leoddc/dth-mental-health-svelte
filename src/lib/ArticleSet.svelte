<script>
    import Article from "./Article.svelte";

    export let articleData = [];
    export let header = "";
    export let sideCar = true;
    export let sizePct = 85;
</script>

<h2>{header}</h2>
<div class="grid-container" style:width={`${sizePct}%`}>
    {#each articleData as { header, text, author, img } (header)}
        <Article {img} headline={header} summary={text} author={author} sideCar={sideCar} />
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
