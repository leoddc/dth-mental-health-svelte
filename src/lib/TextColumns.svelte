<script>
    export let numberOfCols = 1;
</script>

<div class="text-columns" style="--numberOfCols: {numberOfCols};">
    <slot />
</div>

<style>
    .text-columns {
        column-count: var(--numberOfCols, 1);
        column-gap: 35px;
        text-align: justify;
    }
</style>
