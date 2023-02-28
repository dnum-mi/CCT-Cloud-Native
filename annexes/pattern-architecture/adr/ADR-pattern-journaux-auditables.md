#### Pattern Journaux auditables

Date : xx/xx/2022

#### Statut

    Proposition

####  Contexte

    Définition d'un pattern d'architecture sur l'auditabilité des journaux.

#### Decision

Les actions de chaque utilisateur sont enregistrées par les journaux d'audit. En général, les journaux d'audit sont utilisés pour fournir un support client, assurer la conformité et détecter les activités suspectes. Une entrée du journal d'audit enregistre l'identité de l'utilisateur, l'action qu'il a effectuée et l'objet de gestion concerné. Le journal d'audit est généralement stocké dans une table de base de données.

La journalisation de l'audit peut être mise en œuvre de plusieurs manières différentes :
* Ajouter un code de journalisation d'audit à la logique métier : Chaque méthode de service peut créer une entrée de journal d'audit et l'enregistrer dans la base de données.
* Programmation orientée aspect (Aspect-oriented programming) : il s'agit de définir un mecanisme qui intercepte chaque appel de méthode de service et fait persister une entrée de journal d'audit en utilisant un framework AOP.
* Utilisation du sourcing par événement (event sourcing) : "L'event sourcing" fournit par défaut un journal d'audit pour les opérations de création et de mise à jour.
    
Par définition, les modèles d'observabilité ne concernent pas les journaux, les mesures ou les traces, mais plutôt le fait d'être guidé par les données pendant le débogage et d'utiliser le retour d'information pour itérer et améliorer le produit.

####  Consequences
