# Pattern Suivi des exceptions

Date : xx/xx/2022

## Statut

    Brouillon

##  Contexte

Définition d'un pattern d'architecture de suivi des exceptions.

## Decision

Lorsqu'une exception est enregistrée par un service, il est important d'en identifier la cause. 
Les exceptions indiquent un problème ou une erreur de programmation. 
Les journaux sont traditionnellement utilisés pour visualiser les exceptions, mais ceux-ci admettent des limites (pas l'ensemble du contexte d'un evenement signalé, pas de suivi simple de la résolution, pas de dédoublonnage automatique, ...)
    
Les services de suivi des exceptions constituent une meilleure approche. Les services signalent les exceptions à un service centralisé, qui dédouble les exceptions, génère des alertes et gère la gestion des exceptions.

##  Consequences

__
