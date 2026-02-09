<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documentación Dashboard - Ask A Manager 2021</title>
    <style>
        body {
            font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f4f4f9;
        }
        header {
            border-bottom: 2px solid #333;
            padding-bottom: 10px;
            margin-bottom: 30px;
        }
        h1, h2, h3 {
            background-color: #ffeb3b; /* Amarillo corporativo */
            padding: 10px;
            display: inline-block;
            width: 100%;
            box-sizing: border-box;
            border-radius: 4px;
        }
        .meta-info {
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: #fff;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th {
            background-color: #f2f2f2;
            padding: 12px;
            text-align: left;
        }
        td {
            padding: 10px;
            vertical-align: top;
        }
        .dashboard-container {
            text-align: center;
            margin: 40px 0;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .step-list {
            background: #fff;
            padding: 20px 40px;
            border-radius: 8px;
            border-left: 5px solid #ffeb3b;
        }
        .footer-link {
            display: inline-block;
            margin-top: 10px;
            color: #0056b3;
            text-decoration: none;
            font-weight: bold;
        }
        .footer-link:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

<header>
    <h1>Documentación Dashboard: Ask A Manager Salary Survey 2021</h1>
    <div class="meta-info">
        <p><strong>Fuente:</strong> Ask A Manager Salary Survey 2021</p>
        <p><strong>Herramienta:</strong> Looker Studio</p>
    </div>
</header>

<h2>1. Diccionario de Variables y Estructura de Datos</h2>
<p>La siguiente tabla detalla la arquitectura de la base de datos utilizada para el análisis salarial. Se incluyen tanto las variables de captura original como las variables calculadas para la normalización financiera.</p>

<table>
    <thead>
        <tr>
            <th>Variable</th>
            <th>Tipo de Dato</th>
            <th>Descripción Funcional</th>
            <th>Ejemplo de Registro</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Timestamp</td><td>Temporal</td><td>Fecha y hora de captura de la encuesta.</td><td>2021-04-27 11:02:10</td></tr>
        <tr><td>How old are you?</td><td>Categórica Ordinal</td><td>Segmentación por rangos etarios.</td><td>25-34</td></tr>
        <tr><td>What industry do you work in?</td><td>Categórica Nominal</td><td>Sector económico de desempeño.</td><td>Education (Higher Education)</td></tr>
        <tr><td>Job title</td><td>Texto</td><td>Denominación del cargo.</td><td>Research and Instruction Librarian</td></tr>
        <tr><td>Job title (Context)</td><td>Texto</td><td>Aclaraciones cualitativas sobre el rol.</td><td>Puchasing Specialist</td></tr>
        <tr><td>Annual salary</td><td>Numérica Continua</td><td>Salario base anual (Moneda original).</td><td>55,000</td></tr>
        <tr><td>Additional compensation</td><td>Numérica Continua</td><td>Bonos, horas extra y variables anuales.</td><td>0</td></tr>
        <tr><td>Currency</td><td>Categórica Nominal</td><td>Divisa de reporte.</td><td>USD</td></tr>
        <tr><td>Currency (Other)</td><td>Texto</td><td>Especificación manual de moneda.</td><td>USD</td></tr>
        <tr><td>Income context</td><td>Texto</td><td>Observaciones sobre el esquema de ingresos.</td><td>Pago Semestral</td></tr>
        <tr><td>Country</td><td>Categórica Nominal</td><td>País de residencia laboral.</td><td>United States</td></tr>
        <tr><td>State (U.S. only)</td><td>Categórica Nominal</td><td>Estado de trabajo (Filtro para EE.UU.).</td><td>Massachusetts</td></tr>
        <tr><td>City</td><td>Categórica Nominal</td><td>Ciudad de trabajo.</td><td>Boston</td></tr>
        <tr><td>Experience (overall)</td><td>Categórica Ordinal</td><td>Trayectoria profesional total acumulada.</td><td>5–7 years</td></tr>
        <tr><td>Experience (field)</td><td>Categórica Ordinal</td><td>Trayectoria específica en el área actual.</td><td>5–7 years</td></tr>
        <tr><td>Education level</td><td>Categórica Ordinal</td><td>Máximo grado académico obtenido.</td><td>Master's degree</td></tr>
        <tr><td>Gender</td><td>Categórica Nominal</td><td>Identidad de género del consultado.</td><td>Woman</td></tr>
        <tr><td>Race</td><td>Multicategórica</td><td>Identificación étnico-racial.</td><td>White</td></tr>
    </tbody>
</table>

<h2>Visualización del Business Intelligence</h2>
<div class="dashboard-container">
    <iframe width="100%" height="600" src="https://lookerstudio.google.com/embed/reporting/64d26999-8da1-4997-953f-3b274fae0b56/page/Wc7mF" frameborder="0" style="border:0" allowfullscreen sandbox="allow-storage-access-by-user-activation allow-scripts allow-same-origin allow-popups allow-popups-to-escape-sandbox"></iframe>
    <br>
    <a class="footer-link" href="https://lookerstudio.google.com/reporting/64d26999-8da1-4997-953f-3b274fae0b56" target="_blank">Ver reporte en pantalla completa &#10697;</a>
</div>

<h2>2. Variables de Transformación y Normalización (ETL)</h2>
<p>Durante el proceso de transformación se crearon variables para garantizar consistencia y permitir comparaciones transnacionales.</p>

<table>
    <thead>
        <tr>
            <th>Variable</th>
            <th>Tipo</th>
            <th>Descripción</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Country_Normalized</td><td>Texto</td><td>País estandarizado para evitar duplicados por escritura.</td></tr>
        <tr><td>City_Normalized</td><td>Texto</td><td>Ciudad normalizada.</td></tr>
        <tr><td>salario_anual_cop</td><td>Numérica continua</td><td>Salario anual convertido a pesos colombianos.</td></tr>
        <tr><td>compensaciones_cop</td><td>Numérica continua</td><td>Compensaciones monetarias convertidas a COP.</td></tr>
        <tr><td>total_compensacion_cop</td><td>Numérica continua</td><td>Suma de salario anual y compensaciones en COP.</td></tr>
    </tbody>
</table>

<h3>Lógica de Conversión Monetaria</h3>
<p>Se aplicó una tasa de cambio fija representativa para las siguientes divisas hacia COP:</p>
<ul>
    <li>USD, GBP, CAD, EUR, AUD/NZD, CHF, JPY, SEK, ZAR, HKD.</li>
    <li>Para la categoría <strong>"Other"</strong>, se realizó una validación manual del campo de especificación.</li>
</ul>

<h2>3. Notas Metodológicas y Paso a Paso</h2>
<div class="step-list">
    <p><strong>Consistencia de Tipos:</strong> Las variables ordinales mantienen su jerarquía lógica para evitar sesgos en tendencias.</p>
    <p><strong>Tratamiento Monetario:</strong> Los campos con sufijo <code>_cop</code> permiten cálculos estadísticos homogéneos.</p>
    <hr>
    <h3>Procedimiento de Replicabilidad</h3>
    <ol>
        <li><strong>Carga:</strong> Importación de fuente original a Looker Studio.</li>
        <li><strong>Limpieza:</strong> Normalización de textos y tratamiento de valores nulos.</li>
        <li><strong>Conversión:</strong> Creación de campos calculados con tasas de cambio actualizadas.</li>
        <li><strong>Agregación:</strong> Generación de la variable de compensación total.</li>
        <li><strong>Visualización:</strong> Construcción de gráficos de correlación (Industria, Experiencia, Género).</li>
        <li><strong>Actualización:</strong> Reemplazo de archivo fuente y refresco del modelo.</li>
    </ol>
</div>

<h2>4. Conclusión</h2>
<p>Este modelo garantiza la <strong>trazabilidad y reproducibilidad</strong> de los datos salariales. Al convertir los valores a una moneda común (COP) y normalizar las variables geográficas, se eliminan ruidos estadísticos, permitiendo una interpretación estratégica de la relación entre educación, experiencia y remuneración.</p>

</body>
</html>
