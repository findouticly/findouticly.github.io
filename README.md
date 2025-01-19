# Single Input Calculator

This is a simple HTML calculator that allows the user to input a single number. The entered number is multiplied by 12,500, and the result is displayed immediately.

## Usage

To use this calculator, simply input a number into the text field. The result will be displayed dynamically as you type.

### Code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 100px;
        }
        .calculator {
            display: inline-block;
            margin: auto;
        }
        input[type="number"] {
            padding: 10px;
            font-size: 16px;
            margin-right: 10px;
            width: 200px;
        }
        .result {
            display: inline-block;
            font-size: 16px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="number" id="inputNumber" placeholder="Enter a number" oninput="calculate()">
        <span class="result" id="result">Result: </span>
    </div>
    <script>
        function calculate() {
            const input = document.getElementById('inputNumber').value;
            const result = input * 12500;
            document.getElementById('result').textContent = `Result: ${result}`;
        }
    </script>
</body>
</html>
