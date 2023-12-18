<!DOCTYPE html>
<html>
<head>
    <title>Transmision</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
            color: #333;
        }
        .container {
            width: 80%;
            margin: auto;
            background-color: white;
            padding: 20px;
            box-shadow: 0px 0px 10px #888888;
            border-radius: 10px;
        }
        video {
            width: 100%;
            display: none; /* El video está oculto inicialmente */
            border-radius: 10px;
        }
        .match-info {
            margin-top: 20px;
        }
        button {
            background-color: #008CBA; /* Azul */
            border: none;
            color: white;
            padding: 15px 32px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 10px;
        }
        select {
            width: 100%;
            padding: 16px 20px;
            border: none;
            border-radius: 4px;
            background-color: #f1f1f1;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Transmision en Vivo</h1>
        <select id="match-select">
            <!-- Aquí se colocan las opciones de los partidos -->
            <option value="">Selecciona un partido</option>
        </select>
        <button id="play-button">Reproducir Partido</button>
        <video id="match-video" controls>
            <!-- El enlace al video se coloca aquí -->
        </video>
        <div class="match-info">
            <h2>Informacion del Partido</h2>
            <p>Equipo Local: <span id="local-team">Equipo Local</span></p>
            <p>Equipo Visitante: <span id="visitor-team">Equipo Visitante</span></p>
            <p>Fecha y Hora: <span id="date-time">Fecha y Hora</span></p>
            <p>Estadio: <span id="stadium">Estadio</span></p>
        </div>
    </div>
    <script>
        document.getElementById('play-button').addEventListener('click', function() {
            // Cuando se hace clic en el botón, se muestra el video y se comienza a reproducir
            var video = document.getElementById('match-video');
            video.style.display = 'block';
            video.src = document.getElementById('match-select').value; // Usa el valor seleccionado en la lista desplegable
            video.play();
        });
    </script>
</body>
</html>
