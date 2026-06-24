# tonatovalentina
misitioweb
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Primera Página con Chatbot</title>
    <style>
        /* Estilos básicos de la página */
        body { font-family: Arial, sans-serif; background-color: #f4f4f9; padding: 20px; }
        
        /* Contenedor del Chatbot flotante */
        .chatbot-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 300px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
            border: 1px solid #ccc;
            overflow: hidden;
        }
        .chatbot-header {
            background-color: #4A00E0;
            color: white;
            padding: 10px;
            font-weight: bold;
            text-align: center;
        }
        .chatbot-body {
            height: 200px;
            padding: 10px;
            overflow-y: auto;
            font-size: 14px;
            background-color: #f9f9f9;
        }
        .chatbot-input {
            display: flex;
            border-top: 1px solid #ccc;
        }
        .chatbot-input input {
            flex: 1;
            padding: 10px;
            border: none;
            outline: none;
        }
        .chatbot-input button {
            background-color: #4A00E0;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <h1>¡Hola mundo! Esta es mi página web</h1>
    <p>Proyecto listo para GitHub Pages.</p>

    <!-- AQUÍ EMPIEZA EL CHATBOT -->
    <div class="chatbot-container">
        <div class="chatbot-header">Asistente Virtual</div>
        <div class="chatbot-body" id="chatBody">
            <p><strong>Bot:</strong> ¡Hola! ¿En qué puedo ayudarte hoy?</p>
        </div>
        <div class="chatbot-input">
            <input type="text" id="userInput" placeholder="Escribe un mensaje...">
            <button onclick="enviarMensaje()">Enviar</button>
        </div>
    </div>

    <!-- Lógica simple para que el chat responda algo automáticamente -->
    <script>
        function enviarMensaje() {
            var input = document.getElementById("userInput");
            var body = document.getElementById("chatBody");
            
            if(input.value.trim() !== "") {
                // Mensaje del usuario
                body.innerHTML += "<p><strong>Tú:</strong> " + input.value + "</p>";
                
                // Respuesta automática simulada
                setTimeout(function() {
                    body.innerHTML += "<p><strong>Bot:</strong> ¡Entendido! Estoy procesando tu mensaje... 🤖</p>";
                    body.scrollTop = body.scrollHeight; // Auto-scroll hacia abajo
                }, 1000);
                
                input.value = ""; // Limpiar cuadro de texto
                body.scrollTop = body.scrollHeight;
            }
        }
    </script>

</body>
</html>
