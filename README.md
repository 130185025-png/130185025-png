<!DOCTYPE html>
<html lang="ta">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>Amma, Unakkaga ❤️</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+Thambi+2:wght@500;700&family=Catamaran:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
<style>
  :root{
    --rose-deep:#c4536b;
    --rose:#e88ca0;
    --rose-soft:#f7c9d3;
    --blush:#fdeef1;
    --cream:#fff8f3;
    --plum:#54293f;
    --gold:#e0a94f;
    --gold-soft:#f3d9a4;
    --line-max: 560px;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html,body{
    height:100%;
    background: var(--blush);
    color: var(--plum);
    font-family:'Catamaran', sans-serif;
    overflow-x:hidden;
  }
  body{
    background:
      radial-gradient(circle at 15% 10%, rgba(255,255,255,.9), transparent 40%),
      radial-gradient(circle at 85% 85%, rgba(247,201,211,.9), transparent 45%),
      linear-gradient(160deg, var(--blush) 0%, #fbe0e6 55%, var(--rose-soft) 100%);
    min-height:100vh;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:flex-start;
    position:relative;
  }
  .tamil{ font-family:'Baloo Thambi 2', 'Catamaran', sans-serif; }

  /* ---------- floating hearts background ---------- */
  #heartLayer{
    position:fixed; inset:0; pointer-events:none; z-index:0; overflow:hidden;
  }
  .fheart{
    position:absolute;
    bottom:-10%;
    font-size: 22px;
    color: var(--rose);
    opacity:.55;
    animation: floatUp linear infinite;
    will-change: transform;
  }
  @keyframes floatUp{
    0%{ transform: translateY(0) translateX(0) rotate(0deg); opacity:0;}
    8%{ opacity:.6;}
    100%{ transform: translateY(-115vh) translateX(var(--drift,20px)) rotate(25deg); opacity:0;}
  }

  /* ---------- sparkles ---------- */
  .sparkle{
    position:absolute;
    width:10px; height:10px;
    pointer-events:none;
  }
  .sparkle::before{
    content:'✦';
    color: var(--gold);
    font-size:14px;
    display:block;
    animation: twinkle 1.6s ease-in-out infinite;
  }
  @keyframes twinkle{
    0%,100%{ opacity:.2; transform:scale(.7);}
    50%{ opacity:1; transform:scale(1.15);}
  }

  /* ---------- shared layout ---------- */
  .stage{
    position:relative;
    z-index:2;
    width:100%;
    min-height:100vh;
    display:none;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    padding: 48px 24px 64px;
  }
  .stage.active{
    display:flex;
    animation: stageIn .7s ease both;
  }
  @keyframes stageIn{
    from{ opacity:0; transform: translateY(18px);}
    to{ opacity:1; transform: translateY(0);}
  }

  .card{
    width:100%;
    max-width: var(--line-max);
    text-align:center;
  }

  .eyebrow{
    display:inline-block;
    font-size:13px;
    letter-spacing:.04em;
    color: var(--rose-deep);
    margin-bottom: 14px;
    opacity:.85;
  }

  h1.title{
    font-family:'Baloo Thambi 2', sans-serif;
    font-weight:700;
    font-size: clamp(26px, 6vw, 38px);
    color: var(--plum);
    line-height:1.35;
    margin-bottom: 14px;
  }
  p.sub{
    font-size: clamp(16px,4vw,18px);
    color:#7a4a5c;
    line-height:1.6;
    margin-bottom: 30px;
  }

  /* buttons */
  .btn{
    appearance:none; border:none; cursor:pointer;
    font-family:'Catamaran', sans-serif;
    font-weight:700;
    font-size:17px;
    color:#fff;
    background: linear-gradient(135deg, var(--rose-deep), var(--rose));
    padding: 15px 34px;
    border-radius: 999px;
    box-shadow: 0 10px 24px -8px rgba(196,83,107,.55);
    transition: transform .18s ease, box-shadow .18s ease;
    position:relative;
  }
  .btn:active{ transform: scale(.96); }
  .btn:hover{ transform: translateY(-2px); box-shadow: 0 14px 28px -8px rgba(196,83,107,.65); }
  .btn.ghost{
    background: transparent;
    color: var(--rose-deep);
    border: 2px solid var(--rose-soft);
    box-shadow:none;
  }
  .btn.pulse{ animation: pulseBtn 1.8s ease-in-out infinite; }
  @keyframes pulseBtn{
    0%,100%{ box-shadow: 0 10px 24px -8px rgba(196,83,107,.55);}
    50%{ box-shadow: 0 14px 32px -6px rgba(196,83,107,.8);}
  }

  .heart-icon{ display:inline-block; animation: beat 1.1s ease-in-out infinite; }
  @keyframes beat{
    0%,100%{ transform:scale(1);}
    50%{ transform:scale(1.22);}
  }

  /* ---------- welcome ---------- */
  .locket{
    width:120px; height:120px;
    margin: 0 auto 26px;
    border-radius:50%;
    background: linear-gradient(150deg, var(--rose-soft), var(--gold-soft));
    display:flex; align-items:center; justify-content:center;
    font-size:52px;
    box-shadow: 0 18px 40px -14px rgba(196,83,107,.5), inset 0 0 0 6px rgba(255,255,255,.6);
    animation: floaty 3.2s ease-in-out infinite;
  }
  @keyframes floaty{
    0%,100%{ transform: translateY(0) rotate(-2deg);}
    50%{ transform: translateY(-10px) rotate(2deg);}
  }

  /* ---------- questions ---------- */
  .progress-dots{
    display:flex; gap:8px; justify-content:center; margin-bottom:22px;
  }
  .progress-dots span{
    width:8px; height:8px; border-radius:50%;
    background: var(--rose-soft);
    transition: all .3s ease;
  }
  .progress-dots span.done{ background: var(--rose-deep); width:22px; border-radius:6px;}
  .progress-dots span.current{ background: var(--rose); }

  .q-icon{ font-size:44px; margin-bottom:12px; display:block; }
  .q-text{
    font-family:'Baloo Thambi 2', sans-serif;
    font-size: clamp(19px,5vw,23px);
    line-height:1.55;
    color: var(--plum);
    margin-bottom: 30px;
    font-weight:500;
  }
  .options{
    display:flex; flex-direction:column; gap:14px;
    max-width:340px; margin: 0 auto;
  }
  .opt-btn{
    appearance:none; cursor:pointer;
    font-family:'Catamaran', sans-serif;
    font-size:17px; font-weight:600;
    color: var(--rose-deep);
    background:#fff;
    border: 2px solid var(--rose-soft);
    padding:16px 20px;
    border-radius:18px;
    transition: transform .15s ease, background .2s ease, border-color .2s ease;
    box-shadow: 0 8px 18px -12px rgba(196,83,107,.4);
  }
  .opt-btn:active{ transform: scale(.97); }
  .opt-btn.yes{ border-color: var(--rose-deep); }
  .opt-btn.chosen{
    background: linear-gradient(135deg, var(--rose-deep), var(--rose));
    color:#fff; border-color: transparent;
  }
  .transition-msg{
    font-family:'Baloo Thambi 2', sans-serif;
    font-size: clamp(18px,5vw,22px);
    color: var(--plum);
    line-height:1.6;
  }

  /* ---------- gift box ---------- */
  .gift-wrap{ position:relative; width:220px; height:200px; margin: 10px auto 34px; }
  .gift-box{
    position:absolute; bottom:0; left:0; right:0; margin:auto;
    width:180px; height:130px;
    background: linear-gradient(135deg, var(--rose-deep), var(--rose));
    border-radius: 10px;
    box-shadow: 0 20px 40px -16px rgba(196,83,107,.6);
  }
  .gift-box::before{ /* vertical ribbon */
    content:''; position:absolute; left:50%; top:0; bottom:0; width:22px;
    transform: translateX(-50%);
    background: var(--gold);
  }
  .gift-lid{
    position:absolute; left:-10px; right:-10px; top:-34px;
    height:44px;
    background: linear-gradient(135deg, var(--gold), var(--gold-soft));
    border-radius:10px;
    box-shadow: 0 10px 18px -10px rgba(196,83,107,.5);
    transform-origin: left center;
    transition: transform .8s cubic-bezier(.4,1.6,.4,1), opacity .6s ease .3s;
  }
  .gift-lid::before{
    content:''; position:absolute; left:50%; top:-22px; width:26px; height:34px;
    transform: translateX(-50%);
    background: var(--gold);
    border-radius: 50% 50% 0 0 / 60% 60% 0 0;
  }
  .gift-wrap.open .gift-lid{
    transform: rotate(-115deg) translateY(-6px);
    opacity:0;
  }
  .gift-wrap.open .gift-box{ animation: giftShake .5s ease; }
  @keyframes giftShake{
    0%,100%{ transform: translateX(0);}
    25%{ transform: translateX(-4px) rotate(-1deg);}
    75%{ transform: translateX(4px) rotate(1deg);}
  }
  .burst{
    position:absolute; left:50%; top:-10px; transform: translateX(-50%);
    font-size:0; opacity:0; pointer-events:none;
  }
  .gift-wrap.open .burst{ opacity:1; }
  .burst span{
    position:absolute; font-size:20px;
    animation: burstOut .9s ease forwards;
    opacity:0;
  }

  /* ---------- photos ---------- */
  .slideshow{
    position:relative;
    width:100%; max-width:340px;
    aspect-ratio: 3/4;
    margin: 0 auto 22px;
    border-radius:20px;
    overflow:hidden;
    box-shadow: 0 26px 50px -20px rgba(84,41,63,.45);
    background:#fff;
  }
  .slide{
    position:absolute; inset:0;
    opacity:0;
    transition: opacity 1s ease;
  }
  .slide.show{ opacity:1; }
  .slide img{
    width:100%; height:100%; object-fit:cover; display:block;
  }
  .slide-cap{
    position:absolute; left:0; right:0; bottom:0;
    padding: 26px 16px 16px;
    background: linear-gradient(to top, rgba(84,41,63,.75), transparent);
    color:#fff;
    font-size:14px;
    text-align:left;
  }
  .slide-dots{ display:flex; gap:6px; justify-content:center; margin-bottom:22px; flex-wrap:wrap; }
  .slide-dots span{ width:6px; height:6px; border-radius:50%; background: var(--rose-soft); }
  .slide-dots span.active{ background: var(--rose-deep); }

  /* ---------- song ---------- */
  .song-art{
    width:200px; height:200px; margin: 0 auto 22px;
    border-radius:50%;
    overflow:hidden;
    border: 6px solid #fff;
    box-shadow: 0 20px 40px -16px rgba(84,41,63,.5);
    animation: spinSlow 14s linear infinite;
    animation-play-state: paused;
  }
  .song-art.playing{ animation-play-state: running; }
  .song-art img{ width:100%; height:100%; object-fit:cover; }
  @keyframes spinSlow{ to{ transform: rotate(360deg); } }

  .player{
    display:flex; align-items:center; justify-content:center; gap:16px;
    margin-top: 10px;
  }
  .play-btn{
    width:64px; height:64px; border-radius:50%;
    background: linear-gradient(135deg, var(--rose-deep), var(--rose));
    color:#fff; font-size:24px;
    display:flex; align-items:center; justify-content:center;
    border:none; cursor:pointer;
    box-shadow: 0 14px 26px -10px rgba(196,83,107,.6);
  }
  .bars{ display:flex; gap:4px; align-items:flex-end; height:28px; }
  .bars span{
    width:4px; background: var(--rose-deep); border-radius:2px; height:6px;
    animation: barBounce 1s ease-in-out infinite;
    opacity:.4;
  }
  .bars.playing span{ opacity:1; }
  .bars span:nth-child(1){ animation-delay:0s;}
  .bars span:nth-child(2){ animation-delay:.15s;}
  .bars span:nth-child(3){ animation-delay:.3s;}
  .bars span:nth-child(4){ animation-delay:.45s;}
  @keyframes barBounce{
    0%,100%{ height:6px; }
    50%{ height:26px; }
  }
  .song-title{ font-family:'Baloo Thambi 2', sans-serif; font-size:19px; margin-top:18px; color:var(--plum); }
  .song-sub{ font-size:14px; color:#9c6779; margin-top:4px; }

  /* ---------- poem ---------- */
  .poem-box{
    text-align:center;
    font-family:'Baloo Thambi 2', sans-serif;
    font-size: clamp(16px,4.3vw,18px);
    line-height:2.05;
    color: var(--plum);
  }
  .poem-line{
    opacity:0;
    transform: translateY(10px);
    transition: opacity .8s ease, transform .8s ease;
    margin-bottom: 2px;
  }
  .poem-line.show{ opacity:1; transform:translateY(0); }
  .poem-line.gap{ height:14px; }
  .poem-sign{ margin-top:22px; color: var(--rose-deep); font-weight:600;}

  /* ---------- final ---------- */
  .collage{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap:8px;
    max-width:360px;
    margin: 0 auto 26px;
  }
  .collage img{
    width:100%; height:100%; aspect-ratio:1/1; object-fit:cover;
    border-radius:12px;
    box-shadow: 0 8px 16px -8px rgba(84,41,63,.4);
  }
  .collage div:nth-child(1){ grid-column: span 2; grid-row: span 2; }
  .collage div:nth-child(1) img{ aspect-ratio: auto; height:100%; }

  .final-words{
    font-family:'Baloo Thambi 2', sans-serif;
    font-size: clamp(19px,5vw,23px);
    line-height:1.7;
    color: var(--plum);
    margin-bottom:16px;
  }
  .final-signoff{
    font-size:17px; color: var(--rose-deep); font-weight:700;
  }

  /* nav */
  .next-wrap{ margin-top:30px; }

  /* mute toggle */
  #muteBtn{
    position:fixed; top:16px; right:16px; z-index:50;
    width:44px; height:44px; border-radius:50%;
    background:rgba(255,255,255,.85);
    border:1px solid var(--rose-soft);
    color: var(--rose-deep);
    font-size:18px;
    display:flex; align-items:center; justify-content:center;
    cursor:pointer;
    box-shadow: 0 6px 14px -6px rgba(84,41,63,.3);
  }

  /* confetti */
  #confettiLayer{
    position:fixed; inset:0; pointer-events:none; z-index:40;
  }
  .confetti-piece{
    position:absolute; top:-5%;
    width:8px; height:14px;
    animation: confettiFall linear forwards;
  }
  @keyframes confettiFall{
    to{ transform: translateY(105vh) rotate(540deg); opacity:.9; }
  }

  @media (prefers-reduced-motion: reduce){
    *{ animation-duration:.01ms !important; animation-iteration-count:1 !important; transition-duration:.01ms !important; }
  }
</style>
</head>
<body>

<div id="heartLayer"></div>
<div id="confettiLayer"></div>
<button id="muteBtn" aria-label="Mute music">🔊</button>

<!-- background music -->
<audio id="bgMusic" src="assets/audio/neeye-neeye.mp3" loop preload="auto"></audio>
<audio id="songMusic" src="assets/audio/thaai-kelavi.mp3" preload="auto"></audio>

<!-- ============ 1. WELCOME ============ -->
<section class="stage active" id="stage-welcome">
  <div class="card">
    <div class="locket">💗</div>
    <span class="eyebrow tamil">Amma...</span>
    <h1 class="title">Mom, I have a little surprise for you… <span class="heart-icon">❤️</span></h1>
    <p class="sub">Konjam neram edutha, konjo love kaatanum nu nenachen. Ready aa? 🥺</p>
    <button class="btn pulse" onclick="goTo('stage-questions'); startBgMusic();">Start ✨</button>
  </div>
</section>

<!-- ============ 2. QUESTIONS ============ -->
<section class="stage" id="stage-questions">
  <div class="card">
    <div class="progress-dots" id="qDots"></div>
    <div id="qContainer"></div>
  </div>
</section>

<!-- transition after questions -->
<section class="stage" id="stage-transition">
  <div class="card">
    <span class="q-icon">💝</span>
    <p class="transition-msg tamil">You answered all my questions…<br>but your real surprise is still waiting! 💝</p>
    <div class="next-wrap">
      <button class="btn" onclick="goTo('stage-gift')">Continue ➡️</button>
    </div>
  </div>
</section>

<!-- ============ 3. GIFT BOX ============ -->
<section class="stage" id="stage-gift">
  <div class="card">
    <span class="eyebrow">Amma, this is for you</span>
    <h1 class="title tamil">Mom, this gift is specially for you… 🎀</h1>
    <div class="gift-wrap" id="giftWrap">
      <div class="burst" id="giftBurst"></div>
      <div class="gift-lid"></div>
      <div class="gift-box"></div>
    </div>
    <button class="btn pulse" id="openGiftBtn" onclick="openGift()">Open Your Gift 🎁</button>
  </div>
</section>

<!-- ============ 4. PHOTOS ============ -->
<section class="stage" id="stage-photos">
  <div class="card">
    <span class="eyebrow">Namma nyabagangal</span>
    <h1 class="title" style="margin-bottom:22px;">Beautiful memories with you ❤️</h1>
    <div class="slideshow" id="slideshow"></div>
    <div class="slide-dots" id="slideDots"></div>
    <div class="next-wrap">
      <button class="btn" onclick="goToSong()">Continue ➡️</button>
    </div>
  </div>
</section>

<!-- ============ 5. SONG ============ -->
<section class="stage" id="stage-song">
  <div class="card">
    <p class="sub tamil" style="margin-bottom:22px;">Now, listen to this song… because it reminds me of you. ❤️🎶</p>
    <div class="song-art" id="songArt">
      <img src="assets/img/photo6.jpg" alt="Amma">
    </div>
    <div class="song-title tamil">Thaai Kelavi</div>
    <div class="song-sub">Thiruchitrambalam</div>
    <div class="player">
      <button class="play-btn" id="songPlayBtn" onclick="toggleSong()">▶</button>
      <div class="bars" id="songBars"><span></span><span></span><span></span><span></span></div>
    </div>
    <div class="next-wrap">
      <button class="btn ghost" onclick="goToPoem()">Continue ➡️</button>
    </div>
  </div>
</section>

<!-- ============ 6. POEM ============ -->
<section class="stage" id="stage-poem">
  <div class="card">
    <h1 class="title tamil" style="margin-bottom:26px;">🌷 என் அம்மாவுக்கு… 🌷</h1>
    <div class="poem-box" id="poemBox"></div>
    <div class="next-wrap">
      <button class="btn" id="poemNextBtn" onclick="goTo('stage-final')" style="display:none;">Continue ➡️</button>
    </div>
  </div>
</section>

<!-- ============ 7. FINAL ============ -->
<section class="stage" id="stage-final">
  <div class="card">
    <p class="final-words tamil">Mom, I may not say it every day,<br>but you mean more to me<br>than words can explain.</p>
    <div class="collage" id="collage"></div>
    <p class="final-words" style="margin-top:6px;">Thank you for everything.</p>
    <p class="final-signoff">I love you, Mom. ❤️🥹</p>
  </div>
</section>

<script>
/* ================= DATA ================= */
const PHOTOS = [
  { src:'assets/img/photo4.jpg', cap:'Where it all began ❤️' },
  { src:'assets/img/photo1.jpg', cap:'So young, so full of love 💕' },
  { src:'assets/img/photo5.jpg', cap:'Your little girl, always ❤️' },
  { src:'assets/img/photo2.jpg', cap:'Watching me grow up 🥹' },
  { src:'assets/img/photo3.jpg', cap:'Us, always together 💗' },
  { src:'assets/img/photo6.jpg', cap:'My favourite person 🥹' },
  { src:'assets/img/photo7.jpg', cap:'Beautiful memories with you ❤️' },
  { src:'assets/img/photo8.jpg', cap:'Amma & Appa, my world 💞' },
];

const QUESTIONS = [
  {
    icon:'🎁',
    text:'Naan unakku oru special gift vachirukken nu sonna nambuveengala? 👀🎁',
    options:[{label:'YES', val:'yes'},{label:'NO', val:'no'}]
  },
  {
    icon:'🥹',
    text:'Amma, naan unakku romba pidicha ponna? 🥹❤️',
    options:[{label:'YES', val:'yes'},{label:'NO', val:'no'}]
  },
  {
    icon:'💝',
    text:'Amma, indha ulagathula enakku kidaicha biggest blessing nee dhaane? 🥹❤️',
    options:[{label:'YES 🥺', val:'yes'},{label:'YESSSS! 😭❤️', val:'yesss'}],
    final:true
  }
];

const POEM_LINES = [
"அன்புக்கு ஒரு உருவம் இருந்தால்,",
"அது என் அம்முவின் முகம் தான்…",
"",
"நான் உலகத்தை அறியும் முன்பே,",
"என்னை உலகமாக நினைத்தவள் நீ…",
"",
"நான் பேசத் தெரியாத வயதிலேயே",
"என் மௌனத்தையும் புரிந்தவள் நீ…",
"",
"என் சிரிப்புக்குப் பின்னால் இருக்கும் சந்தோஷத்தையும்,",
"என் அமைதிக்குள் மறைந்திருக்கும் கவலையையும் உணர்ந்தவள் நீ…",
"",
"எனக்கு உயிரை மட்டும் தரவில்லை அம்மு,",
"வாழ்க்கையை எப்படி வாழ வேண்டும் என்பதையும்",
"உன் அன்பால் கற்றுக் கொடுத்தாய்.",
"",
"நான் எத்தனை முறை விழுந்தாலும்,",
"என்னைத் தூக்க ஒரு கை இருந்தது… அது உன் கை.",
"",
"நான் எவ்வளவு தூரம் சென்றாலும்,",
"என்னை காத்திருக்கும் ஒரு வீடு இருந்தது… அது உன் இதயம்.",
"",
"சில நேரங்களில் “நன்றி” என்று சொல்ல மறந்திருக்கலாம்…",
"“நான் உன்னை நேசிக்கிறேன்” என்று தினமும் சொல்லாமல் இருக்கலாம்…",
"",
"ஆனால் அம்மா, என் ஒவ்வொரு கனவிலும்,",
"என் ஒவ்வொரு வெற்றியிலும், என் ஒவ்வொரு சிரிப்பிலும்",
"உன் அன்பின் ஒரு சிறு பகுதி இருக்கிறது.",
"",
"நீ என் அம்மா மட்டுமல்ல…",
"என் முதல் நண்பி, என் முதல் ஆசிரியர்,",
"என் நிம்மதி, என் பாதுகாப்பு,",
"என் வாழ்நாளின் மிக அழகான வரம்.",
"",
"இந்த வாழ்க்கை முடிந்து மீண்டும் ஒரு வாழ்க்கை கிடைத்தாலும்…",
"அந்த வாழ்க்கையிலும் நான் உன் குழந்தையாகவே பிறக்க வேண்டும். ❤️",
];

/* ================= STAGE NAV ================= */
function goTo(id){
  document.querySelectorAll('.stage').forEach(s=>s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  window.scrollTo({top:0, behavior:'smooth'});
}

/* ================= BACKGROUND HEARTS ================= */
(function initHearts(){
  const layer = document.getElementById('heartLayer');
  const emojis = ['💗','💕','💓','❤️','💖'];
  for(let i=0;i<