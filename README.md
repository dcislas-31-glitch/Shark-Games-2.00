<html lang="en">
<head>
<meta charset="UTF-8">
<title>Shark Games</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<script>
alert("Do Not Share");
</script>

<style>
* {
  box-sizing: border-box;
}

html, body {
  height: 100%;
  margin: 0;
}

body {
  font-family: Arial, sans-serif;
  background: linear-gradient(rgba(10,10,25,0.85), rgba(5,5,15,0.95)),
  url('https://static.wixstatic.com/media/5ed219_8a6b736413a74792b04a8f14d267da20~mv2.jpg') 
  no-repeat center center fixed;
  background-size: cover;
  color: white;

  display: flex;
  justify-content: center;  /* horizontal */
  align-items: center;      /* vertical */
}

.mainContent {
  text-align: center;
}

h1 {
  font-size: 42px;
  margin-bottom: 30px;
}

.buttonContainer {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

button {
  padding: 18px 28px;
  font-size: 18px;
  background: rgba(12, 60, 18, 0.07);
  color: white;
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: 8px;
  cursor: pointer;
  transition: 0.3s ease;
}

button:hover {
  background: rgba(30, 0, 255, 0.2);
  transform: translateY(-4px);
}

#homeBtn {
  position: fixed;
  top: 15px;
  left: 15px;
  padding: 8px 14px;
  font-size: 14px;
  display: none;
  z-index: 20;
}

iframe {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  border: none;
  z-index: 5;
  background: black;
}
</style>
</head>

<body>

<div class="mainContent">
  <h1>Shark Games</h1>

  <div class="buttonContainer">
    <button onclick="openGame('playFrame')">Playtropolis</button>
    <button onclick="openGame('minecraftFrame')">Minecraft</button>
    <button onclick="openGame('infiniteFrame')">Infinite Craft</button>
    <button onclick="openGame('soundboardFrame')">Soundboard</button>

    <button onclick="opengame('territorialFrame')">Territorial</button>
  </div>
</div>

<button id="homeBtn" onclick="goHome()">Home</button>

<iframe id="playFrame" src="https://www.playtropolis.com" allowfullscreen></iframe>
<iframe id="minecraftFrame" src="https://eaglercraftx.org/" allowfullscreen></iframe>
<iframe id="infiniteFrame" src="https://infinite-craft.org/infinite-craft/" allowfullscreen></iframe>
<iframe id="soundboardFrame" src="https://www.myinstants.com/en/index/us/" allowfullscreen></iframe>
<iframe id="territorialFrame" src="https://territorial.io/" allowfullscreen></iframe>

<script>
function hideAll(){
  document.querySelectorAll("iframe").forEach(frame => {
    frame.style.display = "none";
  });
}

function openGame(id){
  hideAll();

  document.querySelector(".mainContent").style.display = "none";
  document.getElementById(id).style.display = "block";
  document.getElementById("homeBtn").style.display = "block";

  document.body.style.display = "block";
  document.body.style.overflow = "hidden";
}

function goHome(){
  hideAll();

  document.querySelector(".mainContent").style.display = "block";
  document.getElementById("homeBtn").style.display = "none";

  document.body.style.display = "flex";
  document.body.style.justifyContent = "center";
  document.body.style.alignItems = "center";
  document.body.style.overflow = "auto";
}
</script>

</body>
</html>
