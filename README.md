# my-website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lilly the Virtual Flower Pot</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            background-color: #f0fdf4;
            color: #2d3748;
            padding: 50px;
        }
        .pot-container {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.05);
            display: inline-block;
        }
        .flower {
            font-size: 80px;
            margin: 20px 0;
            transition: transform 0.3s ease;
        }
        .status {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 20px;
        }
        button {
            background-color: #3b82f6;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1rem;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.2s;
        }
        button:hover {
            background-color: #2563eb;
        }
    </style>
</head>
<body>

    <div class="pot-container">
        <h1>Lilly 🌸</h1>
        <div class="flower" id="flower-emoji">🌸</div>
        <div class="status" id="hydration-status">Lilly is 40% hydrated</div>
        <button onclick="waterLilly()">💧 Water Lilly</button>
    </div>

    <script>
        // Track Lilly's starting hydration level
        let hydration = 40;

        function waterLilly() {
            // Increase hydration by 10, capped at 100%
            if (hydration < 100) {
                hydration += 10;
            }
            
            // Update the text on the screen
            document.getElementById("hydration-status").innerText = `Lilly is ${hydration}% hydrated`;
            
            // Add a little bounce effect when watered
            const flower = document.getElementById("flower-emoji");
            flower.style.transform = "scale(1.2)";
            setTimeout(() => flower.style.transform = "scale(1)", 300);
        }
    </script>

</body>
</html>


