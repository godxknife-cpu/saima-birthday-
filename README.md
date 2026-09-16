# saima-birthday-
happy_birthday_saima.<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Saima 🎂</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "Courier New", monospace;
    background: #050509;
    color: white;
    overflow-x: hidden;
}

/* ---------- BACKGROUND ---------- */

body::before {
    content: "";
    position: fixed;
    inset: 0;
    background:
        radial-gradient(circle at 20% 20%, rgba(0, 255, 255, .12), transparent 30%),
        radial-gradient(circle at 80% 70%, rgba(255, 0, 180, .12), transparent 30%);
    pointer-events: none;
    z-index: -2;
}

/* ---------- CODE SCREEN ---------- */

#terminal {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px;
}

.terminal-box {
    width: min(850px, 100%);
    background: rgba(5, 5, 10, .92);
    border: 1px solid #00ffff;
    border-radius: 18px;
    box-shadow:
        0 0 20px rgba(0,255,255,.25),
        inset 0 0 30px rgba(0,255,255,.04);
    overflow: hidden;
}

.terminal-top {
    height: 42px;
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 0 15px;
    background: #101018;
    border-bottom: 1px solid rgba(0,255,255,.25);
}

.dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
}

.red { background: #ff4b4b; }
.yellow { background: #ffd93d; }
.green { background: #39ff88; }

.terminal-content {
    padding: 30px;
    min-height: 430px;
    line-height: 1.8;
    color: #00ff9d;
}

.prompt {
    color: #00ffff;
}

.cursor {
    display: inline-block;
    width: 9px;
    height: 19px;
    background: #00ff9d;
    animation: blink .7s infinite;
    vertical-align: middle;
}

@keyframes blink {
    50% { opacity: 0; }
}

.start-btn {
    margin-top: 25px;
    padding: 14px 25px;
    border: 1px solid #00ffff;
    background: transparent;
    color: #00ffff;
    border-radius: 10px;
    cursor: pointer;
    font-family: inherit;
    font-size: 16px;
    transition: .3s;
}

.start-btn:hover {
    background: #00ffff;
    color: #050509;
    box-shadow: 0 0 25px #00ffff;
}

/* ---------- MAIN ---------- */

#main {
    display: none;
    min-height: 100vh;
}

.hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px 20px;
    position: relative;
}

.small-code {
    color: #00ffff;
    letter-spacing: 3px;
    font-size: 13px;
    margin-bottom: 20px;
}

.hero h1 {
    font-family: Arial, sans-serif;
    font-size: clamp(48px, 12vw, 110px);
    background: linear-gradient(90deg, #00ffff, #ffffff, #ff54d9);
    -webkit-background-clip: text;
    color: transparent;
    text-shadow: 0 0 35px rgba(0,255,255,.2);
}

.hero h2 {
    margin-top: 10px;
    color: #ddd;
    font-size: clamp(18px, 4vw, 28px);
}

.hero p {
    margin-top: 25px;
    max-width: 650px;
    color: #aaa;
    line-height: 1.7;
}

.reveal-btn {
    margin-top: 35px;
    padding: 16px 30px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    font-weight: bold;
    font-size: 16px;
    color: #050509;
    background: linear-gradient(90deg, #00ffff, #ff54d9);
    box-shadow: 0 0 30px rgba(0,255,255,.3);
    transition: .3s;
}

.reveal-btn:hover {
    transform: scale(1.07);
}

/* ---------- SECTIONS ---------- */

.section {
    padding: 90px 20px;
    max-width: 1000px;
    margin: auto;
    text-align: center;
}

.section h2 {
    font-family: Arial, sans-serif;
    font-size: clamp(30px, 6vw, 50px);
    margin-bottom: 45px;
}

.code-title {
    color: #00ffff;
    font-size: 13px;
    letter-spacing: 3px;
    margin-bottom: 10px;
}

/* ---------- REASONS ---------- */

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}

.card {
    padding: 28px 20px;
    border: 1px solid rgba(0,255,255,.25);
    background: rgba(255,255,255,.03);
    border-radius: 18px;
    transition: .3s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: #00ffff;
    box-shadow: 0 0 25px rgba(0,255,255,.12);
}

.card span {
    font-size: 35px;
}

.card h3 {
    margin: 15px 0 10px;
    color: #00ffff;
}

.card p {
    color: #aaa;
    line-height: 1.6;
}

/* ---------- MESSAGE ---------- */

.message-box {
    padding: 35px 25px;
    border-radius: 20px;
    border: 1px solid #ff54d9;
    background: rgba(255,84,217,.04);
    box-shadow: 0 0 30px rgba(255,84,217,.08);
}

.message-box p {
    color: #ddd;
    font-family: Arial, sans-serif;
    font-size: 18px;
    line-height: 1.9;
}

/* ---------- SECRET ---------- */

.secret {
    margin-top: 30px;
    padding: 20px;
    border: 1px dashed #00ff9d;
    border-radius: 15px;
    color: #00ff9d;
    cursor: pointer;
}

.secret-content {
    display: none;
    margin-top: 15px;
    color: white;
    line-height: 1.7;
}

/* ---------- PHOTO ---------- */

.photo-box {
    width: min(400px, 90%);
    margin: auto;
    aspect-ratio: 1 / 1;
    border-radius: 25px;
    border: 2px dashed #00ffff;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    background: rgba(0,255,255,.03);
}

.photo-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.photo-placeholder {
    padding: 30px;
    color: #777;
}

/* ---------- FOOTER ---------- */

footer {
    text-align: center;
    padding: 50px 20px;
    color: #666;
}

footer span {
    color: #00ffff;
}

/* ---------- FLOATING PARTICLES ---------- */

.particle {
    position: fixed;
    width: 4px;
    height: 4px;
    background: #00ffff;
    border-radius: 50%;
    pointer-events: none;
    animation: float 7s linear infinite;
    opacity: .5;
}

@keyframes float {
    from {
        transform: translateY(100vh);
    }
    to {
        transform: translateY(-10vh);
    }
}

/* ---------- CONFETTI ---------- */

.confetti {
    position: fixed;
    width: 9px;
    height: 15px;
    top: -20px;
    z-index: 100;
    animation: fall linear forwards;
}

@keyframes fall {
    to {
        transform: translateY(110vh) rotate(720deg);
    }
}

@media(max-width:600px) {
    .terminal-content {
        padding: 20px;
        font-size: 13px;
    }

    .section {
        padding: 70px 18px;
    }
}
</style>
</head>

<body>

<!-- ================= TERMINAL ================= -->

<section id="terminal">

    <div class="terminal-box">

        <div class="terminal-top">
            <div class="dot red"></div>
            <div class="dot yellow"></div>
            <div class="dot green"></div>
        </div>

        <div class="terminal-content">

            <div id="terminalText"></div>
            <span class="cursor"></span>

            <br>

            <button class="start-btn" onclick="startBirthday()">
                &gt; EXECUTE BIRTHDAY.exe
            </button>

        </div>

    </div>

</section>


<!-- ================= MAIN WEBSITE ================= -->

<main id="main">

    <section class="hero">

        <div class="small-code">
            SYSTEM.STATUS = "SPECIAL_PERSON_FOUND";
        </div>

        <h1>SAIMA</h1>

        <h2>🎂 Happy Birthday 🎂</h2>

        <p>
            Some people enter your life normally...
            and somehow become unforgettable.
            Today is about celebrating one of those people.
        </p>

        <button class="reveal-btn" onclick="revealMessage()">
            ✨ Open Your Birthday Surprise
        </button>

    </section>


    <!-- ================= REASONS ================= -->

    <section class="section">

        <div class="code-title">
            // WHY_SAIMA_IS_SPECIAL
        </div>

        <h2>5 Reasons 💙</h2>

        <div class="cards">

            <div class="card">
                <span>🫶</span>
                <h3>Understanding</h3>
                <p>
                    You understand things even when words aren't enough.
                </p>
            </div>

            <div class="card">
                <span>😊</span>
                <h3>Good Vibes</h3>
                <p>
                    Somehow you can make normal conversations memorable.
                </p>
            </div>

            <div class="card">
                <span>🤝</span>
                <h3>Support</h3>
                <p>
                    A real friend knows how to be there when it matters.
                </p>
            </div>

            <div class="card">
                <span>✨</span>
                <h3>Unique</h3>
                <p>
                    There is only one Saima — and that's what makes you special.
                </p>
            </div>

            <div class="card">
                <span>💙</span>
                <h3>Memories</h3>
                <p>
                    The little moments and random conversations become great memories.
                </p>
            </div>

        </div>

    </section>


    <!-- ================= PERSONAL MESSAGE ================= -->

    <section class="section">

        <div class="code-title">
            // PERSONAL_MESSAGE
        </div>

        <h2>A Message For You 💌</h2>

        <div class="message-box">

            <p>
                Dear Saima,<br><br>

                Happy Birthday! 🎂✨<br><br>

                I hope this new year of your life brings you
                lots of happiness, success, laughter and beautiful memories.
                You deserve all the good things that life has to offer.<br><br>

                Keep smiling, keep being yourself,
                and keep making the people around you smile.
                Never forget how special you are to the people who care about you. 💙<br><br>

                Have an amazing birthday! 🎉
            </p>

        </div>

    </section>


    <!-- ================= PHOTO ================= -->

    <section class="section">

        <div class="code-title">
            // MEMORY_DATABASE
        </div>

        <h2>One Special Memory 📸</h2>

        <div class="photo-box">

            <!--
                Replace "saima.jpg" with your photo filename.
                Example:
                <img src="saima.jpg" alt="Saima">
            -->

            <div class="photo-placeholder">
                📸<br><br>
                Add your favourite photo of Saima here.
            </div>

        </div>

    </section>


    <!-- ================= SECRET ================= -->

    <section class="section">

        <div class="code-title">
            // HIDDEN_FILE
        </div>

        <h2>There Is A Secret... 👀</h2>

        <div class="secret" onclick="openSecret()">

            🔐 CLICK TO DECRYPT

            <div class="secret-content" id="secretContent">

                Access granted... ✅<br><br>

                If you're reading this,
                just remember one thing:<br><br>

                <strong>
                    You're genuinely an important part of some
                    really good memories. 💙
                </strong>
                <br><br>

                Don't forget to smile today. 😊

            </div>

        </div>

    </section>


    <footer>

        SYSTEM MESSAGE:
        <span>SAIMA.exe successfully celebrated 🎂</span>

        <br><br>

        Made with 💙 for Saima

    </footer>

</main>


<script>

/* ================= TERMINAL TYPING ================= */

const lines = [
    "> Initializing birthday_protocol...",
    "> Scanning friendship_database...",
    "> Searching for special person...",
    "> Person found: SAIMA",
    "> Friendship_level: SPECIAL",
    "> Birthday_mode: ACTIVATED",
    "> Loading happiness.exe...",
    "> Loading memories...",
    "> Loading surprises...",
    "> System ready."
];

let lineIndex = 0;
let charIndex = 0;

const terminalText = document.getElementById("terminalText");

function typeLine() {

    if (lineIndex >= lines.length) return;

    if (charIndex < lines[lineIndex].length) {

        terminalText.innerHTML += lines[lineIndex].charAt(charIndex);

        charIndex++;

        setTimeout(typeLine, 28);

    } else {

        terminalText.innerHTML += "<br>";

        lineIndex++;
        charIndex = 0;

        setTimeout(typeLine, 250);
    }
}

typeLine();


/* ================= START BIRTHDAY ================= */

function startBirthday() {

    document.getElementById("terminal").style.display = "none";

    document.getElementById("main").style.display = "block";

    window.scrollTo(0, 0);

    createParticles();

    setTimeout(() => {
        createConfetti();
    }, 500);
}


/* ================= REVEAL ================= */

function revealMessage() {

    createConfetti();

    alert(
        "🎂 HAPPY BIRTHDAY SAIMA! 🎂\n\n" +
        "Today is your special day.\n" +
        "Keep smiling and keep shining! ✨💙"
    );

}


/* ================= SECRET ================= */

function openSecret() {

    const secret = document.getElementById("secretContent");

    if (secret.style.display === "block") {

        secret.style.display = "none";

    } else {

        secret.style.display = "block";

        createConfetti();

    }
}


/* ================= PARTICLES ================= */

function createParticles() {

    for (let i = 0; i < 35; i++) {

        const particle = document.createElement("div");

        particle.className = "particle";

        particle.style.left = Math.random() * 100 + "%";

        particle.style.animationDelay =
            Math.random() * 7 + "s";

        particle.style.animationDuration =
            (5 + Math.random() * 7) + "s";

        document.body.appendChild(particle);
    }
}


/* ================= CONFETTI ================= */

function createConfetti() {

    for (let i = 0; i < 100; i++) {

        const confetti = document.createElement("div");

        confetti.className = "confetti";

        confetti.style.left =
            Math.random() * 100 + "vw";

        confetti.style.animationDuration =
            (2 + Math.random() * 4) + "s";

        confetti.style.transform =
            `rotate(${Math.random() * 360}deg)`;

        confetti.style.background =
            `hsl(${Math.random() * 360}, 100%, 65%)`;

        document.body.appendChild(confetti);

        setTimeout(() => {
            confetti.remove();
        }, 6500);
    }
}

</script>

</body>
</html>
