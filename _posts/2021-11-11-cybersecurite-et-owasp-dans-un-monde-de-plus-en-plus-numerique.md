---
layout: post
title:  "Cybersécurité et OWASP dans un monde de plus en plus numérique"
date:   2021-11-11 21:42:21 +0300
categories: security owasp
image: "/assets/images/owasp.png"
author: "Mahefa Abel"
---

![Cybersécurité et OWASP](/assets/images/owasp.png)

Alors que le monde évolue de plus en plus vers un format numérique, la cybersécurité devient plus importante que jamais. C'est d'autant plus important que 51 % des entreprises américaines ont subi une attaque de ransomware en 2020. C'est un nombre impressionnant de vulnérabilités de sécurité qui ne devraient vraiment pas exister de nos jours. Pourtant, c'est relativement compréhensible.

## Sécurité des applications

Fondamentalement, la question de la sécurité des applications est multiforme, avec une variété de techniques, de philosophies et de certifications qui peuvent être appliquées pour rendre toutes les applications plus sûres.

Par exemple, prenez la récente mise à jour de l'énumération des faiblesses communes (CWE) de MITRE, qui elle-même a été construite sur le cadre incroyablement populaire ATT&CK. Parrainé par l'Agence américaine de cybersécurité et de sécurité des infrastructures (CISA), l'objectif est de catégoriser les faiblesses et les vulnérabilités de la sécurité dans l'espoir de comprendre les défauts spécifiques de chaque catégorie et de savoir comment les atténuer. En fait, CWE compte plus de 600 catégories, allant du débordement de la mémoire tampon aux scripts intersites et même aux conditions de concurrence.

## Sécurité Web et cloud

Comme vous pouvez l'imaginer, une grande partie du monde moderne est hébergée dans le cloud. et par conséquent, la sécurité du cloud joue un rôle important pour garantir la sécurité des données. En fait, la sécurité des applications hébergées dans le cloud est devenue un problème, d'autant plus qu'il n'y a souvent pas de personne DevSecOps spécifique au cloud pour s'assurer que l'application est à l'abri des vulnérabilités extérieures potentielles.

## L'importance de l'OWASP

C'est là que l'Open Web Application Security Project (OWASP) devient un guide précieux. OWASP est un ensemble de directives et de critères stricts pour la sécurité des applications. La liste de contrôle OWASP aide les développeurs à intégrer plus facilement les normes de sécurité recommandées tout en aidant à éviter les failles de codage qui peuvent compromettre la sécurité.

-   **Encodage de sortie**: Toute information saisie par un utilisateur doit être encodée avant d'être validée car elle est un vecteur possible d'attaque. Cela signifie que la sortie doit être filtrée contextuellement à l'aide d'une routine de test standard. En fait, .Net Core a un codage de sortie intégré.

-   **Validation d'entrée**: Il est important de s'assurer que les données saisies par un utilisateur sont valides et ne permettent aucune forme d'attaque. Cela prend souvent la forme d'une vérification par rapport à une variété de listes qui s'assurent que les données d'entrée sont sécurisées ou ne vont pas conduire à une forme d'attaque par injection.

-   **Pratiques cryptographiques**: Garantir la capacité de gérer plusieurs connexions à une application Web en même temps est vital pour la sécurité. C'est là que HTTP ainsi que d'autres techniques telles que la génération de nouveaux identifiants de session lors de la réauthentification et les délais d'inactivité de session jouent un rôle.

-   **Pratiques cryptographiques**: Comme pour tout sur le Web, il est extrêmement important de maintenir une stricte confidentialité et l'intégrité des données. De bonnes pratiques cryptographiques, y compris la défaillance sécurisée des modules cryptographiques, les politiques de gestion des clés cryptographiques et l'utilisation et la mise en œuvre d'un système de confiance sont essentielles pour y parvenir.

-   **Sécurité des communications**: Les attaques de type man-in-the-middle sont beaucoup trop courantes, et c'est là qu'il est important de s'assurer que non seulement les données sont protégées des interceptions extérieures, mais qu'elles sont également facilement compréhensibles par le récepteur autorisé. Une mise en œuvre solide de TLS est importante, ainsi que la configuration appropriée du protocole.

-   **Sécurité de la base de données**: Des informations d'identification de base de données valides et la désactivation des fonctionnalités inutiles sont primordiales pour garantir les normes de sécurité de la base de données.

-   **Gestion de la mémoire**: Avec une variété de violations de sécurité liées aux fuites de mémoire récemment, il est important de garder la mémoire au premier plan des considérations de sécurité. Par exemple, un débordement de tampon peut être une énorme faille de sécurité, et il en va de même pour une dépendance à l'égard de la « récupération de données » telle que les objets de connexion et les descripteurs de fichiers.