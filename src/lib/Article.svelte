<script>
    export let img = "";
    export let headline;
    export let summary = "";
    export let author;
</script>

<div class="article">
    <div class="wrapper">
        {#if img}
            <img src={img} alt={headline} />
        {/if}
        <div class="text-wrapper">
            <h3>{headline}</h3>
            {#if summary}
                <p class="summary">{summary}</p>
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
    }
    .article {
        display: inline;
    }
    img {
        width: 100%;
        object-fit: cover;
    }
    h3 {
        line-height: 1.27273em;
        font-size: 22px;
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
        font-size: 17px;
    }
    .author {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 600;
        font-size: 14px;
    }
</style>
