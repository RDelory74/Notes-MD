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

    1. displayLetters() // On test l'affichage des lettres au lancement de la page //

    import describe from vitest

        Arrange : 

       Jquery            lettersElement = 
       String Array      alphabet =
       Html Element      button =
       Array             guessedLetters =

        Act : 

        it return the correct letters button in the good range


        Assert : 

        expect (result) to contain letters from word from Json

    2. handleKeyPress()
    3. handleGuess(letter)
    4. checkWin()
    5. checkLose()
    6. disableallButtons()




### Ressources 

https://2023.stateofjs.com/en-US
