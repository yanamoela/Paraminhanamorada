# Paraminhanamorada
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Surpresa para você</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #add8e6, #87cefa);
      overflow: hidden;
    }

    .intro {
      position: fixed;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      background: linear-gradient(to bottom right, #add8e6, #87cefa);
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      z-index: 10;
      transition: opacity 1s ease;
    }

    .intro.hidden {
      opacity: 0;
      pointer-events: none;
    }

    .intro button {
      font-size: 1.5rem;
      padding: 1rem 2rem;
      background-color: #ff4d6d;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .intro button:hover {
      transform: scale(1.05);
    }

    .container {
      display: none;
      padding: 3rem;
      text-align: center;
      max-width: 700px;
      margin: 10vh auto;
      background-color: white;
      border-radius: 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      z-index: 2;
      position: relative;
    }

    .container.visible {
      display: block;
      animation: fadeIn 1.5s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      color: #2e8bc0;
    }

    .heart {
      font-size: 2rem;
      color: #ff4d6d;
      animation: pulse 1.2s infinite;
      margin-top: 20px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }

    .flower {
      position: fixed;
      top: -50px;
      font-size: 24px;
      animation: fall linear infinite;
      color: pink;
      z-index: 1;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh);
        opacity: 0;
      }
    }

    .floating-heart {
      position: fixed;
      bottom: 0;
      left: 50%;
      font-size: 4rem;
      color: #ff4d6d55;
      animation: floatUp 6s ease-in-out infinite;
      z-index: 0;
    }

    @keyframes floatUp {
      0% { transform: translateX(-50%) translateY(0); opacity: 1; }
      100% { transform: translateX(-50%) translateY(-100vh); opacity: 0; }
    }

    iframe {
      display: none;
    }
  </style>
</head>
<body>

  <!-- Tela inicial -->
  <div class="intro" id="intro">
    <h2 style="color: white;">Tem uma surpresa pra você...</h2>
    <button onclick="showLove()">Clique aqui, meu amor</button>
  </div>

  <!-- Coração flutuando -->
  <div class="floating-heart">❤️</div>

  <!-- Flores caindo -->
  <script>
    for(let i=0; i<25; i++) {
      let flower = document.createElement("div");
      flower.className = "flower";
      flower.innerText = "❀";
      flower.style.left = Math.random() * 100 + "vw";
      flower.style.animationDuration = (Math.random() * 5 + 5) + "s";
      flower.style.fontSize = (Math.random() * 20 + 15) + "px";
      document.body.appendChild(flower);
    }
  </script>

  <!-- Texto romântico -->
  <div class="container" id="mainContent">
    <h1>Eu te amo muito, meu amor!</h1>
    <p>Eu sou completamente apaixonado por você, e sou a pessoa mais feliz do mundo por ter você ao meu lado. Você é o motivo do meu sorriso quando acordo, é o brilho dos meus dias e a mulher mais linda e perfeita que existe.</p>
    <p>Eu sonho com a gente juntos pra sempre — ficando bem velhinhos, criando nossos filhos e construindo uma família cheia de amor, paz e sem brigas. Quero te abraçar logo, sentir teu cheiro, e viver contigo todos os momentos que a distância agora não permite.</p>
    <p>Quero meu Instagram cheio de fotos nossas — e principalmente suas, porque eu me orgulho demais da mulher incrível que tenho. Eu quero te amar pra sempre, meu amor. Não importa o que aconteça, nenhuma briga vai me fazer desistir do que estamos construindo juntos.</p>
    <p>Que o nosso amor seja forte, leve, verdadeiro… e infinito.</p>
    <div class="heart">Te amo demais, minha princesa!</div>
  </div>

  <!-- Música do YouTube -->
  <iframe id="musicPlayer" width="0" height="0"
    src="https://www.youtube.com/embed/3qet3W5kfXg?autoplay=1"
    allow="autoplay"></iframe>

  <script>
    function showLove() {
      document.getElementById("intro").classList.add("hidden");
      document.getElementById("mainContent").classList.add("visible");
      document.getElementById("musicPlayer").style.display = "block";
    }
  </script>

</body>
</html>
