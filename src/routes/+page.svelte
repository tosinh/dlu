<script>
    import { DarkMode } from "flowbite-svelte";
    import NavHome from "../components/navHome.svelte";
    import Main from "../components/main.svelte";
    let btnClass =
        "float-right text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2";
</script>

<svelte:head>
    <title>Trường đại học Dầ Lạt</title>
</svelte:head>

<header>
    <DarkMode {btnClass} />
    <NavHome />
</header>
<Main />
