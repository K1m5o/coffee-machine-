<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Coffee Dispenser</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f4f1ee;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem;
    }



    
    h1 {
      color: #5b3c11;
    }
    .button {
      padding: 1rem 2rem;
      margin: 0.5rem;
      font-size: 1.1rem;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      background-color: #6f4e37;
      color: white;
      transition: background 0.3s ease;
    }
    .button:hover {
      background-color: #56371e;
    }
    #output {
      margin-top: 2rem;
      font-size: 1.2rem;
      color: #333;
    }
  </style>
</head>
<body>

  <h1>☕ JavaScript Coffee Dispenser</h1>

  <button class="button" onclick="dispenseCoffee('Espresso')">Espresso</button>
  <button class="button" onclick="dispenseCoffee('Latte')">Latte</button>
  <button class="button" onclick="dispenseCoffee('Cappuccino')">Cappuccino</button>

  <div id="output"></div>

  <script>
    const coffeeCounts = {
      Espresso: 0,
      Latte: 0,
      Cappuccino: 0
    };

    function dispenseCoffee(type) {
      coffeeCounts[type]++;
      const output = `
        You made a ${type}!<br><br>
        <strong>Total dispensed:</strong><br>
        Espresso: ${coffeeCounts.Espresso}<br>
        Latte: ${coffeeCounts.Latte}<br>
        Cappuccino: ${coffeeCounts.Cappuccino}
      `;
      document.getElementById("output").innerHTML = output;
    }
  </script>

</body>
</html># coffee-machine-
