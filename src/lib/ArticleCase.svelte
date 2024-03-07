<script>
    import Carousel from "svelte-carousel";
    import Article from "./Article.svelte";

    export let header = "";
    export let articleData = [];
</script>

<h2>{header}</h2>
<Carousel particlesToScroll={4} particlesToShow={4} swiping={false}>
    {#each articleData as { header, text, author, img } (header)}
        <Article
            img={img}
            headline={header}
            summary={text}
            author={author}
        />
    {/each}
</Carousel>

<style>
    h2 {
        font-size: 28px;
    }
</style>