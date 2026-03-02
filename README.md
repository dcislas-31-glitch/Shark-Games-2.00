<html lang="en">
<head>
<meta charset="UTF-8">
<title>Shark Games</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<h1>CREDITS TO https://onclu.github.io/easywaystolearn/</h1>
<script>
alert("Do Not Share")
</script>
<style>
body {
  min-height:200vh;
  background: linear-gradient(rgba(10,10,25,0.85), rgba(5,5,15,0.95)),
url('https://static.wixstatic.com/media/5ed219_8a6b736413a74792b04a8f14d267da20~mv2.jpg/v1/fill/w_800,h_555,al_c,q_85/5ed219_8a6b736413a74792b04a8f14d267da20~mv2.jpg') no-repeat center center fixed;
  background-size:cover;
  color:white;
  overflow-x:hidden;
  scroll-behavior:smooth;
}
button {
  padding:18px;
  font-size:18px;
  background: rgba(12, 60, 18, 0.07);
  color:white;
  border:1px solid rgba(255,255,255,0.2);
  border-radius:6px; /* square look */
  cursor:pointer;
  transition:0.3s ease;
  backdrop-filter: blur(6px);
}
button: hover {
  background: rgba(30, 0, 255, 0.15);
  transform: translateY(-4px);
}
#homeBtn {
  position:fixed;
  top:15px;
  left:15px;
  padding:6px 10px;
  font-size:13px;
  background:rgba(255,255,255,0.08);
  border:1px solid rgba(0, 0, 0, 0.2);
  border-radius:4px;
  color:#ccc;
  cursor:pointer;
  display:none;
  z-index:20;
  transition:0.3s;
}

#homeBtn:hover {
  background:rgba(255, 249, 249, 0.2);
  color:white;
}

</style>
</head>
<body>
 <button id="homeBtn" onclick="goHome()">home</button>
<div class="buttonContainer">
    <button onclick="openGame('playFrame')">Playtropolis</button>
    <button onclick="openGame('minecraftFrame')">Minecraft</button>
    <button onclick="openGame('infiniteFrame')">Infinite Craft</button>
    <button onclick="openGame('soundboardFrame')">Soundboard</button>
  <button onclick="opengame('territorialFrame')"Territorial</button>
  </div>
<iframe id="playFrame" src="https://www.playtropolis.com" allowfullscreen></iframe>
<iframe id="minecraftFrame" src="https://eaglercraftx.org/" allowfullscreen></iframe>
<embed id="infiniteFrame" src="https://infinite-craft.org/infinite-craft/" width="100%" height="100%" style="display:none;" allowfullscreen>
<iframe id="soundboardFrame" src="https://www.myinstants.com/en/index/us/" allowfullscreen></iframe>
<iframe id="territorialFrame" src="https://territorial.io/" allowfullscreen></iframe>

 
</body>

