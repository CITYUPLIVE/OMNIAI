<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>OMNIA AI – Generator Szczęśliwych Liczb</title>
  <style>
    body {
      background: #0f0f0f;
      color: #ffffff;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      text-align: center;
    }

    h1 {
      font-size: 2.5em;
      color: #00ffcc;
      margin-bottom: 10px;
    }

    p {
      font-size: 1.2em;
      color: #cccccc;
      margin-top: 0;
    }

    .numbers {
      font-size: 2em;
      margin: 30px 0;
      letter-spacing: 15px;
      font-weight: bold;
      color: #ffff66;
    }

    button {
      background: #00ffcc;
      color: #000;
      border: none;
      border-radius: 8px;
      padding: 15px 25px;
      font-size: 1em;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background: #00cc99;
    }
  </style>
</head>
<body>
  <h1>OMNIA AI</h1>
  <p>Twoja przepustka do szczęścia</p>
  <div class="numbers" id="numbers">-- -- -- -- -- --</div>
  <button onclick="generate()">Wylosuj liczby</button>

  <script>
    function generate() {
      let nums = [];
      while (nums.length < 6) {
        let n = Math.floor(Math.random() * 49) + 1;
        if (!nums.includes(n)) nums.push(n);
      }
      document.getElementById("numbers").innerText = nums.join(" ");
    }
  </script>
</body>
</html>
