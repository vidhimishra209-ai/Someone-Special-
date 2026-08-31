<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For My Behen, Khanak ♡</title>

<style>

/* =========================
   BASIC SETUP
========================= */

*{
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    margin:0;
    font-family:Georgia,serif;
    color:#514653;
    background:#fbf5f8;
    overflow-x:hidden;
}

.screen{
    min-height:100vh;
    padding:35px 20px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
}

.hidden{
    display:none !important;
}

.container{
    width:100%;
    max-width:750px;
}

button{
    border:none;
    cursor:pointer;
    font-family:Georgia,serif;
}

/* =========================
   FLOATING HEARTS
========================= */

#background{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
}

.float{
    position:absolute;
    animation:floatUp linear infinite;
    opacity:.4;
}

@keyframes floatUp{
    from{
        transform:translateY(110vh) rotate(0deg);
        opacity:0;
    }

    20%{
        opacity:.5;
    }

    to{
        transform:translateY(-20vh) rotate(180deg);
        opacity:0;
    }
}

/* =========================
   LANDING
========================= */

#home{
    color:white;
    background:
        radial-gradient(circle at 50% 30%,#83718f,#51485c 45%,#292631);
    position:relative;
    overflow:hidden;
}

.moon{
    width:110px;
    height:110px;
    background:#fff8dc;
    border-radius:50%;
    margin:0 auto 30px;
    box-shadow:0 0 50px rgba(255,248,220,.5);
}

.mini{
    letter-spacing:4px;
    text-transform:uppercase;
    font-size:11px;
    opacity:.7;
    margin-bottom:20px;
}

h1{
    font-size:clamp(48px,13vw,85px);
    font-style:italic;
    font-weight:normal;
    margin:0 0 20px;
}

.homeText{
    max-width:550px;
    margin:auto;
    line-height:1.9;
    opacity:.85;
}

.mainBtn{
    margin-top:35px;
    padding:15px 30px;
    border-radius:40px;
    background:white;
    color:#65556c;
    font-size:16px;
    transition:.3s;
}

.mainBtn:hover{
    transform:translateY(-4px) scale(1.03);
}

/* =========================
   ENVELOPE
========================= */

#envelopeScreen{
    background:linear-gradient(135deg,#faedf3,#eee8f6);
}

.title{
    font-size:38px;
    font-style:italic;
    color:#745d70;
    margin-bottom:40px;
}

.envelope{
    width:310px;
    height:200px;
    position:relative;
    margin:auto;
    cursor:pointer;
}

.envBack{
    position:absolute;
    inset:0;
    background:#e2cedc;
    border-radius:8px;
    box-shadow:0 20px 45px rgba(80,60,80,.2);
}

.flap{
    position:absolute;
    top:0;
    left:0;
    width:0;
    height:0;
    border-left:155px solid transparent;
    border-right:155px solid transparent;
    border-top:110px solid #c6adbf;
    transform-origin:top;
    transition:1s;
    z-index:4;
}

.letterPeek{
    position:absolute;
    width:245px;
    height:160px;
    left:32px;
    top:18px;
    background:#fffdfa;
    z-index:2;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:21px;
    font-style:italic;
    color:#80697b;
    transition:1s;
}

.envelope.open .flap{
    transform:rotateX(180deg);
    z-index:1;
}

.envelope.open .letterPeek{
    transform:translateY(-110px);
}

.tap{
    margin-top:45px;
    color:#897688;
}

/* =========================
   CASE AGAINST VIDHI
========================= */

#case{
    background:#fff9fb;
}

.caseBox{
    background:white;
    padding:40px 25px;
    border-radius:25px;
    box-shadow:0 15px 45px rgba(90,65,90,.12);
}

.caseTitle{
    font-size:40px;
    color:#725d70;
}

.verdict{
    margin:25px 0;
    line-height:1.8;
}

.evidenceGrid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
    margin-top:30px;
}

.evidence{
    padding:25px 12px;
    background:#f6edf3;
    border-radius:18px;
    cursor:pointer;
    transition:.3s;
}

.evidence:hover{
    transform:translateY(-5px);
}

.evidenceText{
    display:none;
    margin-top:15px;
    font-size:13px;
    line-height:1.7;
}

.evidence.active .evidenceText{
    display:block;
}

.guilty{
    margin-top:30px;
    padding:13px 25px;
    border-radius:30px;
    background:#846d80;
    color:white;
}

/* =========================
   APOLOGY
========================= */

#apology{
    background:#fcf7f9;
}

.apologyBox{
    max-width:700px;
}

.apologyBox h2{
    font-size:45px;
    color:#745d70;
    font-style:italic;
}

.apologyIntro{
    line-height:1.9;
    margin-bottom:35px;
}

.apologyButtons{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:15px;
}

.apologyButton{
    padding:20px;
    border-radius:18px;
    background:white;
    color:#6f5b6c;
    box-shadow:0 8px 25px rgba(90,70,90,.09);
    font-size:15px;
}

.apologyButton:hover{
    background:#f6edf3;
}

.apologyAnswer{
    display:none;
    margin-top:25px;
    padding:25px;
    background:#f8eff4;
    border-radius:20px;
    line-height:1.9;
    animation:appear .5s;
}

.apologyAnswer.show{
    display:block;
}

@keyframes appear{
    from{
        opacity:0;
        transform:translateY(10px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* =========================
   QUIZ
========================= */

#quiz{
    background:linear-gradient(135deg,#f1ebf6,#fff1f4);
}

.quizBox{
    max-width:650px;
}

.quizBox h2{
    font-size:42px;
    color:#735e71;
}

.question{
    background:white;
    margin:18px 0;
    padding:25px;
    border-radius:20px;
    box-shadow:0 8px 25px rgba(90,70,90,.08);
}

.option{
    display:block;
    width:100%;
    padding:12px;
    margin:8px 0;
    border-radius:20px;
    background:#f5edf3;
    color:#655565;
}

.option:hover{
    background:#e8d9e4;
}

.result{
    margin-top:25px;
    font-size:18px;
    line-height:1.8;
}

/* =========================
   BEHEN ACHIEVEMENTS
========================= */

#achievements{
    background:#fffafa;
}

.badges{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:18px;
    margin-top:35px;
}

.badge{
    padding:30px 15px;
    background:white;
    border-radius:22px;
    box-shadow:0 10px 30px rgba(90,70,90,.09);
    cursor:pointer;
    transition:.4s;
}

.badge:hover{
    transform:rotate(-2deg) scale(1.03);
}

.badgeInfo{
    display:none;
    margin-top:12px;
    font-size:14px;
    line-height:1.7;
}

.badge.active .badgeInfo{
    display:block;
}

/* =========================
   800 KM
========================= */

#distance{
    background:
        radial-gradient(circle at 50% 35%,#82718d,#4e4659 55%,#292631);
    color:white;
}

.distanceBox{
    max-width:750px;
}

.distanceBox h2{
    font-size:45px;
    font-style:italic;
}

.map{
    margin:50px auto;
    max-width:600px;
    position:relative;
    height:100px;
}

.line{
    position:absolute;
    top:50%;
    left:8%;
    right:8%;
    height:2px;
    background:rgba(255,255,255,.4);
}

.dot{
    position:absolute;
    top:calc(50% - 9px);
    width:18px;
    height:18px;
    border-radius:50%;
    background:white;
    box-shadow:0 0 20px white;
}

.you{
    left:5%;
}

.khanak{
    right:5%;
}

.label{
    position:absolute;
    top:70%;
    font-size:14px;
    opacity:.8;
}

.labelYou{
    left:0;
}

.labelKhanak{
    right:0;
}

.distanceText{
    line-height:1.9;
    opacity:.85;
}

.hugBtn{
    margin-top:25px;
    padding:15px 25px;
    border-radius:30px;
    background:white;
    color:#62546a;
}

#hugMessage{
    margin-top:25px;
    font-size:18px;
    line-height:1.8;
}

/* =========================
   BEHEN PACT
========================= */

#pact{
    background:#fbf5f8;
}

.pactBox{
    max-width:650px;
}

.pactBox h2{
    font-size:45px;
    color:#735e71;
}

.pactItem{
    margin:15px 0;
    padding:22px;
    background:white;
    border-radius:18px;
    cursor:pointer;
    box-shadow:0 7px 20px rgba(90,70,90,.07);
}

.pactAnswer{
    display:none;
    margin-top:10px;
    line-height:1.7;
}

.pactItem.active .pactAnswer{
    display:block;
}

/* =========================
   FINAL
========================= */

#final{
    background:
        radial-gradient(circle at 50% 35%,#776680,#403848 55%,#211f27);
    color:white;
}

.finalBox{
    max-width:650px;
}

.finalHeart{
    font-size:70px;
    animation:pulse 2s infinite;
}

@keyframes pulse{
    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.12);
    }
}

.finalBox h2{
    font-size:50px;
    font-style:italic;
}

.finalBox p{
    line-height:2;
    opacity:.85;
}

.restore{
    margin-top:25px;
    padding:15px 28px;
    border-radius:30px;
    background:white;
    color:#62546a;
}

#finalMessage{
    display:none;
    margin-top:35px;
    font-size:22px;
    line-height:1.9;
    animation:appear 1s;
}

/* =========================
   MOBILE
========================= */

@media(max-width:600px){

    .evidenceGrid{
        grid-template-columns:1fr;
    }

    .apologyButtons{
        grid-template-columns:1fr;
    }

    .badges{
        grid-template-columns:1fr;
    }

    .envelope{
        transform:scale(.85);
    }

    .envelope:hover{
        transform:scale(.85);
    }

    .caseTitle,
    .apologyBox h2,
    .quizBox h2,
    .distanceBox h2,
    .pactBox h2{
        font-size:35px;
    }

    .finalBox h2{
        font-size:40px;
    }
}

</style>
</head>


<body>

<div id="background"></div>


<!-- =========================
     1. LANDING
========================= -->

<section id="home" class="screen">

<div class="container">

<div class="moon"></div>

<div class="mini">
A very important announcement
</div>

<h1>
For my behen, Khanak ♡
</h1>

<p class="homeText">
Okay. So apparently I messed up.
And instead of sending you a boring paragraph,
I made an entire website because apparently
that's how I deal with problems now.
</p>

<button class="mainBtn" onclick="show('envelopeScreen','home')">
Enter the nonsense →
</button>

</div>

</section>


<!-- =========================
     2. ENVELOPE
========================= -->

<section id="envelopeScreen" class="screen hidden">

<div class="container">

<h2 class="title">
First things first...
</h2>

<div class="envelope" id="envelope" onclick="openEnvelope()">

<div class="letterPeek">
For Khanak ♡
</div>

<div class="envBack"></div>

<div class="flap"></div>

</div>

<p class="tap">
Tap the envelope.
Yes, actually tap it.
</p>

</div>

</section>


<!-- =========================
     3. COURTROOM
========================= -->

<section id="case" class="screen hidden">

<div class="caseBox">

<h2 class="caseTitle">
⚖️ The Case Against Vidhi
</h2>

<p class="verdict">

<strong>Accused:</strong> Vidhi<br>
<strong>Crime:</strong> Being an idiot<br>
<strong>Victim:</strong> Khanak's patience<br>
<strong>Current status:</strong> Guilty 😔

</p>

<p>
Tap the evidence.
</p>

<div class="evidenceGrid">

<div class="evidence" onclick="toggle(this)">
😂
<h3>The Situation</h3>

<div class="evidenceText">
The whole G situation became so chaotic
that it somehow turned into comedy material.
Unfortunately, I took that a little too far.
</div>

</div>


<div class="evidence" onclick="toggle(this)">
👀
<h3>Vaishnavi</h3>

<div class="evidenceText">
I shared a summary with her.
I know now that I should have thought about
whether that was something you'd be comfortable with.
</div>

</div>


<div class="evidence" onclick="toggle(this)">
🤦🏻‍♀️
<h3>My Brain</h3>

<div class="evidenceText">
Apparently my brain decided:
"Funny situation = share it."
My brain has been formally fired.
</div>

</div>

</div>

<button class="guilty"
onclick="show('apology','case')">

Fine. I'm guilty. 😭

</button>

</div>

</section>


<!-- =========================
     4. APOLOGY
========================= -->

<section id="apology" class="screen hidden">

<div class="apologyBox">

<h2>
Okay. Seriously now. 🤍
</h2>

<p class="apologyIntro">
I know I hurt you.
I know what I did was wrong,
and I'm genuinely sorry.
I don't want to defend it or make excuses.
I just want to explain what I understand now.
Tap each part.
</p>

<div class="apologyButtons">

<button class="apologyButton"
onclick="answer('a1')">
What I'm sorry for
</button>

<button class="apologyButton"
onclick="answer('a2')">
What I understand now
</button>

<button class="apologyButton"
onclick="answer('a3')">
What I should've done
</button>

<button class="apologyButton"
onclick="answer('a4')">
What I want you to know
</button>

</div>

<div id="a1" class="apologyAnswer">
I'm sorry for sharing something involving you
without thinking enough about how you'd feel about it.
Even though the situation was funny to us,
I should still have respected that boundary.
</div>

<div id="a2" class="apologyAnswer">
I understand that my intention doesn't cancel
out the effect of what I did.
I didn't mean to hurt you,
but I did, and I'm sorry.
</div>

<div id="a3" class="apologyAnswer">
I should have stopped and thought before telling
someone else about it.
I should have considered your privacy first.
That part was on me.
</div>

<div id="a4" class="apologyAnswer">
You're my behen.
We've had so many stupid conversations,
random laughs and completely unnecessary chaos.
One stupid mistake doesn't change how much
I value our behenship.
</div>

<button class="mainBtn"
onclick="show('quiz','apology')">

Okay, next →
</button>

</div>

</section>


<!-- =========================
     5. QUIZ
========================= -->

<section id="quiz" class="screen hidden">

<div class="quizBox">

<h2>
Behen Knowledge Test™
</h2>

<p>
Let's see if this behenship has been functioning correctly.
</p>


<div class="question">

<p>
<strong>1. What is our greatest communication skill?</strong>
</p>

<button class="option"
onclick="quizAnswer(this,true)">
Understanding each other's silence
</button>

<button class="option"
onclick="quizAnswer(this,false)">
Talking 24/7
</button>

<button class="option"
onclick="quizAnswer(this,false)">
Being normal
</button>

</div>


<div class="question">

<p>
<strong>2. What do we excel at?</strong>
</p>

<button class="option"
onclick="quizAnswer(this,false)">
Being sensible
</button>

<button class="option"
onclick="quizAnswer(this,true)">
Laughing at ridiculous things
</button>

<button class="option"
onclick="quizAnswer(this,false)">
Making calm decisions
</button>

</div>


<div class="question">

<p>
<strong>3. How far apart are we?</strong>
</p>

<button class="option"
onclick="quizAnswer(this,true)">
About 800 km
</button>

<button class="option"
onclick="quizAnswer(this,false)">
8 km
</button>

<button class="option"
onclick="quizAnswer(this,false)">
8,000 km
</button>

</div>

<div id="quizResult" class="result">
Tap your answers 👀
</div>

<button class="mainBtn"
onclick="show('achievements','quiz')">

Continue →
</button>

</div>

</section>


<!-- =========================
     6. ACHIEVEMENTS
========================= -->

<section id="achievements" class="screen hidden">

<div class="container">

<h2 class="title">
🏆 Behenship Achievements
</h2>

<p>
Tap the achievements.
You earned these through sheer chaos.
</p>

<div class="badges">

<div class="badge" onclick="toggle(this)">
😂
<h3>Professional Laughers</h3>

<div class="badgeInfo">
Some things are objectively not funny.
We laugh anyway.
</div>

</div>


<div class="badge" onclick="toggle(this)">
💀
<h3>Chaos Survivors</h3>

<div class="badgeInfo">
Somehow we have survived multiple situations
that should probably have required adult supervision.
</div>

</div>


<div class="badge" onclick="toggle(this)">
🌙
<h3>Long Distance Legends</h3>

<div class="badgeInfo">
800 km apart and still somehow managing
to remain in each other's lives.
</div>

</div>


<div class="badge" onclick="toggle(this)">
🤍
<h3>Still My Behen</h3>

<div class="badgeInfo">
A stupid fight doesn't delete the entire
behenship database.
</div>

</div>

</div>

<button class="mainBtn"
onclick="show('distance','achievements')">

Next →
</button>

</div>

</section>


<!-- =========================
     7. 800 KM
========================= -->

<section id="distance" class="screen hidden">

<div class="distanceBox">

<h2>
800 km apart.
</h2>

<p class="distanceText">
Apparently geography decided that being besties
wasn't difficult enough already.
</p>

<div class="map">

<div class="line"></div>

<div class="dot you"></div>
<div class="dot khanak"></div>

<div class="label labelYou">
You
</div>

<div class="label labelKhanak">
Khanak
</div>

</div>

<p class="distanceText">
Physical distance: <strong>800 km</strong><br>
Emotional distance after this fight:
<strong>absolutely unacceptable.</strong>
</p>

<button class="hugBtn"
onclick="sendHug()">

Send a virtual hug 🫂

</button>

<div id="hugMessage"></div>

<button class="hugBtn"
onclick="show('pact','distance')">

Continue →
</button>

</div>

</section>


<!-- =========================
     8. BEHEN PACT
========================= -->

<section id="pact" class="screen hidden">

<div class="pactBox">

<h2>
The Behen Pact ♡
</h2>

<p>
Tap each rule.
</p>

<div class="pactItem" onclick="toggle(this)">
🤍 Rule 01
<div class="pactAnswer">
We can get angry at each other,
but we talk about it instead of silently
letting everything become weird.
</div>
</div>

<div class="pactItem" onclick="toggle(this)">
😂 Rule 02
<div class="pactAnswer">
We are legally required to continue
making each other laugh over stupid things.
</div>
</div>

<div class="pactItem" onclick="toggle(this)">
🌷 Rule 03
<div class="pactAnswer">
Mistakes can be acknowledged,
apologised for and learned from.
</div>
</div>

<div class="pactItem" onclick="toggle(this)">
🫶 Rule 04
<div class="pactAnswer">
800 km cannot cancel a behenship.
Nice try, geography.
</div>
</div>

<button class="mainBtn"
onclick="show('final','pact')">

Restore Behenship →
</button>

</div>

</section>


<!-- =========================
     9. FINAL
========================= -->

<section id="final" class="screen hidden">

<div class="finalBox">

<div class="finalHeart">
♡
</div>

<h2>
Behenship Status
</h2>

<p>
One stupid fight: <strong>YES</strong><br>
One person who messed up: <strong>ME</strong><br>
One genuine apology: <strong>ALSO ME</strong><br>
Behenship cancelled: <strong>ABSOLUTELY NOT</strong>
</p>

<p>
I don't expect you to instantly stop being angry.
I just wanted you to know that I know I was wrong,
I'm genuinely sorry, and I really value you.
</p>

<button class="restore"
onclick="restore()">

RESTORE BEHENSHIP ♡

</button>

<div id="finalMessage">

✨ BEHENSHIP RESTORED ✨

<br><br>

800 km apart.<br>
One stupid fight.<br>
Still my behen. 🤍

<br><br>

Now please stop giving me dry replies,
because I have suffered enough. 😭

<br><br>

— Vidhi ♡

</div>

</div>

</section>


<script>

/* =========================
   BACKGROUND HEARTS
========================= */

const background =
document.getElementById("background");

for(let i=0;i<35;i++){

    const item=document.createElement("div");

    item.className="float";

    item.innerHTML=
    Math.random()>.5 ? "♡" : "✦";

    item.style.left=
    Math.random()*100+"%";

    item.style.fontSize=
    (Math.random()*15+8)+"px";

    item.style.animationDuration=
    (Math.random()*8+7)+"s";

    item.style.animationDelay=
    Math.random()*8+"s";

    background.appendChild(item);
}


/* =========================
   SECTION NAVIGATION
========================= */

function show(next,current){

    document.getElementById(current)
    .classList.add("hidden");

    document.getElementById(next)
    .classList.remove("hidden");

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });
}


/* =========================
   ENVELOPE
========================= */

function openEnvelope(){

    const env=
    document.getElementById("envelope");

    if(env.classList.contains("open"))
    return;

    env.classLis
