
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For Kulott 💌</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500;600&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow-x: hidden;
    font-family: "Poppins", sans-serif;
    background:
        radial-gradient(circle at top left, #fff 0%, transparent 30%),
        radial-gradient(circle at bottom right, #ffd8e8 0%, transparent 35%),
        linear-gradient(135deg, #ffeaf3, #fff8fb, #fce1ed);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px;
    color: #5d4650;
}

/* =========================
   FLOATING DECORATIONS
========================= */

.decor {
    position: fixed;
    pointer-events: none;
    z-index: 0;
    opacity: .65;
    animation: floating 5s ease-in-out infinite;
}

.d1 {
    top: 8%;
    left: 7%;
    font-size: 30px;
}

.d2 {
    top: 15%;
    right: 8%;
    font-size: 24px;
    animation-delay: 1s;
}

.d3 {
    bottom: 12%;
    left: 9%;
    font-size: 25px;
    animation-delay: 2s;
}

.d4 {
    bottom: 8%;
    right: 10%;
    font-size: 32px;
    animation-delay: 3s;
}

.d5 {
    top: 50%;
    left: 3%;
    font-size: 18px;
    animation-delay: 1.5s;
}

.d6 {
    top: 45%;
    right: 3%;
    font-size: 20px;
    animation-delay: 2.5s;
}

@keyframes floating {
    0%,100% {
        transform: translateY(0) rotate(-5deg);
    }

    50% {
        transform: translateY(-18px) rotate(7deg);
    }
}

/* =========================
   ENVELOPE PAGE
========================= */

.envelope-page {
    position: relative;
    z-index: 2;
    text-align: center;
    animation: fadeIn 1.2s ease;
}

.small-title {
    font-size: 13px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: #bd7c98;
    margin-bottom: 8px;
}

.envelope-page h1 {
    font-family: "Great Vibes", cursive;
    font-size: 55px;
    color: #c95f88;
    font-weight: normal;
    margin-bottom: 8px;
}

.subtitle {
    color: #8d6d78;
    font-size: 14px;
    margin-bottom: 35px;
}

/* ENVELOPE */

.envelope-wrapper {
    width: 340px;
    height: 230px;
    margin: auto;
    position: relative;
    perspective: 1000px;
}

.envelope {
    width: 100%;
    height: 100%;
    position: relative;
    cursor: pointer;
    transition: transform .4s ease;
    filter: drop-shadow(0 18px 20px rgba(190, 91, 130, .20));
}

.envelope:hover {
    transform: translateY(-7px);
}

/* BACK */

.envelope-back {
    position: absolute;
    width: 100%;
    height: 100%;
    background: #f7b2cc;
    border-radius: 13px;
}

/* LETTER INSIDE */

.letter-paper {
    position: absolute;
    width: 86%;
    height: 85%;
    left: 7%;
    top: 7%;
    background: #fffdfb;
    border-radius: 6px;
    z-index: 2;
    transition: transform 1s cubic-bezier(.2,.8,.2,1);
    display: flex;
    justify-content: center;
    align-items: center;
    color: #c7658b;
    font-family: "Great Vibes", cursive;
    font-size: 25px;
    box-shadow: 0 3px 10px rgba(0,0,0,.05);
}

/* FRONT */

.envelope-front {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 62%;
    background: #ee8fb3;
    clip-path: polygon(
        0 0,
        50% 57%,
        100% 0,
        100% 100%,
        0 100%
    );
    z-index: 4;
    border-radius: 0 0 13px 13px;
}

/* FLAP */

.envelope-flap {
    position: absolute;
    top: 0;
    width: 100%;
    height: 63%;
    background: #f6a8c5;
    clip-path: polygon(
        0 0,
        100% 0,
        50% 100%
    );
    transform-origin: top center;
    transition: transform 1s cubic-bezier(.2,.8,.2,1);
    z-index: 5;
    border-radius: 13px 13px 0 0;
}

/* SEAL */

.seal {
    position: absolute;
    z-index: 6;
    left: 50%;
    top: 55%;
    transform: translate(-50%, -50%);
    width: 55px;
    height: 55px;
    background: #c85b82;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 22px;
    box-shadow:
        0 5px 12px rgba(150, 60, 95, .25),
        inset 0 0 0 3px rgba(255,255,255,.25);
    transition: opacity .5s ease, transform .5s ease;
}

/* OPENING */

.envelope.open .envelope-flap {
    transform: rotateX(180deg);
}

.envelope.open .letter-paper {
    transform: translateY(-120px);
}

.envelope.open .seal {
    opacity: 0;
    transform: translate(-50%, -50%) scale(.5);
}

.open-text {
    margin-top: 32px;
    color: #a16f82;
    font-size: 13px;
    letter-spacing: 1px;
}

.click-heart {
    display: inline-block;
    margin-top: 10px;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0%,100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.18);
    }
}

/* =========================
   LETTER
========================= */

.letter-page {
    display: none;
    width: 100%;
    max-width: 720px;
    position: relative;
    z-index: 3;
    animation: letterAppear 1.2s ease forwards;
}

.paper {
    position: relative;
    background: rgba(255,255,255,.96);
    border-radius: 25px;
    padding: 55px 55px 45px;
    box-shadow:
        0 25px 60px rgba(165, 78, 111, .15),
        0 5px 15px rgba(165, 78, 111, .08);
    border: 1px solid #f7d4e1;
}

/* PAPER CORNERS */

.paper::before,
.paper::after {
    content: "🌷";
    position: absolute;
    font-size: 25px;
}

.paper::before {
    top: 18px;
    left: 22px;
}

.paper::after {
    bottom: 18px;
    right: 22px;
}

.top-decoration {
    text-align: center;
    font-size: 24px;
    letter-spacing: 8px;
    margin-bottom: 10px;
}

.paper h2 {
    text-align: center;
    font-family: "Great Vibes", cursive;
    font-size: 48px;
    color: #c85d86;
    font-weight: normal;
    margin-bottom: 30px;
}

.letter-content {
    font-size: 15px;
    line-height: 2;
    color: #654f58;
}

.letter-content p {
    margin-bottom: 20px;
}

.highlight {
    color: #c85d86;
    font-weight: 600;
}

.signature {
    text-align: right;
    margin-top: 35px;
    font-family: "Great Vibes", cursive;
    font-size: 30px;
    color: #c85d86;
}

.bottom-message {
    text-align: center;
    margin-top: 30px;
    padding-top: 20px;
    border-top: 1px solid #f2d8e2;
    color: #b17b91;
    font-size: 12px;
    letter-spacing: 1px;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes letterAppear {
    from {
        opacity: 0;
        transform: translateY(40px) scale(.96);
    }

    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}

/* =========================
   MOBILE
========================= */

@media(max-width: 600px) {

    body {
        padding: 18px;
    }

    .envelope-page h1 {
        font-size: 45px;
    }

    .envelope-wrapper {
        width: 290px;
        height: 195px;
    }

    .paper {
        padding: 40px 25px 35px;
    }

    .paper h2 {
        font-size: 40px;
    }

    .letter-content {
        font-size: 14px;
        line-height: 1.85;
    }

    .signature {
        font-size: 27px;
    }
}
</style>
</head>

<body>

<!-- FLOATING DECORATIONS -->

<div class="decor d1">🌸</div>
<div class="decor d2">✨</div>
<div class="decor d3">🌷</div>
<div class="decor d4">🎀</div>
<div class="decor d5">♡</div>
<div class="decor d6">✦</div>


<!-- =========================
     ENVELOPE
========================= -->

<section class="envelope-page" id="envelopePage">

    <div class="small-title">
        A little something for you
    </div>

    <h1>For You, Kulott</h1>

    <p class="subtitle">
        There's something I really want to tell you...
    </p>

    <div class="envelope-wrapper">

        <div class="envelope" id="envelope" onclick="openLetter()">

            <div class="envelope-back"></div>

            <div class="letter-paper">
                A letter for you 🌷
            </div>

            <div class="envelope-flap"></div>

            <div class="envelope-front"></div>

            <div class="seal">
                ♥
            </div>

        </div>

    </div>

    <p class="open-text">
        Click the envelope to open
        <span class="click-heart">♡</span>
    </p>

</section>


<!-- =========================
     LETTER
========================= -->

<section class="letter-page" id="letterPage">

    <div class="paper">

        <div class="top-decoration">
            🌷　🎀　♡　🎀　🌷
        </div>

        <h2>Dear Kulott...</h2>

        <div class="letter-content">

            <p>
                Hi Lot,
            </p>

            <p>
                I know <span class="highlight">akig kapa sakon</span>,
                and I really want to say that
                <strong>I'm really sorry</strong> for everything.
                I know nga may mga actions ko nga nakapasakit sa imo,
                and honestly, I feel really guilty about it.
            </p>

            <p>
                Sorry gid sa mga actions nga ginhimo ko.
                I know nga maybe I didn't think enough before doing
                some things, and I understand if nasakitan ka or
                na-disappoint ka because of me.
            </p>

            <p>
                I never wanted to hurt you or make you feel that way.
                If I could take back those things, I would.
                But I know I can't change what already happened,
                so all I can do now is admit my mistake,
                learn from it, and sincerely say
                <strong>I'm sorry.</strong>
            </p>

            <p>
                I don't expect you to forgive me right away.
                I understand if you need time, and I respect
                whatever you feel right now.
                I just hope that someday, we can talk about everything
                and fix what happened between us.
            </p>

            <p>
                <span class="highlight">I really hope maging okay na ta.</span>
                I don't want this misunderstanding to make us
                completely distant from each other.
                I really value you and our friendship,
                and I don't want to lose that just because of
                the mistakes I made.
            </p>

            <p>
                I'm sorry if there were times nga I acted without
                thinking about your feelings.
                I'm sorry for the things I did wrong,
                for the moments I made you feel bad,
                and for anything I did that made you question
                how much I value you.
            </p>

            <p>
                I hope you know that this apology is genuine.
                I'm not saying sorry just because I want everything
                to be okay immediately.
                I'm saying sorry because
                <strong>I know I made a mistake,
                and I genuinely regret it.</strong>
            </p>

            <p>
                I hope we can slowly fix things,
                even if it takes time.
                I don't want to force anything.
                I just want you to know that I'm willing to make things
                right and do better next time.
            </p>

            <p>
                Again, I'm really, really sorry, Lot.
                I hope someday,
                <span class="highlight">maging okay na gid ta.</span>
            </p>

            <p>
                Please take your time.
                I just wanted you to know what's in my heart
                and how sorry I truly am.
            </p>

        </div>

        <div class="signature">
            I'm really sorry, Kulott. ♡
        </div>

        <div class="bottom-message">
            🌸 Some things are worth fixing. 🌸
        </div>

    </div>

</section>


<script>

function openLetter() {

    const envelope = document.getElementById("envelope");
    const envelopePage = document.getElementById("envelopePage");
    const letterPage = document.getElementById("letterPage");

    envelope.classList.add("open");

    setTimeout(function() {

        envelopePage.style.opacity = "0";

        setTimeout(function() {
            envelopePage.style.display = "none";
            letterPage.style.display = "block";
        }, 500);

    }, 1100);
}

</script>

</body>
</html>
