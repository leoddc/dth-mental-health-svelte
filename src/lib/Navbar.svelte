<script>
    import { onMount, onDestroy } from "svelte";
    export let data = [];

    let navbarElement;
    let isSticky = false;

    onMount(() => {
        const sticky = navbarElement.offsetTop;

        function handleScroll() {
            isSticky = window.scrollY >= sticky;
        }

        window.addEventListener("scroll", handleScroll);

        // Cleanup
        return () => {
            window.removeEventListener("scroll", handleScroll);
        };
    });
</script>

<nav bind:this={navbarElement} class={isSticky ? "sticky" : ""}>
    <div class="ul-wrapper">
        <div class="scrollable">
            <ul>
                {#each data as { text, url }}
                    <li>
                        <a href={url}>{text}</a>
                    </li>
                {/each}
            </ul>
        </div>
    </div>
</nav>

<style>
    ul {
        display: flex;
        list-style: none;
        margin: auto;
        padding: 15px 20px;
        width: max-content;
    }

    .scrollable {
        overflow-x: scroll;
    }

    li {
        margin-left: 20px;
    }

    li:nth-child(1) {
        margin-left: 0;
    }

    a {
        text-decoration: none;
        color: #000;
        font-family: Arial, sans-serif;
        font-weight: 600;
    }

    nav {
        width: 100%;
        border-bottom: var(--black) solid 1px;
        background-color: var(--white);
        z-index: 999;
    }

    .ul-wrapper {
        position: relative;
    }

    .ul-wrapper::after {
            content: "";
            position: absolute;
            right: 0;
            bottom: 0;
            width: 60px;
            height: 100%;
            background: linear-gradient(90deg, transparent, var(--white));
            pointer-events: none;
            z-index: 999;
        }
</style>
