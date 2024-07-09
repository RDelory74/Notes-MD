# LARAVEL

## API REST

API: Application programming interface permet de mettre a jour les informations d'interface sans avoir besoin de refresh (API WEB) Json

API REST: C'est une architecture de request via les fonctions (GET/POST/PUT ou PATCH/DELETE) afin d'intéragir avec les données de ma base. Son écriture se fait de la façon suivante: 

Admettons que je veuille créer une API WEB pour un site e-commerce de jeux vidéos (tiens!!!) et que je veuille récupérer/lire le nom d'un jeux avec l'ID 8 dans ma base de donnée qui s'appelle api j'aurais l'écriture suivante: 

        - GET /api/products/video_games/8/name
        - $api->get(product/video_games="8")

## MVC / RMVC


Modèle: Contient les données et la logique métier (c'est à dire le code qui décide du traitement des données | les requêtes SQL et autres algorythmes)
Controlleur: Gére les actions entre l'utilisateur (vue) et le modèle.
Vue: Affiche le resultat de la requête sur l'interface. Code HTML et manip' PHP (boucles et conditions)

Router: la route de la requête jusqu'au retour. 


CRUD Creat Read Update Delete


## LES DESIGN PATTERNS

Patron de conception – sont des méthodes de codage reconnues, qui permettent de résoudre des problèmes récurrents.