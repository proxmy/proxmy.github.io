# Ramiro Estrella Pernetti

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<link rel="stylesheet" href="assets/css/styles.css">

<script>
  function setTheme(themeName) {
    localStorage.setItem('theme', themeName);
    document.documentElement.setAttribute('data-theme', themeName);
  }

  function toggleTheme() {
    if (localStorage.getItem('theme') === 'dark') {
      setTheme('light');
    } else {
      setTheme('dark');
    }
  }

  (function () {
    if (localStorage.getItem('theme') === 'dark') {
      setTheme('dark');
    } else {
      setTheme('light');
    }
  })();
</script>

<button onclick="toggleTheme()">Toggle Theme</button>

<div style="display: flex; align-items: flex-start;">
  <div style="flex: 1; margin-right: 20px;">
    <img src="assets/me.jpeg" alt="Foto de Perfil" style="width: 100%; max-width: 300px;">

    ## IT Systems Technician

    ### Contacto
    <div class="social-links">
      <a href="https://www.linkedin.com/in/ramiropernetti/" class="fab fa-linkedin"></a>
      <a href="mailto:tomasestrellaramiro@gmail.com" class="fas fa-envelope"></a>
    </div>
  </div>

  <div style="flex: 2;">
    ### Educación
    - Grado en Ingeniería Telemática, Universidad Abierta de Cataluña (2024 - Actual)
    - Grado en Ingeniería Telemática, Universidad Politécnica Alcalá de Henares (2023 - No finalizado)
    - Técnico superior en telecomunicaciones y sistemas informáticos, CIFP Ferrolterra (2019 - 2021)

    ### Experiencia Laboral
    **Técnico en operaciones de sistemas informáticos en la DGSYFYP**  
    _Septiembre 2023 - Actual_
    - Monitorización de infraestructura
    - Documentación detallada de procedimientos y configuraciones
    - Maquetación de equipos
    - Gestión de usuarios M365
    - Participación en proyecto de migración de M365 junto con servidor Exchange
    - Gestión de ticketing mediante software propietario
    - Participación en proyectos de implantación del ENS CCN-CERT

    **Técnico de instalación y mantenimiento de telecomunicaciones**  
    _Junio 2022 - Septiembre 2022_
    - Instalación y mantenimiento de equipos de telecomunicaciones
    - Gestión de redes estructuradas
    - Maquetación de equipos
    - Gestión usuarios M365
    - Virtualización de equipos con VMWare
    - Gestión de ticketing mediante software propietario

    ### Certificaciones
    - [Microsoft Certified: Azure Fundamentals](enlace)
    - [Microsoft 365 Certified: Fundamentals](enlace)
    - [ITIL 4 ® Foundation](enlace)
  </div>
</div>


