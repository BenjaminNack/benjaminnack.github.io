<script>
    import Index from './pages/Index.svelte';

    let page = 0;
</script>

<nav>
    <ul class="page-list">
        <li class="page-item" on:click={() => page = 0}>Portfolio</li>
    </ul>
</nav>

{#if page === 0}
<Index/>
{/if}

<style>
    .page-list {
        list-style-type: none;
        padding-left: 20px;
    }

    .page-item {
        user-select: none;
        -webkit-touch-callout: none;
        -webkit-user-select: none;
        -khtml-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
    }

    .page-item:hover {
        color: #8baaff;
    }
</style>