<script>
    // Height/width of a 1:1 `Panel` on desktop screens,
    // higher size `Panel`s derived from this. Disregarded on mobile screens.
    export let panelSize = 180;

    // The number of columns to display the `Panel`s in. The number of `Panel`s this
    // allows to fit on one row is determined by each `Panel`'s `width`.
    export let columns = 4;

    // The number of rows to display the `Panel`s in. The number of `Panel`s this allows
    // to fit on one column is determined by each `Panel`'s `height`.
    export let rows = 4;
    
    $: style = `grid-template: repeat(${rows}, ${panelSize}px) / \
    repeat(${columns}, ${panelSize}px);`
</script>

<div class="panel-group" style={style}>
    <slot></slot>
</div>

<style>
    .panel-group {
        display: grid;
        gap: 24px;
        align-items: stretch;
    }
</style>
