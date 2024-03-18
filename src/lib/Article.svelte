<script>
    export let img = "";
    export let headline;
    export let summary = "";
    export let author = "";
    export let sideCar = false;
    export let headerSize = 22;
    export let summarySize = 17;
    export let invertColors = false;
    export let isLink = true;
    export let url = "";
</script>

<div class="article">
    <div
        class="wrapper"
        style:display={sideCar ? "grid" : "unset"}
        style:align-items={sideCar ? "center" : "unset"}
    >
        {#if img}
            <img src={img} alt={headline} />
        {/if}
        <div class="text-wrapper">
            <h3 style="font-size: {headerSize}px;" style:color={invertColors ? "var(--white)" : "var(--black)"}>{headline}</h3>
            {#if summary}
                <p
                    class="summary"
                    style="font-size: {summarySize}px;"
                    style:color={invertColors ? "var(--white)" : "var(--black)"}
                >
                    {summary}
                </p>
            {/if}
            {#if author}
                <p class="author">By {author}</p>
            {/if}
        </div>
    </div>
</div>

<style>
    a {
        text-decoration: none;
        color: unset;
    }
    .text-wrapper {
        /* margin: 0 10px; */
    }
    .wrapper {
        outline-offset: 5px;
        margin: 5px 10px;
        overflow: hidden;
        grid-template-columns: auto auto;
        gap: 20px;
    }
    .article {
        display: flex;
    }
    img {
        width: 100%;
        object-fit: cover;
    }
    h3 {
        line-height: 1.27273em;
        font-weight: 600;
    }
    h3,
    p {
        margin: 10px 0;
    }
    p {
        line-height: 1.41176em;
    }
</style>
