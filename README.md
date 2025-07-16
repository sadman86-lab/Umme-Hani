<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Greeting</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #fef3c7;
            color: #333;
            text-align: center;
            padding: 40px;
        }
        .container {
            background: #fff8dc;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: auto;
        }
        h1 {
            color: #d97706;
            margin-bottom: 10px;
        }
        .creator {
            margin-top: 30px;
            font-size: 14px;
            color: #555;
            font-style: italic;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 id="message"></h1>
        <div class="creator">Created by Humayes Ahmed</div>
    </div>

    <script>
        function getParameterByName(name) {
            const url = window.location.href;
            name = name.replace(/[\[\]]/g, '\\$&');
            const regex = new RegExp('[?&]' + name + '(=([^&#]*)|&|#|$)');
            const results = regex.exec(url);
            if (!results) return null;
            if (!results[2]) return '';
            return decodeURIComponent(results[2].replace(/\+/g, ' '));
        }

        const nama = getParameterByName('nama');
        const messageEl = document.getElementById('message');

        if(nama && nama.trim() !== ""){
            messageEl.textContent = `Congratulations our new platform ${nama} 💞`;
        } else {
            messageEl.textContent = "Welcome! Please provide a name in the URL.";
        }
    </script>
</body>
</html>
