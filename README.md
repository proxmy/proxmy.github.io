# Ramiro Estrella Pernetti
**IT Systems Technician**
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<link rel="stylesheet" href="assets/css/styles.css">

<script>
  function setTheme(themeName) {
    localStorage.setItem('theme', themeName);
    document.documentElement.setAttribute('data-theme', themeName);
    updateButtonIcon();
  }

  function toggleTheme() {
    if (localStorage.getItem('theme') === 'dark') {
      setTheme('light');
    } else {
      setTheme('dark');
    }
    updateButtonIcon();
  }

  function updateButtonIcon() {
    const theme = localStorage.getItem('theme');
    const button = document.getElementById('themeToggleButton');
    if (theme === 'dark') {
      button.innerHTML = '<i class="fas fa-sun"></i>';
    } else {
      button.innerHTML = '<i class="fas fa-moon"></i>';
    }
  }

  document.addEventListener('DOMContentLoaded', function () {
    if (localStorage.getItem('theme') === 'dark') {
      setTheme('dark');
    } else {
      setTheme('light');
    }
    updateButtonIcon();
  });
</script>

<button id="themeToggleButton" onclick="toggleTheme()" style="margin-bottom: 20px; padding: 5px 10px; font-size: 16px;">
  <i class="fas fa-moon"></i>
</button>

<div style="display: flex; flex-direction: column; align-items: center; max-width: 1200px; margin: auto;">
  <!-- Barra lateral izquierda -->
  <div style="flex: 1; margin-bottom: 20px; text-align: center;">
    <img src="assets/me.jpeg" alt="Foto de Perfil" style="width: 150px; border-radius: 50%; margin-bottom: 20px;">

    <h3>Contacto</h3>
    <div class="social-links" style="margin-bottom: 20px;">
      <a href="https://www.linkedin.com/in/ramiropernetti/" class="fab fa-linkedin"></a>
      <a href="mailto:tomasestrellaramiro@gmail.com" class="fas fa-envelope"></a>
    </div>
  </div>

  <!-- Blog con acceso directo -->
  <div style="width: 100%; text-align: center; margin-bottom: 40px;">
    <h2><a href="#blog">Blog</a></h2>
  </div>

  <!-- Contenido principal -->
  <div style="flex: 2; width: 100%;">
    <h3>Educación</h3>
    <ul>
      <li>Grado en Ingeniería Telemática, Universidad Abierta de Cataluña (2024 - Actual)</li>
      <li>Grado en Ingeniería Telemática, Universidad Politécnica Alcalá de Henares (2023 - No finalizado)</li>
      <li>Técnico superior en telecomunicaciones y sistemas informáticos, CIFP Ferrolterra (2019 - 2021)</li>
    </ul>

    <h3>Experiencia Laboral</h3>
    <h4>Técnico en operaciones de sistemas informáticos en la DGSYFYP</h4>
    <p><em>Septiembre 2023 - Actual</em></p>
    <ul>
      <li>Monitorización de infraestructura</li>
      <li>Documentación detallada de procedimientos y configuraciones</li>
      <li>Maquetación de equipos</li>
      <li>Gestión de usuarios M365</li>
      <li>Participación en proyecto de migración de M365 junto con servidor Exchange</li>
      <li>Gestión de ticketing mediante software propietario</li>
      <li>Participación en proyectos de implantación del ENS CCN-CERT</li>
    </ul>

    <h4>Técnico de instalación y mantenimiento de telecomunicaciones</h4>
    <p><em>Junio 2022 - Septiembre 2022</em></p>
    <ul>
      <li>Instalación y mantenimiento de equipos de telecomunicaciones</li>
      <li>Gestión de redes estructuradas</li>
      <li>Maquetación de equipos</li>
      <li>Gestión usuarios M365</li>
      <li>Virtualización de equipos con VMWare</li>
      <li>Gestión de ticketing mediante software propietario</li>
    </ul>

    <h3>Certificaciones</h3>
    <ul>
      <li><a href="https://learn.microsoft.com/api/credentials/share/es-es/RamiroTomasEstrellaPernetti-6834/CB26E0CCBAA26064?sharingId">Microsoft 365 Certified: Fundamentals</a></li>
      <li><a href="https://learn.microsoft.com/api/credentials/share/es-es/RamiroTomasEstrellaPernetti-6834/66DFD3245BC67BE9?sharingId">Microsoft Certified: Azure Fundamentals</a></li>
      <li><a href="https://www.credly.com/badges/d071d42f-62a6-4be2-acc5-af5090ec9914/linked_in_profile">ITIL 4 ® Foundation</a></li>
      <li><a href="https://www.credly.com/badges/27bf2bd1-137e-4977-87f6-3f74c846bdc9/linked_in_profile">AWS Certified Cloud Practitioner</a></li>
    </ul>

    <h3 id="blog">Blog</h3>
    <ul>
      {% for post in site.posts %}
        <li>
          <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
          <p><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
          <p>{{ post.excerpt }}</p>
        </li>
      {% endfor %}
    </ul>
  </div>
</div>

body {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

header, main, footer {
  margin-bottom: 20px;
}

@media (min-width: 768px) {
  body {
    padding: 40px;
  }
}

