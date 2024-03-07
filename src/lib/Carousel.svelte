<script>
    export let components = [];
    export let itemsPerSlide = 3;
    export let shiftAmount = 1;

    let currentStartIndex = 0;

    function nextSlide() {
        currentStartIndex =
            (currentStartIndex + shiftAmount) % components.length;
    }

    function prevSlide() {
        currentStartIndex =
            (currentStartIndex - shiftAmount + components.length) %
            components.length;
    }

    $: visibleComponents = [];
    $: {
        const endIndex = currentStartIndex + itemsPerSlide;
        if (endIndex > components.length) {
            visibleComponents = components
                .slice(currentStartIndex, components.length)
                .concat(components.slice(0, endIndex % components.length));
        } else {
            visibleComponents = components.slice(currentStartIndex, endIndex);
        }
    }
</script>

<div class="carousel-container">
    <button on:click={prevSlide}>
        <i class="fa-solid fa-chevron-left"></i>
    </button>
    <div class="carousel-window">
        {#each visibleComponents as component (component.key)}
            <div class="carousel-item">
                <svelte:component
                    this={component.component}
                    {...component.props}
                />
            </div>
        {/each}
    </div>
    <button on:click={nextSlide}>
        <i class="fa-solid fa-chevron-right"></i>
    </button>
</div>

<style>
    .carousel-container {
        display: flex;
        align-items: center;
        margin: 20px auto;
    }
    .carousel-window {
        display: flex;
        overflow: hidden;
        padding: 20px;
    }
    .carousel-item {
        flex: 0 0 auto;
        width: calc(100% / var(--items-per-slide));
        padding: 0 10px;
        display: flex;
    }
    button {
        background-color: unset;
        border: none;
    }
    button:hover {
        cursor: pointer;
    }
</style>
