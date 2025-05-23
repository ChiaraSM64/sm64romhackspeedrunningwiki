<script>
    import Sidebar from './Sidebar.svelte';

    let { children } = $props();
</script>

<div class="wrapper">
    <Sidebar />

    <div class="content">
        {@render children()}
    </div>
</div>

<style>
    :global(h1) {
        font-size: 1.88em;
        margin: 20px 0;
        border-bottom: 1px solid #CCC;
        font-family: Georgia;
        font-weight: normal;
    }

    :global(h1:first-child) {
        margin-top: 10px;
    }

    :global(h2) {
        font-size: 1.25em;
        margin: 15px 0;
        border-bottom: 1px solid #CCC;
        font-family: Georgia;
        font-weight: normal;
    }

    :global(h3) {
        font-size: 1em;
        margin: 15px 0;
        font-family: Arial;
        font-weight: 700;
    }

    :global(p) {
        font-size: 0.9em;
        margin: 20px 0;
        font-family: Arial;
    }

    :global(a:not(:hover)) {
        text-decoration: none;
    }

    :global(ol) {
        font-size: 0.9em;
        margin: 0;
    }

    :global(ol ul) {
        margin: 10px 0;
        padding: 0 20px;
        list-style-type: disc;
    }

    :global(li.active) {
        font-weight: bold;
    }

    .wrapper {
        display: flex;
        flex-direction: row;
        align-items: stretch;
        min-height: 100%;
    }

    .content {
        flex: 1;
        font-family: Arial;
        padding: 20px;
    }
</style>
