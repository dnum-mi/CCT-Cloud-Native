### Pattern Health Check API

Date : xx/xx/2022

#### Statut

    Proposition

####  Contexte

Définition d'un pattern d'architecture de contrôle de l'état de santé d'un service (API Health Check).

#### Decision

** Problèmes : ** 
Il peut arriver qu'un service soit en cours d'exécution mais incapable de traiter les demandes. Une instance de service nouvellement démarrée peut être en train de s'initialiser et d'effectuer quelques vérifications avant de pouvoir traiter les demandes.
    
** Comportement attendu : **
Il n'est pas logique que l'infrastructure de déploiement achemine les demandes HTTP vers une instance de service avant qu'elle ne soit prête à les traiter.

** Problèmes :**
Il peut également arriver que l'instance de service échoue sans se terminer, par exemple, toutes les connexions à la base de données sont utilisées et il est impossible d'accéder à la base de données. 
    
** Comportement attendu : **
L'infrastructure de déploiement ne doit pas acheminer les demandes vers une instance de service qui a échoué et qui est toujours en cours d'exécution ; si l'instance de service ne parvient pas à se rétablir, elle doit être arrêtée et une nouvelle instance doit être créée. Une instance de service doit être capable d'indiquer à l'infrastructure de déploiement si elle est en mesure de traiter les demandes ou non.

En synthèse, le service doit possèder une API HealthCheck qui renverra l'état de santé du service. Le gestionnaire du endPoint de l'API effectue divers contrôles, tels que :
* l'état des connexions aux services d'infrastructure utilisés par l'instance de service
* l'état de l'infrastructure hôte, par exemple l'espace disque
* la logique propre à l'application.
     
Un element de contrôle (health check client, outil de monitoring, service regisrty ou load Balancer) invoque périodiquement le endPoint pour vérifier l'état de santé de l'instance de service.

####  Consequences

__
