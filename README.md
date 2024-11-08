# Temperature-converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <label for="tempInput">Enter Temperature:</label>
        <input type="number" id="tempInput" required>
 <fieldset>
            <legend>Select Unit:</legend>
            <input type="radio" name="unit" value="Celsius" checked>Celsius (°C)<br>
            <input type="radio" name="unit" value="Fahrenheit">Fahrenheit (°F)<br>
            <input type="radio" name="unit" value="Kelvin">Kelvin (K)<br>
        </fieldset>

  <button onclick="convertTemperature()">Convert</button>

   <div id="result">Converted Temperature:</div>
    </div>
</body>
</html>
