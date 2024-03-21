<script>
    export let img = "";
    export let headline;
    export let summary = "";
    export let author = "";
    export let sideCar = false;
    export let headerSize = 22;
    export let summarySize = 17;
    export let invertColors = false;
    export let url = "";
    export let label = "";
    export let newspaper = "";

    function labelColor(label) {
        let l = label.toLowerCase()
        switch (l) {
            case "university":
                return "#41AD49";
            case "city & state":
                return "#41AD49";
            case "sports":
                return "#D2232A";
            case "lifestyle":
                return "#FB8500";
            case "opinion":
                return "#6F2DBD";
            case "column":
                return "#6F2DBD";
            default:
                return "#cc2626";
        }
    }
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
            {#if label}
                <p class="label" style:color={labelColor(label)}>{label}</p>
            {/if}
            {#if url}
                <a href={url}>
                    <h3
                        style="font-size: {headerSize}px;"
                        style:color={invertColors
                            ? "var(--white)"
                            : "var(--black)"}
                    >
                        {headline}
                    </h3>
                </a>
            {:else}
                <h3
                    style="font-size: {headerSize}px;"
                    style:color={invertColors ? "var(--white)" : "var(--black)"}
                >
                    {headline}
                </h3>
            {/if}
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
                <p class="author">By {author}
                    {#if newspaper}
                        <br>{newspaper}
                    {/if}
                </p>
            {/if}
        </div>
    </div>
</div>

<style>
    a {
        text-decoration: none;
        color: unset;
    }
    a:hover {
        text-decoration: underline;
    }

    .label {
        font-family: Arial, sans-serif;
        font-size: 14px;
        font-weight: 600;
        margin: 0;
        text-transform: uppercase;
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
        max-width: 400px;
        margin: 10px auto;
    }
    img {
        width: 100%;
        aspect-ratio: 3/2;
        object-fit: cover;
    }
    h3 {
        line-height: 1.27273em;
        font-weight: 600;
    }
    h3,
    p {
        margin: 10px 0 0px 0;
    }
    p {
        line-height: 1.41176em;
    }
</style>
