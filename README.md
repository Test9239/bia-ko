<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pomoc dla studenta</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f5f5f5;
            padding: 50px;
        }

        h1 {
            color: #333;
        }

        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            margin: 0 auto;
        }

        img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin-top: 20px;
        }

        .buttons {
            margin-top: 20px;
        }

        .buttons button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #4CAF50;
            color: white;
            transition: background-color 0.3s;
        }

        .buttons button:hover {
            background-color: #45a049;
        }

        .response {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: #333;
        }

        .response.missclick {
            color: #ff5722;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Biedny student nie ma na białko, czy go wspomożesz?</h1>
        <img src="./bialko-kfd-premium-wpc-82-700g-naturalne-b-iext120926577.webp" alt="Białko">
        
        <div class="buttons">
            <button id="yesBtn">Tak</button>
            <button id="noBtn">Nie</button>
        </div>

        <div id="response" class="response"></div>
    </div>

    <script>
        const yesBtn = document.getElementById("yesBtn");
        const noBtn = document.getElementById("noBtn");
        const response = document.getElementById("response");

        yesBtn.addEventListener("click", function() {
            response.textContent = "Dziękuję, doliczam do rachunku :*";
            response.classList.remove("missclick");
        });

        noBtn.addEventListener("click", function() {
            response.textContent = "Na pewno to missclick!";
            response.classList.add("missclick");
            setTimeout(function() {
                response.textContent = "Możesz naprawić błąd i kliknąć tylko opcję 'Tak'.";
                response.classList.remove("missclick");
            }, 3000);
        });
    </script>

</body>
</html>
