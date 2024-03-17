<script>
    import Carousel from "svelte-carousel";
    import Article from "./lib/Article.svelte";
    import ArticleCase from "./lib/ArticleCase.svelte";
    import Feature from "./lib/Feature.svelte";
    import ArticleSet from "./lib/ArticleSet.svelte";
    import TextColumns from "./lib/TextColumns.svelte";
    import Navbar from "./lib/Navbar.svelte";

    const collborativeStories = [
        {
            header: "'It’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading ito the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, hewrks hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, heworks hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading int the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const theDailyTarHeelStories = [
        {
            header: "'It’s jus crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s akiller,he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a do, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const thePendulumStories = [
        {
            header: "'I’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general election, th mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, hworks hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the genera election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the geneal election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const oldGoldAndBlackStories = [
        {
            header: "'It’s jst crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general election, he mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heaing into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dg, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const nineTimeStories = [
        {
            header: "'It’s just craz': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a og, he’s a killer, he works hard': RJ Davis' rise fom New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trmp world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const theSeahawkStories = [
        {
            header: "'It’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the genral election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog,he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into th general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading nto the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const theEastCarolinianStories = [
        {
            header: "'It’s just craz': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general electin, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s ailler, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the genera election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const aAndTRegisterStories = [
        {
            header: "'It’s ust crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’sa kiler, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the geeral election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const theChronicleStories = [
        {
            header: "'It’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Headin into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’ a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading int the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];

    const technicianStories = [
        {
            header: "'It’s just crazy': Armando Bacot tearily reminisces on his five years at UNC after senior night win",
            text: "Headin into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’ a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading int the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'He’s a dog, he’s a killer, he works hard': RJ Davis' rise from New York Gauchos to dominance in the ACC",
            text: "Heading into the general election, the mood in Trump world is buoyant.",
            author: "Juy Goe",
            img: "https://source.unsplash.com/random/300x200",
        },
    ];
</script>

<!-- 
    Collaborative Stories - 3 
    The Daily Tar Heel - 21 
    The Pendulum - 3 
    Old Gold & Black - 3 
    Nine Times - 2 
    The Seahawk - 2
    The East Carolinian - 2 
    A&T Register - 2 
    The Chronicle - 1
 -->

<div style:background-color={"var(--black)"}>
    <Feature
        headerSize={40}
        invertColors={true}
        img={"https://source.unsplash.com/random"}
        headline={"The Mental Health Edition"}
        size={100}
    />
</div>

<Navbar
    data={[
        { url: "#introduction", text: "Introduction" },
        { url: "#collaborative-stories", text: "Collaborative Stories" },
        { url: "#the-daily-tar-heel", text: "The Daily Tar Heel" },
        { url: "#the-pendulum", text: "The Pendulum" },
        { url: "#old-gold-and-black", text: "Old Gold & Black" },
        { url: "#nine-times", text: "Nine Times" },
        { url: "#the-seahawk", text: "The Seahawk" },
        { url: "#the-east-carolinian", text: "The East Carolinian" },
        { url: "#a-and-t-register", text: "A&T Register" },
        { url: "#a-and-t-register", text: "A&T Register" },
        { url: "#the-chronicle", text: "The Chronicle" },
    ]}
/>

<main>
    <div class="columns anchor-wrapper">
        <span class="anchor" id="introduction"></span>
        <h2>Behind the Mental Health Collaborative</h2>
        <p class="author">
            By Emmy Martin<br /><span class="byline"
                >Editor in Chief of The Daily Tar Heel</span
            >
        </p>
        <TextColumns numberOfCols={2}>
            Every time I walk through the Pit at UNC, I remember the sticky
            notes and flowers left on those four green chairs three years ago. I
            remember the candles that sat at their feet, the messages written in
            chalk on the bricks.<br>“You’re fire will never truly die,” the largest
            chalk message said. I remember the four students who died by suicide
            that semester.<br>The mental health crisis we face has not subsided.
            Last year, N.C. State lost seven students to suicide. From 2016 to
            2020, there were 878 deaths by suicide in North Carolina of people
            ages 15-24. A national survey conducted by the American College
            Health Association found that 52 percent of undergraduate students
            regularly experienced moderate psychological distress. While this
            problem isn’t new, it feels more important that ever.<br>That’s why The
            Daily Tar Heel partnered with eight other college newspapers to
            report on mental health challenges shared by those in each of their
            communities. What you hold in your hands is the result of months of
            rigorous reporting, research, conversations, writing, editing and
            designing. This initiative began in 2023, when The Daily Tar Heel
            was awarded a grant from the Solutions Journalism Network as part of
            its Student Media Challenge initiative. That grant helped fund the
            collaborative work of this project. Many of the stories you will
            read in this newspaper do more than just present a problem — they
            also explore solutions to this crisis.<br>The Daily Tar Heel is honored
            to have had the privilege of working with The A&T Register, The Duke
            Chronicle, The East Carolinian, The Niner Times, The Old Gold &
            Black, The Pendulum, The Seahawk and The Technician on this project.<br>
            With more than 40 reported stories and seven opinion pieces, we
            touch many issues related to mental health — from wow Wake Forest
            University trains its faculty to be on the frontline of mental
            health care to how international students create community at East
            Carolina Univeristy.<br>While there’s more that still must be, this is
            a step toward that future. As we navigate the complexities of mental
            health, we must not lose sight of the individual people behind the
            statistics — the students, faculty, families and communities
            affected. Their stories, their struggles and their resilience should
            serve as a guiding light. We hope that this mental health
            collaborative project serves as a call to action to create a future
            where no one suffers in silence.
        </TextColumns>
    </div>
</main>
<div class="article-set case black-back anchor-wrapper">
    <span class="anchor" id="collaborative-stories"></span>
    <h2 class="edge-header" style:color={"white"}>Collaborative Stories</h2>
    <ArticleSet
        articleData={collborativeStories}
        sideCar={false}
        invertColors={true}
    />
</div>
<main>
    <div class="carousel-container article-set case anchor-wrapper">
        <span class="anchor" id="the-daily-tar-heel"></span>
        <ArticleCase
            headerImg={"mastheads/dth-masthead.png"}
            articleData={theDailyTarHeelStories}
        />
    </div>

    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-pendulum"></span>
        <ArticleSet
            sizePct={70}
            articleData={thePendulumStories}
            sideCar={false}
            headerImg={"mastheads/pendulum-masthead.png"}
            imgSize={200}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="old-gold-and-black"></span>
        <ArticleSet
            sizePct={70}
            articleData={oldGoldAndBlackStories}
            sideCar={false}
            headerImg={"mastheads/ogb-masthead.png"}
            imgSize={275}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="nine-times"></span>
        <ArticleSet
            sizePct={70}
            articleData={nineTimeStories}
            sideCar={false}
            headerImg={"mastheads/nt-masthead.png"}
            imgSize={225}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-seahawk"></span>
        <ArticleSet
            sizePct={70}
            articleData={theSeahawkStories}
            sideCar={false}
            headerImg={"mastheads/seahawk-masthead.png"}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-east-carolinian"></span>
        <ArticleSet
            sizePct={70}
            articleData={theEastCarolinianStories}
            sideCar={false}
            header={"The East Carolinian"}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="a-and-t-register"></span>
        <ArticleSet
            sizePct={70}
            articleData={aAndTRegisterStories}
            sideCar={false}
            headerImg={"mastheads/register-masthead.png"}
            imgSize={175}
        />
    </div>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-chronicle"></span>
        <ArticleSet
            sizePct={70}
            articleData={theChronicleStories}
            sideCar={false}
            header={"The Chronicle"}
        />
    </div>

    <div class="case">
        <Feature
            invertColors={false}
            img={"https://source.unsplash.com/random"}
            headline={"Youth on the UNC men's lacrosse team show promise in weekend games against Princeton and Penn"}
            summary={"Heading into the general election, the mood in Trump world is buoyant."}
            author={"Leo Davidson"}
        />
    </div>
</main>

<style>
    main {
        margin: auto;
        width: 90%;
    }

    .anchor-wrapper {
        position: relative;
    }

    .anchor {
        position: absolute;
        top: -100px;
    }

    .edge-header {
        width: 90%;
        margin: 20px auto;
    }

    .black-back {
        background-color: var(--black);
        width: 100%;
        padding: 20px 0;
    }

    .case {
        margin: 80px auto;
    }

    .byline {
        font-style: italic;
        font-family: Arial, sans-serif;
        font-size: 14px;
        margin-top: 0px;
        font-weight: 300;
    }

    .columns {
        width: 60%;
        margin: 60px auto;
    }

    @media only screen and (max-width: 900px) {
        .columns {
            width: 80%;
        }
    }
    .carousel-container {
        width: 100%;
        margin: auto;
    }

    .article-set {
        width: 100%;
    }
</style>
