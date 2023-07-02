<script>
    const partnerItems = [
        {
            id: 0,
            path: "../src/public/partner/partner1.png",
        },
        {
            id: 1,
            path: "../src/public/partner/partner2.png",
        },
        {
            id: 2,
            path: "../src/public/partner/partner3.png",
        },
        {
            id: 3,
            path: "../src/public/partner/partner4.png",
        },
        {
            id: 4,
            path: "../src/public/partner/partner5.png",
        },
        {
            id: 5,
            path: "../src/public/partner/partner6.png",
        },
        {
            id: 6,
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

<div class="logos">
    <div class="logos-slide">
        {#each partnerItems as item (item.id)}
            <img src={item.path} alt={item.id} />
        {/each}
        {#each partnerItems as item (item.id)}
            <img src={item.path} alt={item.id} />
        {/each}
    </div>
</div>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        background: #f2f2f2;
    }

    @keyframes slide {
        from {
            transform: translateX(0);
        }
        to {
            transform: translateX(-100%);
        }
    }

    .logos {
        overflow: hidden;
        padding: 60px 0;
        background: white;
        position: relative;
        display: flex;
        justify-content: center;
    }

    .logos:before,
    .logos:after {
        position: absolute;
        top: 0;
        width: 250px;
        height: 100%;
        content: "";
        z-index: 2;
    }

    .logos:before {
        left: 0;
        background: linear-gradient(to left, rgba(255, 255, 255, 0), white);
    }

    .logos:after {
        right: 0;
        background: linear-gradient(to right, rgba(255, 255, 255, 0), white);
    }

    .logos:hover .logos-slide {
        animation-play-state: paused;
    }

    .logos-slide {
        display: inline-flex;
        animation: 35s slide infinite linear;
    }

    .logos-slide img {
        height: 100px;
        margin: 0 40px;
    }
</style>
