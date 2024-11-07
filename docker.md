# DOCKER: 

https://hub.docker.com/search

https://www.youtube.com/watch?v=orS3UCIH4wg

    USING WEB-BASED LOGIN
    To sign in with credentials on the command line, use 'docker login -u <username>'

    Your one-time device confirmation code is: ZHDZ-VJPP
    Press ENTER to open your browser or submit your device code here: https://login.docker.com/activate

    Waiting for authentication in the browser…

    WARNING! Your password will be stored unencrypted in /home/rodolphe-delory/.docker/config.json.
    Configure a credential helper to remove this warning. See
    https://docs.docker.com/engine/reference/commandline/login/#credential-stores


Docker est une plateforme qui permet de créer, déployer et gérer des applications dans des conteneurs. Un conteneur est une sorte de "boîte" qui contient tout ce dont une application a besoin pour fonctionner : le code, les bibliothèques, les dépendances, etc. C'est un peu comme une machine virtuelle, mais plus léger et rapide.

Pourquoi utiliser Docker ?
Isolation : Chaque application fonctionne dans son propre environnement, donc pas de conflits entre versions de bibliothèques ou de logiciels.

Portabilité : Tu peux créer une image Docker d'une application sur ton PC et l'exécuter exactement de la même manière sur un autre serveur, une autre machine ou dans le cloud.

Facilité de déploiement : Docker simplifie le déploiement d'applications. Il suffit d'exécuter une image Docker pour avoir une application prête à l'emploi.

Modularité : Avec Docker Compose, tu peux gérer plusieurs services (par exemple, une application web, une base de données, un serveur cache) dans des conteneurs séparés.



### Version Chat GPT (putin il est fort ce con)

La conteneurisation, avec des technologies comme Docker, offre de nombreux avantages pour le développement et le déploiement d'applications. Voici un aperçu des grands principes de la conteneurisation et des avantages qu’elle apporte :

#### 1. Isolation des applications
Principe : Chaque conteneur fonctionne dans son propre environnement, totalement isolé du reste du système et des autres conteneurs. Cela signifie que chaque application peut avoir ses propres dépendances, versions de logiciels, et configurations sans interférer avec d'autres applications.
Avantage : Plus de conflits entre les environnements ! Par exemple, tu peux avoir deux applications utilisant des versions différentes de PHP (comme PHP 7.4 et PHP 8.1) qui tournent sur la même machine sans problème.

#### 2. Portabilité
Principe : Les conteneurs sont identiques, peu importe l'endroit où ils sont exécutés. Une fois que tu crées une image Docker, elle peut être exécutée sur n'importe quel système supportant Docker (localement, dans le cloud, sur un serveur, etc.).
Avantage : "Ça marche sur ma machine" devient "Ça marche partout". Ce que tu développes en local fonctionnera exactement de la même manière en production, dans le cloud ou sur un autre serveur.
#### 3. Légèreté par rapport aux machines virtuelles
Principe : Contrairement aux machines virtuelles qui nécessitent un système d'exploitation complet, les conteneurs partagent le noyau du système d'exploitation de l'hôte, mais gardent leurs environnements isolés.
Avantage : Les conteneurs consomment moins de ressources, démarrent beaucoup plus vite (en quelques secondes) et sont plus efficaces que les machines virtuelles, car ils ne nécessitent pas de charger tout un OS supplémentaire.
#### 4. Scalabilité et flexibilité
Principe : Tu peux facilement déployer plusieurs instances d'un conteneur pour répondre à la demande (scaling). Les conteneurs sont stateless par nature, ce qui signifie que tu peux en démarrer ou arrêter autant que nécessaire, sans souci de compatibilité.
Avantage : La scalabilité devient plus simple et automatique. Dans des environnements cloud (comme AWS, Google Cloud), tu peux augmenter ou réduire le nombre de conteneurs en fonction de la charge de travail.
#### 5. Gestion facilitée des microservices
Principe : Les architectures basées sur les microservices divisent les applications en petites unités autonomes (services) qui peuvent être déployées et gérées indépendamment.
Avantage : Docker est parfait pour les microservices, car chaque service peut être placé dans un conteneur distinct, permettant une gestion plus fine et indépendante de chaque partie de l'application.
#### 6. Déploiement rapide et cohérent
Principe : Grâce à la nature des images Docker (qui incluent tout le nécessaire pour exécuter une application), le déploiement d'une application devient très rapide et automatisé.
Avantage : Tu peux passer d'une phase de développement à la mise en production très rapidement, en quelques commandes. Tout est automatisé et scriptable, donc il y a moins de risques d'erreurs humaines.
#### 7. Reproductibilité des environnements
Principe : Le fichier Dockerfile contient toutes les instructions pour créer un environnement reproductible (par exemple, quelle version de NGINX, PHP, ou MySQL utiliser, quelles dépendances installer).
Avantage : L'environnement dans lequel l'application tourne est toujours le même, quel que soit l'endroit où le conteneur est exécuté. Cela réduit les problèmes liés aux différences d'environnement entre les développeurs, le staging et la production.
#### 8. Isolation des ressources
Principe : Docker permet de limiter l'accès aux ressources de la machine hôte pour chaque conteneur (CPU, RAM, espace disque).
Avantage : Chaque conteneur peut fonctionner sans affecter négativement les autres, et les limites de ressources peuvent être définies pour empêcher qu'un conteneur ne consomme toutes les ressources de l'hôte.
#### 9. Sécurité
Principe : Les conteneurs fonctionnent dans des environnements isolés et peuvent être configurés avec des permissions spécifiques pour renforcer la sécurité.
Avantage : Même si un conteneur est compromis, les autres conteneurs ou le système hôte ne sont pas directement affectés, ce qui renforce la sécurité globale.
#### 10. Gestion facile avec des outils comme Docker Compose et Kubernetes
Principe : Des outils comme Docker Compose permettent de définir et gérer plusieurs conteneurs interconnectés (par exemple, un serveur web, une base de données, et un service de cache). Kubernetes permet de gérer et orchestrer des conteneurs à grande échelle.
Avantage : Gestion simplifiée des déploiements complexes, en particulier pour les grandes architectures basées sur des microservices ou nécessitant beaucoup de scalabilité.
#### Conclusion
La conteneurisation apporte des avantages majeurs en termes de portabilité, isolation, légèreté, et facilité de déploiement. Elle est particulièrement utile pour les développeurs cherchant à garantir que leurs applications fonctionnent de manière cohérente dans différents environnements, et pour les entreprises cherchant à adopter des approches modernes comme les microservices ou les déploiements cloud natifs.
##### Pouvoir accéder à nginx à l’url http://localhost:8080. Vous devez voir apparaître la phrase Welcome to nginx!

/home/rodolphe-delory/Images/Captures d’écran/

##### Quelle est la différence entre une image Docker et un conteneur ?

Ma VERSION
Un image est une application qui utilise plusieurs containers //faux//

La version de CHAT GPT (putin il est fort ce con)

    1. Image Docker :
    Définition : Une image Docker est un modèle statique ou une photo figée d'un environnement logiciel. Elle contient tout ce dont une application a besoin pour fonctionner, comme le code de l'application, les dépendances, les bibliothèques, les configurations, etc.
    Caractéristiques :
    Statique : Une image ne change pas une fois créée.
    Lecture seule : Les images sont immuables, c'est-à-dire qu'elles ne peuvent pas être modifiées une fois construites.
    Modèle de conteneur : Une image est comme un plan ou une recette pour créer des conteneurs. Elle contient les instructions de base, comme celles présentes dans un Dockerfile, pour démarrer un conteneur.
    Exemple : Une image NGINX que tu peux télécharger depuis Docker Hub (nginx:alpine) contient tout ce qu'il faut pour exécuter un serveur web NGINX.

    2. Conteneur Docker :
    Définition : Un conteneur Docker est une instance en cours d'exécution d'une image. C'est un environnement isolé qui fonctionne en utilisant l'image comme base. Tu peux imaginer un conteneur comme une machine virtuelle légère qui démarre à partir d'une image.
    Caractéristiques :
    Dynamique : Contrairement à une image, un conteneur est en constante évolution. Tu peux interagir avec lui, ajouter des fichiers, exécuter des processus, etc.
    Modifiable : Pendant que le conteneur tourne, tu peux lire, écrire et modifier des fichiers à l'intérieur du conteneur (bien que l'image sous-jacente reste inchangée).
    Éphémère : Un conteneur peut être démarré, arrêté, ou supprimé sans affecter l'image de base. Une fois arrêté, il peut être supprimé ou recréé à partir de la même image.
    Exemple : Lorsque tu fais tourner l'image nginx:alpine avec la commande docker run, tu crées un conteneur en fonctionnement basé sur cette image. Ce conteneur a son propre environnement de serveur NGINX, isolé du reste de ton système.

    Métaphore simple :
    Image : Imagine une image Docker comme un moule à gâteau. C'est un modèle prêt à l'emploi que tu utilises pour créer quelque chose.
    Conteneur : Le conteneur, c'est le gâteau que tu obtiens en utilisant le moule. C'est l'élément final, en cours d'exécution, basé sur l'image. Tu peux faire autant de gâteaux que tu veux à partir d'un seul moule.

    Résumé :
    Image Docker = modèle statique (comme une recette ou un moule).
    Conteneur Docker = instance en cours d'exécution de l'image (comme le gâteau final, actif et fonctionnel).
    Ainsi, une image Docker est utilisée pour créer des conteneurs, et les conteneurs sont ce que tu exécutes pour héberger et gérer tes applications.

##### Que fait Docker si l’image demandée n’est pas présente localement?

Il va la chercher automatiquement et la télécharger pour pouvoir la réutiliser ultérieurement comme si elle était en locale. 


#### Petite comandes bien interressantes 

Pour l'instalation : 

    Installation de Docker (Linux Ubuntu)
    Voici comment tu peux installer Docker :

    Mettre à jour le système :

    bash
    Copier le code
    sudo apt update
    sudo apt upgrade
    Installer les paquets nécessaires :

    bash
    Copier le code
    sudo apt install apt-transport-https ca-certificates curl software-properties-common
    Ajouter la clé GPG officielle de Docker :

    bash
    Copier le code
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    Ajouter le dépôt Docker :

    bash
    Copier le code
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    Installer Docker :

    bash
    Copier le code
    sudo apt update
    sudo apt install docker-ce
    Vérifier l'installation :

    bash
    Copier le code
    sudo systemctl status docker
    (Optionnel) Exécuter Docker sans sudo :

    bash
    Copier le code
    sudo usermod -aG docker ${USER}


Pour voir les containeurs présents sur mon pc: 

    sudo docker ps (-a)

Pour voir les images 

    sudo docker image ls 

Pour récupérer une image depuis dockerHub: 

    sudo docker pull (nom de l'image désirée)

Pour la supprimer 

    sudo docker image rm (puis Id trouvé en faisant image ls)

Pour executer une image 

    sudo docker run (nom de l'image)

Pour rediriger un port 

    sudo docker run -p -d(détach) 8080:80 (nom de l'image)

        (vers) 8080:(depuis)80
        (detach) pour pas afficher les logs

Docker compose: 

https://docs.docker.com/compose/gettingstarted/

    On a les
    
    || containers: (Les instances des images  **Le gâteau**)  ||


    CONTAINER ID   IMAGE            COMMAND                  CREATED          STATUS          PORTS                                     NAMES

838cdeec7b68   mariadb:latest   "docker-entrypoint.s…"   44 minutes ago   Up 44 minutes   3306/tcp                                  some-mariadb
d3aa6a76f493   mon-site-web     "/docker-entrypoint.…"   5 hours ago      Up 5 hours      0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   silly_kilby
6ade1058e635   nginx            "/docker-entrypoint.…"   6 hours ago      Up 6 hours      80/tcp                                    some-nginx


    ||      Les images: (Les moules du **gateau**)          || 

REPOSITORY     TAG                      IMAGE ID       CREATED         SIZE
mon-site-web   latest                   f3ba5ac7ca4b   5 hours ago     43.3MB
mariadb        latest                   09f5b532c2ef   2 weeks ago     414MB
nginx          alpine                   c7b4f26a7d93   4 weeks ago     43.2MB
nginx          stable-alpine3.20-perl   5d48b5a661a1   4 weeks ago     80.8MB
nginx          latest                   39286ab8a5e1   4 weeks ago     188MB
hello-world    linux                    d2c94e258dcb   16 months ago   13.3kB


    ||      Les docker compose (Les recettes pour lancer la preparation des **gateaux**) ||

    Il s'agit d'un fichier Yaml qu'on créé à la racine du repertoire du projet et dans lequel on va indiquer les séquences et lancmeent des applications. 


Qu'est-ce que Docker Compose ?
Docker Compose est un outil qui permet de définir et de gérer des applications multi-conteneurs. Il utilise un fichier YAML (docker-compose.yml) pour décrire la configuration de tes services (conteneurs), ce qui permet de les lancer, les arrêter et les gérer facilement ensemble.

Par exemple, tu peux utiliser Docker Compose pour déployer une application web qui nécessite un serveur web (NGINX), une base de données (MySQL), et un cache (Redis), tout en les gérant avec une seule commande.

Fonctionnement de Docker Compose :
Définition : Tous les services de ton application sont décrits dans un fichier docker-compose.yml (par exemple, le serveur web, la base de données).
Gestion : Avec une seule commande (docker-compose up), tu peux démarrer tous les conteneurs définis dans ce fichier.
Simplicité : Plus besoin d'exécuter des docker run multiples pour chaque conteneur ; Docker Compose s'occupe de tout.
Comment créer un fichier docker-compose.yml ?
Structure d'un fichier docker-compose.yml : Voici un exemple de fichier simple pour une application avec un service web NGINX et une base de données MySQL :

yaml
Copier le code
version: '3'
services:
  web:
    image: nginx:alpine
    ports:
      - "8080:80"
    volumes:
      - ./datahive:/usr/share/nginx/html
  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: example
version : La version du format Compose.
services : Liste des conteneurs à lancer (ici web et db).
image : Les images Docker utilisées (par exemple, nginx:alpine).
ports : Les ports à exposer (ex : 8080:80 pour le service web).
volumes : Montre un dossier local dans le conteneur (ici, ton dossier datahive est monté dans NGINX).
Où mettre le fichier docker-compose.yml ?

Emplacement : Le fichier docker-compose.yml doit être placé à la racine de ton projet, là où tu souhaites gérer les services. Il est souvent au même niveau que le Dockerfile.
Exemple de structure :

markdown

Copier le code

mon-projet/
├── docker-compose.yml
├── Dockerfile
└── datahive/
    └── index.html

Utilisation de Docker Compose : Après avoir créé le fichier docker-compose.yml, tu peux utiliser les commandes suivantes :

Pour démarrer les services :

bash
Copier le code
docker-compose up
Pour arrêter les services :

bash
Copier le code
docker-compose down
En résumé :
Docker Compose est un outil pour gérer des applications multi-conteneurs.
Tu crées un fichier docker-compose.yml à la racine de ton projet.
Ce fichier décrit tous les services de ton application.
Avec une seule commande (docker-compose up), tu lances tous tes services en même temps.


version: '3.8'
services:
  wordpress:
    image: wordpress:latest
    container_name: wordpress
    restart: always
    environment:
      WORDPRESS_DB_HOST: mariadb:3306
      WORDPRESS_DB_USER: wordpress_user
      WORDPRESS_DB_PASSWORD: secret_password
      WORDPRESS_DB_NAME: wordpress_db
    ports:
      
"8080:80" # WordPress sera accessible via localhost:8080
  volumes:
wordpress_data:/var/www/html
networks:
wp_network

  mariadb:
    image: mariadb:10.6.4-focal
    container_name: mariadb
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: root_password
      MYSQL_DATABASE: wordpress_db
      MYSQL_USER: wordpress_user
      MYSQL_PASSWORD: secret_password
    volumes:
      
mariadb_data:/var/lib/mysql
  networks:
wp_network
expose:
"3306" # Expose uniquement au réseau interne (pas accessible de l'extérieur)

volumes:
  wordpress_data:
  mariadb_data:

networks:
  wp_network:
    driver: bridge

