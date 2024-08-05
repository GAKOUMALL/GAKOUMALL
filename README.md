<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Ferme</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <img src="OIG4.jpeg" alt="Une image d'un lapin et d'une poule"
    style="width: 150;" height="150">
  <a href="#A propos de La Ferme">A propos de La Ferme</a>
  <a href="#Boutique">Boutique</a>
  <a href="#Contacts">Contacts</a>
</header>
  <main>
    <section id="A propos de La Ferme" class="container">
        <h2>A propos de La Ferme</h2>
        <p>Bienvenue à La Ferme, située à Adjamé-Bingerville. Depuis sa création, nous élevons des lapins et des poulets de haute qualité.
        <ul>
            <br><li><strong>Notre Mission</strong></li>
        </ul>
           <br> Offrir des produits d'élevage sains tout en respectant l'environnement et le bien-être animal.
    </section>

    <section id="Boutique" class="container">
        <h2>Boutique</h2>
        <div>
        <img src="OIP.jpeg" alt="Photo de lapin">
        <button id="buybutton">Acheter</button>
        <img src="R.jpeg" alt="Photo  dee lapin"> 
        <button id="buybutton">Acheter</button>
        <img src="télécharger.jpeg" alt="Photo  dee lapin">
        <button id="buybutton">Acheter</button>
        <hr><img src="OIP (1).jpeg" alt="Photo de poulet">
        <button id="buybutton">Acheter</button>
        <img src="OIP (2).jpeg" alt="Photo de poulet">
        <button id="buybutton">Acheter</button>
        <img src="télécharger (1).jpeg" alt="Photo de poulet">
        <button id="buybutton">Acheter</button>
    </div>
    <script>
        // Sélectionner le bouton
        const button = document.getElementById('buybutton');

        // Ajouter un événement de clic au bouton
        button.addEventListener('click', function() {
            // Rediriger vers un site externe
            window.location.href = 'https://linktr.ee/gakoumall';
        });
    </script>
    </section>

    <section id="Contacts" class="container">
        <h2>Contacts</h2>
        p
    </section>
  </main>
</body>
</html>
