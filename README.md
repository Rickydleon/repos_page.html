<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Viaje de Momentos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        h1 {
            color: #333;
            margin-top: 50px;
        }
        p {
            width: 80%;
            margin: 0 auto;
            font-size: 18px;
            line-height: 1.6;
        }
        .question {
            font-size: 24px;
            color: #4a4a4a;
            margin-top: 30px;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            background-color: #333;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        .buttons button:hover {
            background-color: #555;
        }
    </style>
    <script>
        function showMemory1() {
            document.getElementById("initialText").style.display = "none";
            document.getElementById("memory1").style.display = "block";
        }

        function showMemory2() {
            document.getElementById("memory1").style.display = "none";
            document.getElementById("memory2").style.display = "block";
        }

        function showMemory3() {
            document.getElementById("memory2").style.display = "none";
            document.getElementById("memory3").style.display = "block";
        }

        function revealQuestion() {
            document.getElementById("memory3").style.display = "none";
            document.getElementById("questionText").style.display = "block";
        }

        function positiveResponse() {
            alert('¡Sabía que dirías que sí! 😊 Prometo hacerte feliz, a pesar de la distancia.');
        }

        function unsureResponse() {
            alert('No hay presión, pero estoy aquí, esperando que la respuesta sea la que quiero 😜');
        }

        function funnyResponse() {
            alert('Oh, parece que necesitas pensarlo... 🤔 ¡Tómate tu tiempo, aunque ya te extraño más!');
        }

        function friendZoneResponse() {
            alert('Ouch... eso duele 😅 Pero no me rindo tan fácil.');
        }

        function destinyResponse() {
            alert('Es como si el destino nos estuviera dando una segunda oportunidad. 🥰');
        }
    </script>
</head>
<body>
    <h1>Un Viaje de Momentos</h1>
    <p id="initialText">Te he preparado algo especial... toca el botón cuando estés lista para comenzar nuestro viaje.</p>
    
    <button onclick="showMemory1()" style="background-color: #4a90e2; color: white; padding: 10px 25px; border: none; font-size: 18px; border-radius: 5px; cursor: pointer; margin-top: 20px;">
        Comenzar el viaje
    </button>

    <div id="memory1" style="display: none;">
        <p class="question">📅 7 de noviembre</p>
        <p>Esa fue la fecha de nuestro primer beso. Ese momento fue increíble, y desde entonces, no dejo de pensar en ti. Tocaste algo en mí que nunca había sentido antes.</p>
        <button onclick="showMemory2()">Siguiente</button>
    </div>

    <div id="memory2" style="display: none;">
        <p class="question">📍 La Distancia</p>
        <p>Aunque estemos lejos ahora, siento que cada día nos acercamos más. Te extraño tanto que cada mensaje, cada llamada se siente como una pequeña reunión entre nosotros.</p>
        <button onclick="showMemory3()">Siguiente</button>
    </div>

    <div id="memory3" style="display: none;">
        <p class="question">⏳ Tiempo Incompleto</p>
        <p>No tuve tiempo de hacerte una pregunta importante cuando estábamos juntos, así que aquí estoy, a pesar de la distancia, queriendo hacerla ahora.</p>
        <button onclick="revealQuestion()">Hazme la pregunta</button>
    </div>

    <div id="questionText" style="display: none;">
        <p class="question">¿Quieres ser mi novia?</p>
        <div class="buttons">
            <button onclick="positiveResponse()">Sí, claro que sí</button>
            <button onclick="unsureResponse()">Tal vez...</button>
            <button onclick="funnyResponse()">Mmm... no estoy segura</button>
            <button onclick="friendZoneResponse()">Solo como amigos</button>
            <button onclick="destinyResponse()">Esto es cosa del destino ❤</button>
        </div>
    </div>
</body>
</html>
