<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gakou Ousmane - Entrepreneur & Visionnaire</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1 contenteditable="true" class="editable">Gakou Ousmane</h1>
        <button id="editButton">Modifier</button>
        <button id="saveButton">Sauvegarder</button>
    </header>

    <section id="accueil">
        <h2>Bienvenue</h2>
        <p contenteditable="true" class="editable">
            Je suis Gakou Ousmane, entrepreneur ivoirien, passionné de business et de technologie.
        </p>
    </section>

    <section id="biographie">
        <h2>Biographie</h2>
        <p contenteditable="true" class="editable">
            Je suis né le <strong>14 mars 2009</strong> à <strong>Abidjan</strong>, dans la commune d’<strong>Adjamé</strong>.
        </p>
    </section>

    <section id="gakou-mall">
        <h2>GAKOU MALL</h2>
        <p contenteditable="true" class="editable">
            J’ai fondé <strong>GAKOU MALL</strong>, une plateforme de vente de chaussures, vêtements, montres et bijoux.
        </p>
    </section>

    <footer>
        <p>© 2025 Gakou Ousmane - Tous droits réservés</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
}

button {
    margin: 10px;
    padding: 10px;
    border: none;
    background-color: #28a745;
    color: white;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

section {
    padding: 20px;
    background: white;
    margin: 10px;
    border-radius: 10px;
}

footer {
    background-color: #333;
    color: white;
    padding: 10px;
    margin-top: 20px;
}
document.getElementById('editButton').addEventListener('click', function() {
    document.querySelectorAll('.editable').forEach(el => el.setAttribute('contenteditable', 'true'));
    alert("Mode édition activé ! Vous pouvez modifier le texte.");
});

document.getElementById('saveButton').addEventListener('click', function() {
    let content = {};
    document.querySelectorAll('.editable').forEach((el, index) => {
        content[index] = el.innerHTML;
    });
    localStorage.setItem('savedContent', JSON.stringify(content));
    alert("Modifications sauvegardées !");
});

window.onload = function() {
    let savedContent = localStorage.getItem('savedContent');
    if (savedContent) {
        savedContent = JSON.parse(savedContent);
        document.querySelectorAll('.editable').forEach((el, index) => {
            if (savedContent[index]) el.innerHTML = savedContent[index];
        });
    }
};
