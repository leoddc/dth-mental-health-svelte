<script>
    import Carousel from "svelte-carousel";
    import Article from "./lib/Article.svelte";
    import ArticleCase from "./lib/ArticleCase.svelte";
    import Feature from "./lib/Feature.svelte";

    let colors = [
        {
            header: "'It’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text:  "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "'It's gone in the blink of an eye': Cormac Ryan reflects on his college basketball career after Senior Night win",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "Column: As women, taking every precaution against violence is still not enough",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "Stephanie Hutchison educates students about foreign service as Diplomat in Residence",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "UNC students work to close information gaps on Wikipedia at Art + Feminism Edit-a-thon event",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "Wilson Library construction timeline extended, library open to the public for the foreseeable future",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
        {
            header: "Youth on the UNC men's lacrosse team show promise in weekend games against Princeton and Penn",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        },
    ];
</script>

<div style="width: 400px;">
    <Article headline={"A headline"} author={"Leo Davidson"} img={"https://source.unsplash.com/random"} sideCar={true}/>
</div>

<Feature img={"https://source.unsplash.com/random"} headline={"Youth on the UNC men's lacrosse team show promise in weekend games against Princeton and Penn"} summary={"Heading into the general election, the mood in Trump world is buoyant."} author={"Leo Davidson"}/>

<div class="carousel-container">
    <ArticleCase header={"The Daily Tar Heel"} articleData={colors}/>
</div>

<style>
    .carousel-container {
        width: 90%;
        margin: auto;
    }
</style>
