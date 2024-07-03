

# POO (Programmation Orientée Objet)



## Principe de la programmation orientée Objet

Un paradigme de structure de code, ou d'agencement de code ou chaque entité est un objet issu d'une classe et contenant des attributs ainsi que des méthodes 

## Programmation proccédurale et programmation Orientée Objet

La programmation proccédurale est le mode de programmation classique 

## Glossaire et Concept


### Concept

Encapsulation: C'est le fait de protéger des données en forçant l'utilisateur à utiliser certaines méthodes.

Propriétés: Il s'agit des caractérisiques d'un classe (pour une classe appellée: voiture on va lui attribuer des propriétés: type moteur, vitesse max, couleur, nb de porte) (->)

### Glossaire 

getters / setters :

    Set on assigne une valeur à une variable.
    Get on obtient (récupère) la valeur d'une variable.

methodes : 

    Est une action associée à un objet (exemple: porte.ouvrir ou alors ampoule.allumer on obtient une écriture de type objet.méthode) 

instancier :

     C'est la création d'un objet à partir d'une classe. (new)

Objet : 

    C'est la caractéristique d'une classe (ex: la taille, la race)

Classe :

     C'est le type d'une entité (exemple une classe: Chiens) c'est le mode d'emploi, le modèle pour instancier des objets 

héritage :

     / par abstraction l'objet hérite de la classe par lequel il est instancier. 

abstraction :

    Est une classe qu'on ne peux pas instancier. Parent utlime

interfaces :

    L'ensemble des actions imposées par une classe abstraite et qui découlera sur les classes enfants.


surcharge :

    Avec la commande extends on permet d'assigner les mêmes propriétées qu'une classe déja existante mais d'en modifier certaine méthode pour les besoins de l'objet. 

attributs: 

    C'est la caractéristique d'un Objet 

Visibilité d'une variable: 

    Public : N'importe qui à accés à la valeur
    Private : Il faut un getteur pour récupérer une valeur, et un setteur pour la modifier
    Protected : Il n'y a que les enfants qui peuvent le modifier


### Découverte des outils 

C’est quoi un autoload en php ?

    C'est une fonction qui va se charger de lancer un fichier lorsqu'on appel une classe. 


Qu’est-ce qu’un fichier .PHAR ?

    C'est une archive zipper d'un ensemble de fichier PHP que l'on peut faire tourner sans l'extraire 

Qu’est-ce que composer ?

    C'est un gestionnaire de téléchargement de packages. 

Quel intérêt y-a-t’il à l’utiliser ?

    Il permet de gérer et d'intégrer des paquets dans leur projets PHP. 

Quelle est la version actuelle de composer ?

    Composer v2.7.7


C’est quoi PSR ?

    L'ensemble des normes qui régissent l'écriture du code PHP c'est un standard d'écriture
    https://www.itefficience.com/article/qu-est-ce-que-les-psrs-et-a-quoi-servent-ils

C’est quoi PSR-4 ?

    Définit un système d'autoloading pour permettre aux dévellopeur d'appeller des classes sans avoir à les inclures. (Chargement automatique des classes)



## Ressources Supp 

https://php.watch/versions/8.1/readonly

https://www.w3schools.com/php/php_oop_classes_abstract.asp

https://www.w3schools.com/php/php_namespaces.asp

https://grafikart.fr/tutoriels/presentation-1091#autoplay





https://what-if.xkcd.com/29/


$animals = array(
    array("Poisson",5,getNoise()),
    array("BubbleFish",3,noise()),
    array("CatFish",2,noise()),
    array("ClownFish",1,noise()),
    array("Dove",2,noise()),
    array("Elephant",2,noise()),
    array("Zebra",1,noise()),
    array("Parrot",10,noise())
);



for ($row =0; $row < count($animals); $row++) {
    echo $animals[$row][0] . "\n";
    for($col = 0; $col < count($animals[$row]); $col++) {
        echo "L'animal".$animals[$row][$col] . "\n";
    }
}   