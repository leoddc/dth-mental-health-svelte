<script>
    import Article from "./Article.svelte";

    export let articleData = [];
    export let header = "";
    export let headerImg = "";
    export let sideCar = true;
    export let sizePct = 85;
    export let invertColors = false;
    export let imgSize = 250;
</script>

{#if header}
    <h2>{header}</h2>
{/if}
{#if headerImg}
    <img src="{headerImg}" alt="Masthead" width="{imgSize}" class="masthead">
{/if}
<div class="grid-container" style="width: {sizePct}%;">
    {#each articleData as { header, text, author, img }}
        <Article
            {img}
            headline={header}
            summary={text}
            {author}
            {sideCar}
            {invertColors}
        />
    {/each}
</div>

<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 40px;
        margin: auto;
    }
    @media (max-width: 750px) {
        .grid-container {
            grid-template-columns: 1fr;
        }
    }
</style>
