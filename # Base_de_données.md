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
|            5 |Le nouveau film, Jurassic park
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

    SELECT SUM(NB_DE_PLACE), NOM
	FROM mydb.SALLE
    JOIN CINEMA ON CINEMA_iDCINEMA = idCINEMA
    GROUP BY CINEMA.NOM;

+------------------+------------+
| SUM(NB_DE_PLACE) | NOM        |
+------------------+------------+
|             1540 | Pathée     |
|              565 | Megarama   |
|              157 | La turbine |
+------------------+------------+

Budget total de tous les films par année de sortie

|  3000000 | 1999           | Mon voisin Totoro                                 |
+----------+----------------+---------------------------------------------------+

## Insertion, mise à jour et suppression

Créer un film avec au moins trois projections pour le mois prochain

Le nouveau film, Jurassic park

    INSERT INTO mydb.FILM (TITRE,DATE_DIFFUSION,GENRE,BUDGET,DUREE)
    VALUES ('Jurassic Park', '1993', 'aventure, science-fiction', '63000000', '127min');

Les nouvelles seances

    INSERT INTO mydb.CINEMA_has_SALLE_has_FILM (CINEMA_idCINEMA,SALLE_idSALLE,FILM_idFILM,DATE)
    VALUES 
    (1,7,8, '2024-06-28 20:00:00'),
    (2,6,8, '2024-07-02 22:00:00'),
    (3,10,8, '2024-08-03 20:00:00');

Les Acteurs 

    INSERT INTO mydb.ACTEURS(NOM,PRENOM,DATE_DE_NAISSANCE,NATIONALITE,ROLES)
    VALUES
    ('Sam', 'Neill', '14 septembre 1947', 'néo-zélandais', 'Dr. Alan Grant'),
    ('Laura', 'Dern', '10 février 1967', 'américaine', 'Dr. Ellie Sattler');

Et enfin le tableau des FILM_has_ACTEURS

    INSERT INTO mydb.FILM_has_ACTEURS(FILM_idFILM,ACTEURS_idACTEURS,ROLES)
    VALUES
    (8,20,'Dr. Alan Grant'),
    (8,21,'Dr. Ellie Sattler');


Ajouter un cinéma et ses salles

Le cinéma

    INSERT INTO mydb.CINEMA(NOM,ADRESSE,VILLE,COMPAGNIE)
    VALUES
    ('DECAVISION EPAGNY', '145 ROUTE DE LA PRAIRE', 'EPAGNY', 'DECAVISION');

Les Salles

    INSERT INTO mydb.SALLE(NUM_DE_SALLE,NB_DE_PLACE,CINEMA_idCINEMA)
    VALUES
    (1,800,4),
    (2,500,4),
    (3,300,4);

Ajouter 1 000 000 au budget du film que vous avez créé

    UPDATE mydb.FILM 
    SET BUDGET = '64000000'
    WHERE idFILM = 8;

Augmenter de 5% le budget de tous les films

    UPDATE mydb.FILM
    SET BUDGET = BUDGET *1.05;

+--------+---------------------------------------------------+----------------+---------------------------+----------+-------+
| idFILM | TITRE                                             | DATE_DIFFUSION | GENRE                     | BUDGET   | DUREE |
+--------+---------------------------------------------------+----------------+---------------------------+----------+-------+
|      1 | Indiana Jones Les Aventuriers de l’Arche perdue   | 1981           | aventure                  | 21000000 |   115 |
|      2 | Star wars                                         | 1977           | aventure                  | 12075000 |   105 |
|      3 | Pulp fiction                                      | 1994           | drame                     |  8400000 |   154 |
|      4 | Le cinquième élément                              | 1997           | action                    | 78750000 |   126 |
|      5 | Apocalypse Now                                    | 1979           | guerre                    | 32550000 |   153 |
|      6 | La cité de la peur                                | 1994           | comédie                   |  7875000 |   113 |
|      7 | Mon voisin Totoro                                 | 1999           | Jeunesse                  |  3150000 |    86 |
|      8 | Jurassic Park                                     | 1993           | aventure, science-fiction | 67200000 |   127 |
+--------+---------------------------------------------------+----------------+---------------------------+----------+-------+

Supprimer un film (dans ce cas attention, obligation de supprimer toutes les associations précedentes)

Suppression d'abord depuis le ternaire Seances CINEMA_has_SALLE_has_FILM

    DELETE FROM mydb.CINEMA_has_SALLE_has_FILM
    WHERE FILM_idFILM = 5;

Puis suppression du film dans FILM_has_ACTEURS

    DELETE FROM mydb.FILM_has_ACTEURS
    WHERE FILM_idFILM = 5;

Enfin suppression du FILM

    DELETE FROM mydb.FILM
    WHERE idFILM = 5;

Supprimer les films n’ayant aucune projection

    DELETE FROM mydb.FILM       //  commande de supression dans le tableau FILM
    WHERE NOT EXISTS (      //  Condition ou il n'exist pas 
    SELECT 1    //  selectionne une valeur on aurai pu utiliser *(tous) mais pour des raison d'optimisation de performance c'est mieux de préciser 1
    FROM mydb.CINEMA_has_SALLE_has_FILM     // le tableau ou doit s'appliquer la condition 
    WHERE mydb.CINEMA_has_SALLE_has_FILM.FILM_idFILM = mydb.FILM.idFILM);  // la condtion de jointure entre les deux tableaux via les id de liaisons

Dans ce cas ce sera le film N°7 qui sera supprimé. 

## Pour aller plus loin (optionnel)

Liste de tous les films qui passent aujourd'hui

    SELECT mydb.FILM.*
    FROM mydb.FILM
    JOIN CINEMA_has_SALLE_has_FILM ON FILM.idFILM = CINEMA_has_SALLE_has_FILM.FILM_idFILM
    WHERE DATE(CINEMA_has_SALLE_has_FILM.DATE) = CURRENT_DATE (); 

A ce jour il n'y en a pas, mais je vais en ajouter une de Jurassic Park (un revival)

    INSERT INTO mydb.CINEMA_has_SALLE_has_FILM (CINEMA_idCINEMA, SALLE_idSALLE, FILM_idFILM,DATE)
    VALUES (1,7,8,'2024-06-13 20:00:00');

Et je reais un test

    SELECT mydb.FILM.*
    FROM mydb.FILM
    JOIN CINEMA_has_SALLE_has_FILM ON FILM.idFILM = CINEMA_has_SALLE_has_FILM.FILM_idFILM
    WHERE DATE(CINEMA_has_SALLE_has_FILM.DATE) = CURRENT_DATE (); 

Parfait, Film trouvé !!! 

+--------+---------------+----------------+---------------------------+----------+-------+
| idFILM | TITRE         | DATE_DIFFUSION | GENRE                     | BUDGET   | DUREE |
+--------+---------------+----------------+---------------------------+----------+-------+
|      8 | Jurassic Park | 1993           | aventure, science-fiction | 67200000 |   127 |
+--------+---------------+----------------+---------------------------+----------+-------+

Durée totale de projection pour chaque cinéma

    SELECT SUM(DUREE), NOM
    FROM mydb.FILM
    JOIN CINEMA_has_SALLE_has_FILM ON FILM.idFILM = CINEMA_has_SALLE_has_FILM.FILM_idFILM
    JOIN CINEMA ON CINEMA_idCINEMA = idCINEMA
    GROUP BY CINEMA.NOM;

+------------+------------+
| SUM(DUREE) | NOM        |
+------------+------------+
|       1377 | Pathée     |
|       1404 | Megarama   |
|        337 | La turbine |
+------------+------------+

Liste de tous les films ne contenant pas Harrison Ford

    SELECT mydb.FILM.TITRE      // Dans cet exercice je reprend la même pratique que pour supprimer les films qui n'ont pas de séances
    FROM mydb.FILM
    WHERE NOT EXISTS(
    SELECT *
    FROM mydb.FILM_has_ACTEURS
    WHERE FILM_has_ACTEURS.FILM_idFILM = mydb.FILM.idFILM
    AND FILM_has_ACTEURS.ACTEURS_idACTEURS = 16);       // Sauf qu'ici j'ajoute une condition via la commande AND 

Liste des cinéma qui passent tous les films

    SELECT mydb.CINEMA.NOM
    FROM mydb.CINEMA
    WHERE EXISTS(
    SELECT*
    FROM mydb.CINEMA_has_SALLE_has_FILM
    WHERE mydb.CINEMA_has_SALLE_has_FILM.CINEMA_idCINEMA = mydb.CINEMA.idCINEMA
    AND mydb.CINEMA_has_SALLE_has_FILM.FILM_idFILM = 1 ANd 2 ANd 3 ANd 4 ANd 6 AND 8);  // Ici j'ajoute les conditions nécessaires via les AND

+----------+
| NOM      |
+----------+
| Pathée   |
| Megarama |
+----------+

# Initiation NoSQL et MongoDB

## NoSQL, Quésaco ?

Le NoSQL c'est une approche qui se base sur une simplification du traitement des données en évitant l'utilisation conforme des tables, l'objectif est ici d'améliorer la scalabilité horizontale ((scale-out) // ajout de serveurs aux cluster de traitement plutôt que d'améliorer la machine (ajout de ressources type CPU,RAM (scale-UP)))  en fonction de l'évolution des besoins. En sacrifiant une des propriétées ACID on va pouvoir augmenter les autres en rapport avec les besoin de la demande. On favorise ici le codefirst ou l'ensemble des données est  directement intégré au code de l'application ou du programme. 

Type REDIS qui est un modèle de base de données qui va sacrifier la durabilité (sa persistence face aux conflits accidents ou crash) au profit d'une vitesse très élevé, ce qui est très important pour les systèmes bancaires ou de reservation. On va chercher à traiter les conflits de simultanéité par le traçage horaire. 


    ACID

    A pour Atomic, l'idée d'un tout, tout fonctionne ensemble ou rien ne marche, l'état est executé ou annulé.

    C pour Coherence, il s'agit de la coherence des données au travers d'une base de donnée une fois qu'elle est executée. Elle traduit la continuité au travers des états relationnels de la base de donnée. 
    
    I pour Isolation, il s'agit de l'étanchéité d'une transaction, le fait qu'elle soit isolé des autres pour éviter les conflits
    
    D pour durabilité il s'agit de la persistence d'une donnée une fois qu'elle est validée (commit) et ce face aux crash, panne accident. 


Type DYNAMODB est un type de base de données supporté par AWS (Amazon Web Service), il a l'avantage d'être structuré sur reseau important de serveurs, ce qui privilégie  la quantité, la durabilité (enregistre sur plusieurs zone pour faire face aux pannes) et la disponibilité au détriment de la coherence. Après les taux de traitement de vitesse ne sont pas ocmparable à ceux 'une base de donnée de type REDIS. 

Enfin le type MongoDB est populaire pour les applications Web App et IoT, il offre une grande flexibilité dans l'écriture et lui permet de s'adapter à d'autre technologies. son écriture ets en Json et il sauvegarde les données sur plusieurs serveurs (sharding). Il permet aussi une certaine structure des données et donc la possibilité de faire des requêtes plus poussées.

Et pour finir les clé-valeurs sont des types de données utilisés dans une base de données, elles stockent des valeurs de plusierus type et sont accès sur l'accés rapide et simple.  

Ci-dessous un exemple de clé-valeur sous json: 

         {
      "utilisateur1": {
        "nom": "Alice",
        "âge": 30,
        "ville": "Paris"
      },
      "utilisateur2": {
        "nom": "Bob",
        "âge": 25,
        "ville": "New York"
      },
      "produit123": {
        "nom": "Smartphone",
        "prix": 599,
        "stock": 50
      },
      "configuration": {
        "langue": "français",
        "thème": "clair",
        "notifications": true
      }
    }

Aller c'est parti pour l'instalation de MonDB. 

mongodb-compass-1.43.1.x86_64.deb

Je travail principalement sur MongDB Atlas qui ne nécessite pas d'installation de serveur en local et permet de faire les premières insertons de documents:

        {"_id":{"$oid":"666c17eb33157f49c6e2ecb8"},
        "NOM": "Megarama",
            "ADRESSE": "1 Rue du Tremblay",
            "VILLE": "Seynod",
            "COMPAGNIE": "Gaumont",
          	"SALLES": [
              {
                "Numéro":1,
                "nb_place":157
              },
               {
                "Numéro":2,
                "nb_place":158
              },
               {
                "Numéro":3,
                "nb_place":120
              },
               {
                "Numéro":4,
                "nb_place":130
              }
            ]
        }

 Pour présenter les associations possibles entre les deux formats SQL / NoSql: 

   ![SQLvsNoSql](./Capture%20d’écran%20du%202024-06-14%2013-46-42.png).
   ![SQLvsNoSql](./Capture%20d’écran%20du%202024-06-14%2013-48-12.png).




  {
    "idCINEMA": 1,
    "NOM": "Pathée",
    "ADRESSE": "7 Av de Brogny",
    "VILLE": "Annecy",
    "COMPAGNIE": "Pathe"
  }
  {
    "idCINEMA": 2,
    "NOM": "Megarama",
    "ADRESSE": "1 Rue du Tremblay",
    "VILLE": "Seynod",
    "COMPAGNIE": "Gaumont"
  }
  {
    "idCINEMA": 3,
    "NOM": "La turbine",
    "ADRESSE": "3 Rue des Tisserands",
    "VILLE": "Cran Gevrier",
    "COMPAGNIE": "CG"
  }
  {
    "idCINEMA": 4,
    "NOM": "DECAVISION EPAGNY",
    "ADRESSE": "145 ROUTE DE LA PRAIRE",
    "VILLE": "EPAGNY",
    "COMPAGNIE": "DECAVISION"
  }

