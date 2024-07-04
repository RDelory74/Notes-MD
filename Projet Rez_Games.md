# Lancement du Projet Rez'Games

Choisir un produit service soit: 

    - D’une application mobile et sa page marketing desktop

On axe toute l'UX/UI sur l'utilisation App Mobile et on va créer en second une landing page (plutot static) pour rediriger ver l'app (PWA) 

    - D’un produit/service cross-platform disponible à la fois sur appli et sur navigateur

On axe notre UX/UI sur une utilisation cross-plateform, c'est à dire tant Descktop que mobile. 


### Notre choix se portera sur: 

    - D'un produit/service cross-plateform disponible à la fois sur appli et sur navigateur

### Car: 

    - Possibilité de charger des photos et de consulter en ligne à la maison et correspond plus à notre persona principal

### Personna:
1. Créer un à trois persona pour le projet
     Qui sont vos cibles ?
     Quels sont leur besoins,
    leurs habitudes numériques, 
    les freins envers le projet, 
    leur but immédiat… 

    //PERSONA

… Nom               | Johan le Passionnée de Jeux vidéo       | Moumen le Collectionneur Dévoué                     |        Rodolphe le Cosplayeur   |
… Tranche d'âge     |  22 ans                                 |  40 ans                                             |  30 ans                         | 
… Profession        |  Employé                                |  Ingénieur logiciel                                 |  Intermittent                   | 
… Centre d'interet  |  Jouer                                  |  Constituer sa collection                           |  Se déguiser en Cosplay         |
… Objectifs         |  Acheter le derniers jeux               |  Cherche des pièces rares                           |  Trouver des accessoires costume|
… Objectifs         |  Acheter une version unique             |  Faire estimer sa collection                        |  Acheter des Figurines déco     |
… Objectifs         | (re)Découvrir des Jeux                  | Compléter sa collection                             |                                 |
… Objectifs         | Acheter pas chère                       | Etre informé de la dispo d'un article recherché     |                                 |
… Frustrations      | Ne pas trouver le jeux rechercher       | Recevoir un faux/Contrefaçon                        | Recevoir une contrefaçon        |
… Frustrations      | Recevoir un jeux qui fonctionne pas/mal | Avoir une mauvaise estimation                       |                                 |
… Frustrations      | Attendre pour la livraison              | Probléme de livraison                               |                                 |
… Frustrations      |                                         | Manque de confiance des les revendeurs              |                                 |
… Frustrations      |                                         | Difficulté à estimer collection autres plateformes  |                                 |




### Fonctionnalité:
2. Lister les fonctionnalités que vous souhaitez proposer Les hiérarchiser en plusieurs lots en fonction de leur pertinence par rapport à votre concept et vos cibles

### Experience utilisation 
3. Définir l’expérience d’utilisation de votre app Mapper la navigation dans l’application, les différents écrans et les possibilités d’interaction grâce à un user flow

### Wireframe
4. Détailler les wireframes des écrans principaux Choisissez un scénario de démo pour la présentation, et faites des wireframes pour chacun des écrans qui le compose. Laisser de côté les écrans de connexion/inscription et autres réglages, concentrez vous sur une ou plusieurs proposition de valeur.

### Le MarkDown
5. Consignez ces éléments dans un document de la forme de votre choix Il représentera votre dossier de conception




# Projet Method Agile

##  _Vision product_ R€Z' GAMES (RETRO)
 
Offrir un site de confiance qui permet de revaloriser et de certifier des produits issus des tendances rétro de la culture Geek
 
### _POUR_
 
Tous les gamers et passionnés de culture Geek
 
### _QUI SOUHAITENT_
 
Revendre ou acheter des produits issus de la culture Geek et faire une analyse, une certification et une estimation  tarifiaire
 
### _NOTRE PRODUIT EST_
 
n site d'achat de revente et d'analyse de Jeux videos et de produits liés à la culture Geek
 
### _QUI_
 
Offrir une seconde vie au marché gaming d'occasion et assure la remise en valeur des collections
 
### _A LA DIFFERENCE DE_
 
Estimation en rapport avec les argus du net
Service de certification
Notation juste et précise
 
### _PERMET DE_
Racheter et revendre des produits rétro Geek au prix du marché
Remise en valeur des collections

![Vision product](/home/rodolphe-delory/Notes-MD/Images/Vision_Product_REZ.jpeg "Vision schema")



## User story Map

### Types d'utilisateur

Geek Passionnée (visiteur/acheteur/vendeur)
Expert 
ADMIN


### MVP 1

#### On défini quelles fonctionnalitées on veut mettre en priorité // On utilise l'app scrum-time 
    +---------------------------------------------+------------------+
    | Usert story                                 |Note complexité   |
    +---------------------------------------------+------------------+
    | Consulter des produits                      |M |   |   |   |   |
    | Créer un compte                             |S |   |   |   |   |
    | Etre livré à une certaine adresse           |S |   |   |   |   |
    | Suivre ma commande                          |M |   |   |   |   |
    | Pouvoir accéder à une page produit détaillé |M |   |   |   |   |
    | Afficher un panier                          |  |M  |   |   |   |
    | Ajouter à un panier                         |  |S  |   |   |   |
    | Supprimer à un panier                       |  |S  |   |   |   |
    | Paiement CB                                 |S |   |   |   |   |
    | Moyen de connection ADMIN                   |  |M  |   |   |   |
    | Ajouter des données                         |  |S  |   |   |   |
    | Supprimer des données                       |  |S  |   |   |   |
    | Modifier des données                        |  |M  |   |   |   |
    | Gérer mon Compte                            |M |   |   |   |   |
    +---------------------------------------------+------------------+

    On voit que pour pour les user story (Accéder à un panier) et (Pouvoir gérer mes produits) on pourrais les re-découper de la sorte: 

        - Accéder à un panier (GEEK): 
            - Tache : Afficher un panier
            - Tache : Ajouter un nouveau produit à mon panier
            - Tache : Supprimer dans mon panier 

        - Pouvoir gérer mes produits (ADMIN): 
            - Tache : Ajouter
            - Tache : Supprimer
            - Tache : Modifier
            - Tache : interface
            - Tache : Connection 


    On va mesurer le tout en taille de t-shirt, l'important est de garder une coherence entre les differentes taches, a savoir si on a une user story en XL cela peut vouloir dire qu'il faut la rediviser en petites tâches

#### Etablir les taches techniques et estimer le temps en heure pour les réaliser

#### Préparer les bases de données

BASE CLIENT 

    +---------------------------------------------+------+--------+---------------------+--------------+--------+-----+
    | Base de client                              | Nom  | Prenom | Adresse             | Code postal  | Ville  | Age |
    +---------------------------------------------+------+--------+---------------------+--------------+--------+-----+
    |                                             |      |        |                     |              |        |     |
    | Rodolphe Delory                             |Delory|Rodolphe|145 rue de la prairie|74330         | Epagny | 36  |
    +---------------------------------------------+----+----------+---------------------+--------------+--------+-----+




