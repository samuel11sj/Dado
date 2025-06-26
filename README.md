<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Simulador de Dados</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Simulador de Dados</h1>
  <button onclick="girarDados()">Girar Dados</button>
  
  <div class="resultado">
    <p>D6: <span id="d6">-</span></p>
    <p>D8: <span id="d8">-</span></p>
    <p>D20: <span id="d20">-</span></p>
  </div>

  <script>
    function girarDados() {
      const d6 = Math.floor(Math.random() * 6) + 1;
      const d8 = Math.floor(Math.random() * 8) + 1;
      const d20 = Math.floor(Math.random() * 20) + 1;

      document.getElementById('d6').textContent = d6;
      document.getElementById('d8').textContent = d8;
      document.getElementById('d20').textContent = d20;
    }
  </script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 50px;
  background-color: #f0f0f0;
}

button {
  padding: 10px 20px;
  font-size: 18px;
  cursor: pointer;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 8px;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #45a049;
}

.resultado {
  margin-top: 30px;
  font-size: 24px;
  color: #333;
}
