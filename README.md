# random-number
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Number Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }

        .container {
            text-align: center;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            margin-bottom: 20px;
        }

        .random-number {
            font-size: 24px;
            color: #333;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Random Number Generator</h1>
    <div class="random-number">
        <script>
            // JavaScript code to generate and display a random number between 1 and 100
            document.write(Math.floor(Math.random() * 100) + 1);
        </script>
    </div>
</div>

</body>
</html>
