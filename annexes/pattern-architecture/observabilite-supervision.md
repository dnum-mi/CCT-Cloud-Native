# L'observabilité et la supervision

- [L'observabilité et la supervision](#lobservabilité-et-la-supervision)
  - [Contexte <a class="anchor" id="contexte"></a>](#contexte-)
    - [Le pattern d'observabilité <a class="anchor" id="patternobservablite"></a>](#le-pattern-dobservabilité-)
  - [Impact sur les applications au MI <a class="anchor" id="impactSurApplications"></a>](#impact-sur-les-applications-au-mi-)
    - [Les offres et solutions <a class="anchor" id="offreDNUMObservabilite"></a>](#les-offres-et-solutions-)

## Contexte <a class="anchor" id="contexte"></a>

Dans le monde de L'Informatique et de la digitalisation des processus d'entreprise, la supervision des systèmes opérants a toujours été un enjeu majeur pour la pérénnisation des services dans la durée.
Cet élément essentiel se base sur une organisation, en haute disponibilité, et un ensemble d'outils de collecte, d'analyse et de moyens d'actions.

### Le pattern d'observabilité <a class="anchor" id="patternobservablite"></a>

L'observabilité est le sur-ensemble de la supervision.

<img src="../../assets/img/observabilité_schema1.jpg" width="50%" heigth="50%">


En plus de fournir un aperçu approfondi des modes de défaillance implicites, elle offre une vue d'ensemble de haut niveau de la santé du système surveillé. De plus, un système observable fournit un contexte ample sur son fonctionnement interne, permettant la découverte de problèmes systémiques plus profonds.

Pour tout service déployé, les attentes sont les suivantes :

- le suivi fonctionnel de son comportement, sa performance vis a vis des enjeux metier
- le suivi technique de son comportement, ses délais de réponse, l'utilisation des ressources techniques, etc...
- la remontée d'alerte en cas de défaillance du service, d'origine comportementale ou d'origine materielle, voir en survenance pour anticiper les pannes potentielles (ex. saturation des espaces de stockage)
- l'auditabilité du système, en cas de nécessité de justification d'un comportement non attendu

Pour tout service mis en oeuvre et opéré, il est nécessaire d'appliquer plusieurs patterns qui faciliteront la gestion et le dépannage des services. Les patterns suivants peuvent nous aider à concevoir des services observables :

<img src="../../assets/img/observabilité_schema2GlobalPattern.jpg" width="50%" heigth="50%"> 


- [**Health Check API**](adr/ADR-pattern-API-HealthCheck.md): mise en place une API de contrôle de l'état de santé du service.
- [**L'aggrégation de journaux**](./adr/ADR-pattern-aggregation-journaux.md) : la centralisation des logs pour en simplifier l'accès et la recherche.
- [**Traçage en environnements distribués**](./adr/ADR-pattern-trace-env-distrib.md) : l'Identification des demandes entrantes, des éléments transmis et les sollicitations de systèmes tiers par un identifiant unique afin de suivre leur circulation entre les systèmes.
- [**La collecte des exception**](./adr/ADR-pattern-suivi-exceptions.md) : Les exceptions (incidents, alertes, ...) doivent être remontées à un service de suivi des exceptions qui les dédouble, alerte les équipes responsables et suit leur résolution.
- [**La collecte des métriques applicatifs**](./adr/ADR-pattern-suivi-metrique-applicatif.md) : Les métriques telles que les Valeurs de comptage et les valeurs seuil sont fournis par les services, centralisés et exposées sur des tableaux de bord de métriques.
- [**Journaux auditables**](./adr/ADR-pattern-journaux-auditables.md) : les evenements et les actions des utilisateurs, ainsi que le contexte de l'application sont à sauvegarder afin d'en permettre l'accès et le rejeu.

## Impact sur les applications au MI <a class="anchor" id="impactSurApplications"></a>

### Les offres et solutions <a class="anchor" id="offreDNUMObservabilite"></a>
