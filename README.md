 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <label for="celsius">Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter Celsius">
        <button onclick="convertToFar()">Convert</button>
        <p id="result">Result: </p>
    </div>
    <script src="script.js"></script>
</body>
</html>
[10:45, 9/13/2023] ESHAAN: body {
    font-family: Arial, sans-serif;
}

.container {
    max-width: 300px;
    margin: 0 auto;
    text-align: center;
}

button {
    margin-top: 10px;
}

p {
    font-weight: bold;
}
[10:45, 9/13/2023] ESHAAN: function convertToFar() {
    const celsius = parseFloat(document.getElementById("celsius").value);
    if (!isNaN(celsius)) {
        const fahrenheit = (celsius * 9/5) + 32;
        document.getElementById("result").textContent = `Result: ${fahrenheit.toFixed(2)} °F`;
    } else {
        document.getElementById("result").textContent = "Invalid input. Please enter a number.";
    }
}
