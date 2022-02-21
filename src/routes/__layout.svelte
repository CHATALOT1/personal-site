<script>
    import Footer from "$lib/Footer.svelte";
    import Theme from "$lib/Theme.svelte";

    let rows;
</script>

<Theme>
    <header>
        <h1>CHATALOT</h1>
    </header>

    <main>
        <slot />
    </main>

    <Footer />
</Theme>

<style>
    /* Base */
    :global(html) {
        font-size: 32px;
        line-height: 90%;
        text-align: center;
        height: 100%;
        font-family: "Dongle", sans-serif;
        color: var(--text-color);
    }
    :global(body) {
        margin: 0;
        background-image: linear-gradient(to left bottom, var(--bg-gradient-start), var(--bg-gradient-end));
        background-attachment: fixed;
    }
    :global(a) {
        text-decoration: none;
        color: var(--emphasis-color);
    }
    :global(.small) {
        font-size: 70%;
    }
    main {
        display: table;
        margin: 12px auto;
    }
    

    /* Fonts */
    
    /* dongle-regular - latin */
    @font-face {
    font-family: 'Dongle';
    font-style: normal;
    font-weight: 400;
    src: local(''),
        url('/fonts/dongle-v6-latin-regular.woff2') format('woff2'), /* Chrome 26+, Opera 23+, Firefox 39+ */
        url('/fonts/dongle-v6-latin-regular.woff') format('woff'); /* Chrome 6+, Firefox 3.6+, IE 9+, Safari 5.1+ */
    }
</style>