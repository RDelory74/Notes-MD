# JAVA
## RESSOURCES
https://www.w3schools.com/java/java_getstarted.asp

https://www.codecademy.com/learn/learn-java

https://openclassrooms.com/en/courses/6173501-apprenez-a-programmer-en-java

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


### Le Scanner

### L'Héritage

### Surcharger ou remplacer des comportement de classe mère: Le polymorphisme

En réutilisant un méthode de classe on applique un: 
Avec super. 

On vient mettre un 

@Override au dessus de la méthode pour lui indiquer qu'on va la surcharger. 



import java.util.Scanner;
import java.awt.event.KeyEvent;
import java.util.Random;



public class Menu {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random random = new Random();

        System.out.println("Welcome to Dungeons & Dragons!");
        System.out.println("Let's create a new player");


        System.out.print("Enter your character name: ");
        String characterName = sc.nextLine();
        System.out.print("Enter your character Type Choose Warrior or Wizard: ");
        String characterType = sc.nextLine();

        if( characterType.equals("Warrior")||characterType.equals("Wizard")) {
            Character character = new Character(characterName, characterType);

        System.out.println("C'est alors que des entrailles de l'abysse jailli notre nouveau héros: " + character.toString());
        System.out.println("Character name: " + characterName);
        System.out.println("Character type: " + characterType);

        while (true) {
            System.out.println("\nMain Menu:");
            System.out.println("1. Voir Info Héros");
            System.out.println("2. Modifier infos Héros");
            System.out.println("0. Exit");
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();
            if (choice == 0) {
                break;
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
                if (custChoice == 0) {
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
__________ZZZ_ZZZ_ZZZ_ZZZ_ZZZ
___________ZZZZZZZZZZZZZZZZZ
______________ZZZZZZZZZZZ


____*#####*
___*########*
_*###########*
_*############*
_*#############*_________*##*
_*#############*_____*#######*
_*#############*___*##########*
__*#############*_*###########*
___*#############*############*
____*########################*
_____*#######################*
______*#####################*
________*##################*
_________*################*
__________*#############*
___________*##########*
____________*#######*
_____________*#####*
______________*###*
_______________*#*
________________*

