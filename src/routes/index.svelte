<script>
    import Panel from "$lib/layout/Panel.svelte";
    import Page from "$lib/Page.svelte";

    import Github from "$lib/svg/Github.svelte";
    import Discord from "$lib/svg/Discord.svelte";
    import Email from "$lib/svg/Email.svelte";
</script>

<svelte:head>
    <title>CHATALOT</title>
</svelte:head>


<Page rows={3}>
    <Panel height=3 width=2>
        <h2>Welcome!</h2>
        <p>
            Take a poke around this website if you'd like to see some of my projects or 
            look at my blog that I use for self-motivation and progress updates.
        </p>
        <p>
            The four buttons on the top can be used to get around, and the buttons on
            the right of this panel can be used to view me on other platforms.
        </p>
        <p>
            Please note that I do not use public social media. Any account that has my
            username on social media is probably not me.
        </p>
    </Panel>
    <Panel width=2 link="https://github.com/CHATALOT1" highlight="#161B22"><Github /></Panel>
    <Panel height=2 link="https://discordapp.com/users/353574266236567556" highlight="#5865F2"><Discord /></Panel>
    <Panel height=2 link="mailto:me@chatalot.xyz" highlight="#FF4040"><Email /></Panel>
</Page>