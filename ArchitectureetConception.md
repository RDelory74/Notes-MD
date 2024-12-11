
# Qu’est-ce qu’une architecture technique ?

## La stack 

LAMP : Linux, Apache, MySQL, PHP.
MEAN : MongoDB, Express, Angular, Node.js.
MERN : MongoDB, Express, React, Node.js.

## Patterns d’Architecture et Modélisation de la Logique Métier

    MVC (Model-View-Controller)
    MVVM (Model-View-ViewModel)


# Modélisation de la logique métier 

## Diagrammes d'activitées UML 

@startuml

class Patient {
  
id : int
nom : String
prenom : String
email : String
telephone : String
+ prendreRendezVous(creneau : Creneau) : boolean+ annulerRendezVous(rendezVous : RendezVous) : boolean
}

class Medecin {
  
id : int
nom : String
specialite : String
nombreRendezVous : int
+ verifierDisponibilite(date : Date, heure : Time) : boolean+ ajouterRendezVous(rendezVous : RendezVous) : void
}

class RendezVous {
  
id : int
date : Date
heure : Time
statut : String
patient : Patient
medecin : Medecin
+ confirmer() : void+ annuler() : boolean
}

class Creneau {
  
id : int
date : Date
heureDebut : Time
heureFin : Time
estDisponible : boolean
medecin : Medecin
+ reserver(patient : Patient) : boolean
}

class Notification {
  
id : int
type : String
dateEnvoi : Date
destinataire : Patient
+ envoyer() : void
}

class ListeAttente {
  
id : int
patients : List<Patient>
date : Date
+ ajouterPatient(patient : Patient) : void+ notifierProchainPatient() : void
}

Patient "1" -- "n" RendezVous
Medecin "1" -- "n" RendezVous
RendezVous "1" -- "1" Creneau
Creneau "1" -- "1" Medecin
Notification "1" -- "1" Patient
ListeAttente "1" -- "n" Patient

@enduml

                 ┌──────────────────────┐                                                                                 
                 │Notification          │   ┌────────────────────────────────────────────────────────────────────────────┐
                 ├──────────────────────┤   │ListeAttente                                                                │
                 │                      │   ├────────────────────────────────────────────────────────────────────────────┤
                 │id : int              │   │                                                                            │
                 │type : String         │   │id : int                                                                    │
                 │dateEnvoi : Date      │   │patients : List<Patient>                                                    │
                 │destinataire : Patient│   │date : Date                                                                 │
                 │+ envoyer() : void    │   │+ ajouterPatient(patient : Patient) : void+ notifierProchainPatient() : void│
                 └──────────────────────┘   └────────────────────────────────────────────────────────────────────────────┘
                                                                                                                          
                                                                                                                          
    ┌──────────────────────────────────────────────────────────────────────────────────────────────────────┐              
    │Patient                                                                                               │              
    ├──────────────────────────────────────────────────────────────────────────────────────────────────────┤              
    │                                                                                                      │              
    │id : int                                                                                              │              
    │nom : String                                                                                          │              
    │prenom : String                                                                                       │              
    │email : String                                                                                        │              
    │telephone : String                                                                                    │              
    │+ prendreRendezVous(creneau : Creneau) : boolean+ annulerRendezVous(rendezVous : RendezVous) : boolean│              
    └──────────────────────────────────────────────────────────────────────────────────────────────────────┘              
                                                        |                                                                 
                                   ┌─────────────────────────────────────────┐                                            
                                   │RendezVous                               │                                            
                                   ├─────────────────────────────────────────┤                                            
                                   │                                         │                                            
                                   │id : int                                 │                                            
                                   │date : Date                              │                                            
                                   │heure : Time                             │                                            
                                   │statut : String                          │                                            
                                   │patient : Patient                        │                                            
                                   │medecin : Medecin                        │                                            
                                   │+ confirmer() : void+ annuler() : boolean│                                            
                                   └─────────────────────────────────────────┘                                            
                                                                                                                          
                                                                                                                          
                                                ┌───────────────────────────────────────┐                                 
                                                │Creneau                                │                                 
                                                ├───────────────────────────────────────┤                                 
                                                │                                       │                                 
                                                │id : int                               │                                 
                                                │date : Date                            │                                 
                                                │heureDebut : Time                      │                                 
                                                │heureFin : Time                        │                                 
                                                │estDisponible : boolean                │                                 
                                                │medecin : Medecin                      │                                 
                                                │+ reserver(patient : Patient) : boolean│                                 
                                                └───────────────────────────────────────┘                                 
                                                                                                                          
┌───────────────────────────────────────────────────────────────────────────────────────────────────────────────┐         
│Medecin                                                                                                        │         
├───────────────────────────────────────────────────────────────────────────────────────────────────────────────┤         
│                                                                                                               │         
│id : int                                                                                                       │         
│nom : String                                                                                                   │         
│specialite : String                                                                                            │         
│nombreRendezVous : int                                                                                         │         
│+ verifierDisponibilite(date : Date, heure : Time) : boolean+ ajouterRendezVous(rendezVous : RendezVous) : void│         
└───────────────────────────────────────────────────────────────────────────────────────────────────────────────┘         

https://plantuml.com/fr-dark/sequence-diagram

# Diagramme de flux

