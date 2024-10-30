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


### Controller, Service, DAO 

 @Service

Comme j'ai compris les choses, on va avoir le Controller qui va router les requêtes et les retours server. 
La DAO (Repository) qui va gérer les requêtes simple à la BDD ,type CRUD.
Le service qui va  s'occuper de la logique métier appliquée à la DAO. 

Il s'agit d'une forme de factorisation dans le sens ou on va découper les traitement en plusieurs couches dans un soucis d'isolation et de maintenance. 

En gros: 

    LeController
        |_LeService
            |_LaDao(Repository)
                |_LeModel(Domaine)


Si demain j'arrive sur le code et que j'ai bespoin d'appliquer une logique métier sur ce dernier je n'aurais besoin d'intervenir que sur le couche Service sans toucher à la DAO ni au controller ni au model. 

@Transactional

Qu'est-ce qu'une transaction dans les méthodes de service ?

Dans une méthode de service annotée avec @Transactional, Spring garantit que toutes les opérations dans cette méthode s'exécutent dans le cadre d'une seule transaction. Par exemple, si la méthode exécute plusieurs opérations de base de données (comme enregistrer un client, créer une réservation de voiture, et mettre à jour l’inventaire), toutes ces opérations sont traitées comme une seule transaction.
Pourquoi utiliser @Transactional ?

Avec @Transactional, si une opération dans la méthode échoue (comme une exception due à un problème d'insertion de données), toutes les opérations précédentes sont annulées. Ce mécanisme s'appelle le rollback, et il garantit que la base de données reste cohérente et n’applique pas partiellement des modifications en cas d'erreur.
Comment fonctionne le rollback avec @Transactional ?
Spring surveille les exceptions qui surviennent dans la méthode de service annotée. En cas d'exception non récupérée (comme une RuntimeException), Spring annule automatiquement les changements pour que la base de données retrouve son état initial, comme si la méthode n'avait jamais été exécutée.
C’est l’occasion parfaite pour moi pour vous parler d’un point important : les transactions.

Les transactions sont le mécanisme qui permet de respecter les propriétés ACID :

Atomicité : Une transaction s’effectue entièrement, ou pas du tout.

Cohérence : Le contenu d’une base doit être cohérent au début et à la fin d’une transaction.

Isolation : Les modifications d’une transaction ne sont visibles/modifiables que quand celle-ci a été validée.

Durabilité : Une fois la transaction validée, l’état de la base est permanent (non affecté par les pannes ou autre).

Le respect de ces propriétés est synonyme de fiabilité dans le traitement de vos données.

## Projet JAVA 

Introduction
Le but de ce projet est de développer un site permettant de réserver un véhicule auprès d’un
loueur de véhicule. Ce site utilisera Spring Boot, sous forme d’architecture microservice
(MSA - pour MicroService Architecture).

Livrables
Le code est déposé sous github.
Une présentation des choix d’architecture et du travail réalisé. (15 à 20 minutes par groupe
maximum)

Une représentation graphique de votre architecture pour chaque itération que vous
aurez identifié comme nécessaire.
La définition de vos API pour chacun des microservices.

Objectifs
Création d’une webapp sous forme de micro services en Java Spring Boot.
Solidification des compétences techniques acquises lors de la 1ère phase de
ce module.

Modalités
Le projet s’effectue en binôme, un seul livrable sera rendu (sur GitHub).
Le projet devant être réalisé sous forme de MSA, la planification du travail se
fera en équipe entière mais les tâches seront réparties




### Divers (insert sql and other)

  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(1, 'Robert', 'Deplante', 499865, '25.10.1980');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(2, 'Jhon', 'Dumoulin', 599862, '17.02.1996');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(3, 'Maîté', 'Pasla', 599684, '01.05.1968');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(4, 'Alice', 'Dupont', 123456, '10.02.1990');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(5, 'Bob', 'Martin', 234567, '15.06.1985');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(6, 'Maîté', 'Pasla', 599684, '01.05.1968');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(7, 'Charles', 'Durand', 345678, '20.11.1978');
  INSERT INTO LocationVehicule.user (`id`, `username`,`firstname`,`licenceId`,`Date_Of_Birth`) VALUES(8, 'Emma', 'Leroy', 456789, '25.12.2000');

  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(1, 'Robert', 'Deplante', 499865, '25.10.1980');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(2, 'Jhon', 'Dumoulin', 599862, '17.02.1996');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(3, 'Maîté', 'Pasla', 599684, '01.05.1968');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(4, 'Alice', 'Dupont', 123456, '10.02.1990');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(5, 'Bob', 'Martin', 234567, '15.06.1985');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(6, 'Maîté', 'Pasla', 599684, '01.05.1968');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(7, 'Charles', 'Durand', 345678, '20.11.1978');
  INSERT INTO LocationVehicule.user (id, username,firstname,licenceId,Date_Of_Birth) VALUES(8, 'Emma', 'Leroy', 456789, '25.12.2000');
    

     CREATE TABLE User (
        id INT AUTO_INCREMENT PRIMARY KEY,
        firstname VARCHAR(50) NOT NULL,
        username VARCHAR(50) NOT NULL,
        licenseId INT,
        dateOfBirth VARCHAR(10)
    );

    
