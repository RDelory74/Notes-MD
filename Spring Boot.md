# Spring Boot

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


    B. Les methodes 


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


Enfin on va avoir les classes de gestion de connction avec la base de donnée (les DAO) Data Access Object qui vont nous permettre à partir des classes d'interagir avec la bdd

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