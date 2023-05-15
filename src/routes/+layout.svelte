<script lang='ts'>
    import '../app.css';

    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class='min-h-screen flex flex-col'>
    <div class='flex-grow'>
        <Header/>

        <main class='md:container md:mx-auto p-10'>
            <slot/>
        </main>

    </div>
    <Footer/>
</div>
