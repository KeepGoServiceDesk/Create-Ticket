<html lang="es" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="Content-Language" content="es">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mesa de Servicio - Levantar Ticket</title>
  <link rel="stylesheet" href="css/master.css">

  <style>
    body {
      font-family: "Segoe UI", Arial, sans-serif;
      background: #f4f6f9;
      margin: 0;
      padding: 0;
    }

    .container {
      max-width: 600px;
      margin: 40px auto;
      padding: 25px;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    h1 {
      text-align: center;
      font-size: 1.6rem;
      margin-bottom: 20px;
      color: #333;
    }

    .form-group {
      margin-bottom: 18px;
    }

    label {
      display: block;
      font-weight: 600;
      margin-bottom: 6px;
      color: #444;
    }

    input[type="text"], input[type="email"] {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
      transition: border-color 0.3s;
    }

    input[type="text"]:focus, input[type="email"]:focus {
      outline: none;
      border-color: #4a90e2;
      box-shadow: 0 0 4px rgba(74,144,226,0.4);
    }

    .btn-submit {
      width: 100%;
      padding: 12px;
      background: #4a90e2;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      color: white;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s;
    }

    .btn-submit:hover {
      background: #357ab8;
    }

    .footer {
      margin-top: 20px;
      font-size: 0.85rem;
      text-align: center;
      color: #777;
    }

    .footer a {
      color: #4a90e2;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Levantar Ticket</h1>
    <form action="https://stratech.sysaidit.com:443/webformsubmit?pageEncoding=utf-8" method="post" name="frm" onsubmit="return ValidateFrm();">
      
      <!-- Campos ocultos necesarios -->
      <input type="hidden" name="X_TOKEN_stratech" value="b754c10a-bee6-4069-bfd2-6b2cd94a5ff9">
      <input type="hidden" name="accountID" value="stratech">
      <input type="hidden" name="formID" value="64a1d9ed:1990633a44d:-2a93">
      <input type="hidden" name="reRoute" value="0">

      <div class="form-group">
        <label for="firstName">Nombre</label>
        <input type="text" id="firstName" name="firstName" maxlength="40">
      </div>

      <div class="form-group">
        <label for="lastName">Apellidos</label>
        <input type="text" id="lastName" name="lastName" maxlength="50">
      </div>

      <div class="form-group">
        <label for="cellphone">Teléfono móvil</label>
        <input type="text" id="cellphone" name="cellphone" maxlength="32">
      </div>

      <div class="form-group">
        <label for="email">Correo electrónico</label>
        <input type="email" id="email" name="email" maxlength="64">
      </div>

      <div class="form-group">
        <label for="title">Título del reporte</label>
        <input type="text" id="title" name="title" maxlength="100">
      </div>

      <button type="submit" class="btn-submit">📨 Enviar Ticket</button>
    </form>

<div class="footer" style="text-align:center; font-family: Arial, sans-serif; font-size:14px;">
  <p>Powered by <span style="color:blue; font-weight:bold;">KeepGo</span></p>
</div>


  <script>
    function ValidateFrm(){
      const nombre = document.getElementById("firstName").value.trim();
      const apellidos = document.getElementById("lastName").value.trim();
      const telefono = document.getElementById("cellphone").value.trim();
      const correo = document.getElementById("email").value.trim();
      const titulo = document.getElementById("title").value.trim();

      if(!nombre){ alert("Introduzca su nombre"); return false; }
      if(!apellidos){ alert("Introduzca sus apellidos"); return false; }
      if(!telefono){ alert("Introduzca un teléfono móvil"); return false; }
      if(!correo){ alert("Introduzca su correo electrónico"); return false; }
      if(!titulo){ alert("Introduzca un título para el ticket"); return false; }

      return true;
    }
  </script>
