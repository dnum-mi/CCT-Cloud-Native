![alt_text](images/image1.png "image_tooltip") 

```
Cadre de Cohérence Technique (CCT)

Volet  : Cloud π Native  à portée interministérielle

Version : Pour appel à commentaire initial
Date : 05/12/2022
Auteur : Direction du numérique Ministère de l’Intérieur
``````
![alt_text](images/image2.png "image_tooltip")![alt_text](images/image4.png "image_tooltip")

##

Cette version RFC (request for comment) vous permet de proposer vos commentaires de plusieurs manières: 

- faire des Pulls request sur le repository
- faire des issues
- utiliser le fichier de relecture proposé 
[Fichier pour commentaires ](https://github.com/dnum-mi/CCT-Cloud-Native/blob/main/gabarit-pour-commentaires.ods)
 et l’envoyer à : dnum-architecture-entreprise@interieur.gouv.fr

##

# CCT-Cloud-Native, Introduction.

Le présent volet, du cadre de cohérence technique Cloud Pi Native, concerne la conception et l’hébergement d’applications s’exécutant côté serveur. Une offre de service à portée interministérielle conforme et soutenant ce cadre est mise à disposition des développeurs.

Cette offre s'appuie sur l’opportunité technologique d’orchestration native de conteneurs Kubernetes, couplée à une double chaîne de livraison logicielle en continu dite DevSecOps :  primaire (pour le développeur) et secondaire (pour l'homologation en continue et la dépolution ).
Cet ensemble s'inscrit dans le cadre de la doctrine Cloud au centre de l’État.

La conformité à ce cadre est fortement recommandée. Le respect de ce cadre permet à la direction d’application l’usage du socle de déploiement et de sécurité Cloud Pi Native. Ce dernier accélère la livraison d’applications de qualité qui répondent au besoin.

Des dérogations à ce cadre, dûment justifiées, sont étudiées en comité de gouvernance ad-hoc. Les applications peuvent contribuer via un échange préalable, aux fonctionnalités de l’offre directement via un processus d’intégration en continu.

Ce cadre, ainsi que l’offre de services mis à disposition, permet de :

- guider les concepteurs d’applications afin d’optimiser les architecture produites selon les normes industrielles, les meilleures pratiques DevSecOps et Cloud ;
- réaliser et maintenir des applications avec une efficience des ressources consommées ( financière, RH, énergétique) ;
- soutenir, en continu, la qualité et la sécurité des solutions ;
- normaliser et optimiser l’usage nominal de l’offre ;
- autonomiser les clients dans leur usage des services de l’offre ;
- maintenir un niveau de compatibilité minimal avec d’autres offres cloud ;
- soutenir l’accès à des ressources d’infrastructures utilisables en quelques jours ;
- fluidifier et sécuriser le déploiement en continu, soutenant l’agilité et permettant de réduire la distance entre le fonctionnel proposé et les attentes des usagers;
- mettre en place un modèle de responsabilité et de collaboration étendu ;
- disposer d’une trajectoire soutenable pour ceux en charge de maintenir l’offre.

Ce cadre se décline sur les configurations suivantes :

- l’hébergement d’applications sur les infrastructures internes infogérées par le ministère de l’intérieur ;
- l’hébergement d’applications sur des infrastructures cloud externes ;
- l’hébergement d’applications sur des infrastructures Ministérielles dédiées et gérées par l’application.
- Le cadre de cohérence technique est découpé en 2 parties applicables
- ce document qui présente et explique le présent cadre et les spécificités de l’offre ;
- le référentiel d’exigences techniques, organisationnelles et administratives.

Le lecteur pressé peut aller directement à la revue des exigences qui sont de 2 natures : 
- Primordiales, ces exigences sont obligatoires, le non-respect peut entraîner une exclusion administrative dans le cadre d’un marché public 
- Importantes ce sont des exigences recommandées pour maximiser la performance de la conception et du contexte d’organisation avec le bon usage de kubernetes.

La direction d’application devra valider les conditions générales d’usage de l’offre (CGU) Cloud Pi Native lors de la souscription. Les CGUs reprennent les exigences qui ont été déclinées au sein de l’offre. Le lecteur est invité à vérifier qu’il dispose de la dernière version de ce document ainsi que de la liste d’exigences.

Les  différents documents qui constituent le cadre de cohérence technique  :
- [Lien vers le corps descriptif du CCT ](https://github.com/dnum-mi/CCT-Cloud-Native/blob/main/cct-cloud-native.md)
- [Lien vers la liste des exigences associées au CCT ](https://github.com/dnum-mi/CCT-Cloud-Native/blob/main/cct-exigences.md)
- [Lien vers le glossaire](https://github.com/dnum-mi/CCT-Cloud-Native/blob/main/cct-glossaire.md)
