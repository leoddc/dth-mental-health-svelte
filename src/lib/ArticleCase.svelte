<script>
    import { onMount } from "svelte";
    import Carousel from "svelte-carousel";
    import Article from "./Article.svelte";

    export let header = "";
    export let headerImg = "";
    export let articleData = [];

    let particlesToShow = 4;
    let particlesToScroll = 4;

    function updateCarouselSettings() {
        if (window.innerWidth < 600) {
            particlesToShow = 1;
            particlesToScroll = 1;
        } else {
            particlesToShow = 4;
            particlesToScroll = 4;
        }
    }

    onMount(() => {
        updateCarouselSettings();
        window.addEventListener("resize", updateCarouselSettings);

        return () => {
            window.removeEventListener("resize", updateCarouselSettings);
        };
    });
</script>

{#if header}
    <h2>{header}</h2>
{/if}
{#if headerImg}
    <img src={headerImg} alt="Masthead" width="250" class="masthead" />
{/if}
<Carousel {particlesToScroll} {particlesToShow} swiping={false}>
    {#each articleData as { header, text, author, img, url, label }}
        <Article
            {img}
            headline={header}
            summary={text}
            {author}
            {url}
            {label}
        />
    {/each}
</Carousel>
