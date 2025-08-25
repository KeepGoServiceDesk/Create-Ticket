<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="Content-Language" content="es" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Crear Ticket</title>
  <link rel="stylesheet" href="css/master.css">

  <!-- Estilos modernos -->
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

    <form action="https://stratech.sysaidit.com:443/webformsubmit?pageEncoding=utf-8" method="post" name="frm" onsubmit="return ValidateFrm();">
      <!-- Campos ocultos -->
      <input type="hidden" name="X_TOKEN_stratech" value="a7687a9f-5934-4e36-a1d4-08ea7f4083cb">
      <input type="hidden" name="accountID" value="stratech">
      <input type="hidden" name="formID" value="55039d52:198e2dee0de:38fe">
      <input type="hidden" name="reRoute" value="0">
      <input type="hidden" name="OK" value="">

      <!-- Campos visibles -->
      <label for="firstName">Nombre</label>
      <input type="text" id="firstName" name="firstName" maxlength="40">

      <label for="lastName">Apellidos</label>
      <input type="text" id="lastName" name="lastName" maxlength="50">

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

  <!-- Validación -->
  <script>
    function ValidateFrm() {
      const phone = document.getElementById("cellphone").value.trim();
      const title = document.getElementById("title").value.trim();

      if (phone.length === 0) {
        alert("Introduzca Teléfono móvil");
        return false;
      }
      if (title.length === 0) {
        alert("Introduzca un título para el ticket.");
        return false;
      }
      return true;
    }
  </script>

</body>
</html>
