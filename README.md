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
  overflow-x:hidden;
}

h1 {
  text-align:center;
  margin-top:20px;
}

.buttonContainer {
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:15px;
  margin-top:40px;
}

button {
  padding:18px;
  font-size:18px;
  background: rgba(12, 60, 18, 0.07);
  color:white;
  border:1px solid rgba(255,255,255,0.2);
  border-radius:6px;
  cursor:pointer;
  transition:0.3s ease;
  backdrop-filter: blur(6px);
}

button:hover {
  background: rgba(30, 0, 255, 0.15);
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

  <!-- Territorial opens directly -->
  <button onclick="window.location.href='https://territorial.io/'">
    Territorial
  </button>
</div>

<iframe id="playFrame" src="https://www.playtropolis.com" allowfullscreen></iframe>
<iframe id="minecraftFrame" src="https://eaglercraftx.org/" allowfullscreen></iframe>
<iframe id="infiniteFrame" src="https://infinite-craft.org/infinite-craft/" allowfullscreen></iframe>
<iframe id="soundboardFrame" src="https://www.myinstants.com/en/index/us/" allowfullscreen></iframe>

<script>
function hideAll(){
  document.querySelectorAll("iframe").forEach(el => el.style.display="none");
}

function openGame(id){
  hideAll();

  document.querySelector("h1").style.display="none";
  document.querySelector(".buttonContainer").style.display="none";

  document.getElementById(id).style.display="block";
  document.getElementById("homeBtn").style.display="block";

  document.body.style.overflow="hidden";
}

function goHome(){
  hideAll();

  document.querySelector("h1").style.display="block";
  document.querySelector(".buttonContainer").style.display="flex";

  document.getElementById("homeBtn").style.display="none";

  document.body.style.overflow="auto";
}
</script>

</body>
</html>
