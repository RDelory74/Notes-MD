# Algorithmie

## Haaaaa l'Algo  !!
On parle à la machine directement ici, pas de chichi de l'execution et il faut pas que ça déborde, une virgule, une faute de casse et "ça péte tout". Ca fait mal au crâne, les exercices nous demandent de conceptualiser le truc puis de tester des trucs. Bref des trucs, qui font des trucs ... Ou pas ! 

### Alors En gros c'est quoi ? 

De ce que j'ai compris, il s'agit des languages qui servent à créer les logiciels, à parler avec la machine pour lui demander de "faire". On s'approche de la machine et notre ésprit doit sérieusement s'adapter pour intéragir avec elle.

J'ai utilisé plusieurs outils: 
 - La variable (elle peut être d'un entier (int) d'un décimale (float) ou booléenne (retourne une vérité "true" ou une erreur "false")). Dit comme ça c'est forcement mal dit mais ça demandera à être amélioré. 
- La fonction, on entend souvent c'est la commande de la recette type couper l'oignon. Cependant attention elle aussi est de type int (si elle retourne un entier) float (pour la gestion de virgules) ou void pour annoncer quelle est vide. 
- La boucle avec for pour pouvoir lui donner une durée (Le truc à tester; la course; l'update) mais aussi avec while pour qu'elle se répéte jusqu'a ce qu'elle atteigne un état (truc à tester jusqu'a ce qu'il devienne une valeur ou true ou autre)
- La condition qui nous permet de déclarer une action en fonction qu'une variable ou une fonction est "true" ou "false". 
- Le void setup () pour lancer l'affichage 
- Le void Draw pour lancer le refresh (60 fps de base) 
- Le void buffer pour assurer la mémoire des actions


C'est un peu ledge mais on travaille sur Processing pour l'instant et disont qu'on ne se confronte pas à l'ensemble de ce que la programmation nous imposera et heureusement j'ai envi de dire, parce que j'ai rarement eu la sensation d'autant modifier mon esprit pour comprendre. A chaque exercice j'ai l'impression de plier mon cerveau pour esperer comprendre. 

# Algorithmie Avancée

Haaa Alors ça y est, il s'en est passé du temps depuis le premier module d'algo, (4 mois peu être plus), j'en ai vu des languages j'en ai appliqué des boucles for des variables des méthode / ou fonctions. Bref, je trouve interressant de voir comment je vais m'en sortir cette fois ci avec ce module. 

Il est en tout prévu d'aborder: 

    - Le pseudo-code et l'anticipation du comportement d'alogrithme
    - Décourverte de stratégie divide-and-conquer
    - Choix des structure de donnée pour un algo
    - notions de compléxité algo et espace

A première  vue, j'ai l'impression qu'il va y avoir pas mal de conception autour de l'algo.


### Decouverte des algo de tri 

## J'ai pensé au Tri a Bulles: 

    Je vais itérer sur mon tableau et je compare la valeur de chaque case avec la case précedente. 
    Si la valeur de la case précedente est plus petite je modifie son index de -1 je la recule d'un 
    cran vers a gauche. Et je recommence sur le tableau jusqu'a ce que toutes la valeurs soit triées. 

## les 2 grands types de tri

    linéaire, O(n), si le temps de calcul est proportionnel au nombre d'éléments. linéarithmique, 
    O(n log n), si le temps de calcul est proportionnel au nombre d'éléments multiplié par le 
    logarithme du nombre d'éléments. quadratique, O(n²), si le temps de calcul et proportionnel 
    au carré du nombre d'éléments

    La compléxité : (source wiki)

La complexité temporelle (en moyenne ou dans le pire des cas) mesure le nombre d'opérations élémentaires
 effectuées pour trier une collection d'éléments. C'est un critère majeur pour comparer les algorithmes 
 de tri, puisque c'est une estimation directe du temps d'exécution de l'algorithme. Dans le cas des algorithmes 
 de tri par comparaison, la complexité en temps est le plus souvent assimilable au nombre de comparaisons effectuées, 
 la comparaison et l'échange éventuel de deux valeurs s'effectuant en temps constant.

 La complexité spatiale (en moyenne ou dans le pire des cas) représente, quant à elle, la quantité de mémoire
dont va avoir besoin l'algorithme pour s'exécuter. Celle-ci peut dépendre, comme le temps d'exécution, de la
 taille de l'entrée. Il est fréquent que les complexités spatiales en moyenne et dans le pire des cas soient
 identiques. C'est souvent implicitement le cas lorsqu’une complexité est donnée sans indication supplémentaire.


On a abordé la recursivité: 

    C'est quand une fonction est appellé dans une fonction, elle vas déscendre en récursive. 


