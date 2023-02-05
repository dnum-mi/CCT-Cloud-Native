
# Référentiel d’exigences applicables au cadre de cohérence Cloud Pi Native

Note: le terme développeur est générique et fait référence à l’individu ou l’organisation pluridisciplinaire qui est chargée de produire et maintenir :  la base de code, le corpus de tests et les fichiers de description d’infrastructure et les documentation technique et usager.

Il est responsable de l'adéquation et de la qualité de la solution au besoin des usagers en collaborant de manières étendues avec les autres acteurs impliqués.


<table>
  <tr>
   <td><strong>ID</strong>
   </td>
   <td><strong>Type</strong>
   </td>
   <td><strong>Exigence</strong>
   </td>
   <td><strong>Nature</strong>
   </td>
   <td><strong>Catégorisation</strong>
   </td>
  </tr>
  <tr>
   <td>EX1
   </td>
   <td><strong>I</strong>
   </td>
   <td>Respect des standards et des normes applicables industrielles, européennes et étatiques, pour la conception de solutions numériques hébergées dans le cloud native (kubernetes), Design Système de l’État, RGAA, RGS, RGI, doctrine Cloud au centre.
   </td>
   <td>Ministériel
   </td>
   <td>Autres normes et standards
   </td>
  </tr>
  <tr>
   <td>EX2
   </td>
   <td><strong>P</strong>
   </td>
   <td>Principe de non déviance et de non fragmentation des normes. Les éventuelles instructions de niveaux inférieurs ne peuvent prévaloir sur les présentes exigences.
   </td>
   <td>Ministériel
   </td>
   <td>Autres normes et standards
   </td>
  </tr>
  <tr>
   <td>EX3
   </td>
   <td><strong>P</strong>
   </td>
   <td>Dans le cadre d’un appel d’offre en cas d’incohérence entre les documents, le cct et la liste des exigences sont supérieurs. Le lecteur est invité à vérifier s’il dispose de la version la plus à jour.
   </td>
   <td>Ministériel
   </td>
   <td>Autres normes et standards
   </td>
  </tr>
  <tr>
   <td>EX4
   </td>
   <td><strong>P</strong>
   </td>
   <td>Conformité au modèle de responsabilité Cloud Pi Native. Les développeurs/concepteurs sont responsables de la partie développement, du maintien en continu d’une qualité constante de la solution, l’absence de défaut de sécurité et de correction avant toute mise en production.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX5
   </td>
   <td><strong>P</strong>
   </td>
   <td>Intégration technique de l’usine logicielle à la chaîne De SecOps, maintien par le développeur en condition de disponibilité et de sécurité du point de vérité du logiciel et code d’infrastructure. Exigence limitée à la durée du marché pour un opérateur économique, mais permanent pour la direction d’application.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX6
   </td>
   <td><strong>I</strong>
   </td>
   <td>Conformité au modèle de responsabilité “you built it - you run it”
<p>
Les développeurs/concepteurs sont responsables du bon fonctionnement de l’application en production. ( il collabore avec l’hébergeur le cas échéant)
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX7
   </td>
   <td><strong>P</strong>
   </td>
   <td>L’orchestration de la sauvegarde est de la responsabilité de l’application
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX8
   </td>
   <td><strong>I</strong>
   </td>
   <td>L’équipe projet teste régulièrement sa capacité à restaurer l’ensemble de l’architecture et des données de l’application avec un scénario de test connu à l’avance
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX9
   </td>
   <td><strong>I</strong>
   </td>
   <td>Couverture fonctionnelle des tests du front end permet de s’assurer de non-régression majeure. (exigence à affiner)
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX10
   </td>
   <td><strong>I</strong>
   </td>
   <td>La couverture fonctionnelle des tests unitaires du back end est de 100%
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX11
   </td>
   <td>I
   </td>
   <td>Le développeur, usagers de la chaîne de livraison logicielle, signale les éventuels défauts ou besoin d’évolution, il soumet le cas échéant une rectification ou une évolution sur le dépôt de code après l’avoir testé.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX12
   </td>
   <td>P
   </td>
   <td>Mise en place organisationnelle et technique de modalité de collaboration étendue continue intégrant le flux d’erreur de la chaîne de DevSecOps Ministérielle. («  shift-lent »)
<p>
Exigence limitée à la durée du marché pour un opérateur économique, mais permanente pour la direction d’application.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX13
   </td>
   <td>P
   </td>
   <td>Conformité au modèle de responsabilité Cloud Pi Native L'opérateur de la chaîne CI/CD est responsable du build, de l'exécution des tests fournis et du déploiement de l'application
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX14
   </td>
   <td>P
   </td>
   <td>Le développeur prend en compte qu’aucune modification n’est effectuée directement en production. Il n’accède pas à l’API kubectl.
<p>
Toute modification en production doit être effectuée via un versionning du point de vérité GitOps
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX15
   </td>
   <td>P
   </td>
   <td>L'ensemble des éléments permettant de compilers / builder, tester et exécuter l'application ainsi que déployer l'infrastructure et ouvrir les flux réseaux doivent être fournis par le Développeur / Concepteur à l'opérateur de la chaîne CI/CD
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX16
   </td>
   <td>I
   </td>
   <td>Intégration technique de l’usine logicielle à la chaine DevSecOps, maintien par le développeur en condition de disponibilité et de sécurité du point de vérité du logiciel et code d’infrastructure et du WebHook ”shift-left”  par l’équipe de développement tout au long du contrat.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX17
   </td>
   <td>I
   </td>
   <td>L’agilité (à l’échelle) en tant que cadre de travail privilégié et mise en place d’un principe de livraison continue par lot de taille réduite.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX18
   </td>
   <td>P
   </td>
   <td>Mise en place d’un principe de collaboration étendue, continue et intégré des processus de livraisons, adéquation de la solution au besoin via l’observabilité, maintien de la qualité, de la disponibilité  et de sécurité depuis le développement juste qu’à la production
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX19
   </td>
   <td>P
   </td>
   <td>La disponibilité cible de l’application est de la responsabilité de la direction d’application qui définit l’architecture technique et organisationnelle en s’appuyant sur les services de l’opérateur et la disponibilité visée
   </td>
   <td>Ministériel
   </td>
   <td>Infrastructure
   </td>
  </tr>
  <tr>
   <td>EX20
   </td>
   <td>I
   </td>
   <td>Formation et de maintien réguliers des compétences des personnels à la technologie Cloud Native (kubernetes), l’agilité et au devsecops, intégration et contribution à la communauté de pratiques Cloud (pi) Native.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX21
   </td>
   <td>I
   </td>
   <td>Remontée des défauts, contribution à l’enrichissement de la chaîne DevSecOps et l’offre Cloud Native.
   </td>
   <td>Ministériel
   </td>
   <td>Modèle d'Opération
   </td>
  </tr>
  <tr>
   <td>EX22
   </td>
   <td><strong>P</strong>
   </td>
   <td>Le code applicatif doit être testé avant d'être soumis à la chaîne CI/CD du ministère(fonctionnellement, techniquement et sécurité)
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX23
   </td>
   <td><strong>P</strong>
   </td>
   <td>L’ensemble des logs techniques, fonctionnels et de sécurité doivent obligatoirement être centralisés en utilisant les patterns d'observabilité recommandés. Cela concerne les login d’utilisateur et de de consommation des API.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX24
   </td>
   <td><strong>P</strong>
   </td>
   <td>Le concepteur/développeur est libre d'utiliser le langage de programmation de son choix issu de la liste des langages autorisés. ( principaux langages )
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX25
   </td>
   <td><strong>P</strong>
   </td>
   <td>L’application doit pouvoir être monitorable techniquement et fonctionnellement (dont healthcheck) au travers du service de télémétrie mis à disposition
<p>
Mise à disposition obligatoire au sein de la solution des API de supervision auto descriptive /health  (json+problem) et /metrics (prométheus) et Intégration obligatoire de la solution dans la (ou les) chaîne(s) de supervision
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX26
   </td>
   <td>I
   </td>
   <td>Respect du guide d'éco-conception. La conception frugale vis à vis des ressources d’infrastructures consommées et l'impact vis-à-vis du terminal de la solution.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX27
   </td>
   <td>I
   </td>
   <td>Le back-end la couverture des tests unitaires est 100% code sur et xx sur le front end les défauts éventuels rencontrés lors de l’usage sont implémentés sous la forme de test et capitalisés dans la base de cas de tests avant l’écriture d’un correctif.
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX28
   </td>
   <td><strong>P</strong>
   </td>
   <td>Les pods “stateless” doivent pouvoir être redémarrés à tout instant sans perte de sessions, données ou de transactions.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX29
   </td>
   <td><strong>P</strong>
   </td>
   <td>Les  sources d’OS servant à la constitution de images de l’application proviennent exclusivement de souche os ayant un support long terme (LTS)  maîtrisé par un processus organisationnel à révision contrôlé.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX30
   </td>
   <td>I
   </td>
   <td>Utilisation privilégiée de composants open-source et avec une communauté active
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX31
   </td>
   <td>I
   </td>
   <td>L’architecture de la solution est modulaire, le couplage organisationnel et technique est lâche entre les composants (ex APi)., les services de haut niveau ne dépendent pas de l’interface offerte de composants de niveau inférieur ( dépendance inversion principe)
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX32
   </td>
   <td>P
   </td>
   <td>Les conteneurs s'exécutent sans requérir à l’utilisateur root et les ports réseaux internes sont > 1024. ( l’exécution de conteneur non rootless est bloquée en production )
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX33
   </td>
   <td>I
   </td>
   <td>Le point de présence et de vérité de la sauvegarde est assuré par un service de type S3 indépendant et résilient de l’architecte de production dont le Concepteur/Développeur s’assure régulièrement de sa capacité à restaurer.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX34
   </td>
   <td>P
   </td>
   <td>La compilation et la certification des images est effectuée au sein de l’orchestrateur DevSecOps ministériel. Le développeur s’organise autour de cette contrainte.
   </td>
   <td>Ministériel
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX35
   </td>
   <td>P
   </td>
   <td>Choix d’un hébergement adapté à la nature de la donnée manipulée et selon le cadre légal adapté. (Cloud public, Cloud Régalien référencé par la doctrine Cloud au centre, Dédié)
   </td>
   <td>Ministériel
   </td>
   <td>Infrastructure
   </td>
  </tr>
  <tr>
   <td>EX36
   </td>
   <td>I
   </td>
   <td>Les services applicatifs d'observabilité (logs et télémétrie), registre d'image et gestion des secrets mis à disposition doivent être utilisés.
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX37
   </td>
   <td>I
   </td>
   <td>Consommation systématique des données de référence ministérielles
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX38
   </td>
   <td>I
   </td>
   <td>Référencement des objets Métiers dans le catalogue des données Métier du MI
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX39
   </td>
   <td>P
   </td>
   <td>Les services applicatifs mis à disposition ne doivent pas être remplacés par un équivalent
<p>
Consommation systématique des services socles à enrollment automatisés : IAM, service d’échange (ident/authent, preuve probante/non-répudiation, exposition de services, référentiels, pfs SIG, ...)
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX40
   </td>
   <td>I
   </td>
   <td>Le service de stockage objet doit systématiquement être utilisés pour les sauvegardes
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX41
   </td>
   <td>P
   </td>
   <td>Le bastion doit systématiquement être utilisé pour les accès applicatifs d'administration
   </td>
   <td>Ministériel
   </td>
   <td>Services Mutualisés
   </td>
  </tr>
  <tr>
   <td>EX42
   </td>
   <td>I
   </td>
   <td>L’application minimise le besoin d’échange synchrone, les échanges asynchrones sont réalisés via un bus de message.
   </td>
   <td>Ministériel
   </td>
   <td>Intéractions & Flux
   </td>
  </tr>
  <tr>
   <td>EX43
   </td>
   <td>
   </td>
   <td>Séparation des flux usagers, de services et d’administration, utilisation privilégiée du protocole http
   </td>
   <td>Ministériel
   </td>
   <td>Intéractions & Flux
   </td>
  </tr>
  <tr>
   <td>EX44
   </td>
   <td>I
   </td>
   <td>Toute API exposée doit l'être via le service API management mis à disposition qui identifie + authentifie les consommateurs. L’application met en place la traçabilité en s’appuyant sur la solution d’observabilité disponible.
   </td>
   <td>Ministériel
   </td>
   <td>Intéractions & Flux
   </td>
  </tr>
  <tr>
   <td>EX45
   </td>
   <td>I
   </td>
   <td>Les objets et données métiers doivent systématiquement être exposés via le service d'API management fourni.
<p>
Enrollement automatisé des objets métiers via API ( restful, GraphQL,gRPC) sur les passerelles API Cloud Native. La direction de programme fournit une description de son api et précise les conditions d’accès:
<p>
La direction de programme fournit un kit de proxification de l’APi de son service avec une donnée libre d’usage (Ex: Données anonymisees )  permettant de dérouler des cas de tests significatifs. Le kit livré est déployable sous la forme d’un micro-service déployable dans Kubernetes via chart Helm qui est inscrit au catalogue du mi.. (Voir les exemples de service d’accélération)
   </td>
   <td>Ministériel
   </td>
   <td>Intéractions & Flux
   </td>
  </tr>
  <tr>
   <td>EX46
   </td>
   <td><strong>P</strong>
   </td>
   <td>L’application est responsable de fournir un fichier de description (ex: open api  / swagger ) qui respecte les standards, préalablement à l’enrôlement en production l’application une vérification est effectuée et l’application doit corriger les défauts.
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX47
   </td>
   <td><strong>P</strong>
   </td>
   <td>Utilisation de la variabilisation des configuration d’environnement, des services de support (bdd, cache distribué,..), service externe, connectivités.. .la configuration de l’application ne doit jamais être codé en dur (Principe de Configuration)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX48
   </td>
   <td>I
   </td>
   <td>Maximiser l'accès aux Services tiers et locaux au travers de chaînes de connexion standard (non spécifique au fournisseur de solutions pour favoriser les changements de Service sans impact utilisateur (Principe de d’architecture BackEnd)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX49
   </td>
   <td>P
   </td>
   <td>L'application s'exécute sans état (Stateless). Ses processus/microservices sont indépendants les uns des autres. Les états sont stockés dans un magasin de données centralisé. Cela pour garantir un mise à l'échelle et continuité de service de l’application (Principe Stateless)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX50
   </td>
   <td>P
   </td>
   <td>Garantir l’idempotence des transactions en cas d'arrêt progressif des services (SIGTERM).
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX51
   </td>
   <td>I
   </td>
   <td>S’efforcer de minimiser le temps de démarrage du processus/service en limitant l’environnement au juste nécessaire. (principe Jetable)
   </td>
   <td>CloudNative
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>EX52
   </td>
   <td>I
   </td>
   <td>L’application est prévue pour un déploiement en continu, la conception du modèle de données permet à la version future et l’actuelle de coexister sans impact fonctionnel.
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX53
   </td>
   <td>I
   </td>
   <td>L’ensemble des services applicatifs/processus de l’application, et ses services de supports génèrent leurs propres flux d'événement bruts pour apporter une visibilité sur son comportement. La norme de nommage des fluxs d'événement est, sans condition, respectée. (Principe d’observabilité)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX54
   </td>
   <td><strong>P</strong>
   </td>
   <td>Toutes applications mise en ligne doit fournir une API clairement définie et documentée, pour faciliter sa consommation future des contrats d’interface (Principe de Api first)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX55
   </td>
   <td><strong>P</strong>
   </td>
   <td>La performance de toutes les transactions réalisées par l’application doit être mesurable en temps réel pour contrôler la qualité de services et soutenir les investigations en cas de dysfonctionnement. Il est préconisé d’assurer la surveillance de l’application à minima au travers de : Flux d'événement de performance applicative, flux d'événement et donnée pour analyse et reporting métier, journaux d’intégrité et du système (Principe de Télémétrie)
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX56
   </td>
   <td><strong>P</strong>
   </td>
   <td>Identification utilisateur : L’application doit obligatoirement utiliser le SSO Agent disponible et/ou France connect pour les citoyens
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
  <tr>
   <td>EX57
   </td>
   <td><strong>P</strong>
   </td>
   <td>Pour la persistance de données personnelles soumises au RGPD, le modèle de données intègre dès la conception, un tag RGPD, des champs dupliqués dédiés à l’anonymisation et des règles et processus d’anonymisation ainsi qu’une politique de droits associés.
   </td>
   <td>CloudNative
   </td>
   <td>Code Applicatif & Image
   </td>
  </tr>
</table>
