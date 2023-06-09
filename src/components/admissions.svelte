<script>
    const imagesAdmissions = [
        {
            id: "anh1",
            path: "../src/public/admissions/anh1.jpg",
        },
        {
            id: "anh2",
            path: "../src/public/admissions/anh2.png",
        },
        {
            id: "anh3",
            path: "../src/public/admissions/anh3.png",
        },
        {
            id: "anh4",
            path: "../src/public/admissions/anh4.png",
        },
    ];
</script>

<div class="admissions-wrap">
    <h2>
        <span class="span-h">TUYỂN SINH</span>
    </h2>
    <div class="admissions-image">
        {#each imagesAdmissions as image}
            <a href="#"><img src={image.path} alt={image.id} /></a>
        {/each}
    </div>
</div>

<style>
    .admissions-wrap {
        width: 1170px;
        widows: 100%;
        margin: 40px auto;
        text-align: center;
    }
    .span-h {
        text-align: center;
        text-transform: uppercase;
        color: rgb(122, 162, 40);
        font-size: 24px;
        font-weight: 700;
        line-height: 80px;
        margin: 20px 0;
        border-bottom: 2px solid rgb(122, 162, 40);
    }
    .admissions-image {
        display: flex;
        justify-content: space-around;
    }
    img {
        max-width: 268px;
        height: 250px;
    }
</style>
