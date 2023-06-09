<script>
    import { onMount } from "svelte";

    const headerItems = [
        { label: "Khoa", href: "#" },
        { label: "Phòng", href: "#" },
        { label: "Viện", href: "#" },
        { label: "Trung Tâm", href: "#" },
        { label: "Thư Viện", href: "#" },
        { label: "QLGD", href: "#" },
        { label: "Đảng - Đoàn thể", href: "#" },
    ];

    const inforItems = [
        { label: "logo", href: "#" },
        { label: "Cán bộ/Giảng viên", href: "#" },
        { label: "Sinh viên", href: "#" },
        { label: "Liên hệ", href: "#" },
    ];
</script>

<header>
    <div class="inner">
        <div>
            <div class="middle-line" />
        </div>
        <ul class="navbar-list list-header">
            {#each headerItems as item}
                <li>
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
        <ul class="navbar-list list-infor">
            {#each inforItems as item}
                <li>
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
    </div>
</header>

<style>
    header {
        background-color: rgb(121, 162, 39);
        font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
        height: 45px;
    }
    .inner {
        max-width: 1200px;
        padding-left: 20px;
        padding-right: 20px;
        margin: auto;
        box-sizing: border-box;
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 100%;
    }
    .navbar-list {
        display: flex;
        width: 100%;
        margin: 0;
    }
    .list-infor {
        justify-content: flex-end;
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
        background-color: rgb(121, 162, 39);
    }

    .navbar-list a {
        color: #fff;
        text-decoration: none;
        display: flex;
        height: 45px;
        align-items: center;
        padding: 0 10px;
        font-size: 13px;
    }
</style>
