<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Flores animadas</title>

<style>

body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background: radial-gradient(#0a1a1f,#000);
    overflow:hidden;
    font-family: Arial;
}

/* texto */
.mensaje{
    position:absolute;
    bottom:60px;
    color:#ffd700;
    letter-spacing:3px;
    font-size:18px;
}

/* contenedor */
.jardin{
    display:flex;
    gap:80px;
}

/* tallo */
.flor{
    position:relative;
    width:10px;
    height:120px;
    background:linear-gradient(#0f0,#063);
    animation:mover 3s ease-in-out infinite;
}

/* centro */
.flor::before{
    content:"";
    position:absolute;
    top:-20px;
    left:-10px;
    width:30px;
    height:30px;
    background:#ffeb3b;
    border-radius:50%;
}

/* pétalos */
.flor::after{
    content:"";
    position:absolute;
    top:-30px;
    left:-20px;
    width:50px;
    height:50px;
    background:radial-gradient(circle,#ffd54f 40%,transparent 41%);
    border-radius:50%;
}

/* movimiento */
@keyframes mover{
    0%{ transform:rotate(-5deg);}
    50%{ transform:rotate(5deg);}
    100%{ transform:rotate(-5deg);}
}

</style>
</head>

<body>

<div class="jardin">

<div class="flor"></div>
<div class="flor" style="animation-delay:0.5s"></div>
<div class="flor" style="animation-delay:1s"></div>

</div>

<div class="mensaje">
UNA ROSA AMARILLA PARA ILUMINAR TU DÍA CON ALEGRÍA
</div>

</body>
</html>
