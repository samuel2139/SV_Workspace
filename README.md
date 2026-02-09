<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ask A Manager – Salary Analytics 2021</title>

  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background-color: #fffdf4;
      color: #2c2c2c;
      line-height: 1.6;
    }

    header {
      background-color: #f4c430; /* Amarillo principal */
      padding: 35px 50px;
      color: #1f1f1f;
    }

    header h1 {
      margin: 0;
      font-size: 34px;
    }

    header p {
      margin-top: 10px;
      font-size: 16px;
    }

    section {
      max-width: 1200px;
      margin: auto;
      padding: 40px 50px;
    }

    h2 {
      color: #b58900;
      border-bottom: 3px solid #f4c430;
      padding-bottom: 6px;
      margin-top: 50px;
    }

    ul {
      margin-left: 20px;
    }

    iframe {
      width: 100%;
      height: 800px;
      border: none;
      margin-top: 25px;
    }

    footer {
      background-color: #f4c430;
      text-align: center;
      padding: 20px;
      font-size: 14px;
      margin-top: 60px;
    }
  </style>
</head>

<body>

<header>
  <h1>Ask A Manager – Salary Analytics 2021</h1>
  <p>
    <strong>Fuente:</strong> Ask A Manager Salary Survey 2021<br>
    <strong>Herramienta:</strong> Looker Studio
  </p>
</header>

<section>

  <h2>📊 Descripción del proyecto</h2>
  <p>
    Este sitio documenta el análisis salarial basado en la encuesta
    <strong>Ask A Manager Salary Survey 2021</strong>. El proyecto incluye
    procesos de limpieza de datos, modelado, normalización geográfica,
    conversión de monedas y visualizaciones analíticas.
  </p>

  <p>
    El objetivo principal es analizar la relación entre industria,
    experiencia profesional y compensación total anual, expresando
    todos los valores monetarios en <strong>pesos colombianos (COP)</strong>
    para garantizar comparabilidad entre países y sectores económicos.
  </p>

  <h2>📈 Dashboard interactivo</h2>
  <p>
    El dashboard fue desarrollado en <strong>Looker Studio</strong> y se
    encuentra conectado al modelo de datos previamente construido y
    transformado.
  </p>

  <p>
    A través de este tablero interactivo es posible explorar:
  </p>

  <ul>
    <li>Salario promedio anual por industria</li>
    <li>Compensación total anual en pesos colombianos (COP)</li>
    <li>Relación entre salario, nivel educativo y años de experiencia</li>
    <li>Comparaciones salariales mediante filtros por país, industria y variables demográficas</li>
  </ul>

  <p><strong>👉 Dashboard embebido:</strong></p>

  <!-- PEGA AQUÍ EL IFRAME DE LOOKER STUDIO --> <iframe width="600" height="450" src="https://lookerstudio.google.com/embed/reporting/64d26999-8da1-4997-953f-3b274fae0b56/page/Wc7mF" frameborder="0" style="border:0" allowfullscreen sandbox="allow-storage-access-by-user-activation allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox"></iframe>
  <iframe 
    src="https://lookerstudio.google.com/reporting/64d26999-8da1-4997-953f-3b274fae0b56"
    allowfullscreen>
  </iframe>

</section>

<footer>
  Proyecto de Analytics – Documentación y Dashboard Integrado | Looker Studio
</footer>

</body>
</html>
