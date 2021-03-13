---
layout: post
title:  "Interagir avec Google et Amazon"
date:   2021-03-02 18:26:45 +0300
categories: cloud
---

L’objectif de cet article est de partager les fondamentaux du Cloud Computing

-   Primo, nous clarifierons ce qu’est le Cloud Computing.
-   Puis nous décrirons sa modélisation et son implémentation dans le système d’information ainsi que les responsabilités qui y sont associées.
-   Nous terminerons avec une proposition de valeur reposant sur l’économie et l’optimisation.

# Qu’est-ce que le Cloud Computing

La technologie Cloud Computing est la plus populaire aujourd’hui en raison de sa flexibilité et de sa mobilité. Le Cloud Computing permet l’accès aux ressources personnelles et partagées avec une gestion minimale. Il repose souvent sur Internet. Une solution cloud tierce est également disponible, ce qui permet d’économiser des ressources et de la maintenance. L’exemple le plus approprié de cloud computing est Amazon Elastic Cloud Compute (EC2), très performant, peu coûteux et flexible.

Le cloud computing est une prestation à la demande de capacités informatiques où l’infrastructure et les applications informatiques sont fournies aux abonnés sous la forme d’un service mesuré sur un réseau.

# Types de services de cloud computing

## Infrastructure en tant que service (IaaS)

Fournit des machines virtuelles et d’autres matériels et systèmes d’exploitation abstraits qui peuvent être contrôlés via une API de service.  
Iaas également connu sous le nom de service d’infrastructure Cloud est essentiellement un modèle de libre-service. Iaas est utilisé pour accéder, surveiller et gérer des fins.  
Par exemple, au lieu d’acheter du matériel supplémentaire comme un pare-feu, des périphériques réseau, un serveur et de dépenser de l’argent pour le déploiement, la gestion et la maintenance, le modèle IaaS propose une infrastructure cloud pour déployer un centre de données distant.  
Par exemple, Amazon EC2, Go grid, Sungrid, Windows SkyDrive, etc.

## Plate-forme en tant que service (PaaS)

Offre des outils de développement, une gestion de la configuration et des plateformes de déploiement à la demande qui peuvent être utilisés par les abonnés pour développer des applications personnalisées.  
Il permet de développer, exécuter et gérer des applications. Paas propose la gestion de la configuration des outils de développement, les plates-formes de déploiement et la migration de l’application vers des modèles hybrides. Il aide essentiellement à développer et à personnaliser des applications, à gérer les systèmes d’exploitation, la visualisation, le stockage et la mise en réseau, etc.  
Par exemple, Intel MashMaker, Google App Engine, Force.com, Microsoft Azure, etc.

## Logiciel en tant que service (SaaS)

Propose des logiciels aux abonnés à la demande sur Internet.  
Le SaaS est le type de service Cloud Computing le plus populaire et le plus utilisé. Service à la demande hébergé de manière centralisée pour être accessible aux utilisateurs utilisant le client via les navigateurs.  
Par exemple, des applications bureautiques Web telles que Google Docs of Calendar, Salesforce CRM, etc.

# Le principe du Cloud Computing

Le Cloud Computing met en évidence deux grands principes d’infrastructure que sont la  **virtualisation**  et la  **mutualisation**.

De fait, un DataCenter est constitué de ressources de traitement (CPU), de mémoire (ou RAM, « Random Access Memory ») et de disque (Espace de stockage). Notons dans le même temps qu’une application s’appuie sur des ressources de traitement et sur un système d’exploitation.

![](https://miro.medium.com/max/60/0*2-U04NzPVvyKikCR?q=20)

![](https://miro.medium.com/max/66/0*2-U04NzPVvyKikCR)

![](https://miro.medium.com/max/60/0*XT_Fnyu_LWWu1IcX.png?q=20)

![](https://miro.medium.com/max/1546/0*XT_Fnyu_LWWu1IcX.png)

Le  **principe de virtualisation** nous permet de créer une couche d’abstraction logicielle sur la couche matérielle afin de répartir les ressources virtuellement sous la forme de vCPU (Virtual CPU), RAM et Disque. La couche logicielle permettant la virtualisation est appelée « hyperviseur » (au même niveau qu’un système d’exploitation ou OS). La création d’une nouvelle couche d’abstraction virtuelle nous permet de recréer des serveurs applicatifs à partir de ressources distribuées virtuellement. Nous noterons la notion de machine virtuelle ou de VM dans ce cas.

![](https://miro.medium.com/max/60/0*m_yJ51OSfGSXtrbK?q=20)

![](https://miro.medium.com/max/66/0*m_yJ51OSfGSXtrbK)

![](https://miro.medium.com/max/60/0*c76SbGzCm0tAshlc.png?q=20)

![](https://miro.medium.com/max/945/0*c76SbGzCm0tAshlc.png)

La notion clé dans une machine virtuelle est la couche d’abstraction sur laquelle celle-ci repose. En effet, la machine virtuelle ne dépendant pas d’une couche physique mise à disposition par les serveurs du datacenter, il est donc possible de la positionner de la même manière sur n’importe quel serveur du DataCenter.

Le  **principe de**  **mutualisation**  des ressources consiste en la multiplication des ressources physiques sous forme de grappes (clusters). En déployant le même hyperviseur sur l’ensemble de ces ressources, nous constituons un pool composé de machines virtuelles fonctionnant en parallèle.

![](https://miro.medium.com/max/60/0*301oqLheMJN9XT1t.png?q=20)

![](https://miro.medium.com/max/1546/0*301oqLheMJN9XT1t.png)

Ces mécanismes permettent d’ajouter ou de supprimer des serveurs physiques au pool de ressources mutualisées, le tout très facilement. L’abstraction du matériel physique permet alors de rendre le système hautement disponible et flexible. Ce faisant, il est alors possible de créer le Cloud, cloud dans lequel l’application finale est supportée par un nuage de serveurs et non plus par une unité physique spécifique.