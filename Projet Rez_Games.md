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




