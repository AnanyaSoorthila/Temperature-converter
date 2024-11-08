# Temperature-converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif; 
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        h1 {
            text-align: center;
        }
        .container {
            max-width: 400px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        #result {
            margin-top: 20px;
            font-weight: bold;
            text-align: center;
        }
    </style>
    <script>
        function convertTemperature() {
            const tempInput = parseFloat(document.getElementById("tempInput").value);
            const unit = document.querySelector('input[name="unit"]:checked').value;
            let result;
 if (isNaN(tempInput)) {
                alert("Please enter a valid number.");
                return;
            }
switch (unit) {
                case "Celsius":
                    result = (tempInput * 9/5) + 32 + " °F | " + (tempInput + 273.15) + " K";
                    break;
                case "Fahrenheit":
                    result = (tempInput - 32) * 5/9 + " °C | " + ((tempInput - 32) * 5/9 + 273.15) + " K";
                    break;
                case "Kelvin":
                    result = (tempInput - 273.15) + " °C | " + ((tempInput - 273.15) * 9/5 + 32) + " °F";
                    break;
            }
document.getElementById("result").innerText = "Converted Temperature: " + result;
        }
    </script>
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
