---
layout: default
title: Brown - Shunting
parent: Core Model
grand_parent: 5-Data Model
nav_order: 2
---

# Shunting #

## Introduction ##
<p align="center"><img src="../../assets/img/data-model/Shunting.png" width="250"></p>

L'expérience de __XXXX__ a permis de démontrer que des __composants__ et fonctionalités de __Matching et Routing__ sont __similaires__ en maintenance et fonctionalités,
La révision __2.0.0__ du modèle __XXXX__ a donc permis de créer un nouveau composant, le __Shunting__.

Le __Shunting__ sera donc la __gare de triage de FCT__ que ce soit depuis une __communication externe__ ou même à l'interieur d'un __scénario__.
> **Example:** Deux messages sont récupérés d'un même dossier mais le traitement est différent en fonction des données

> **Example:** Le traitement en deux sous branches d'un message XML par exemple vers EDIFACT et vers X12.

L'idée sera d'utiliser cette fonction à __l'interieur d'un scénario__ uniquement en cas de besoin de __triage__.
> **Example:** En fonction d'une donnée interne au message, il est envoyé à un client A ou B 

## Shunting ##
C'est la table __primaire du Shunting__, elle autorise jusqu'à __5 clés de filtrage__ basiques appelées __SHUNTER_KEY__.
Ceci ne signifie pas qu'il ne sera pas possible de filtrer au dela de 5 clés, mais plutôt que ces __5 clés__ représentent un __filtrage plus rapide__.
L'__IHM__ de FCT sera utilisée avec la fonctionnalité de __Generic Codes__ afin de customiser le __nom des clés__ en fonction de __l'utilisateur__.
> **Example:** Chez XXXX, nous avons Sender, Receiver, ShipcompCode, TradingPartner et MessageCode

La __priorité__ a pour but d'__augmenter les performances__ du Shunter car il est possible qu'un channel transmette plusieurs type de messages, il est donc préférable de mettre en __priorité 1__, les __messages__ les plus __nombreux__ selon les __statistiques__ afin d'éviter trop de __calcul inutile__.

En toute bonne __gare de triage__, cette table aura le plus de __liens__ avec les autres. Elle sera __centrale au modèle__.
Il sera donc possible de passer d'un __Channel à un Scenario__, d'une __Data à un Stage__ ou d'une __Data à un Channel__.

## Rules ##
Cette table est basée sur le __principe de clé/valeur__. C'est une __extension de Shunting__ afin d'ajouter de nouveau mode plus __avancés__.
L'idée est de pouvoir créer de nouvelles __briques d'identifications__, __pas__ toujours forcément __nécessaires mais utiles__ dans certains cas.
> **Example:** des règles de type EDIFACT afin de vérifier une valeur précise à l'interieur d'un fichier IN

> **Example:** des règles de type REGEX appliquées sur le nom du fichier IN

Pour qu'un __Shunting soit validé__, il faudra que l'intégralité des __rules__ liées le soit __aussi__.
La __priorité__ y sera aussi géré mais d'une façon différent du Shunting. Il sera ici question de définir en __priorité 1__, les __règles__ qui sont __vrai le moins souvent__ possible. De cette façon, la __première rule non valide__ permettera d'__invalider le Shunting__ lié.
