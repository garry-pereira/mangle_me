<script>
    import Header from "../components/Header.svelte";
    import Banner from "../components/Banner.svelte";
    import Navbar from "../components/Navbar.svelte";
    import Footer from "../components/Footer.svelte";
    import "../app.css";
</script>

<div class="app min-h-screen flex flex-col justify-between">
    <Header>
        <Banner />
        <Navbar />
    </Header>

    <main>
        <slot />
    </main>

    <Footer />
</div>

<style>
</style>
