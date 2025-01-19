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
    <title>Fancy Calculator</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #fdf2e9, #d9c4b0);
            color: #5a4635;
        }
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .calculator {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        input[type="number"] {
            padding: 10px;
            font-size: 16px;
            margin-right: 10px;
            width: 200px;
            border: 1px solid #b08a74;
            border-radius: 5px;
            background: #f9f4f0;
        }
        input[type="number"]:focus {
            outline: none;
            border-color: #a4755d;
            box-shadow: 0 0 8px rgba(164, 117, 93, 0.5);
        }
        .result {
            display: inline-block;
            font-size: 18px;
            font-weight: bold;
            margin-top: 10px;
        }
        .footer {
            position: fixed;
            bottom: 10px;
            right: 10px;
            font-size: 12px;
            color: #8b6a52;
        }
        .footer a {
            color: #a4755d;
            text-decoration: none;
        }
        .footer a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="calculator">
            <input type="number" id="inputNumber" placeholder="Enter a number" oninput="calculate()">
            <span class="result" id="result">Result: </span>
        </div>
    </div>
    <div class="footer">made by <a href="https://findouticly.github.io" target="_blank">findouticly</a></div>
    <script>
        function calculate() {
            const input = document.getElementById('inputNumber').value;
            const result = input * 12500;
            document.getElementById('result').textContent = `Result: ${result}`;
        }
    </script>
</body>
</html>
