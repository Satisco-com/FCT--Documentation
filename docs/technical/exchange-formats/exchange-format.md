---
layout: default
title: Exchange Formats
nav_order: 5200
permalink: /docs/technical/exchange-formats
---

# Exchange Formats

## Why
Si l'on compare SSB à des briques de construction, il y a un standard qui a été mise en place afin de rendre toute les briques compatibles entre elles.
C'est ce choix de standardisation qui permet la modularité et l'intégration de nouvelle briques avec le temps.

Ici, le but est de garder une modularité du SSB, il est donc indispensable de définir un standard entre tous les composants.
Dans le monde de l'IT, ce standard n'aura pas seulement pour effet de faciliter la communication des briques entre elle mais aussi la maintenance et le support car les informations seront toujours au même endroit.

## What
Il existe de nombreux format de fichiers mais ils ne sont pas tous propice à la modélisation d'un Bus générique et modulaire.
De plus, il faut bien prendre en compte le langage principal utilisé pour SSB, ici ITX car même si ITX est capable de gérer tous type de format de fichier, certains sont plus facilement intégrables que d'autre.

Deux formats sont aujourd'hui très facilement gérable avec ITX, le XML et le JSON.
Tous deux ont un format de schéma relatif, le XSD pour le XML et le JSON Schema pour JSON.
Dans ITX, il est possible de les utiliser pour générer un type tree mais attention en ITX 9, l'importateur JSON n'est pas optimisé et l'importateur XML a lui aussi certaine limite comme la gestion du CDATA en mode Classic ou de la concaténation de XML en mode Xerces.

L'expérience XXXX nous a démontré que le XML ne se prête pas bien à toute les situations et contient certaines limitations.
Par exemple, le besoin UTF-8 ou l'encodage en Base64 pour intégrer un XML dans un XML (le xs:any n'est pas bien représenté en ITX).
De plus le XML reste l'un des formats les plus verbeux et même s'il est facilement lisible par l'Humain, il est consommateur de ressource.

Notre attention se portera donc au JSON, plus léger et "ouvert".
Un convertisseur JSON/XML pourra être pensé dans le cas où d'autre logiciel du SSB ne sont pas capable de traiter le JSON mais l'important est le core et donc ITX.

## How
Le JSON représentera un message qui transit à l'intérieur du SSB et permettra de suivre son évolution au fur et à mesure des composants.
Il sera nécessaire de découper le SSB Message en plusieurs sous catégories afin de l'organiser au mieux pour faciliter le support et la maintenance.

Il y a des avis contradictoires sur le fait que ce message porte ou non la partie configuration d'un flux.
Ils sont contradictoires car ils dépendent du besoin exact.
L'absence de la partie configuration complète du flux supprimera la visibilité passée et future du message. Cela diminuera la maintenance et supprimera la possibilité de relancer le flux dans un contexte identique à son exécution cependant cela rendra le SSB Message beaucoup plus léger.
Il est possible d'imaginer le core framework dépendant d'un ou plusieurs paramètres qui activerai le nettoyage du SSB Message au fur et a mesure de ses étapes. C'est une option envisageable.
Je pense personnellement (Anthony DANSET) qu'il ne faut pas perdre le contexte du message et donc sa configuration car la maintenance qui en découle sera beaucoup plus complexe. Si le message est considéré comme trop gros, c'est qu'il y a un soucis d'architecture avant tout.

L'idée des sections sera la suivante:
- La partie setup: les info nécessaires au traitement du message
- La partie broker: les info relatives à SSB (ID interne, date d'entrée, shunter key, class de SSB Message)
- La partie contextuelle: les info de la provenance et la direction du message à un instant T
- La partie Data: le payload et les autre fichiers/data nécessaires au contexte d'exécution
