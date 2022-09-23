<script>
    import { ConfettiExplosion } from "svelte-confetti-explosion";
    import { fly } from "svelte/transition";

    var start = new Date("05/24/2022");
    var now = new Date();
    $: hours = now.getHours();
    $: mins = now.getMinutes();
    $: seconds = now.getSeconds();
    var timer;

    const days = () => {
        var timeDiff = now.getTime() - start.getTime();
        var dayDiff = timeDiff / (1000 * 3600 * 24);
        return Math.trunc(dayDiff);
    };

    const day = days();

    setInterval(function () {
        now = new Date();
    }, 1000);
</script>

<main>
    {#if timer != "1803"}
        <section class="wish">
            <h1 transition:fly={{ x: 200, duration: 2000 }}>
                Enter our Password
            </h1>
            <input
                transition:fly={{ x: 200, duration: 2000 }}
                type="text"
                bind:value={timer}
            />
        </section>
    {:else}
        <ConfettiExplosion
            particleCount={500}
            duration={3000}
            colors={["#e06c75", "#98c379", "#e5c07b", "#61afef"]}
        />
        <section class="wish" id="wish">
            <ConfettiExplosion
                particleCount={500}
                duration={5000}
                colors={["#e06c75", "#98c379", "#e5c07b", "#61afef"]}
            />
            <div class="time">
                <h1>We Have Been Together For</h1>
            </div>
            <div>
                <h1 class="days">{day} Days</h1>
            </div>
            <div>
                <h1 class="hours">{hours} Hour's</h1>
            </div>
            <div>
                <h1 class="minutes">{mins} Minute's</h1>
            </div>
            <div>
                <h1 class="seconds">{seconds} Second's</h1>
            </div>
        </section>
    {/if}
</main>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Dancing+Script&family=Pacifico&family=Qwitcher+Grypen&display=swap");
    @import url("https://fonts.googleapis.com/css2?family=Rampart+One&family=Source+Sans+Pro&display=swap");

    .wish {
        background-color: #282c34;
        height: 800px;
    }

    .wish {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .wish {
        color: #aba2ab;
        font-family: "Rampart One", cursive;
    }

    input {
        width: 200px;
        height: 30px;
        border-radius: 5px;
        border: none;
        font-size: 20px;
        text-align: center;
        font-family: sans-serif;
    }
</style>
