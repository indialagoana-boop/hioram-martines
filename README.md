# hioram-martines<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Hioram Martines</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Montserrat:wght@300;500&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0b0b0b;
      color: #f5f5f5;
      font-family: 'Montserrat', sans-serif;
    }

    header {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 20px;
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      letter-spacing: 3px;
    }

    header p {
      margin-top: 15px;
      font-weight: 300;
      opacity: 0.7;
    }

    section {
      max-width: 900px;
      margin: auto;
      padding: 80px 20px;
      text-align: center;
    }

    section h2 {
      font-family: 'Playfair Display', serif;
      margin-bottom: 20px;
      font-size: 2rem;
    }

    section p {
      opacity: 0.75;
      line-height: 1.7;
    }

    footer {
      text-align: center;
      padding: 30px;
      opacity: 0.4;
      font-size: 0.9rem;
    }

    /* LOGIN ADMIN */
    .admin-login {
      position: fixed;
      bottom: 15px;
      right: 15px;
      opacity: 0.2;
      cursor: pointer;
      font-size: 0.8rem;
    }

    .login-box {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.95);
      align-items: center;
      justify-content: center;
    }

    .login-box div {
      background: #111;
      padding: 40px;
      border-radius: 8px;
      text-align: center;
      width: 300px;
    }

    .login-box input {
      width: 100%;
      padding: 10px;
      margin-top: 15px;
      background: #000;
      border: 1px solid #333;
      color: white;
    }

    .login-box button {
      margin-top: 15px;
      padding: 10px;
      width: 100%;
      background: white;
      color: black;
      border: none;
      cursor: pointer;
      font-weight: bold;
    }

    .admin-panel {
      display: none;
      padding: 80px 20px;
      text-align: center;
    }
  </style>
</head>
<body>

<header>
  <div>
    <h1>HIORAM MARTINES</h1>
    <p>Identidade. Estilo. Presença.</p>
  </div>
</header>

<section>
  <h2>Sobre</h2>
  <p>
    Uma marca pessoal construída com autenticidade, estética e propósito.
    Menos excesso, mais essência.
  </p>
</section>

<footer>
  © 2026 • Hioram Martines
</footer>

<div class="admin-login" onclick="abrirLogin()">admin</div>

<div class="login-box" id="loginBox">
  <div>
    <h2>Admin</h2>
    <input type="password" id="senha" placeholder="Senha">
    <button onclick="login()">Entrar</button>
  </div>
</div>

<div class="admin-panel" id="adminPanel">
  <h2>Painel Administrativo</h2>
  <p>Aqui você pode planejar conteúdos, ideias e estrutura da marca.</p>
</div>

<script>
  const senhaCorreta = "guerra99";

  function abrirLogin() {
    document.getElementById("loginBox").style.display = "flex";
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
