<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Perspectiva - Opinión y Noticias de Fútbol</title>
  <style>
    /* Paleta de colores estilo Mundial 2014 */
    :root {
      --accent: #1a8f5b;
      --accent-hover: #146c45;
      --background: #f2f2f2;
      --text: #222;
      --light-text: #666;
      --white: #fff;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--background);
      color: var(--text);
    }

    header {
      background: var(--accent);
      color: var(--white);
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header .logo {
      font-size: 20px;
      font-weight: bold;
    }

    nav a {
      color: var(--white);
      text-decoration: none;
      margin-left: 15px;
      font-weight: bold;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .destacada {
      padding: 30px;
      background: var(--white);
      margin: 20px auto;
      max-width: 900px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .destacada h2 {
      color: var(--accent);
    }

    .articulos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      max-width: 1000px;
      margin: 20px auto;
      padding: 0 20px;
    }

    .articulo {
      background: var(--white);
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .articulo h3 {
      margin-top: 0;
      color: var(--accent);
    }

    .articulo p {
      color: var(--light-text);
    }

    .sobre-mi {
      max-width: 900px;
      margin: 40px auto;
      background: var(--white);
      padding: 20px;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .sobre-mi img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      margin-bottom: 15px;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: var(--accent);
      color: var(--white);
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">⚽ Perspectiva</div>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#opiniones">Opiniones</a>
      <a href="#internacional">Internacional</a>
      <a href="#colombiano">Colombiano</a>
      <a href="#sobre-mi">Sobre mí</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <!-- Opinión destacada -->
  <section class="destacada" id="inicio">
    <h2>Opinión destacada</h2>
    <p>Bienvenidos a <b>Perspectiva</b>, un espacio donde comparto mi visión sobre lo que pasa en el mundo del fútbol. Aquí encontrarás análisis, opinión e información sobre lo que nos apasiona: el balompié.</p>
  </section>

  <!-- Artículos -->
  <section class="articulos" id="opiniones">
    <div class="articulo">
      <h3>Último partido de Champions</h3>
      <p>Un análisis rápido sobre el desempeño de los equipos y lo que nos dejó esta jornada emocionante.</p>
    </div>
    <div class="articulo">
      <h3>Opinión: El fútbol colombiano</h3>
      <p>Mi mirada sobre el nivel actual del fútbol en nuestro país y los retos que enfrenta.</p>
    </div>
    <div class="articulo">
      <h3>Jugador de la semana</h3>
      <p>Destacamos al futbolista que brilló y fue determinante en los resultados de su equipo.</p>
    </div>
  </section>

  <!-- Sobre mí -->
  <section class="sobre-mi" id="sobre-mi">
    <img src="tu-foto.jpg" alt="Mi foto">
    <h2>Sobre mí</h2>
    <p>Hola, soy el autor de <b>Perspectiva</b>. Me encanta el fútbol y compartir mis opiniones con quienes sienten la misma pasión. Este es mi espacio para expresarme y conectar con otros aficionados.</p>
  </section>

  <footer id="contacto">
    <p>&copy; 2025 Perspectiva | Opinión y Noticias de Fútbol</p>
  </footer>
</body>
</html>
