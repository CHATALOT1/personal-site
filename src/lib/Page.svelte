<script>
    import PanelGroup from "./layout/PanelGroup.svelte";
    import NavButtons from "./NavButtons.svelte";

    export let rows = 2;
    // One row is added for the `NavButtons`.
    rows += 1
</script>

<PanelGroup {rows}>
    <NavButtons />
    <slot></slot>
</PanelGroup>