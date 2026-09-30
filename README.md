<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Teachers' Day 💐</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Poppins", Arial, sans-serif;
    overflow: hidden;

    background: linear-gradient(
        135deg,
        #ff9a9e,
        #fad0c4,
        #a18cd1,
        #fbc2eb,
        #84fab0
    );

    background-size: 400% 400%;
    animation: backgroundMove 12s ease infinite;
}

@keyframes backgroundMove {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

/* Floating decorations */

.float {
    position: fixed;
    font-size: 35px;
    animation: floating 5s ease-in-out infinite;
    pointer-events: none;
    z-index: 1;
}

.f1 {
    top: 8%;
    left: 8%;
}

.f2 {
    top: 15%;
    right: 10%;
    animation-delay: 1s;
}

.f3 {
    bottom: 10%;
    left: 12%;
    animation-delay: 2s;
}

.f4 {
    bottom: 15%;
    right: 10%;
    animation-delay: 3s;
}

.f5 {
    top: 45%;
    left: 3%;
    animation-delay: 1.5s;
}

.f6 {
    top: 50%;
    right: 3%;
    animation-delay: 2.5s;
}

@keyframes floating {
    0%, 100% {
        transform: translateY(0) rotate(0deg);
    }

    50% {
        transform: translateY(-25px) rotate(12deg);
    }
}

/* Main card */

.card {
    position: relative;
    z-index: 5;

    width: min(92%, 850px);
    min-height: 90vh;

    padding: 35px 25px 30px;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    text-align: center;

    background: rgba(255, 255, 255, 0.20);
    border: 2px solid rgba(255, 255, 255, 0.55);
    border-radius: 35px;

    backdrop-filter: blur(18px);
    -webkit-backdrop-filter: blur(18px);

    box-shadow:
        0 25px 70px rgba(65, 25, 90, 0.35),
        inset 0 0 30px rgba(255,255,255,0.15);

    animation: cardAppear 1.2s ease;
}

@keyframes cardAppear {
    from {
        opacity: 0;
        transform: scale(.8) translateY(30px);
    }

    to {
        opacity: 1;
        transform: scale(1) translateY(0);
    }
}

/* Top label */

.badge {
    background: rgba(255,255,255,.85);
    color: #8e44ad;
    padding: 9px 22px;
    border-radius: 30px;
    font-size: 14px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 15px;
    box-shadow: 0 8px 20px rgba(0,0,0,.12);
}

/* Heading */

h1 {
    color: white;
    font-size: clamp(42px, 8vw, 75px);
    line-height: 1.05;

    text-shadow:
        3px 3px 0 #8e44ad,
        0 0 25px rgba(255,255,255,.7);

    animation: titleGlow 2s ease-in-out infinite alternate;
}

@keyframes titleGlow {
    from {
        text-shadow:
            3px 3px 0 #8e44ad,
            0 0 10px white;
    }

    to {
        text-shadow:
            3px 3px 0 #8e44ad,
            0 0 30px white;
    }
}

.subtitle {
    margin-top: 12px;
    color: white;
    font-size: clamp(18px, 3vw, 25px);
    font-weight: 500;
}

/* Teacher photo */

.photo-frame {
    position: relative;
    width: 250px;
    height: 250px;
    margin: 25px 0;

    padding: 8px;

    border-radius: 50%;

    background: linear-gradient(
        135deg,
        #ff4d6d,
        #ffd166,
        #06d6a0,
        #4cc9f0,
        #c77dff
    );

    background-size: 300% 300%;
    animation: rainbow 5s linear infinite;
}

@keyframes rainbow {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

.photo {
    width: 100%;
    height: 100%;
    object-fit: cover;

    border-radius: 50%;
    border: 6px solid white;

    box-shadow:
        0 15px 40px rgba(0,0,0,.3);

    transition: .5s;
}

.photo:hover {
    transform: scale(1.05) rotate(2deg);
}

/* Message */

.message {
    max-width: 650px;
    color: white;
    font-size: 18px;
    line-height: 1.7;

    text-shadow: 0 2px 4px rgba(0,0,0,.2);
}

.message strong {
    color: #fff8a8;
}

/* Quote */

.quote {
    margin-top: 12px;
    color: white;
    font-size: 17px;
    font-style: italic;
}

/* Button */

.music-button,
.celebrate-button {
    border: none;
    cursor: pointer;

    padding: 13px 25px;
    margin: 8px;

    border-radius: 30px;

    font-size: 16px;
    font-weight: bold;

    color: #8e44ad;
    background: white;

    box-shadow: 0 8px 20px rgba(0,0,0,.2);

    transition: .3s;
}

.music-button:hover,
.celebrate-button:hover {
    transform: translateY(-4px) scale(1.05);

    color: white;

    background: linear-gradient(
        135deg,
        #8e44ad,
        #e84393
    );
}

.controls {
    margin-top: 18px;
}

/* Music visualizer */

.visualizer {
    display: flex;
    justify-content: center;
    align-items: flex-end;

    gap: 5px;
    height: 30px;

    margin-top: 10px;
}

.bar {
    width: 5px;
    height: 10px;

    border-radius: 10px;

    background: white;

    animation: musicBars .7s ease-in-out infinite alternate;
}

.bar:nth-child(2) {
    animation-delay: .1s;
}

.bar:nth-child(3) {
    animation-delay: .2s;
}

.bar:nth-child(4) {
    animation-delay: .3s;
}

.bar:nth-child(5) {
    animation-delay: .4s;
}

@keyframes musicBars {
    from {
        height: 7px;
    }

    to {
        height: 28px;
    }
}

/* Confetti */

.confetti {
    position: fixed;

    width: 10px;
    height: 18px;

    top: -30px;

    z-index: 100;

    animation: confettiFall 4s linear forwards;
}

@keyframes confettiFall {
    to {
        transform:
            translateY(110vh)
            rotate(720deg);
    }
}

/* Hearts */

.heart {
    position: fixed;
    bottom: -30px;

    font-size: 25px;

    animation: heartUp 5s linear forwards;

    z-index: 3;
}

@keyframes heartUp {
    0% {
        transform: translateY(0) scale(.7);
        opacity: 0;
    }

    15% {
        opacity: 1;
    }

    100% {
        transform: translateY(-110vh) scale(1.5);
        opacity: 0;
    }
}

/* Mobile */

@media (max-width: 600px) {

    .card {
        width: 94%;
        min-height: 92vh;
        padding: 25px 18px;
    }

    .photo-frame {
        width: 190px;
        height: 190px;
        margin: 20px 0;
    }

    .message {
        font-size: 15px;
    }

    .quote {
        font-size: 14px;
    }

    .float {
        font-size: 25px;
    }
}
</style>
</head>

<body>

<!-- Floating decorations -->

<div class="float f1">🌸</div>
<div class="float f2">⭐</div>
<div class="float f3">📚</div>
<div class="float f4">💜</div>
<div class="float f5">✏️</div>
<div class="float f6">🌈</div>


<!-- Main Greeting Card -->

<div class="card">

    <div class="badge">
        💐 SPECIAL GREETING 💐
    </div>

    <h1>
        Happy<br>
        Teachers' Day!
    </h1>

    <div class="subtitle">
        🌟 To an Amazing Teacher 🌟
    </div>


    <!-- ONE PHOTO -->

    <div class="photo-frame">

        <!-- Replace teacher.jpg with your photo -->
        <img
            src="pic.jpg"
            alt="My Wonderful Teacher"
            class="photo"
        >

    </div>


    <!-- Message -->

    <div class="message">

        <strong>Dear Sir Randy Bello</strong>

        <br><br>

        happy Teacher’s day sir! Thank you for your patience, guidance, and dedication.
      we truly appreciate everything you do for us mahal ka namin sirr!>_<

        <br><br>

        godbless you always sir randy

    </div>


    <div class="quote">
        “A great teacher inspires, encourages,
        and changes lives.” ✨
    </div>


    <!-- Buttons -->

    <div class="controls">

        <button
            class="music-button"
            onclick="toggleMusic()"
            id="musicBtn">
            🎵 Play Music
        </button>

        <button
            class="celebrate-button"
            onclick="celebrate()">
            🎉 Celebrate!
        </button>

    </div>


    <!-- Music Visualizer -->

    <div class="visualizer" id="visualizer">

        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>

    </div>

</div>


<!-- MUSIC -->

<audio id="music" loop>

    <!--
        Put your music file in the same folder
        and name it:

        teachers-day.mp3
    -->

    <source
        src="evergreen.mp3"
        type="audio/mpeg">

</audio>


<script>

const music = document.getElementById("music");
const musicBtn = document.getElementById("musicBtn");
const visualizer = document.getElementById("visualizer");

let playing = false;


/* MUSIC */

function toggleMusic() {

    if (!playing) {

        music.play();

        playing = true;

        musicBtn.innerHTML = "🔊 Music On";

        visualizer.style.opacity = "1";

    } else {

        music.pause();

        playing = false;

        musicBtn.innerHTML = "🎵 Play Music";

        visualizer.style.opacity = ".4";
    }
}


/* CONFETTI */

function celebrate() {

    for (let i = 0; i < 100; i++) {

        const confetti =
            document.createElement("div");

        confetti.className = "confetti";

        const colors = [
            "#ff4d6d",
            "#ffd166",
            "#06d6a0",
            "#4cc9f0",
            "#c77dff",
            "#ffffff",
            "#ff9f1c"
        ];

        confetti.style.background =
            colors[
                Math.floor(
                    Math.random() * colors.length
                )
            ];

        confetti.style.left =
            Math.random() * 100 + "vw";

        confetti.style.animationDuration =
            (Math.random() * 2 + 2) + "s";

        confetti.style.animationDelay =
            Math.random() * .8 + "s";

        document.body.appendChild(confetti);


        setTimeout(() => {
            confetti.remove();
        }, 5000);
    }


    /* Hearts */

    for (let i = 0; i < 20; i++) {

        const heart =
            document.createElement("div");

        heart.className = "heart";

        heart.innerHTML =
            Math.random() > .5 ? "💖" : "💐";

        heart.style.left =
            Math.random() * 100 + "vw";

        heart.style.animationDuration =
            (Math.random() * 2 + 3) + "s";

        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5500);
    }
}


/* Small automatic celebration */

setTimeout(() => {

    for (let i = 0; i < 20; i++) {

        const heart =
            document.createElement("div");

        heart.className = "heart";

        heart.innerHTML = "✨";

        heart.style.left =
            Math.random() * 100 + "vw";

        heart.style.animationDuration =
            (Math.random() * 3 + 3) + "s";

        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 6500);
    }

}, 1000);

</script>

</body>
</html>

