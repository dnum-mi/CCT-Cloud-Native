# Pattern Traçage en environnements distribués

Date : xx/xx/2022

## Statut

    Brouillon

##  Contexte

Définition d'un pattern d'architecture de mise en correlation données evenements/alertes des servces liés.

## Decision

Dans un contexte applicatif, plusieurs services peuvent être impliqués. L'utilisation d'un suivi distribué peut donner un aperçu de ce que font les services. 
    
Un traceur distribué est similaire à un profileur de performance dans une application monolithique. Il enregistre des informations sur les appels de service qui sont effectués lors du traitement d'une requête. Vous pouvez alors voir comment les services interagissent pendant le traitement des demandes externes, ainsi que le temps passé sur chaque service.
    
Chaque demande externe se voit attribuer un identifiant unique et est suivie au fur et à mesure qu'elle passe d'un service à un autre sur un serveur centralisé qui fournit une visualisation et une analyse.

##  Consequences

__