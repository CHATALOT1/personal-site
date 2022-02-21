<script>
    import Panel from "$lib/layout/Panel.svelte";
    import Page from "$lib/Page.svelte";
</script>

<svelte:head>
    <title>CHATALOT - About</title>
</svelte:head>

<Page rows={7}>
    <Panel width=2 link="https://jeremynoesen.xyz">
        <p>
            This website is made from scratch, but takes heavy inspiration from the site
            of Jeremy Noeson with explicit permission from him. Click on this panel to
            visit it.
        </p>
    </Panel>
    <Panel width=2 height=2>
        <h2>Hi! I'm Sylvia!</h2>
        <p>Often known on the internet as CHATALOT or CHATALOT1.</p>
        <p>
            This site was created to showcase some of my projects, act as a small
            personal blog to keep me motivated, acquire some experience with Svelte, and
            because, frankly, I wanted a personal site.
        </p>
        <p class="small">(All the cool kids have one)</p>
    </Panel>
    <Panel width=2 height=5>
        <h2>Learning to program</h2>
        <p>
            I've always been interested in technology and "how things work", ever since
            even before I could walk.
        </p>
        <p>
            In primary school, this interest was somewhat recognised and I was taught
            some of the absolute basics of programming. However, my interest dawdled as
            the curriculum was heavily limited.
        </p>
        <p>
            Over the years, I briefly attempted to get back into programming many times,
            and from various angles.
        </p>
        <p>
            Some time later, and towards the end of the two years that I spent out of
            formal education for personal reasons, I became interested in creating
            automations ('bots') for Discord. Before too long, this curiosity grew and
            yet again rekindled my inspiration to become a programmer!
        </p>
        <p>
            I attended a one-week summer camp to learn Python but once again got
            frustrated with the limited curriculum. Before I had even finished the week,
            I was furthering my knowledge on my own in the evenings after it ended,
            using online resources.
        </p>
    </Panel>
    <Panel width=2 height=3>
        <h2>Onwards and upwards!</h2>
        <p>
            After I began to learn programming properly, I couldn't stop myself from
            exploring as many avenues as I was drawn to, diversifying and expanding my
            knowledge constantly.
        </p>
        <p>
            This trend carries on to this day, and I often find myself eager to learn
            new programming languages and frameworks.
        </p>
        <p>
            My brain provides a constant stream of ideas that I can sometimes struggle
            to keep up with and my curiosity powers me to learn new tools all the time.
        </p>
    </Panel>
    <Panel width=2 height=2 link="https://github.com/ganymeade">
        <h2>What do I do now?</h2>
        <p>
            I am currently preparing to work on Ganymeade RPG by learning the
            technologies that I believe will benefit the project most.
        </p>
        <p class="small">(Click me to go to the Github org!)</p>
    </Panel>
    <Panel width=2 link="/projects">
        <h2>What have I done?</h2>
        <p>Click here to go to the projects page and see what I have created.</p>
    </Panel>
</Page>