<script>
    export let data;
</script>

<div class="layout py-8">
    <main>
        <slot/>
    </main>

    <aside>
        <h2>More Products</h2>
        <ul>
            {#each data.details as { slug, name}}
                <li>
                    <a href="/product/{slug}">{name}</a>
                </li>
            {/each}
        </ul>
    </aside>
</div>

<style>
    @media (min-width: 640px){
        .layout {
            display: grid;
            gap: 2em;
            grid-template-columns: 1fr 16em;
    }
    }
</style>