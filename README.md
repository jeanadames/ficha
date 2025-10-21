<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ficha Institucional</title>
  <style>
    body { font-family: Arial; padding: 30px; background: #f4f4f4; }
    .ficha { background: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px #ccc; max-width: 500px; margin: auto; }
    h2 { color: #2c3e50; }
    .dato { margin: 10px 0; font-size: 18px; }
  </style>
</head>
<body>
  <div class="ficha">
    <h2>Ficha Institucional</h2>
    <div class="dato"><strong>Acta:</strong> <span id="acta"></span></div>
    <div class="dato"><strong>Tipo:</strong> <span id="tipo"></span></div>
    <div class="dato"><strong>Fecha:</strong> <span id="fecha"></span></div>
    <div class="dato"><strong>Nombre del Inscrito:</strong> <span id="nombre"></span></div>
  </div>

  <script>
    // Función para leer parámetros de la URL
    function getParam(name) {
      const urlParams = new URLSearchParams(window.location.search);
      return urlParams.get(name) || "No disponible";
    }

    // Asignar valores a los campos
    document.getElementById("acta").textContent = getParam("acta");
    document.getElementById("tipo").textContent = getParam("tipo");
    document.getElementById("fecha").textContent = getParam("fecha");
    document.getElementById("nombre").textContent = decodeURIComponent(getParam("nombre"));
  </script>
</body>
</html>

