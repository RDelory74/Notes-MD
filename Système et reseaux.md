# Système Reseaux

Pour vous, qu’est ce qu’un réseau ?

        Un lien entre plusieurs entité numériques pour transférer de l'information. 

Quel est le lien entre la notion de réseau et Internet?

        Un reseau c'est les liens dans une infrastructure, alors que le reseau internet est un lien vers l'exeterieur

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
    
    9. Réseau Peer-to-Peer (P2P - Peer-to-Peer Network)
    Dans un réseau P2P, chaque appareil connecté au réseau peut agir à la fois comme client et comme serveur. Il n'y a pas de serveur centralisé, et les appareils partagent directement des ressources entre eux.

        Exemple : Les réseaux de partage de fichiers tels que BitTorrent, où les utilisateurs échangent des données directement sans passer par un serveur centralisé.
    
    Chaque type de réseau est adapté à des besoins spécifiques en termes de distance, de sécurité, de vitesse et de coût.

Quels sont les principaux équipements physiques d’un réseau LAN?

    des ordinateurs, des imprimantes et des serveurs, une box de connection, un routeur, base de données 

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
