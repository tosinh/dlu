<script>
    import { onMount } from "svelte";

    let showMobileMenu = false;

    const navItems = [
        { label: "logo", href: "#" },
        { label: "Giới thiệu", href: "#" },
        { label: "Tin tức", href: "#" },
        { label: "Đào tạo", href: "#" },
        { label: "Research Portal", href: "#" },
        { label: "Văn bản", href: "#" },
        { label: "Tra cứu văn bằng", href: "#" },
        { label: "Tuyển sinh", href: "#" },
        { label: "Tuyển sinh", href: "#" },
        { label: "Bản đồ Website", href: "#" },
        { label: "Search", href: "#" },
    ];

    const handleMobileIconClick = () => (showMobileMenu = !showMobileMenu);

    const mediaQueryHandler = (e) => {
        if (!e.matches) {
            showMobileMenu = false;
        }
    };

    onMount(() => {
        const mediaListener = window.matchMedia("(max-width: 767px)");

        mediaListener.addListener(mediaQueryHandler);
    });
</script>

<nav>
    <div class="inner">
        <div
            on:click={handleMobileIconClick}
            class={`mobile-icon${showMobileMenu ? " active" : ""}`}
        >
            <div class="middle-line" />
        </div>
        <ul class={`navbar-list${showMobileMenu ? " mobile" : ""}`}>
            {#each navItems as item}
                <li>
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
    </div>
</nav>

<style>
    nav {
        background-color: rgba(255, 255, 255, 0.8);
        font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
        height: 45px;
        margin: 20px 0;
        border-top: 2px solid rgb(121, 162, 39);
    }
    .inner {
        max-width: 1200px;
        padding-left: 20px;
        padding-right: 20px;
        margin: auto;
        box-sizing: border-box;
        display: flex;
        align-items: center;
        height: 100%;
    }

    .mobile-icon {
        width: 25px;
        height: 14px;
        position: relative;
        cursor: pointer;
    }

    .mobile-icon:after,
    .mobile-icon:before,
    .middle-line {
        content: "";
        position: absolute;
        width: 100%;
        height: 2px;
        background-color: #000;
        transition: all 0.4s;
        transform-origin: center;
    }

    .mobile-icon:before,
    .middle-line {
        top: 0;
    }

    .mobile-icon:after,
    .middle-line {
        bottom: 0;
    }

    .mobile-icon:before {
        width: 66%;
    }

    .mobile-icon:after {
        width: 33%;
    }

    .middle-line {
        margin: auto;
    }

    .mobile-icon:hover:before,
    .mobile-icon:hover:after,
    .mobile-icon.active:before,
    .mobile-icon.active:after,
    .mobile-icon.active .middle-line {
        width: 100%;
    }

    .mobile-icon.active:before,
    .mobile-icon.active:after {
        top: 50%;
        transform: rotate(-45deg);
    }

    .mobile-icon.active .middle-line {
        transform: rotate(45deg);
    }

    .navbar-list {
        display: none;
        width: 100%;
        justify-content: space-between;
        margin: 0;
        padding: 0 40px;
    }

    .navbar-list.mobile {
        background-color: rgba(255, 2555, 255, 0.8);
        position: fixed;
        display: block;
        height: calc(100% - 45px);
        bottom: 0;
        left: 0;
    }

    .navbar-list li {
        list-style-type: none;
        position: relative;
    }

    .navbar-list li:before {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background-color: #fff;
    }

    .navbar-list a {
        color: #000;
        text-decoration: none;
        display: flex;
        height: 45px;
        align-items: center;
        padding: 0 10px;
        font-size: 13px;
    }

    @media only screen and (min-width: 767px) {
        .mobile-icon {
            display: none;
        }

        .navbar-list {
            display: flex;
            padding: 0;
        }

        .navbar-list a {
            display: inline-flex;
        }
    }
</style>
