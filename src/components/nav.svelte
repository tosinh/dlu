<script>
    import { onMount } from "svelte";

    let showMobileMenu = false;
    export let inputValue = "";

    const navItems = [
        { label: "Giới thiệu", href: "#" },
        { label: "Tin tức", href: "https://dlu.edu.vn/tin-tuc/" },
        { label: "Đào tạo", href: "#" },
        { label: "Research Portal", href: "#" },
        { label: "Văn bản", href: "#" },
        { label: "Tra cứu văn bằng", href: "#" },
        { label: "Tuyển sinh", href: "#" },
        { label: "Tuyển sinh", href: "#" },
        { label: "Bản đồ Website", href: "#" },
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
        <div class="logo">
            <svg
                fill="#fff"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                width="20px"
                height="20px"
                viewBox="0 0 495.398 495.398"
                xml:space="preserve"
            >
                <g>
                    <g>
                        <g>
                            <path
                                d="M487.083,225.514l-75.08-75.08V63.704c0-15.682-12.708-28.391-28.413-28.391c-15.669,0-28.377,12.709-28.377,28.391
                       v29.941L299.31,37.74c-27.639-27.624-75.694-27.575-103.27,0.05L8.312,225.514c-11.082,11.104-11.082,29.071,0,40.158
                       c11.087,11.101,29.089,11.101,40.172,0l187.71-187.729c6.115-6.083,16.893-6.083,22.976-0.018l187.742,187.747
                       c5.567,5.551,12.825,8.312,20.081,8.312c7.271,0,14.541-2.764,20.091-8.312C498.17,254.586,498.17,236.619,487.083,225.514z"
                            />
                            <path
                                d="M257.561,131.836c-5.454-5.451-14.285-5.451-19.723,0L72.712,296.913c-2.607,2.606-4.085,6.164-4.085,9.877v120.401
                       c0,28.253,22.908,51.16,51.16,51.16h81.754v-126.61h92.299v126.61h81.755c28.251,0,51.159-22.907,51.159-51.159V306.79
                       c0-3.713-1.465-7.271-4.085-9.877L257.561,131.836z"
                            />
                        </g>
                    </g>
                </g>
            </svg>
        </div>
        <ul class={`navbar-list${showMobileMenu ? " mobile" : ""}`}>
            {#each navItems as item}
                <li>
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
        <input
            type="text"
            placeholder="Search..."
            autocomplete="off"
            id="searchInput"
            bind:value={inputValue}
            on:input
        />
        <span id="search-icon">🔍</span>
    </div>
</nav>

<style>
    svg {
        margin: auto;
        align-items: center;
    }
    .logo {
        width: 40px;
        height: 40px;
        background-color: #5f7adb;
        display: flex;
        border-radius: 4px;
    }
    nav {
        background-color: rgba(255, 255, 255, 0.8);
        font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
        height: 45px;
        margin: 20px 0;
        border-top: 2px solid #5f7adb;
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
    #searchInput {
        box-sizing: border-box;
        font-size: 1.2rem;
        border: none;
        border-bottom: 1px solid #ddd;
    }
    #searchInput:focus {
        outline: 3px solid #ddd;
    }

    #search-icon {
        left: 10px;
        top: 10px;
        font-size: 1.2rem;
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
