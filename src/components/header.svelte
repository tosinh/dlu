<script>
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
        <ul class="header-list list-header">
            {#each headerItems as item}
                <li class="header-item">
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
        <ul class="header-list list-infor">
            {#each inforItems as item}
                <li class="header-item">
                    <a href={item.href}>{item.label}</a>
                </li>
            {/each}
        </ul>
    </div>
</header>

<style>
    header {
        background-color: #5f7adb;
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
    .header-list {
        display: flex;
        position: relative;
        width: 100%;
        margin: 0;
    }
    .list-infor {
        justify-content: flex-end;
    }
    .header-list li {
        list-style-type: none;
        position: relative;
    }

    .header-list li:before {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background-color: #5f7adb;
    }

    .header-list a {
        color: #fff;
        text-decoration: none;
        display: flex;
        height: 45px;
        align-items: center;
        padding: 0 10px;
        font-size: 13px;
    }
    .header-item:after {
        content: "";
        display: block;
        position: absolute;
        border-left: 1px solid #fff;
        height: 14px;
        right: 0px;
        top: 50%;
        transform: translateY(-50%);
    }
</style>
