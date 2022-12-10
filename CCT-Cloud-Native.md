```
Cadre de Cohérence Technique (CCT)

Volet  : Cloud π Native  à portée interministérielle

Version : Pour appel à commentaire initial
Date : 05/12/2022
Auteur : Direction du numérique Ministère de l’Intérieur
```



# TABLE DES MATIÈRES
</br>1 - Guide d’utilisation rapide
</br>1 - Le contexte, les enjeux, la vision
</br>2 - Principes généraux cadre Cloud Native
</br>  Les configurations d’hébergement prises en compte
</br>  Gestion des non-conformités, dérogations et contribution
</br>  Les normes industrielles, institutionnelles applicables.
</br>  Le modèle organisationnel, de responsabilité et de collaboration Cloud Native
</br>  Préconisations générales d’architecture et technique
</br>  Des spécificités à prendre en compte sur la création des conteneurs
</br>  Des spécificités à prendre en compte sur la topologie réseau et les ouvertures de flux
</br>  Modèle d’intégration d’une application dans le cadre Cloud Native
</br>3 - Présentation de l’offre interMinistérielle Cloud Pi Native
</br>4 - Référentiel d’exigences et modalités d'usage	
</br>5 - Annexes
</br>  Liens vers autres documents et contenus utiles(informatif)
</br> Glossaire
## 
# 1 - Le contexte, les enjeux, la vision 

**Le cloud : des nouvelles possibilités techniques, une collaboration étendue des acteurs pour répondre aux enjeux d’un contexte exigeant, incertain et accéléré.**

À travers sa doctrine « Cloud au centre », l’État encourage l’ensemble des acteurs publics à se saisir de son potentiel afin de développer une nouvelle génération de services numériques de qualité et qui répond au besoin dans un cadre de normes juridiques adapté à l’usage. Cela répond notamment au besoin accru d’agilité et d’efficience de l’administration.

Le Cloud est une approche d’accès à l’infrastructure d’hébergement à travers une interface standardisée et abstraite des technologies sous-jacentes. Cette abstraction permet une automatisation poussée, supprimer les frictions organisationnelles, les non-qualités et lenteurs induites par des opérations manuelles. L’infrastructure est pilotable par du logiciel et donc automatisable avec des processus reproductibles.

 

La technologie Cloud Native fait référence à l’usage de Kubernetes. Kubernetes est une technologie issue des travaux des grands acteurs de l’Internet il y a plus de 15 ans pour rendre encore plus efficace et sécurisée l’usage des infrastructures techniques, la résilience des hébergements et apporter une souplesse organisationnelle accrue.

Les grands services de l’internet s'appuient sur cette technologie pour gérer une demande  extrême. L’ensemble des organisations ayant mis en œuvre cette technologie telle que EDF, Orange, des services de vente en ligne, des Banques, Airbus, Urssaf, etc… ont vu également leurs efficiences de l’usage du numérique augmenter, il y a un _avant et un après_.

Le ministère de l’intérieur, l’un des premiers acteurs étatiques à avoir proposé une offre Cloud il y a plus de 5 ans, étend son offre de service, en proposant l’offre Cloud Pi Native combinant une offre d'hébergement kubernetes sécurisée jusqu’au niveau DR. Cette offre est accompagnée d’un modèle DevSecOps outillé permettant une fluidité organisationnelle accrue et un renforcement de la qualité des solutions numériques.

Pour tirer parti au maximum du cloud, les architectures ont évolué ainsi que les modèles de responsabilité et organisationnel. L’une des problématiques majeures des pratiques du passé était la segmentation des responsabilités entre la construction, la vérification, le déploiement et l’hébergement. Les approches cloud, devops et l’agilité ont progressivement permis de concilier des postures antagonistes : les développeurs ayant besoin de pouvoir déployer fréquemment, et l’exploitation ayant au contraire besoin de stabilité et de diminuer les risques liés au changement. La clé réside dans une collaboration étendue de tous les acteurs en prenant compte de la sécurité à toutes les étapes.



**Une évolution des pratiques pour un numérique efficient et éco-responsable et réactif**

Les contraintes s’accentuent sur la production de services numériques, le standard de qualité général a augmenté massivement avec les acteurs du net et industrielle qui produisent des solutions ergonomiques, sécurisées qui montent à l’échelle facilement. Un fossé important s’est creusé entre l’efficience du numérique ‘legacy’ et ce monde moderne. 

L’environnement change rapidement, il devient incertain, il faut réagir de plus en plus rapidement, la pression augmente sur la production de solutions numériques ergonomique, nécessitant des cycles raccourcis, la prise en compte de l’éco responsabilité, de l’accessibilité et le maintien d’un haut standard de qualité et de sécurisation. 

Seul un changement majeur de pratiques s’appuyant sur l’opportunité du Cloud Native ( kubernetes ) et du DevSecOps permettent de satisfaire ce nouveau standard d’exigences.

**<span style="text-decoration:underline;">Les principales caractéristiques du modèle opérationnel Cloud Native:</span>**

** **

Un mode de collaboration étendu, la suppression de la fragmentation des responsabilités et l’automatisation :



* Le développeur (l’équipe) voit ses prérogatives étendues, il est responsabilisé sur la qualité de la solution produite jusqu'à la production, c’est le modèle « You build it you run it ». ( vous l’avez construit vous l’opérez )
* L’hébergeur assure quant à lui, la mise à disposition d’une offre de service hautement disponible et sécurisée. L’usage de l’offre est réalisé via une console, une interface technique normée (API), une documentation et des exemples fonctionnels permettant un démarrage accéléré.

Les clients sont autonomes, l’hébergeur n’échange pas avec la direction d’application. Il n’y a pas de nécessité de réaliser d’opérations manuelles.

L’ensemble des opérations réalisées manuellement auparavant lors des étapes d’élaboration sont complètement automatisées. Le code logiciel est testé en permanence et automatiquement par un outillage : l’orchestrateur DevSecOps. 

Pour assurer la qualité du code, plusieurs principes sont mis en œuvre automatiquement : 



* une couverture de test (100% sur le back-end)
* l’analyse statique du code
* l’analyse récursive de vulnérabilité des composants importés (librairie, images )
* des tests de sécurité et de performances. 

Le développeur est prévenu au plus tôt par l’orchestrateur DevSecOps en cas de non-qualité. Seul un logiciel ayant atteint le niveau de qualité fixé peut être déployé. 

Soutenus par l’outillage, les développeurs assurent continuellement la qualité et la sécurité du code produit, la non-régression et l'absence de vulnérabilité.

Les architectures sont modulaires et les composants internes ainsi que les interfaces entre applications sont découplées, c’est à dire rendus indépendants techniquement et organisationnellement via des interfaces normées (APi). Cela permet la maintenance et les  évolutions indépendantes entre composants. Ce découplage contribue fortement à réduire le coût des changements et faciliter les transitions technologiques en cas d’obsolescence.

La conception de l’architecture, le choix des langages sont faits pour une efficience de l’usage des ressources d’infrastructures et également sur l’impact sur le poste de travail.

La conteneurisation, l'élasticité dynamique de la solution d'orchestration de conteneurs kubernetes, la mutualisation des infrastructures physiques soutiennent fortement cette  efficience.

Le non-respect de ce principe de modularité a été identifié par la direction interministérielle du numérique comme l’une des causes d’échec des grands programmes de l’État.

La modularité, l’indépendance des modules lors du déploiement, permettent de réduire la taille des déploiements ce qui contribue à réduire les risques et fluidifier les mises en production. Les déploiements peuvent ainsi être rendus transparents pour  des usagers et les retours arrière éventuels sont  facilités. Il est ainsi possible de déployer en confiance, plusieurs évolutions par jour si nécessaire.

L’automatisation permet de  mieux contrôler et rendre les actions prédictibles, faciliter la reprise en cas d’incident et minimiser les coûts de maintien en conditions opérationnelles et de sécurité des applications. Plus aucune intervention manuelle n’est effectuée sur les environnements ce qui permet de réduire la variance, les non-qualités, et aussi de (re)construire très rapidement des plateformes.

In fine, la conception doit s’inscrire dans une démarche d’éco-conception et de sobriété numérique des conceptions (green IT)  permettant un usage plus efficient des ressources  qu’elles soient RH, financières. L’État devant être exemplaire. cf guide d’éco-conception.

 


## 


# 2 - Principes généraux cadre Cloud Native 

Le cadre de cohérence technique régule et normalise les différents domaines associés à l’élaboration et au maintien des ressources partagées nécessaires à la mise à disposition de solutions numériques de qualité répondant au besoin. Il s’assure que l’ensemble peut-être mis en œuvre de manière cohérente avec une consommation minimisée des ressources : financière, RH et écologique. Il recommande ou fixe les mesures permettant d’atteindre l’objectif, tout en favorisant l’innovation, la prise en compte de l’obsolescence régulière des technologies et la manœuvre RH nécessaire (formation continue, recrutement …)



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


Figure 1 - Architecture des différents volets du CCT.

Le volet Cloud Native du ministère de l’intérieur, hérite de normes industrielles, interMinistérielles, européennes. La portée est interMinistérielle, ce document a fait l’objet d’échanges avec la direction interMinistérielle du numérique et des ministères primo-accédants.

Pour le ministère de l'intérieur, il encadre la conception et l’hébergement d’applications qu’elles soient hébergées dans les datacenters du ministère ou bien à l’externe sur des clouds public. Ce volet s’applique notamment lors de la conception d’une nouvelle application ou une évolution significative d’une application existante. (cf Doctrine Cloud au centre)

Pour les autres entités étatiques, ce volet sert de présentation de bonnes pratiques et présente les conditions générales d’utilisation de l’offre Cloud Pi Native.

Ce document ainsi que le référentiel d’exigences sont annexés aux dossiers de consultation des entreprises. La portée administrative étant précisée par le règlement de consultation (RC) du marché lui-même, typiquement le RC et le Cadre des clauses administratives particulières (CCAP) peuvent exclure administrativement un candidat en cas de non-respect des exigences P primordiale. (hors dérogation soumise, instruite et accordée).

D’autres référentiels d’exigences ou des guides peuvent être applicables ou conseillés. voir plus loin le chapitre sur les cadres de normes supérieures.

**Offre de service Cloud (π) Native :** 

Concerne la description de l’offre de service managé d’infrastructure Cloud **π** et d’une chaîne DevSecOps assurant l’homologation en continu et le déploiement en production. Cf. présentation de l’offre plus loin dans ce document.

**Poste de travail agent : **

Dans le cadre d’une application rendue accessible sur le poste de travail de l’agent, le lecteur est invité à se conformer également au volet _Environnement Numérique de Travail_, notamment sur les aspects d’intégration au SSO et la politique des navigateurs. 

**Ouverture des données : **

Sur la thématique de l’ouverture et de la circulation de la donnée, le projet est invité à se mettre en conformité avec le volet idoine. Cela concerne notamment le référencement des objets métiers dans le référentiel de cartographie des données et la mise à disposition d’une facilité technique d’accès à la donnée basée sur un standard d’échange de type API. 

L’ensemble des acteurs de l’État est invité à faire circuler la donnée au profit d’une simplification du fonctionnement des administrations et d’un service public ergonomique et proactif .  (cf rapport Bothorel, lois CRPA et 3DS, … )


## Les configurations d’hébergement prises en compte

Les configurations suivantes sont prises en compte par ce volet Cloud Native du CCT.



* Hébergement sur les clusters kubernetes managés par le ministère de l’Intérieur, jusqu’au niveau « donnée restreinte » ;
* Hébergement sur un cluster kubernetes externe au ministère, compatible avec la sensibilité des données manipulées ;
* Hébergement sur un cluster kubernetes dédié et géré par l’application;
* Une approche hybride multi-clusters.

Pour l’ensemble de ces configurations l’usage de la chaîne DevSecOps managée par le Ministère de l’Intérieur est impératif. (hors cadre dérogatoire accordée) 


## Gestion des non-conformités, dérogations et contribution 

L’évolution rapide des technologies cloud peut conduire à ce que le cadre CCT restreigne l’innovation. Il est également souhaité, pour éprouver le modèle, de notifier le département architecture d'entreprise du Ministère de l'intérieur au plus tôt des éventuelles impossibilités ou limitations remarquées. Les directions d’applications ou les organisations utilisatrices peuvent contribuer, via un échange préalable, à enrichir les fonctionnalités de l’offre ou du cadre lui-même. Sur l’offre la contribution est effectuée directement sur le repository open source de la solution via un pull request.

En cas de non-conformité au CCT ou absence de contribution à l’offre, une demande de dérogation dûment motivée sera formulée à l’avance par la direction d’application. Seule la notification de la décision permet d’amender le besoin de conformité au cadre, temporairement ou de manière pérenne dans le cadre d’une dérogation. Dans le cadre d’une dérogation, la direction d’application prend à sa charge le surcoût complet de possession. ( formation, homologation, personnel assurant la tme, etc… ) 

Lors de l’utilisation du cadre et de l’offre Cloud PI Native, toute organisation souhaitant décliner ce cadre dans un document de norme inférieur pour un besoin propre est invitée à référencer la dernière version de ce document en l’état.  Dans la hiérarchie des normes, une instruction de niveau inférieur ne peut entrer en conflit ou contredire ce présent document.


## Les normes industrielles, institutionnelles applicables.

La conception de système d’information dans le cadre de l’État est encadrée par un ensemble de recommandations ou règles à mettre en œuvre.  Ces normes sont citées ci-dessous. Le lecteur est invité à vérifier qu’il dispose des versions les plus à jour.

**Normes industrielles applicables pour cloud native **

**Kubernetes** : [https://kubernetes.io/fr/](https://kubernetes.io/fr/)

**Guides & outils pour la conception**

**DSFR **: Design System FR. La charte internet de l’État ( qui intègre le RGAA )

[https://www.systeme-de-design.gouv.fr/](https://www.systeme-de-design.gouv.fr/)

**Guide d’eco conception** : [https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/](https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/)

**Cadres de pratiques de conception et de conduite de projet agile**

[https://www.numerique.gouv.fr/actualites/guide-pour-allier-agilite-et-securite-numeriques/](https://www.numerique.gouv.fr/actualites/guide-pour-allier-agilite-et-securite-numeriques/)

**SILL **: Socle InterMinistériel des Logiciels Libres, de par sa fonction de source pour le référentiel de produits du CCT Ministériel : [https://sill.etalab.gouv.fr/fr/software](https://sill.etalab.gouv.fr/fr/software)

**Normes interMinistérielles de conception de solutions **

**Doctrine cloud de l’état :<span style="text-decoration:underline;"> [https://www.legifrance.gouv.fr/circulaire/id/45205](https://www.legifrance.gouv.fr/circulaire/id/45205)</span>**

**RGAA **: Référentiel Général d’Accessibilité pour les Administrations 

[https://accessibilite.numerique.gouv.fr/](https://accessibilite.numerique.gouv.fr/)

**RGS **: Référentiel Général de Sécurité, en association avec le règlement européen et l’EIDAS. 

[https://www.ssi.gouv.fr/entreprise/reglementation/confiance-numerique/liste-des-documents-constitutifs-du-rgs-v-2-0/](https://www.ssi.gouv.fr/entreprise/reglementation/confiance-numerique/liste-des-documents-constitutifs-du-rgs-v-2-0/)

[https://www.ssi.gouv.fr/entreprise/reglementation/confiance-numerique/le-reglement-eidas/](https://www.ssi.gouv.fr/entreprise/reglementation/confiance-numerique/le-reglement-eidas/)

**R2GA **: Référentiel Général de Gestion des Archives [https://francearchives.fr/fr/circulaire/R2GA_2013_10](https://francearchives.fr/fr/circulaire/R2GA_2013_10)

**RGPD ** :  règlement européen sur la protection des données personnelles

déclinaison française : [https://www.cnil.fr/fr/reglement-europeen-protection-donnees](https://www.cnil.fr/fr/reglement-europeen-protection-donnees)


## Le modèle organisationnel, de responsabilité et de collaboration Cloud Native

L’architecture, le modèle de responsabilité et d’organisation à mettre en place est orienté pour maximiser la qualité, la sécurité, la fluidité opérationnelle et l’évolutivité du produit en  tirant parti au maximum des possibilités offertes par la technologie kubernetes, un flux de production DevSecOps et une collaboration étendue entre les acteurs. 

**L’élargissement de la responsabilité du développeur**

La responsabilité du développeur est élargie dans le cadre Cloud Native. Il élabore et exploite une solution qui répond au besoin métier généralement une automatisation d’un ou plusieurs processus métiers . Le développeur s'assure de la qualité et de la disponibilité du service rendu à l’usager selon le précepte : « You build it, you run it ». Il s’organise en équipe intégrée, si nécessaire avec de l’externalisation.

Le développeur met à disposition d’un point de vérité du code sous la forme d’un ou plusieurs dépôts de code logiciel fonctionnel et d’infrastructure. Il met en place un flux intégré et continu de production en s'appuyant sur un orchestrateur primaire DevSecOps qu’il construit et opère. 

Le développeur initialise et supervise le pipeline de l’orchestrateur secondaire opéré par le ministère de l’Intérieur (cf plus loin sur la configuration de l’offre Cloud Pi Native). Il intègre les étapes de vérification de sécurité génériques imposées par le minist!re et spécifiques issus de la démarche d’homologation. 

L’ensemble combiné des orchestrateurs primaire et secondaire assure la fonction d’homologation et de déploiement en continu du produit numérique. 

Dans le cas de la détection d’une non-qualité, la progression du déploiement est stoppée par la/les chaînes, le développeur est prévenu en temps réel et doit corriger au plus tôt les défauts remontés. Cette approche permet de garantir un niveau de qualité, évite des régressions et maintient la dette technique au niveau le plus bas.

Sur le plan organisationnel le développeur met généralement en place :



* l’agilité** **avec des itérations courtes de constructions et de vérification des usagers ;
* le découpage des livraisons en lot de taille de réduite ;
* la mise en place d’une culture de collaboration étendue et des pratiques intégrant la sécurité à toutes les étapes.

**<span style="text-decoration:underline;">La répartition des responsabilités s'établit de la manière suivante :</span>**

**Le Concepteur / Développeur :**



* est responsable de l’application, de la qualité du code  et du bon fonctionnement de l’application pendant <span style="text-decoration:underline;">l’ensemble du cycle de vie de l’application. </span>
* est responsable de définir et d’ajuster l’infrastructure et l’élasticité du dimensionnement, nécessaire à son application (sur la base de l’offre Cloud adaptée selon la sensibilité des données) Il s'appuie sur les patterns applicatives validées, les pratiques cloud native sécurisées, l’offre de service des _operators _et charts helm disponibles.
* fourni un code de qualité exempt de défaut d'algorithmes, de qualité et de vulnérabilité.
* met en œuvre le flux de production, logiciel local permettant d’assurer la production et la démonstration d’un code de qualité exempt d’anomalie fonctionnelle, de non-qualité et de vulnérabilité, notamment dans les librairies importées. 
* Il pose les normes de développement des langages utilisés.
* Il met en place un orchestrateur et des pratiques DevSecOps visant un maintien de la qualité dans le temps avec les composantes suivantes :
    * test driven development
    * une couverture de test unitaire à 100% du back-end
    * une couverture significative des tests du front de l’application
    * analyse statique de qualité du code
    * analyse récursive des vulnérabilités des librairies importées
    * utilisation exclusivement d’images sources maintenues en condition de sécurité et certifiées (distribution LTS) ;
    * la conception des tests d’intégration en sandbox.
* Il met en place un hébergement sur une plateforme kubernetes afin d’assurer la démonstration du bon fonctionnement de l’application avec la solution qu’il préfère soit internalisée (avec un moyen de mener des démonstrations) ou sur cloud public. 
* Il met en œuvre l’intégration technique et organisationnelle avec la chaîne DevSecOps de l’offre Cloud Pi Native et initialise le flux logiciel  global (cf plus bas). 
* Il maintient un point de vérité du code logiciel ainsi que celui du code d’infrastructure. Celui-ci est accédé par la chaîne DevSecOps étatique, la sécurisation d’accès issus par token.
* Il est responsable de la surveillance de l’ensemble des pipelines, y compris pour celui géré côté ministère. 
* Il met en place une intégration du flux de retour d’anomalie “shift-left” des orchestrateurs afin de permettre une correction au plus tôt des anomalies.
* Il effectue l’apprentissage comportemental du firewall applicatif Web (WAF) vis-à-vis de l’application dans le cadre fixé par le ministère.
* Il est invité à mettre en œuvre ce pipeline au plus tôt dans le processus de réalisation. 

**L’exploitant Ministériel de l’orchestrateur DevSevOps** :



* Il assure de la disponibilité et de la qualité de fonctionnement de la chaîne DevSecOps et maintient à jour la documentation sur le fonctionnement des interfaces et assure les évolutions fonctionnelles ;
* Il assure les retours d'anomalies "shift-left" lors des opérations de déploiement continu. L'intégration et leurs traitements sont à la charge du Concepteur / développeur ;
* Il contribue à la mise en place et l’évolution du catalogue d’operator Kubernetes, de charts helm et du référentiel de pattern de référence;
* Il est également en lien avec les autorités d’homologation afin de s’assurer que l’ensemble est en condition d’assurer la protection d’ensemble;
* Il intègre les propositions d'évolution “pull request” proposée en fonction de son plan de charge et d’une négociation préalable.

**L’opérateur Cloud** :



* Il assure le maintien en condition de disponibilité et de sécurité de l’offre d’hébergement, l’interface API de management, la console,  la gestion capacité et les offres de services managées.

Des pratiques complémentaires sont introduites dans la configuration Cloud Native :

**Le “GitOps”, **contraction de git et opération, est indispensable à la gestion des applications Cloud Native avec Kubernetes. Ce mode d’organisation du code d'infrastructure permet de maîtriser la description de l’infrastructure de production avec les mêmes pratiques de revue collaborative que celle du logiciel. Il est par exemple strictement interdit de faire des modifications «à la main » sur l’environnement de production, toute variation est supprimée, l’infrastructure réelle est strictement celle décrite par les fichiers d’infrastructure.

Le **“shift-left” **(vers la gauche, du processus) fait référence à la remontée le plus tôt possible vers le développeur des anomalies identifiées par la chaîne de déploiement et de vérification DevSecOps. 

**<span style="text-decoration:underline;">Présentation du cycle d’usage de l’offre pour les directions d’applications:</span>**

**Phase d’initialisation du projet**



* Le développeur initialise l’environnement de développement, il est autonome pour les choix techniques, il respecte les exigences organisationnels et de processus automatisé permettant de maintenir une qualité constante ;
* Le développeur décide de l’infrastructure d’hébergement en fonction des contraintes sur les données (ministère de l’intérieur, cloud externe ou dédié)
* Le développeur commande, (signature de convention), initialise l’espace projet au ministère et configure selon son choix d’infrastructure les environnements désirés. Il récupère les clés techniques nécessaires à l’intégration des pipelines.
* Le développeur effectue l’intégration des pipelines, cf  labels (2) , et (4) si l’infrastructure est externe.
* Il vérifie que l’ensemble du pipeline est opérationnel à partir d’un code d’exemple fourni de type “hello word”.

**Phase de fonctionnement en régime régulier du pipeline ( processus simplifié )**



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")




* _Vision générale du pipeline de construction / déploiement_

Note : le sens des flèches est logique, typiquement pour 4/ 



* **[1]** Le code logiciel ainsi que celui de description des infrastructures est produit au sein de l’espace du développeur/concepteur, généralement externe au Ministère de l’Intérieur.
* **[2]** Le développeur expose le point de vérité du logiciel et de l’infrastructure : aucune modification de code ou d’infrastructure ne sera effectuée plus loin dans la chaîne.
* **[2]** Une interface bi-directionelle entre l’espace du concepteur / développeur et celui de DSO permet dans un sens à DSO de récupérer automatiquement l’ensemble du code et des dépendances nécessaires et dans l’autre sens au Concepteur/développeur d’avoir un retour d’information détaillée sur le succès ou sur une éventuelle erreur lors des tests et lors du build de l’application par DSO.
* **[3]** La chaîne d’orchestration DevSecOps effectue la récupération du code, des tests de qualité du code, scan de vulnérabilité des dépendances, la reconstruction, les tests de nos régressions, des tests d’homologation, vérification des manifests / charts etc… au regard des politiques de sécurité et dépose les images certifiées sur la registry de la chaîne ainsi que le code d’infrastructure. 
* **[3]** : Un point de vérité du code logiciel et infrastructure “homologué” se trouve donc du côté de la chaîne DSO.
* **[4]** : L’infrastructure vient ensuite vérifier les changements et déploie les services sur la/les plateformes cibles. Note :  Le développeur n’accède pas à la production. ( mode “gitops” via argo CD, la console pousse les objets nécessaires,secret, objets utilisé par argo cd )


## Préconisations générales d’architecture et technique

Ce chapitre précise les aspects importants liés à l’usage de kubernetes dans le cadre du ministère de l’intérieur.  Il est attendu que les acteurs soient correctement formés à la solution kubernetes et se maintiennent à jour. La technologie évoluant rapidement. 	

Le fondement des normes techniques est issu du cadre “Cloud Native”, largement accepté et appliqué au sein de l'État et le secteur privé, tel que les “15 factors”. 

C’est le respect de ces normes qui permet à la fois d’adresser les enjeux de performance en termes de vitesse de livraison et de qualité de service, mais aussi de normaliser les applicatifs pour une meilleure évolutivité et maîtrise de la dette technique. Enfin, elles assurent une intégration fluide au sein des systèmes d’informati	on Ministériels.

Un des principes cœurs est de laisser un certain degré de liberté au concepteur/développeur sur le fonctionnement interne de son application. Au contraire, les intéractions avec les autres applications et services seront particulièrement contraintes.

Il est à noter qu’uniquement la plateforme d’orchestration de conteneurs Kubernetes est considérée dans le cadre de ce cadre de cohérence, celle-ci étant considérée comme l’état de l’art, et open-source de surcroît.

À propos de la solution mutualisée d’hébergement Cloud π Native

La solution d’hébergement est basée sur la solution Openshift de l’éditeur Redhat, sa configuration technique et organisationnelle s’appuie sur les recommandations de sécurisation de l’ensemble des acteurs cyber.

Les développeurs n’accèdent pas directement à la plateforme, cet accès s’effectue via une console dédiée et un flux “gitops”. ( via l’usage d’ArgoCD)

Pour information : des tests de compatibilité avec d’autres solutions d’hébergement d’acteurs du cloud public ont été menés avec succès. 


## Des spécificités à prendre en compte sur la création des conteneurs 

Kubernetes impose une rigueur un peu plus élevée à l’initialisation que d’autres solutions.

Les pods (conteneurs) sont **obligatoirement rootless**, c’est à dire que le compte root n’est jamais utilisé pour faire fonctionner le service et ils utilisent uniquement des ports > 1024. 

**Note:** Openshift interdit le lancement de pod utilisant le compte root. Ce point n’est pas modifiable. Ceci est un point d’attention majeur, la quasi-totalité des conteneurs à disposition sur les plateformes de partage de conteneurs ne sont pas rootless.

Les pods doivent démarrer dans leur configuration cible sans état, ou de nécessiter un passage de paramètres de démarrage ou d’environnement.

Les pods doivent démarrer rapidement afin de permettre au mécanisme d’orchestration de fonctionner rapidement. 

Les pods sont responsables de vérifier au lancement, si l’application est dans la condition initiale de 1er lancement, ou bien s’il faut initialiser ou modifier d’autres ressources telles qu’une base de données. 

L’architecture de l’application, hors persistance de données, est conçue pour être complètement stateless, c'est-à-dire, sans aucune persistance de sessions, états et liens, les pods peuvent être basculés à la volée d’un nœud à l’autre sans préavis.


## Des spécificités à prendre en compte sur la topologie réseau et les ouvertures de flux

L’organisation de réseau est segmenté par type de service porté par le flux. Les règles ingress et egress doivent 


## Modèle d’intégration d’une application dans le cadre Cloud Native

Le schéma ci-dessous précise le cadre d’intégration d’une application. Le respect de cadre permet à la direction d’application d’accéder à un socle de sécurité accélérant les homologations, l’ouverture automatique des segments réseau et l’homologation en continu. 


## 

<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")


Le schéma (indicatifs) précise l’architecture d’intégration d’une application est les types de flux: 

(1) Inbound usager : accès à l’application des usagers https / websockets ( depuis RIE ou Internet )

(2a) SSO Citoyens + (2b) SSO AGENT : authentification des usagers ( OIDC / SAML V2 )

(3) Acces objets S3 : accès à la persistance objets de l’application

(4) Echanges inter-applicatifs : permet d’échange entre des applications de porteurs différentes, selon plusieurs modalités possibles : API restful synchrone,  Asynchrone , fichiers

(5) Autres types de flux : autres types d’échange, sortie vers internet, vers d’autres zone d’hébergement, ou entre des zones de sensibilité différentes

(6) échanges entre noeuds de l’application : permet la réplication de l’application entre 2 data centers au même niveau sensibilité de données

(7a) Déploiement des ressources de l’application : gestionnaire & console DEVSECOPS / le pipeline interagit avec le/les clusters kubernetes et les gestionnaires d’infrastructures utilisés ( ouverture de flux réseaux, etc... )

(7b) Artefacts images & paramétrage : ensemble des ressources liées à une application ou communes ( ex : sources d’images de référence )

(7c) Observation : permet de collecter les données liées à l’usage pour la mise au point de l’application ou données de vie.

(8) Kubernetes, sous la forme d’un ou plusieurs namespace(s) isolés ou couplés : fournis l’espace d’exécution de l’application et la gestion des volumes pour le stockage bloc.


# 3 - Présentation de l’offre interMinistérielle Cloud Pi Native

L’offre Cloud PI native DevSecOps répond aux exigences du CCT à travers un ensemble organisationnel et technique. Elle propose une offre Cloud régalienne, souveraineté, sécurisée et isolée de toute problématique juridique.

Les offres d’hébergement compatibles avec les applications « Cloud Native » du ministère de l’intérieur sont :



* Hébergement de l’application sur les infrastructures internes infogérées ;
* Hébergement de l’application sur des infrastructures cloud externes ;
* Hébergement de l’application sur des infrastructures gérées par l’application.

L’ensemble de l’administration technique de la plateforme et des infrastructures est automatique « pilotée » par le développeur/concepteur via l’orchestration DevSecOps.  

Pour rappel, le développeur n’accède pas à l’environnement de production. Toute correction ou évolution devra suivre le processus de déploiement décrit ci-dessus.

Le modèle de responsabilité est présenté ci-dessous:

 

<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")


L’ensemble du code source de l’offre Cloud PI Native et sa documentation sont disponibles en open-source sous la licence MIT. Toute contribution est la bienvenue.


# 


# 4 - Référentiel d’exigences et modalités d'usage

Les exigences du CCT sont classées en 2 niveaux d’exigence (périmètre du Ministère de l’Intérieur) :



* Primordial : L’exigence est impérative et traitée administrativement. 
* I – Important : Exigence prise en compte pour la notation technique de la solution

 

Précisions sur le cas de l’exclusion administrative (périmètre du Ministère de l’Intérieur) :



* La non-conformité au cadre de norme entraîne l’exclusion administrative lors du dépouillement et la mise en œuvre des actions de remédiation du marché lors de l’exécution du marché.
* La non-conformité aux exigences d’architecture entraîne l’impossibilité d’utilisation du socle de sécurité associé à l’offre Cloud Native

Par défaut les règles du CCT s’imposent. Elles peuvent être précisées dans le cas d’un appel d'offres dans le règlement de consultation pour le dépouillement des offres et dans le CCAP pour l’exécution du marché. Une demande de dérogation est possible. ( cf paragraphe ad hoc )

 

Pour information les exigences sont organisées telles que décrites ci-dessous.



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")




1. **Standards & Normes industrielles et étatiques :** ensemble des exigences relatives aux normes de niveau supérieur à respecter pour toute application étatique
2. **Code applicatif & Image :** exigences issues des “15 factors” pour garantir la conception d’une application “Cloud Native”, associées aux exigences minimales permettant de s’intégrer au contexte du Ministère de l’Intérieur
3. **Modèle d’opération :** _voir le chapitre précédent_
4. **Intéractions & Flux :** exigences d’intégration et d’intéraction inter-applicatives dans le contexte étatique et du Ministère de l’Intérieur
5. **Infrastructure :** exigences et prérequis concernant l’infrastructure sous-jacente (notamment Kubernetes)
6. **Services mutualisés Applicatifs et d'Infrastructure :** exigences d’intégration aux services centralisés du Ministère de l’Intérieur, permettant une homogénéisation de la production, un meilleur contrôle et une maîtrise de la dette technique

--- page laissée vide ---


# 


# 5 - Annexes


## Liens vers autres documents et contenus utiles(informatif)

[https://kubernetes.io/fr/](https://kubernetes.io/fr/)

[https://www.rancher.com/products/k3s](https://www.rancher.com/products/k3s)

<span style="text-decoration:underline;">https://www.redhat.com/en/technologies/cloud-computing/openshift</span>

[https://argo-cd.readthedocs.io/en/stable/](https://argo-cd.readthedocs.io/en/stable/)

[https://www.redhat.com/en/topics/microservices/what-is-a-service-mesh](https://www.redhat.com/en/topics/microservices/what-is-a-service-mesh)

<span style="text-decoration:underline;">https://www.redhat.com/en/topics/devops/what-is-gitops</span>

[https://www.cloudcomputingpatterns.org/](https://www.cloudcomputingpatterns.org/)

[https://12factor.net/fr/](https://12factor.net/fr/)

[https://tanzu.vmware.com/content/blog/beyond-the-twelve-factor-app](https://tanzu.vmware.com/content/blog/beyond-the-twelve-factor-app) 

[https://www.techworld-with-nana.com/devops-bootcamp](https://www.techworld-with-nana.com/devops-bootcamp)

[https://ecoresponsable.numerique.gouv.fr/publications/bonnes-pratiques/bonnes-pratiques/#bonnes-pratiques-services-numeriques](https://ecoresponsable.numerique.gouv.fr/publications/bonnes-pratiques/bonnes-pratiques/#bonnes-pratiques-services-numeriques)

La documentation sur le CloudPI (RIE) :[ https://pi.minint.fr/reseau-cas-dusage/](https://pi.minint.fr/reseau-cas-dusage/) 
