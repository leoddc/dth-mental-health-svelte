<script>
    import Carousel from "svelte-carousel";
    import Article from "./lib/Article.svelte";
    import ArticleCase from "./lib/ArticleCase.svelte";
    import Feature from "./lib/Feature.svelte";
    import ArticleSet from "./lib/ArticleSet.svelte";
    import TextColumns from "./lib/TextColumns.svelte";
    import Navbar from "./lib/Navbar.svelte";
    import LogoGrid from "./lib/LogoGrid.svelte";

    const logoList = [
        {
            img: "mastheads/dtc-masthead.png",
            url: "https://www.dukechronicle.com/",
        },
        {
            img: "mastheads/dth-masthead.png",
            url: "https://www.dailytarheel.com/",
        },
        {
            img: "mastheads/nt-masthead.png",
            url: "https://www.ninertimes.com/",
        },
        {
            img: "mastheads/ogb-masthead.png",
            url: "https://wfuogb.com/",
        },
        {
            img: "mastheads/pendulum-masthead.png",
            url: "https://www.elonnewsnetwork.com/",
        },
        {
            img: "mastheads/register-masthead.png",
            url: "https://ncatregister.com/",
        },
        {
            img: "mastheads/seahawk-masthead.png",
            url: "https://theseahawk.org/",
        },
        {
            img: "mastheads/tec-masthead.png",
            url: "https://www.piratemedia1.com/theeastcarolinian/",
        },
        {
            img: "mastheads/technician-masthead.png",
            url: "https://www.technicianonline.com/",
        },
    ];

    const theDailyTarHeelStories = [
        {
            header: "Study examines mental health impact of campus gun-related incidents",
            author: "Lucy Kraus",
            img: "images/dth-university-post-shooting-mental-health.png",
            url: "https://www.dailytarheel.com/article/2024/03/dth-university-post-shooting-mental-health",
            label: "university",
        },
        {
            header: "UNC students of color find mental health support through community",
            author: "Hamsini Sivakumar and Daneen Khan",
            img: "images/20240201-gao-Dth-university-lifestyle-mental-health-experience-as-poc-at-pwi.jpg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/dth-university-lifestyle-mental-health-experience-as-poc-at-pwi-caps-latinx-center"
        },
        {
            header: "'It's OK to ask for assistance': how UNC's elite athletes use mental health as an edge",
            author: "Shelby Swanson",
            img: "images/Dth-sports-feature-rucker-mental-health.jpeg",
            label: "sports",
            url: "https://www.dailytarheel.com/article/2024/03/sports-mental-health-athletes-unc-north-carolina-football-field-hockey-kaimon-rucker"
        },
        {
            header: "Club and intramural sports foster community, outlet for UNC students",
            author: "Moira Martin",
            img: "images/im-sports.jpg",
            label: "sports",
            url: "https://www.dailytarheel.com/article/2024/03/club-sports-outlet-mental-health-unc-campus-recreation-justin-ford"
        },
        {
            header: "LGBTQ+ support groups provide community care for substance abuse",
            author: "Eliza Benbow",
            img: "images/Diehl_lifestyle-queer-substance-abuse-solutions.jpeg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/dth-lifestyle-queer-substance-abuse-solutions"
        },
        {
            header: "Culture-responsive care addresses mental health disparities in tribal communities",
            author: "Kaitlyn Church",
            img: "images/20240205_TRAN-lifestyle-indigenous-mental-health-resources-2.jpg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/lifestyle-indigenous-mental-health-in-nc-mental-health-resources"
        },
        {
            header: "'Could have been doing this all along': State budget invests in mental health resources",
            author: "Lucy Marques",
            img: "images/Dth-city-politics-of-mental-funding-state.jpeg",
            label: "city",
            url: "https://www.dailytarheel.com/article/2024/02/dth-city-politics-of-mental-funding-state-legislators-general-assembly-medicaid-services-workforce",
        },
        {
            header: "'Testament to how seriously the state is taking suicide prevention': State launches mental health lifeline dashboard",
            author: "Lola Oliverio",
            img: "images/Dth-city-ncdhhs-mental-health-dashboard-data.jpg",
            label: "city",
            url: "https://www.dailytarheel.com/article/2024/02/city-child-behavioral-health-dashboard-north-carolina-dhhs",
        },
        {
            header: "How two flagship North Carolina universities responded after several student deaths",
            author: "Emmy Martin and Emily Vespa",
            img: "images/dth–technician-mental-health-public-suicide.jpg",
            label: "collaboration",
            url: "https://www.dailytarheel.com/article/2024/03/how-two-flagship-north-carolina-universities-responded-after-several-student-deaths"
        },
        {
            header: "Op-ed: It's time to replace the word 'stigma' with 'sanism'",
            author: "Krista Savage-White",
            img: "images/dth-default.png",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/03/dth-oped-replace-stigma-with-sanism#:~:text=Sanism%20identifies%20how%20attitudes%20surrounding,of%20topics%2C%20political%20or%20not.",
        },
        {
            header: "Community members find mental health relief in spirituality",
            author: "Marisa Rosa",
            img: "images/dth-lifestyle-mental-health-spirituality.jpeg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/dth-lifestyle-mental-health-spirituality",
        },
        {
            header: "Column: Mental health is generational in minority communities. Acknowledge it",
            author: "Ankur Mutyala",
            img: "images/dth-opinion-generational-mental-health.jpeg",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/03/opinion-generational-mental-health"
        },
        {
            header: "Op-ed: Make space to help those struggling with their mental health",
            author: "Lior Vered-Langley",
            img: "images/dth-default.png",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/03/dth-oped-sucide-prevention"
        },
        {
            header: "Elected officials must do more for mental health",
            author: "the Editorial Board",
            img: "images/calling-out-elected-officials.jpg",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/03/dth-opinion-editorial-calling-out-elected-officials-real"
        },
        {
            header: "Mental health providers, patients face inconsistencies in insurance coverage",
            author: "Tori Newby and Maddie Policastro",
            img: "images/Dth-city-insurance-coverage-gap-statewide-solution.jpeg",
            label: "city",
            url: "https://www.dailytarheel.com/article/2024/02/dth-city-insurance-coverage-gap-statewide-solution",
        },
        {
            header: "Criminal justice diversion programs redirect, guide individuals",
            author: "Sarah Smiley",
            img: "images/20200208_dth-city-orange-county-diversion-program-solutions.jpeg",
            label: "city",
            url: "https://www.dailytarheel.com/article/2024/03/dth-city-orange-county-diversion-program-solutions"
        },
        {
            header: "'It's about the process': Art therapy provides creative outlet as mental health care",
            author: "Mila Mascenik and Sophia Melin",
            img: "images/Dth-lifestyle-alternative-forms-of-therapy-in-arts.jpeg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/dth-lifestyle-alternative-forms-of-therapy-in-arts"
        },  
        {
            header: "The Farm at Penny Lane grows hope through therapy programs",
            author: "Madison Gagnon",
            img: "images/contrib-dth-lifestyle-farm-helping-mental-health-solutions.jpg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/dth-lifestyle-farm-at-penny-lane-unc-chapel-hill-mental-health"
        },
        {
            header: "Health humanities laboratory looks to bridge medical, social sciences",
            author: "Charlene Wu",
            img: "images/Dth-lifestyle-health-humanities-mental-health-creative-solutions.jpeg",
            label: "lifestyle",
            url: "https://www.dailytarheel.com/article/2024/03/lifestyle-health-humanities-mental-health-creative-solutions-unc"
        },
        {
            header: "'Therapy should be affordable to everyone': CAPS addresses financial burdens of therapy",
            author: "Samantha Nichols",
            img: "images/dth-university-mental-health-cost-breakdown.png",
            label: "university",
            url: "https://www.dailytarheel.com/article/2024/02/dth-university-access-to-mental-health-cost-breakdown",
        },
        {
            header: "Students and faculty reflect on university well-being days across North Carolina",
            author: "Alli Pardue",
            img: "images/university-well-being-checks-days.png",
            label: "university",
            url: "https://www.dailytarheel.com/article/2024/03/dth-university-well-being-checks-days"
        },
        {
            header: "Op-ed: UNC’s win-at-all-cost attitude jeopardizes the safety of athletes",
            author: "Samuel Long and Olivia Gschwind",
            img: "images/dth-default.png",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/02/dth-oped-athlete-mental-health-unc-swim-and-dive",
        },
        {
            header: "Column: Remission from major depressive disorder is possible",
            author: "Kennedy Cox",
            img: "images/dth-default.png",
            label: "opinion",
            url: "https://www.dailytarheel.com/article/2024/03/donotpub-dth-opinion-alterntive-mh-treatments",
        },
    ];

    const thePendulumStories = [
        {
            header: "Phoenix Free: Sobriety on campus",
            author: "Avery Sloan",
            img: "images/phoenixfree.png",
            label: "University",
            url: "https://www.elonnewsnetwork.com/article/2024/03/phoenix-free-sobriety-on-campus"
        },
        {
            header: "College culture’s influence on eating disorders",
            author: "Nia Bedard",
            img: "images/EatingDisorders.jpg",
            label: "University",
            url: "https://www.elonnewsnetwork.com/article/2024/03/elon-professor-sheds-light-college-students-eating-disorders"
        },
        {
            header: "HealthEU moves toward new wellness center",
            author: "Lilly Molina",
            img: "images/healthEU.JPG",
            label: "University",
            url: "https://www.elonnewsnetwork.com/article/2024/03/healtheu-moves-toward-new-wellness-center"
        },
    ];

    const oldGoldAndBlackStories = [
        {
            header: "If You’re Reading This: Student-led mental health resource offers fresh perspectives",
            author: "Aaron Nataline",
            url: "https://wfuogb.com/23721/special-editions/ifyourereadingthis-student-led-mental-health-resource-offers-fresh-perspectives/",
            img: "images/ogb-harris-ifyourereadingthis-feature.jpg",
            label: "University",
        },
        {
            header: "The UCC’s journey from pandemic pitfalls and back",
            author: "Breanna Laws",
            img: "images/ogb-CC-mh-2.jpg",
            label: "University",
            url: "https://wfuogb.com/23730/special-editions/the-uccs-journey-from-pandemic-pitfalls-and-back/"
        },
        {
            header: "How Wake Forest trains its faculty to be on the frontline of mental health care",
            author: "Christa Dutton",
            img: "images/how-train.jpg",
            label: "University",
            url: "https://wfuogb.com/23726/special-editions/how-wake-forest-trains-its-faculty-to-be-on-the-front-line-of-mental-health-care/"
        },
    ];

    const nineTimeStories = [
        {
            header: "How UNC Charlotte’s student support organizations help international students with off-campus housing challenges",
            author: "Sunnya Hadavi and AJ Siegel ",
            img: "images/grad-housing.png",
            url: "https://www.ninertimes.com/news/how-unc-charlotte-s-student-support-organizations-help-international-students-with-off-campus-housing-challenges/article_a2aa7ba8-e58b-11ee-bf7d-53ab7eded94a.html",
            label: "City & State",
        },
        {
            header: "Partnership between AthleteTalk and Charlotte Athletics is helping student-athletes grow mental health literacy",
            author: "Bryson Foster ",
            img: "images/niner-times-sports-student-athlete-mental-health-graphic.jpg",
            url: "https://www.ninertimes.com/news/partnership-between-athletetalk-and-charlotte-athletics-is-helping-student-athletes-grow-mental-health-literacy/article_5b35db4a-e58c-11ee-9a60-ef6e8b54e0a4.html",
            label: "sports",
        },
    ];

    const theSeahawkStories = [
        {
            header: "Community, Isolation and Politics: The Mental Health of Queer Students at UNCW",
            author: "Hannah Markov",
            img: "images/sh-ph.jpeg",
            label: "University",
            url: "https://theseahawk.org/36076/showcase/community-isolation-and-politics-the-mental-health-of-queer-students-at-uncw/"
        },
    ];

    const theEastCarolinianStories = [
        {
            header: "The community building within ECU",
            author: "Kiarra Crayton",
            img: "images/team.jpg",
            label: "University",
            url: "http://www.piratemedia1.com/theeastcarolinian/article_0f4e95ba-e649-11ee-8fef-7b074c40d8db.html"
        },
        {
            header: "Morgan’s Message spreads mental health awareness in student-athletes",
            author: "Kiarra Crayton",
            img: "images/morgan-message.JPG",
            label: "University",
            url: "http://www.piratemedia1.com/theeastcarolinian/article_72cbd932-e648-11ee-9019-ff593a101979.html"
        },
    ];

    const aAndTRegisterStories = [
        {
            header: "The state of mental health at N.C. A&T and where it can improve",
            author: "Rosegalie Cineus and Kaila Collier",
            img: "images/aandt-mentalphealth.jpg",
            label: "University",
            url: "https://ncatregister.com/22317/the-yard/mental-health-edition/the-state-of-mental-health-at-n-c-at/"
        },
        {
            header: "HBCUs grapple with tuition increases and student mental health",
            author: "Dasia Williams",
            img: "images/ncat-services.png",
            label: "University",
            url: "https://ncatregister.com/22322/the-yard/mental-health-edition/hbcus-grapple-with-tuition-increases-and-student-mental-health/"
        },
    ];

    const theChronicleStories = [
        {
            header: "Duke researchers work on mental wellbeing studies exploring how we think, feel and socialize",
            author: "Winston Qian",
            img: "images/duke-medical-school-stock.jpg",
            label: "University",
            url: "https://www.dukechronicle.com/article/2024/03/duke-university-exploring-how-we-think-feel-socialize-mental-health-research-a-look-into"
        },
    ];

    const technicianStories = [
        {
            header: "Campus community uses AI to address mental health",
            author: "Ethan Bakogiannis and Jameson Wolf",
            img: "images/tech-stem-graphic.PNG",
            url: "https://www.technicianonline.com/campus-community-uses-ai-to-address-mental-health/article_783976b2-e590-11ee-9a4b-7ba3b69aa934.html",
            label: "University",
        },
        {
            header: "How we talk about suicide online matters",
            author: "Kate Denning",
            img: "images/tech-how-we-talk.png",
            url: "https://www.technicianonline.com/opinion-how-we-talk-about-suicide-online-matters/article_5f3104a6-e58f-11ee-8d68-1f50c1a1f39a.html",
            label: "Opinion",
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
        invertColors={true}
        img={"images/main-art.png"}
        imgSize={"80%"}
        size={100}
        normalImg={false}
    >
        <div slot="text">
            <h1 style:font-size={"40px"}>A statewide issue.</h1>
            <p
                style:font-size={"1.2em"}
                style:line-height={"26px"}
                style:padding={"0 60px"}
            >
                Nine North Carolina college newsrooms partner to cover the
                mental health crisis faced by their communities
            </p>
        </div>
    </Feature>
</div>

<Navbar
    data={[
        { url: "#introduction", text: "Welcome" },
        { url: "#the-daily-tar-heel", text: "The Daily Tar Heel" },
        { url: "#the-pendulum", text: "The Pendulum" },
        { url: "#old-gold-and-black", text: "Old Gold & Black" },
        { url: "#nine-times", text: "Niner Times" },
        { url: "#the-east-carolinian", text: "The East Carolinian" },
        { url: "#a-and-t-register", text: "A&T Register" },
        { url: "#technician", text: "Technician" },
        { url: "#the-seahawk", text: "The Seahawk" },
        { url: "#the-chronicle", text: "The Chronicle" },
    ]}
/>

<main>
    <div class="columns anchor-wrapper">
        <span class="anchor" id="introduction"></span>
        <h2>Behind the Mental Health Collaborative</h2>
        <p class="author" style:line-height={"19px"}>
            By <a href="https://www.dailytarheel.com/staff/emmy-martin"
                >Emmy Martin</a
            ><br /><span class="byline"
                >Editor-in-Chief of The Daily Tar Heel</span
            >
        </p>
        <div style:margin-top={"15px"}>
            <TextColumns numberOfCols={2}>
                <span class="column">
                    <p style:margin-top={0}>
                        Every time I walk through the Pit at UNC, I remember the
                        sticky notes and flowers left on those green chairs
                        three years ago. I remember the candles that sat at
                        their feet, the messages written in chalk on the bricks.
                    </p>
                    <p>
                        “Your fire will never truly die,” the largest chalk
                        message said. I remember the four students who died by
                        suicide that semester.
                    </p>
                    <p>
                        The mental health crisis we face has not subsided. Last
                        year, N.C. State lost seven students to suicide. From
                        2016 to 2020, there were 878 deaths by suicide of people
                        ages 15 to 24 in North Carolina. A national survey
                        conducted by the American College Health Association
                        found that 52 percent of undergraduate students
                        regularly experienced moderate psychological distress.
                        While this problem isn’t new, it feels more important
                        than ever.
                    </p>
                    <p>
                        That’s why The Daily Tar Heel partnered with eight other
                        college newspapers to report on mental health challenges
                        shared by those in each of their communities. This
                        Mental Health Collaborative is the result of months of
                        rigorous reporting, research, conversations, writing,
                        editing and designing. This initiative began in 2023
                        when The Daily Tar Heel was awarded a grant from the
                        Solutions Journalism Network as part of its Student
                        Media Challenge initiative. That grant helped fund the
                        collaborative work of this project. Many of the stories
                        you will read in this collaborative do more than just
                        present a problem — they also explore solutions to this
                        crisis.
                    </p>
                    <p>
                        The Daily Tar Heel is honored to have had the privilege
                        of working with The A&T Register, The Duke Chronicle,
                        The East Carolinian, The Niner Times, The Old Gold &
                        Black, The Pendulum, The Seahawk and Technician on this
                        project.
                    </p>
                    <p>
                        With more than 30 reported stories and seven opinion
                        pieces, we touch on many issues related to mental
                        health, from how Wake Forest University trains its
                        faculty to be on the frontline of mental health care to
                        how international students create community at East
                        Carolina University.
                    </p>
                    <p>
                        While there’s still more that must be done, this is a
                        step toward that future. As we navigate the complexities
                        of mental health, we must not lose sight of the
                        individual people behind the statistics — the students,
                        faculty, families and communities affected. Their
                        stories, their struggles and their resilience should
                        serve as a guiding light. We hope that this mental
                        health collaborative project serves as a call to action
                        to create a future where no one suffers in silence.
                    </p>
                </span>
            </TextColumns>
        </div>
    </div>
    <div style="margin: 40px auto; width: fit-content;">
        <LogoGrid {logoList} />
    </div>
</main>
<div class="black-back">
    <Feature
        img={"images/university-well-being-checks-days.png"}
        textLeft={false}
        invertColors={true}
    >
        <Article
            slot="text"
            headline={"Students and faculty reflect on university well-being days across North Carolina"}
            author={"Alli Pardue"}
            summary={"Six schools out of the 17 within the UNC System have instituted wellness days this year. UNC-CH's well-being days — initially called wellness days — began in fall 2020 as a response to students requesting more breaks.<br>Former Chancellor Kevin Guskiewicz and former Provost Robert Blouin said the days off would replace the campus’s 2021 spring break in an effort to limit the spread of COVID-19."}
            headerSize={28}
            invertColors={true}
            newspaper={"The Daily Tar Heel"}
            label={"university"}
            url={"https://www.dailytarheel.com/article/2024/03/dth-university-well-being-checks-days"}
        />
    </Feature>
</div>
<main>
    <div class="carousel-container article-set case anchor-wrapper">
        <span class="anchor" id="the-daily-tar-heel"></span>
        <ArticleCase
            headerImg={"mastheads/dth-masthead.png"}
            articleData={theDailyTarHeelStories}
        />
    </div>
</main>
<div class="black-back">
    <Feature
        img={"images/dth–technician-mental-health-public-suicide.jpg"}
        invertColors={true}
    >
        <Article
            slot="text"
            headline={"How two flagship North Carolina universities responded after several student deaths"}
            author={"Emmy Martin and Emily Vespa"}
            summary={"After more than 10 students died by suicide on their campuses over the last few years, UNC-CH and N.C. State partnered with The Jed Foundation to improve mental health programs and suicide prevention efforts and revised their postvention student death protocols."}
            headerSize={28}
            newspaper={"The Daily Tar Heel & Technician"}
            invertColors={true}
            label={"University"}
            url={"https://www.dailytarheel.com/article/2024/03/how-two-flagship-north-carolina-universities-responded-after-several-student-deaths"}
        />
    </Feature>
</div>
<main>
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
</main>
<div class="black-back">
    <Feature
        img={"images/grad-housing.png"}
        textLeft={false}
        invertColors={true}
    >
        <Article
            slot="text"
            headline={"How UNC Charlotte’s student support organizations help international students with off-campus housing challenges"}
            author={"Sunnya Hadavi and AJ Siegel"}
            headerSize={28}
            summary={"At UNC Charlotte, the Triveni Indian Student Association helps international students with housing maintenance and damages, advocating on their behalf and pushing landowners to resolve problems promptly."}
            newspaper={"The Niner Times"}
            invertColors={true}
            label={"City & State"}
            url={"https://www.ninertimes.com/news/how-unc-charlotte-s-student-support-organizations-help-international-students-with-off-campus-housing-challenges/article_a2aa7ba8-e58b-11ee-bf7d-53ab7eded94a.html"}
        />
    </Feature>
</div>
<main>
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
</main>
<div class="black-back">
    <Feature
        img={"images/tech-how-we-talk.png"}
        textLeft={true}
        invertColors={true}
    >
        <Article
            slot="text"
            headline={"How we talk about suicide online matters"}
            author={"Ethan Bakogiannis and Jameson Wolf"}
            label={"COLUMN"}
            summary={"Media coverage is a primary driving factor in suicide contagion, when exposure to a suicide leads to increased risk of suicidal behavior. Researchers have developed guidelines for responsible reporting on suicide, and, when followed, these guidelines can successfully reduce the risk of contagion."}
            headerSize={28}
            newspaper={"Technician"}
            invertColors={true}
            url={"https://www.technicianonline.com/opinion-how-we-talk-about-suicide-online-matters/article_5f3104a6-e58f-11ee-8d68-1f50c1a1f39a.html"}
        />
    </Feature>
</div>
<main>
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
</main>
<div class="black-back">
    <Feature
        img={"images/ogb-CC-mh-2.jpg"}
        invertColors={true}
        textLeft={false}
    >
        <Article
            slot="text"
            headline={"The UCC’s journey from pandemic pitfalls and back"}
            summary={"The COVID-19 pandemic posed challenges to the Wake Forest University Counseling Center and forced the center to adapt its methods.<br>Now, with the acute challenges of the pandemic largely subsided, the Wake Forest University Counseling Center has increased its satisfaction rating among students."}
            author={"Breanna Laws"}
            headerSize={28}
            newspaper={"Old Gold & Black"}
            invertColors={true}
            label={"University"}
            url={"https://wfuogb.com/23730/special-editions/the-uccs-journey-from-pandemic-pitfalls-and-back/"}
        />
    </Feature>
</div>
<main>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-east-carolinian"></span>
        <ArticleSet
            sizePct={70}
            articleData={theEastCarolinianStories}
            sideCar={false}
            headerImg={"mastheads/tec-masthead.png"}
        />
    </div>
</main>
<div class="black-back">
    <Feature
        img={"images/Diehl_lifestyle-queer-substance-abuse-solutions.jpeg"}
        invertColors={true}
        textLeft={true}
    >
        <Article
            slot="text"
            headline={"LGBTQ+ support groups provide community care for substance abuse"}
            summary={"After feeling like North Carolina lacked support for members of the LGBTQ+ community struggling with substance abuse, Jemm Merritt-Feder became a certified peer support specialist and founded One Day at a Time, a peer support group for gender-diverse individuals to discuss their experiences with gender transition, mental health and substance abuse in a nonjudgmental space."}
            author={"Eliza Benbow"}
            headerSize={28}
            newspaper={"The Daily Tar Heel"}
            invertColors={true}
            label={"Lifestyle"}
            url={"https://www.dailytarheel.com/article/2024/03/dth-lifestyle-queer-substance-abuse-solutions"}
        />
    </Feature>
</div>
<main>
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
</main>
<div class="black-back">
    <Feature
        img={"images/20240201-gao-Dth-university-lifestyle-mental-health-experience-as-poc-at-pwi.jpg"}
        invertColors={true}
        textLeft={false}
    >
        <Article
            slot="text"
            headline={"UNC students of color find mental health support through community"}
            summary={"As of fall 2023, 54.5 percent of UNC’s student population identified as white, while approximately 13 percent of the student population identified as Asian, nine percent as Hispanic and around nine percent as Black or African-American."}
            author={"Hamsini Sivakumar and Daneen Khan"}
            headerSize={28}
            newspaper={"The Daily Tar Heel"}
            invertColors={true}
            label={"Lifestyle"}
            url={"https://www.dailytarheel.com/article/2024/03/dth-university-lifestyle-mental-health-experience-as-poc-at-pwi-caps-latinx-center#:~:text=For%20students%20of%20color%20seeking,UNC%20double%2Dalumna%20Theresa%20Flores"}
        />
    </Feature>
</div>
<main>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="technician"></span>
        <ArticleSet
            sizePct={70}
            articleData={technicianStories}
            sideCar={false}
            headerImg={"mastheads/technician-masthead.png"}
            imgSize={175}
        />
    </div>
</main>
<div class="black-back">
    <Feature
        img={"images/calling-out-elected-officials.jpg"}
        invertColors={true}
        textLeft={true}
    >
        <Article
            slot="text"
            headline={"Elected officials must do more for mental health"}
            summary={"Alleviating issues like community violence and student safety begins with mental health. It is essential that our legislators commit to representing their constituents by addressing the lack of adequate funding towards improved mental health services as well as their accessibility."}
            author={"Editorial Board"}
            headerSize={28}
            newspaper={"The Daily Tar Heel"}
            invertColors={true}
            label={"Opinion"}
            url={"https://www.dailytarheel.com/article/2024/03/dth-opinion-editorial-calling-out-elected-officials-real"}
        />
    </Feature>
</div>
<main>
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-seahawk"></span>
        <ArticleSet
            sizePct={70}
            articleData={theSeahawkStories}
            sideCar={false}
            headerImg={"mastheads/seahawk-masthead.png"}
        />
    </div>
    <hr />
    <div class="article-set case anchor-wrapper">
        <span class="anchor" id="the-chronicle"></span>
        <ArticleSet
            sizePct={70}
            articleData={theChronicleStories}
            sideCar={false}
            headerImg={"mastheads/dtc-masthead.png"}
            imgSize={200}
        />
    </div>
</main>
<footer>
    <div class="footer-wrapper">
        <section class="footer-grid">
            <p>
                <b>Mental Health Resources</b><br />
                Call or text 988 or chat online if you’re thinking about suicide,
                are worried about a friend or need emotional support. Text START
                to the Crisis Text Line at 741-741.
            </p>
            <div>
                <p>
                    Click here to read these stories in The Daily Tar Heel’s Special Edition Mental Health Newspaper
                </p>
                <p>
                    Special thanks to the <a
                        href="https://www.solutionsjournalism.org/"
                        >Solutions Journalism Network</a
                    > for funding this collaborative project.
                </p>
                <p>Developed by Leo Davidson</p>
            </div>
        </section>
    </div>
</footer>

<style>
    main {
        margin: auto;
        width: 90%;
    }

    hr {
        border: #e4e3e3 solid 1px;
        width: 75%;
    }

    footer {
        width: 100%;
        background-color: var(--black);
        color: var(--white);
        padding: 60px 0;
    }

    .footer-logo {
        margin: auto;
    }

    .footer-wrapper {
        width: 50%;
        text-align: center;
        margin: auto;
    }

    .footer-grid {
        display: grid;
        grid-template-columns: auto auto;
        gap: 20px;
    }

    .footer-wrapper p {
        font-family: Arial, sans-serif;
    }

    .footer-wrapper a {
        font-family: Arial, sans-serif;
        color: var(--white);
    }

    .footer-wrapper p b {
        font-family: Georgia, serif;
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
    }

    .case {
        margin: 80px auto;
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

    @media only screen and (max-width: 900px) {
        .columns {
            width: 80%;
        }
    }

    @media only screen and (max-width: 750px) {
        .footer-grid {
            grid-template-columns: auto;
        }

        .footer-wrapper {
            width: 75%;
        }
    }
    .carousel-container {
        width: 100%;
    }

    .article-set {
        width: 100%;
    }
</style>
