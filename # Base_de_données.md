# Base de données

## Deux grandes composantes de base de donnée : les données et le SGBD

(Système de gestion de base de données) système de requêtage qui traite notre demande et nous retourne des resultats. 

Les données sont structurées: 

    - Banque de donnée: ensemble de bases de donnée (type un repertoir ou dossier) 
    - Bases de données 
    - Tables (voir ça comme un tableau) type une feuille dans un excel 
    - Lignes d'enregistrement (des entrées)
  
  Le tout constitut une hierarchie de base donnée;

  Le rôle du SGBD en quatre taches: 

    - le moteur SQL: Il lit les differentes lignes d'enregistrement
    - Le catalogue: Déscription de notre base de donnée et info sur les utilisateurs avec leur droit d'accès. 
    - Language de requête (traitement): SQL
    - processeur de requête: prendre notre requête et la transformer en commande auprès du moteur. 

## Le processus: 

    1 - J'écris ma requête et je l'envoi au processeur de requête (un plan d'execution)
    2 - Puis il vérifie les droits dans le catalogue pour effectuer les opérations 
    3 - Les commandes sont ensuite envoyé au moteur SQL qui exectute les traitement nécessaires.
    4 - Le moteur nous retourne ensuite les resultats. 

Selon ce que l'on va demander, il peut y avoir plusieurs plans d'execution. 

## Modèle entité association

    Attributs: Catégorie par type (REFPROD/DESIGN/NUMFACTU)


Les cardinalités, sont les sequences minimum et maximum possibles entre deux entités elles sont traitées comme suit: 
/
  
Ont les distinguent en 2 catégories (minimum et maximum) que l'ont sépare par une virgule: 

        - 0,1 (Peux ne pas en avoir mais s'il en a il en aura qu'un)
        - 0,n (Peux ne pas en avoir ou en avoir plusieurs)
  

   * Exemple // Marque et Auto // *

        Une marque peut avoir au moins un modèle de voiture mais aussi plusieurs (1,n)
        Une Autombile doit avoir au moins une marque et ne peut en avoir plus (1,1)

    ![Exemple Schema](/home/rodolphe-delory/Images/Captures d’écran/Capture d’écran du 2024-06-10 10-00-18.png) "Exemple Auto".

## Glossaire 

<ins>table</ins> : Un tableau comprenant toutes nos lignes d'enregistrement
<ins>clefs</ins> : Réference unique d'une entité, permet de cibler une entité
<ins>index</ins> : Est une structure qui permet de segmenter les données afin d'améliorer la recherche du SGBD
<ins>relation</ins> : La liaison entre les entités
<ins>les differents types de données</ins>: une chaine de caractères, un réel /float/ (nb à virgule), un entier (num de fact), une date ou une heure / var char (variable charactéres) 
<ins>SGBD</ins>: Système de gestion de base de données 
<ins>SGBDR</ins> : Système de gestion de base de données relationnelle (la relation entre entre deux tableaux)
<ins>MDC</ins> : Modèle conceptuel de données qui textualise les données de la manière dont elles seront stockées. 
<ins>MLD</ins> : Modèle logique de données organise les données avec les tables, les colonnes et les clées primaires. 
<ins>Clé primaire</ins> : Identifiant d'une entité 
<ins>Clé Etrangère</ins> : (Foreigner Key) permet d'appeller l'ID d'une entité dans un table.  



![Schema BDD](/home/rodolphe-delory/Images/Schema_BDD_websites.png "Schema BDD").


## Création des base de données 

Après avoir installé MySQL: 

Je crée mes bases de données: 

Pour se connecter à MySql via le terminal de commande je proccède comme suit: 

    -  sudo mysql -u Rodhk -p 

Je rentre le mot de passe Linux (sudo) et puis le mot de passe MySql 

Je me positionne sur la database MySql sur lequel je veut travailler: 

    - use mydb

Et après avec les commande setect / insert into / ALter je modifie mes tableaux, pour plus de commande j'utilise le site ci-dessous: 

    http://www.edu4java.com/en/sql/sql6.html
    https://sql.sh/cours/alter-table


Je compose mes bases de données avec visual studio pro (voir les exemple ci-dessous) , cela me permet de me familiariser avec les commandespour faire des selections multiples. 

Par exemple pour intégrer la base de données ci-dessous j'utilise la commade suivant:  

        - INSERT INTO nom_du_tableau (nom_colonne_1,nom_colonne_2,nom_colonne_3) VALUES
  


('Chantal', 'Lauby', '23 mars 1948', 'française', 'comique'),
('Alain', 'Chabat', '24 novembre 1958', 'française', 'acteur et réalisateur'),
('Dominique', 'Farrugia', '2 septembre 1962', 'française', 'comique'),
('Gérard', 'Darmon', '29 février 1948', 'française', 'acteur et chanteur'),
('Albert', 'Hall', '0 novembre 1937', 'Américain', 'acteur polyvalent'),
('Robert', 'Duvall', '5 janvier 1931', 'Américaine', 'acteur réalisateur et producteur'),
('Frederic', 'Forrest', '23 décembre 1936', 'Américaine', 'acteur de film de guerre'),
('Martin', 'Sheen', '3 août 1940', 'Américaine', 'Acteur'),
('Milla', 'Jovovich', '17 décembre 1975', 'Ukrainienne', 'Actrice'),
('Ian', 'Holm', '12 septembre 1931', 'Anglaise', 'Acteur'),
('Bruce', 'Willis', '19 mars 1955', 'Américaine', 'Acteur de film d’action'),
('John', 'Travolta', '18 février 1954', 'Américaine', 'Acteur et Danseur'),
('Samuel', 'L.Jackson',' 21 décembre 1948', 'Américain', 'Acteur'),
('Uma', 'Thurman', '29 avril 1970', 'Américaine', 'Actrice'),
('Mark', 'Hamill', '25 septembre 1951', 'Américaine', 'Maîtrise la force'),
('Harrison', 'Ford', '13 juillet 1942', 'Américaine', 'Acteur'),
('Carrie', 'Fisher', '13 juillet 1942', 'Américaine', 'Actrice'),
('Karen', 'Allen', '5 octobre 1951', 'Américaine', 'Actrice');

On met bien une virgule entre chaque ligne et un point virgule à la fin des données. 

('Indiana Jones, Les Aventuriers de l’Arche perdue', '1981', 'aventure', '20 000 000','115min'),
('Star wars', '1977', 'aventure','11,5 000 000', '105min'),
('Pulp fiction', '1994', 'drame', '8 000 000', '154min'),
('Le cinquième élément', '1997', 'action', '75 000 000','126min'),
('Apocalypse Now', '1979', 'guerre', '31 000 000', '153min),
('La cité de la peur', '1994', 'comédie', '7.5 000 000', '113min'),
('Mon voisin Totoro', '1999', 'Jeunesse', '3 000 000', '86min,';')

(1,'350',1),
(2,'420',1),
(3,'220',1),
(4,'270',1),
(5,'280',1),
(1,'157',2),
(2,'158',2),
(3,'120',2),
(4,'130',2),
(1,'157',3);

Via le terminal de commande j'utilise la commande: 

    - select *from Nom_de_table;
  
Qui se traduit par selectionne toutes les entités de la table nom_de_table et affiche les moi. 

+---------+--------------+-------------+-----------------+
| idSALLE | NUM_DE_SALLE | NB_DE_PLACE | CINEMA_idCINEMA |
+---------+--------------+-------------+-----------------+
|       1 |            1 | 350         |               1 |
|       2 |            2 | 420         |               1 |
|       3 |            3 | 220         |               1 |
|       4 |            4 | 270         |               1 |
|       5 |            5 | 280         |               1 |
|       6 |            1 | 157         |               2 |
|       7 |            2 | 158         |               2 |
|       8 |            3 | 120         |               2 |
|       9 |            4 | 130         |               2 |
|      10 |            1 | 157         |               3 |
+---------+--------------+-------------+-----------------+

+----------+------------+------------------------------+--------------+-----------+
| idCINEMA | NOM        | ADRESSE                      | VILLE        | COMPAGNIE |
+----------+------------+------------------------------+--------------+-----------+
|        1 | Pathée     | adresse 7 Av de Brogny       | Annecy       | Pathe     |
|        2 | Megarama   | adresse 1 Rue du Tremblay    | Seynod       | Gaumont   |
|        3 | La turbine | adresse 3 Rue des Tisserands | Cran Gevrier | CG        |
+----------+------------+------------------------------+--------------+-----------+
+-------------+-------------------+------------------------------+
| FILM_idFILM | ACTEURS_idACTEURS | ROLES                        |
+-------------+-------------------+------------------------------+
|           1 |                16 | Indiana Jones                |
|           1 |                18 | Marion Ravenwood             |
|           2 |                15 | Luke Skywalker               |
|           2 |                16 | Han Solo                     |
|           2 |                17 | La princesse Leia Organa     |
|           3 |                11 | Butch Coolidge               |
|           3 |                12 | Vincent Vega                 |
|           3 |                13 | Jules Winnfield              |
|           4 |                 9 | Leeloo                       |
|           4 |                10 | Father Vito Corneluis        |
|           4 |                11 | Korben Dallas                |
|           4 |                19 | Jean-Baptiste Emanuel Zorg   |
|           5 |                 5 | Chef Philipps                |
|           5 |                 6 | Le lieutenant colonel Kilgor |
|           5 |                 7 | Chef                         |
|           5 |                 8 | Le capitaine Willard         |
|           6 |                 1 | Odile Deray                  |
|           6 |                 2 | Serge Karamazov              |
|           6 |                 3 | Simon Jeremy                 |
|           6 |                 4 | Comissaire Patrick Biales    |
+-------------+-------------------+------------------------------+

+--------+---------------------------------------------------+----------------+----------+----------+--------+
| idFILM | TITRE                                             | DATE_DIFFUSION | GENRE    | BUDGET   | DUREE  |
+--------+---------------------------------------------------+----------------+----------+----------+--------+
|      1 | Indiana Jones Les Aventuriers de l’Arche perdue   | 1981           | aventure | 20000000 | 115min |
|      2 | Star wars                                         | 1977           | aventure | 11500000 | 105min |
|      3 | Pulp fiction                                      | 1994           | drame    |  8000000 | 154min |
|      4 | Le cinquième élément                              | 1997           | action   | 75000000 | 126min |
|      5 | Apocalypse Now                                    | 1979           | guerre   | 31000000 | 153min |
|      6 | La cité de la peur                                | 1994           | comédie  |  7500000 | 113min |
|      7 | Mon voisin Totoro                                 | 1999           | Jeunesse |  3000000 | 86min  |
+--------+---------------------------------------------------+----------------+----------+----------+--------+

INSERT INTO CINEMA_has_SALLE_has_FILM (CINEMA_idCINEMA,SALLE_idSALLE,FILM_idFILM,DATE) VALUES

(1,5 ,3, '2023-12-09 18:00:00'),
(1,4 ,2, '2023-12-27 20:00:00'),
(3,10,2, '2023-12-13 20:00:00'),
(1,1 ,5, '2023-12-02 18:00:00'),
(1,2 ,1, '2023-12-19 20:00:00'),
(2,7 ,3, '2023-12-20 18:00:00'),
(2,7 ,5, '2023-12-15 21:00:00'),
(1,5 ,5, '2023-12-22 21:00:00'),
(2,6 ,3, '2023-12-23 17:00:00'),
(2,9 ,1, '2023-12-07 21:00:00'),
(1,2 ,6, '2023-12-16 16:30:00'),
(1,1 ,4, '2023-12-21 18:00:00'),
(2,9 ,1, '2023-12-26 15:00:00'),
(1,4 ,5, '2023-12-07 12:00:00'),
(2,8 ,2, '2023-12-25 21:00:00'),
(1,2 ,1, '2023-12-01 20:00:00'),
(1,1 ,5, '2023-12-01 21:00:00'),
(2,9 ,4, '2023-12-14 19:00:00'),
(2,7 ,3, '2023-12-06 18:00:00'),
(2,9 ,4, '2023-12-29 18:00:00'),
(1,4 ,4, '2023-12-18 18:00:00'),
(1,5 ,3, '2023-12-19 18:00:00'),
(3,10,2, '2023-12-20 21:00:00'),
(2,2 ,1, '2023-12-21 22:00:00'),
(1,4 ,1, '2023-12-22 18:00:00'),
(2,7 ,6, '2023-12-02 22:00:00');

## Requêtes de selection 

Mainteant que j'ai implémenté toutes mes données dans mes tables de données je vais effectuer des requêtes. 

Pour effectuer une requête sur MySql et dans le terminal,  j'utilise la commande suivante: 

Lister l’ensemble des films.

        - select *from FILM; 

+--------+---------------------------------------------------+----------------+----------+----------+-------+
| idFILM | TITRE                                             | DATE_DIFFUSION | GENRE    | BUDGET   | DUREE |
+--------+---------------------------------------------------+----------------+----------+----------+-------+
|      1 | Indiana Jones Les Aventuriers de l’Arche perdue   | 1981           | aventure | 20000000 | 115   |
|      2 | Star wars                                         | 1977           | aventure | 11500000 | 105   |
|      3 | Pulp fiction                                      | 1994           | drame    |  8000000 | 154   |
|      4 | Le cinquième élément                              | 1997           | action   | 75000000 | 126   |
|      5 | Apocalypse Now                                    | 1979           | guerre   | 31000000 | 153   |
|      6 | La cité de la peur                                | 1994           | comédie  |  7500000 | 113   |
|      7 | Mon voisin Totoro                                 | 1999           | Jeunesse |  3000000 |  86   |
+--------+---------------------------------------------------+----------------+----------+----------+-------+



Liste des films plus long que 2 heures

        - SELECT * FROM FILM WHERE DUREE > '200'

+--------+-------------------------+----------------+--------+----------+-------+
| idFILM | TITRE                   | DATE_DIFFUSION | GENRE  | BUDGET   | DUREE |
+--------+-------------------------+----------------+--------+----------+-------+
|      3 | Pulp fiction            | 1994           | drame  |  8000000 |   154 |
|      4 | Le cinquième élément    | 1997           | action | 75000000 |   126 |
|      5 | Apocalypse Now          | 1979           | guerre | 31000000 |   153 |
+--------+-------------------------+----------------+--------+----------+-------+


Liste des films par ordre alphabétique décroissant

        - SELECT TITRE FROM mydb.FILM ORDER BY TITRE DESC;

+---------------------------------------------------+
| TITRE                                             |
+---------------------------------------------------+
| Star wars                                         |
| Pulp fiction                                      |
| Mon voisin Totoro                                 |
| Le cinquième élément                              |
| La cité de la peur                                |
| Indiana Jones Les Aventuriers de l’Arche perdue   |
| Apocalypse Now                                    |
+---------------------------------------------------+


Liste des séances sur les 10 derniers jours

        -SELECT * FROM mydb.CINEMA_has_SALLE_has_FILM WHERE DATE < '2023-12-31' AND DATE > '2023-12-21';
-------------+-------------------+---------------+
| FILM_idFILM | ACTEURS_idACTEURS | ROLES         |
+-------------+-------------------+---------------+
|           1 |                16 | Indiana Jones |
|           2 |                16 | Han Solo      |
+-------------+-------------------+---------------+


+-----------------+---------------+-------------+---------------------+
| CINEMA_idCINEMA | SALLE_idSALLE | FILM_idFILM | DATE                |
+-----------------+---------------+-------------+---------------------+
|               1 |             1 |           4 | 2023-12-21 18:00:00 |
|               2 |             2 |           1 | 2023-12-21 22:00:00 |
|               1 |             4 |           1 | 2023-12-22 18:00:00 |
|               1 |             4 |           2 | 2023-12-27 20:00:00 |
|               1 |             5 |           5 | 2023-12-22 21:00:00 |
|               2 |             6 |           3 | 2023-12-23 17:00:00 |
|               2 |             8 |           2 | 2023-12-25 21:00:00 |
|               2 |             9 |           1 | 2023-12-26 15:00:00 |
|               2 |             9 |           4 | 2023-12-29 18:00:00 |
+-----------------+---------------+-------------+---------------------+



## Créer les différentes tables de la base de données

Liste des films avec Harrison Ford dans son casting

    - SELECT * FROM mydb.FILM_has_ACTEURS WHERE ACTEURS_idACTEURS = 16;

+-------------+-------------------+---------------+
| FILM_idFILM | ACTEURS_idACTEURS | ROLES         |
+-------------+-------------------+---------------+
|           1 |                16 | Indiana Jones |
|           2 |                16 | Han Solo      |
+-------------+----------------c un film ayant Bruce Willis ou Harrison Ford dans son casting

    SELECT SALLE.NUM_DE_SALLE
     FROM mydb.SALLE
     JOIN CINEMA_has_SALLE_has_FILM ON idSALLE = SALLE_idSALLE
     JOIN FILM ON CINEMA_has_SALLE_has_FILM.FILM_iDFILM = idFILM
     JOIN FILM_has_ACTEURS ON idFILM = FILM_has_ACTEURS.FILM_idFILM
	 JOIN ACTEURS ON ACTEURS_idACTEURS = idACTEURS
	 WHERE FILM_has_ACTEURS.ACTEURS_idACTEURS = 16 OR FILM_has_ACTEURS.ACTEURS_idACTEURS = 11;

+--------------+
| NUM_DE_SALLE |
+--------------+
|            5 |
|            5 |
|            1 |
|            2 |
|            2 |
|            1 |
|            4 |
|            4 |
|            4 |
|            2 |
|            2 |
|            4 |
|            2 |
|            4 |
|            4 |
|            4 |
|            3 |
|            1 |
|            1 |
+--------------+

Nombre de places totale pour le cinéma Mégarama

    SELECT SUM(NB_DE_PLACE)
	FROM mydb.SALLE
    JOIN CINEMA ON CINEMA_iDCINEMA = idCINEMA
    WHERE CINEMA.NOM = 'MEGARAMA';

+------------------+
| SUM(NB_DE_PLACE) |
+------------------+
|              565 |
+------------------+

Liste des films projetés dans une salle entre 100 et 200 places

    SELECT TITRE
    FROM mydb.FILM
    JOIN CINEMA_has_SALLE_has_FILM ON FILM.idFILM = CINEMA_has_SALLE_has_FILM.FILM_idFILM
    JOIN SALLE ON SALLE_idSALLE = idSALLE
    WHERE SALLE.NB_DE_PLACE < 200 AND SALLE.NB_DE_PLACE > 100;

+---------------------------------------------------+
| TITRE                                             |
+---------------------------------------------------+
| Pulp fiction                                      |
| Pulp fiction                                      |
| Pulp fiction                                      |
| Apocalypse Now                                    |
| La cité de la peur                                |
| Star wars                                         |
| Indiana Jones Les Aventuriers de l’Arche perdue   |
| Indiana Jones Les Aventuriers de l’Arche perdue   |
| Le cinquième élément                              |
| Le cinquième élément                              |
| Star wars                                         |
| Star wars                                         |
+---------------------------------------------------+

Tous les cinémas qui ont passé ou vont passer star wars

    SELECT NOM
    FROM mydb.CINEMA
    JOIN CINEMA_has_SALLE_has_FILM ON idCINEMA = CINEMA_has_SALLE_has_FILM.CINEMA_idCINEMA
    JOIN FILM ON CINEMA_has_SALLE_has_FILM.FILM_idFILM = FILM.idFILM
    WHERE CINEMA_has_SALLE_has_FILM.FILM_idFILM = 'STAR WARS';

+------------+
| NOM        |
+------------+
| Pathée     |
| Megarama   |
| La turbine |
| La turbine |
+------------+


Nombre total de place par cinéma

    SELECT SUM(NB_DE_PLACE)
	FROM mydb.SALLE
    JOIN CINEMA ON CINEMA_iDCINEMA = idCINEMA
    WHERE CINEMA.NOM = 'MEGARAMA';
