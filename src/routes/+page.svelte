<script>
    import { DarkMode } from "flowbite-svelte";
    import NavHome from "../components/navHome.svelte";
    import { Carousel } from "flowbite-svelte";
    import { images } from "../routes/data.js";
    import Sidebar from "../components/sidebarHome.svelte";
    let btnClass =
        "float-right text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2";
    let showThumbs = false;
    let showCaptions = false;
</script>

<svelte:head>
    <title>Trường đại học Dầ Lạt</title>
</svelte:head>
<!-- <DarkMode {btnClass} /> -->
<header class="sticky top-0 z-40 w-full">
    <NavHome />
</header>

<aside class="float-left">
    <Sidebar />
</aside>
<main class="ml-40">
    <div class="max-w-6xl m-auto z-0">
        <Carousel {images} loop {showCaptions} {showThumbs} duration="3000" />
    </div>
</main>
