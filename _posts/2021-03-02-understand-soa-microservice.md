---
layout: post
title:  "Comprendre l’architecture orientée service et le microservice"
date:   2021-03-02 17:26:45 +0300
categories: architecture
# image: "/assets/images/wso2-apim.gif"
author: "Mahefa Abel"
---

# Qu’est-ce que l’architecture orientée services?

**Def 1.**  L’architecture orientée services (SOA) est un style de conception logicielle où les services sont fournis aux autres composants par des composants d’application, via un protocole de communication sur un réseau. Ses principes sont indépendants des fournisseurs et des autres technologies. Dans une architecture orientée services, un certain nombre de services communiquent entre eux, de deux manières: en transmettant des données ou par le biais de deux services ou plus coordonnant une activité.

**Def 2.**  Une architecture orientée services (notée SOA pour Services Oriented Architecture) est une architecture logicielle s’appuyant sur un ensemble de services simples. Elle permet de décomposer une fonctionnalité en un ensemble de fonctions basiques, appelées services, fournies par des composants et de décrire finement le schéma d’interaction entre ces services.  
Lorsque l’architecture SOA s’appuie sur des web services, on parle alors de WSOA, pour Web Services Oriented Architecture.

# L’approche du SOA

![](https://miro.medium.com/max/60/1*FQ99eK0sxBD_xzF8ojr8tQ.png?q=20)

![](https://miro.medium.com/max/674/1*FQ99eK0sxBD_xzF8ojr8tQ.png)

## Couplage faible

Un principe sous-jacent dans l’application de la SOA aux technologies de l’information est le principe du couplage lâche, c’est-à-dire éviter ou au moins encapsuler les contraintes temporelles, technologiques et organisationnelles dans la conception du système d’information. Prise en charge du système à couplage lâche pour une liaison tardive ou dynamique à d’autres composants pendant l’exécution, et peut arbitrer la différence dans la structure, le modèle de sécurité, les protocoles et la sémantique du composant, ce qui élimine la volatilité. Le couplage lâche dans SOA est la façon dont les services sont mis en œuvre sans impact sur d’autres services ou applications. La seule interaction entre l’application et les services se fait via les interfaces de publication. Cela signifie que l’application ne s’intéresse pas à la façon dont les services ont été mis en œuvre

## Transparence de l’emplacement

La transparence de l’emplacement signifie que le consommateur du service ne se soucie pas de l’endroit où réside la mise en œuvre des services. Il peut s’agir du même serveur ou d’un autre serveur sur Internet. Les appels des consommateurs sont indépendants de l’emplacement du service.

## Réutilisabilité

La conformité SOA aux services Web et donc aux applications exécutées sur l’une ou l’autre plate-forme peut également consommer des services exécutés sur l’autre en tant que services Web qui facilitent la réutilisation. Une application SOA correctement conçue et mise en œuvre fournit une infrastructure qui offre des possibilités de réutilisation dans un environnement hétérogène tel que C, C ++, Java, .Net, etc.

## Testabilité riche

Étant donné que SOA confère une architecture basée sur les couches, il divise les tests en zones de test définissables telles que les services, la sécurité et la gouvernance, etc. Ces zones de test seraient testées séparément à l’aide des meilleurs outils et de la meilleure approche. Pour référence, JUnit ou NUnit permet la création d’une suite de tests. La suite de tests comprend un certain nombre de procédures, chacune étant conçue pour tester un service ou un composant. Dans l’environnement SOA, l’automatisation des tests est très courante pour les services d’entreprise qui changent fréquemment, ce qui améliore l’efficacité des tests de régression. L’autre aspect des tests SOA est que les tests de services réutilisables indépendants qui peuvent être testés indépendamment obligent le testeur à ne pas tester l’application globale à moins que tous les services ne soient passés avec succès. Des tests plus nombreux et de meilleure qualité signifient généralement moins de défauts et un niveau de qualité global plus élevé.

## Développement parallèle

L’architecture orientée services prône plus de parallélisme dans l’environnement de développement car la SOA est basée sur une architecture basée sur des couches. Étant donné que l’architecture orientée services confère une architecture basée sur les couches, elle préconise donc un développement plus parallèle. SOA consiste en un inventaire de services indépendants basés sur des contrats qui pourraient être développés en parallèle.

## Disponibilité supérieure et meilleure évolutivité

SOA une architecture multicouche peut être mise en cluster individuellement avec un équilibrage de charge approprié pour faire évoluer le système. Comme nous le savons, la redondance est la clé pour que la SOA haute disponibilité atteigne la redondance en introduisant des éléments redondants via le clustering. SOA utilise une architecture de couches pour faciliter le découplage logique qui permet de concevoir un système très résilient avec chaque couche de la pile des liaisons de communication doubles, aux routeurs et commutateurs redondants, aux serveurs en cluster et aux bases de données redondantes.

## Avantages / Incovenient

Les avantages de l’utilisation d’une architecture orientée services incluent:

-   La qualité du code est cohérente à travers le domaine.
-   Le partage des connaissances est facile dans le domaine.
-   Les erreurs ne se répètent pas, car l’équipe du domaine est au courant des échecs précédents.
-   Plus de ressources peuvent être mises en service si besoin est.

Les inconvénients de l’utilisation d’une architecture orientée services incluent:

-   Un bug / interruption dans un service peut affecter plusieurs services / couches.
-   Il manque une symphonie de domaines en raison de laquelle l’innovation pourrait faire défaut.
-   Les équipes peuvent finir par travailler sur une seule couche si elles ne sont pas gérées correctement.
-   La gestion de plusieurs fonctionnalités est difficile car elle peut impliquer des modifications sur plusieurs services.
-   Un service pourrait finir par changer beaucoup.

# Différences entre l’architecture orientée services et les microservices

![](https://miro.medium.com/max/60/1*8-uN932TKtSjNwLw3XuoJQ.png?q=20)

![](https://miro.medium.com/max/1325/1*8-uN932TKtSjNwLw3XuoJQ.png)

Les microservices, également connus sous le nom d’architecture de microservices, sont un «style architectural qui structure une application comme une collection de petits services autonomes, modélisés autour d’un domaine d’entreprise».  
Bien que les microservices et l’architecture orientée services soient similaires à certains égards, les principales différences résident dans leurs fonctionnalités. Les services sont, évidemment, la principale composante des deux. Il existe quatre types de services de base:

-   Service fonctionnel: ceux-ci définissent les opérations commerciales de base
-   Service d’entreprise: ceux-ci implémentent la fonctionnalité définie par les services fonctionnels
-   Service d’application: ils sont limités à un contenu d’application spécifique
-   Service d’infrastructure: implémente des tâches non fonctionnelles telles que l’authentification, l’audit, la sécurité et la journalisation