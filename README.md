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

    input[type="text"] {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
      transition: border-color 0.3s;
    }

    input:focus {
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
      
      <!-- Campos ocultos -->
      <input type="hidden" name="X_TOKEN_stratech" value="e667e799-a5ab-4a19-827c-dd3a505f7030">
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
        <input type="text" id="firstName" name="firstName" maxlength="40" onfocus="global_value=this.value" onkeyup="checkChange(this.value)" onchange="setChange();">
      </div>

      <div class="form-group">
        <label for="lastName">Apellidos</label>
        <input type="text" id="lastName" name="lastName" maxlength="50" onfocus="global_value=this.value" onkeyup="checkChange(this.value)" onchange="setChange();">
      </div>

      <div class="form-group">
        <label for="cellphone">Teléfono móvil</label>
        <input type="text" id="cellphone" name="cellphone" maxlength="32" onfocus="global_value=this.value" onkeyup="checkChange(this.value)" onchange="setChange();">
      </div>

      <div class="form-group">
        <label for="title">Título del reporte</label>
        <input type="text" id="title" name="title" maxlength="100" onfocus="global_value=this.value" onkeyup="checkChange(this.value)" onchange="setChange();">
      </div>

      <button type="submit" class="btn-submit">📨 Enviar Ticket</button>
    </form>

<div class="footer" style="text-align:center; font-family: Arial, sans-serif; font-size:14px;">
  <p>Powered by <span style="color:blue; font-weight:bold;">KeepGo</span></p>
</div>

  <script>
    var changes = false;
    var global_value;

    function setChange() {
      changes = true;
    }

    function checkChange(val) {
      if (global_value.length !== val.length) {
        setChange();
        return;
      }
      for (let i = 0; i < global_value.length; i++) {
        if (global_value.charAt(i) !== val.charAt(i)) {
          setChange();
          break;
        }
      }
    }

    function ValidateFrm() {
      const nombre = document.getElementById("firstName").value.trim();
      const apellidos = document.getElementById("lastName").value.trim();
      const telefono = document.getElementById("cellphone").value.trim();
      const titulo = document.getElementById("title").value.trim();

      if (!nombre) {
        alert("Introduzca Nombre");
        document.getElementById("firstName").focus();
        return false;
      }
      if (!apellidos) {
        alert("Introduzca Apellidos");
        document.getElementById("lastName").focus();
        return false;
      }
      if (!telefono) {
        alert("Introduzca Teléfono móvil");
        document.getElementById("cellphone").focus();
        return false;
      }
      if (!titulo) {
        alert("Introduzca un título.");
        document.getElementById("title").focus();
        return false;
      }

      return true;
    }
  </script>

  <!-- Scripts externos de SysAid -->
  <script src="https://stratech.sysaidit.com:443/calendar3.js" type="text/javascript"></script>
  <script src="https://stratech.sysaidit.com:443/webformsubmit?getJS=YES&accountID=stratech&formID=64a1d9ed:1990633a44d:-2a93" type="text/javascript"></script>
