<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Perspectiva: Opinión y noticias del fútbol desde otro ángulo." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    /* Variables de colores */
    :root{
      --card:#ffffff;
      --muted:#444;
      --text:#111;
      --accent:#009739; 
      --accent-hover:#f7c600;
      --tag:#002776;
    }

    /* Reset y tipografía */
    *{box-sizing:border-box;margin:0;padding:0;}
    body{
      font-family:'Poppins', system-ui, sans-serif;
      background: radial-gradient(circle at 20% 30%, rgba(247,198,0,0.5) 0%, transparent 50%),
                  radial-gradient(circle at 80% 20%, rgba(0,151,57,0.4) 0%, transparent 50%),
                  radial-gradient(circle at 30% 70%, rgba(60,190,241,0.4) 0%, transparent 50%),
                  radial-gradient(circle at 70% 80%, rgba(233,78,60,0.3) 0%, transparent 50%),
                  #f5f5f5;
      background-attachment: fixed;
      color: var(--text);
    }

    a{
      color:var(--accent);
      text-decoration:none;
      transition:color .2s ease;
    }
    a:hover{
      color:var(--accent-hover);
      text-decoration:underline;
    }

    /* Header */
    header{
      position:sticky;
      top:0;
      z-index:1000;
      background: rgba(255,255,255,0.85);
      backdrop-filter: saturate(120%) blur(10px);
      border-bottom:2px solid rgba(0,0,0,0.1);
    }
    .header-inner{
      max-width:1200px;
      margin:0 auto;
      padding:16px 20px;
      display:flex;
      align-items:center;
      gap:20px;
    }
    .logo{ font-size:24px;font-weight:800;color:var(--accent); }
    nav{
      display:flex;
      gap:16px;
      flex:1;
    }
    nav a{
      font-weight:600;
      color:var(--text);
      padding:8px 12px;
      border-radius:6px;
      transition:all .2s ease;
    }
    nav a:hover{
      background:var(--accent);
      color:#fff;
    }

    /* Hero */
    .hero{
      text-align:center;
      padding:80px 20px;
      background: rgba(255,255,255,0.8);
      border-radius:12px;
      margin:40px auto;
      max-width:1000px;
    }
    .hero h1{
      font-size:42px;
      color:var(--accent);
      margin-bottom:10px;
    }
    .hero p{ font-size:18px; margin-bottom:20px; }
    .hero-btn{
      background:var(--accent);
      color:#fff;
      padding:12px 24px;
      border-radius:8px;
      font-weight:600;
      transition:all .2s ease;
    }
    .hero-btn:hover{ background:var(--accent-hover); }

    /* Opinión destacada */
    .destacada{
      margin:40px auto;
      max-width:1000px;
    }
    .destacada h2{ margin-bottom:20px;color:var(--accent); }
    .destacada article{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:20px;
      background:rgba(255,255,255,0.9);
      border-radius:12px;
      overflow:hidden;
      box-shadow:0 6px 20px rgba(0,0,0,.15);
    }
    .destacada img{ width:100%; height:100%; object-fit:cover; }
    .destacada .content{ padding:20px; }
    @media(max-width:800px){ .destacada article{grid-template-columns:1fr;} }

    /* Categorías rápidas */
    .categorias{
      text-align:center;
      margin:40px auto;
      max-width:1000px;
    }
    .categorias h2{ margin-bottom:20px;color:var(--accent); }
    .cat-grid{
      display:flex;
      gap:16px;
      justify-content:center;
      flex-wrap:wrap;
    }
    .cat-btn{
      background:rgba(255,255,255,0.9);
      padding:12px 20px;
      border-radius:10px;
      box-shadow:0 4px 10px rgba(0,0,0,0.15);
      font-weight:600;
      transition:all .2s ease;
    }
    .cat-btn:hover{ background:var(--accent); color:#fff; }

    /* Layout principal */
    main{
      max-width:1200px;
      margin:24px auto;
      padding:0 16px;
      display:grid;
      grid-template-columns:3fr 1fr;
      gap:24px;
    }
    @media(max-width:900px){ main{ grid-template-columns:1fr; } }

    /* Tarjetas de noticias/opiniones */
    .grid{
      display:grid;
      grid-template-columns: repeat(2, 1fr);
      gap:20px;
    }
    @media(max-width:800px){ .grid{ grid-template-columns:1fr; } }

    article{
      background:rgba(255,255,255,0.9);
      border-radius:12px;
      border:1px solid rgba(0,0,0,.1);
      box-shadow:0 6px 20px rgba(0,0,0,.15);
      overflow:hidden;
      transition:transform .2s ease;
    }
    article:hover{transform:translateY(-4px)}
    .cover{width:100%;height:180px;object-fit:cover;}
    .content h2{ font-size:18px;margin-bottom:6px;color:var(--accent);line-height:1.3; }
    .meta{ font-size:14px;color:var(--muted);margin-bottom:10px; }
    .tag{ background:var(--tag);color:#fff;padding:2px 8px;border-radius:999px;font-size:12px;margin-left:8px; }
    .readmore{ display:inline-block;margin-top:8px;color:var(--accent); }

    /* Sidebar */
    aside{
      position:sticky;
      top:100px;
      background:rgba(255,255,255,0.85);
      border-radius:12px;
      padding:16px;
      box-shadow:0 4px 12px rgba(0,0,0,.15);
      height:fit-content;
    }
    aside h3{ margin-bottom:12px;color:var(--accent); }
    aside ul{ list-style:none;padding:0;margin:0; }
    aside li{ margin-bottom:10px; }

    /* Sobre mí */
    .sobre-mi{
      background:rgba(255,255,255,0.9);
      padding:30px;
      border-radius:12px;
      margin:40px auto;
      max-width:1000px;
      box-shadow:0 6px 20px rgba(0,0,0,0.15);
      text-align:center;
    }
    .sobre-mi img{
      width:120px;
      height:120px;
      object-fit:cover;
      border-radius:50%;
      margin-bottom:15px;
      border:3px solid var(--accent);
    }
    .sobre-mi h2{color:var(--accent);}
    .sobre-mi p{max-width:700px;margin:auto;}

    /* Contacto */
    .contacto{
      padding:40px 20px;
      background:rgba(255,255,255,0.9);
      border-radius:12px;
      margin:40px auto;
      max-width:1000px;
      box-shadow:0 6px 20px rgba(0,0,0,0.15);
    }
    .contacto h2{ color: var(--accent); margin-bottom:10px; text-align:center; }
    .contacto p{ text-align:center; margin-bottom:20px; }
    .contact-form{
      display:flex;
      flex-direction:column;
      gap:15px;
      max-width:700px;
      margin:0 auto;
    }
    .contact-form label{ font-weight:600; }
    .contact-form input,
    .contact-form textarea{
      padding:12px;
      border:1px solid #ccc;
      border-radius:8px;
      font-size:16px;
      font-family:inherit;
      background:#fff;
    }
    .contact-form button{
      background:var(--accent);
      color:#fff;
      border:none;
      padding:14px;
      font-size:16px;
      font-weight:600;
      border-radius:8px;
      cursor:pointer;
      transition:all .2s ease;
      width:fit-content;
      align-self:center;
    }
    .contact-form button:hover{ background:var(--accent-hover); }

    footer{
      margin:40px 0 20px;
      text-align:center;
      color:var(--muted);
    }

  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="header-inner">
      <div class="logo">⚽ Perspectiva</div>
      <nav>
        <a href="#inicio">Inicio</a>
        <a href="#opiniones">Opiniones</a>
        <a href="#internacional">Internacional</a>
        <a href="#colombiano">Colombiano</a>
        <a href="#sobre-mi">Sobre mí</a>
        <a href="#contacto">Contacto</a>
      </nav>
    </div>
  </header>

  <!-- Opinión destacada -->
  <section class="destacada">
    <article>
      <img src="https://cdn.pixabay.com/photo/2015/01/09/11/29/bleachers-594201_1280.jpg" alt="Disturbio en Gradas" />
      <div class="content">
        <div class="meta">20 de agosto de 2025 <span class="tag">Copa Sudamericana</span></div>
        <h3>🚨 Incidentes en el partido Independiente vs Universidad de Chile</h3>
        <p>El partido entre Independiente y Universidad de Chile prometía ser un duelo intenso de fútbol sudamericano… pero lo que ocurrió superó cualquier expectativa. Entre goles, emoción y tensión, las gradas se convirtieron en un escenario de caos que dejó a todos con la boca abierta. ¿Qué pasó realmente en ese enfrentamiento que terminó suspendido y con graves consecuencias?</p>
        <a href="#" class="readmore">Seguir leyendo →</a>
      </div>
    </article>
  </section>

  <!-- Contenido principal -->
  <main>
    <!-- Noticias/opiniones -->
    <section id="opiniones" class="grid">
      <!-- Aquí van todos tus artículos -->
<article>
  <img class="cover" src="https://cdn.pixabay.com/photo/2021/06/20/22/58/balls-6352271_1280.jpg" alt="Protesta" />
  <div class="content">
    <div class="meta">20 de agosto de 2025 <span class="tag">Liga BetPlay</span></div>
    <h2>🔵👟 “Comunidad se queda sin Zapatos Tras protesta en el Campin: Millonarios en Crisis”</h2>
    <p></p>
    <a href="#" class="readmore">Seguir leyendo →</a>
  </div>
</article>

   
    </section>

    <!-- Sidebar -->
    <aside>
      <h3>📰 Opiniones destacadas</h3>
      <ul>
        <li><a href="#">🚨 Incidentes en el partido Independiente vs Universidad de Chile</a></li>
        <li><a href="#">🔵👟 “Comunidad se queda sin Zapatos Tras protesta en el Campin: Millonarios en Crisis”</a></li>
        <li><a href="#"></a></li>
      </ul>
    </aside>
  </main>

  <!-- Sobre mí -->
  <section id="sobre-mi" class="sobre-mi">

    <img src="imagenes/Snapchat-1939099584.jpg" alt="Foto" />
    <h2>Sobre mí</h2>
    <p>👋 Hola, soy Jesus Rojas, un apasionado del fútbol y creador de Perspectiva. Desde joven, me ha fascinado analizar tácticas, seguir la actualidad de equipos y jugadores, y compartir opiniones fundamentadas sobre lo que sucede dentro y fuera de la cancha.

En este espacio encontrarás noticias, análisis y opiniones sobre fútbol colombiano e internacional. Mi objetivo es ofrecer un punto de vista claro, cercano y que genere conversación, porque creo que el fútbol se disfruta más cuando se comparte y se debate con respeto.</p>
    
  </section>

  <!-- Contacto -->
  <section id="contacto" class="contacto">
    <h2>📩 Contáctame</h2>
    <p>¿Tienes una opinión, sugerencia o quieres debatir de fútbol? Escríbeme aquí:</p>
    <form class="contact-form">
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" name="nombre" required placeholder="Tu nombre">
      <label for="correo">Correo electrónico:</label>
      <input type="email" id="correo" name="correo" required placeholder="tunombre@email.com">
      <label for="mensaje">Mensaje:</label>
      <textarea id="mensaje" name="mensaje" rows="5" required placeholder="Escribe tu mensaje aquí..."></textarea>
      <button type="submit">Enviar</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Perspectiva</p>
  </footer>

</body>
</html>
