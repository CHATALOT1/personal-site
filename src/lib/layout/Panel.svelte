<script>
    // Relative width and height compared to other panels in its PanelGroup,
    // both values multiplied by panelSize in normal mode.
    export let width = 1;
    export let height = 1;

    // Is this panel a button link that the user can click?
    export let link = "";

    // The colour used to highlight panels when hovered over by the user
    export let highlight = "var(--emphasis-color)";

    $: imageWidth = `${(0.5 ** width) * 100}%`
    $: imageHeight = `${(0.5 ** height) * 100}%`

    $: style = `grid-column: span ${width}; grid-row: span ${height}; \
    --image-width: ${imageWidth}; --image-height: ${imageHeight}; \
    --highlight: ${highlight};`
</script>

{#if link}
    <a href={link} class="panel button" style={style}>
        <slot />
    </a>
{/if}

{#if !link}
    <div class="panel" style={style}>
        <slot />
    </div>
{/if}

<style>
    a {
        color: inherit;
    }
    .panel {
        display: flex;
        height: 100%;
        width: 100%;
        flex-direction: column;
        border-radius: 32px;
        box-shadow: -6px 8px 12px var(--panel-shadow);
        transition: transform 0.25s cubic-bezier(0.5, 0, 0.25, 2), box-shadow 0.25s cubic-bezier(0.5, 0, 0.25, 2), background-color 0.25s, color 0.25s;
        text-decoration: none;
        place-items: center;
        justify-content: center;
    }
    .panel:hover {
        transform: scale(1.015);
        background-color: var(--highlight);
        color: var(--text-hover);
    }
    .button:hover {
        transform: translateY(8px);
        box-shadow: -12px 16px 24px var(--panel-shadow-hover);
    }
    .button:active {
        transform: translateY(12px);
    }

    /* Apply globally to panel children */
    :global(.panel *) {
        display: flex;
    }
    :global(.panel p) {
        color: var(--paragraph-color);
        margin: 0.4em;
        transition: inherit;
    }
    :global(.panel:hover p) {
        color: var(--paragraph-hover);
    }
    :global(.panel svg) {
        width: var(--image-width);
        height: var(--image-height);
    }
    :global(.panel h1) {
        font-size: 60px;
    }
    :global(.panel h2) {
        margin: 0;
    }
</style>
