## SPA ( SINGLE PaGE APPLICATION) Vue.js (javascirpt)

## Voir le design pattern (MVVM)

### Langague ES6+: 


my-vue-app/
├── src/
│   ├── assets/              # Pour les fichiers statiques (images, styles CSS)
│   ├── components/          # Composants réutilisables (ex : Navbar, Footer)
│   ├── views/               # Pages (ex : Home, Orders, Vehicules)
│   ├── router/              # Gestion du routage
│   ├── store/               # Gestion de l'état global avec Vuex (si nécessaire)
│   ├── services/            # Fichiers pour les appels API
│   ├── App.vue              # Composant principal
│   └── main.js              # Point d'entrée de l'application
└── public/
    └── index.html           # Template HTML de l'application

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

#### FrameWork : EXpress sert à faire des API, interressant d'aller y faire un saut. 

Checker aussi les Websocket pour le multi joueur 



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

Vitejs le bundler  axios utile pour la création des requêtes Get Post Put Delete 

vitejs.dev/guide  Router et pinia



Décrire le concept de Single Page App

    On affiche un site entier sur une seule page html, le header et le footer sont statics et c'est le contenu qui va changer en fonction des requêtes http


Différencier le web mobile du mobile natif

    Le web mobile est dévelloppé pour un navigateur mobile et computer, le native est spécialement dévellopé pour le mobile et peut utiliser les fonctionnalité native des appareils, tels que :

    Suivi de la localisation de l'appareil
    Microphone et caméras de l'appareil
    Listes de contacts des utilisateurs
    Gestes tactiles, inclinaison de l'appareil et autres interactions de l'utilisateur
    Fonctionnalités de sécurité de l'appareil comme la numérisation d'empreintes digitales ou la reconnaissance faciale

Comprendre l’utilité de l’approche composants

    L'approche composant est une manière d'organiser son code pour le single page application en créant un composant pour un tache et permettant de décomposer au maximum les items d'une page. 

Quand et pourquoi ce type d'applications a vu le jour ?

    Introduit en 2005 par Steve Yen afin d'éviter de recharger toute la page mais seulement la partie de son contenu nécessaire. 
    Permet un meilleur affichage (plus léger) des pages web pour les ordinateurs certes mais aussi et surtout pour les mobiles (le fait d'avoir une utilisation nomade rapport à la couverture reseau)


Quels sont les avantages et inconvénients de cette approche ?

    Les avantages: 
    rapidité, débugging sans se soucier du coté serveur, adaptabilité aux applications mobiles

    Les inconvenient: 
    Moins bon SEO (moins d'informations )

Quels sont les principaux frameworks utilisés pour développer des "SPA" de nos jours ?
 
    { 
      "Framework":"SPA",
      { "nom" : "Angular", "Date_de_sortie":"2010", "Mainteneur" : "Google", "Licence": "MIT", "Spec":"Approche modulaire orientée composant basé sur modèle MVVM"}, 
      { "nom" : "React", "Date_de_sortie":"2013", "Mainteneur" : "Facebook", "Licence": "MIT", "Spec":"Approche orienté composant qui s'apparente à une bibliothèque"}, 
      { "nom" : "Angular", "Date_de_sortie":"2014", "Mainteneur" : "Ancien Dev Angular ", "Licence": "MIT", "Spec":"Approche modulaire orienté compposant de type bibliothèque"} 
    }

Pour tout savoir : https://digiwin.fr/actualites/angular-react-et-vue-quel-framework-spa-choisir/#:~:text=Pr%C3%A9sentation%20de%20Angular%2C%20React%20et,Ils%20sont%20open%2Dsource.



### Exercices sur playground Vue.js 

Rendez votre application réactive : affichez dans le titre du texte qui sera renseigné en Javascript, dans l'objet data de Vue.
Modifiez la valeur de votre data dans l'extension Vue DevTools.
Un champ input permettant de mettre à jour le contenu d’une balise H1
Un champ input permettant de mettre à jour le contenu d’une balise H1 au clic sur un bouton. Attention, pas seulement quand l'input perd le focus !
Une checkbox permettant d’ajouter la classe "red" aux H1 et H2 quand elle est cochée
Une checkbox pour afficher / masquer une image

    <template>
      <h1>{{titre}}</h1>
      <input placeholder= "change le titre en haut" v-model="titre"/> 
      <input placeholder= "change le titre en bas avec boutton" v-model="titreChanger" />
      <button @click="changeTitre">Change le Titre</button>
      <input type="checkbox" v-model="changeColor" > Title in Red </input>
      <input type="checkbox" v-model="imgPrint" > Affiche l'image </input>
      <h1 :class="{redColor:changeColor}">{{titreBoutton}}</h1> 
      <img v-if="imgPrint" src="https://www.journalduluxe.fr/files/mercedes-haute-voiture_70b6b237f932ea3aaddcc781e6bd1c0a.jpeg"/> 
    </template>

    <script>
    
    
    export default {
      data(){
        return {
          titre: "",
          titreBoutton: "",
          titreChanger: "",
          changeColor:false,
          imgPrint:false
        }
      },
      methods:{
      changeTitre() {
        console.log(this.titreChanger)
        this.titreBoutton = this.titreChanger;
      },
    }
    }
    </script>


    <style>
    
    .redColor {
      color: red;
    }

    </style>

## API 

https://abhiappmobiledeveloper.medium.com/free-api-huge-list-of-public-apis-for-developertesting-b9cf371282b3

