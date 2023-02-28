#### Pattern Suivi des métriques applicatifs

Date : xx/xx/2022

#### Statut

    Proposition

####  Contexte

Définition d'un pattern d'architecture de suivi des métriques applicatifs.

#### Decision

La supervision des comportements et des alertes sont des éléments clés de l'environnement de production. Les systèmes de surveillance rassemblent des mesures qui fournissent des informations essentielles sur la santé d'une application à partir de toutes les parties de sa pile technologique. Ces mesures vont des mesures faites au niveau de l'infrastructure (utilisation du processeur, de la mémoire et du disque) aux mesures faites au niveau de l'application (temps de latence des demandes de service, nombre de demandes traitées, ...)
    
Les métriques relèvent de la responsabilité du développeur de services de deux manières. Il doit d'abord instrumenter son service pour collecter des mesures sur son comportement. Ensuite, il doit exposer ces mesures liées au service, ainsi que celles du cadre d'application, au serveur de surveillance et de generation des alertes. Ce serveur interroge les endPoints pour récupérer les métriques. Un outil de visualisation des données peut être utilisé pour afficher les métriques à la demande. 
    
Le couple logiciel actuellement utilisé pour collecter les metriques et pour les visualiser au sein de la DNUM sont Prometheus et Grafana.  

####  Consequences

__
