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

<nav bind:this={navbarElement} class="{isSticky ? 'sticky' : ''}">
    <ul>
        {#each data as { text, url }}
            <li>
                <a href={url}>{text}</a>
            </li>
        {/each}
    </ul>
</nav>

<style>
    ul {
        display: flex;
        list-style: none;
        padding: 0;
        margin: auto;
        width: fit-content;
    }

    li {
        margin: 0 20px;
    }

    a {
        text-decoration: none;
        color: #000;
        font-family: Arial, sans-serif;
        font-weight: 600;
    }

    nav {
        width: 100%;
        padding: 20px 0;
        border-bottom: #000 solid 1px;
        background-color: #fff;
        z-index: 999;
    }
</style>
