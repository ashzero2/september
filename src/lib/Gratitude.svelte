<script>
    import { fly } from "svelte/transition";
    const events = [
        {
            day: 1,
            event: "Fairy & Story",
            note: "Stories ? more like angels song :) She made me sleep by telling cute little stories she made. epome nan soliye palakam but this time she did it, I just melted on that instant and enjoyed that much, she wanted to make me sleep, but instead i kept on thinking of her during that night. I wanna hold her arms and make her sleep by telling stories, i'll take care of my girl ❤",
        },
        {
            day: 2,
            event: "Prepared & Tired",
            note: "Ah yes, pavam pilla avala potu atha padi itha padi nu usura vangiten, epdio oru valia ramco and Hexaware ku thangakutty ready ! she will pass this one i have trust on my bb girl. Romba tired aita chlokutty. Once she get placed avala nan pathupen (place agala nalum pathupen) she's mine eh",
        },
        {
            day: 3,
            event: "Finally Placed",
            note: "Podu nan nethu nenacha mathire baby got placed in ramco systems, this day awwwwwww. I cant forget this. I got hyped so much, we literally waited for this day to come and here it is, me and baby waited for the result and kai vidala, chlolkutty nethu okanthu avalo prepare panathu and her hard works finally returned good. Wonderful day in my life i wanna shout that my babe got placedd",
        },
        {
            day: 4,
            event: "She & Dad",
            note: "God ! i cant belive wut just happened today, I went out to a hotel with my father-in-law, Im literally shocked but pannikutty evlo calm a thinutu iruku paru, nanum sidela munadi angutu ingutu nu sight adichtu iruken, enaku briyani than mukkiam  nu onu okanthu nalla kotitu iruku.My father hugged me a bit, i felt like ... i can't express it :) Best moment",
        },
        {
            day: 5,
            event: "Hex & Vex",
            note: "I made her go crazy and she got angry on me, And recieved confirmation of hexaware 2nd round for her Hex for me Vex",
        },
        {
            day: 6,
            event: "Stories & Stuffs",
            note: "I told her a lot of stories and she listened to it like a child, i feel like baby kuda irukura all days are spl to me.She's like a child, i wanna protect her and see her smile everyday",
        },
        {
            day: 7,
            event: "Turn On Time",
            note: "Aandavarae, iva irukale, kai ah vachutu summa irukia d, suma suma lip kita kondu poorathu, tease panrathu, madam lip ah screen kitaka kondu varuvanga nanum kiss kedaikum nu aaa nu iruntha angutu apdie poiruvanga -_-. ena kadupethi pakrathula ena oru santhosham eruma maadu ku. oru naal maatamaya poiruva :",
        },
        {
            day: 8,
            event: "Incomming ..",
            note: "To Be Fullfilled",
        },
        {
            day: 9,
            event: "Prep Trip",
            note: "Nalaiku trip ponum, so kelambitu irunthen, avala pakrathe saturday than, athum ipo mudiala, will miss my little girl a lot. Nalla kadupethiten, Ehpaa oru trip ku nee vara varathu iruke nu solra alavu, ena oru anantham enaku. i went to a shop and she choosed a color for me, ice vaikalam nu pathen but mudialaye",
        },
        {
            day: 10,
            event: "Shitty Day",
            note: "Wut day this is, shitty day i've ever seen, kalaila iruntha nadantha elathayum babe ta solalam alaga katha kepa, apdinu ena enamo neanchutu irunthen, but cuz of a stupid scum babe got angry with me and blocked me, i cried like crazy, god i dont wanna lose her, i just want her, i want her to be on my side and to be with me.She's the one, i'm always sofi's achu.i love her, and will continue to",
        },
        {
            day: 11,
            event: "Sad :)",
            note: "She told me to choose between being a friend / don't speak with me. Enala epdi mudium ithu rendum , bothare like , i cant, sofi is my girl, always my girl.i wanna love her, i want her to love me. this is the day i cried like child.i said her my surprise gift(this cards), somehow she gave me a min to ask her and she'll do it, i asked love me, she put conditions, but anything is fine if she's with me, i can do anything, i just want her forever ❤ ",
        },
        {
            day: 12,
            event: "Thank God",
            note: "i came home, yet apdi thonala, cuz i need her, she is my home. My heart is with her.We talked some things, and she wanted to see the gratitutde app, i showed her, but on the half way, i started crying reading those things. i want my sofi always.I cant afford to lose her. i wont leave her. ill make her achive everything, babe got sleepy after reading those gratitudes and said she's sleepy, she told love u, butterflies moment, i am ready to die even now",
        },
        {
            day: 13,
            event: "One Calm Day",
            note: "Finally fight's over, as always she's mine, Loving her is the best thing i can do",
        },
        {
            day: 14,
            event: "Peak and Travels",
            note: "Baby veetuku vanthutu iruntha, nanum ponen, we met in madurai and had food and travelled together, I touched her stomach :> apro apdie methuva anga anga, little bit romance, little bit talks, and her care for my face aww i just melted like ice cream, and she gave me a surprise lip kiss awwwwwwww, i can't hold myself",
        },
        {
            day: 15,
            event: "HairStyle Day",
            note: "Chellathuku ena mood vanchu ne thrla she suddenly tried school hairstyles, aasa vantu pola she tried hairstyles and showed it to me, she was cute asalways pilla kasta patu night fulla potum seriave varala pola, and we talked a bit, she felt sleepy katha solu nu solitu solrathukula thoongita maadu maddu",
        },
        {
            day: 16,
            event: "Tired N Treats",
            note: "Friday, so much tired, epo da evening polam nu irunthen, oru valia train la home ku reached,thinu thinu na olunga thingala eruma maadu, apro veetuku vantha apro we talked a lot, little little treats for my eyes, pakama iruka mudialaye, ivlo alaga iruntha nan ena panrathu",
        },
        {
            day: 17,
            event: "Saturday",
            note: "Finally after 2 weeks babe ah nerla pathuten, felt so much happy as well as emotional, i really do wanna hug her and say that `I missed you` but i can't. I missed her so much in this 2 weeks. but evening vera lvl uh, Aww treat oh treat uh, ennah ponnu da, kuduthu vachavan nanu ^-^",
        },
        {
            day: 18,
            event: "Weekend Emotions",
            note: "Sunday, asusual 1 mani vera pannikutty thoongita, apro enthika vachu sapta vachu, apro pilla drama paka poita, evening padikalam pathom but pesa arambichutom, shared some things, cried some times. It's both a sad and happy day for me :(, i shouldn't have hurted her,but i'll make sure to treat her like a princess",
        },
        {
            day: 19,
            event: "Padikalam patha thoongiachu",
            note: "Nalaiku IAT eh seekram padika vachu pillaya thoonga vaikalam patha, padichutu varen nu solitu nalla thoongira vendiathu pannikutty",
        },
        {
            day: 20,
            event: "mrng 4 study",
            note: "Nethu padikala so mrng 4 maniku enchu kasta patu padichu oru valia muduchachu ahpadaaa.",
        },
        {
            day: 21,
            event: "Not much talks wash",
            note: "Neria pesala, Missing her, thovachutu romba tired ah iruku nu thoongita chellakutty",
        },
        {
            day: 22,
            event: "Bad Day Yes",
            note: "----",
        },
    ];
</script>

<main>
    <section
        transition:fly={{ y: 200, duration: 2000 }}
        class="gratitude"
        id="gratitude"
    >
        <h1 style="text-align:center;padding:10px;color:#abb2bf">
            Gratitude Page
        </h1>
        <div class="cards">
            {#each events as { day, event, note }}
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <h1>September</h1>
                            <h1>{day}</h1>
                        </div>
                        <div class="flip-card-back">
                            <h1>{event}</h1>
                            <p>{note}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>

<style>
    * {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #282c34;
    }

    .flip-card-back > h1 {
        background-color: #aab2bf;
        font-family: "Dancing Script", cursive;
    }

    .flip-card-back > p {
        background-color: #aab2bf;
        font-family: "Source Sans Pro", sans-serif;
    }

    .flip-card-front > h1 {
        background-color: #31353f;
        margin-top: 65px;
        font-family: "Rampart One", cursive;
    }

    .flip-card-front,
    .flip-card-back {
        background-image: url("./wallpaper.png");
    }

    .cards {
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 50px;
        margin: 50px;
        align-items: center;
        flex-wrap: wrap;
    }

    .flip-card {
        background-color: transparent;
        width: 300px;
        height: 300px;
        perspective: 1000px;
    }

    .flip-card-inner {
        position: relative;
        width: 100%;
        height: 100%;
        text-align: center;
        transition: transform 0.6s;
        transform-style: preserve-3d;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.5);
    }

    .flip-card:hover .flip-card-inner {
        transform: rotateY(180deg);
    }

    .flip-card-front,
    .flip-card-back {
        position: absolute;
        width: 100%;
        text-align: center;
        padding: 10px;
        height: 100%;
        -webkit-backface-visibility: hidden;
        backface-visibility: hidden;
    }

    .flip-card-front {
        background-color: #31353f;
        color: #abb2bf;
    }

    .flip-card-back {
        background-color: #aab2bf;
        color: #282c34;
        transform: rotateY(180deg);
    }
</style>
