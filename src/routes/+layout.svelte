<script>
    import Header from "../lib/global/Header.svelte";
    import Schedule from "../lib/schedule/Schedule.svelte";

</script>



<Header />

<Schedule />

<main>
    <slot>
        
    </slot>
</main>
    


<style>
    main {
        max-width: 1200px;
        min-height: 100vh;
        margin: 0 auto;
        padding: 1em;
        position: relative;
        overflow-x: hidden;
    }
</style>