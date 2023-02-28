# pattern Gestion des secrets

Date : 15/02/2023

## Statut

Proposée

##  Contexte

Définition des règles liées à la gestion des secrets

## Decision

 * Les secrets ne doivent pas être stockés dans le code source d'une application. 
 * Les secrets doivent être stockés dans un emplacement centralisé pour améliorer la sécurité et faciliter la gestion des secrets dans un environnement Cloud Native.


##  Consequences

Le pattern d'architecture sur la centralisation de la gestion des secrets impose des adaptations nécessaires pour une application :
 * L'accès aux secrets impose une modification du code de l'application existante ou une construction différente :  les applications doivent être configurés pour accéder aux secrets stockés dans le gestionnaire de secrets plutôt que de stocker les secrets eux-mêmes.
 * Les politiques de sécurité doivent être mises en oeuvre pour réglementer l'accès aux secrets, mettre en œuvre une surveillance des activités humaines et organiser une modification régulière de chaque secret.
 * Mettre en place des mécanismes de cache et d'optimisation des performances pour les applications qui sollicitent beaucoup le gestionnaire de secrets
 * S'assurer de la disponibilité du gestionnaire de secrets centralisé : la solution est donc critique, elle doit être gérée comme telle (architecture résiliente)
