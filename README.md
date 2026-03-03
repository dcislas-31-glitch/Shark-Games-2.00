<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Shark Games</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<script>
alert("Do Not Share");
</script>

<style>
body {
  margin:0;
  font-family: Arial, sans-serif;
  background: linear-gradient(rgba(10,10,25,0.85), rgba(5,5,15,0.95)),
  url('https://static.wixstatic.com/media/5ed219_8a6b736413a74792b04a8f14d267da20~mv2.jpg') 
  no-repeat center center fixed;
  background-size:cover;
  color:white;
  overflow:hidden;

  /* THIS centers everything */
  display:flex;
  flex-direction:column;
  justify-content:center;   /* vertical center */
  align-items:center;       /* horizontal center */
  height:100vh;
}

h1 {
  margin-bottom:40px;
  font-size:40px;
  text-align:center;
}

.buttonContainer {
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:20px;
  max-width:800px;
}

button {
  padding:18px 28px;
  font-size:18px;
  background: rgba(12, 60, 18, 0.07);
  color:white;
  border:1px solid rgba(255,255,255,0.2);
  border-radius:8px;
  cursor:pointer;
  transition:0.3s ease;
  backdrop-filter: blur(6px);
}

button:hover {
  background: rgba(30, 0, 255, 0.2);
  transform: translateY(-4px);
}

#homeBtn {
  position:fixed;
  top:15px;
  left:15px;
  padding:8px 14px;
  font-size:14px;
  background:rgba(255,255,255,0.08);
  border:1px solid rgba(0,0,0,0.2);
  border-radius:4px;
  color:#ccc;
  cursor:pointer;
  display:none;
  z-index:20;
}

#homeBtn:hover {
  background:rgba(255,255,255,0.2);
  color:white;
}

iframe {
  display:none;
  position:fixed;
  top:0;
  left:0;
  width:100vw;
  height:100vh;
  border:none;
  z-index:5;
  background:black;
}
</style>
</head>

<body>

<h1>Shark Games</h1>

<button id="homeBtn" onclick="goHome()">Home</button>

<div class="buttonContainer">
  <button onclick="openGame('playFrame')">Playtropolis</button>
  <button onclick="openGame('minecraftFrame')">Minecraft</button>
  <button onclick="openGame('infiniteFrame')">Infinite Craft</button>
  <button onclick="openGame('soundboardFrame')">Soundboard</button>

  <!-- Opens in new tab because it blocks iframes -->
  <button onclick="window.open('https://territorial.io/', '_blank')">
    Territorial
  </button>
</div>

<!-- Iframes -->
<iframe id="playFrame" src="https://www.playtropolis.com" allowfullscreen></iframe>
<iframe id="minecraftFrame" src="https://eaglercraftx.org/" allowfullscreen></iframe>
<iframe id="infiniteFrame" src="https://infinite-craft.org/infinite-craft/" allowfullscreen></iframe>
<iframe id="soundboardFrame" src="https://www.myinstants.com/en/index/us/" allowfullscreen></iframe>

<script>
function hideAll(){
  document.querySelectorAll("iframe").forEach(frame => {
    frame.style.display = "none";
  });
}

function openGame(id){
  hideAll();

  document.querySelector("h1").style.display = "none";
  document.querySelector(".buttonContainer").style.display = "none";

  document.getElementById(id).style.display = "block";
  document.getElementById("homeBtn").style.display = "block";

  document.body.style.display = "block";
  document.body.style.overflow = "hidden";
}

function goHome(){
  hideAll();

  document.querySelector("h1").style.display = "block";
  document.querySelector(".buttonContainer").style.display = "flex";

  document.getElementById("homeBtn").style.display = "none";

  document.body.style.display = "flex";
  document.body.style.flexDirection = "column";
  document.body.style.justifyContent = "center";
  document.body.style.alignItems = "center";
  document.body.style.height = "100vh";
  document.body.style.overflow = "hidden";
}
</script>

</body>
</html>
