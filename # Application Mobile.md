# Application Mobile

## La structure 

IDE: Android Studio 

Langage: Kotlin (the new JAVA)

build.gradle.kts = C'est le fichier qui va permettre de construire (compiler) l'application en indiquant les dépedances et toutes les informations relatives à son instalation à l'image d'un dockerfile.   Configure les tâches et dépendances spécifiques au module.

settings.gradle.kts = Configure la strcture globale

libs.versions.toml = Centralise les librairies pour simplifier les mise à jour.


New design pattern: le MVP Model-View-Presenter

|View/Activity||Presenter||Model|

## Créer un ViewModel : Gérez la logique de l’appel API et exposez un état à observer par le composable.

Utiliser LaunchedEffect : Déclenchez l’appel API lorsque le composable est affiché pour la première fois ou lorsque des paramètres changent.

Mettre à jour l’état avec un SideEffect : Si nécessaire, déclenchez des effets secondaires (par ex., enregistrement d’un journal ou suivi analytique).


## La sealed class les ENUM

Une sealed class en Kotlin est une classe qui permet de restreindre la hiérarchie de classes - c'est comme une enum class plus puissante. Elle est particulièrement utile pour représenter un ensemble limité d'états ou de types possibles. Dans notre cas, elle représente les différents écrans de navigation possibles.

## Singleton 

Objet unique avec un seul point d'entrée 

exemple: le DwitchService qui gère la connection avec retrofit et moshi pour la transformation de json en objet kotlin. 

## Nommage et typage des dossiers

Les fichiers en Pascal
Les classes en Pascal
Les attributs en camel
Les fonctions/methodes en camel Si composant nommage en pascal
les annotations en Pascal


## LE MVVM

Model : Représente les données et la logique métier.
 Par exemple, ici, les données des articles sont obtenues via l'API grâce à Retrofit, et transformées en objets Kotlin (News, NewsResponse).
View : C'est l'interface utilisateur (UI).
 Dans ce projet, la vue est créée avec Jetpack Compose. Elle réagit aux états exposés par le ViewModel.
ViewModel : Sert de pont entre la vue et le modèle. 
Il contient la logique pour gérer les données (comme les appels API) et expose des états réactifs (via StateFlow) que la vue peut observer.

### Rappel de SOLID

|S| Single Responsibility Principle (SRP)
    |_Une classe ne faire qu'une seule chose 
|O| Open/Closed Principle (OCP)
    |_Une classe doit être ouverte à l'extansion et fermée à la modfication 
|L| Liskov Substitution Principle (LSP)
    |_Les classe enfant ne doivent pas alterrer les classes Parentes
|I| Interface Segregation Principle (ISP)
    |_Les Interface proposent des contrats de méthodes uniquement utiles à l'utilisateur
|D| Dependency Inversion Principle (DIP)
    |_Tout faire pour favoriser les classes abstraites et les implémentations pour éviter les dépendances directs


    Single Responsability Principle ou « principe de responsabilité unique »
    Open Close Principle ou « principe Ouvert / Fermé »
    Liskov Substitution Principle ou « principe de substitution de Liskov »
    Interface Segregation Principle ou « principe de ségrégation d’interface »
    Dependency Inversion Principle ou « principe d’inversion des dépendances »

## Framework JetPack Compose

Il s'agit d'un framework qui permet de créer des interfaces UI en Kotlin et qui permet de se passer du XML pour la gestion des views. 

Il permet quand même de continuer à utiliser du XML pour gérer les views. 

Pour transformer du code en interface on utilise des annotation (tel que @composable) pour indiquer un élement d'interface. 

Programmation impérative =  On dit comment faire 

            fun sumOfEvenNumbersImperative(numbers: List<Int>): Int {
            var sum = 0
            for (number in numbers) {
             if (number % 2 == 0) { // Vérifie si le nombre est pair
            sum += number // Ajoute le nombre à la somme
                    }
                }
            return sum
            }

            fun main() {
                val numbers = listOf(1, 2, 3, 4, 5, 6)
                println(sumOfEvenNumbersImperative(numbers)) // Sortie : 12
            }


Programmation déclarative = On dit quoi faire

            fun sumOfEvenNumbersDeclarative(numbers: List<Int>): Int {
            return numbers.filter { it % 2 == 0 } 
                  .sum()
            }

            fun main() {
                val numbers = listOf(1, 2, 3, 4, 5, 6)
                println(sumOfEvenNumbersDeclarative(numbers)) 
            }


Après avoir creuser le sujet des programmation déclarative et impérative, j'ai l'imprression que dans l'impérative on va articuler les méthodes avec des boucles, des conditions, alors qu'avec le déclaratif on s'appuis plus sur les méthodes et déclaration pour obtenir un resultat. 

    Arborescence d'un projet avec JetPack Compose: 

src/main/
├── java/com/example/app/
│   ├── data/
│   │   ├── model/
│   │   │   ├── User.kt
│   │   │   ├── Post.kt
│   │   │   ├── Comment.kt
│   │   │   ├── ApiResponse.kt
│   │   │   └── [Autres modèles liés aux données]
│   │   ├── repository/
│   │   │   ├── UserRepository.kt
│   │   │   ├── PostRepository.kt
│   │   │   └── [Autres classes de gestion de données]
│   │   └── datasource/
│   │       ├── remote/
│   │       │   ├── ApiService.kt
│   │       │   └── [Sources de données distantes]
│   │       └── local/
│   │           ├── Database.kt
│   │           ├── UserDao.kt
│   │           └── [Sources de données locales]
│   ├── ui/
│   │   ├── theme/
│   │   │   ├── Color.kt
│   │   │   ├── Typography.kt
│   │   │   ├── Theme.kt
│   │   ├── screen/
│   │   │   ├── home/
│   │   │   │   ├── HomeScreen.kt
│   │   │   │   ├── HomeViewModel.kt
│   │   │   │   ├── HomeUiState.kt
│   │   │   │   └── [Composables liés à l'écran d'accueil]
│   │   │   ├── detail/
│   │   │   │   ├── DetailScreen.kt
│   │   │   │   ├── DetailViewModel.kt
│   │   │   │   └── [Composables liés à l'écran de détails]
│   │   │   └── [Autres écrans]
│   │   └── [Autres composants UI]
│   └── utils/
│       ├── Constants.kt
│       ├── Extensions.kt
│       └── [Autres utilitaires]
└── res/
    ├── drawable/
    ├── layout/
    ├── values/
    └── [Ressources UI]



## Concernant le Front

Hyper important pour tous ce qui est application mobile, il existe des pattern et des design déja fait qui correspondent à des utilisation adaptée pour portable pas besoin de réinventer la roue, il faut principalement privilégier l'utilisation du material

Utiliser les composants Material Design

https://m3.material.io/

#### Le scaffold
https://developer.android.com/develop/ui/compose/components/scaffold?hl=fr

### Ressources

https://www.chrbutler.com/gestalt-principles-of-design-proximity
https://lawsofux.com/
https://docs.strapi.io/dev-docs/backend-customization

dependencies {
    // Retrofit & OkHttp
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.okhttp3:okhttp:4.11.0")
    implementation("com.squareup.okhttp3:logging-interceptor:4.11.0") // Pour log des requêtes

    // Moshi & Moshi Converter
    implementation("com.squareup.moshi:moshi:1.15.0")
    implementation("com.squareup.retrofit2:converter-moshi:2.9.0")

    // KSP pour Moshi
    ksp("com.squareup.moshi:moshi-kotlin-codegen:1.15.0")


Manifest
    <uses-permission android:name="android.permission.INTERNET" />


projet Ktolin 
framework JetPack compose
ide android studio 

api management 
retrofit
moshi
ksp




// Créez d'abord un sealed class pour représenter les écrans
sealed class Screen(val route: String, val icon: ImageVector, val label: String) {
    object Profile : Screen("profile", Icons.Default.Person, "Profile")
    object News : Screen("news", Icons.Default.Star, "News")
    object Ordering : Screen("ordering", Icons.Default.ShoppingCart, "Commandes")
}

@Composable
fun MainScreen() {
    var currentScreen by remember { mutableStateOf<Screen>(Screen.Profile) }
    
    DwitchAppTheme {
        Scaffold(
            topBar = {
                TopAppBar(
                    colors = TopAppBarDefaults.topAppBarColors(
                        containerColor = Color(0xFFFFC078),
                        titleContentColor = Color(0xFF212529),
                    ),
                    title = {
                        Text("Mes Commandes")
                    }
                )
            },
            bottomBar = {
                BottomAppBar(
                    containerColor = Color(0xFFFFC078),
                ) {
                    val items = listOf(
                        Screen.Profile,
                        Screen.News,
                        Screen.Ordering
                    )
                    items.forEach { screen ->
                        NavigationBarItem(
                            icon = { Icon(screen.icon, contentDescription = screen.label) },
                            label = { Text(screen.label) },
                            selected = currentScreen == screen,
                            onClick = { currentScreen = screen }
                        )
                    }
                }
            }
        ) { innerPadding ->
            Column(
                modifier = Modifier
                    .padding(innerPadding)
                    .background(Color(0xFF000000))
            ) {
                when (currentScreen) {
                    Screen.Profile -> ProfileScreen()
                    Screen.News -> NewsScreen()
                    Screen.Ordering -> OrderingScreen()
                }
            }
        }
    }
}

// Modifiez votre MainActivity comme ceci :
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContent {
            MainScreen()
        }
    }
}

username: Rodolphe 
e-mail: rodolphe@test.fr
pswd: password2024