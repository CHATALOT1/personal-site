<script>
    import Page from "./Page.svelte";
    import Panel from "./layout/Panel.svelte";
</script>

<Page rows={2}>
    <Panel width=4>
        <slot />
    </Panel>
    <Panel width=4 link="/">
        <h2>Click here to return to the home page</h2>
    </Panel>
</Page>