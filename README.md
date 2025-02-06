echo "# Marcos" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/tranferencia/Marcos.git
git push -u origin main
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Datos de Transferencia</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      text-align: center;
      width: 300px;
    }

    h1 {
      font-size: 24px;
      margin-bottom: 20px;
    }

    .account-info {
      font-size: 18px;
      margin-bottom: 20px;
      background-color: #f1f1f1;
      padding: 10px;
      border-radius: 4px;
    }

    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #45a049;
    }

    .copy-success {
      display: none;
      color: green;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Detalles de Transferencia</h1>
    <div class="account-info" id="account-info">
      Cuenta: <strong>123-456-7890</strong><br>
      Banco: <strong>Banco Ejemplo</strong><br>
      Nombre: <strong>Juan Pérez</strong><br>
    </div>
    <button onclick="copyToClipboard()">Copiar Datos</button>
    <p id="copy-success" class="copy-success">¡Datos copiados con éxito!</p>
  </div>

  <script>
    function copyToClipboard() {
      const accountInfo = document.getElementById("account-info").innerText;
      const textarea = document.createElement("textarea");
      textarea.value = accountInfo;
      document.body.appendChild(textarea);
      textarea.select();
      document.execCommand("copy");
      document.body.removeChild(textarea);

      const successMessage = document.getElementById("copy-success");
      successMessage.style.display = "block";
      setTimeout(() => {
        successMessage.style.display = "none";
      }, 2000);
    }
  </script>

</body>
</html>
