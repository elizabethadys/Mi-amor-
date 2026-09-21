<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para Adys</title>
<style>
body{margin:0;background:#000;display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:100vh;color:#fff;font-family:sans-serif;overflow:hidden}
h1{letter-spacing:3px}
.flor-principal{font-size:100px;cursor:pointer;animation:latido 1.5s infinite}
@keyframes latido{0%,100%{transform:scale(1)}50%{transform:scale(1.2)}}
#jardin{display:none;flex-direction:column;align-items:center;text-align:center;padding:20px}
#jardin.mostrar{display:flex}
.foto{width:200px;height:200px;border-radius:50%;object-fit:cover;border:3px solid #ffeb3b;box-shadow:0 0 20px #ffeb3b;margin:20px 0}
.flores{font-size:50px;animation:flotar 2s infinite alternate}
@keyframes flotar{from{transform:translateY(0)}to{transform:translateY(-10px)}}
</style>
</head>
<body>

<h1>PARA MI VIDA</h1>
<div id="portada" style="text-align:center">
  <div class="flor-principal" id="florBtn">🌼</div>
  <p>Tócala, amor...</p>
  <p style="font-size:12px;opacity:0.6">Que me haya demorado no significa que serás espectadora, mi vida 💗</p>
</div>

<div id="jardin">
  <div class="flores">🌼🌼💛🌼🌼🌼</div>
  <img src="assets/foto-adys.png" class="foto" alt="Adys">
  <h2>Para ti, Adys</h2>
  <p>Estas flores amarillas son para recordarte lo mucho que te amo.<br>Gracias por existir en mi vida.</p>
  <div class="flores">🌼💛🌼</div>
</div>

<audio id="musica" src="assets/stand-by-me.mp4" loop></audio>

<script>
const btn = document.getElementById('florBtn');
const musica = document.getElementById('musica');
const jardin = document.getElementById('jardin');
const portada = document.getElementById('portada');

btn.addEventListener('click', () => {
  musica.play().catch(e=>console.log("Error musica:", e));
  portada.style.display = 'none';
  jardin.classList.add('mostrar');
});

btn.addEventListener('touchstart', () => {
  musica.play().catch(e=>console.log("Error musica:", e));
  portada.style.display = 'none';
  jardin.classList.add('mostrar');
});
</script>

</body>
</html>
