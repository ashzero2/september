<script>
    import Carousel from "svelte-carousel";
    import { fly } from "svelte/transition";

    let carousel;

    var images = [
        {
            name: "Lovable Image",
            path: "images/wallpaper.png",
            text: "Enaku epome pidicha image, this will remain in our heart forever",
        },
        {
            name: "Cute Couples",
            path: "images/wallpaper.png",
            text: "As u know bb, see this image, we are literally the best couples out there, love u",
        },
        {
            name: "My Queen",
            path: "images/wallpaper.png",
            text: "Yes, ofcourse my precious and cute queen and princess of my heart",
        },
        {
            name: "Love You",
            path: "images/wallpaper.png",
            text: "IDK why but i like this picture so much, daily morning ill see this picture and admire how i got a cutie like u as my girl :) love u",
        },
    ];
</script>

<main>
    <h1 class="title">Gallery</h1>
    <Carousel bind:this={carousel}>
        {#each images as image}
            <div transition:fly={{ y: 200, duration: 2000 }}>
                <img src={image.path} height="500" width="800" alt="" />
                <h5>{image.name}</h5>
                <p>{image.text}</p>
            </div>
        {/each}
    </Carousel>
</main>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Rampart+One&family=Source+Sans+Pro&display=swap");

    * {
        background-color: #282c34;
    }

    .title {
        font-family: "Rampart One", cursive;
        margin-bottom: 30px;
    }

    div {
        display: flex;
        flex-direction: column;
    }

    h1,
    h5,
    p {
        text-align: center;
        color: #abb2bf;
    }

    h5 {
        margin-top: 20px;
    }
</style>
