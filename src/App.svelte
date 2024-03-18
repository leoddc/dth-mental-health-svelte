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
            header: "Study examines mental health impact of campus gun-related incidents",
            text: "Students more likely to have PTSD symptoms after UNC’s two incidents of gun violence",
            author: "Lucy Kraus",
            img: "images/dth-university-post-shooting-mental-health.png",
        },
        {
            header: "UNC students of color find mental health support through community",
            text: "Mental health resources, student organizations build communities for students of color",
            author: "Hamsini Sivakumar and Daneen Khan",
            img: "images/20240201-gao-Dth-university-lifestyle-mental-health-experience-as-poc-at-pwi.jpg",
        },
        {
            header: "'It's OK to ask for assistance': how UNC's elite athletes use mental health as an edge",
            text: "Sports across UNC use mental health resources, ask for help when needed",
            author: "Shelby Swanson",
            img: "images/Dth-sports-feature-rucker-mental-health.jpeg",
        },
        {
            header: "LGBTQ+ support groups provide community care for substance abuse",
            text: "LGBTQ+ individuals more likely to have serious mental illness, intersectional care provides support",
            author: "Eliza Benbow",
            img: "images/Diehl_lifestyle-queer-substance-abuse-solutions.jpeg",
        },
        {
            header: "Culture-responsive care addresses mental health disparities in tribal communities",
            text: "Culturally relevant practices look at cultural stressors, increasing accessibility of care",
            author: "Kaitlyn Church",
            img: "public/images/20240205_TRAN-lifestyle-indigenous-mental-health-resources-2.jpg",
        },
        {
            header: "'Could have been doing this all along': State budget invests in mental health resources",
            text: "Includes increase in Medicaid reimbursement rates, expanding justice system programs",
            author: "Lucy Marques",
            img: "images/Dth-city-politics-of-mental-funding-state.jpeg",
        },
        {
            header: "'Testament to how seriously the state is taking suicide prevention': State launches mental health lifeline dashboard",
            text: "Dashboard tracks calls made to crisis lifelines, providing transparency on service",
            author: "Lola Oliverio",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'Testament to how seriously the state is taking suicide prevention': State launches mental health lifeline dashboard",
            text: "Content warning: This article contains mentions of suicide and death.",
            author: "Emmy Martin and Emily Vespa",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "Op-ed: It's time to replace the word 'stigma' with 'sanism'",
            text: "",
            author: "Krista Savage-White",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "Community members find mental health relief in spirituality",
            text: "",
            author: "Marisa Rosa",
            img: "images/dth-lifestyle-mental-health-spirituality.jpeg",
        },
        {
            header: "Column: Mental health is generational in minority communities. Acknowledge it",
            text: "",
            author: "Ankur Mutyala",
            img: "images/dth-opinion-generational-mental-health.jpeg",
        },
        {
            header: "Op-ed: Make space to help those struggling with their mental health",
            text: "Content warning: This op-ed contains mention of suicide.",
            author: "Lior Vered-Langley",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "IN PROGRESS",
            text: "",
            author: "",
            img: "images/calling-out-elected-officials.jpg",
        },
        {
            header: "Mental health providers, patients face inconsistencies in insurance coverage",
            text: "",
            author: "Tori Newby and Maddie Policastro",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "Criminal justice diversion programs redirect, guide individuals",
            text: "",
            author: "Sarah Smiley",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'It's about the process': Art therapy provides creative outlet as mental health care",
            text: "",
            author: "Mila Mascenik and Sophia Melin",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "The Farm at Penny Lane grows hope through therapy programs",
            text: "",
            author: "Madison Gagnon",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "Health humanities laboratory looks to bridge medical, social sciences",
            text: "",
            author: "Charlene Wu",
            img: "images/Dth-lifestyle-health-humanities-mental-health-creative-solutions.jpeg",
        },
        {
            header: "Study examines mental health impact of campus gun-related incidents",
            text: "",
            author: "Lucy Kraus",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "'Therapy should be affordable to everyone': CAPS addresses financial burdens of therapy",
            text: "",
            author: "Samantha Nichols",
            img: "public/images/dth-university-mental-health-cost-breakdown.png",
        },
        {
            header: "Students and faculty reflect on university well-being days across North Carolina",
            text: "Content Warning: This article contains mention of suicide.",
            author: "Alli Pardue",
            img: "images/university-well-being-checks-days.png",
        },
        {
            header: "NO TITLE",
            text: "",
            author: "Samuel Long and junior Olivia Gschwind",
            img: "https://source.unsplash.com/random/300x200",
        },
        {
            header: "NO TITLE",
            text: "",
            author: "NO AUTHOR",
            img: "images/Dth-lifestyle-alternative-forms-of-therapy-in-arts.jpeg",
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
        { url: "#technician", text: "The Technician" },
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
            <span class="column">
                <p style:margin-top={0}>Every time I walk through the Pit at UNC, I remember the sticky notes and flowers left on those green chairs three years ago. I remember the candles that sat at their feet, the messages written in chalk on the bricks. </p>
                <p>“You’re fire will never truly die,” the largest chalk message said. I remember the four students who died by suicide that semester. </p>
                <p>The mental health crisis we face has not subsided. Last year, N.C. State lost seven students to suicide. From 2016 to 2020, there were 878 deaths by suicide in North Carolina of people ages 15 to 24. A national survey conducted by the American College Health Association found that 52 percent of undergraduate students regularly experienced moderate psychological distress. While this problem isn’t new, it feels more important that ever. </p>
                <p>That’s why The Daily Tar Heel partnered with eight other college newspapers to report on mental health challenges shared by those in each of their communities. This Mental Health Collaborative is the result of months of rigorous reporting, research, conversations, writing, editing and designing. This initiative began in 2023, when The Daily Tar Heel was awarded a grant from the Solutions Journalism Network as part of its Student Media Challenge initiative. That grant helped fund the collaborative work of this project. Many of the stories you will read in this collaborative do more than just present a problem — they also explore solutions to this crisis.</p>
                <p>The Daily Tar Heel is honored to have had the privilege of working with The A&T Register, The Duke Chronicle, The East Carolinian, The Niner Times, The Old Gold & Black, The Pendulum, The Seahawk and The Technician on this project.</p>
                <p>With more than 40 reported stories and seven opinion pieces, we touch many issues related to mental health — from how Wake Forest University trains its faculty to be on the frontline of mental health care to how international students create community at East Carolina Univeristy. </p>
                <p>While there’s more that still must be, this is a step toward that future. As we navigate the complexities of mental health, we must not lose sight of the individual people behind the statistics — the students, faculty, families and communities affected. Their stories, their struggles and their resilience should serve as a guiding light. We hope that this mental health collaborative project serves as a call to action to create a future where no one suffers in silence. </p>
                
            </span>
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
        <span class="anchor" id="technician"></span>
        <ArticleSet
            sizePct={70}
            articleData={aAndTRegisterStories}
            sideCar={false}
            headerImg={"mastheads/technician-masthead.png"}
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
<footer></footer>

<style>
    main {
        margin: auto;
        width: 90%;
    }

    footer {
        width: 100%;
    }

    .column {
        line-height: 23px;
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
