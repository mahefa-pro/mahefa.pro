---
layout: post
title:  "Microservices : C'est que c'est et son architecture"
date:   2021-11-02 20:22:21 +0300
categories: microservice
image: "/assets/images/Microservice-cloud.jpg"
author: "Mahefa Abel"
---

![Micro Service](/assets/images/Microservice-cloud.jpg)

## Microservices, c'est quoi ?

**Microservices** est un modèle d'architecture orienté service dans lequel les applications sont construites comme un ensemble de diverses unités de service indépendantes les plus petites. Il s'agit d'une approche d'ingénierie logicielle qui se concentre sur la décomposition d'une application en modules à fonction unique avec des interfaces bien définies. Ces modules peuvent être déployés et exploités indépendamment par de petites équipes qui possèdent l'intégralité du cycle de vie du service.

Le terme « micro » fait référence au dimensionnement d'un microservice qui doit être gérable par une seule équipe de développement (5 à 10 développeurs). Dans cette méthodologie, les grosses applications sont divisées en plus petites unités indépendantes.

## Qu'est-ce que l'architecture de microservices ?

**Microservice Architecture**  is an architectural development style that allows building applications as a collection of small autonomous services developed for a business domain. It is a variant of structural style architecture that helps arrange applications as a loosely coupled service collection. The Microservice Architecture contains fine-grained services and lightweight protocols.

Let’s take an example of e-commerce application developed with microservice architecture. In this Microservices architecture example, each microservice is focused on single business capability. Search, Rating & Review and Payment each have their instance (server) and communicate with each other.

![Microservices Architecture](/assets/images/micro-service-ui-2.png)

<!-- ## Microservices vs. Monolithic Architecture -->

## Les défis des microservices

- Les MicroServices dépendent les uns des autres, et ils devront communiquer entre eux.
- Par rapport aux systèmes monolithiques, il y a plus de services à surveiller qui sont développés en utilisant différents langages de programmation.
- S'agissant d'un système distribué, il s'agit d'un modèle intrinsèquement complexe.
- Différents services auront leur mécanisme séparé, ce qui entraînera une grande quantité de mémoire pour des données non structurées.
- Gestion efficace et travail d'équipe requis pour éviter les problèmes en cascade
- Reproduire un problème sera une tâche difficile lorsqu'il est parti dans une version et revient dans la dernière version.
- Le déploiement indépendant est compliqué avec les microservices.
- L'architecture de microservices entraîne de nombreux frais généraux d'exploitation.
- Il est difficile de gérer l'application lorsque de nouveaux services sont ajoutés au système
- Un large éventail de professionnels qualifiés est nécessaire pour prendre en charge les microservices distribués de manière hétérogène
- Le microservice est coûteux, car vous devez conserver un espace serveur différent pour différentes tâches commerciales.

## Les outils Microservices

### 1) Wiremock: Tester les microservices

WireMock est une bibliothèque flexible pour le stub et les services Web moqueurs. Il peut configurer la réponse renvoyée par l'API HTTP lorsqu'il reçoit une requête spécifique. Il est également utilisé pour tester les microservices.

**Lien de téléchargement:**  [**http://wiremock.org/**](http://wiremock.org/)

### 2) Docker

Docker est un projet open source qui nous permet de créer, déployer et exécuter des applications à l'aide de conteneurs. En utilisant ces conteneurs, les développeurs peuvent exécuter une application en tant que package unique. Il vous permet d'expédier des bibliothèques et d'autres dépendances dans un seul paquet.

**Lien de téléchargement:**  [**https://www.docker.com/**](https://www.docker.com/)

### 3) Hystrix

Hystrix est une bibliothèque Java de tolérance aux pannes. Cet outil est conçu pour séparer les points d'accès aux services distants, aux systèmes et aux bibliothèques tierces dans un environnement distribué comme les microservices. Il améliore le système global en isolant les services défaillants et en empêchant l'effet en cascade des défaillances.

**Lien de téléchargement:**  [https://github.com/Netflix/Hystrix](https://github.com/Netflix/Hystrix)