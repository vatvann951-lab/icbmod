<!DOCTYPE html>
<html lang="km">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ICB MOD - Store</title>
  <style>
    :root {
      --cyan: #00ffff;
      --bg1: #001f3f;
      --bg2: #000428;
      --green: #00ff6a;
      --telegram-blue: #33bdf8;
    }
    body {
      margin: 0;
      font-family: "Khmer OS Battambang", sans-serif;
      background: radial-gradient(circle at top, var(--bg1), var(--bg2));
      color: #fff;
      text-align: center;
      padding: 25px 12px;
    }
    h1 {
      color: var(--cyan);
      text-shadow: 0 0 15px var(--cyan);
      font-size: 28px;
    }
    .container {
      background: rgba(255,255,255,0.06);
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 0 15px rgba(0,255,255,0.3);
      margin-bottom: 20px;
    }
    input[type="datetime-local"] {
      padding: 8px;
      border-radius: 8px;
      border: none;
      margin: 10px 0;
      text-align: center;
    }
    .calc-btn {
      padding: 10px 25px;
      border-radius: 10px;
      border: none;
      background: var(--cyan);
      color: #000;
      font-weight: bold;
      box-shadow: 0 0 10px var(--cyan);
    }
    .panel {
      width: 160px;
      height: 80px;
      background: #000;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(255,255,255,0.15);
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
      font-weight: bold;
      text-shadow: 0 0 10px #fff;
      margin: 0 auto;
    }
    .section { margin-top: 20px; }
    .section-text {
      margin-top: 8px;
      color: #ccc;
      text-shadow: 0 0 8px #ccc;
      font-weight: bold;
    }
    .buy-btn {
      padding: 8px 30px;
      border-radius: 10px;
      border: none;
      cursor: pointer;
      font-weight: bold;
      margin-top: 8px;
      background: var(--green);
      color: #000;
      box-shadow: 0 0 15px var(--green);
    }

    /* Floating social bar */
    .social-bar {
      position: fixed;
      top: 35%;
      left: 10px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      z-index: 999;
    }
    .social-bar a {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #fff;
      box-shadow: 0 0 10px rgba(255,255,255,0.2);
      transition: 0.2s;
    }
    .social-bar a:hover { transform: scale(1.1); }
    .social-bar img { width: 25px; height: 25px; border-radius: 50%; }
  </style>
</head>
<body>

<!-- Floating social bar -->
<div class="social-bar">
  <a href="https://www.tiktok.com/@riki72y" target="_blank" style="background:#000;">
    <img src="https://upload.wikimedia.org/wikipedia/en/a/a9/TikTok_logo.svg" alt="TikTok">
  </a>
  <a href="https://facebook.com/" target="_blank" style="background:#1773ea;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Facebook_Logo.png" alt="Facebook">
  </a>
  <a href="https://www.youtube.com/@CIB-q8x" target="_blank" style="background:#ff0000;">
    <img src="E1EA9586-1EA6-4EA1-8A56-88375EB8F629.jpeg" alt="YouTube">
  </a>
  <a href="https://t.me/vanndavt" target="_blank" style="background:#33bdf8;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram">
  </a>
</div>

<h1> ICB MOD - Store </h1>

<div class="container">
  <label>បញ្ចូលថ្ងៃ និងម៉ោងចាប់ផ្តើម:</label><br>
  <input id="startTime" type="datetime-local"><br>
  <button class="calc-btn" onclick="calculate()">គណនា</button>
  <div id="resultBox" style="margin-top:10px; display:none; color:#00ffff; font-weight:bold;"></div>
</div>

<!-- Store Sections -->
<div class="section"><div class="panel">GTA<br>San Andreas</div><div class="section-text">Apple ID GTA SA</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">Minecraft</div><div class="section-text">Apple ID Minecraft</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">E-Sign</div><div class="section-text">App E-Sign</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">MOD Free Fire</div><div class="section-text">Free Fire Hack Mod</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">MOD Mobile Legend</div><div class="section-text">Mobile Legend Hack Mod</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">MOD 8Ball Pool</div><div class="section-text">Pool Hack Account</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">MOD PUBG</div><div class="section-text">PUBG Mobile Mod</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">Apple ID Shadowrocket</div><div class="section-text">iOS VPN App Access</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>
<div class="section"><div class="panel">Acc Telegram KH</div><div class="section-text">Telegram Account Access</div><a href="https://t.me/vanndavt"><button class="buy-btn">Buy</button></a></div>

<script>
function calculate(){
  const input=document.getElementById("startTime").value;
  const box=document.getElementById("resultBox");
  if(!input){box.style.display="block";box.innerHTML="⚠️ សូមបញ្ចូលថ្ងៃ និងម៉ោងមុន!";return;}
  const start=new Date(input);
  // 74 hours instead of 72
  const end=new Date(start.getTime()+74*60*60*1000);
  const days=["អាទិត្យ","ចន្ទ","អង្គារ","ពុធ","ព្រហស្បតិ៍","សុក្រ","សៅរ៍"];
  const months=["មករា","កម្ភៈ","មិនា","មេសា","ឧសភា","មិថុនា","កក្កដា","សីហា","កញ្ញា","តុលា","វិច្ឆិកា","ធ្នូ"];
  const d=days[end.getDay()];
  const m=months[end.getMonth()];
  const day=end.getDate();
  const y=end.getFullYear();
  let h=end.getHours();
  const min=String(end.getMinutes()).padStart(2,"0");
  const p=h>=12?"រសៀល":"ព្រឹក";
  if(h>12)h-=12; if(h===0)h=12;
  box.innerHTML=`${d} ទី ${day} ${m} ${y} ម៉ោង ${h}:${min} នាទី ${p}`;
  box.style.display="block";
}
</script>

</body>
</html>
