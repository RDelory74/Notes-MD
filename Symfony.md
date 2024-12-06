# SYMFONY
La structure du framework. 

Symfony, est un ensemble de composants, pour la gestion des requêtes to requêtes (ce n'est pas un MVC) la gestion des repository et des entity (modeles) est assurée par Doctrine. 
Tandis que les view sont gérées par Twig. 

## Les bases et l'installation 

    On est sur un framework php, donc l'instalation est gérée par composer 

## Les commandes magik 

    Symfony 7.1.9 (env: dev, debug: true)
    
    Usage:
      command [options] [arguments]
    
    Options:
      -h, --help            Display help for the given command. When no command is given display help for the list command
      -q, --quiet           Do not output any message
      -V, --version         Display this application version
          --ansi|--no-ansi  Force (or disable --no-ansi) ANSI output
      -n, --no-interaction  Do not ask any interactive question
      -e, --env=ENV         The Environment name. [default: "dev"]
          --no-debug        Switch off debug mode.
          --profile         Enables profiling (requires debug).
      -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug
    
    Available commands for the "make" namespace:
      make:auth                   Create a Guard authenticator of different flavors
      make:command                Create a new console command class
      make:controller             Create a new controller class
      make:crud                   Create CRUD for Doctrine entity class
      make:docker:database        Add a database container to your compose.yaml file
      make:entity                 Create or update a Doctrine entity class, and optionally an API Platform resource
      make:fixtures               Create a new class to load Doctrine fixtures
      make:form                   Create a new form class
      make:functional-test        Create a new test class
      make:listener               [make:subscriber] Creates a new event subscriber class or a new event listener class
      make:message                Create a new message and handler
      make:messenger-middleware   Create a new messenger middleware
      make:migration              Create a new migration based on database changes
      make:registration-form      Create a new registration form system
      make:reset-password         Create controller, entity, and repositories for use with symfonycasts/reset-password-bundle
      make:schedule               Create a scheduler component
      make:security:custom        Create a custom security authenticator.
      make:security:form-login    Generate the code needed for the form_login authenticator
      make:serializer:encoder     Create a new serializer encoder class
      make:serializer:normalizer  Create a new serializer normalizer class
      make:stimulus-controller    Create a new Stimulus controller
      make:subscriber             Creates a new event subscriber class or a new event listener class
      make:test                   [make:unit-test|make:functional-test] Create a new test class
      make:twig-component         Create a twig (or live) component
      make:twig-extension         Create a new Twig extension with its runtime class
      make:unit-test              Create a new test class
      make:user                   Create a new security user class
      make:validator              Create a new validator and constraint class
      make:voter                  Create a new security voter class
      make:webhook                Create a new Webhook
    
## Ressources 

Upload files

//controller new

       $photoFile = $form->get('photo')->getData();
            if ($photoFile) {
                $newFilename = uniqid() . '.' . $photoFile->guessExtension();
                $photoFile->move(
                    $this->getParameter('uploads_directory'), // Configure ce paramètre dans services.yaml
                    $newFilename
                );
                $quack->setPhoto($newFilename);
            }

// FormQuack 

              ->add('photo', FileType::class, [
                'label' => 'Photo',
                'required' => false,
                'mapped' => false, // Le champ photo n'est pas mappé directement à l'entité
            ])

// Services.yaml

    parameters:
    timezone: '%env(APP_TIMEZONE)%'

    //
    uploads_directory: '%kernel.project_dir%/public/uploads'
