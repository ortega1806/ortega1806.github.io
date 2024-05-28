<!DOCTYPE html>
<html lang="es">
<head>
    <script>
        let language = 'en'; // Idioma predeterminado: español
    
        function search() {
            var query = document.getElementById("search-input").value;
            var searchResults = document.querySelector('.search-results');
    
            // Lógica de búsqueda simple
            if (query.toLowerCase().includes('enfermedades') && language === 'es') {
                searchResults.innerHTML += '<p class="bot-message">Aquí tienes información sobre enfermedades.</p>';
            } else if (query.toLowerCase().includes('medicamentos') && language === 'es') {
                searchResults.innerHTML += '<p class="bot-message">Aquí tienes información sobre medicamentos.</p>';
            } else if (query.toLowerCase().includes('diseases') && language === 'en') {
                searchResults.innerHTML += '<p class="bot-message">Here is information about diseases.</p>';
            } else if (query.toLowerCase().includes('medications') && language === 'en') {
                searchResults.innerHTML += '<p class="bot-message">Here is information about medications.</p>';
            } else {
                searchResults.innerHTML += '<p class="bot-message">Sorry, I did not find information about that.</p>';
            }
        }
    
        function changeLanguage() {
            language = document.getElementById("language-select").value;
            var searchResults = document.querySelector('.search-results');
            searchResults.innerHTML = ''; // Limpiar los resultados al cambiar de idioma
        }
        <div class="language-selector">
    <label for="language-select">Selecciona tu idioma:</label>
    <select id="language-select" onchange="changeLanguage()">
        <option value="en">English</option>
        <option value="es">Español</option>
    </select>
</div>
    </script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Procesamiento de Información Médica</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f8f9fa;
            color: #333;
            margin: 0;
            padding: 0;
        }

        .search-bar {
            background-color: #007bff;
            padding: 10px;
            text-align: center;
        }

        input[type="text"] {
            padding: 5px;
            margin-right: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }

        button {
            padding: 5px 10px;
            background-color: #fff;
            color: #007bff;
            border: 1px solid #007bff;
            border-radius: 3px;
            cursor: pointer;
        }

        button:hover {
            background-color: #007bff;
            color: #fff;
        }

        h1 {
            color: #007bff;
            text-align: center;
            margin-top: 20px;
        }

        p {
            font-size: 1.1em;
            line-height: 1.6;
            margin: 15px 0;
        }

        ul {
            list-style-type: disc;
            margin-left: 20px;
        }

        li {
            margin-bottom: 10px;
        }

        h2 {
            color: #333;
            margin-top: 20px;
        }

        h3 {
            color: #555;
        }

        .function-description {
            background-color: #f0f0f0;
            padding: 10px;
            border-radius: 5px;
            margin-bottom: 10px;
        }

        .chat-container {
            background-color: #f0f0f0;
            padding: 10px;
            border-radius: 5px;
            margin: 10px;
        }

        .user-message {
            background-color: #007bff;
            color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            margin: 5px;
            max-width: 70%;
        }

        .bot-message {
            background-color: #f0f0f0;
            padding: 5px 10px;
            border-radius: 5px;
            margin: 5px;
            max-width: 70%;
        }
    </style>
</head>
<body>
    <div class="search-bar">
        <input type="text" placeholder="Buscar..." id="search-input">
        <button onclick="buscar()">Buscar</button>
    </div>
    <h1>Procesamiento de Información Médica</h1>
    <h2>Funcionalidades</h2>
    <ul>
        <li class="function-description">Extracción de contenido: Extrae el texto plano de una página web específica.</li>
        <li class="function-description">Procesamiento de texto: Aplica técnicas de PLN para identificar entidades relevantes (enfermedades, medicamentos, procedimientos, etc.), relaciones entre entidades y generar resúmenes de texto.</li>
        <li class="function-description">Creación de base de datos: Crea una base de datos SQLite para almacenar la información extraída.</li>
        <li class="function-description">Almacenamiento de información: Almacena la información procesada (entidades, relaciones, resúmenes) en la base de datos.</li>
        <li class="function-description">Rastreo de sitio web: Rastreo un sitio web y extrae información de las páginas relevantes (en desarrollo).</li>
        <li class="function-description">chatbot:interacion con el usuario a traves de un chatbot</li>
    </ul>

    <script>
        function buscar() {
            var input = document.getElementById("search-input").value;
            // Implementar la funcionalidad de búsqueda aquí
            alert("Buscando por: " + input);
        }
    </script><BR>
          <p> <em> <strong>DAVID ORTEGA</strong> </EM></p>
</body>
</html>
