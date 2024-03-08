<script>
    import Carousel from "svelte-carousel";
    import Article from "./lib/Article.svelte";
    import ArticleCase from "./lib/ArticleCase.svelte";
    import Feature from "./lib/Feature.svelte";
    import ArticleSet from "./lib/ArticleSet.svelte";

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

    let set = [
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
            header: "'He’s a a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200"
        }
    ];

    let set2 = [
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
        }
    ];
</script>

<div style:background-color={"black"}>
    <Feature headerSize={40} invertColors={true} img={"https://source.unsplash.com/random"} headline={"The Mental Health Edition"} size={240}/>
</div>

<main>
    <div class="article-set">
        <ArticleSet articleData={set} sideCar={false} header={"Lorem ipsum dolar iset"}/>
    </div>
    
    <div class="article-set">
        <ArticleSet sizePct={70} articleData={set2} sideCar={false} header={"Lorem ipsum dolar iset"}/>
    </div>
    
    <div>
        <Feature invertColors={false} img={"https://source.unsplash.com/random"} headline={"Youth on the UNC men's lacrosse team show promise in weekend games against Princeton and Penn"} summary={"Heading into the general election, the mood in Trump world is buoyant."} author={"Leo Davidson"}/>
    </div>
    
    <div class="carousel-container article-set">
        <ArticleCase header={"The Daily Tar Heel"} articleData={colors}/>
    </div>
</main>

<style>
    main {
        margin: auto;
        width: 90%;
    }
    .carousel-container {
        width: 100%;
        margin: auto;
    }

    .article-set {
        width: 100%;
        margin: auto;
    }
</style>
