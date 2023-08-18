<script>
    import Header from "../lib/global/Header.svelte";

</script>


<Header />

<main>
    <slot>
        
    </slot>
</main>


<style>
    main {
        max-width: 1200px;
        margin: 0 auto;
    }
</style>