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
            - Les ransomwares: Technique qui bloque l'accés à un utilisateur sur un terminal ou à des données et à qui ont va demande une rancçon pour retrouver son accès. (Attention dans bien des cas rien ne garantie le retour à cet accès)
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

            - C'est controler les accés strcitement nécessaire à un utilisateur pour effectuer son travail ( typiquement reduire l'accés aux navigateurs internet)

    - AUTHENTIFICATION A DEUX FACTEURS (2FA)

            C'est le système de sécurisation en utilisant deux moyens de connections distings


## Les Contremesures


### Analyse d'attaques courantes

    Attaque par Deni de Service (DoS/DDoS)

        Attaque réalisées par une pertubation du traffic sur un service, un reseau ou un serveur. Cet action est mise en place à l'aide d'une _botnet_, c'est une armée de _bot_, qui est concentré sur la cible afin de la saturer. Chaque bot envoi des requêtes à l'adresse IP de la cible ce qui va saturer le traffic et provoquer un déni de service. 

        - IDENTIFICATION: 

            - 1 Quantité suspecte de requêtes provenant de la même adresse IP ou de la même plage d'adresse IP. 
            - 2 Flot de traffic provenant d'utilisateur présentant des similitudes, type même navigateur, même géolocalisation, même appareil utilisé. 
            - 3 Un comportement inhabituel du traffic comme des pics toutes les 10 min, à des horaires anormaux, ou sur des terminaisons innapropriées.

        - ATTAQUE DE LA COUCHE D'APPLICATION: 
        - ATTAQUE PROTOCOLAIRE
        - ATTAQUE VOLUMETRIQUE