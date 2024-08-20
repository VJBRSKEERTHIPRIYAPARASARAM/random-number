<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Random Number Generator</title>
    <style>
        body {
            font-family: 'Verdana', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #e0f7fa;
            margin: 0;
        }

        .container {
            text-align: center;
            padding: 40px;
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        h1 {
            margin-bottom: 20px;
            color: #00796b;
        }

        .random-number {
            font-size: 45px;
            font-weight: bold;
            color: #00796b;
            padding: 10px;
            border: 2px solid #00796b;
            border-radius: 8px;
            margin-top: 20px;
            display: inline-block;
        }

        input {
            padding: 10px;
            margin: 10px;
            font-size: 16px;
            border-radius: 8px;
            border: 2px solid #00796b;
            text-align: center;
            color: #00796b;
        }

        button {
            padding: 12px 24px;
            font-size: 18px;
            color: white;
            background-color: #00796b;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 20px;
        }

        button:hover {
            background-color: #004d40;
        }
    </style>
</head>

<body>

    <div class="container">
        <h1>Random Number Generator</h1>
        <form onsubmit="generateRandomNumber(event)">
            <input type="number" id="min" placeholder="Min number" required>
            <input type="number" id="max" placeholder="Max number" required>
            <br>
            <button type="submit">Generate</button>
        </form>
        <div class="random-number" id="random-number"></div>
    </div>

    <script>
        function generateRandomNumber(event) {
            event.preventDefault(); 
            const min = parseInt(document.getElementById('min').value);
            const max = parseInt(document.getElementById('max').value);

            if (min > max) {
                alert('Min number should be less than or equal to Max number');
                return;
            }

            const randomNumber = Math.floor(Math.random() * (max - min + 1)) + min;
            document.getElementById('random-number').textContent = randomNumber;
        }
    </script>

</body>

</html>
