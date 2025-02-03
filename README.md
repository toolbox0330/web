<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body {
            background: linear-gradient(to right, #1a1a1a, #333333);
            font-family: 'Playfair Display', serif;
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
            width: 300px;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 1rem;
            font-weight: 700;
            color: #ff6b6b;
        }

        .image-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 1rem;
        }

        .image-container img {
            width: 60%;
            max-width: 150px;
            border-radius: 10px;
            object-fit: cover;
            border: 3px solid #ff6b6b;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        label {
            font-size: 1.1rem;
            color: #ffffff;
        }

        input {
            padding: 0.5rem;
            font-size: 1rem;
            border: 1px solid #555;
            border-radius: 5px;
            background-color: rgba(255, 255, 255, 0.1);
            color: #ffffff;
            transition: border-color 0.3s;
        }

        input:focus {
            border-color: #ff6b6b;
            outline: none;
        }

        button {
            padding: 0.7rem;
            background-color: #ff6b6b;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #ff4c4c;
        }

        #message {
            margin-top: 1rem;
            color: #ff6b6b;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <div class="container">
        <h1>HOLA CARIÑO</h1>
        <div class="image-container">
            <img src="https://i.pinimg.com/736x/2f/d0/1c/2fd01c097abe2caf2a33f6ec273e758d.jpg" alt="Imagen reducida" />
        </div>
        <form id="loginForm">
            <label for="password">¿Quieres ser mi 14 de Febrero?:</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">continuar</button>
        </form>
        <p id="message"></p>
        
    </div>

    <script>
     

        document.getElementById("loginForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const password = document.getElementById("password").value.toLowerCase();
            const message = document.getElementById("message");

            if (password === "si") {
                message.style.color = "#4caf50";
                message.textContent = "¡Que emoción!";
            } else {
                message.style.color = "#ff6b6b";
                message.textContent = "Lol que mal.";
            }
        });
    </script>
</body>
</html>
