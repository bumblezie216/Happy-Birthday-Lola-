<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Lola ♡</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Georgia, "Times New Roman", serif;
    background:
        radial-gradient(circle at 20% 20%, rgba(120,180,255,.15), transparent 25%),
        radial-gradient(circle at 80% 70%, rgba(100,150,255,.12), transparent 25%),
        #050817;
    color: #eaf4ff;
    min-height: 100vh;
    overflow-x: hidden;
}

body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    background-image:
        radial-gradient(circle, white 1px, transparent 1px),
        radial-gradient(circle, rgba(180,220,255,.7) 1px, transparent 1px);
    background-size: 90px 90px, 150px 150px;
    background-position: 10px 20px, 50px 80px;
    opacity: .35;
    z-index: 0;
}

.container {
    width: min(900px, 92%);
    margin: auto;
    position: relative;
    z-index: 1;
}

section {
    padding: 90px 0;
}

.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.hero-inner {
    max-width: 750px;
}

.small-title {
    color: #a9d9ff;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-size: .8rem;
    margin-bottom: 25px;
}

h1 {
    font-size: clamp(3.5rem, 13vw, 7rem);
    color: #bde5ff;
    text-shadow: 0 0 30px rgba(130,200,255,.35);
    margin-bottom: 20px;
}

h2 {
    font-size: clamp(2rem, 6vw, 3.5rem);
    color: #bde5ff;
    margin-bottom: 25px;
}

h3 {
    color: #c8eaff;
    margin-bottom: 12px;
}

p {
    line-height: 1.8;
    color: #d9e9f7;
}

.hero p {
    font-size: 1.15rem;
    max-width: 650px;
    margin: auto;
}

.button {
    display: inline-block;
    margin-top: 35px;
    padding: 14px 25px;
    border: 1px solid rgba(180,220,255,.5);
    border-radius: 50px;
    color: #eaf7ff;
    text-decoration: none;
    background: rgba(120,190,255,.08);
    transition: .3s;
    cursor: pointer;
    font-family: inherit;
    font-size: 1rem;
}

.button:hover {
    background: rgba(150,210,255,.2);
    transform: translateY(-3px);
    box-shadow: 0 0 25px rgba(150,210,255,.2);
}

.card {
    background: rgba(255,255,255,.055);
    border: 1px solid rgba(180,220,255,.15);
    border-radius: 25px;
    padding: 30px;
    margin: 25px 0;
    backdrop-filter: blur(10px);
    box-shadow: 0 10px 40px rgba(0,0,0,.2);
}

.center {
    text-align: center;
}

.intro {
    font-size: 1.15rem;
    max-width: 720px;
    margin: auto;
}

.reasons {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 15px;
    margin-top: 35px;
}

.reason {
    border: 1px solid rgba(180,220,255,.15);
    border-radius: 18px;
    padding: 20px;
    background: rgba(255,255,255,.045);
    transition: .3s;
}

.reason:hover {
    transform: translateY(-4px);
    background: rgba(150,210,255,.09);
}

.reason-number {
    color: #83caff;
    font-size: .85rem;
    margin-bottom: 8px;
}

.timeline {
    position: relative;
    margin-top: 40px;
}

.timeline-item {
    padding: 25px;
    margin: 20px 0;
    border-left: 2px solid #83caff;
    background: rgba(255,255,255,.04);
    border-radius: 0 18px 18px 0;
}

.favourites {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 15px;
    margin-top: 30px;
}

.favourite {
    text-align: center;
    padding: 25px 15px;
    border-radius: 20px;
    background: rgba(255,255,255,.05);
    border: 1px solid rgba(180,220,255,.12);
}

.favourite-icon {
    font-size: 2rem;
    margin-bottom: 10px;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
    margin-top: 30px;
}

.photo {
    min-height: 220px;
    border-radius: 22px;
    border: 1px dashed rgba(180,220,255,.35);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 20px;
    color: #a9cce5;
    background: rgba(255,255,255,.035);
}

.photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 18px;
}

.open-when {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-top: 30px;
}

.open-button {
    padding: 25px 15px;
    border: 1px solid rgba(180,220,255,.2);
    border-radius: 20px;
    background: rgba(255,255,255,.045);
    color: #dff3ff;
    font-family: inherit;
    font-size: 1rem;
    cursor: pointer;
    transition: .3s;
}

.open-button:hover {
    background: rgba(150,210,255,.12);
    transform: translateY(-3px);
}

.future-list {
    list-style: none;
    margin-top: 30px;
}

.future-list li {
    padding: 18px;
    margin: 10px 0;
    border-radius: 15px;
    background: rgba(255,255,255,.045);
    border: 1px solid rgba(180,220,255,.1);
}

.future-list li::before {
    content: "✦ ";
    color: #83caff;
}

.final-card {
    text-align: center;
    padding: 50px 30px;
    background: linear-gradient(
        135deg,
        rgba(130,200,255,.1),
        rgba(255,255,255,.04)
    );
}

.hidden-message {
    display: none;
    margin-top: 30px;
    font-size: 1.2rem;
    line-height: 1.9;
    color: #dff3ff;
}

footer {
    text-align: center;
    padding: 40px 20px;
    color: #7fa3bd;
    font-size: .9rem;
}

@media (max-width: 600px) {
    section {
        padding: 65px 0;
    }

    .card {
        padding: 22px;
    }

    .gallery {
        grid-template-columns: 1fr;
    }

    .photo {
        min-height: 180px;
    }
}
</style>
</head>

<body>

<!-- =====================================================
     EDIT HERE 🩵
     Change the things below whenever you want!
     You do NOT need to change the rest of the code.
     ===================================================== -->

<script>
const birthday = {
    name: "Lola",
    age: 27,
    from: "Bree / Putiputi",

    birthdayMessage:
        "Today isn't just about another year passing. It's about celebrating the person who makes my world softer simply by existing in it.",

    intro:
        "So I made you a tiny universe. Every little corner is here because it reminds me of you.",

    finalMessage:
        "If I could give you anything for your birthday, it would be the ability to see yourself through my eyes. Maybe then you'd finally understand why I love you so much. Happy 27th birthday, my love. 🩵"
};


/* 27 REASONS */
const reasons = [
    "Your hazel eyes.",
    "Your voice.",
    "The way you make me feel at home.",
    "Your little laugh.",
    "Your beautiful heart.",
    "Your softness.",
    "Your strength.",
    "Your love for otters.",
    "Your baby blue world.",
    "Your black coffee.",
    "The way you make me smile.",
    "The way you listen.",
    "Your little habits.",
    "Your beautiful soul.",
    "The way you calm me.",
    "The way you make ordinary moments special.",
    "Your kindness.",
    "Your patience.",
    "Your silly side.",
    "Your beautiful mind.",
    "The way you make distance feel smaller.",
    "The way you became my home.",
    "The way you make me feel understood.",
    "Your dreams.",
    "Your courage.",
    "The person you are becoming.",
    "Simply because you're Lola."
];


/* LOLA'S FAVOURITE THINGS */
const favourites = [
    ["🩵", "Baby blue"],
    ["🦦", "Otters"],
    ["☕", "Black coffee"],
    ["🍣", "Sushi"],
    ["🌊", "The ocean"],
    ["⭐", "Stars"],
    ["🤎", "Hazel eyes"],
    ["🎂", "Twenty-seven"]
];


/* OPEN WHEN MESSAGES */
const openWhen = {
    miss:
        "If you miss me, look at the sky. Somewhere beneath that same sky is a girl who is missing you too. Distance doesn't change where my heart belongs. 🩵",

    sad:
        "If you're sad, you don't have to pretend to be okay. Come exactly as you are. You can be messy, tired, quiet or broken. I'll still love you through every version of you.",

    sleep:
        "If you can't sleep, imagine me beside you. No distance. No screens. Just quiet, warm and safe. Close your eyes and imagine my hand in yours.",

    loved:
        "If you need to feel loved, remember this: you are loved beyond the kilometres between us, beyond the days we spend apart and beyond anything words could ever properly explain."
};


/* OUR FUTURE */
const future = [
    "The ocean",
    "A sunrise together",
    "Somewhere new",
    "A little place of our own",
    "A sky full of stars"
];


/* GALLERY CAPTIONS */
const gallery = [
    "Our first picture",
    "Our second picture",
    "Our third picture",
    "Our fourth picture"
];
</script>


<!-- HERO -->

<section class="hero">
    <div class="container hero-inner">

        <div class="small-title">
            A little universe made for
        </div>

        <h1 id="heroName"></h1>

        <p>
            <span id="heroAge"></span> years of you.
        </p>

        <p style="margin-top:20px;">
            And somehow, in all the billions of people in this world,
            I got lucky enough to find you.
        </p>

        <a href="#birthday" class="button">
            Enter my little universe ↓
        </a>

    </div>
</section>


<!-- BIRTHDAY -->

<section id="birthday">
    <div class="container">

        <div class="card center">

            <div class="small-title">
                September skies & birthday stars
            </div>

            <h2 id="birthdayTitle"></h2>

            <p class="intro" id="birthdayMessage"></p>

            <p class="intro" style="margin-top:20px;" id="birthdayIntro"></p>

        </div>

    </div>
</section>


<!-- 27 REASONS -->

<section>
    <div class="container">

        <div class="center">
            <div class="small-title">
                Twenty-seven little reasons
            </div>

            <h2>Why I love you</h2>

            <p>
                One for every year you've existed in this world.
            </p>
        </div>

        <div class="reasons" id="reasons"></div>

    </div>
</section>


<!-- OUR STORY -->

<section>
    <div class="container">

        <div class="center">
            <div class="small-title">
                Our little story
            </div>

            <h2>Then, now, always.</h2>
        </div>

        <div class="timeline">

            <div class="timeline-item">
                <h3>Then there was you.</h3>
                <p>
                    Somewhere among all the people in this enormous world,
                    our paths crossed.
                </p>
            </div>

            <div class="timeline-item">
                <h3>The distance.</h3>
                <p>
                    Different countries. Different skies. So many kilometres.
                    And somehow you still became one of the closest people to my heart.
                </p>
            </div>

            <div class="timeline-item">
                <h3>All the little things.</h3>
                <p>
                    The conversations, the laughter, the quiet moments,
                    the storms, the sleepy nights and everything in between.
                </p>
            </div>

            <div class="timeline-item">
                <h3>And now you're 27.</h3>
                <p>
                    Another year of you existing, growing, dreaming and becoming
                    the beautiful person you are.
                </p>
            </div>

        </div>

    </div>
</section>


<!-- FAVOURITES -->

<section>
    <div class="container">

        <div class="center">

            <div class="small-title">
                Things that remind me of you
            </div>

            <h2>Your little universe</h2>

        </div>

        <div class="favourites" id="favourites"></div>

    </div>
</section>


<!-- GALLERY -->

<section>
    <div class="container">

        <div class="center">

            <div class="small-title">
                Us
            </div>

            <h2>Pieces of us ♡</h2>

            <p>
                Add your favourite pictures of us here.
            </p>

        </div>

        <div class="gallery" id="gallery"></div>

    </div>
</section>


<!-- OPEN WHEN -->

<section>
    <div class="container">

        <div class="center">

            <div class="small-title">
                For whenever you need me
            </div>

            <h2>Open when...</h2>

        </div>

        <div class="open-when">

            <button class="open-button" onclick="showMessage('miss')">
                💌 You miss me
            </button>

            <button class="open-button" onclick="showMessage('sad')">
                🩵 You're sad
            </button>

            <button class="open-button" onclick="showMessage('sleep')">
                🌙 You can't sleep
            </button>

            <button class="open-button" onclick="showMessage('loved')">
                ⭐ You need to feel loved
            </button>

        </div>

    </div>
</section>


<!-- MUSIC -->

<section>
    <div class="container">

        <div class="card center">

            <div class="small-title">
                A song for you 🎵
            </div>

            <h2>The One That Got Away</h2>

            <p>
                This song has always felt like it belongs somewhere
                inside our story.
            </p>

            <p style="margin-top:20px;">
                🎵 Add an audio file you're legally allowed to use here.
            </p>

            <div style="margin-top:25px;">
                <audio controls style="width:100%; max-width:500px;">
                    <source src="birthday-song.mp3" type="audio/mpeg">
                    Your browser does not support audio.
                </audio>
            </div>

        </div>

    </div>
</section>


<!-- FUTURE -->

<section>
    <div class="container">

        <div class="center">

            <div class="small-title">
                Things I want with you
            </div>

            <h2>Our someday</h2>

        </div>

        <ul class="future-list" id="future"></ul>

    </div>
</section>


<!-- FINAL -->

<section>
    <div class="container">

        <div class="card final-card">

            <div class="small-title">
                One last thing
            </div>

            <h2>Until I can give you these things in person...</h2>

            <p>
                let this little universe hold them for me.
            </p>

            <p style="margin-top:20px;">
                Love always,<br>
                <span id="fromName"></span> ♡
            </p>

            <button class="button" onclick="revealFinal()">
                One last thing... 🩵
            </button>

            <div class="hidden-message" id="finalMessage"></div>

        </div>

    </div>
</section>


<footer>
    Made with an unreasonable amount of love by
    <span id="footerName"></span> ♡
</footer>


<script>

/* HERO */

document.getElementById("heroName").textContent =
    birthday.name + " ♡";

document.getElementById("heroAge").textContent =
    "Twenty-seven";

document.getElementById("birthdayTitle").textContent =
    "Happy " + birthday.age + "th Birthday, my love.";

document.getElementById("birthdayMessage").textContent =
    birthday.birthdayMessage;

document.getElementById("birthdayIntro").textContent =
    birthday.intro;

document.getElementById("fromName").textContent =
    birthday.from;

document.getElementById("footerName").textContent =
    birthday.from;


/* REASONS */

const reasonsContainer =
    document.getElementById("reasons");

reasons.forEach((reason, index) => {

    const div = document.createElement("div");

    div.className = "reason";

    div.innerHTML = `
        <div class="reason-number">
            ${index + 1} / ${birthday.age}
        </div>

        <p>${reason}</p>
    `;

    reasonsContainer.appendChild(div);
});


/* FAVOURITES */

const favouritesContainer =
    document.getElementById("favourites");

favourites.forEach(item => {

    const div = document.createElement("div");

    div.className = "favourite";

    div.innerHTML = `
        <div class="favourite-icon">
            ${item[0]}
        </div>

        <p>${item[1]}</p>
    `;

    favouritesContainer.appendChild(div);
});


/* GALLERY */

const galleryContainer =
    document.getElementById("gallery");

gallery.forEach(caption => {

    const div = document.createElement("div");

    div.className = "photo";

    div.innerHTML = `
        <span>
            📷<br><br>
            ${caption}
        </span>
    `;

    galleryContainer.appendChild(div);
});


/* FUTURE */

const futureContainer =
    document.getElementById("future");

future.forEach(item => {

    const li = document.createElement("li");

    li.textContent = item;

    futureContainer.appendChild(li);
});


/* OPEN WHEN */

function showMessage(type) {

    alert(openWhen[type]);

}


/* FINAL MESSAGE */

function revealFinal() {

    const message =
        document.getElementById("finalMessage");

    message.textContent =
        birthday.finalMessage;

    message.style.display = "block";

}

</script>

</body>
</html>
