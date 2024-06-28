<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ecoguerreros</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-image: url('agricultura_campo.jpg'); /* Asegúrate de tener esta imagen en tu carpeta */
            background-size: cover;
            margin: 0;
            padding: 0;
            color: #333;
            height: 100vh; /* Añadido para cubrir toda la altura de la pantalla */
            display: flex;
            justify-content: center; /* Centrado horizontal de todo el contenido */
            align-items: center; /* Centrado vertical de todo el contenido */
        }
        .container {
            width: 90%;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border: 1px solid #000;
            border-radius: 10px;
            text-align: center; /* Centrado del contenido dentro del contenedor */
        }
        .header {
            margin-bottom: 20px;
        }
        .menu {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 40px;
        }
        .menu a {
            text-decoration: none;
            color: #000;
            background-color: #ddd;
            padding: 10px 20px;
            border: 1px solid #000;
            border-radius: 5px;
            font-weight: bold;
        }
        .menu a:hover {
            background-color: #ccc;
        }
        .social-media {
            display: flex;
            justify-content: center; /* Alineación centrada */
            gap: 20px;
            margin-bottom: 20px; /* Reducido el espacio inferior */
        }
        .social-media .box {
            text-align: center;
            border: 1px solid #000;
            padding: 20px;
            width: 150px; /* Tamaño ajustado de los contenedores */
            height: 150px; /* Ajuste de altura para que sean cuadrados */
            background-color: rgba(255, 255, 255, 0.8); /* Fondo semi-transparente */
            display: flex;
            justify-content: center; /* Centrado horizontal */
            align-items: center; /* Centrado vertical */
        }
        .social-media .box img {
            width: 100px; /* Tamaño ajustado de las imágenes */
            height: auto;
            opacity: 0.7; /* Opacidad para hacerlas transparentes */
            transition: opacity 0.3s ease; /* Transición suave */
        }
        .social-media .box img:hover {
            opacity: 1; /* Opacidad completa al pasar el mouse */
        }
        section {
            margin-bottom: 40px;
            display: none; /* Ocultamos todas las secciones por defecto */
        }
        .description .box {
            text-align: center;
            border: 1px solid #000;
            padding: 20px;
            width: 30%;
            background-color: #fff;
            margin: 0 10px;
            display: inline-block;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // Función para mostrar la sección correspondiente al hacer clic en un enlace del menú
            const menuLinks = document.querySelectorAll('.menu a');
            menuLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1); // Obtener el ID del objetivo
                    const targetSection = document.getElementById(targetId);
                    
                    // Ocultar todas las secciones
                    const sections = document.querySelectorAll('section');
                    sections.forEach(section => {
                        section.style.display = 'none';
                    });

                    // Mostrar la sección correspondiente
                    targetSection.style.display = 'block';
                });
            });
        });
    </script>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Ecoguerreros</h1>
        </div>
        <div class="menu">
            <a href="#quienes-somos">¿Quiénes somos?</a>
            <a href="#contactos">Contactos</a>
            <a href="#oferta-de-productos">Oferta de productos</a>
        </div>
        <div class="social-media">
            <div class="box">
                <a href="https://www.tiktok.com" target="_blank">
                    <img src="tik_tok.jpg" alt="Tik Tok">
                </a>
            </div>
            <div class="box">
                <a href="https://www.instagram.com" target="_blank">
                    <img src="instagram.jpg" alt="Instagram">
                </a>
            </div>
            <div class="box">
                <a href="https://www.facebook.com" target="_blank">
                    <img src="facebook.png" alt="Facebook">
                </a>
            </div>
        </div>

        <!-- Secciones adicionales -->
        <section id="quienes-somos">
            <h2>¿Quiénes somos?</h2>
            <div class="description">
                <div class="box">
                    <h3>Misión</h3>
                </div>
                <div class="box">
                    <h3>Visión</h3>
                </div>
                <div class="box">
                    <h3>Objetivos</h3>
                </div>
            </div>
            <p>Información sobre Ecoguerreros...</p>
        </section>

        <section id="contactos">
            <h2>Contactos</h2>
            <p>Información de contacto...</p>
        </section>

        <section id="oferta-de-productos">
            <h2>Oferta de productos</h2>
            <p>Detalles de los productos...</p>
        </section>
    </div>
</body>
</html>
