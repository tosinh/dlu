<script>
    import { flip } from "svelte/animate";
    import { onDestroy } from "svelte";

    export let images;
    export let imageWhidth = 980;
    export let imageSpacing = 20;
    export let transitionSpeed = 500;
    export let autoplay = false;
    export let autoplaySpeed = 3000;
    let interval;

    const rotateLeft = (e) => {
        const transitioningImage = images[images.length - 1];
        document.getElementById(transitioningImage.id).style.opacity = 0;
        images = [
            images[images.length - 1],
            ...images.slice(0, images.length - 1),
        ];
        setTimeout(() => {
            document.getElementById(transitioningImage.id).style.opacity = 1;
        }, transitionSpeed);
    };

    const rotateRight = (e) => {
        const transitioningImage = images[0];
        document.getElementById(transitioningImage.id).style.opacity = 0;
        images = [...images.slice(1, images.length), images[0]];
        setTimeout(() => {
            document.getElementById(transitioningImage.id).style.opacity = 1;
        }, transitionSpeed);
    };

    const startAutoPlay = () => {
        if (autoplay) {
            interval = setInterval(rotateLeft, autoplaySpeed);
        }
    };

    const stopAutoPlay = () => {
        clearInterval(interval);
    };

    if (autoplay) {
        startAutoPlay();
    }

    onDestroy(() => {
        stopAutoPlay();
    });
</script>

<div class="carousel-container">
    <div class="carousel-imges" autoplay="2000">
        {#each images as image (image.id)}
            <img
                src={image.path}
                alt={image.id}
                id={image.id}
                style={`width:${imageWhidth}px; 
                margin = 0 ${imageSpacing}px;`}
                on:mouseover={stopAutoPlay}
                on:mouseout={startAutoPlay}
                on:click={() => dispatch("imageClicked", image.path)}
                animate:flip={{ duration: transitionSpeed }}
            />
        {/each}
    </div>
    <button id="left" on:click={rotaceLeft}>
        <slot name="left-control">
            <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                id="left-arrow"
                width="50"
                height="70"
                ><path
                    d="m8.5 12.8 5.7 5.6c.4.4 1 .4 1.4 0 .4-.4.4-1 0-1.4l-4.9-5 4.9-5c.4-.4.4-1 0-1.4-.2-.2-.4-.3-.7-.3-.3 0-.5.1-.7.3l-5.7 5.6c-.4.5-.4 1.1 0 1.6 0-.1 0-.1 0 0z"
                /></svg
            >
        </slot>
    </button>
    <button id="right" on:click={rotaceRight}>
        <slot name="right-control">
            <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                id="right-arrow"
                width="50"
                height="70"
                ><path
                    d="M15.54,11.29,9.88,5.64a1,1,0,0,0-1.42,0,1,1,0,0,0,0,1.41l4.95,5L8.46,17a1,1,0,0,0,0,1.41,1,1,0,0,0,.71.3,1,1,0,0,0,.71-.3l5.66-5.65A1,1,0,0,0,15.54,11.29Z"
                /></svg
            >
        </slot>
    </button>
</div>

<style>
    .carousel-container {
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        overflow-x: hidden;
        position: relative;
    }

    .carousel-imges {
        display: flex;
        -webkit-mask: linear-gradient(
            to right,
            transparent,
            black 40%,
            black 60%,
            transparent
        );
        mask: linear-gradient(
            to right,
            transparent,
            black 40%,
            black 60%,
            transparent
        );
        justify-content: center;
        align-items: center;
        flex-wrap: nowrap;
    }

    button {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        color: white;
        background-color: transparent;
        border: none;
    }
    button:focus {
        outline: 1px solid white;
    }
    #left {
        left: 10px;
    }
    #right {
        right: 10px;
    }
</style>
