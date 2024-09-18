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