<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Te amo Gianela</title>
    <style>
        body {
            text-align: center;
            background-color: pink;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        h1 {
            color: red;
            font-size: 3em;
            margin-top: 50px;
        }
        .heart {
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: red;
            clip-path: polygon(50% 0%, 100% 33%, 83% 100%, 50% 67%, 17% 100%, 0% 33%);
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0% { transform: translateY(0); }
            50% { transform: translateY(-100px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <h1>Te amo Gianela, feliz día de la novia</h1>
    <div class="heart"></div>

    <audio autoplay loop>
        <source src="ruta-a-tu-cancion.mp3" type="audio/mpeg">
        Tu navegador no soporta la reproducción de audio.
    </audio>

    <script>
        const heart = document.querySelector('.heart');
        setInterval(() => {
            const newHeart = heart.cloneNode(true);
            document.body.appendChild(newHeart);
            newHeart.style.left = `${Math.random() * window.innerWidth}px`;
            newHeart.style.top = `${Math.random() * window.innerHeight}px`;
        }, 500);
    </script>
</body>
</html>
