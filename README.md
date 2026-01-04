<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Hioram Martines</title>

  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">

  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      font-family: 'Montserrat', sans-serif;
      background-color: #f5f5f3;
      color: #222;
    }
    header {
      min-height: 100vh;
      background:
        linear-gradient(rgba(255,255,255,0.8), rgba(255,255,255,0.8)),
        url("fundo.jpg") center/cover no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 40px 20px;
    }
    header img { width: 130px; margin-bottom: 30px; }
    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      letter-spacing: 2px;
      margin-bottom: 15px;
    }
    header p { font-size: 1rem; letter-spacing: 4px; text-transform: uppercase; color: #777; }
    section {
      max-width: 900px;
      margin: auto;
      padding: 100px 20px;
      text-align: center;
    }
    .impact {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 60px;
      cursor: pointer; /* Indica que pode clicar */
    }
    .about { font-size: 1.05rem; color: #555; max-width: 700px; margin: auto; margin-bottom: 60px; line-height: 1.8; transition: background 0.5s; padding: 20px; border-radius: 10px;}
    .buttons a {
      display: inline-block;
      margin: 12px;
      padding: 14px 36px;
      border: 1px solid #222;
      text-decoration: none;
      color: #222;
      font-size: 0.9rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      transition: 0.3s;
    }
    .buttons a:hover { background: #222; color: #fff; }
    footer { background: #ffffff; padding: 40px; text-align: center; font-size: 0.8rem; color: #999; }
  </style>
</head>

<body>

  <header>
    <img src="logo.png" alt="Hioram Martines">
    <h1>HIORAM MARTINES</h1>
    <p>Marca pessoal • Estética • Presença</p>
  </header>

  <section>
    <div class="impact" onclick="mudarImpacto()">
      Elegância é quando a presença fala antes das palavras.
    </div>

    <div class="about" id="sobre">
      Hioram Martines é uma marca pessoal guiada pela estética,
      pelo cuidado com os detalhes e pela construção de uma identidade
      sofisticada, limpa e autêntica.  
      Cada escolha comunica. Cada presença permanece.
    </div>

    <div class="buttons">
      <a href="#" onclick="abrirInstagram()">Instagram</a>
      <a href="#" onclick="abrirWhatsApp()">WhatsApp</a>
      <a href="#" onclick="mudarCorSobre()">Mudar Fundo</a>
    </div>
  </section>

  <section>
    <h2>Experiência</h2>
    <p class="about">
      Atendimento focado em estética, presença e identidade.
      Cada detalhe pensado para transmitir sofisticação,
      cuidado e exclusividade.
    </p>
  </section>

  <footer>
    © 2026 · Hioram Martines
  </footer>

  <script>
    // Função para abrir Instagram com confirmação
    function abrirInstagram() {
      if(confirm("Você quer realmente abrir o Instagram?")) {
        window.open("https://www.instagram.com/bruno_eu_hioram", "_blank");
      }
    }

    // Função para abrir WhatsApp com confirmação
    function abrirWhatsApp() {
      if(confirm("Deseja iniciar uma conversa no WhatsApp?")) {
        window.open("https://wa.me/message/PIVHCRXKTGIJL1", "_blank");
      }
    }

    // Função para mudar a frase de impacto
    function mudarImpacto() {
      const frases = [
        "Elegância é quando a presença fala antes das palavras.",
        "Detalhes fazem toda a diferença.",
        "A sofisticação está na autenticidade.",
        "Cada escolha comunica, cada presença permanece."
      ];
      const impact = document.querySelector(".impact");
      let novaFrase = frases[Math.floor(Math.random() * frases.length)];
      while(novaFrase === impact.textContent) {
        novaFrase = frases[Math.floor(Math.random() * frases.length)];
      }
      impact.textContent = novaFrase;
    }

    // Função para mudar cor de fundo da seção "Sobre"
    function mudarCorSobre() {
      const cores = ["#f5f5f3","#ffe4e1","#d1ffd6","#cce7ff","#fff4b2"];
      const sobre = document.getElementById("sobre");
      let novaCor = cores[Math.floor(Math.random() * cores.length)];
      while(novaCor === sobre.style.backgroundColor) {
        novaCor = cores[Math.floor(Math.random() * cores.length)];
      }
      sobre.style.backgroundColor = novaCor;
    }
  </script>

</body>
</html>
