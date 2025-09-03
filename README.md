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
      max-width: 650px;
      margin: 40px auto;
      padding: 25px;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    h1 {
      text-align: center;
      font-size: 1.7rem;
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

    input[type="text"], select {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
      transition: border-color 0.3s;
    }

    input:focus, select:focus {
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

    .footer span {
      color: blue;
      font-weight: bold;
    }
  </style>
</head>

<body>
  <div class="container">
    <h1>Levantar Ticket</h1>

    <form action="https://stratech.sysaidit.com:443/webformsubmit?pageEncoding=utf-8" 
          method="post" 
          name="frm" 
          onsubmit="return ValidateFrm();">
      
      <!-- Campos ocultos de SysAid -->
      <input type="hidden" name="X_TOKEN_stratech" value="824d1f26-ba8b-4905-be83-29408f94328f">
      <input type="hidden" name="accountID" value="stratech">
      <input type="hidden" name="formID" value="64a1d9ed:1990633a44d:-2a93">
      <input type="hidden" name="reRoute" value="0">
      <input type="hidden" name="parentPageName" value="WebFormHTML.jsp?idx=0">
      <input type="hidden" name="paneMessage" value="">
      <input type="hidden" name="paneType" value="">
      <input type="hidden" name="paneBtnArrayButtons" value="">
      <input type="hidden" name="panePreSubmitFunc" value="">
      <input type="hidden" name="paneTextRow" value="">
      <input type="hidden" name="centerPopup" value="">
      <input type="hidden" name="OK" value="">
      <input type="hidden" name="email" id="email" value="">

      <div class="form-group">
        <label for="firstName">Nombre</label>
        <input type="text" id="firstName" name="firstName" maxlength="40" required>
      </div>

      <div class="form-group">
        <label for="lastName">Apellidos</label>
        <input type="text" id="lastName" name="lastName" maxlength="50" required>
      </div>

      <div class="form-group">
        <label for="cellphone">Teléfono móvil</label>
        <input type="text" id="cellphone" name="cellphone" maxlength="32" required>
      </div>

      <div class="form-group">
        <label for="title">Título del reporte</label>
        <input type="text" id="title" name="title" maxlength="100" required>
      </div>

      <div class="form-group">
        <label for="CustomColumn449sr">Mesa de primer nivel</label>
        <select id="CustomColumn449sr" name="CustomColumn449sr" required>
          <option value="" disabled selected>Seleccione un valor</option>
          <option value="1">MESA ON</option>
          <option value="2">MESA FDA</option>
          <option value="3">MESA FS</option>
        </select>
      </div>

      <button type="submit" class="btn-submit" onclick="ExecuteOK(); return false;">📨 Enviar Ticket</button>
    </form>

    <div class="footer">
      <p>Powered by <span>KeepGo</span></p>
    </div>
  </div>

  <script>
    function ValidateFrm() {
      const nombre = document.getElementById("firstName").value.trim();
      const apellidos = document.getElementById("lastName").value.trim();
      const telefono = document.getElementById("cellphone").value.trim();
      const titulo = document.getElementById("title").value.trim();
      const mesa = document.getElementById("CustomColumn449sr").value;

      if (!nombre) { alert("Introduzca Nombre"); return false; }
      if (!apellidos) { alert("Introduzca Apellidos"); return false; }
      if (!telefono) { alert("Introduzca Teléfono móvil"); return false; }
      if (!titulo) { alert("Introduzca un título."); return false; }
      if (!mesa) { alert("Seleccione una mesa de primer nivel."); return false; }

      return true;
    }

    function ExecuteOK(){
      if (!ValidateFrm()) return;
      document.frm.OK.value = "OK";
      document.frm.submit();
    }
  </script>

  <!-- Scripts externos de SysAid -->
  <script src="https://stratech.sysaidit.com:443/calendar3.js" type="text/javascript"></script>
  <script src="https://stratech.sysaidit.com:443/webformsubmit?getJS=YES&accountID=stratech&formID=64a1d9ed:1990633a44d:-2a93" type="text/javascript"></script>
