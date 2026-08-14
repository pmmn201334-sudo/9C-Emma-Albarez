<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Estación Lumina · Calculadora de notas</title>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --fondo:#0B1026;
      --texto:#F4F6FF;
      --acento:#00E5A0;
      --acento-oscuro:#00C48A;
      --tarjeta:rgba(244,246,255,0.06);
      --borde:rgba(244,246,255,0.18);
    }
    *{margin:0;padding:0;box-sizing:border-box;}
    html{scroll-behavior:smooth;}
    body{
      font-family:'Space Grotesk','Segoe UI',Arial,sans-serif;
      background:var(--fondo);
      color:var(--texto);
      min-height:100vh;
      padding:1.5rem 1rem 3rem;
      background-image:
        radial-gradient(circle at 20% 15%,rgba(0,229,160,0.12),transparent 40%),
        radial-gradient(circle at 85% 85%,rgba(0,229,160,0.10),transparent 40%);
      background-attachment:fixed;
    }
    .contenedor{max-width:840px;margin:0 auto;}
    h1{font-size:2.5rem;line-height:1.15;margin-bottom:.5rem;}
    h2{font-size:1.6rem;color:var(--acento);margin-bottom:1rem;}
    h3{font-size:1.2rem;}
    p{line-height:1.6;}
    .encabezado{text-align:center;margin-bottom:2rem;}
    .encabezado p{opacity:.85;}
    .barra-superior{display:flex;justify-content:space-between;align-items:center;max-width:840px;margin:0 auto 1.5rem;}
    .barra-superior a{color:var(--acento);text-decoration:none;font-weight:700;}
    .tarjeta{background:var(--tarjeta);border:1px solid var(--borde);border-radius:1.2rem;padding:1.5rem;margin:1.25rem 0;}
    .boton{
      display:inline-block;
      background:var(--acento);
      color:#06281C;
      border:none;
      border-radius:999px;
      padding:.85rem 1.7rem;
      font-size:1rem;
      font-weight:700;
      font-family:inherit;
      cursor:pointer;
      text-decoration:none;
      box-shadow:0 0 18px rgba(0,229,160,.35);
      transition:transform .15s ease,background .15s ease;
    }
    .boton:hover{background:var(--acento-oscuro);transform:translateY(-2px);}
    .boton.secundario{background:transparent;color:var(--texto);border:2px solid var(--borde);box-shadow:none;}
    .boton.peligro{background:transparent;color:#FF5C5C;border:2px solid rgba(255,92,92,.5);box-shadow:none;padding:.45rem 1rem;font-size:.85rem;}
    .boton.peligro:hover{background:rgba(255,92,92,.15);}
    .fila-botones{display:flex;gap:1rem;flex-wrap:wrap;justify-content:center;}
    input,textarea,select{
      width:100%;
      background:rgba(244,246,255,.05);
      border:1px solid var(--borde);
      border-radius:.8rem;
      color:var(--texto);
      padding:.7rem 1rem;
      font-family:inherit;
      font-size:1rem;
    }
    input:focus,textarea:focus{outline:2px solid var(--acento);}
    label{display:block;margin:1rem 0 .3rem;opacity:.9;}
    table{width:100%;border-collapse:collapse;background:var(--tarjeta);border:1px solid var(--borde);border-radius:1rem;overflow:hidden;}
    th,td{border:1px solid var(--borde);padding:.6rem .4rem;text-align:center;font-size:.9rem;}
    th{background:rgba(0,229,160,.15);color:var(--acento);}
    .tabla-scroll{overflow-x:auto;}
    .vacio{opacity:.7;text-align:center;padding:1rem;}
    .nota-final{text-align:center;padding:1.5rem;}
    .nota-final .valor{font-size:3.5rem;font-weight:700;color:var(--acento);}
    .nota-final.aprobada .valor{color:var(--acento);}
    .nota-final.reprobada .valor{color:#FF5C5C;}
    .resultado-estado{font-size:1.2rem;margin-top:.5rem;}
  </style>
</head>
<body>
  <div class="contenedor">
    <nav class="barra-superior">
      <a href="menu.html">← Sala de Mando</a>
      <span>Estación Lumina</span>
    </nav>

    <header class="encabezado">
      <h1>Calculadora de notas</h1>
      <p>Promedia tus notas del colegio y mira si apruebas (la nota mínima para pasar es 3.0).</p>
    </header>

    <section class="tarjeta">
      <h2>Agregar nota</h2>
      <div class="grid" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:1rem;">
        <div>
          <label>Materia</label>
          <input id="materia" placeholder="Ejemplo: Matemáticas">
        </div>
        <div>
          <label>Nota (0 a 5)</label>
          <input id="nota" type="number" min="0" max="5" step="0.1" placeholder="4.5">
        </div>
      </div>
      <div class="fila-botones" style="margin-top:1.2rem;">
        <button class="boton" onclick="agregarNota()">Agregar nota</button>
      </div>
    </section>

    <section>
      <h2>Notas guardadas</h2>
      <div class="tabla-scroll">
        <table id="tablaNotas">
          <thead>
            <tr><th>Materia</th><th>Nota</th><th></th></tr>
          </thead>
          <tbody id="cuerpoTabla"></tbody>
        </table>
      </div>
      <p class="vacio" id="mensajeVacio">Aún no hay notas. ¡Agrega la primera!</p>
    </section>

    <section class="tarjeta nota-final" id="resultado" hidden>
      <h2>Tu promedio</h2>
      <div class="valor" id="valorPromedio"></div>
      <p class="resultado-estado" id="estadoResultado"></p>
    </section>
  </div>

  <script>
    let notas = JSON.parse(localStorage.getItem('lumina_notas') || '[]');

    function agregarNota() {
      const materia = document.getElementById('materia').value.trim();
      const nota = parseFloat(document.getElementById('nota').value);
      if (!materia) { alert('Escribe el nombre de la materia.'); return; }
      if (isNaN(nota) || nota < 0 || nota > 5) { alert('Escribe una nota entre 0 y 5.'); return; }
      notas.push({ id: Date.now(), materia: materia, nota: nota });
      localStorage.setItem('lumina_notas', JSON.stringify(notas));
      document.getElementById('materia').value = '';
      document.getElementById('nota').value = '';
      pintarNotas();
    }

    function eliminarNota(id) {
      notas = notas.filter(function (n) { return n.id !== id; });
      localStorage.setItem('lumina_notas', JSON.stringify(notas));
      pintarNotas();
    }

    function pintarNotas() {
      const cuerpo = document.getElementById('cuerpoTabla');
      cuerpo.innerHTML = '';
      document.getElementById('mensajeVacio').style.display = notas.length === 0 ? 'block' : 'none';
      let suma = 0;
      notas.forEach(function (n) {
        suma += n.nota;
        const fila = document.createElement('tr');
        const c1 = document.createElement('td');
        c1.textContent = n.materia;
        const c2 = document.createElement('td');
        c2.textContent = n.nota.toFixed(1);
        const c3 = document.createElement('td');
        const borrar = document.createElement('button');
        borrar.textContent = 'Eliminar';
        borrar.className = 'boton peligro';
        borrar.onclick = function () { eliminarNota(n.id); };
        c3.appendChild(borrar);
        fila.appendChild(c1);
        fila.appendChild(c2);
        fila.appendChild(c3);
        cuerpo.appendChild(fila);
      });
      const resultado = document.getElementById('resultado');
      if (notas.length === 0) { resultado.hidden = true; return; }
      const promedio = suma / notas.length;
      resultado.hidden = false;
      resultado.className = 'tarjeta nota-final ' + (promedio >= 3 ? 'aprobada' : 'reprobada');
      document.getElementById('valorPromedio').textContent = promedio.toFixed(1);
      document.getElementById('estadoResultado').textContent =
        promedio >= 3
          ? '¡Apruebas la misión! La Estación Lumina está orgullosa.'
          : 'Todavía no alcanzas la nota mínima. ¡Échale ganas, tripulante!';
    }

    pintarNotas();
  </script>
</body>
</html>
