<script>
    export let img = "";
    export let headline;
    export let summary = "";
    export let author;
    export let sideCar = false;
    export let headerSize = 22;
    export let summarySize = 17;
</script>

<div class="article">
    <div class="wrapper" style:display={sideCar ? "grid" : "unset"} style:align-items={sideCar ? "center" : "unset"}>
        {#if img}
            <img src={img} alt={headline} />
        {/if}
        <div class="text-wrapper">
            <h3 style="font-size: {headerSize}px;">{headline}</h3>
            {#if summary}
                <p class="summary" style="font-size: {summarySize}px;">{summary}</p>
            {/if}
            <p class="author">By {author}</p>
        </div>
    </div>
</div>

<style>
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
    .summary {
        color: #353535;
    }
    .author {
        font-family: Helvetica, sans-serif;
        font-weight: 600;
        font-size: 14px;
    }
</style>
