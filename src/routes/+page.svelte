<script>
    import Header from "../lib/components/Header.svelte";
    import BackLog from "../lib/components/BackLog.svelte";
    import Footer from "../lib/components/Footer.svelte";
    import Generalidades from "../lib/components/Generalidades.svelte";
    import Home from "../lib/components/Home.svelte";
    import Solicitud from "../lib/components/Solicitud.svelte";

    let currentPage = "home";

    function goToPage(page) {
        currentPage = page;
    }
</script>

<Header {goToPage} />

<main>
    {#if currentPage === "home"}
        <Home />
    {:else if currentPage === "Solicitud"}
        <Solicitud {goToPage} />
    {:else if currentPage === "Generalidades"}
        <Generalidades />
    {:else if currentPage === "BackLog"}
        <BackLog {goToPage} />
    {/if}
</main>

<Footer />

<style>
    :global(body) {
        font-family: "Arial", sans-serif;
        padding: 0;
        margin: 0;
        background-color: #e0e0e0;
    }
</style>

