<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EcoSemillas - Papel Sembrable</title>
  <style>
    /* --- RESETEO GENERAL --- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Arial", sans-serif;
      line-height: 1.6;
      background-color: #f9fff9;
      color: #333;
    }

    /* --- ENCABEZADO --- */
    header {
      background-color: #3b7a57;
      color: white;
      padding: 30px 15px;
      text-align: center;
    }

    header h1 {
      font-size: 2rem;
    }

    header p {
      font-size: 1rem;
      margin-top: 5px;
    }

    /* --- NAVEGACIÓN --- */
    nav {
      background-color: #2d5e44;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      padding: 15px 20px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s;
    }

    nav a:hover {
      background-color: #469b6e;
    }

    /* --- SECCIONES --- */
    section {
      padding: 50px 25px;
      text-align: center;
    }

    h1, h2 {
      color: #2d5e44;
      margin-bottom: 15px;
    }

    p {
      max-width: 800px;
      margin: 0 auto;
      font-size: 1rem;
    }

    /* --- PRODUCTOS --- */
    .productos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .producto {
      background-color: white;
      border: 1px solid #d9d9d9;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .producto:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }

    .producto img {
      width: 100%;
      height: auto;
      border-radius: 12px;
      object-fit: cover;
    }

    .producto h3 {
      margin-top: 10px;
      font-size: 1.2rem;
      color: #2d5e44;
    }

    .boton {
      background-color: #3b7a57;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
      transition: background 0.3s;
    }

    .boton:hover {
      background-color: #2d5e44;
    }

    .detalles {
      display: none;
      text-align: left;
      margin-top: 10px;
      background-color: #f0fff0;
      padding: 10px;
      border-radius: 8px;
    }

    /* --- CARRITO --- */
    #carrito {
      position: fixed;
      right: 15px;
      bottom: 15px;
      background: white;
      border: 2px solid #3b7a57;
      border-radius: 10px;
      padding: 15px;
      width: 280px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      z-index: 1000;
    }

    #carrito h3 {
      text-align: center;
      color: #2d5e44;
      margin-bottom: 10px;
    }

    #listaCarrito {
      max-height: 120px;
      overflow-y: auto;
      list-style: none;
      margin-bottom: 10px;
    }

    /* --- TABLAS --- */
    table {
      border-collapse: collapse;
      margin: 20px auto;
      width: 90%;
      max-width: 700px;
      font-size: 0.95rem;
    }

    th, td {
      border: 1px solid #ccc;
      padding: 8px;
    }

    th {
      background-color: #e8f5e9;
    }

    tr:nth-child(even) {
      background-color: #f5fff5;
    }

    /* --- PIE DE PÁGINA --- */
    footer {
      background-color: #2d5e44;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
      font-size: 0.9rem;
    }

    /* --- RESPONSIVIDAD --- */
    @media (max-width: 900px) {
      nav a {
        padding: 10px;
        font-size: 0.9rem;
      }

      header h1 {
        font-size: 1.7rem;
      }

      section {
        padding: 30px 15px;
      }

      #carrito {
        width: 90%;
        right: 5%;
        bottom: 10px;
      }
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 1.5rem;
      }

      header p {
        font-size: 0.9rem;
      }

      .producto h3 {
        font-size: 1rem;
      }

      nav {
        flex-direction: column;
      }

      nav a {
        width: 100%;
        text-align: center;
        border-top: 1px solid rgba(255,255,255,0.2);
      }

      #carrito {
        width: 95%;
        right: 2.5%;
        bottom: 5px;
        font-size: 0.9rem;
      }

      table {
        font-size: 0.85rem;
      }

      .boton {
        padding: 8px 10px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>EcoSemillas 🌱</h1>
    <p>Papel sembrable 100% reciclado y biodegradable</p>
  </header>

  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#nosotros">Nosotros</a>
    <a href="#productos">Productos</a>
    <a href="#proceso">Proceso</a>
    <a href="#costos">Costos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <section id="inicio">
    <h2>♻️ Bienvenido a EcoSemillas ♻️</h2>
    <p>Transformamos el papel en vida 🌿. Cada hoja contiene semillas listas para germinar y cuidar el planeta.</p>
  </section>

  <section id="nosotros">
    <h2>Sobre Nosotros</h2>
    <p><b>EcoSemillas</b> nació como una propuesta sustentable para reducir residuos y promover la conciencia ambiental.</p>
    <p>Elaboramos papel sembrable artesanalmente, con amor por la naturaleza y compromiso con el futuro.</p>
  </section>

  <section id="productos">
    <h2>Nuestros Productos</h2>
    <div class="productos">
      <div class="producto">
        <img src="imagenes/tarjeta.jpg" alt="Tarjetas sembrables con semillas">
        <h3>Tarjetas Sembrables</h3>
        <p>$1.200</p>
        <button class="boton" onclick="toggleDetalles(this)">Más detalles</button>
        <div class="detalles">
          <p>Tarjetas ecológicas personalizadas con semillas de flores o hierbas. Perfectas para eventos y regalos.</p>
        </div>
        <button class="boton" onclick="agregarCarrito('Tarjetas Sembrables', 1200)">Agregar al carrito</button>
      </div>

      <div class="producto">
        <img src="imagenes/etiqueta.jpg" alt="Etiquetas sembrables">
        <h3>Etiquetas Sembrables</h3>
        <p>$1.000</p>
        <button class="boton" onclick="toggleDetalles(this)">Más detalles</button>
        <div class="detalles">
          <p>Etiquetas hechas con papel reciclado y semillas de rúcula o menta. Una forma original de cuidar el planeta.</p>
        </div>
        <button class="boton" onclick="agregarCarrito('Etiquetas Sembrables', 1000)">Agregar al carrito</button>
      </div>

      <div class="producto">
        <img src="imagenes/cuaderno.jpg" alt="Cuadernos ecológicos">
        <h3>Cuadernos Ecológicos</h3>
        <p>$3.500</p>
        <button class="boton" onclick="toggleDetalles(this)">Más detalles</button>
        <div class="detalles">
          <p>Cuadernos con tapas de papel sembrable, hechos a mano. Cada uno puede dar vida a una planta.</p>
        </div>
        <button class="boton" onclick="agregarCarrito('Cuadernos Ecológicos', 3500)">Agregar al carrito</button>
      </div>
    </div>
  </section>

  <section id="proceso">
    <h2>Proceso Productivo</h2>
    <p>Recolectamos papel usado, lo trituramos, mezclamos con semillas y moldeamos artesanalmente. Cada hoja seca al sol, conservando el poder de germinar. 🌸</p>
  </section>

  <section id="costos">
    <h2>💰 Análisis de Costos y Rentabilidad</h2>
    <!-- tablas igual que antes -->
  </section>

  <section id="contacto">
    <h2>Contacto</h2>
    <p>📍 S.M TUCUMÁN, Argentina</p>
    <p>📧 ecosiemillas@gmail.com</p>
    <p>📱 Instagram: <a href="https://www.instagram.com/eco_.semillas" target="_blank" style="color:#3b7a57; font-weight:bold;">@eco_.semillas</a></p>
    <p>☎️ +54 381 511 1428</p>
  </section>

  <div id="carrito">
    <h3>🛒 Carrito</h3>
    <ul id="listaCarrito"></ul>
    <p><b>Total:</b> $<span id="total">0</span></p>
    <button class="boton" onclick="finalizarCompra()">Finalizar compra</button>
  </div>

  <footer>
    <p>© 2025 EcoSemillas - Papel que florece 🌱</p>
  </footer>

  <script>
    function toggleDetalles(boton) {
      const detalles = boton.nextElementSibling;
      detalles.style.display = detalles.style.display === "block" ? "none" : "block";
    }

    let carrito = [];
    let total = 0;

    function agregarCarrito(nombre, precio) {
      carrito.push({ nombre, precio });
      total += precio;
      actualizarCarrito();
    }

    function actualizarCarrito() {
      const lista = document.getElementById("listaCarrito");
      lista.innerHTML = "";
      carrito.forEach(item => {
        const li = document.createElement("li");
        li.textContent = `${item.nombre} - $${item.precio}`;
        lista.appendChild(li);
      });
      document.getElementById("total").textContent = total;
    }

    function finalizarCompra() {
      if (carrito.length === 0) {
        alert("Tu carrito está vacío 🌱");
      } else {
        alert("Gracias por tu compra ecológica 💚");
        carrito = [];
        total = 0;
        actualizarCarrito();
      }
    }
  </script>
</body>
</html>
