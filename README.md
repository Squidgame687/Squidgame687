<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Squid Game : Le Livre - Téléchargement Gratuit</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 50px; background-color: #f8f8f8; }
        .container { max-width: 500px; margin: auto; background: white; padding: 20px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        .btn { display: inline-block; padding: 10px 20px; background: #d10000; color: white; text-decoration: none; border-radius: 5px; margin-top: 10px; }
        input, button { width: 100%; padding: 10px; margin-top: 10px; }
    </style>
</head>
<body>

    <div class="container">
        <h2>Squid Game : Le Livre</h2>
        <p>Téléchargez gratuitement votre copie en PDF.</p>
        
        <form id="downloadForm">
            <input type="email" id="email" placeholder="Votre email" required>
            <button type="button" onclick="sendDownloadLink()">Recevoir le livre</button>
        </form>

        <p>Ou téléchargez-le directement :</p>
        <a href="https://mon-site.com/squid-game-le-livre.pdf" class="btn" download>Télécharger le livre</a>
    </div>

    <script>
        function sendDownloadLink() {
            var email = document.getElementById("email").value;
            if (!email) {
                alert("Veuillez entrer un email valide.");
                return;
            }

            fetch('send_email.php', {
                method: 'POST',
                headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
                body: 'email=' + encodeURIComponent(email)
            })
            .then(response => response.text())
            .then(result => alert(result))
            .catch(error => alert('Erreur : ' + error));
        }
    </script>

</body>
</html>
