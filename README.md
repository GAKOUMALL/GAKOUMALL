<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Joyeux Anniversaire Gakou Ousmane !</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="container">
        <h1>🎉 Joyeux Anniversaire Gakou Ousmane ! 🎉</h1>
        <p>Aujourd'hui, nous célébrons un jeune entrepreneur inspirant, fondateur de <strong>GAKOU MALL</strong> !</p>
        <p>Que cette journée soit remplie de bonheur, de succès et de nouvelles opportunités ! 🚀</p>
        <button onclick="showSurprise()">Clique ici pour une surprise 🎁</button>
        <p id="surprise-message" style="display: none;">✨ GAKOU MALL offre une réduction spéciale aujourd'hui ! Profitez-en ! ✨</p>
    </div>

    <script src="script.js"></script>

</body>
</html><!D                                                                                                                                                                                                                                                                                                                                                                            body {
    font-family: Arial, sans-serif;
    text-align: center;
    background: linear-gradient(45deg, #ff9a9e, #fad0c4);
    color: white;
    margin: 0;
    padding: 0;
}

.container {
    margin-top: 20vh;
}

h1 {
    font-size: 2.5em;
    animation: glow 1.5s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px white; }
    to { text-shadow: 0 0 20px yellow; }
}

button {
    background: #ffcc00;
    border: none;
    padding: 15px 25px;
    font-size: 1.2em;
    cursor: pointer;
    margin-top: 20px;
    border-radius: 5px;
}

button:hover {
    background: #ff9900;
}

#surprise-message {
    font-size: 1.5em;
    margin-top: 20px;
    font-weight: bold;
}                                                                                                                                                                                         function showSurprise() {
    document.getElementById("surprise-message").style.display = "block";
}                                                                                                                                                                                                                                                                                                                                           
