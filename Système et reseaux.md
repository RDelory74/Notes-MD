# Système Reseaux

#### Me connecter au serveur Ngnix via SSH : 

 ssh rodolphe@212.47.230.222

 Puis dans le dossier /var/www/



Pour vous, qu’est ce qu’un réseau ?

        Un lien entre plusieurs entité numériques pour transférer de l'information.

Quel est le lien entre la notion de réseau et Internet?

        Un reseau c'est les liens dans une infrastructure, alors que le reseau internet est un lien vers l'exterieur (un reseau de reseau)

Quelle est la différence entre Internet et le Web ? Ou a-t-il été inventé ?(Tips : c’est pas si loin d’où vous êtes )

        Il a été inventer au CERN. Internet c'est l'ensemble des liens qui relient les entités au niveau mondial, le web c'est le support et le moyen de transfer de données (inventé au CERN).

Quels sont les différents types de réseaux informatiques ? Pour chaque type de réseau, donner un exemple concret.

Reponse de Chat GPT qui m'a semblée la plus fournie et la plus pertinente:

        Les différents types de réseaux informatiques sont classés principalement selon leur taille, leur portée et leur objectif. Voici les principaux types de réseaux et des exemples concrets pour chacun :

    1. Réseau Local (LAN - Local Area Network)
    Un réseau LAN connecte des ordinateurs et des périphériques dans une petite zone géographique, comme un bâtiment ou un campus, sur une courte distance. Il utilise généralement des câbles Ethernet ou des connexions Wi-Fi.

     Exemple : Le réseau informatique d'une entreprise ou d'une école qui connecte des ordinateurs, des imprimantes et des serveurs sur un même site.

    2. Réseau Métropolitain (MAN - Metropolitan Area Network)
    Un réseau MAN couvre une ville ou une agglomération, reliant plusieurs réseaux LAN. Il peut être utilisé pour connecter des entreprises ou des institutions réparties dans une ville.

        Exemple : Le réseau qui interconnecte plusieurs campus universitaires situés dans une même ville.

    3. Réseau Étendu (WAN - Wide Area Network)
    Un réseau WAN relie des réseaux sur une vaste zone géographique, comme un pays ou même à l'échelle mondiale. L'Internet est le plus grand exemple de WAN.

        Exemple : Le réseau informatique d'une multinationale qui relie ses bureaux dans différents pays.

    4. Réseau Personnel (PAN - Personal Area Network)
    Un réseau PAN relie des dispositifs personnels à courte portée, généralement sur quelques mètres. Il est souvent utilisé pour connecter des appareils comme des téléphones, tablettes, et ordinateurs via Bluetooth ou Wi-Fi.

        Exemple : La connexion entre un smartphone et une montre connectée via Bluetooth.

    5. Réseau Local Sans Fil (WLAN - Wireless Local Area Network)
    Un WLAN est une version sans fil du réseau local (LAN), utilisant principalement des technologies sans fil comme le Wi-Fi pour connecter des appareils dans une zone définie, comme un bâtiment ou un campus.

        Exemple : Le réseau Wi-Fi dans un café ou dans une maison qui permet à plusieurs utilisateurs de se connecter à Internet sans fil.

    6. Réseau d'Entreprise (Enterprise Network)
    Un réseau d'entreprise est un réseau informatique interne à une organisation, conçu pour connecter différents services et départements. Ce réseau peut inclure des éléments de LAN, WAN et MAN.

        Exemple : Le réseau interne d'une grande entreprise comme Google, qui relie ses centres de données, ses bureaux dans le monde entier, ainsi que ses employés.

    7. Réseau de Stockage (SAN - Storage Area Network)
    Un SAN est un réseau spécialisé, conçu pour fournir un accès à des ressources de stockage de données sur des serveurs. Il est utilisé dans les centres de données et les grandes entreprises pour gérer les grands volumes de données.

        Exemple : Un réseau SAN dans un centre de données pour gérer les serveurs de stockage qui hébergent les bases de données d'une banque.

    8. Réseau Virtuel Privé (VPN - Virtual Private Network)
    Un VPN est un réseau sécurisé qui utilise une connexion Internet publique pour permettre aux utilisateurs d'accéder à un réseau distant comme s'ils étaient physiquement connectés à celui-ci, tout en protégeant leurs données.

        Exemple : Un employé travaillant depuis chez lui utilise un VPN pour se connecter au réseau interne de son entreprise et accéder à des fichiers confidentiels.

    9. Réseau Peer-to-Peer (P2P - Peer-to-Peer Network) // Pas vraiment un reseau //
    Dans un réseau P2P, chaque appareil connecté au réseau peut agir à la fois comme client et comme serveur. Il n'y a pas de serveur centralisé, et les appareils partagent directement des ressources entre eux.

        Exemple : Les réseaux de partage de fichiers tels que BitTorrent, où les utilisateurs échangent des données directement sans passer par un serveur centralisé.

    Chaque type de réseau est adapté à des besoins spécifiques en termes de distance, de sécurité, de vitesse et de coût.

Quels sont les principaux équipements physiques d’un réseau LAN?

    des ordinateurs,
    des imprimantes et
    des serveurs,
    une box de connection,
    un routeur,
    cable,  //cable droit // cable croisé
    switch
    point d'accés

Les differents cables ethernet:

    Les câbles Ethernet peuvent être de deux types principaux : câble droit et câble croisé. La différence entre eux réside dans la manière dont les fils internes sont connectés entre les deux extrémités du câble. Ils sont utilisés pour des connexions spécifiques en fonction du type d'équipement à connecter.

    1. Câble Ethernet droit (Straight-through cable)
    Le câble droit est le plus couramment utilisé. Il est conçu pour connecter des appareils de type différent (par exemple, un ordinateur à un commutateur, un routeur, ou une box Internet).

    Caractéristiques :
    Dans un câble droit, les paires de fils à l'intérieur du câble sont connectées de la même manière à chaque extrémité, selon le standard de câblage TIA/EIA 568A ou TIA/EIA 568B.
    La disposition des fils suit la même séquence de couleurs aux deux extrémités du câble.
    Utilisation :
    PC à commutateur (switch).
    PC à routeur.
    PC à point d'accès Wi-Fi.
    Commutateur à routeur.
    Exemple de câblage droit :
    Si vous suivez le standard TIA/EIA 568B, voici la disposition des fils :

    markdown
    Copier le code
    Extrémité 1       Extrémité 2
    1. Blanc/Orange   ->  Blanc/Orange
    2. Orange         ->  Orange
    3. Blanc/Vert     ->  Blanc/Vert
    4. Bleu           ->  Bleu
    5. Blanc/Bleu     ->  Blanc/Bleu
    6. Vert           ->  Vert
    7. Blanc/Marron   ->  Blanc/Marron
    8. Marron         ->  Marron
    Les deux extrémités sont câblées de manière identique.

    2. Câble Ethernet croisé (Crossover cable)
    Le câble croisé est conçu pour connecter des appareils de même type directement entre eux, sans passer par un commutateur ou un routeur.

    Caractéristiques :
    Dans un câble croisé, les paires de fils sont croisées à une extrémité. Cela signifie que certains fils qui transportent les données d'envoi à une extrémité sont connectés aux fils qui transportent les données de réception à l'autre extrémité.
    Il utilise une combinaison des standards TIA/EIA 568A et TIA/EIA 568B. Typiquement, l'une des extrémités suit le standard 568A, et l'autre le 568B.
    Utilisation :
    PC à PC (sans commutateur).
    Commutateur à commutateur (dans certains cas).
    Routeur à routeur (dans certains cas).
    Exemple de câblage croisé :
    Si l'une des extrémités suit le standard TIA/EIA 568A et l'autre suit le TIA/EIA 568B, cela ressemble à ceci :

    markdown
    Copier le code
    Extrémité 1 (TIA/EIA 568A)     Extrémité 2 (TIA/EIA 568B)
    1. Blanc/Vert   ->  Blanc/Orange
    2. Vert         ->  Orange
    3. Blanc/Orange ->  Blanc/Vert
    4. Bleu         ->  Bleu
    5. Blanc/Bleu   ->  Blanc/Bleu
    6. Orange       ->  Vert
    7. Blanc/Marron ->  Blanc/Marron
    8. Marron       ->  Marron
    Le croisement se produit entre les fils 1/3 et 2/6 pour permettre la transmission directe des données entre appareils similaires.

    Exemple concret d'utilisation :
    Câble droit : Si vous voulez connecter votre PC à un routeur, vous utiliseriez un câble droit pour permettre la communication entre votre PC et l'Internet via le routeur.
    Câble croisé : Si vous voulez connecter directement deux PC entre eux sans utiliser de commutateur ou de routeur, vous utiliseriez un câble croisé pour permettre l'échange direct de données.
    Aujourd'hui, de nombreux équipements modernes, tels que les commutateurs, les routeurs et les cartes réseau, sont capables de détecter automatiquement le type de câble utilisé (câble droit ou croisé) grâce à la technologie Auto-MDI/MDI-X, ce qui rend souvent l'utilisation spécifique de câbles croisés moins nécessaire. Cependant, connaître la différence reste important dans certains contextes.

Qu’est ce que la commande ping ? A quoi sert-elle ?

    La commande ping de premier abord me semblerait être une requête de connection pour tester cette dernière, elle permet de:

        Tester la disponibilité d'une machine sur un réseau.
        Mesurer la latence d'une connexion.
        Diagnostiquer les problèmes de connectivité.

Test de ping:

    ~/Notes-MD main* ❯ ping google.com                                                                                                                          09:53:32
    PING google.com (172.217.20.174) 56(84) bytesuof data.
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=1 ttl=116 time=11.8 ms
    64 bytes from waw02s07-iu-f174.1e100.net (172.217.20.174): icmp_seq=2 ttl=116 time=11.7 ms
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=3 ttl=116 time=11.7 ms
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=4 ttl=116 time=11.8 ms
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=5 ttl=116 time=11.9 ms
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=6 ttl=116 time=11.7 ms
    64 bytes from waw02s07-in-f174.1e100.net (172.217.20.174): icmp_seq=7 ttl=116 time=12.6 ms


    ~/Notes-MD main* ❯ ping 192.0.2.255                                                                                                                      6s 12:05:18
    PING 192.0.2.255 (192.0.2.255) 56(84) bytes of data.

    --- 192.0.2.255 ping statistics ---
    35 packets transmitted, 0 received, 100% packet loss, time 34828ms

    ~/Notes-MD main* ❯ ping 172.217.20.174                                                                                                                      12:07:42
    PING 172.217.20.174 (172.217.20.174) 56(84) bytes of data.
    64 bytes from 172.217.20.174: icmp_seq=1 ttl=116 time=12.1 ms
    64 bytes from 172.217.20.174: icmp_seq=2 ttl=116 time=11.7 ms

    --- 172.217.20.174 ping statistics ---
    2 packets transmitted, 2 received, 0% packet loss, time 1001ms
    rtt min/avg/max/mdev = 11.715/11.886/12.057/0.171 ms

Quelles sont les machines / types de machines qui vont intervenir dans ce réseau ?

       1. Réseau Local (LAN - Local Area Network)
    Un réseau LAN connecte des ordinateurs et des périphériques dans une petite zone géographique, comme un bâtiment ou un campus, sur une courte distance. Il utilise généralement des câbles Ethernet ou des connexions Wi-Fi.

     Exemple : Le réseau informatique d'une entreprise ou d'une école qui connecte des ordinateurs, des imprimantes et des serveurs sur un même site.

Quel type de support de communication choisir ?(câble cuivre, fibre optique, Sans-fil…)

    Cable ethernet, fibre optique et wifi pour certain appareils

Comment les machines sont identifiées au sein d’un réseau ?

    Grace à leur IP

Qu’est ce qu’une interface réseau ?

    Le programme ou le logiciel à l'interieur d'une machine pour quelle puisse se connecter, type:

    C'est le composant qui permet de connécter un appareil à un autre.

    Carte Ethernet : Permet de se connecter à un réseau via un câble Ethernet (filaire).
    Carte Wi-Fi : Permet de se connecter à un réseau sans fil (Wi-Fi).
    Modem 4G/5G : Permet de se connecter à un réseau mobile.

Qu’est ce qu’une adresse MAC ?

    00:1B:44 est l'identifiant du fabricant (OUI).
    11:3A:B7 est l'identifiant unique de l'appareil.

    Une adresse MAC (Media Access Control) est un identifiant unique attribué à chaque interface réseau d'un appareil connecté à un réseau, que ce soit via Wi-Fi ou par un câble Ethernet. Elle permet de distinguer chaque périphérique sur un réseau local (LAN) et est utilisée pour la communication au niveau de la couche liaison de données (couche 2) du modèle OSI.

    Caractéristiques de l'adresse MAC :
    Longueur : Elle est composée de 48 bits (6 octets), généralement représentée sous forme de 12 caractères hexadécimaux séparés par des deux-points ou des tirets (par exemple : 00:1A:2B:3C:4D:5E ou 00-1A-2B-3C-4D-5E).
    Unicité : Chaque adresse MAC est censée être unique et est attribuée par le fabricant de l'interface réseau. Les trois premiers octets de l'adresse identifient le fabricant (c'est l'OUI ou Organizationally Unique Identifier), tandis que les trois derniers octets sont spécifiques à l'appareil.
    Inaltérable (en principe) : L'adresse MAC est normalement inscrite physiquement (hard-coded) dans la carte réseau (NIC - Network Interface Controller). Cependant, il est possible de modifier (ou "spoof") l'adresse MAC sur certains systèmes pour des raisons de confidentialité ou de diagnostic.

Qu’est ce qu’une adresse IP ? Comment peut-on la paramétrer ?

    C'est un identifiant propre à chaque appereil sur un reseau, 2 versions ipv4  et ipv6.

    Dynamique ou static, idresse IP d'une box n'est pas fixe.
    Soit on les paramètre manuel (via administrateur reseau), ou alors en dynamiquement

    Dans l'interface du terminal on tape ping (un nom de domaine) pour le test de connection

//
Soit l’adresse réseau suivante : 192.168.1.0

Quel est son masque ? /24
Combien d’adresses IP peut-on attribuer dans ce réseau. Attention, il y a un piège : faite une recherche sur l’adresse IP de broadcast

    254 adresses IP peuvent être adréssée à ce réseau.

//
Soit les adresses ip suivantes : 192.168.1.1/24 et 192.168.24.3/24

Sont-elles sur le même réseau ?
Quelles sont les adresses réseaux respectives ?

    Non nous allons avoir l'adresse réseau (192.168.1.) ainsi que l'adresse reseau (192.168.24.)

Enfin pour compléter cet exercice on constate que le paquet fait le chemin depuis un pc d'Orion vers le switch (sociéte Orion) pui vers le routeur puis vers le switch (société StarLit) pour arriver enfin au serveur. Le ping reviens ensuite par le même chemoin vers le pc Orion émetteur.

OSI et TCP/IP

    Modèle OSI: Il est composé de 7 couches ( 7 règles d'harmonisation ) c'est le modèle academique


         -  Physique : Transmission des bits (électrique, optique).

- Le cable ethernet ou le wifi

      -  Liaison de données : Envoi de trames entre deux machines reliées.

- La carte réseau ou carte wifi ou le switch qui interprètre les données ( un cadre ou frame ) c'est ici qu'intervient l'adresse MAC

  - Réseau : Routage des paquets entre réseaux (ex: IP).

- Le routeur il dispatch l'information en fonction des adresses IP

  - Transport : Assure la livraison fiable des données (ex: TCP).

- Les numéros de port, les differents flux du reseau, en fonction du service,elle va rediriger les requêtes au travers des differents ports.

  - Session : Gère les connexions entre deux applications.

- Initier une session avec la destination afin d'échanger des données.

  - Présentation : Traduction des formats de données.

- Présentation des données dans un language adapter à l'interface, (ex: chiffrement)

  - Application : Interface utilisateur (ex: HTTP, FTP).

- Le navigateur web, la dernière couche de l'utilisateur.

Le TCP/IP reprend le même modèle que OSI sauf qu'il va compacter les couches 5 à 7.

Encapsulation / decapsulation : c'est l'ajout d'entête à chaque étape de la transmission des données

    La couche 4 ajoute un en-tête TCP (numero de port source et destination)
    La couche 3 ajoute l'adresse IP (source et destination)
    La couche 2 ajoute en-tête ethernet qui incluera l'adresse MAC (source et destination)

Elle s'encapsule vers la destination et se decapsule vers la source. Il y a toujours une notions d'aller retour.

Le TCP/IP est responsable du hashage des données avant des encapsuler.

Concernant l'exemple StarLit et Orion, nous avons pour chacun des support les couches suivantes:

    Pc: Couche de niveau 7
    Switch: couche de niveau 2
    Routeur: couche de niveau 3
    Serveur: Couche de niveau 7
    Cables:Couche de niveau 1
    Navigateur ou explorateur: Couche de niveau 7
    Carte reseau et ou carte wifi : Couche de niveau 2

Le DNS:

Le DNS (Domain Name System) est un système utilisé pour traduire les noms de domaine lisibles par l'homme (comme www.example.com) en adresses IP compréhensibles par les machines (comme 192.168.1.1). Cela permet aux utilisateurs d'accéder à des sites web sans avoir à retenir des adresses IP. Un exemple concret est lorsque vous tapez "www.google.com" dans votre navigateur, le DNS résout ce nom en une adresse IP spécifique pour permettre la connexion au serveur web de Google.

    Quel est l’ordre des actions (Requête/Réponse DNS, ping) effectuées pour réaliser lorsque, depuis le PC10, j’utilise la commande ping PC11 ? Attention : le PC10 ne connaît pas l’adresse IP de PC11.

    On utilise un serveur DNS à qui on envoi un ping avec une url qu'il va convertir en IP puis qu'il va renvoyer pour qu'on puisse accéder au site en question.

Le Protocole HTTP, c’est quoi ?

Qu’est ce qu’une API (et plus spécifiquement une API REST)?

Qu'est-ce qu'une API ?
Une API est un ensemble de définitions et de protocoles qui facilite la création et l'intégration de logiciels d'applications. Elle est parfois considérée comme un contrat entre un fournisseur d'informations et un utilisateur d'informations, qui permet de définir le contenu demandé au consommateur (l'appel) et le contenu demandé au producteur (la réponse).

REST
REST est un ensemble de contraintes architecturales. Il ne s'agit ni d'un protocole, ni d'une norme. Les développeurs d'API peuvent mettre en œuvre REST de nombreuses manières.

Qu’est ce que le protocole HTTP ?
Quelles sont les méthodes disponibles avec le protocole HTTP ? CRUD
Quelle est la différence entre le protocole HTTP et le protocole HTTPS ? La sécruité
Qu’est ce qu’un Bearer token ? un token qui permet l'acces en GEt à une URL

Exo HTTP

Route 1:  
Route 2: https://http-exercice.williamburillon.com/api/route-2/?favoritePokemon=pikachu&favoritePokemon=Bulbizarre
Route 3: https://http-exercice.williamburillon.com/api/route-3/
Route 4: https://http-exercice.williamburillon.com/api/route-4/
Route 5: https://http-exercice.williamburillon.com/api/route-5/
Route 6: https://http-exercice.williamburillon.com/api/route-6/?user_id=integer
Route 7: https://http-exercice.williamburillon.com/api/route-7/value1/value2
Route 8: https://http-exercice.williamburillon.com/api/route-8/
Route 9: https://http-exercice.williamburillon.com/api/register
https://http-exercice.williamburillon.com/api/login

         Manipuler toutes le foncitons de postman et les URL

SSH

https://doc.fedora-fr.org/wiki/SSH_:_Authentification_par_cl%C3%A9

Protocoles remplacés par SSH : SSH (Secure Shell) a remplacé des protocoles comme Telnet, rlogin, FTP et rsh, qui transmettaient les données en clair sur le réseau, ce qui les rendait vulnérables aux interceptions.

Différents modes d'utilisation de SSH (sécurité) :

Authentification par mot de passe : Moins sécurisé, car vulnérable aux attaques par force brute.
Authentification par clé publique/privée : Méthode recommandée. Le client utilise une clé privée pour prouver son identité, et le serveur vérifie à l’aide d’une clé publique.
Tunnels SSH : Permet de chiffrer le trafic entre le client et le serveur pour protéger d'autres services (ex : port forwarding).
SSH agent forwarding : Permet d'utiliser des clés SSH sur des machines distantes sans les transférer.
Connexion SSH sécurisée (schéma simplifié) :

Client Serveur
|--- Génération d'une paire de clés (privée/publique) --|
|--- Envoie la clé publique --------------------------->|
|<-- Challenge (chiffrement avec la clé publique) -------|
|--- Réponse (déchiffrement avec la clé privée) -------->|
|--- Connexion sécurisée établie -----------------------|

Fermer le serveur: 

    sudo shutdown

redémarrer le serveur: 

    shutdown -r now // immediatement; shutdown -r 5 // dans 5 min

La connexion se fait via une vérification mutuelle entre la clé privée du client et la clé publique du serveur, assurant une connexion chiffrée.

Commande linux pour créer une clé ssh public et privée, elle va être ensuite créée dans un dossier avec les fichiers suivants: 

    $ ssh-keygen -t 

    id_e2548
    id_e2548.pub
    id_rsa
    id_rsa.pub
    authorised_keys


Catégorie	Ligne de commande

Navigation et Gestion de Fichiers	

    ls  //affiche le contenu du dossier 
    cd  // se déplacer 
    pwd //afficher le path

Manipulation de Fichiers et de Répertoires

    cp  // copier
    mkdir   // créer un dosssier    
    touch   //créer un fichier
    mv  // mv déplacer ou renomer un dossier ou un fichier
    rm  // supprimer

Affichage et lecture de contenu de fichier

    cat // prévisualiser
    less    // prévisualise un fichier d'avant en arrière possible
    find    // trouve un fichier 
    grep    // trouve un terme dans un fichier et l'affiche

Transfert et Synchronisation de Fichiers

    scp     //transféré des ficchier entre serveurs et machine  /scp -p root@162.168.1.1:/media/scp.png hostinger@162.168.1.2:/bureau/destination
    rsync   //  permet de transférer et mettre à jour des fichiers // rsync  version 3.1.2  protocol version 31

Éditeur de Texte	

    vim // vim /chemin/texte éditer un texte
    nano    // parcourir et modifier un texte

Generating public/private rsa key pair.


Enter file in which to save the key (/home/rodolphe-delory/.ssh/id_rsa):                                                
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/rodolphe-delory/.ssh/id_rsa
Your public key has been saved in /home/rodolphe-delory/.ssh/id_rsa.pub
The key fingerprint is:

    SHA256:vGhjZ2VQUfDdTZvppVDLuhsMgHH4HnmUE3Su3suEJkI rodolphe-delory@rodolphe-delory-HP-CNA-102

The key's randomart image is:

+---[RSA 3072]----+
|      ....**o . .|
|      .+ .++ + +=|
|      ..oo .+ +++|
|       .+o.. o...|
|      E.So= . .. |
|     . ..= = .   |
|      * = + *    |
|     o = o o +   |
|            +    |
+----[SHA256]-----+




https://www.hostinger.fr/tutoriels/generer-cle-ssh

Connection à un serveur SSH: 
Configurer son serveur 
https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04

Ici on s'assure que le firewall est bien activée et qu'il laisse OpenSSH taffer

Installation de Nginx
https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-on-ubuntu-20-04-fr

NGINX

Serveur Web : Nginx est capable de traiter des fichiers statiques tels que HTML, CSS, JavaScript et images, ainsi que de gérer des requêtes HTTP/HTTPS. Il est célèbre pour sa rapidité et son efficacité dans la gestion simultanée de plusieurs connexions.

Reverse Proxy : Nginx peut être configuré en tant que proxy inverse afin de rediriger le trafic HTTP/HTTPS vers des serveurs d'application ou des serveurs web backend. Cela facilite la répartition du trafic, la gestion de la mise en cache et l'amélioration de la sécurité.

Équilibrage de charge : l'équilibrage de charge peut être effectué par Nginx en répartissant les requêtes entre plusieurs serveurs backend. Cela permet de répartir la charge sur plusieurs serveurs, ce qui augmente la disponibilité et les performances.

Gestion des certificats SSL/TLS : Nginx prend en charge le chiffrement SSL/TLS, ce qui permet aux clients et aux serveurs web de sécuriser les communications. Il est également possible de configurer des certificats SSL, tels que Let's Encrypt, avec cet outil.

Redirections et gestion des connexions : Nginx est un excellent choix pour les sites web avec beaucoup de connexions simultanées. Il est également capable de configurer des redirections HTTP, y compris les redirections permanentes (301) et temporaires (302).

Règles de routage URL : la configuration de règles de routage basées sur les URL permet de diriger les requêtes vers différents endroits en fonction des chemins d'URL.

PHP FPM

PHP-FPM, ou « PHP FastCGI Process Manager », est un gestionnaire de processus FastCGI avancé et performant pour PHP. Il résout le problème de concurrence du serveur intégré de PHP en générant plusieurs workers, qui peuvent gérer plusieurs requêtes simultanément.

En gros et dans mon language, Nginx va permettre gérer le serveur les requêtes les ports ainsi que l'attribution des IP, il va permettre aussi la gestion des reverse vers d'autres servers afin de mieux gérer les flux. Il est principalement utilisé pour les site à lourdes charges. *
Et PHP-FPM, est lui un gestionnaire avancé qui va permettre à Nginx de traité des requêtes via des fichiers .php (pour rappel à la nginx ne peu traiter que des fichiers HTML/CSS/Javascript et Images), ci-dessous le code à implémenter dans le fichier: 

    etc/nginx/conf.d/nomdusite.conf

article super interressant qui explique bien tout: 
https://medium.com/@mgonzalezbaile/demystifying-nginx-and-php-fpm-for-php-developers-bba548dd38f9


/home/rodolphe-delory/Images/Captures d’écran/


Il est nécessaire de configurer nginx: 

Création d'un fichier /var/www/ dans lequel tu mets ton site pis après tu configure le fichier 'nom du site' qui se trouve à l'adresse:

Se positionner dans le dossier /var/www/ puis Utilisation de Git clone du HTTP du projet sur github

    /etc/nginx/sites-availables

    puis tu fais un sudo nano du fichier du site: 


##### Autorise l'ouverture des ports :sudo ufw allow 81


 server {
        listen 80;
        server_name 212.47.230.222;

       root /var/www/datahive;
        index index.php index.html index.htm;

        location / {
            try_files $uri $uri/ =404;
        }

        location ~ \.php$ {
            include snippets/fastcgi-php.conf;
            fastcgi_pass unix:/run/php/php7.4-fpm.sock;
        }

        location ~ /\.ht {
            deny all;
        }
    }

Quelles sont les problématiques qui vont survenir par rapport à la gestion des différents code source (notamment par rapport à la diversité des technologies)?

Le problème lorsque l'on fait fonctionner plusieurs sites sur le même serveur c'est s'il y en a un qui merde et que l'on doit faire de la maintenance, ça peut bloquer tous les autres, on a donc un problème d'isolation entre les domaines.


# Certificats TLS/SSL

https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-20-04-fr

Obtenir un domaine sécure HTTPS





Le hacking: 

En 4 phases 

- La reconnaissance :

- Le scan : le port 20 / le port 22 (pour la ssh) le port 25: SNTP /  HTTP: port 8080  / HTTPS: 443 // Une des bonnes pratiques c'est de changer les ports          standardisés. 

- L'exploitation : 

- Maintient: 

rodolphe@server-delory:/etc/nginx/sites-enabled$ cd
rodolphe@server-delory:~$ sudo apt install certbot python3-certbot-nginx
[sudo] password for rodolphe: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  python3-acme python3-certbot python3-configargparse python3-icu python3-josepy python3-parsedatetime python3-requests-toolbelt python3-rfc3339 python3-zope.component
  python3-zope.event python3-zope.hookable
Suggested packages:
  python-certbot-doc python3-certbot-apache python-acme-doc python-certbot-nginx-doc
The following NEW packages will be installed:
  certbot python3-acme python3-certbot python3-certbot-nginx python3-configargparse python3-icu python3-josepy python3-parsedatetime python3-requests-toolbelt python3-rfc3339
  python3-zope.component python3-zope.event python3-zope.hookable
0 upgraded, 13 newly installed, 0 to remove and 38 not upgraded.
Need to get 993 kB of archives.
After this operation, 5077 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-josepy all 1.10.0-1 [22.0 kB]
Get:2 http://archive.ubuntu.com/ubuntu jammy/main amd64 python3-requests-toolbelt all 0.9.1-1 [38.0 kB]
Get:3 http://archive.ubuntu.com/ubuntu jammy/main amd64 python3-rfc3339 all 1.1-3 [7110 B]
Get:4 http://archive.ubuntu.com/ubuntu jammy-updates/universe amd64 python3-acme all 1.21.0-1ubuntu0.1 [36.4 kB]
Get:5 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-configargparse all 1.5.3-1 [26.9 kB]
Get:6 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-parsedatetime all 2.6-2 [32.9 kB]
Get:7 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-zope.hookable amd64 5.1.0-1build1 [11.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-zope.event all 4.4-3 [8180 B]
Get:9 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-zope.component all 4.3.0-3 [38.3 kB]
Get:10 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-certbot all 1.21.0-1build1 [175 kB]
Get:11 http://archive.ubuntu.com/ubuntu jammy/universe amd64 certbot all 1.21.0-1build1 [21.3 kB]
Get:12 http://archive.ubuntu.com/ubuntu jammy/universe amd64 python3-certbot-nginx all 1.21.0-1 [35.4 kB]
Get:13 http://archive.ubuntu.com/ubuntu jammy/main amd64 python3-icu amd64 2.8.1-0ubuntu2 [540 kB]
Fetched 993 kB in 0s (7165 kB/s)  
Preconfiguring packages ...
Selecting previously unselected package python3-josepy.
(Reading database ... 102321 files and directories currently installed.)
Preparing to unpack .../00-python3-josepy_1.10.0-1_all.deb ...
Unpacking python3-josepy (1.10.0-1) ...
Selecting previously unselected package python3-requests-toolbelt.
Preparing to unpack .../01-python3-requests-toolbelt_0.9.1-1_all.deb ...
Unpacking python3-requests-toolbelt (0.9.1-1) ...
Selecting previously unselected package python3-rfc3339.
Preparing to unpack .../02-python3-rfc3339_1.1-3_all.deb ...
Unpacking python3-rfc3339 (1.1-3) ...
Selecting previously unselected package python3-acme.
Preparing to unpack .../03-python3-acme_1.21.0-1ubuntu0.1_all.deb ...
Unpacking python3-acme (1.21.0-1ubuntu0.1) ...
Selecting previously unselected package python3-configargparse.
Preparing to unpack .../04-python3-configargparse_1.5.3-1_all.deb ...
Unpacking python3-configargparse (1.5.3-1) ...
Selecting previously unselected package python3-parsedatetime.
Preparing to unpack .../05-python3-parsedatetime_2.6-2_all.deb ...
Unpacking python3-parsedatetime (2.6-2) ...
Selecting previously unselected package python3-zope.hookable.
Preparing to unpack .../06-python3-zope.hookable_5.1.0-1build1_amd64.deb ...
Unpacking python3-zope.hookable (5.1.0-1build1) ...
Selecting previously unselected package python3-zope.event.
Preparing to unpack .../07-python3-zope.event_4.4-3_all.deb ...
Unpacking python3-zope.event (4.4-3) ...
Selecting previously unselected package python3-zope.component.
Preparing to unpack .../08-python3-zope.component_4.3.0-3_all.deb ...
Unpacking python3-zope.component (4.3.0-3) ...
Selecting previously unselected package python3-certbot.
Preparing to unpack .../09-python3-certbot_1.21.0-1build1_all.deb ...
Unpacking python3-certbot (1.21.0-1build1) ...
Selecting previously unselected package certbot.
Preparing to unpack .../10-certbot_1.21.0-1build1_all.deb ...
Unpacking certbot (1.21.0-1build1) ...
Selecting previously unselected package python3-certbot-nginx.
Preparing to unpack .../11-python3-certbot-nginx_1.21.0-1_all.deb ...
Unpacking python3-certbot-nginx (1.21.0-1) ...
Selecting previously unselected package python3-icu.
Preparing to unpack .../12-python3-icu_2.8.1-0ubuntu2_amd64.deb ...
Unpacking python3-icu (2.8.1-0ubuntu2) ...
Setting up python3-configargparse (1.5.3-1) ...
Setting up python3-requests-toolbelt (0.9.1-1) ...
Setting up python3-parsedatetime (2.6-2) ...
Setting up python3-icu (2.8.1-0ubuntu2) ...
Setting up python3-zope.event (4.4-3) ...
Setting up python3-zope.hookable (5.1.0-1build1) ...
Setting up python3-josepy (1.10.0-1) ...
Setting up python3-rfc3339 (1.1-3) ...
Setting up python3-zope.component (4.3.0-3) ...
Setting up python3-acme (1.21.0-1ubuntu0.1) ...
Setting up python3-certbot (1.21.0-1build1) ...
Setting up certbot (1.21.0-1build1) ...
Created symlink /etc/systemd/system/timers.target.wants/certbot.timer → /lib/systemd/system/certbot.timer.
Setting up python3-certbot-nginx (1.21.0-1) ...
Processing triggers for man-db (2.10.2-1) ...
Scanning processes...                                                                                                                                                                   
Scanning linux images...                                                                                                                                                                

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
rodolphe@server-delory:~$ sudo nano /etc/nginx/sites-available/CV
rodolphe@server-delory:~$ sudo nano /etc/nginx/sites-available/CV
rodolphe@server-delory:~$ sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
rodolphe@server-delory:~$ sudo systemctl reload nginx
rodolphe@server-delory:~$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere                  
Nginx HTTP                 ALLOW       Anywhere                  
81                         ALLOW       Anywhere                  
OpenSSH (v6)               ALLOW       Anywhere (v6)             
Nginx HTTP (v6)            ALLOW       Anywhere (v6)             
81 (v6)                    ALLOW       Anywhere (v6)             

rodolphe@server-delory:~$ sudo ufw allow 'Nginx Full'
sudo ufw delete allow 'Nginx HTTP'
Rule added
Rule added (v6)
Rule deleted
Rule deleted (v6)
rodolphe@server-delory:~$ sudo ufw allow 'Nginx Full'
Skipping adding existing rule
Skipping adding existing rule (v6)
rodolphe@server-delory:~$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere                  
81                         ALLOW       Anywhere                  
Nginx Full                 ALLOW       Anywhere                  
OpenSSH (v6)               ALLOW       Anywhere (v6)             
81 (v6)                    ALLOW       Anywhere (v6)             
Nginx Full (v6)            ALLOW       Anywhere (v6)             

rodolphe@server-delory:~$ sudo certbot --nginx -d rod-cv.fr -d www.rod-cv.fr
Saving debug log to /var/log/letsencrypt/letsencrypt.log
Enter email address (used for urgent renewal and security notices)
 (Enter 'c' to cancel): rodolphe.delory@le-campus-numerique.fr

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Please read the Terms of Service at
https://letsencrypt.org/documents/LE-SA-v1.4-April-3-2024.pdf. You must agree in
order to register with the ACME server. Do you agree?
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
(Y)es/(N)o: y

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Would you be willing, once your first certificate is successfully issued, to
share your email address with the Electronic Frontier Foundation, a founding
partner of the Let's Encrypt project and the non-profit organization that
develops Certbot? We'd like to send you email about our work encrypting the web,
EFF news, campaigns, and ways to support digital freedom.
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
(Y)es/(N)o: n
Account registered.
Requesting a certificate for rod-cv.fr and www.rod-cv.fr

Successfully received certificate.
Certificate is saved at: /etc/letsencrypt/live/rod-cv.fr/fullchain.pem
Key is saved at:         /etc/letsencrypt/live/rod-cv.fr/privkey.pem
This certificate expires on 2024-12-15.
These files will be updated when the certificate renews.
Certbot has set up a scheduled task to automatically renew this certificate in the background.

Deploying certificate
Could not install certificate

NEXT STEPS:
- The certificate was saved, but could not be installed (installer: nginx). After fixing the error shown below, try installing it again by running:
  certbot install --cert-name rod-cv.fr

Could not automatically find a matching server block for rod-cv.fr. Set the `server_name` directive to use the Nginx installer.
Ask for help or search for solutions at https://community.letsencrypt.org. See the logfile /var/log/letsencrypt/letsencrypt.log or re-run Certbot with -v for more details.
rodolphe@server-delory:~$ sudo nano /etc/nginx/sites-available/CV
rodolphe@server-delory:~$ sudo certbot install --cert-name rod-cv.fr
Saving debug log to /var/log/letsencrypt/letsencrypt.log
Deploying certificate
Successfully deployed certificate for rod-cv.fr to /etc/nginx/sites-enabled/CV
Successfully deployed certificate for www.rod-cv.fr to /etc/nginx/sites-enabled/CV
rodolphe@server-delory:~$ 



