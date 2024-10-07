# JAVA
## RESSOURCES
https://www.w3schools.com/java/java_getstarted.asp

https://www.codecademy.com/learn/learn-java


JM DOUDOU 

https://www.jmdoudoux.fr/accueil.html

Baeldung 

https://www.baeldung.com/

La doc Oracle

****https://docs.oracle.com/


### Nommage 

Constructeur commence par une majuscule 

Classe commence par une majuscule

Variable c'est un nom, commence par une minuscule Camel case

Méthode est un verbe commence par une minucscule sauf constructeur 

### QuickStart 

In Java, every application begins with a class name, and that class must match the filename.

Let's create our first Java file, called Main.java, which can be done in any text editor (like Notepad).

The file should contain a "Hello World" message, which is written with the following code:


### CLasses

J'ai utilisé deux fichier .java, un que l'on retrouve toujour est Main.java ou l'on appellé les instances et puis (par exemple) Dog.java ou je vais intégrer ma class et son constructeur.  
//Dog.java ne pas utiliser

        public class Dog {

           String bredd;
           double weight;

           public static void main(String[] args) {

               Dog Argentain = new Dog();
               Argentain.breed = "Veyron";
               Argentain.weight = 37.8;

           }
        }

//Dog.java exemple 2

        public class Dog {

           String breed;
           double weight;

           public static void main(String dogBreed, double dogWeight) {
               breed = dogBreed;
               weight = dogWeight;
           }
           }

// A vérifier mais il semblerait que l'on pourrait l'écrire aussi comme-suit: A creuser, a creuser!!!

public Car(String model, int maxSpeed) {
this.model = model;
this.maxSpeed = maxSpeed;
}

//Main.java

    public class Main {
      public static void main(String[] args) {

        Dog Argentain = new Dog ("Argentain", 37.8)
      }
    }

### Méthodes

On crée des méthodes afin de les associer à des actions sur des classes exemple:

//Dog.java

    public class Dog {

        //instance fields

           String breed;
           double weight;

        //constructor method

           public static void main(String dogBreed, double dogWeight) {
               breed = dogBreed;
               weight = dogWeight;
           }

        //additionnals methods

        public void wouaf(){
            String noisyMess = "C'est un chien de race" + breed + "Il fait WOUAF";
            System.out.println (noisyMess);
        }
           }

//Main.java

    public class Main {
      public static void main(String[] args) {

        Dog argentain = new Dog ("Argentain", 37.8)
        argentain.wouaf();
      }
    }

### Conditions des boucles

//Dog.java

    public class Dog {

        //instance fields

           String breed;
           double weight;

        //constructor method

           public static void main(String dogBreed, double dogWeight) {
               breed = dogBreed;
               weight = dogWeight;
           }

        //additionnals methods

        public void wouaf(){
            String noisyMess = "C'est un chien de race" + breed + "Il fait WOUAF";
            System.out.println (noisyMess);
        }
           }


        // if then

        if (dog.weight > 12) {

        System.out.println("Ha ouais c'est un gros chien !! ");

        } else {

        System.out.println("Ha ouais c'est un p'tit chien!! ");
        
        }

// exemple avec True / False

boolean isValidPassword = true;

if (isValidPassword) {

  System.out.println("Password accepted!");

}

// exemple de else / if

    String course = "Theatre";

    if (course.equals("Biology")) {

      // Enroll in Biology course

    } else if (course.equals("Algebra")) {

      // Enroll in Algebra course

    } else if (course.equals("Theatre")) {

      // Enroll in Theatre course

    } else {

      System.out.println("Course not found!");

    }
// Un autre exemple

        int testScore = 72;

    if (testScore >= 90) {

      System.out.println("A");

    } else if (testScore >= 80) {

      System.out.println("B");

    } else if (testScore >= 70) {

      System.out.println("C");

    } else if (testScore >= 60) {

      System.out.println("D");

    } else {

      System.out.println("F");

    }
    // prints: C

//Les conditions chaudes du cul // les nested

if (outer condition) {
  if (nested condition) {
    Instruction to execute if both conditions are true
  }
}

A savoir ça s'écrit aussi comme ça: 

if (tuitionPaid && hasPrerequisite) {
  // enroll student
}

pour l'équivalent en nested: 

if (tuitionPaid) {
  if (hasPrerequisite) {
    // enroll student
  }
}


Pour les conditions on peu utiliser aussi le switch // exemple // 

String course = "History";

switch (course) {
  case "Algebra": 
    // Enroll in Algebra
    break; 
  case "Biology": 
    // Enroll in Biology
    break;
  case "History": 
    // Enroll in History
    break;
  case "Theatre":
    // Enroll in Theatre
    break;
  default:
    System.out.println("Course not found");
}


Nota bene que le break arrête le programme de chercher dans les autres case qaund il entre dans un case. On peu faire sans mais c'est PAS BIEN

Condition

https://content.codecademy.com/courses/learn-java/AP-Computer-Science-A/conditional-operators/TruthTable-All.svg


public class Main {
    public static void main(String[] args) {
        double nbCartons = 34;
        System.out.println("Il y a " + nbCartons + " cartons dans le local.");
        double truckCapacity = 9;
        System.out.println("Et le camion à une capacité de " + truckCapacity + " cartons par voyages.");
        double nbVoyages = nbCartons / truckCapacity;
        System.out.println("Il faudra faire " + Math.round(nbVoyages) + " voyages.");


        while (nbCartons > 0 && truckCapacity<nbCartons) {

            nbCartons = nbCartons - truckCapacity;
            System.out.println("Un voyage de "+truckCapacity+" cartons.");
            System.out.println("Il reste "+nbCartons+" au locale.");
        }
    }
}

public class Main {
    public Main() {
    }

    public static void main(String[] args) {
        double nbCartons = 34.0;
          System.out.println("Il y a " + nbCartons + " cartons dans le local.");
        double truckCapacity = 9.0;
          System.out.println("Et le camion à une capacité de " + truckCapacity + " cartons par voyages.");
        double nbVoyages = nbCartons / truckCapacity;
          System.out.println("Il faudra faire " + Math.round(nbVoyages) + " voyages.");

        while(nbCartons > 0.0 && truckCapacity < nbCartons) {
            nbCartons -= truckCapacity;
            System.out.println("Un voyage de " + truckCapacity + " cartons.");
            System.out.println("Il reste " + nbCartons + " au locale.");
        }
        System.out.println("Dernier voyage avec " + nbCartons + " dans le camion.");
    }
}


### Getter / Setter 

Lorsqe l'on met des attribut en private il est nécessaire de créer des méthode get et set pour récupérer ou modifier les attirbuts de la clzasse au travers du code. 

https://codegym.cc/fr/groups/posts/getters-et-setters-en-java

En gros quand on met de chants d'instance en private afin de limiter l'accés aux données par nos pairs, cela nous permet après de leur appliquer des méthodes, afin de s'assurer du type ou de l'affectation des valeurs. 

On va donc ajouter dans le fichier class les getter et les setters associé à notre constructeur et ainsi leur appliquer des méthodes pour contraindre les affectations. 


### System.out.printf (format)

Avec cette commande tu peux formater les valeurs de sortie avec différents méthodes (voir la doc // https://www.baeldung.com/java-printstream-printf) 
La méthode s'écri avec un % au debut et doit respecter l'ordre d'apparitiondes variables séparée elles par une virgule. 


Exponant help 

https://www.baeldung.com/java-calculating-the-power-without-math-pow

Something is truee right above

### Le Buffer

La mémoire tampon des infos dans le cache lors du déroulement du programme. 


### L'Héritage

C'est la 

### Surcharger ou remplacer des comportement de classe mère: Le polymorphisme

En réutilisant un méthode de classe on applique un: 
Avec super. 

On vient mettre un 

@Override au dessus de la méthode pour lui indiquer qu'on va la surcharger. 



Ca se passe comme ça:   - public Mother abstract class ------------------- public Children (abstract) class // Extends Mother
                            |_____ (inclus abstrcat méthode)                            |____ (inclus abstract methode)


### Méthode sur les Array:

  Pour l'ajout:

        plateau.add(new Empty(1));
        plateau.add(new Arme("Excalibur",5,"sword"));
        plateau.add(new Ennemis("Gobelin",6,3));
        plateau.add(new Potion("Potion standard",2,"healPotion"));
        plateau.add(new Ennemis("Sorcier",9,2));
        plateau.add(new Ennemis("Dragon",15,4));
        plateau.add(new Bouclier("Bouclier en métal de fou",15,"Bouclier"));

Pour mélanger: 

        Collections.shuffle(plateau);

Code une fonction pour générer une chaine de caractère aléatoire.

        https://www.codeurjava.com/2015/03/generer-des-caracteres-aleatoires.html

### Le Scanner

Pour récupérer la saisie d'un utilisateur 

    import java.util.Scanner;
    Scanner sc = new Scanner scanner;

Méthode Java qui permet de récupérer ce que l'utilisateur écrit: 

      Scanner sc = Scanner scanner
      int variable = sc.Int(); 
      String variable = sc.nextLine();

Pour initier une méthode random. 

    import java.util.Random;
    Random rd = new Random random;

### Connecter BDD 


IDE: Intellij
Création de Database dans Mysql: 

    mysql> CREATE DATABASE DonjonsEtDragons;

Ajout d'un plugin dans l'IDe pour gérer les BDD: 

    DB navigator

Installation d'une librairie pour la gestion des bdd (connection et requêtes) jdbc: (fichier .jar à installer dans un dossier lib (créé par mes soins) que l'ont va ensuite configurer pour indiquer à l'IDE qu'il s'agit d'un fichier source de controle et de librairie (https://www.geeksforgeeks.org/how-to-add-external-jar-file-to-an-intellij-idea-project/) )

tel du fichier .jar: 

      https://www.geeksforgeeks.org/how-to-add-external-jar-file-to-an-intellij-idea-project/

Ensuite on fait une configuration de notre plugin: 

Configurer la connexion :
Nom de la base de données : entre DonjonsEtDragons.
Host : entre l'adresse IP du serveur MySQL (si c'est en local, utilise localhost ou 127.0.0.1).
Port : entre le port par défaut de MySQL, généralement 3306.
User : entre ton nom d'utilisateur MySQL (ex. root).
Password : entre le mot de passe de ton utilisateur MySQL.
Database : spécifie le nom de la base, ici DonjonsEtDragons.


Notre Bdd devrait connéctée à ce stade: on va pouvoir y intégrer les tables nécessaires: (type Player) 

      CREATE TABLE Player (
          id INT AUTO_INCREMENT PRIMARY KEY,  
          name VARCHAR(100),
          pv INT,
          strength INT,
          weapon VARCHAR(100),
          defense VARCHAR(100),
          type VARCHAR(100),
          exp INT,
          gold INT,    
          level INT
      );



Enfin je créé des Class que je prend soin d'installer dans un dossier db (au même niveau que les dossiers item et autres)

Ces classes vont me permettre de gérer la connection ainsi que l'interaction avec ma base de donnée. 

Je la structure comme suit: 

  - Les imports et packages classiques
    + import java.sql.*;

  - la méthode de connection à configurer

            private Connection connect() {
             // Connection
             Connection conn = null;
             try {
                 String url = "jdbc:mysql://localhost:3306/DonjonsEtDragons";
                 String user = "root";
                 String password = "password";
                 conn = DriverManager.getConnection(url, user, password);
             } catch (SQLException e) {
                 System.out.println(e.getMessage());
             }
             return conn;
            }    

  - les méthodes CREATE, SHOW, INSERT, PUT et autres 

  Exemple de méthode et sa structure. 

    // D'abord je créé une variable String dans laquel jRandom random = new Random();

pstmt.executeUpdate();

Statement

ResultSet rs = stmt.executeQuery(sql)


           public void createPlayer(Player player) {

        // Méthode pour créer un joueur
        String sql = "INSERT INTO Player(name, pv, strength, weapon, defense, type, exp, or, level) VALUES(?, ?, ?, ?, ?, ?, ?, ?, ?)";

        try (Connection conn = this.connect();
             PreparedStatement pstmt = conn.prepareStatement(sql)) {

            pstmt.setString(1, player.getName());
            pstmt.setInt(2, player.getVie());
            pstmt.setInt(3, player.getStrength());
            pstmt.setString(4, player.getWeapon());
            pstmt.setString(5, player.getDefense());
            pstmt.setString(6, player.getType());
            pstmt.setInt(7, player.getExp());
            pstmt.setInt(8, player.getOr());
            pstmt.setInt(9, player.getLevel());

            pstmt.executeUpdate();
            System.out.println("Player created successfully.");
        } catch (SQLException e) {
            System.out.println(e.getMessage());
        }
    }

https://www.jmdoudoux.fr/java/dej/chap-jdbc.htm


### Notes et divers 

public class Menu {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random random = new Random();

        System.out.println("Welcome to Dungeons & Dragons!");
        System.out.println("Let's create a new player");


        System.out.print("Enter your character name: ");
        String characterName = sc.nextLine();
        System.out.print("Enter your character Type Random random = new Random();
            } else if (choice == 1) {
                System.out.println("Info Héros");
                System.out.println("Name :" + character.getName() +
                        "\n" + "PV :" + character.getVie() +
                        "\n" + "Force :" + character.getStrength() +
                        "\n" + "Arme :" + character.getWeapon() +
                        "\n" + "Defense :" + character.getDefense() +
                        "\n" + "Type :" + character.getType() +
                        "\n");
            } else if (choice == 2) {
                System.out.println("\nModifier Héros:");
                System.out.println("1. Modifier Nom");
                System.out.println("2. Modifier Type");
                System.out.println("0. Back");
                System.out.print("Enter your choice: ");
                int custChoice = sc.nextInt();
                if (custChoice == 0) {Random random = new Random();
                    System.out.println("Retour au menu");
                } else if (custChoice == 1) {
                    System.out.println("Nouveau nom du Héros:");
                    character.setName(sc.nextLine());
                    System.out.println("Le nouveau nom du héros a bien été remplacé par: "+character.getName());
                } else if (custChoice == 2) {
                    System.out.println("Nouveau type de Héros (Wizard ou Warrior): ");
                    character.setType(sc.nextLine());
                    System.out.println("Le nouveau type du héros a bien été remplacé par: "+character.getType());
                } else {
                    System.out.println("Invalid choice. Try again.");
                }
            } else {
                System.out.println("Invalid choice. Try again.");
            }
        }
        }else {
            System.out.println("Invalid choice. Try again.");
        }
    }
}



DD Help https://github.com/LucasMouraDeOliveira/Dungeon/blob/master/src/dungeon/Game.java#L18

https://github.com/srajan-kiyotaka/Dungeons-and-Dragons/blob/main/Java/D%26D_Medium.java

https://devpost.com/software/dungeons-and-dragons-wdl825#updates

____________ZZZZZZZZZZZZZZZZZZZZZ
__________ZZZZZ______________ZZZZZZ
________ZZZZZ____________________ZZZZ
______ZZZZZ_______________________ZZZZZ
____ZZZZZ___________________________ZZZZ
___ZZZZ______________________________ZZZZ
__ZZZ__________________________________ZZZ
_ZZZ____________________________________ZZZ
ZZZZ____________________________________ZZZ
ZZZ_____________________________________ZZZ
ZZZ_____________________________________ZZZ
ZZZ_____________________________________ZZZ
ZZZ_____________________________ZZ______ZZZ
ZZZ___________________________ZZZZZ_____ZZZ
ZZZ________________________ZZZZZZZZZ__ZZZZZ
ZZZZ____ZZZ______________ZZZZZZZZZZZZ_ZZZZ
ZZZZ___ZZZZZZ___________ZZZZZZZZZZZZZ_ZZZ
ZZZZ__ZZZZZZZZZZ_______ZZZZZZZZZZZZZ__ZZ
ZZZZ__ZZZZZZZZZZZ______ZZZZZZZZZZZZ___ZZ
_ZZZ___ZZZZZZZZZZZ______ZZZZZZZZZZ____ZZ
_ZZZ____ZZZZZZZZZ_ZZZZZ___ZZZZZZ____ZZZZ
__ZZZ____ZZZZZZZ__ZZZZZZ___________ZZZZ
___ZZZZZ__________Z__ZZZ_____ZZZZZZZZZ
____ZZZZZZZZ__________ZZ____ZZZZZZZZ
_____ZZZZZZZZ_____________ZZZZZ
__________ZZZ__Z___Z___Z__ZZZ
__________ZZZ_ZZZ_ZZZ_ZZZ_ZZZ
__________ZZZ_ZZZ_ZZZ_ZZZ_ZZZ
__________ZZZ_ZZZ_ZZZ_ZZZ_ZZZRandom random = new Random();
________*##################*
_________*################*
__________*#############*
___________*##########*
____________*#######*
_____________*#####*
______________*###*
_______________*#*
________________*


 ____               _                    _   
|  _ \  ___  _ __  (_) ___  _ __     ___| |_ 
| | | |/ _ \| '_ \ | |/ _ \| '_ \   / _ \ __|
| |_| | (_) | | | || | (_) | | | | |  __/ |_ 
|____/ \___/|_| |_|/ |\___/|_| |_|  \___|\__|
|  _ \ _ __ __ _ |__/_  ___  _ __  ___       
| | | | '__/ _` |/ _` |/ _ \| '_ \/ __|      
| |_| | | | (_| | (_| | (_) | | | \__ \      
|____/|_|  \__,_|\__, |\___/|_| |_|___/      
                 |___/                       


           ,   ,
         ,-`{-`/
      ,-~ , \ {-~~-,
    ,~  ,   ,`,-~~-,`,
  ,`   ,   { {      } }                                             }/
 ;     ,--/`\ \    / /                                     }/      /,/
;  ,-./      \ \  { {  (                                  /,;    ,/ ,/
; /   `       } } `, `-`-.___                            / `,  ,/  `,/
 \|         ,`,`    `~.___,---}                         / ,`,,/  ,`,;
  `        { {                                     __  /  ,`/   ,`,;
        /   \ \                                 _,`, `{  `,{   `,`;`
       {     } }       /~\         .-:::-.     (--,   ;\ `,}  `,`;
       \\._./ /      /` , \      ,:::::::::,     `~;   \},/  `,`;     ,-=-
        `-..-`      /. `  .\_   ;:::::::::::;  __,{     `/  `,`;     {
                   / , ~ . ^ `~`\:::::::::::<<~>-,,`,    `-,  ``,_    }
                /~~ . `  . ~  , .`~~\:::::::;    _-~  ;__,        `,-`
       /`\    /~,  . ~ , '  `  ,  .` \::::;`   <<<~```   ``-,,__   ;
      /` .`\ /` .  ^  ,  ~  ,  . ` . ~\~                       \\, `,__
     / ` , ,`\.  ` ~  ,  ^ ,  `  ~ . . ``~~~`,                   `-`--, \
    / , ~ . ~ \ , ` .  ^  `  , . ^   .   , ` .`-,___,---,__            ``
  /` ` . ~ . ` `\ `  ~  ,  .  ,  `  ,  . ~  ^  ,  .  ~  , .`~---,___
/` . `  ,  . ~ , \  `  ~  ,  .  ^  ,  ~  .  `  ,  ~  .  ^  ,  ~  .  `-,


        ,     \    /      ,        
       / \    )\__/(     / \       
      /   \  (_\  /_)   /   \      
 ____/_____\__\@  @/___/_____\____ 
|             |\../|              |
|              \VV/               |
|        ----------------         |
|_________________________________|
 |    /\ /      \\       \ /\    | 
 |  /   V        ))       V   \  | 
 |/     `       //        '     \| 
 `              V                '



                           __.--|~|--.__                               ,,;/;
                         /~     | |    ;~\                          ,;;;/;;'
                        /|      | |    ;~\\                      ,;;;;/;;;'
                       |/|      \_/   ;;;|\                    ,;;;;/;;;;'
                       |/ \          ;;;/  )                 ,;;;;/;;;;;'
                   ___ | ______     ;_____ |___....__      ,;;;;/;;;;;'
             ___.-~ \\(| \  \.\ \__/ /./ /:|)~   ~   \   ,;;;;/;;;;;'
         /~~~    ~\    |  ~-.     |   .-~: |//  _.-~~--,;;;;/;;;;;'
        (.-~___     \.'|    | /-.__.-\|::::| //~     ,;;;;/;;;;;'
        /      ~~--._ \|   /          `\:: |/      ,;;;;/;;;;;'
     .-|             ~~|   |  /V""""V\ |:  |     ,;;;;/;;;;;' \
    /                   \  |  ~`^~~^'~ |  /    ,;;;;/;;;;;'    ;
   (        \             \|`\._____./'|/    ,;;;;/;;;;;'      '\
  / \        \                             ,;;;;/;;;;;'     /    |
 |            |                          ,;;;;/;;;;;'      |     |
|`-._          |                       ,;;;;/;;;;;'              \
|             /                      ,;;;;/;;;;;'  \              \__________
(             )                 |  ,;;;;/;;;;;'      |        _.--~
 \          \/ \              ,  ;;;;;/;;;;;'       /(     .-~_..--~~~~~~~~~~
 \__         '  `       ,     ,;;;;;/;;;;;'    .   /  \   / /~
 /          \'  |`._______ ,;;;;;;/;;;;;;'    /   :    \/'/'       /|_/|   ``|
| _.-~~~~-._ |   \ __   .,;;;;;;/;;;;;;' ~~~~'   .'    | |       /~ (/\/    ||
/~ _.-~~~-._\    /~/   ;;;;;;;/;;;;;;;'          |    | |       / ~/_-'|-   /|
(/~         \| /' |   ;;;;;;/;;;;;;;;            ;   | |       (.-~;  /-   / |
|            /___ `-,;;;;;/;;;;;;;;'            |   | |      ,/)  /  /-   /  |
 \            \  `-.`---/;;;;;;;;;' |          _'   |R|    /'('  /  /|- _/  //
   \           /~~/ `-. |;;;;;''    ______.--~~ ~\  |o|  ,~)')  /   | \~-==//
     \      /~(   `-\  `-.`-;   /|    ))   __-####\ |d|   (,   /|    |  \
       \  /~.  `-.   `-.( `-.`~~ /##############'~~)| |   '   / |    |   ~\
        \(   \    `-._ /~)_/|  /############'       |D|      /  \     \_\  `\
        ,~`\  `-._  / )#####|/############'   /     |e|  _--~ _/ | .-~~____--'
       ,'\  `-._  ~)~~ `################'           |l| ((~>/~   \ (((' -_
     ,'   `-.___)~~      `#############             |o|           ~-_     ~\_
 _.,'        ,'           `###########              |r|            _-~-__    (
|  `-.     ,'              `#########       \       |y|          ((.-~~~-~_--~
`\    `-.;'                  `#####"                | |           "     ((.-~~
  `-._   )               \     |   |        .       |  \                 "
      `~~  _/                  |    \               |   `---------------------
        |/~                `.  |     \        .     |  O    __.---------------
         |                   \ ;      \             |   _.-~
         |                    |        |            |  /  |
          |                   |         |           |/'  |

                    ____
                  .'* *.'
               __/_*_*(_
              / _______ \
             _\_)/___\(_/_
            / _((\- -/))_ \
            \ \())(-)(()/ /
             ' \(((()))/ '
            / ' \)).))/ ' \
           / _ \ - | - /_  \
          (   ( .;''';. .'  )
          _\"__ /    )\ __"/_
            \/  \   ' /  \/
             .'  '...' ' )
              / /  |  \ \
             / .   .   . \
            /   .     .   \
           /   /   |   \   \
         .'   /    b    '.  '.
     _.-'    /     Bb     '-. '-._
 _.-'       |      BBb       '-.  '-.
(___________\____.dRODb.________)____)

                              .sssssssss.
                        .sssssssssssssssssss
                      sssssssssssssssssssssssss
                     ssssssssssssssssssssssssssss
                      @@sssssssssssssssssssssss@ss
                      |s@@@@sssssssssssssss@@@@s|s
               _______|sssss@@@@@sssss@@@@@sssss|s
             /         sssssssss@sssss@sssssssss|s
            /  .------+.ssssssss@sssss@ssssssss.|
           /  /       |...sssssss@sss@sssssss...|
          |  |        |.......sss@sss@ssss......|
          |  |        |..........s@ss@sss.......|
          |  |        |...........@ss@..........|
           \  \       |............ss@..........|
            \  '------+...........ss@...........|
             \________ .........................|
                      |.........................|
                     /...........................\
                    |.............................|
                       |.......................|
                           |...............|


               __         __  __ ___      __   __  __  __
              |_  | |\ | |_  (_   |      |__) |_  |_  |__)
              |   | | \| |__ __)  |      |__) |__ |__ | \




              /|
                                     |\|
                                     |||
                                     |||
                                     |||
                                     |||
                                     |||
                                     |||
                                  ~-[{o}]-~
                                     |/|
              ___                    |/|
             ///~`     |\\_          `0'         =\\\\         . .
            ,  |='  ,))\_| ~-_                    _)  \      _/_/|
           / ,' ,;((((((    ~ \                  `~~~\-~-_ /~ (_/\
         /' -~/~)))))))'\_   _/'                      \_  /'  D   |
        (       (((((( ~-/ ~-/                          ~-;  /    \--_
         ~~--|   ))''    ')  `                            `~~\_    \   )
             :        (_  ~\           ,                    /~~-     ./
              \        \_   )--__  /(_/)                   |    )    )|
    ___       |_     \__/~-__    ~~   ,'      /,_;,   __--(   _/      |
  //~~\`\    /' ~~~----|     ~~~~~~~~'        \-  ((~~    __-~        |
((()   `\`\_(_     _-~~-\                      ``~~ ~~~~~~   \_      /
 )))     ~----'   /      \                                   )       )
  (         ;`~--'        :                                _-    ,;;(
            |    `\       |                             _-~    ,;;;;)
            |    /'`\     ;                          _-~          _/
           /~   /    |    )                         /;;;''  ,;;:-~
          |    /     / | /                         |;;'   ,''
          /   /     |  \\|                         |   ,;(    -Tua Xiong
        _/  /'       \  \_)                   .---__\_    \,--._______
       ( )|'         (~-_|                   (;;'  ;;;~~~/' `;;|  `;;;\
        ) `\_         |-_;;--__               ~~~----__/'    /'_______/
        `----'       (   `~--_ ~~~;;------------~~~~~ ;;;'_/'
                     `~~~~~~~~'~~~-----....___;;;____---~~

              https://www.ascii.co.uk/art/fantasy

              https://www.asciiart.eu/#google_vignette


____   ____.__        __                       
\   \ /   /|__| _____/  |_  ___________ ___.__.
 \   Y   / |  |/ ___\   __\/  _ \_  __ <   |  |
  \     /  |  \  \___|  | (  <_> )  | \/\___  |
   \___/   |__|\___  >__|  \____/|__|   / ____|
                   \/                   \/     
                           ___
                          ( ((
                           ) ))
  .::.                    / /(
 'M .-;-.-.-.-.-.-.-.-.-/| ((::::::::::::::::::::::::::::::::::::::::::::::.._
(J ( ( ( ( ( ( ( ( ( ( ( |  ))   -====================================-      _.>
 `P `-;-`-`-`-`-`-`-`-`-\| ((::::::::::::::::::::::::::::::::::::::::::::::''
  `::'                    \ \(
                           ) ))
                          (_((

                             _______  _______ ___________________________ _______  _______  _       
(  ____ \(  ____ )\__   __/\__   __/\__   __/(  ____ \(  ___  )( \      
| (    \/| (    )|   ) (      ) (      ) (   | (    \/| (   ) || (      
| |      | (____)|   | |      | |      | |   | |      | (___) || |      
| |      |     __)   | |      | |      | |   | |      |  ___  || |      
| |      | (\ (      | |      | |      | |   | |      | (   ) || |      
| (____/\| ) \ \_____) (___   | |   ___) (___| (____/\| )   ( || (____/\
(_______/|/   \__/\_______/   )_(   \_______/(_______/|/     \|(_______/
                                                                        
 _______ __________________ _______  _______  _             _           
(  ___  )\__   __/\__   __/(  ___  )(  ____ \| \    /\     ( )          
| (   ) |   ) (      ) (   | (   ) || (    \/|  \  / /     | |          
| (___) |   | |      | |   | (___) || |      |  (_/ /    __| |__        
|  ___  |   | |      | |   |  ___  || |      |   _ (    (__   __)       
| (   ) |   | |      | |   | (   ) || |      |  ( \ \      | |          
| )   ( |   | |      | |   | )   ( || (____/\|  /  \ \     | |          
|/     \|   )_(      )_(   |/     \|(_______/|_/    \/     (_)          
                                                                        
 _______  _______                                                       
(  ____ \(  __   )       /\                                             
| (    \/| (  )  |  ()  / /                                             
| (____  | | /   |     / /                                              
(_____ \ | (/ /) |    / /                                               
      ) )|   / | |   / /                                                
/\____) )|  (__) |  / /  ()                                             
\______/ (_______)  \/                                                  


                                    <`--._<`--.____________________________ 
                 Dragon              ) ,..-) ,..------------------------,-' 
                                   ,','  >','  \\                  ,        
                                 ,','  ,','     \\            ,             
                               ,','  ,','        \\       ,                 
                             ,' /  ,' /           \\  ,                     
                            /  /  /  /             \`<                      
                           /  /,-/  /,--------------\/                      
                          /__'--/  (/--.                                    
          .-.     ____, '<.  / '   '   '----.                               
         ( . `. ,'    \  '     .-------.  ` '--,                            
          \_) ,'  (_.  \      /         `-----<\                            
          \'   ,'', `.  \   ,'   ,  '          `\                           
         _/ _/',O)>   )  )_            ,'        >                          
     \  (o /o) \` )  /  /'\`   `------<___   ,   )                          
      \`-)| (/`,)\`-'  /   `.          /   >-'    \                         
       `-VvvV ,/( `---'\     `       ,'   /`.      )                        
           / ,/\    \   `.    `          ' ,'`.   '\                        
         (^^(/`      \    `--<, ` --------' ,' `.   )                       
          ``` ________>  ,'   `-')  `      /     \  |                       
     ,-------'        `  )   .--'     ,   /       \  |_                     
   ,'/ _,--,--,,,-,______>   )     \,    (_.-.     \   ),---.               
  / ,\ )                   ,'     ,'          \ .--.\,  .__, \-.            
 /_/ /\)                  /      /             / )-.    /--`--) \           
( )\ ) `                 .      /             (-'   `--'      `--)          
 \' \'                  ,      .                 )                          
                        ,     ,                ,'                           
                         `.  .               ,'`.                           
                        ,',` |              /-.  `.                         
                       ( (   |              \  \   `._                      
                        \ \  /             \    \     \.                    
                         \ \  /          ,\`-.   \  ,'  )                   
                          \ \  /`--,--,-')   /    \'   /                    
                           \ `---------,'   /-.    \\,'                     
                            `--------,'    /-. \                            
                                    /     /   ) )                           
                                   (      > ,/ (_                           
                                  /`-,---'\ |, ,'                           
                                  `-^-----' |,'




CREATE TABLE Inventory (
    id VARCHAR(36) PRIMARY KEY,
    player_id INT,
    
);
CREATE TABLE Player (
    id VARCHAR(36) PRIMARY KEY, -- UUID
    name VARCHAR(255) NOT NULL, -- Nom du joueur
    pv INT DEFAULT 10,          -- Points de vie
    strength INT DEFAULT 10,    -- Force
    weapon_id VARCHAR(36),              -- Référence à une arme (foreign key)
    defense_id VARCHAR(36),             -- Référence à une défense (foreign key)
    type VARCHAR (255),         -- 
    gold INT DEFAULT 0,         -- Or
    exp INT DEFAULT 0,          -- Expérience
    level INT DEFAULT 1,        -- Niveau
    inventoryCapacity INT DEFAULT 0 -- Capacité de l'inventaire
);

CREATE TABLE Defense (
    id VARCHAR(36) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    defense INT NOT NULL,
    type VARCHAR(255) NOT NULL,
    weight INT NOT NULL,
    value INT NOT NULL
);
INSERT INTO defense(id, name, defense,type ,weight, value )

CREATE TABLE Weapon (
    id VARCHAR(36) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    attack INT NOT NULL,
    type VARCHAR(255),
    value INT NOT NULL,
    weight INT NOT NULL
);



INSERT INTO Weapon(id, name,attack, type, value, weight)



CREATE TABLE Player (
    id VARCHAR(36) PRIMARY KEY, -- UUID
    name VARCHAR(255) NOT NULL, -- Nom du joueur
    pv INT DEFAULT 10,          -- Points de vie
    strength INT DEFAULT 10,    -- Force
    weapon_id VARCHAR(36),              -- Référence à une arme (foreign key)
    defense_id VARCHAR(36),             -- Référence à une défense (foreign key)
    inventory_id VARCHAR(36)
    type VARCHAR (255),         -- 
    gold INT DEFAULT 0,         -- Or
    exp INT DEFAULT 0,          -- Expérience
    level INT DEFAULT 1,        -- Niveau
    inventoryCapacity INT DEFAULT 0 -- Capacité de l'inventaire
);


CREATE TABLE Inventory (
    id VARCHAR(36) PRIMARY KEY,
);

CREATE TABLE Defense (
    id VARCHAR(36) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    defense INT NOT NULL,
    type VARCHAR(255) NOT NULL,
    weight INT NOT NULL,
    value INT NOT NULL,
    inventory_id VARCHAR(36)
);

CREATE TABLE Weapon (
    id VARCHAR(36) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    attack INT NOT NULL,
    type VARCHAR(255),
    value INT NOT NULL,
    weight INT NOT NULL,
    inventory_id VARCHAR(36)
);

