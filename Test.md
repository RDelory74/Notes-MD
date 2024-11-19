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

## Github Action 

Definition google: 

GitHub Actions est une plateforme d'intégration continue et livraison continue (CI/CD)
 qui vous permet d'automatiser votre pipeline de génération, de test et de déploiement.

### les étapes: 

    1. Créer un dossier workflows dans le dossier (caché) .github 
    2. puis dans ce dossier créer un fichier tests.yml 
    3. Configurer son dossier de test (voir exemple ci-dessous à réadapter en fonction des besoins): 
       1. name: Run Tests

            on:
              push:
                branches: [ main, master ]  # s'exécute sur push vers main ou master
              pull_request:
                branches: [ main, master ]  # s'exécute aussi sur les PR vers main ou master

            jobs:
              test:
                runs-on: ubuntu-latest

                steps:
                  - uses: actions/checkout@v3  # récupère le code du repo

                  - name: Set up Node.js
                    uses: actions/setup-node@v3
                    with:
                      node-version: '20'  # utilise Node.js 20.x

                  - name: Install dependencies
                    run: npm ci  # installe les dépendances

                  - name: Run tests
                    run: npm test  # exécute les tests

    4. Puis git add, git commit et git push 
    5. Enfin il est possible de retrouver ses Github Actions dans l'onglet Actions du projet


## Les test END-to-END (E2E)

Les test End-toEnd sont des test qui vont simuler toute une application entière sur l'ensemble des story possible. 
Très efficace et permettant d'identifier les points critiques users (les plus impactants)
                Tester l'application dans son ensemble
                Vérifier l'intégration de tous les composants
                S'assurer que les flux utilisateurs fonctionnent correctement
                Détecter les problèmes dans l'environnement de production


Exemple concret pour un site e-commerce :

    javascriptCopydescribe('Processus d'achat', () => {
      it('permet à l'utilisateur d'acheter un produit', () => {
        // Connexion
        cy.visit('/login')
        cy.get('#email').type('user@example.com')
        cy.get('#password').type('password123')
        cy.get('button[type="submit"]').click()

        // Navigation catalogue
        cy.visit('/products')
        cy.get('.product-card').first().click()

        // Ajout au panier
        cy.get('.add-to-cart').click()

        // Processus de paiement
        cy.get('.checkout').click()
        cy.get('#card-number').type('4242424242424242')
        cy.get('#expiry').type('1225')
        cy.get('#cvv').type('123')
        cy.get('button[type="submit"]').click()

        // Vérification
        cy.get('.confirmation-message')
          .should('contain', 'Commande confirmée')
      })
    })


Outils populaires :

Cypress || Selenium || Playwright || TestCafe || Puppeteer

Avantages || Inconvénients 


    Teste l'application comme un utilisateur réel   || Plus lents à exécuter
    Vérifie l'intégration complète                  || Plus complexes à maintenir
    Identifie les problèmes de performance          || Plus fragiles (peuvent échouer pour des raisons externes)
    Valide les flux utilisateurs critiques          || Plus coûteux en ressources



Bonnes pratiques :

    Tester les parcours utilisateurs critiques
    Maintenir des données de test isolées
    Gérer les temps d'attente intelligemment
    Structurer les tests de manière modulaire
    Utiliser des sélecteurs stables
    Mettre en place du reporting détaillé

Les tests E2E complètent la pyramide de tests traditionnelle (unitaires, intégration) en validant l'application dans son ensemble.

## Cahier de test test avancés (test routes API)

       6. throw 404 if query parameter are outofbounds
    ID: T6
    Objectif: On vérifie que lors du scénario ou la route est appellée  // '/words?limit=10&page=2' // la page affiche bien une liste 10 elements par page puis qu'on est bien sur la page 2, comme il n'y a pas deux pages, je n'insert que deux mots, il faut que j'ai un code errer 404. 
    Etapes de test: 
        - Insertion des deux mots, je met dans une variable response la requête attendu. 
    Resultat attendu: 
        - que le status de la response.body soit égal à 404. 


        7. display pagination with normal scenario
    ID: T7
    Objectif: On vérifie que lors du scénario ou la route est appellée  // '/words?limit=10&page=1' // la page affiche bien une liste 10 elements par page puis qu'on est bien sur la page 1, (je n'intègre que deux elements).
    Etapes de test: 
        - Insertion des deux mots, je met dans une variable response la requête attendu. 
    Resultat attendu: 
        - que le status de la response.body soit égal à:
        {"items": [
                {word:"bateau" },
                {word: "califourchon"}
            ], "currentPage": 1,
            "totalCount": 2,
            "totalPages": 1}

        8. GET'should return correct pages when nbListItemsToDisplay changes'
        ID: T8
    Objectif: On vérifie que l'affichage du nombre de mot dans la variable limit est respecté // '/words?limit=10&page=1' //
    Etapes de test: 
        - Insertion de 30 mots, et calibrage du nombre d'éléments par pages à 6. 
    Resultat attendu: 
        - que le status de la response.body soit égal à:
      {"items": [
                {word:"bateau" },
                {word: "califourchon"}
            ], "currentPage": 1,
            "totalCount": 2,
            "totalPages": 1}

        9. 'GET /checking displaying right number of word by limit value'
        ID: T9
    Objectif: On vérifie que lors du scénario ou le nobre de words est chang le nombre de pages s'adapte  // '/words?limit=10&page=1' //
    Etapes de test: 
        - Insertion de 30 mots, et calibrage du nombre d'éléments par pages à 6. 
    Resultat attendu: 
        - que le status de la response.body soit égal à:
    {"items": [
                 {word: "marmelade"},
                 {word: "oubliette"},
                 {word: "cithare"},
                 {word: "carapace"},
                 {word: "gondole"},
                 {word: "égratignure"}
             ], "currentPage": 3,
             "totalCount": 32,
             "totalPages": 6}

        10. 'GET /checking displaying a random word'
        ID: T10
    Objectif: On vérifie que la requête  // '/words/random' // renvoi un des mots au hasard 
    Etapes de test: 
        - Insertion de 2 mots, et attente du retour de body de correspondre à un des deux mots indiqués. 
    Resultat attendu: 
        - que le status de la response.body soit égal à:
        - expect(validWord).toContainEqual(response.body);

        11. 'POST /checking a new word is adding to a list'
        ID: T11
    Objectif: On vérifie que la requête  // '/words' // ajoute bien un mot au tableau de mots 
    Etapes de test: 
        - Insertion de 2 mots, et ajout de . 
    Resultat attendu: 
        - que le status de la response.body soit égal à:
        - expect(validWord).toContainEqual(response.body);



### Selecteur Stables (petite parenthèse)

Il s'agit de bonne pratique dans la conceptiond des selecteurs HTML plus robustes: 

    Exemple:

        <!-- Mauvais exemple -->

        <button class="btn-blue mt-4">Submit</button>

        <!-- Bon exemple -->

        <button 
          data-testid="submit-button"
          class="btn-blue mt-4"
        >
          Submit
        </button> 


### PlayWright 

// Tuto Claude pour l'installation de Playwirght sur un projet perso afin de lui appliquer des tests automatiques. 

Installer et configurer Playwright pour les tests end-to-end.
En effet, Playwright doit généralement être installé au niveau de la racine de votre projet. Voici la procédure :

À la racine de votre projet, installez Playwright via npm :

bashCopynpm init playwright@latest

Cette commande va :


Installer les dépendances nécessaires
Créer un dossier tests avec un exemple de test
Créer un fichier playwright.config.ts (ou .js) à la racine
Ajouter les scripts nécessaires dans votre package.json

La structure typique ressemblera à :

        Copyvotre-projet/
        ├── node_modules/
        ├── tests/
        │   ├── example.spec.ts
        │   └── ...
        ├── playwright.config.ts
        ├── package.json
        └── ...

Pour exécuter vos tests, vous pourrez utiliser :

bashCopynpx playwright test



### Ressources 

https://2023.stateofjs.com/en-US

https://learn.microsoft.com/fr-fr/dotnet/devops/dotnet-test-github-action


 expect(response.body).toEqual
        ({"items": [
                {word:"bateau" },
                {word: "califourchon"}
            ], "currentPage":1,
            "totalCount": 3,
            "totalPages": 2}
    );