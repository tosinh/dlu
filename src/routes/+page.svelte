<script>
    import { DarkMode } from "flowbite-svelte";
    import NavHome from "../components/navHome.svelte";
    import { Carousel } from "flowbite-svelte";
    import { images } from "../routes/data.js";
    import Sidebar from "../components/sidebarHome.svelte";
    import SpeedDial from "../components/speedDial.svelte";
    import GioiThieu from "../components/gioithieu.svelte";
    import TinTuc from "../components/tintuc.svelte";
    import InfiniteLogo from "../components/infiniteLogo.svelte";
    import Footer from "../components/footerHome.svelte";
    let btnClass =
        "float-right text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2";
    let showThumbs = false;
    let showCaptions = false;
</script>

<svelte:head>
    <link rel="shortcut icon" href="../src/public/home/logodlu.png" />
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
    <div id="gioithieu" class="max-w-6xl ml-32 my-10 mt-24">
        <GioiThieu />
    </div>
    <div id="tintuc" class="max-w-6xl ml-32 my-10 mt-24">
        <TinTuc />
    </div>
    <div><InfiniteLogo /></div>
</main>
<div class="fixed bottom-0 right-0 z-50">
    <SpeedDial />
</div>
<footer class="">
    <Footer />
</footer>
