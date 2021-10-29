---
layout: post
title:  "Some breaking changes in Angular 12"
date:   2021-06-17 18:26:45 +0300
categories: spa angular
image: "/assets/images/Angular-12-Now-Released.png"
author: "Mahefa Abel"
locale: "fr"
---

![Image Angular 12](/assets/images/Angular-12-Now-Released.png)

### Breaking changes in Angular 12

Voici quelques gros changements angular 12

#### Animation:

Dans Angular, la version 12 présente les composants DOM qui sont actuellement éliminés avec précision lorsque la vue racine est supprimée. Si vous utilisez SSR et utilisez le code HTML de l'application pour la livraison, vous devrez garantir que vous enregistrez le code HTML dans une variable avant de détruire l'application.

#### Common:

L'une des principales améliorations d'Angular 12 est que les stratégies de la classe HttpParams reconnaissent actuellement la chaîne, nombre, booléen plutôt que chaîne pour la valeur d'un paramètre. Si vous avez développé cette classe dans votre application, vous devrez mettre à jour les signatures de vos stratégies pour refléter ces changements.

#### Core:

Le type du jeton APP_INITIALIZER a été modifié pour refléter plus précisément les types de valeurs de retour pris en charge par Angular. Avant cela, chaque rappel d'initialisation était composé pour en renvoyer n'importe lequel, il s'agit actuellement de Promise <unknown> | Observable <inconnu> | annuler.

#### Compiler - CLI:

L'une des caractéristiques d'Angular 10 les plus intéressantes a été l'utilisation du nouvel extracteur IVY pour exécuter ng x i18n dans l'une de vos applications. L'une des nouvelles fonctionnalités d'Angular 12 est qu'il ne génère plus d'identifiants de message i18n hérités via des bibliothèques liées.

#### Form:

Auparavant, les attributs « min » et « max » caractérisés sur le `<input type=" number">` étaient ignorés par le module Forms. Actuellement, la présence de ces caractéristiques déclencherait une logique de validation min/max et la comparaison de l'état du contrôle de formulaire refléterait cela. 

#### Platform browser:

XhrFactory a été déplacé de `@angular/normal/http` vers `@angular/normal`.

**Router**:  
Des contrôles non valides stricts rendront compte du fait qu'une partie est peut-être invalide. Le type de l'entrée RouterLinkActive.routerLinkActiveOptions a été étendu pour permettre un contrôle encore plus ajusté. Le code qui a récemment lu cette propriété peut être mis à jour pour représenter le nouveau type.