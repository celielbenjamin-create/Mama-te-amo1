<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sorpresa para mamá</title>

<style>

body{
margin:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:black;
font-family:Arial;
text-align:center;
color:white;
overflow:hidden;
}

#inicio{
text-align:center;
}

#contenido{
display:none;
background:linear-gradient(135deg,#ff7eb3,#ff758c);
position:absolute;
top:0;
left:0;
width:100%;
height:100%;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
}

button{
padding:15px 30px;
font-size:20px;
border:none;
border-radius:10px;
background:#ff4d6d;
color:white;
}

img{
width:220px;
border-radius:20px;
margin-bottom:20px;
box-shadow:0 10px 20px rgba(0,0,0,0.3);
}

h1{
font-size:40px;
animation:latido 1s infinite;
}

@keyframes latido{
0%{transform:scale(1);}
50%{transform:scale(1.1);}
100%{transform:scale(1);}
}

.corazon{
position:absolute;
top:-10px;
font-size:22px;
animation:caer linear infinite;
}

@keyframes caer{
0%{transform:translateY(-10px);}
100%{transform:translateY(100vh);}
}

</style>
</head>

<body>

<div id="inicio">
<h2>Tengo una sorpresa para ti</h2>
<button onclick="abrir()">Abrir sorpresa</button>
</div>

<div id="contenido">

<img src=20251231_132210.jpg>

<h1>Te amo mamá ❤️</h1>

<p>Gracias por todo lo que haces por mí</p>

<audio id="musica" src="cancion.mp3"></audio>

</div>

<script>

function abrir(){

document.getElementById("inicio").style.display="none";
document.getElementById("contenido").style.display="flex";

document.getElementById("musica").play();

}

function crearCorazon(){
const corazon=document.createElement("div");

corazon.classList.add("corazon");
corazon.innerHTML="❤️";

corazon.style.left=Math.random()*100+"vw";
corazon.style.animationDuration=(3+Math.random()*3)+"s";

document.body.appendChild(corazon);

setTimeout(()=>{
corazon.remove();
},6000);
}

setInterval(crearCorazon,300);

</script>

</body>
</html>
