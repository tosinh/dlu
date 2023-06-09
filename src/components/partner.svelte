<script>
    let interval;
    const partnerItems = [
        {
            id: 1,
            path: "../src/public/partner/partner1.png",
        },
        {
            id: 2,
            path: "../src/public/partner/partner2.png",
        },
        {
            id: 3,
            path: "../src/public/partner/partner3.png",
        },
        {
            id: 4,
            path: "../src/public/partner/partner4.png",
        },
        {
            id: 5,
            path: "../src/public/partner/partner5.png",
        },
        {
            id: 6,
            path: "../src/public/partner/partner6.png",
        },
        {
            id: 1,
            path: "../src/public/partner/partner7.png",
        },
        {
            id: 7,
            path: "../src/public/partner/partner8.png",
        },
        {
            id: 8,
            path: "../src/public/partner/partner9.png",
        },
    ];
</script>

<div class="partner-wrap">
    <h2>
        <h2>
            <span class="span-h">CÁC ĐỐI TÁC</span>
        </h2>
    </h2>
    <div class="partner-list">
        {#each partnerItems as item (item.id)}
            <img src={item.path} alt={item.id} />
        {/each}
    </div>
</div>

<style>
    .partner-wrap {
        width: 1170px;
        widows: 100%;
        margin: 40px auto;
        text-align: center;
        overflow: hidden;
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
    img {
        width: 268px;
    }
    .partner-list {
        display: flex;
    }
</style>
