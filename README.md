<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JonhPage - Tu Página Web</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <nav class="navbar">
        <div class="logo">
            <i class="fas fa-code"></i>
            <span>JonhPage</span>
        </div>
        <ul class="nav-links">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#sobre-mi">Sobre mí</a></li>
            <li><a href="#proyectos">Proyectos</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>

    <section id="inicio" class="hero">
        <div class="hero-content">
            <h1>Bienvenido a mi página web</h1>
            <p>Soy Jonh y aquí comparto mis proyectos y conocimientos</p>
            <a href="#proyectos" class="cta-button">Ver Proyectos</a>
        </div>
    </section>

    <section id="sobre-mi" class="about">
        <h2>Sobre mí</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Desarrollador web apasionado por crear experiencias digitales únicas</p>
                <p>Me encanta aprender y compartir conocimiento</p>
            </div>
            <div class="skills">
                <h3>Habilidades</h3>
                <div class="skill-tags">
                    <span>HTML</span>
                    <span>CSS</span>
                    <span>JavaScript</span>
                    <span>Python</span>
                </div>
            </div>
        </div>
    </section>

    <section id="proyectos" class="projects">
        <h2>Mis Proyectos</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Proyecto 1</h3>
                <p>Descripción del proyecto 1</p>
                <a href="#" class="project-link">Ver más</a>
            </div>
            <div class="project-card">
                <h3>Proyecto 2</h3>
                <p>Descripción del proyecto 2</p>
                <a href="#" class="project-link">Ver más</a>
            </div>
        </div>
    </section>

    <section id="contacto" class="contact">
        <h2>Contacto</h2>
        <div class="contact-content">
            <form id="contact-form">
                <input type="text" placeholder="Nombre" required>
                <input type="email" placeholder="Email" required>
                <textarea placeholder="Mensaje" required></textarea>
                <button type="submit" class="submit-button">Enviar</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
        </div>
        <p>&copy; 2025 JonhPage. Todos los derechos reservados.</p>
    </footer>

    <script>
        // Animación de scroll
        document.addEventListener('DOMContentLoaded', () => {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-links a');

            window.addEventListener('scroll', () => {
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    if (scrollY >= sectionTop - 60) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href').slice(1) === current) {
                        link.classList.add('active');
                    }
                });
            });
        });

        // Manejo del formulario de contacto
        document.getElementById('contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('¡Gracias por tu mensaje! Te responderé pronto.');
            e.target.reset();
        });
    </script>
    </main>

    <footer>
        <p>&copy; 2025 Mi Página Web</p>
    </footer>

    <script>
        // Función para cambiar el color del título
        function cambiarColor() {
            const titulo = document.getElementById('titulo');
            const colores = ['red', 'blue', 'green', 'purple'];
            const randomColor = colores[Math.floor(Math.random() * colores.length)];
            titulo.style.color = randomColor;
        }

        // Función para incrementar el contador
        let count = 0;
        function incrementar() {
            count++;
            document.getElementById('contador').textContent = count;
        }

        // Función para saludar
        function saludar() {
            const nombre = document.getElementById('nombre').value;
            const saludoElement = document.getElementById('saludo');
            if (nombre) {
                saludoElement.textContent = `¡Hola, ${nombre}!`;
            } else {
                saludoElement.textContent = 'Por favor, ingresa tu nombre';
            }
        }
    </script>
</body>
</html>
