<script>
    import Error from "$lib/Error.svelte";

    import { page } from "$app/stores";

    $: status = $page.status
</script>

<svelte:head>
    <title>CHATALOT - Error</title>
</svelte:head>

{#if status == "404"}
    <Error>
        <h2>The page you're looking for couldn't be found</h2>
    </Error>
{:else}
    <Error>
        <h2>An unknown error occured</h2>
    </Error>
{/if}