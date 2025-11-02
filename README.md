<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Portafolio - Nicolás Ignacio Maciel</title>

  <!-- Google Fonts + Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

  <style>
    /* === RESET === */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* === BODY === */
body {
  font-family: "Roboto", sans-serif;
  background: #f9f9f9;
  color: #333;
  line-height: 1.7;
  font-size: 17px; /* un poco más grande */
}

/* === PAGE WRAPPER === */
.page {
  max-width: 1400px; /* más ancho */
  margin: 40px auto;
  background: #fff;
  border-radius: 20px;
  box-shadow: 0 0 20px rgba(0,0,0,0.1);
  padding: 40px 50px;
}

/* === HEADER === */
.header {
  text-align: center;
  margin-bottom: 60px;
}

.avatar-wrap {
  position: relative;
  display: inline-block;
  width: 180px;
  height: 180px;
  margin-bottom: 20px;
}

.avatar {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  object-fit: cover;
  z-index: 2;
  position: relative;
}

.avatar-ring-left,
.avatar-ring-right {
  position: absolute;
  width: 210px;
  height: 210px;
  border: 4px solid #ffc107;
  border-radius: 50%;
  top: -15px;
  z-index: 1;
}

.avatar-ring-left {
  left: -15px;
  border-color: #ff9800;
}

.avatar-ring-right {
  right: -15px;
  border-color: #ffb300;
}

.name {
  font-size: 32px;
  font-weight: 700;
  margin-bottom: 8px;
  color: #222;
  letter-spacing: 1px;
}

.meta {
  font-size: 16px;
  color: #666;
}

/* === GRID === */
.grid {
  display: grid;
  grid-template-columns: 1.1fr 1.2fr 1fr;
  gap: 60px; /* más separación entre columnas */
}

/* === SECTION TITLES === */
.section-title {
  font-size: 20px;
  font-weight: 700;
  color: #444;
  border-bottom: 2px solid #ffc107;
  padding-bottom: 6px;
  margin-bottom: 12px;
  letter-spacing: 0.5px;
}

/* === LEFT COLUMN === */
.left {
  padding-right: 20px;
}

.experience .year {
  font-weight: 700;
  color: #ff9800;
  display: block;
  margin-bottom: 4px;
}

.experience p {
  font-size: 15px;
  margin-bottom: 14px;
}

.languages img {
  width: 22px;
  vertical-align: middle;
  margin-right: 6px;
}

/* === CENTER COLUMN === */
.center {
  text-align: center;
}

.quote {
  font-size: 17px;
  color: #444;
  margin-bottom: 40px;
  font-style: italic;
  line-height: 1.8;
}

.open-quote,
.close-quote {
  font-size: 50px;
  color: #ffc107;
  vertical-align: middle;
}


/* === CENTRO: IMÁGENES PORTAFOLIO === */
.center-art {
  position: relative;
  width: 100%;
  max-width: 520px;
  height: 420px;            /* suficiente espacio total */
  margin: 40px auto 0;
  overflow: visible;
  display: block;
  z-index: 2;
}

.center-art img {
  position: absolute;
  object-fit: contain;
  transition: transform 0.25s ease, opacity 0.25s ease;
  opacity: 0.95;
  filter: drop-shadow(0 6px 12px rgba(0,0,0,0.35));
  will-change: transform;
}

/* auriculares */
.center-art img.audiculares {
  top: 90px;
  left: -10%;
  width: 105px;
  transform: rotate(-10deg);
}

/* celular */
.center-art img.celular {
  top: 90px;
  left: 80%;
  width: 105px;
  transform: rotate(8deg);
}

/* computadora (centro principal) */
.center-art img.computadora {
  top: 150px;
  left: 50%;
  width: 220px;
  transform: translateX(-50%);
  z-index: 3;
}

/* libro más apartado a la izquierda */
.center-art img.libro {
  top: 290px;
  left: -10%;
  width: 105px;
  transform: rotate(3deg);
  z-index: 2;
}

/* mouse más arriba y más a la derecha */
.center-art img.mouse {
  top: 270px;          /* subido */
  left: 80%;           /* más a la derecha */
  width: 105px;
  transform: rotate(-6deg);
  z-index: 3;
}

/* portafolio encima de la computadora */
.center-art img.portafolio {
  top: 20px;           /* más arriba, sobre la computadora */
  left: 50%;
  width: 105px;
  transform: translateX(-50%) rotate(-2deg);
  z-index: 4;          /* sobre todo */
}

/* hover sutil */
.center-art img:hover {
  transform: scale(1.06);
  opacity: 1;
}

/* versión móvil */
@media (max-width: 720px) {
  .center-art {
    max-width: 340px;
    height: 280px;
  }
  .center-art img.audiculares { top: 18px; left: 8%; width: 50px; }
  .center-art img.celular     { top: 18px; left: 74%; width: 44px; }
  .center-art img.computadora { top: 90px; width: 150px; }
  .center-art img.libro       { top: 180px; left: 2%; width: 55px; }
  .center-art img.mouse       { top: 140px; left: 80%; width: 50px; }
  .center-art img.portafolio  { top: 70px; left: 50%; width: 70px; }
}

/* Posiciones individuales */
.audiculares { top: 10%; left: 20%; }
.celular { top: 30%; right: 15%; }
.computadora { top: 45%; left: 38%; }
.libro { top: 20%; right: 35%; }
.mouse { top: 65%; left: 25%; }
.portafolio { top: 15%; left: 55%; }

.education-list {
  list-style: none;
  text-align: left;
  margin-top: 10px;
}

.education-list .year {
  color: #ff9800;
  font-weight: 600;
  display: block;
}

/* === RIGHT COLUMN === */
.right {
  padding-left: 20px;
}

.contact {
  list-style: none;
  margin-bottom: 20px;
}

.contact li {
  display: flex;
  align-items: center;
  margin-bottom: 8px;
}

.contact .material-icons {
  color: #ff9800;
  margin-right: 10px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: flex-start;
}

.skill {
  text-align: center;
  width: 90px;
}

.skill-label {
  display: block;
  margin-top: 6px;
  font-weight: 600;
  font-size: 15px;
}

/* Circle Styles */
.circle {
  width: 70px;
  height: 70px;
}

.circle-bg {
  fill: none;
  stroke: #eee;
  stroke-width: 3;
}

.circle-fill {
  fill: none;
  stroke: #ff9800;
  stroke-width: 3;
  stroke-linecap: round;
  animation: progress 1.5s ease-out forwards;
}

@keyframes progress {
  from {
    stroke-dasharray: 0 100;
  }
}

.hobbies {
  list-style: none;
  margin-top: 10px;
}

.hobbies li {
  display: flex;
  align-items: center;
  margin-bottom: 6px;
}

.hobbies .material-icons {
  color: #ff9800;
  margin-right: 8px;
}


/* === LÍNEAS DE CONEXIÓN ENTRE ÍCONOS === */
.center-art .lines {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none; /* No interfiere con los clics */
  z-index: 1;
}

.center-art .line {
  stroke: rgba(255, 255, 255, 0.6);
  stroke-width: 2.5;
  fill: none;
  stroke-linecap: round;
  stroke-dasharray: 6, 4; /* línea punteada sutil */
  transition: stroke 0.3s ease, stroke-width 0.3s ease;
}

/* Efecto de hover sobre cada ícono: resalta su línea */
.center-art img:hover ~ .lines .line {
  stroke: rgba(255, 255, 255, 0.3);
}
.center-art img.audiculares:hover ~ .lines .line-audiculares,
.center-art img.celular:hover ~ .lines .line-celular,
.center-art img.computadora:hover ~ .lines .line-computadora,
.center-art img.libro:hover ~ .lines .line-libro,
.center-art img.mouse:hover ~ .lines .line-mouse,
.center-art img.portafolio:hover ~ .lines .line-portafolio {
  stroke: #ffd700;
  stroke-width: 3.5;
  stroke-dasharray: none;
}

  </style>
</head>
<body>

    <!-- ONDA AMARILLA -->
  <div class="wave-top"></div>
<div class="menu">
  <div class="menu-left">
    <a href="#portafolio">Portafolio</a>
    <a href="#carta">Carta</a>
    <a href="#perfil-profesional">Perfil</a>
  </div>

  <div class="menu-center"></div> <!-- espacio para foto -->

  <div class="menu-right">
    <a href="#contacto">Contacto</a>
    <a href="#habilidades-tecnicas">Habilidades</a>
    <a href="#perfil-profesional">Experiencia</a>
  </div>
</div>


    <div class="background-fixed" style="z-index: -2 !important;">
    <img src="portafolio/fondo.png" alt="Fondo decorativo">
  </div>
  <div class="page">
    <!-- TOP: avatar + name -->
    <header class="header">
      <div class="avatar-wrap">
        <div class="avatar-ring-left"></div>
        <div class="avatar-ring-right"></div>
        <img class="avatar" src="portafolio/foto.png" alt="Retrato Nicolás Maciel">
      </div>

      <h1 id="#perfil-profesional" class="name">NICOLÁS IGNACIO MACIEL</h1>
      <p class="meta">26 años | DNI: 41952385 | Soltero | La Matanza, Buenos Aires, Argentina</p>
    </header>

    <!-- GRID 3 columnas -->
    <main class="grid">
      <!-- LEFT COLUMN -->
      <aside class="col left">
        <h2 id="perfil-profesional" class="section-title">PERFIL PROFESIONAL</h2>
        <p style="font-size:14px; line-height:1.6;">
          Soy estudiante de Ingeniería y cuento con más de seis años de experiencia profesional
          en puestos de analista de sistemas y datos. He complementado mi formación con diversos
          cursos especializados en programación y análisis de datos, lo que ha fortalecido mis
          competencias técnicas y analíticas. Mi experiencia laboral abarca las áreas de analítica
          funcional, análisis de datos, desarrollo web e informática.
        </p>


        <h2 class="section-title" id="experiencia-profesional" style="margin-top:24px;">EXPERIENCIA PROFESIONAL</h2>
        <ul class="experience">
          <li><span class="year">2019-2021</span>
            <p><strong>HDK SA</strong> – Analista de Sistemas y Soporte Administrativo.<br>
            Elaboración de planillas de Excel, desarrollo web interno, carga y gestión de datos, gestión de compras y soporte IT.</p>
          </li>

          <li><span class="year">2021-2023</span>
            <p><strong>Ke Insumos</strong> – Soporte Técnico / Analista de Datos.<br>
            Elaboración de planillas avanzadas, colaboración con consultoras IT, análisis de datos, desarrollo de informes y mantenimiento de bases SQL.</p>
          </li>

          <li><span class="year">2023-Actualidad</span>
            <p><strong>Ministerio de Seguridad - Policía de la Ciudad</strong><br>
            Analista en la Oficina de Transparencia y Control Externo.<br>
            Desarrollo de sitios internos, análisis de datos, automatización de tareas y soporte técnico.</p>
          </li>
        </ul>

        <h2 id="idiomas" style="margin-left:20px;" class="section-title">IDIOMAS</h2>
        <div  style="margin-left:20px;" class="languages">
          <img src="portafolio/ingles.png" alt="Inglés"> 
          <em>Inglés</em>
        </div>
      </aside>

      <!-- CENTER COLUMN -->
      <section class="col center">
        <blockquote class="quote">
          <span class="open-quote">“</span>
          <em >Busco integrarme a un equipo de trabajo donde pueda aplicar y ampliar mis conocimientos, contribuyendo al crecimiento de la organización con innovación, desarrollo y soluciones efectivas.</em>
          <span class="close-quote">”</span>
        </blockquote>
        <!-- CENTRO: IMÁGENES PORTAFOLIO -->
        <div class="center-art" style="margin-top:-10px;">
          <img src="portafolio/audiculares.png" alt="Audiculares" class="audiculares">
          <img src="portafolio/celular.png" alt="Celular" class="celular">
          <img src="portafolio/computadora.png" alt="Computadora" class="computadora">
          <img src="portafolio/libro.png" alt="Libro" class="libro">
          <img src="portafolio/mouse.png" alt="Mouse" class="mouse">
          <img src="portafolio/portafolio.png" alt="Portafolio" class="portafolio">
          <!-- Líneas de conexión -->




        </div>
        <br>

        <section class="education">
          <h2 id="educacion" class="section-title center-title">EDUCACIÓN</h2>
          <ul class="education-list">
            <li>
              <span class="year">Actual</span>
              <div style="margin-left: -100px;"><strong>Ingeniería Informática</strong><br>Universidad Nacional de La Matanza (UNLAM) – San Justo, Buenos Aires / Instituto Superior Santo Domingo (ISSD)</div>
            </li>
            <li><span class="year">Secundario</span>
              <div style="margin-left: -60px;"><strong>Bachiller en Ciencias Sociales</strong><br>Instituto José de San Martín – Virrey del Pino, La Matanza</div>
            </li>
          </ul>

       
         
            <div>
              <h2 id="cursos-certificaciones" class="section-title" style="margin-top:20px;">CURSOS Y CERTIFICACIONES</h2>
            <ul class="education-list">
              <li>
                
                Operador Informático T2 – C.F.P. N406 Felipe Vállese<br><br>
                Desarrollo Web – Instituto de Economía Internacional (Google)<br><br>
                Pensamiento Computacional y Programación - C.F.L N406 Oscar Andrada<br><br>
                Programación en Python – C.F.L. N406 Dr. Oscar Andrada<br><br>
                Programación de Sistemas Informáticos Multimediales – C.F.L. N406 Dr. Oscar Andrada<br><br>
                Base de Datos – ISC Instituto Superior de la Carrera<br><br>
                Excel – ISC Instituto Superior de la Carrera<br><br>
                Maquetación Web – ISC Instituto Superior de la Carrera<br><br>
                SAS® Visual Analytics & Programming – SAS Educación<br><br>
                SAS SQL : Essentials – SAS Educación
              </li>
            </ul>

            </div>

            </li>
          </ul>
        </section>
      </section>

      <!-- RIGHT COLUMN -->
      <aside class="col right" style="margin-left:30px;">
        <h2 id="contacto" class="section-title">CONTACTO</h2>
        <ul class="contact">
          <li>
            <a style="color: #ffff;" href="https://www.google.com/maps?q=La+Matanza,+Buenos+Aires,+Argentina" target="_blank" rel="noopener">
              <span class="material-icons">location_on</span>
              <span>La Matanza, Buenos Aires, Argentina</span>
            </a>
          </li>

          <li>
            <a style="color: #ffff;"  href="tel:+541133345330">
              <span class="material-icons">phone</span>
              <span>+54 11 3334 5330</span>
            </a>
          </li>

          <li>
            <a style="color: #ffff;"  href="mailto:nic.maciel.00.01.10@gmail.com">
              <span class="material-icons">email</span>
              <span>nic.maciel.00.01.10@gmail.com</span>
            </a>
          </li>
        </ul>


      <h2 id="habilidades-tecnicas" class="section-title">HABILIDADES TÉCNICAS</h2>
        <div class="skills">
          <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="70,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">Python</span>
          </div>

          <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="90,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">SQL</span>
          </div>

          <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="100,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">Excel / Sheets</span>
          </div>

                    <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="100,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">Microsoft Office</span>
          </div>

          <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="80,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">SAS</span>
          </div>

           <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="80,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">Tableau</span>
          </div>

          <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="80,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">Looker Studio</span>
          </div>

         <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="75,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">HTML / CSS / PHP / JAVASCRIPT</span>
          </div>

         <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="75,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">C#</span>
          </div>

            <div class="skill">
            <svg viewBox="0 0 36 36" class="circle">
              <path class="circle-bg" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
              <path class="circle-fill" stroke-dasharray="75,100" d="M18 2.0845
                a 15.9155 15.9155 0 0 1 0 31.831
                a 15.9155 15.9155 0 0 1 0 -31.831" />
            </svg>
            <span class="skill-label">SaS Programing</span>
          </div>


        </div>

        <h2 id="habilidades-blandas"  class="section-title" style="margin-top:24px;">HABILIDADES BLANDAS</h2>
        <ul class="hobbies">
          <li><span class="material-icons">psychology</span><span>Creatividad</span></li>
          <li><span class="material-icons">groups</span><span>Trabajo en equipo</span></li>
          <li><span class="material-icons">insights</span><span>Pensamiento analítico</span></li>
          <li><span class="material-icons">leaderboard</span><span>Liderazgo colaborativo</span></li>
        </ul>
      </aside>
    </main>
  </div>
<script>
  // Selecciono todos los enlaces del menú
  const menuLinks = document.querySelectorAll('.menu a');
  const sections = document.querySelectorAll('h2.section-title, h1.name'); // secciones a marcar

  menuLinks.forEach(link => {
    link.addEventListener("click", e => {
      e.preventDefault();
      const target = document.querySelector(link.getAttribute("href"));
      if (!target) return;

      // Altura del menú sticky
      const menuHeight = document.querySelector('.menu').offsetHeight + 200; // un pequeño margen extra

      // Posición final: arriba del todo, dejando espacio para el menú
      const targetPosition = target.offsetTop - menuHeight;

      window.scrollTo({
        top: targetPosition,
        behavior: "smooth"
      });

      // Opcional: marcar sección activa
      menuLinks.forEach(l => l.classList.remove("active"));
      link.classList.add("active");
    });
  });



 </script>

</body>

</html>
