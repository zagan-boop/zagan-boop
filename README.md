<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator Sederhana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 50px;
        }
        .calculator {
            width: 250px;
            background: white;
            padding: 20px;
            margin: auto;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        input {
            width: 90%;
            height: 40px;
            text-align: right;
            font-size: 20px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .btn {
            width: 23%;
            height: 40px;
            margin: 5px;
            font-size: 18px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background: #007bff;
            color: white;
        }
        .btn:hover {
            background: #0056b3;
        }
    </style>
</head>
<body>
    <h2>Kalkulator Sederhana</h2>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <br>
        <button class="btn" onclick="clearDisplay()">C</button>
        <button class="btn" onclick="appendValue('/')">/</button>
        <button class="btn" onclick="appendValue('*')">×</button>
        <button class="btn" onclick="appendValue('-')">-</button>
        <br>
        <button class="btn" onclick="appendValue('7')">7</button>
        <button class="btn" onclick="appendValue('8')">8</button>
        <button class="btn" onclick="appendValue('9')">9</button>
        <button class="btn" onclick="appendValue('+')">+</button>
        <br>
        <button class="btn" onclick="appendValue('4')">4</button>
        <button class="btn" onclick="appendValue('5')">5</button>
        <button class="btn" onclick="appendValue('6')">6</button>
        <button class="btn" onclick="calculate()">=</button>
        <br>
        <button class="btn" onclick="appendValue('1')">1</button>
        <button class="btn" onclick="appendValue('2')">2</button>
        <button class="btn" onclick="appendValue('3')">3</button>
        <br>
        <button class="btn" onclick="appendValue('0')">0</button>
        <button class="btn" onclick="appendValue('.')">.</button>
    </div>

    <script>
        function appendValue(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = "";
        }

        function calculate() {
            try {
                document.getElementById("display").value = eval(document.getElementById("display").value);
            } catch (e) {
                alert("Input tidak valid!");
            }
        }
    </script>
</body>
</html>
