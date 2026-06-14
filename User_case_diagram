@startuml
left to right direction
skinparam packageStyle rectangle

actor "Directeur" as Dir
actor "Caissier" as Cai
actor "Magasinier" as Mag
actor "Chef de rayon" as Chef
actor "Gestionnaire de stock" as Ges
actor "Client" as Cli
actor "Comptable" as Comp

rectangle "SUPERMARKET MANAGER" {
  usecase "Se connecter" as UC_Connexion
  
  usecase "Gérer les ventes et caisse" as UC_Vente
  usecase "Encaisser les paiements" as UC_Paiement
  usecase "Imprimer les factures" as UC_Facture
  
  usecase "Gérer le stock" as UC_Stock
  usecase "Réceptionner les livraisons" as UC_Reception
  
  usecase "Gérer les rayons" as UC_Rayon
  
  usecase "Créer une commande fournisseur" as UC_Cmd
  
  usecase "Consulter les statistiques" as UC_Stats
  usecase "Gérer les employés" as UC_Emp
  
  usecase "Calculer les recettes" as UC_Recette
}

' Héritage ou inclusion globale (tous les employés doivent se connecter)
Cai --> UC_Connexion
Mag --> UC_Connexion
Chef --> UC_Connexion
Ges --> UC_Connexion
Comp --> UC_Connexion
Dir --> UC_Connexion

' Assignation des rôles selon le cahier des charges
Cai --> UC_Vente
Cai --> UC_Paiement
Cai --> UC_Facture

Mag --> UC_Stock
Mag --> UC_Reception

Chef --> UC_Rayon

Ges --> UC_Stock
Ges --> UC_Cmd

Comp --> UC_Vente
Comp --> UC_Paiement
Comp --> UC_Recette

Dir --> UC_Stats
Dir --> UC_Emp

Cli --> UC_Paiement
@enduml
