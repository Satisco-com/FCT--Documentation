---
layout: default
title: ChangeLog
parent: Core Model
grand_parent: Data Model
---

# ChangeLog

All notable changes to this project are documented in this file.

## v0.7.0
[Annex 6](../../../../assets/img/data-model/archives/DataModel-v0.7.0.png)

### Features

- Ajout d'une table de scheduler basée sur le fonctionnement du crontab

## v0.6.0
[Annex 5](../../../../assets/img/data-model/archives/DataModel-v0.6.0.png)

## Features

- Après une courte revu, il parait évident que la décorelation entre Flow, Message et Partner permet de supprimer le besoin d'une table de jonction entre Flow et Stage.
- Nous supprimons donc Scenario pour renommer ensuite Flow par Scenario.

## v0.5.0
[Annex 4](../../../../assets/img/data-model/archives/DataModel-v0.5.0.png)

### Features

- Il est ici question de la gestion événementiel dans SSB.
- L'idée est de supprimer la table côté Framework beaucoup trop générique et de la transposer à l'intérieur de la partie Data.
- Cela va permettre de nettoyer aussi le future Processing d'une gestion EVENT complexe et de les lier directement au produit d'une action.
- Les codes communs sont possiblement à prévoir dans la partie Label/value

## v0.4.0
[Annex 3](../../../../assets/img/data-model/archives/DataModel-v0.4.0.png)

### Features

- Dans cette révision, le focus est mis sur la partie Message préalablement liée à un Flow.
- La problématique d'un Flow est qu'il ne représente pas un seul et unique message mais une liste.
- Le second problème est que bien qu'un Channel puisse être supposé uniquement utilisé pour un type de message, il est impossible de le vérifier tant que celui-ci n'est pas passé dans la partie Processing.
- L'idée est donc de lier un message à la table Data. Ceci permet de spécifier le type de message entrant et sortant pour une activité en particulier et donc dans un contexte précis.

## v0.3.0
[Annex 2](../../../../assets/img/data-model/archives/DataModel-v0.3.0.png)

### Features

- Cette révision du modèle de données de SSB permet de supprimer la relation entre un Partner et un Flux.
- L’idée est de dire qu’un Partner n’est pas forcément lié à un flux mais que dans tous les cas, un Channel lui est forcément lié à un Partner qu’il soit interne ou externe.
- Ceci permet de supprimer la table de jonction entre un Tower Flow et la section Partner.
- Ceci permet de supprimer le lien entre Shunting et Partner, il devient ici implicit via la table Channel.

## v0.2.0
[Annex 1](../../../../assets/img/data-model/archives/DataModel-v0.2.0.png)

### Features
- Suppression de la partie routing pour un merge entre Matching et Routing afin de créer le Shunting
- C'est ici qu'apparait la table Data qui permet de supprimer la partie Routing et ses dépendances complexes

## v0.1.0

### Features

- Point de départ basé sur les connaissances de Anthony DANSET ainsi que ses expériences.
