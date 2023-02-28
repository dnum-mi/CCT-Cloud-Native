### Pattern aggrégation de journaux

Date : xx/xx/2022

#### Statut

    Proposition

####  Contexte

Définition d'un pattern d'architecture de regroupement de logs.

#### Decision

Le dépannage peut être facilité par les logs. Les fichiers de logs sont un bon point de départ si vous voulez déterminer ce qui ne va pas dans votre application. La journalisation dans une architecture complexe peut s'avérer difficile car la journalisation est réalisée de manière dispersées  dans les différents services.
    
Le regroupement des logs est la solution. Les pipelines d'agrégation de journaux envoient ceux de toutes les instances de services à un serveur de journalisation centralisé. 
    
Lorsque les logs sont stockés dans le serveur de journalisation, ils peuvent être visualisés, recherchés et analysés. Vous pouvez également configurer des alertes qui sont déclenchées lorsque certains messages apparaissent dans les journaux.
    
L'infrastructure de journalisation est chargée d'agréger les journaux, de les stocker et de les rendre consultables.

####  Consequences

__
