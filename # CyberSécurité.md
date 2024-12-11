# Cyber-Sécurité

## Les bases de la sécurité

### Décourverte et receuil d'information

    - Qu'est ce que la Cybersécurité 

        - C'est l'ensemble des pratiques visant à protéger les systèmes, les données, les réseaux et les programmes contre des attaques numériques. 
        - Infrastructure 
        - Aplicatif
        - Utilisateur
       Ne pas mettre trop de sécurité si pas necessaire


    - L'importance de la sécurité informatique pour les entreprises 

        - Protéger les données et les accès afin de maintenir et perénniser l'activitée.

        - 3 entitées principales doivent être protégées: 

            - Les terminaux, les périphériques et les routeurs
            - Les réseaux
            - Le cloud

        - Contre les types de menace suivants:

            - Le phishing: C'est une technique qui consiste à voler des informations à un utilisateur par le biais d'un mail ressemblant à un mail de confiance.
            - Les ransomwares: Technique qui bloque l'accés à un utilisateur sur un terminal ou à des données et à qui ont va demander une rançon pour retrouver son accès. (Attention dans bien des cas rien ne garantie le retour à cet accès)
            - Le malware: Il s'agit d'un programme malveillant qui permet d'accéder à un espace sécurisé ou d'endommager un logiciel
            - L'ingénierie sociale: Le fait de se renseigner sur une personne ou de cibler une proie par son âge ses centre d'interets ses points de vue politiques. 

        - Il se distingue sur 4 axes: DICP
              
              - La confidentialité 
              - L'intégrité
              - La disponibilité
              - Preuves 

### Les Bonnes pratiques

    - Le MOT DE PASSE

        Comment bien sécuriser son mot de passe ? 

            - 1 At least 12 character long 
            - 2 Combination of letter, numbers, lowercase/ uppercase, symbols, special characters
            - 3 No personnal information 
            - 4 unique password for each account 
            - 5 use password acount manager
            - 6 Please not use PASSWORD 


    - LE WIFI

        Comment sécuriser son réseau wifi ? 


                -a utiliser une connection WPA3
                -b segmenter ses reseaux, un reseau dédié aux visiteur, et puis idéalement à chaque départements de l'entreprise. 
                -c Autoriser seulement les appareil avec une clé MAC
                -d mettre à jour son routeur

    - LA MISE A JOUR pour les systèmes d'exploitation ainsi que pour les système de gestion d'accés est capitale 

    - LE CONTROLE D'ACCES se base sur 4 types d'information d'identification  

            - 1 Quelque chose que vous avez (Contrôle d'accès par RFID) typiquement une carte à puce ou un porte clés.
            - 2 Quelque chose que vous savez (Contrôle d'accès par code NIP) plus ommunément appeler le code PIN
            - 3 Quelque chose que vous êtes (le scan d'empreinte digitale)
            - 4 le multi-facteur (Association de plusieurs méthode d'identification) le plus souvent par le biais de plusieurs support (couplage portable/ pc) 

    - LE PRINCIPE DE MOINDRE PRIVILEGE

            - C'est controler les accés strictement nécessaire à un utilisateur pour effectuer son travail ( typiquement reduire l'accés aux navigateurs internet)

    - AUTHENTIFICATION A DEUX FACTEURS (2FA)

            C'est le système de sécurisation en utilisant deux moyens de connections distings


## Les Contremesures


### Analyse d'attaques courantes

    A- Attaque par Deni de Service (DoS/DDoS)

        Attaque réalisées par une pertubation du traffic sur un service, un reseau ou un serveur. Cet action est mise en place à l'aide d'une _botnet_, c'est une armée de _bot_, qui est concentré sur la cible afin de la saturer. Chaque bot envoi des requêtes à l'adresse IP de la cible ce qui va saturer le traffic et provoquer un déni de service. 

        _bot_: Zombie, entité numérique piloté par un hacker 
        _botnet_: Armée de bots. 


        - IDENTIFICATION: 

            - 1 Quantité suspecte de requêtes provenant de la même adresse IP ou de la même plage d'adresse IP. 
            - 2 Flot de traffic provenant d'utilisateur présentant des similitudes, type même navigateur, même géolocalisation, même appareil utilisé. 
            - 3 Un comportement inhabituel du traffic comme des pics toutes les 10 min, à des horaires anormaux, ou sur des terminaisons innapropriées.

        - ATTAQUE DE LA COUCHE D'APPLICATION: Attaque de la couche 7, Il s'agit d'une attaque sur la dernière couche du modèle OSI, c'est la couche qui génére les visuels en reposne aux requêtes HTTP, il s'agit des attaques les plus difficiles à gérer parce qu'il est difficile de différencier les utilisateur BOT des vrais utilisateurs. Type d'attaque HTTP flood

        - ATTAQUE PROTOCOLAIRE: Attaque des couches 3 et 4 du modèle OSI, l'attaque a pour but ici de saturer non-plus les requêtes HTTP mais les demandes de connections TCP/IP qui permettent le transfert de paquets SYN. Type d'attaque SYN flood
        
        - ATTAQUE VOLUMETRIQUE: Attaque qui consiste à saturer l'IP d'une cible de requêtes DNS en utilisant des bots.

        - Attaque Multivecteur: lorsque on utilises plusieurs type d'attaque type attaque couche 7 et attaque couche 3/4. 


        - SOLUTIONS: 

            1 - Créer un trou noir pour rediriger les utilisateurs vers une sortie du serveur (solution type antibio qui tue les bonnes et mauvaise bacteries).
            2 - Filtrage - Gérer le taux des requêtes afin de limiter le nombre de requête qu'un srveur peu accepter pendant un moment. Efficace pour ralentir les bot mais suffira pas à elle seule pour gérer l'attaque. 
            3 - Déployer un WAF rules qui permet d'appliquer des régles de requêtes personnalisées entre internet et le serveur. 
            4 - Diviser le reseau principale en plusieurs reseaux. CDN




    B - Man-in-the-Middle (MITM)



        - C'est une attaque ou le hacker se positionne entre deux entités numériques, afin de décrypter les message, les lires et les modifiers. 

    Plus présentent sur les supports mobiles lors de connections vers des reseaux externes (type wifi aeroport, publi, etc) il faut s'assurer de toujours surfer sur des sites HTTPS. 

    Faire attention aux e-mails phishing avec des pièces jointes ou des liens, ne jamais cliquer sur des liens ou ouvrir des pièces jointes. 

    Eviter de se connecter aux wifi publics. 

    S'assurer que son reseau wifi est proitégé avec un mot de passe FORT, pour possiblement ajuster une selection des appareils autorisés à se connécter avec le code MAC. 




    C - injection SQL

        - Attaque suite à une vulnérabilité SQL d'un site ou d'une base de données. Le hacker execute une requête SQL au niveau de la vulnérabilité type modification du password du user N°1. Lui permettant d'obtenir des accès ainsi que des autorisations fortes (les admins sont souvent les premiers de la liste d'employés)


    Utiliser des listes blanches plutôt que des black lists 

    Utiliser les derniers technologies et programme en fonction des codes utilisées //     Utiliser un Framework recent  avec des requêtes préparées


    Ne jamais faire confiance dans une requête utilisateur qu'elle soit interne ou externe. 




    D - Cross-Site Scripting (XSS)

        - Intégrer une attaque dans le code html d'une page. 
        - Controler la taille de champs le type de characères
        - Utiliser le Framework, ne pas faire confiance à ses utilisateurs. 


## LA DEFENSE EN PROFONDEUR
NE JAMAIS REPOSER TOUTE SA DEFENCE SUR UNE STRATEGIE AVOIR TOUJOURS AU MOINS DEUX SOLUTIONS

En TEMPS QUE DEVELOPEUR JE DOIS CONTROLER A CHAQUE FOIS QU'IL Y A UNE INTERFACE DONNEE ENTRE L'EXTERIEUR ET LE SERVEUR 

 Smith' OR '1' = '1'; GRANT UPDATE ON TABLE employees TO unauthorized_user; UPDATE employees set salary = 100000 WHERE FIRST_NAME = 'John'; -- 


 Smith' OR '1' = '1'; GRANT UPDATE ON TABLE employees TO unauthorized_user; UPDATE employees set salary = 100000 WHERE FIRST_NAME = 'John'; -- 

 *' OR '1' = '1'; DROP TABLE access_log; --

 eyJhbGciOiJIUzUxMiJ9.eyJpYXQiOjE3MzQ3OT
 I4Nz
 MsImFkbWluIjoiZmFsc2UiLCJ1c2VyIjoi
 U3lsdmVzdGVyIn0.fYpVMWaMev8Q_DVJWaELS3kGXcjAOfhhFtENJjPOZV9fsmVTkMKfqwnPcM0sCzSnBN3GWrRyygqRXt3GOFCqhQ

 eyJhbGciOiJIUzUxMiJ9.eyJpYXQiOjE3MzQ3OT
 MzNj
 MsImFkbWluIjoiZmFsc2UiLCJ1c2VyIjoi
 VG9tIn0.BIrSC3aqtnlI-E05RiSoWxjwtyfyRQhmGkEoBEwo4Fn3J49KoqOTB2pu7TGt4qN5SnVqqGTQXyjw1uFCCeLY5g;

 