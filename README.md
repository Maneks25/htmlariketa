<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Futbola</title>
    <style>
        body {background-color: #fcf4f4;font-family: Arial, sans-serif; color: #0d0010dd}
        nav a{font-weight:bold;color: rgb(5, 220, 5);}
        h1 { text-align: center; color: #4412e9; }
        h2 { font-size:20px; color: rgb(29, 111, 219);}
        .txikia {
        width: 150px;
        cursor: pointer;
        }
        .handia {
            width: 400px;
        }
        .contenedor-juego {
            width: 320px;
            height: 480px;
            border: 3px solid #333;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f3f3f3;
            margin: 0 auto;
        }
        /* Estilo del canvas */
        canvas {
            width: 100%;
            height: 100%;
        }
    </style>
    </style>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='main.css'>
    <script src='main.js'></script>
</head>
<h1> Futbola</h1>
   <h2>Zer da?</h2>
   <p>Hamaika jokalariz osatutako bi talderen arteko jokoa, eta bere helburua aurkariaren atean sartzea da, eskuekin edo besoekin ukitu ezin den baloi bat, bere atezainaren eremuan izan ezik.</p>
   <img src="./argazkia.jpg" alt="Irudi txikia" onclick="handitu(this)" class="txikia">

   <script>
       function handitu(irudia) {
           if (irudia.classList.contains("txikia")) {
               irudia.classList.remove("txikia");
               irudia.classList.add("handia");
           } else {
               irudia.classList.remove("handia");
               irudia.classList.add("txikia");
           }
       }
 </script>
 <br>
        <a href="Lehena.html"> Euskal taldeak</a>
        <a href="Bigarrena.html"> Garaipenak</a>
        <a href="Hirugarrena.html"> Euskal jokalariak</a>
    </nav>
<br>
<h1>Juego de Flappy Bird en un Cuadro</h1>

<!-- Contenedor del juego -->
<div class="contenedor-juego">
    <canvas id="flappyBirdCanvas"></canvas>
</div>

<!-- Script del juego -->
<script>
    const canvas = document.getElementById("flappyBirdCanvas");
    const ctx = canvas.getContext("2d");

    // Ajustes del tamaño del canvas
    canvas.width = 320;
    canvas.height = 480;

    // Aquí empieza el código básico de un juego de Flappy Bird. Esta es una plantilla básica
    // de cómo iniciar el juego. Reemplaza esto con el código completo del juego si lo tienes.

    let birdY = canvas.height / 2;
    let birdVelocity = 0;
    const gravity = 0.25;

    function drawBird() {
        ctx.fillStyle = "yellow";
        ctx.fillRect(50, birdY, 20, 20); // Representación del "pájaro"
    }

    function update() {
        birdVelocity += gravity;
        birdY += birdVelocity;

        // Limpiar el canvas
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Dibujar el "pájaro"
        drawBird();

        requestAnimationFrame(update);
    }

    // Empezar el juego
    update();

    // Añadir un evento para "saltar"
    window.addEventListener("keydown", (e) => {
        if (e.code === "Space") {  // Espacio para saltar
            birdVelocity = -5;
        }
    });
</script>


</body>
</html>
# htmlariketa
