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

![Schema BDD](/home/rodolphe-delory/Images/Schema_BDD_websites.png "Schema BDD").




