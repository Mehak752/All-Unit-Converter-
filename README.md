<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="<meta name="google-site-verification" content="XM662OW-qKfi8L5Sh6SsuoP5B-ac5Q6GvY6Eey_TbYU" />" content="width=device-width, initial-scale=1.0" />
  <title>All-in-One Unit Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f9f9f9;
      margin: 0;
      padding: 20px;
      color: #333;
    }
    h1 {
      text-align: center;
      color: #444;
    }
    .converter {
      background: #fff;
      max-width: 500px;
      margin: 20px auto;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }
    .converter h2 {
      font-size: 20px;
      margin-bottom: 10px;
    }
    .input-group {
      display: flex;
      margin-bottom: 10px;
    }
    .input-group input {
      flex: 1;
      padding: 10px;
      margin-right: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    .input-group button {
      padding: 10px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
    .result {
      font-weight: bold;
      margin-top: 5px;
    }
  </style>
</head>
<body>
  <h1>All-in-One Unit Converter</h1>

  <div class="converter">
    <h2>Centimeter to Inch</h2>
    <div class="input-group">
      <input id="cmInput" type="number" placeholder="Enter cm" />
      <button onclick="convertCMtoInch()">Convert</button>
    </div>
    <p class="result" id="cmResult"></p>
  </div>

  <div class="converter">
    <h2>Kilogram to Pound</h2>
    <div class="input-group">
      <input id="kgInput" type="number" placeholder="Enter kg" />
      <button onclick="convertKGtoLB()">Convert</button>
    </div>
    <p class="result" id="kgResult"></p>
  </div>

  <div class="converter">
    <h2>Celsius to Fahrenheit</h2>
    <div class="input-group">
      <input id="celsiusInput" type="number" placeholder="Enter °C" />
      <button onclick="convertCtoF()">Convert</button>
    </div>
    <p class="result" id="celsiusResult"></p>
  </div>

  <div class="converter">
    <h2>Meters to Feet</h2>
    <div class="input-group">
      <input id="meterInput" type="number" placeholder="Enter m" />
      <button onclick="convertMtoFt()">Convert</button>
    </div>
    <p class="result" id="meterResult"></p>
  </div>

  <div class="converter">
    <h2>Grams to Ounces</h2>
    <div class="input-group">
      <input id="gramInput" type="number" placeholder="Enter g" />
      <button onclick="convertGtoOz()">Convert</button>
    </div>
    <p class="result" id="gramResult"></p>
  </div>

  <script>
    function convertCMtoInch() {
      const cm = parseFloat(document.getElementById('cmInput').value);
      const inch = cm / 2.54;
      document.getElementById('cmResult').innerText = `${cm} cm = ${inch.toFixed(2)} inches`;
    }

    function convertKGtoLB() {
      const kg = parseFloat(document.getElementById('kgInput').value);
      const lb = kg * 2.20462;
      document.getElementById('kgResult').innerText = `${kg} kg = ${lb.toFixed(2)} lbs`;
    }

    function convertCtoF() {
      const c = parseFloat(document.getElementById('celsiusInput').value);
      const f = (c * 9/5) + 32;
      document.getElementById('celsiusResult').innerText = `${c}°C = ${f.toFixed(2)}°F`;
    }

    function convertMtoFt() {
      const m = parseFloat(document.getElementById('meterInput').value);
      const ft = m * 3.28084;
      document.getElementById('meterResult').innerText = `${m} m = ${ft.toFixed(2)} ft`;
    }

    function convertGtoOz() {
      const g = parseFloat(document.getElementById('gramInput').value);
      const oz = g * 0.035274;
      document.getElementById('gramResult').innerText = `${g} g = ${oz.toFixed(2)} oz`;
    }
  </script>
</body>
</html>
