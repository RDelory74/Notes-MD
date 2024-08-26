## SPA ( SINGLE PaGE APPLICATION)

### Langague ES6+: 

Connaître la différence entre let et const
        
        let: appel une variable que l'on peut modifier
        const: appel une variable qui ne changera pas 

Connaissance du rôle de this

        this: correspond à la valeur du context englobant. Le mot-clé this permet de désigner, dans une classe, l'objet courant de la classe elle-même. Lorsqu'on code une classe, on prévoit le comportement pour un objet que l'on va utiliser.


Importer et exporter des modules

        fonction codée sur un fichier qui fonctionne en isolation et que l'on va importer avec from suivi du chemin relatif du fichier.

        named method to import: import { name, age } from "./person.js"; // default method to import: import message from "./message.js";
        la même pour l'export 

Utilisation du “destructuring”

        methode de création d'objet, écrite differement: 

                // Create an Object
                const person = {
                  firstName: "John",
                  lastName: "Doe",
                  age: 50
                };

                // Destructuring
                let {firstName, lastName} = person;

Utilisation des promesses

        Est un objet qui remplace une fonction avec deux callbacks (voir plusieurs), cela permet de traité du code de façon asynchrone et d'attendre un resultat. On va ensuite avoir un effet de chaînage en fonction des resultats attendus. 

Utilisation de l’API fetch

        Permet d'effectuer des requêtes http suite à une promesse. Il s'agit donc d'une interface en javascript 

Utilisation d’async/await

        Un type de fonction qui se lit de bas en haut, cela permet de lire une fonction de manière inversée

### Node JS: 

Créer script NPM

        il s'agit d'un fichier javascript avec des fonctions et des scirpt à l'intérieur que l'on peut appeller via le terminal et qui nous évite de réécrire le code. On utilise le node-JS packager

Lancer un script avec npm

        npm run //exemple// component [name] [cmd]

Installer un package npm

        npm install // npm install <package-name>

Créer un programme en Node.js

        créer un fichier.js avec un script javascript à l'interieur et l'appeller sur le terminal // node (nom du fichier.js) 


### NPM: 

### FrameWorks: (vue.js)