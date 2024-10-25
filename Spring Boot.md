# Spring Boot

## La doc

https://docs.spring.io/spring-boot/documentation.html

## Découverte du FrameWork

    Après une première passe, il s'agit d'un framework Java très utilisé, de par sa légereté, il n'embarque que les librairies nécessaires, son architecture est en microservices. 

Micro- services: C'est une approche architecturale d'API qui s'articule autour des diffèrents workflows d'une API, un server centrale (appellé le gateway) est chargé de gérer tous les autres. Enfait chaque fonctionnalité va avoir sa propre database son propre CRUD sous forme d'API les isolant les unes des autres permettant une modification et une maintenant independante entre chaque fonctionnalité. 

    Exemples de microservices d'une agence de location de voiture: 

    1. Gestion des véhicules 
    2. Gestion des locations 
    3. Gestion des clients
    4. Gestion des paiements 
    5. Gestion de la maintenance des vehicules

### Servlets ou Contrôlleurs

Chacun des ces microservices va avoir ses routes (les Servlets (Contrôleurs)) depuis l'interface (JSP (fichier HTML enrichi de code Java)) vers le modèle (CLasse JAVA)

    Exemeple de routes pour un service: 

    1. Gestion des clients 
       A. POST /clients : Enregistrer un nouveau client dans le système.
       B. GET /clients/{clientId} : Récupérer les informations d’un client spécifique.
       C. GET /clients/{clientId}/rentals : Obtenir l’historique des locations d’un client.

### JSP 

En bref, les JSP servent de couche de présentation dans les applications web Java, affichant des informations dynamiques à l’utilisateur final et permettant d’interagir avec les données de l’application de manière visuelle et flexible.


### Les modèles (Classe JAVA)

C'est ici qu'on va appliquer la logique métier afin d'interagir avec la BDD, tout comme pour le Donjon et Dragon réalisé il va s'organiser en trois grandes parties: 

1. Les attributs: (exemple Gestion de clients)

        public class Client {
            private Long id;
            private String nom;
            private String prenom;
            private String email;
            private String telephone;


2. Les constructeurs: (exemple Gestion de clients)

            // Constructeur sans paramètres
            public Client() {
            }

            // Constructeur avec paramètres
            public Client(Long id, String nom, String prenom, String email, String telephone) {
                this.id = id;
                this.nom = nom;
                this.prenom = prenom;
                this.email = email;
                this.telephone = telephone;
            }

3. Les méthodes: (exemple Gestion de clients) Que je divise en 2 parties 

    A. Les Getter/ Setter

            // Getters et Setters pour chaque attribut
            public Long getId() {
                return id;
            }

            public void setId(Long id) {
                this.id = id;
            }

            public String getNom() {
                return nom;
            }

            public void setNom(String nom) {
                this.nom = nom;
            }

            public String getPrenom() {
                return prenom;
            }

            public void setPrenom(String prenom) {
                this.prenom = prenom;
            }

            public String getEmail() {
                return email;
            }

            public void setEmail(String email) {
                this.email = email;
            }

            public String getTelephone() {
                return telephone;
            }

            public void setTelephone(String telephone) {
                this.telephone = telephone;
            }


    B. Les methodes spécifiques à l'objet


            // Méthode pour afficher les informations du client
            @Override
            public String toString() {
                return "Client{" +
                        "id=" + id +
                        ", nom='" + nom + '\'' +
                        ", prenom='" + prenom + '\'' +
                        ", email='" + email + '\'' +
                        ", telephone='" + telephone + '\'' +
                        '}';
            }
        }


Enfin on va avoir les classes de gestion de connection avec la base de donnée (les DAO) Data Access Object qui vont nous permettre à partir des classes d'interagir avec la bdd

(Comme dans mon donjon et dragon)

### Vision FrameWork

### Les plus 

    1. Démarrage rapide grace aux starters qui contiennent déja des dépendances déja préconfiguré pour les scénarios courants
    2. Adapté pour le développement et la gestion de microservices
    3. Bonne commu et documentation pour travailler

### Les moins

    1. Poids et perf, l'ensemble des dépendances par defaut qui sont intégrés peuvent ralentir inutilement le processus de petits projets
    2. Courbe d'apprentissag abrupte, très à première vue, il devient vite difficile de s'imiscer dans les rouages dès qu'on veut controler les choses
    3. Les config auto qui sont très pratiques sur du basique mais qui peuvent vite devenir source de conflit si le projet se complexifie


## Les Starters 

Le plus plus courant, le starter web:

        <dependency>

          <groupId>org.springframework.boot</groupId>

          <artifactId>spring-boot-starter-web</artifactId>

        </dependency>


spring-boot-starter-mail : pour les applications et services d'envoi de mails.

spring-boot-starter-thymeleaf : si vous souhaitez créer une application qui offre une interface utilisateur en utilisant le moteur de template Thymeleaf.

spring-boot-starter-web-services : pour les services plus classiques utilisant SOAP.

## Les termes

    Stubs (en test): une fausse classe simplifier pour tester une fonctionnalité
    Mock (en test): redefinition d'un comportement de méthode là encore pour réaliser un test sans avoir à écrire toute la méthode.

#### Beans Factory 

La BeanFactory est un composant central de Spring qui s'occupe de la gestion des objets Java, appelés "beans", dans le contexte d'une application. Elle est responsable de créer, configurer et gérer le cycle de vie des objets.

        <beans>
            <bean id="clientService" class="com.example.ClientService">
                <property name="emailService" ref="emailService" />
            </bean>

            <bean id="emailService" class="com.example.EmailService" />
        </beans>

### Pom.xml

### L'autoconfiguration

Pour activer l'autoconfiguration, on utilise l'annotation  @EnableAutoConfiguration .
Si vous écrivez vos propres configurations, celles-ci priment sur celles de Spring Boot.

### Pour compiler 

Avec Maven dans l'onglet de droite on va dans: 
        |_rentakar
            |_Lifecycle
                |_install

Ca va nous créer un fichier.jar dans le dossier target créé à cet occasion (youpi). 

Enfin avec le terminal pour lancer cette commande on va rentrer la ligne de commande: 

    java -jar /home/rodolphe-delory/rentakar/target/rentakar-0.0.1-SNAPSHOT.jar


### Créer ses controller 

Quand on cré ses controller on assign des annotation à notre classe pour indiquer qu'elle va utiliser des méthodes GET POST PUT PATCH DELETE

L'annotation @RestController au dessus de la classe nous permet de l'identifier ainsis 

puis on va ajouter des annotation mapping tel que @GetMapping 

    Exemple pour mon rentakar
        // ICI le package
        package com.RentaKar.rentakar.web.controller;
        // Les imports en fonctions des annotation et méthodes nécessaires
        import org.springframework.web.bind.annotation.GetMapping;
        import org.springframework.web.bind.annotation.RestController;
        // L'annotation RestController puis ma Classe
        @RestController
        public class UserControler {
        
        @GetMapping("/Users")
            public String listeUsers(){
            return "Liste des users";
        }
        }


    //Dans ce code,  c'est l'annotation @GetMapping  qui permet de faire le lien entre l'URI "/Users", invoquée via GET, et la méthode listeUsers.

De nouvelles annotations sont dorénavant disponibles, telles que @GetMapping, @PostMapping, @PutMapping, @DeleteMapping qui permettent de ne spécifier que l’URL, tout en utilisant le verbe HTTP lié, présent juste avant le mapping.

@Repository : cette annotation est appliquée à la classe afin d'indiquer à Spring qu'il s'agit d'une classe qui gère les données, ce qui nous permettra de profiter de certaines fonctionnalités, comme les translations des erreurs. Nous y reviendrons.

L’annotation @Autowired permet d’activer l’injection automatique de dépendance. Cette annotation peut être placée sur un constructeur, une méthode setter ou directement sur un attribut (même privé). Le Spring Framework va chercher le bean du contexte d’application dont le type est applicable à chaque paramètre du constructeur, aux paramètres de la méthode ou à l’attribut.

Annotation Spring Booot 

https://www.jrebel.com/blog/spring-annotations-cheat-sheet

https://www.jrebel.com/sites/rebel/files/pdfs/cheatsheet-jrebel-spring-annotations.pdf

