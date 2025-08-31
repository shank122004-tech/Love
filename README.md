<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Fun Hub – Professional AI Tools</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;background:#0f0f2f;color:#fff;overflow-x:hidden;
background: linear-gradient(-45deg, #0f0f2f, #1c1c3c, #0f0f2f, #1c1c3c); background-size:400% 400%; animation:gradientBG 15s ease infinite;}
@keyframes gradientBG{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%;}}
header{padding:20px;text-align:center;z-index:2;position:relative;}
header h1{font-size:2.8em;color:#ff4b5c;text-shadow:0 0 20px #ff4b5c,0 0 40px #ff416c;}
header p{margin-top:10px;color:#ccc;font-size:1.2em;}
.nav-tabs{display:flex;justify-content:center;gap:10px;margin:20px 0;flex-wrap:wrap;position:relative;z-index:2;}
.nav-tabs button{padding:12px 20px;border:none;border-radius:20px;cursor:pointer;font-weight:600;transition:0.3s;box-shadow:0 5px 20px rgba(0,0,0,0.3);background: linear-gradient(45deg,#24c6dc,#514a9d);color:#fff;}
.nav-tabs button.active{background:linear-gradient(45deg,#ff416c,#ff4b2b);box-shadow:0 0 20px #ff416c,0 0 40px #ff4b2b;}
.tool-section{text-align:center;z-index:2;position:relative;margin-top:20px;}
input{padding:14px;margin:8px;border-radius:20px;border:none;outline:none;width:220px;max-width:80%;font-size:1em;background:rgba(255,255,255,0.1);color:#fff;box-shadow:0 0 10px rgba(255,255,255,0.1);}
input::placeholder{color:rgba(255,255,255,0.6);}
.card{width:90%;max-width:500px;margin:30px auto;padding:30px;border-radius:25px;color:white;font-size:1.2em;display:none;position:relative;overflow:hidden;backdrop-filter: blur(15px);border:1px solid rgba(255,255,255,0.2);box-shadow:0 10px 40px rgba(0,0,0,0.5);transition:0.3s all;z-index:2;}
.card h2{font-size:2.2em;margin-bottom:10px;text-shadow:0 0 10px #fff;}
.card p{font-size:1.1em;margin:5px 0;}
.card::before{content:'';position:absolute;top:-50%;left:-50%;width:200%;height:200%;background: radial-gradient(circle, rgba(255,255,255,0.05), transparent 70%); animation:rotateGlow 8s linear infinite;pointer-events:none;}
@keyframes rotateGlow{0%{transform:rotate(0deg)}100%{transform:rotate(360deg)}}
.style1{background: linear-gradient(135deg,#ff416c,#ff4b2b);}
.style2{background: linear-gradient(135deg,#24c6dc,#514a9d);}
.style3{background: linear-gradient(135deg,#f7971e,#ffd200); color:#333;}
.style4{background: linear-gradient(135deg,#f953c6,#b91d73);}
.style5{background: linear-gradient(135deg,#11998e,#38ef7d);}
button.predict,button.style{cursor:pointer;border:none;border-radius:20px;padding:12px 25px;font-weight:bold;transition:0.3s;box-shadow:0 0 15px rgba(255,255,255,0.2);}
button.predict{background: linear-gradient(45deg,#ff416c,#ff4b2b); color:#fff;}
button.style{background: linear-gradient(45deg,#24c6dc,#514a9d); color:#fff;}
button:hover{transform:translateY(-3px) scale(1.05);box-shadow:0 0 25px rgba(255,255,255,0.4);}
.share-btns{margin-top:20px;display:none;}
.share-btns button{padding:12px 20px;margin:5px;border-radius:20px;font-weight:bold;border:none;cursor:pointer;box-shadow:0 5px 20px rgba(0,0,0,0.3);}
button.whatsapp{background:#25D366;color:#fff;}
button.facebook{background:#4267B2;color:#fff;}
button.download{background:#ff9800;color:#222;}
footer{text-align:center;padding:30px 10px;font-size:0.9em;color:#aaa;position:relative;z-index:2;}
@media(max-width:500px){input{width:150px;} .nav-tabs button{padding:8px 14px;font-size:0.9em;}}
#neuralCanvas{position:absolute;top:0;left:0;width:100%;height:100%;z-index:0;pointer-events:none;}
.confetti-piece,.heart-piece,.love-object{position:absolute;pointer-events:none;z-index:10;}
.confetti-piece{width:10px;height:10px;}
.heart-piece{font-size:22px;animation-name:floatHeart;animation-timing-function: linear;}
.love-object{animation-name:floatLove;animation-timing-function: linear;}
@keyframes floatHeart{0%{transform:translateY(0) scale(1);opacity:1}100%{transform:translateY(-300px) scale(0.5);opacity:0}}
@keyframes floatLove{0%{transform:translateY(0) scale(1);opacity:1}100%{transform:translateY(-120vh) scale(0.5);opacity:0}}
#floatingShare{position:fixed;bottom:30px;left:20px;display:flex;flex-direction:column;gap:10px;z-index:999;}
#floatingShare button{padding:12px 18px;border:none;border-radius:20px;font-weight:bold;cursor:pointer;box-shadow:0 5px 20px rgba(0,0,0,0.3);}
#floatingShare button.whatsapp{background:#25D366;color:#fff;}
#floatingShare button.facebook{background:#4267B2;color:#fff;}
#floatingShare button.download{background:#ff9800;color:#222;}
#floatingAd { position:fixed;top:50%;right:0;transform:translateY(-50%);z-index:999; transition: transform 0.5s ease; }
#floatingAd:hover { transform: translateY(-52%) scale(1.05); }
#floatingLoveObjects{position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:1;}
</style>
</head>
<body>

<header>
<h1>🤖 AI Fun Hub 🤖</h1>
<p>Try Crush Predictor, Compliment Generator, Fortune Teller & AI Quotes. Share your AI cards instantly!</p>

<!-- Top Banner Ad -->
<div style="text-align:center;margin:10px 0;">
  <ins class="adsbygoogle"
       style="display:block"
       data-ad-client="ca-pub-XXXXXXXXXXXXXX"
       data-ad-slot="1111111111"
       data-ad-format="auto"
       data-full-width-responsive="true"></ins>
</div>
</header>

<div class="nav-tabs">
<button class="active" onclick="showTool('crush')">Crush Predictor ❤️</button>
<button onclick="showTool('compliment')">Compliment Generator 💬</button>
<button onclick="showTool('fortune')">Fortune Teller 🔮</button>
<button onclick="showTool('quote')">Quote Generator ✨</button>
</div>

<!-- Middle Ad -->
<div style="text-align:center;margin:20px 0;">
  <ins class="adsbygoogle"
       style="display:block"
       data-ad-client="ca-pub-XXXXXXXXXXXXXX"
       data-ad-slot="2222222222"
       data-ad-format="auto"
       data-full-width-responsive="true"></ins>
</div>

<section id="crush-tool" class="tool-section">
<input type="text" id="yourName" placeholder="Your Name">
<input type="text" id="crushName" placeholder="Crush's Name"><br>
<button class="predict" onclick="predictLove()">Predict ❤️</button>
<button class="style" onclick="changeStyle()">Change Style 🎨</button>
</section>

<section id="compliment-tool" class="tool-section" style="display:none;">
<button class="predict" onclick="generateCompliment()">Generate Compliment 💬</button>
</section>

<section id="fortune-tool" class="tool-section" style="display:none;">
<button class="predict" onclick="generateFortune()">Reveal Fortune 🔮</button>
</section>

<section id="quote-tool" class="tool-section" style="display:none;">
<button class="predict" onclick="generateQuote()">Get Quote ✨</button>
</section>

<div id="resultCard" class="card style1">
<canvas id="neuralCanvas"></canvas>
</div>

<div class="share-btns" id="shareBtns">
<button class="whatsapp" onclick="shareWhatsApp()">WhatsApp 📲</button>
<button class="facebook" onclick="shareFacebook()">Facebook</button>
<button class="download" onclick="downloadCard()">Download Story Card 📸</button>
</div>

<!-- Bottom Banner Ad -->
<div style="text-align:center;margin:20px 0;">
  <ins class="adsbygoogle"
       style="display:block"
       data-ad-client="ca-pub-XXXXXXXXXXXXXX"
       data-ad-slot="3333333333"
       data-ad-format="auto"
       data-full-width-responsive="true"></ins>
</div>

<footer>Made with ❤️ using AI & JavaScript • Share & have fun!</footer>

<!-- Floating Right Ad -->
<div id="floatingAd">
  <ins class="adsbygoogle"
       style="display:block;width:120px;height:600px;"
       data-ad-client="ca-pub-XXXXXXXXXXXXXX"
       data-ad-slot="4444444444"></ins>
</div>

<!-- Floating Quick Share Panel -->
<div id="floatingShare">
<button class="whatsapp" onclick="shareWhatsApp()">WhatsApp 📲</button>
<button class="facebook" onclick="shareFacebook()">Facebook</button>
<button class="download" onclick="downloadCard()">Download 📸</button>
</div>

<!-- Floating Love Objects -->
<div id="floatingLoveObjects"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});

// --- All JS functions (predictLove, generateCompliment, generateFortune, generateQuote, shareWhatsApp, shareFacebook, downloadCard, animations) ---

let currentStyle=1;
function showTool(tool){
  const sections=document.querySelectorAll('.tool-section');
  sections.forEach(s=>s.style.display='none');
  document.getElementById(tool+'-tool').style.display='block';
  document.querySelectorAll('.nav-tabs button').forEach(btn=>btn.classList.remove('active'));
  event.currentTarget.classList.add('active');
  document.getElementById("resultCard").style.display='none';
  document.getElementById("shareBtns").style.display='none';
}

// --- Predict / Generate Functions ---
function predictLove(){ const name1=document.getElementById("yourName").value.trim(); const name2=document.getElementById("crushName").value.trim(); if(!name1||!name2){alert("Please enter both names!"); return;} const score=Math.floor(Math.random()*51)+50; const messages=["🔥 A match made in heaven!","💖 You two are destined!","🌹 Love is in the air!","⚡ Sparks are flying!","😍 The perfect couple!"]; const msg=messages[Math.floor(Math.random()*messages.length)]; const card=document.getElementById("resultCard"); card.innerHTML=`<canvas id="neuralCanvas"></canvas><h2>${name1} ❤️ ${name2}</h2><p>Compatibility: <b>${score}%</b></p><p>${msg}</p>`; card.style.display='block';document.getElementById("shareBtns").style.display='block'; launchNeuralNetwork();launchConfetti();launchHearts(); launchEmojiRain();}
function changeStyle(){ currentStyle=currentStyle===5?1:currentStyle+1; document.getElementById("resultCard").className="card style"+currentStyle; document.getElementById("resultCard").innerHTML=`<canvas id="neuralCanvas"></canvas>`; launchNeuralNetwork(); }
function generateCompliment(){ const compliments=["You're a star 🌟","Your smile lights up the room 😊","You're unstoppable 💪","You're amazing just as you are 💖","You inspire everyone around you ✨"]; const card=document.getElementById("resultCard"); card.innerHTML=`<canvas id="neuralCanvas"></canvas><h2>💬 Compliment</h2><p>${compliments[Math.floor(Math.random()*compliments.length)]}</p>`; card.style.display='block'; document.getElementById("shareBtns").style.display='block'; launchNeuralNetwork(); launchConfetti(); launchHearts(); launchEmojiRain();}
function generateFortune(){ const fortunes=["Good luck is coming your way 🍀","A surprise encounter awaits 🔮","Today is perfect for new beginnings 🌅","You will make someone smile today 😄","Unexpected joy is near ✨"]; const card=document.getElementById("resultCard"); card.innerHTML=`<canvas id="neuralCanvas"></canvas><h2>🔮 Fortune</h2><p>${fortunes[Math.floor(Math.random()*fortunes.length)]}</p>`; card.style.display='block'; document.getElementById("shareBtns").style.display='block'; launchNeuralNetwork(); launchConfetti(); launchHearts(); launchEmojiRain();}
function generateQuote(){ const quotes=["Believe in yourself 💪","Dream big and act bigger 🌟","Kindness is your superpower 💖","Success is a journey, not a destination 🚀","AI + Fun = Innovation 🤖"]; const card=document.getElementById("resultCard"); card.innerHTML=`<canvas id="neuralCanvas"></canvas><h2>✨ Quote</h2><p>${quotes[Math.floor(Math.random()*quotes.length)]}</p>`; card.style.display='block'; document.getElementById("shareBtns").style.display='block'; launchNeuralNetwork(); launchConfetti(); launchHearts(); launchEmojiRain();}

// --- Share & Download ---
function shareWhatsApp(){ const text=document.getElementById("resultCard").innerText; const url=window.location.href; const message=encodeURIComponent(text+"\nCheck AI Fun Hub: "+url); window.open("https://wa.me/?text="+message,"_blank");}
function shareFacebook(){ const url=encodeURIComponent(window.location.href); window.open("https://www.facebook.com/sharer/sharer.php?u="+url,"_blank");}
function downloadCard(){ const card=document.getElementById("resultCard"); html2canvas(card,{width:1080,height:1920,scale:2}).then(canvas=>{const link=document.createElement("a");link.download="ai_fun_story.png";link.href=canvas.toDataURL();link.click();alert("✅ Story image saved!");});}

// --- Neural Network Animation ---
let neuralInterval;
function launchNeuralNetwork(){
  if(neuralInterval) clearInterval(neuralInterval);
  const canvas=document.getElementById("neuralCanvas");
  canvas.width=canvas.offsetWidth; canvas.height=canvas.offsetHeight;
  const ctx=canvas.getContext("2d");
  let nodes=[];
  for(let i=0;i<12;i++){nodes.push({x:Math.random()*canvas.width,y:Math.random()*canvas.height,vx:(Math.random()-0.5)*1.5,vy:(Math.random()-0.5)*1.5});}
  neuralInterval=setInterval(()=>{
    ctx.clearRect(0,0,canvas.width,canvas.height);
    for(let n of nodes){n.x+=n.vx;n.y+=n.vy;if(n.x<0||n.x>canvas.width)n.vx*=-1;if(n.y<0||n.y>canvas.height)n.vy*=-1;ctx.beginPath();ctx.arc(n.x,n.y,3,0,Math.PI*2);ctx.fillStyle="#fff";ctx.fill();}
    for(let i=0;i<nodes.length;i++){for(let j=i+1;j<nodes.length;j++){let dx=nodes[i].x-nodes[j].x;let dy=nodes[i].y-nodes[j].y;let dist=Math.sqrt(dx*dx+dy*dy);if(dist<150){ctx.beginPath();ctx.moveTo(nodes[i].x,nodes[i].y);ctx.lineTo(nodes[j].x,nodes[j].y);ctx.strokeStyle="rgba(255,255,255,0.2)";ctx.stroke();}}}
  },30);
}

// --- Confetti, Hearts, Emoji Rain ---
function launchConfetti(){for(let i=0;i<30;i++){let c=document.createElement("div");c.className="confetti-piece";c.style.left=Math.random()*window.innerWidth+"px";c.style.background=["#ff0","#f0f","#0ff","#0f0","#f00"][Math.floor(Math.random()*5)];c.style.top="-10px";document.body.appendChild(c);let anim=setInterval(()=>{c.style.top=(parseFloat(c.style.top)+Math.random()*5)+"px";if(parseFloat(c.style.top)>window.innerHeight){c.remove();clearInterval(anim);}},20);}}
function launchHearts(){for(let i=0;i<20;i++){let h=document.createElement("div");h.className="heart-piece";h.innerText="❤️";h.style.left=Math.random()*window.innerWidth+"px";document.body.appendChild(h);setTimeout(()=>h.remove(),4000);}}
function launchEmojiRain(){const emojis=["😍","🔥","💖","✨","🎉"];for(let i=0;i<25;i++){let e=document.createElement("div");e.className="heart-piece";e.style.left=Math.random()*window.innerWidth+"px";e.style.fontSize=(18+Math.random()*15)+"px";e.innerText=emojis[Math.floor(Math.random()*emojis.length)];document.body.appendChild(e);setTimeout(()=>e.remove(),4000);}}

// --- Floating Love Objects ---
function launchLoveObjects(){
  const container = document.getElementById("floatingLoveObjects");
  const symbols = ["❤️","💖","💘","🌹","💕","💞"];
  setInterval(()=>{
    const e = document.createElement("div");
    e.className = "love-object";
    e.innerText = symbols[Math.floor(Math.random()*symbols.length)];
    e.style.left = Math.random()*window.innerWidth + "px";
    e.style.fontSize = (14+Math.random()*20) + "px";
    e.style.animationDuration = (4+Math.random()*4) + "s";
    container.appendChild(e);
    setTimeout(()=>e.remove(),8000);
  }, 400);
}
launchLoveObjects();

</script>
</body>
</html>
