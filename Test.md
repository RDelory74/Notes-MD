# Tests

## Découverte

Selon-vous, qu’est-ce un test ?

	C'est un programme qui va mettre en éxecution toutes les fonctionnalités d'un programme
    afin de s'assure que le build est prêt pour le deployement ou la mise en prod. 

À quoi servent les tests ?

    Bha justement cela permet d'automatiser l'esseayge des fonctionnalité et de leur robustesse. 

Y a-t-il plusieurs types de tests ? Si oui, quelle est leur différence ?

    Oui je pense qu'il y a plusieurs type de tests, après je ne les connais pas, 

    - Test unitaire (test une fonction) une seule chose( un composant, une méthode)
    - Test foncitonnel (tester une fonctionnalité complète type tester le panier.)
    - Test d'integration (n to n) on simuler le comportement de l'utilisateur.
    - Test de sécurité, on vérifie l'isolation 
    - Test charge. Augmentation du traffic on regarde si ça tiens.

Intuitivement, à quelles bonnes pratiques de conception de tests, vous pouvez penser ?

    Il faut que la portée du test soit adapté à ce pourquoi il est conçu pour. 

À l’inverse, et toujours sans vous aider d’internet, qu’est-ce qui pourrait être une mauvaise pratique de conception de test ?

    Il faut que la portée du test soit adapté à ce pourquoi il est conçu pour. 

Définir ce qu’est le TDD et quels sont les avantages de cette pratique.

      Test 
      Driven 
      Developpement

    Test pour développer, on créé des tests pour s'assurer que son code est bon. 

## Cahier des test (Hangman)


Nom du test : Le titre qui décrit la fonctionnalité à tester.

ID du test : Généralement un identifiant numérique ou alphanumérique que les testeurs utilisent pour regrouper les cas de test en suites de test.

Objectif : Également appelé description, ce composant décrit ce que le test doit valider.

Références : Liens vers vos « user stories » et les spécifications de conception ou les exigences que le test doit vérifier.

Conditions préalables : Toutes les conditions nécessaires pour que le testeur puisse effectuer le test.

Configurations : Ce composant identifie ce dont le scénario de test a besoin pour fonctionner correctement, comme la version
de l'application, le système d'exploitation, les exigences en matière de date et d'heure et les spécifications de sécurité.

Étapes de test : Des descriptions détaillées des actions séquentielles qui doivent être effectuées pour terminer le test.

Résultat attendu : Une explication de la manière dont la fonctionnalité ou le système doit réagir.

    Arrange : on initialise les variables nécessaires
    Act : on exécute la ou les fonctions à tester
    Assert : on teste le résultat attendu avec le résultat obtenu

Identifier les méthodes que l'on va tester :

    0.  Nom : Méthode displayedWord - Teste le bon affichage du mot à deviner en fonction des lettres trouvées
    ID : T1
    Objectif : Tester le bon affichage du mot à deviner en fonction des lettres trouvées
    Étapes de test : 
        - Instanciation d'un jeu du pendu avec comme mot à deviner `bonjour` et avec comme scénario le fait d'avoir déjà trouvé la lettre `b`
    Résultat attendu :
        - Le mot affiché devrait être `b _ _ _ _ _ _`

    1. displayLetters() // On test l'affichage des lettres au lancement de la page //
    Id: T2
    Objectif: On vérifie qu'au lancement de la page chaque button comporte bien une lettre et que le nombre de boutons est de 26 ("lenght alphabet")
    Etapes de test :
        - Instanciation de Hangman avec vérification du nombre de lettre puis du contenu de chaque boutons
    Resultats attendu : 
        - La collection d'Elements de boutons doit être de 26 elements, puis que chaque index de button depuis le la colleciton de buttons doit être une lettre de l'alphabet

    2. handleKeyPress() // On test que lorsque un bouton de lettre de A à Z est appuyé la méthode handleGuess est lancée
    ID: T3 
    Objectif: On test que lorsque un bouton est appuyé la méthode handleGuess est lancée
    Etapes de test: 
        - Instanciation de Hangman, vérification que l'entrée d'une lettre sur le clavier est bien transmise à la méthode handleGuess en paramètre. 
    Resulats attendu :
        - Que la méthode handleGuess soit exécuté avec le bon argument.


    3. handleGuess(letter)
    ID: T4
    Objectif: On vérifie qu'avec un scénario ou la bonne lettre est choisie les méthodes displayWord et checkWin soient lancés.
    Etapes de test: 
        - Instanciation de hangman. avec comme variable word: "weapon" et comme letter: "a" 
    Resultat attendu: 
        - Que si la variable word inclus la variable letter en paramètre alors on run displayWord et checkWin


    4. checkWin()
    ID: T5
    Objectif: On vérifie avec un scénario ou displayedWord is full (n'inclus pas de "_") on désactive tous les boutons 
    Etapes de test: 
        - Instanciation de hangman on simule un word et on entre dans guesseLetter les lettres associées alors checkWin() fait son job et disableAllButtons() est appellée
    Resultat attendu: 
        - la methode disableAllButtons() est appellée.


    5. checkLose()
    ID: T6
    Objectif: On vérifie avec un scénario ou l nbr d'essais est plus grand que le nombre d'essai max afin que la méthode checkLose assign bien le message suivant à la variable messageElement.textContent = `You Lose! The word was "${this.word}".` et que la méthode disableAllButtons est appellée. 
    Etapes de test: 
        - Instanciation de hangman, je simule un nombre d'attemps qui est + elevé que le maxAttempts et je lance checkLose;
    Resultat attendu: 
        - messageElement.textContent se voit assigné le mess `You Lose! The word was "${this.word}".` et disableAllButtons est appellée.


    6. disableallButtons()


import { describe, it, expect } from 'vitest'

describe("Méthode displayedWord", () => {
    it("Teste le bon affichage du mot à deviner en fonction des lettres trouvées", () => {
        const hangman = new Hangman({ word: "bonjour", guessedLetters: ["b"]})
        expect(hangman.displayedWord()).toBe("b _ _ _ _ _ _")
    })
})

### Ressources 

https://2023.stateofjs.com/en-US
