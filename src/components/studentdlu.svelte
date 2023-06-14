<script>
    const itemStudentdlu = [
        {
            path: "../src/public/studentdlu/hinh1.jpg",
            id: 1,
        },
        {
            path: "../src/public/studentdlu/hinh2.jpg",
            id: 2,
        },
        {
            path: "../src/public/studentdlu/hinh3.jpeg",
            id: 3,
        },
        {
            path: "../src/public/studentdlu/hinh4.jpg",
            id: 4,
        },
        {
            path: "../src/public/studentdlu/hinh5.jpg",
            id: 5,
        },
        {
            path: "../src/public/studentdlu/hinh6.jpg",
            id: 6,
        },
        {
            path: "../src/public/studentdlu/hinh7.jpg",
            id: 7,
        },
        {
            path: "../src/public/studentdlu/hinh8.jpg",
            id: 8,
        },
    ];
</script>

<div class="studentdlu-wrap">
    <h2>
        <span class="span-h"> ĐỜI SỐNG SINH VIÊN DLU </span>
    </h2>
    <div class="grid grid-cols-4 gap-3">
        {#each itemStudentdlu as item (item.id)}
            <div class="img-item">
                <img src={item.path} alt={item.id} />
            </div>
        {/each}
    </div>
</div>

<style>
    .studentdlu-wrap {
        width: 1170px;
        widows: 100%;
        margin: 40px auto;
        text-align: center;
    }
    .span-h {
        text-align: center;
        text-transform: uppercase;
        color: #5f7adb;
        font-size: 24px;
        font-weight: 700;
        line-height: 80px;
        margin: 20px 0;
        border-bottom: 2px solid #5f7adb;
    }
    .img-item {
        width: 282px;
        height: 200px;
        margin: 0;
        padding: 0;
        background: #fff;
        overflow: hidden;
    }
    .img-item img {
        -webkit-transform: scale(1);
        transform: scale(1);
        -webkit-transition: 0.3s ease-in-out;
        transition: 0.3s ease-in-out;
    }
    img:hover {
        -webkit-transform: scale(1.3);
        transform: scale(1.3);
    }
</style>
