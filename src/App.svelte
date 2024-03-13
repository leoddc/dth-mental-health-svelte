<script>
    import Carousel from "svelte-carousel";
    import Article from "./lib/Article.svelte";
    import ArticleCase from "./lib/ArticleCase.svelte";
    import Feature from "./lib/Feature.svelte";
    import ArticleSet from "./lib/ArticleSet.svelte";
    import TextColumns from "./lib/TextColumns.svelte";

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
        }
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
        }
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
        }
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
        }
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
        }
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
        }
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
        }
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
        }
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
        }
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

<div style:background-color={"black"}>
    <Feature
        headerSize={40}
        invertColors={true}
        img={"https://source.unsplash.com/random"}
        headline={"The Mental Health Edition"}
        size={240}
    />
</div>

<main>
    <div class="columns">
        <h2>Title</h2>
        <p class="author">
            By Emmy Martin<br /><span class="byline">Byline</span>
        </p>
        <TextColumns numberOfCols={2}>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
            Malesuada proin libero nunc consequat interdum varius. Gravida
            rutrum quisque non tellus orci ac. Blandit massa enim nec dui nunc
            mattis enim. Lacinia quis vel eros donec ac odio. Scelerisque
            eleifend donec pretium vulputate sapien. Sagittis eu volutpat odio
            facilisis mauris sit amet. Tellus elementum sagittis vitae et leo
            duis. Ornare quam viverra orci sagittis. Purus viverra accumsan in
            nisl nisi scelerisque. Quis risus sed vulputate odio ut enim blandit
            volutpat. Sit amet justo donec enim diam vulputate. Ipsum
            suspendisse ultrices gravida dictum fusce ut. Massa id neque aliquam
            vestibulum morbi blandit. Rhoncus dolor purus non enim praesent
            elementum facilisis leo vel. Condimentum mattis pellentesque id nibh
            tortor id aliquet lectus. Pellentesque elit eget gravida cum. In
            cursus turpis massa tincidunt dui ut ornare. In mollis nunc sed id
            semper. Eu tincidunt tortor aliquam nulla facilisi cras fermentum.
            Magnis dis parturient montes nascetur ridiculus mus mauris vitae
            ultricies. At ultrices mi tempus imperdiet nulla malesuada
            pellentesque elit eget. Elementum pulvinar etiam non quam lacus
            suspendisse faucibus. Nam aliquam sem et tortor consequat id. Tempus
            imperdiet nulla malesuada pellentesque elit eget gravida cum sociis.
            Nibh ipsum consequat nisl vel pretium. Potenti nullam ac tortor
            vitae purus faucibus. Bibendum est ultricies integer quis auctor.
            Magna eget est lorem ipsum dolor sit amet consectetur adipiscing.
            Laoreet non curabitur gravida arcu ac tortor dignissim convallis.
            Neque viverra justo nec ultrices dui sapien eget mi proin. Mi
            bibendum neque egestas congue. Neque viverra justo nec ultrices dui
            sapien eget mi. Sit amet tellus cras adipiscing. Ut tortor pretium
            viverra suspendisse potenti nullam ac tortor. Eget dolor morbi non
            arcu. Sed velit dignissim sodales ut eu sem integer vitae. Sagittis
            orci a scelerisque purus semper eget. Duis ultricies lacus sed
            turpis tincidunt id aliquet. Sed enim ut sem viverra aliquet. Sapien
            pellentesque habitant morbi tristique. Ac turpis egestas integer
            eget aliquet nibh. Et sollicitudin ac orci phasellus egestas tellus
            rutrum. Blandit turpis cursus in hac habitasse platea dictumst
            quisque. Nisl pretium fusce id velit ut tortor pretium. Ac ut
            consequat semper viverra nam libero justo laoreet. Magna eget est
            lorem ipsum dolor. Nunc eget lorem dolor sed. Eget magna fermentum
            iaculis eu. Quis lectus nulla at volutpat diam. Accumsan tortor
            posuere ac ut consequat. Adipiscing elit pellentesque habitant morbi
            tristique senectus et netus. Ornare arcu dui vivamus arcu felis
            bibendum ut. Faucibus a pellentesque sit amet porttitor eget. Enim
            sit amet venenatis urna cursus. In eu mi bibendum neque egestas
            congue quisque egestas diam. Et netus et malesuada fames ac turpis
            egestas. Felis eget velit aliquet sagittis id. Neque convallis a
            cras semper auctor neque vitae tempus. Cursus vitae congue mauris
            rhoncus. Ac tortor vitae purus faucibus ornare suspendisse. Diam
            vulputate ut pharetra sit amet aliquam. Ut eu sem integer vitae.
            Vitae justo eget magna fermentum iaculis eu non. Blandit aliquam
            etiam erat velit scelerisque in dictum non consectetur. Amet cursus
            sit amet dictum sit amet. Ante metus dictum at tempor commodo
            ullamcorper. Magna fermentum iaculis eu non.
        </TextColumns>
    </div>
    <div class="article-set">
        <ArticleSet
            articleData={collborativeStories}
            sideCar={false}
            header={"Collaborative Stories"}
        />
    </div>

    <div class="carousel-container article-set">
        <ArticleCase header={"The Daily Tar Heel"} articleData={theDailyTarHeelStories} />
    </div>

    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={thePendulumStories}
            sideCar={false}
            header={"The Pendulum"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={oldGoldAndBlackStories}
            sideCar={false}
            header={"Old Gold & Black"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={nineTimeStories}
            sideCar={false}
            header={"Nine Times"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={theSeahawkStories}
            sideCar={false}
            header={"The Seahawk"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={theEastCarolinianStories}
            sideCar={false}
            header={"The East Carolinian"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={aAndTRegisterStories}
            sideCar={false}
            header={"A&T Register"}
        />
    </div>
    <div class="article-set">
        <ArticleSet
            sizePct={70}
            articleData={theChronicleStories}
            sideCar={false}
            header={"The Chronicle"}
        />
    </div>

    <div>
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
    .carousel-container {
        width: 100%;
        margin: auto;
    }

    .article-set {
        width: 100%;
        margin: auto;
    }
</style>
