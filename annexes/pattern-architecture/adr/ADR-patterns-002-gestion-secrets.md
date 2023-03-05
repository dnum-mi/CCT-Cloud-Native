# Pattern Gestion des secrets

Date : 15/02/2023

## Statut

Proposée

##  Contexte

Durant la periode de construction de l'offre Cloud Pi Native et de sa chaine devSecops, des questions se sont posées concernant les bonnes pratiques de gestion des secrets pour les applications qui utilisent l'offre et mettent en oeuvre la démarche.

## Decision

Des éléments importants sont à appliquer :
 * Les secrets ne doivent pas être stockés dans le code source d'une application. 
 * Les secrets doivent être stockés dans un emplacement centralisé pour améliorer la sécurité et faciliter la gestion des secrets dans un environnement Cloud Native.


##  Consequences


Le pattern d'architecture sur la centralisation de la gestion des secrets est avantageux mais impose des adaptations pour une application, mais aussi des nécessités vis à vis du service gestionnaire :
 * L'accès aux secrets impose une modification du code de l'application existante ou une construction différente :  les applications doivent être configurés pour accéder aux secrets stockés dans le gestionnaire de secrets plutôt que de stocker les secrets eux-mêmes.
 * Les politiques de sécurité doivent être mises en oeuvre pour réglementer l'accès aux secrets, mettre en œuvre une surveillance des activités humaines et organiser une modification régulière de chaque secret.
 * Mettre en place des mécanismes de cache et d'optimisation des performances pour les applications qui sollicitent beaucoup le gestionnaire de secrets
 * S'assurer de la disponibilité du gestionnaire de secrets centralisé : la solution est donc critique, elle doit être gérée comme telle (architecture résiliente)
