<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="Content-Language" content="es" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Crear Ticket</title>
  <link rel="stylesheet" href="css/master.css">

  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #2c3e50, #34495e);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .form-container {
      background: #ffffff;
      padding: 40px 30px;
      border-radius: 20px;
      box-shadow: 0px 10px 25px rgba(0,0,0,0.3);
      width: 100%;
      max-width: 550px;
      animation: fadeIn 0.7s ease-in-out;
    }

    h2 {
      text-align: center;
      margin-bottom: 25px;
      color: #2c3e50;
      font-size: 26px;
      font-weight: bold;
    }

    label {
      display: block;
      margin-bottom: 8px;
      font-weight: bold;
      color: #2c3e50;
      font-size: 14px;
    }

    input[type="text"] {
      width: 100%;
      padding: 12px 14px;
      margin-bottom: 18px;
      border: 2px solid #bdc3c7;
      border-radius: 12px;
      font-size: 15px;
      transition: 0.3s;
    }

    input[type="text"]:focus {
      border-color: #2980b9;
      box-shadow: 0px 0px 8px rgba(41,128,185,0.4);
      outline: none;
    }

    .btn-submit {
      width: 100%;
      padding: 15px;
      background: #2980b9;
      color: #fff;
      font-size: 18px;
      font-weight: bold;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: transform 0.2s, background 0.3s;
    }

    .btn-submit:hover {
      background: #1f6391;
      transform: scale(1.03);
    }

    .footer {
      text-align: center;
      font-size: 13px;
      margin-top: 20px;
      color: #555;
    }

    .footer b {
      color: #2980b9;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2>Crear Ticket</h2>

    <form action="https://stratech.sysaidit.com:443/webformsubmit?pageEncoding=utf-8" 
          method="post" name="frm" onsubmit="return ValidateFrm();">

      <!-- CAMPOS OCULTOS DE SYSAID -->
      <input type="hidden" name="X_TOKEN_stratech" value="69487162-e8e9-449a-adc8-d064ca1ed969">
      <input type="hidden" name="accountID" value="stratech">
      <input type="hidden" name="formID" value="64a1d9ed:1990633a44d:-5d6c">
      <input type="hidden" name="reRoute" value="0">
      <input type="hidden" name="parentPageName" value="WebFormHTML.jsp?idx=0">
      <input type="hidden" name="paneMessage" value="">
      <input type="hidden" name="paneType" value="">
      <input type="hidden" name="paneBtnArrayButtons" value="">
      <input type="hidden" name="panePreSubmitFunc" value="">
      <input type="hidden" name="paneTextRow" value="">
      <input type="hidden" name="centerPopup" value="">
      <input type="hidden" name="OK" value="">

      <!-- CAMPOS VISIBLES -->
      <label for="firstName">Nombre *</label>
      <input type="text" id="firstName" name="firstName" maxlength="40" required>

      <label for="lastName">Apellidos *</label>
      <input type="text" id="lastName" name="lastName" maxlength="50" required>

      <label for="cellphone">Teléfono móvil *</label>
      <input type="text" id="cellphone" name="cellphone" maxlength="32" required>

      <label for="title">Título del ticket *</label>
      <input type="text" id="title" name="title" maxlength="100" required>

      <button type="submit" class="btn-submit">🚀 Enviar Ticket</button>
    </form>

    <div class="footer">
      Powered by <b>KeepGo</b>
    </div>
  </div>

  <!-- JS DE SYSAID -->
  <script src="https://stratech.sysaidit.com:443/calendar3.js" type="text/javascript"></script>
  <script src="https://stratech.sysaidit.com:443/webformsubmit?getJS=YES&accountID=stratech&formID=64a1d9ed:1990633a44d:-5d6c" type="text/javascript"></script>

  <!-- VALIDACIÓN -->
  <script>
    function ValidateFrm() {
      const firstName = document.getElementById("firstName").value.trim();
      const lastName = document.getElementById("lastName").value.trim();
      const phone = document.getElementById("cellphone").value.trim();
      const title = document.getElementById("title").value.trim();

      if (!firstName) { alert("Introduzca Nombre"); return false; }
      if (!lastName) { alert("Introduzca Apellidos"); return false; }
      if (!phone) { alert("Introduzca Teléfono móvil"); return false; }
      if (!title) { alert("Introduzca un título para el ticket."); return false; }
      return true;
    }
  </script>

</body>
</html>
