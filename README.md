<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Hioram Martines</title>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f8f8f8;
      color: #1a1a1a;
      line-height: 1.8;
    }

    header {<header>
  <div>
    <img src="logo.png" alt="Bruno Guerra" class="logo">.logo {
  width: 140px;
  margin-bottom: 30px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
    <h1>HIORAM MARTINES</h1>
    <p>Marca pessoal • Estética • Presença</p>
  </div>
</header>
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 20px;
      background: #fdfdfd;
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      letter-spacing: 3px;
    }

    header p {
      margin-top: 20px;
      font-size: 1rem;
      color: #666;
    }

    section {
      max-width: 900px;
      margin: auto;
      padding: 100px 20px;
      text-align: center;
    }

    section h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 30px;
    }

    section p {
      color: #444;
      font-size: 1rem;
    }

    .impact {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem;
      max-width: 700px;
      margin: auto;
      color: #111;
    }

    .socials a {
      display: inline-block;
      margin: 20px 15px 0;
      text-decoration: none;
      color: #111;
      font-weight: 500;
      border-bottom: 1px solid transparent;
    }

    .socials a:hover {
      border-color: #111;
    }

    footer {
      text-align: center;
      padding: 40px;
      font-size: 0.85rem;
      color: #888;
    }

    /* ADMIN */
    .admin-trigger {
      position: fixed;
      bottom: 15px;
      right: 15px;
      font-size: 0.7rem;
      opacity: 0.15;
      cursor: pointer;
    }

    .admin-login {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(255,255,255,0.95);
      align-items: center;
      justify-content: center;
    }

    .admin-box {
      background: #fff;
      padding: 40px;
      border: 1px solid #ddd;
      text-align: center;
      width: 300px;
    }

    .admin-box input {
      width: 100%;
      padding: 10px;
      margin-top: 20px;
      border: 1px solid #ccc;
    }

    .admin-box button {
      margin-top: 20px;
      padding: 10px;
      width: 100%;
      background: #111;
      color: white;
      border: none;
      cursor: pointer;
    }

    .admin-panel {
      display: none;
      padding: 120px 20px;
      text-align: center;
    }
  </style>
</head>
<body><div class="socials">
  <a href="https://www.instagram.com/bruno_eu_hioram?igsh=dThsMDFtY2R4Ynp3&utm_source=qr" target="_blank">Instagram</a>
  <a href="https://wa.me/message/PIVHCRXKTGIJL1" target="_blank">WhatsApp</a>
  <a href="https://wa.me/message/PIVHCRXKTGIJL1" target="_blank">Contato</a>
</div>

<header>
  <div>
    <h1>HIORAM MARTINES</h1>
    <p>Marca pessoal • Estética • Presença</p>
  </div>
</header>

<section>
  <h2>Sobre</h2>
  <p>
    Hioram Martines é uma marca pessoal construída a partir da simplicidade,
    da intenção e do olhar atento aos detalhes.  
    Cada escolha comunica identidade, cada elemento carrega propósito.
  </p>
</section>

<section>
  <p class="impact">
    “Menos ruído. Mais essência.  
    Presença que não precisa ser explicada.”
  </p>
</section>

<section>
  <h2>Conexões</h2>
  <div class="socials">
    <a href="#">Instagram</a>
    <a href="#">WhatsApp</a>
    <a href="#">Contato</a>
  </div>
</section>

<footer>
  © 2026 • Hioram Martines
</footer>

<div class="admin-trigger" onclick="abrirAdmin()">admin</div>

<div class="admin-login" id="adminLogin">
  <div class="admin-box">
    <h3>Administrador</h3>
    <input type="password" id="senha" placeholder="Senha">
    <button onclick="login()">Entrar</button>
  </div><div
</div>
</div>

<div class="admin-panel" id="adminPanel">
  <h2>Painel Administrativo</h2>
  <p>Área reservada para gestão e planejamento da marca.</p>
</div>

<script>
  const senhaCorreta = "guerra99";

  function abrirAdmin() {
    document.getElementById("adminLogin").style.display = "flex";
  }

  function login() {
    const senha = document.getElementById("senha").value;
    if (senha === senhaCorreta) {
      document.body.innerHTML = document.getElementById("adminPanel").outerHTML;
    } else {
      alert("Senha incorreta");
    }
  }
</script>

</body>
</html>
