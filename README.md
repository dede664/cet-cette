# cet-cette
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice - cet vs cette</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        .correct {
            color: green;
        }

        .incorrect {
            color: red;
        }

        .analyse {
            color: blue;
        }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["cet", "cette", "cet", "cette", "cet", "cette", "cet", "cette", "cet", "cette",
                                     "cet", "cette", "cet", "cette", "cet", "cette", "cet", "cette", "cet", "cette"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));
                let analyse = document.getElementById('analyse' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct";
                    analyse.innerText = "";
                    score++;
                } else {
                    feedback.innerText = "❌ Incorrect";
                    feedback.className = "incorrect";
                    analyse.innerText = `La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "cet" est utilisé devant un nom masculin commençant par une voyelle ou un "h" muet (ex : cet arbre, cet homme), tandis que "cette" est utilisé devant un nom féminin (ex : cette voiture).`;
                    analyse.className = "analyse";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>

<body>
    <h2>Règle : "cet" vs "cette"</h2>
    <p>
        - <b>"cet"</b> est un déterminant démonstratif utilisé devant un nom masculin commençant par une voyelle ou un "h" muet. Exemple : "Cet arbre est magnifique".<br>
        - <b>"cette"</b> est un déterminant démonstratif utilisé devant un nom féminin. Exemple : "Cette voiture est rouge".
    </p>

    <h2>Exercice - Complétez avec "cet" ou "cette"</h2>

    <!-- Génération des 20 questions -->
    <div id="exercices">
        <p>1. ___ homme est très gentil.</p>
        <input type="text" id="reponse1"> <span id="feedback1"></span><br>
        <p id="analyse1"></p><br>

        <p>2. ___ fleur est magnifique.</p>
        <input type="text" id="reponse2"> <span id="feedback2"></span><br>
        <p id="analyse2"></p><br>

        <p>3. ___ arbre pousse très vite.</p>
        <input type="text" id="reponse3"> <span id="feedback3"></span><br>
        <p id="analyse3"></p><br>

        <p>4. ___ maison est en construction.</p>
        <input type="text" id="reponse4"> <span id="feedback4"></span><br>
        <p id="analyse4"></p><br>

        <p>5. ___ enfant est très doué.</p>
        <input type="text" id="reponse5"> <span id="feedback5"></span><br>
        <p id="analyse5"></p><br>

        <p>6. ___ idée est brillante.</p>
        <input type="text" id="reponse6"> <span id="feedback6"></span><br>
        <p id="analyse6"></p><br>

        <p>7. ___ hôtel est très luxueux.</p>
        <input type="text" id="reponse7"> <span id="feedback7"></span><br>
        <p id="analyse7"></p><br>

        <p>8. ___ rivière est dangereuse en hiver.</p>
        <input type="text" id="reponse8"> <span id="feedback8"></span><br>
        <p id="analyse8"></p><br>

        <p>9. ___ avion est prêt à décoller.</p>
        <input type="text" id="reponse9"> <span id="feedback9"></span><br>
        <p id="analyse9"></p><br>

        <p>10. ___ route est bloquée à cause des travaux.</p>
        <input type="text" id="reponse10"> <span id="feedback10"></span><br>
        <p id="analyse10"></p><br>

        <p>11. ___ homme est célèbre.</p>
        <input type="text" id="reponse11"> <span id="feedback11"></span><br>
        <p id="analyse11"></p><br>

        <p>12. ___ école est fermée aujourd'hui.</p>
        <input type="text" id="reponse12"> <span id="feedback12"></span><br>
        <p id="analyse12"></p><br>

        <p>13. ___ ordinateur est en panne.</p>
        <input type="text" id="reponse13"> <span id="feedback13"></span><br>
        <p id="analyse13"></p><br>

        <p>14. ___ table est très ancienne.</p>
        <input type="text" id="reponse14"> <span id="feedback14"></span><br>
        <p id="analyse14"></p><br>

        <p>15. ___ animal est blessé.</p>
        <input type="text" id="reponse15"> <span id="feedback15"></span><br>
        <p id="analyse15"></p><br>

        <p>16. ___ porte est fermée.</p>
        <input type="text" id="reponse16"> <span id="feedback16"></span><br>
        <p id="analyse16"></p><br>

        <p>17. ___ éléphant est énorme.</p>
        <input type="text" id="reponse17"> <span id="feedback17"></span><br>
        <p id="analyse17"></p><br>

        <p>18. ___ fenêtre est ouverte.</p>
        <input type="text" id="reponse18"> <span id="feedback18"></span><br>
        <p id="analyse18"></p><br>

        <p>19. ___ accident est survenu hier.</p>
        <input type="text" id="reponse19"> <span id="feedback19"></span><br>
        <p id="analyse19"></p><br>

        <p>20. ___ chanson est ma préférée.</p>
        <input type="text" id="reponse20"> <span id="feedback20"></span><br>
        <p id="analyse20"></p><br>
    </div>

    <button onclick="verifier()">Vérifier</button>
    <p id="score"></p>
</body>

</html>
