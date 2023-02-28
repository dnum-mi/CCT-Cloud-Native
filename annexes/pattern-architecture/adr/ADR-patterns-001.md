# pattern cloud native n-tiers et base de données mono noeud

Date : 12/07/2022

## Statut

    Accepté

##  Contexte

Définition d'un pattern d'architecture cloud native n-tiers avec un *frontend*, un *backend* et une base de données. La base de données n'est pas définie comme hautement disponible.

## Decision

Tous les services métiers sont accessibles via un reverse proxy applicatif. Chaque pod n'est accessible que via un service kubernetes.
La gestion des secrets doit être faites pour chaque tiers applicatif, chaque container. Aucun secret n'est stocké en dur dans chaque container.

##  Consequences

La base de données n'est pas hautement disponible dans ce cas de figure.

