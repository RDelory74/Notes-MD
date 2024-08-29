## SPA ( SINGLE PaGE APPLICATION)

### Langague ES6+: 

#### Connaître la différence entre let et const

        let: appel une variable que l'on peut modifier
        const: appel une variable qui ne changera pas 

#### Connaissance du rôle de this

        this: correspond à la valeur du context englobant. Le mot-clé this permet de désigner, dans une classe, l'objet courant de la classe elle-même. Lorsqu'on code une classe, on prévoit le comportement pour un objet que l'on va utiliser.


#### Importer et exporter des modules

        fonction codée sur un fichier qui fonctionne en isolation et que l'on va importer avec from suivi du chemin relatif du fichier.

        named method to import: import { name, age } from "./person.js"; // default method to import: import message from "./message.js";
        la même pour l'export 

#### Utilisation du “destructuring”

        methode de création d'objet, écrite differement: 

                // Create an Object
                const person = {
                  firstName: "John",
                  lastName: "Doe",
                  age: 50
                };

                // Destructuring
                let {firstName, lastName} = person;

#### Utilisation des promesses

        Est un objet qui remplace une fonction avec deux callbacks (voir plusieurs), cela permet de traiter du code de façon asynchrone et d'attendre un resultat. On va ensuite avoir un effet de chaînage en fonction des resultats attendus.

        On chaine avec then (si la promesse est resolue ou catch si ellee est rejetée) et finally pour executer le code whatever

                try {
                  first().then(()=>secondWithError());
                }
                catch(err){
                  first().then(()=>secondWithError());
                }
                finally {
                  first().then(()=>third());
                }

                first().then(()=>{secondWithError()}).catch(()=>{secondWithError()}).then(()=>{third()});

                first().then(()=>{secondWithError()}).catch(()=>{secondWithError()}).then(()=>{third()});

//////Exemples d'Alban sur les promises:///// 

        function wait(delay, myCallbackFunction){
    setTimeout(() => {
        console.log("dans ma fonction wait")

        const user = {
            firstName: "Alban"
        }

        myCallbackFunction(user, "oisdhfqshdfoiqldsf")
    }, delay)
        }


        console.log("afficher coucou chose après 3s")
        wait(5000, (user, str) => {
    console.log("coucou")
    console.log(user)
    console.log(str)
        })




        async function waitWithPromise(delay){
    r  eturn new Promise((maFonctionQuandToutSePasseBien, reject) => {
        setTimeout(() => {
            console.log("after delay")

            const user = {
                firstName: "Alban"
            }

            reject("Mon serveur est down")
            //maFonctionQuandToutSePasseBien(user)
        }, delay)
    })
        }


        console.log("afficher coucou chose après 3s")
        waitWithPromise(5000).then((user) => {
            console.log("coucou")
            console.log(user)
        }).catch((e) => {
            console.log("Ca a fail")
            console.log(e)
        }).finally(() => {
            console.log("c'est fini")
        })


        try {
            const user = await waitWithPromise(5000)
            console.log("salut")
            console.log(user)
        } catch(e){
            console.log("ça a pas marché")
        }

        const myUser = await waitWithPromise(5000).catch(e => console.log("ça a pas marché non plus"))

#### Utilisation de l’API fetch

        Permet d'effectuer des requêtes http suite à une promesse. Il s'agit donc d'une interface en javascript 

        async function getHumain (){
          const response = await fetch ("https://swapi.dev/api/species/1/");
          const humans = await response.json();
          console.log(humans); 

        }
        getHumain()

Dans le cas ci-dessous ( et c'est très important) les premières parenthèse du then prennent en paramètre les valeurs de la variable de la dernière fonction. (humans)

        getHumain().then((humans)=>postData(humans))



#### Utilisation d’async/await

        async et await c'est une methode appliqué à un fonction pour qu'elle s'execute de manière asynchrone, elle va executer le code après une condition et renvoyer une promesse resolve si le code s'est bien passé, et rejected si le code s'est pas executer normalement. C'est une méthode d'écriture qui vient remplacer la méthode (.then/.catch/.finally)

        Si bien que les deux méthodes s'utilise. 

        Ci-desssous, petit exemple: 

// Utilisation du then

        const makeRequest = () =>
          getJSON()
            .then(data => {
              console.log(data)
              return "done"
            })

        makeRequest()

// Utilisation d'async

        const makeRequest = async () => {
          console.log(await getJSON())
          return "done"
        }

        makeRequest()


Déclaration variable exemple: 

    async function getAsyncNumber1() // renvoie une promesse avec comme valeur un nombre
    async function getAsyncNumber2() // même chose que ligne du dessus

Exemple sans await : 

    const getAsyncAddition = () => getAsyncNumber1().then(number1 => getAsyncNumber2().then(number2 => number1 + number2));

s'écrit aussi:

    const getAsyncAddition = () => {
     let number;
      return getAsyncNumber1()
       .then(vnumber => {
         number1 = vnumber1;
         return getAsyncNumber2();
       })
       .then(number2 => number1 + number2);
    }

avec await: 

    const getAsyncAddition = async () => {
     const number1 = await getAsyncNumber1();
     const number2 = await getAsyncNumber2();
     return number1 + number2;
    }

### Node JS: 

#### C'est quoi Node.js: 

Plateforme pour utiliser et écrire des API alternative à des languages serveur (java, python) elle est non-bloquante ce qui permet de lancer plusieurs taches en même temps sans attendre qu'une tâche soit terminée. 

pour faire lien entre le back-end et le front-end

RTA ça veut dire Real Time Applications, ce sont les applications en temps réel, ce sont ces applications qui ont besoin de se mettre à jour super fréquemment.
exemple what's APP, besoin de mettre à jour fréquement et rapidment 

SPa Single page application 
framework comme angular vue ou react 

multi-thread et single-thread

mutli-thread = plusieurs tahces en parallèle
single-thread = une seule tache à la fois 





Un bref retour sur le Json: 

    Remarquez que JSON requiert non seulement que le nom (la clé) soit entre guillemets, mais aussi que les guillemets soient doubles : les guillemets simples sont possibles sur les objets JavaScript, pas dans JSON.


    // JSON valide
        {
          "foo": "bar"
        }

        // JSON valide
    {
      "species": "Dog",
      "breed": "Labrador Retriever",
      "age": 6,
      "traits": {
        "eyeColor": "brown",
        "coatColor": "yellow",
        "weight": "137lbs"
      }
    }

    // objet JS; non valide en JSON

    let myAnimal = {
      species: "dog",
      breed: "Labrador Retriever",
      age: 6,
      traits: {
        eyeColor: "brown",
        coatColor: "yellow",
        weight: "137lbs"
      }
    }

Transformer du texte en Json 

    La méthode JSON.stringify() prend un paramètre obligatoire (le JSON que vous voulez convertir en string) // on fera l'inverse avec JSON.parse() :

        let myJSON = {
      species: "Dog",
      breed: "Labrador Retriever",
      age: 6,
      traits: {
        eyeColor: "brown",
        coatColor: "yellow",
        weight: "137lbs"
      }
    };

    let myNewJSON = JSON.stringify(myJSON, null, '\t');

    /* output of myNewJSON:
    {
      "species": "Dog",
      "breed": "Labrador Retriever",
      "age": 6,
      "traits": {
        "eyeColor": "brown",
        "coatColor": "yellow",
        "weight": "137lbs"
      }
    }
    */

    Pour aller plus loin : https://la-cascade.io/articles/json-pour-les-debutants


Créer script NPM

        il s'agit d'un fichier javascript avec des fonctions et des scirpt à l'intérieur que l'on peut appeller via le terminal et qui nous évite de réécrire le code. On utilise le node-JS packager

Lancer un script avec npm

        npm run //exemple// component [name] [cmd]

Installer un package npm

        npm install // npm install <package-name>

Créer un programme en Node.js

        créer un fichier.js avec un script javascript à l'interieur et l'appeller sur le terminal // node (nom du fichier.js) 




# vuejs

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).




### FrameWorks: (vue.js)