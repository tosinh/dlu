<script>
    import { DarkMode } from "flowbite-svelte";
    import NavHome from "../components/navHome.svelte";
    import { Carousel } from "flowbite-svelte";
    import { images } from "../routes/data.js";
    import Sidebar from "../components/sidebarHome.svelte";
    import SpeedDial from "../components/speedDial.svelte";
    import TinTuc from "../components/tintuc.svelte";
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
    <div id="tintuc" class="max-w-6xl ml-32 my-10">
        <TinTuc />
    </div>
</main>
<div class="fixed bottom-0 right-0">
    <SpeedDial />
</div>
