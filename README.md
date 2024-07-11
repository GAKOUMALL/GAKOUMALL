<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sondage Gakou Mall</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Sondage Gakou Mall</h1>
    </header>
    <main>
        <section class="survey">
            <h2>Participez à notre sondage</h2>
            <form id="surveyForm">
                <div class="question">
                    <label for="q1">Question 1 : Connaissez-vous Gakou Mall ?</label>
                    <select id="q1" name="q1">
                        <option value="oui">Oui</option>
                        <option value="non">Non</option>
                    </select>
                </div>
                <div class="question">
                    <label for="q2">Question 2 : Quel âge avez-vous ?</label>
                    <select id="q2" name="q2">
                        <option value="18-29">18-29</option>
                        <option value="30-39">30-39</option>
                        <option value="40-49">40-49</option>
                        <option value="50+">50+</option>
                    </select>
                </div>
                <div class="question">
                    <label for="q3">Question 3 : Que pensez-vous de Gakou Mall ?</label>
                    <select id="q3" name="q3">
                        <option value="très bien">Très bien</option>
                        <option value="incroyable">Incroyable</option>
                        <option value="d'accord">D'accord</option>
                        <option value="pas si bon">Pas si bon</option>
                    </select>
                </div>
                <div class="question">
                    <label for="comments">Commentaires :</label>
                    <textarea id="comments" name="comments" rows="4" cols="50"></textarea>
                </div>
                <button type="submit">Soumettre</button>
            </form>
        </section>
        <section class="comments">
            <h3>Commentaires</h3>
            <div class="comment" id="commentSection">
                <!-- Les commentaires soumis apparaîtront ici -->
            </div>
        </section>
    </main>
    <script src="scripts.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f7f7f7;
}

header {
    background-color: #E4002B;
    color: white;
    text-align: center;
    padding: 1em 0;
}

main {
    padding: 2em;
    max-width: 800px;
    margin: 0 auto;
    background-color: white;
}

.survey {
    margin-bottom: 2em;
}

.survey h2 {
    text-align: center;
}

.question {
    margin-bottom: 1em;
}

.question label {
    font-weight: bold;
}

.question select, .question textarea {
    width: 100%;
    padding: 0.5em;
    margin-top: 0.5em;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    display: block;
    width: 100%;
    padding: 0.5em;
    background-color: #E4002B;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    margin-top: 1em;
}

button:hover {
    background-color: #b30022;
}

.comments {
    margin-top: 2em;
}

.comments h3 {
    font-weight: bold;
}

.comment {
    margin-bottom: 1em;
}

.comment p {
    margin: 0.5em 0;
}

.comment strong {
    font-weight: bold;
}
document.getElementById('surveyForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const q1 = document.getElementById('q1').value;
    const q2 = document.getElementById('q2').value;
    const q3 = document.getElementById('q3').value;
    const comments = document.getElementById('comments').value;

    const commentSection = document.getElementById('commentSection');

    const newComment = document.createElement('div');
    newComment.classList.add('comment');

    newComment.innerHTML = `
        <p><strong>Réponse au sondage</strong></p>
        <p>Connaissez-vous Gakou Mall ? ${q1}</p>
        <p>Âge : ${q2}</p>
        <p>Avis sur Gakou Mall : ${q3}</p>
        <p>Commentaire : ${comments}</p>
    `;

    commentSection.appendChild(newComment);

    document.getElementById('surveyForm').reset();
});
