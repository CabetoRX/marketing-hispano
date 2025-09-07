<style>
  .form-container {
    max-width: 420px;
    margin: 40px auto;
    padding: 25px;
    background: #f9f9f9;
    border-radius: 14px;
    box-shadow: 0 6px 12px rgba(0,0,0,0.1);
    font-family: 'Segoe UI', sans-serif;
    text-align: center;
  }

  .form-container img {
    max-width: 120px;
    margin-bottom: 20px;
  }

  .form-container h3 {
    color: #222;
    margin-bottom: 25px;
  }

  .form-container label {
    font-weight: bold;
    display: block;
    margin-bottom: 8px;
    color: #444;
    text-align: left;
  }

  .form-container input {
    width: 100%;
    padding: 10px;
    margin-bottom: 18px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 15px;
  }

  .form-container button {
    width: 100%;
    padding: 14px;
    background-color: #25D366;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 17px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  .form-container button:hover {
    background-color: #1ebe5d;
  }
</style>

<div class="form-container">
  <img src="https://assets.zyrosite.com/cdn-cgi/image/format=auto,w=375,fit=crop,q=95/mePJ8rnDjxUX0gZN/zixxar-logo-dJobXpLRG8h2GgpG.jpg" alt="Logo Zixxar">
  <h3>📲 Comparte tu invitación por WhatsApp</h3>

  <label for="nombre">Tu nombre como patrocinador:</label>
  <input type="text" id="nombre" placeholder="Ej. Carlos Ortiz">

  <label for="enlace">Tu enlace de registro:</label>
  <input type="text" id="enlace" placeholder="Ej. https://shop.zixxar.net/signup/...">

  <button onclick="compartirWhatsApp()">Compartir por WhatsApp</button>
</div>

<script>
function compartirWhatsApp() {
  const nombre = document.getElementById("nombre").value.trim();
  const enlace = document.getElementById("enlace").value.trim();

  if (!nombre || !enlace) {
    alert("Por favor, completa ambos campos.");
    return;
  }

  const paginaEquipo = "https://zixxarequipohispano.site/";
  const mensaje = `Hola 👋\nQuiero compartir contigo una oportunidad muy grande. La empresa se llama Zixxar y fue creada por CryptoData. Estoy desarrollando una carrera sólida en ella y me gustaría que pudieras ver de qué se trata.\n\nAquí tienes el enlace a la web de nuestro equipo, donde encontrarás toda la información sobre los proyectos:\n${paginaEquipo}\n\nAdemás, yo voy a ser tu patrocinador: ${nombre}\nConmigo contarás con formación, respaldo y el apoyo de un equipo comprometido con tu crecimiento.\n\nEste es el enlace para que crees tu cuenta y entres en mi equipo:\n${enlace}\n\n🚀 La vida te da oportunidades. Si quieres tener éxito, aprovecha la mayor cantidad de ellas. Recuerda recorrer la milla extra y salir de tu zona de confort.`;

  const whatsappURL = `https://wa.me/?text=${encodeURIComponent(mensaje)}`;
  window.open(whatsappURL, "_blank");
}
</script>
