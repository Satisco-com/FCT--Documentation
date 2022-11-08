---
layout: default
title: DAOUT
nav_order: 300
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/daout
---


# Datout

## Présentation

<p align="center"><img src="../../../assets/img/functions/Functions-Processing-2.png" width="400"></p>

Il est ici question d'une fonctionalité assez inédite n'existant pas encore.
Il faut tout d'abord noter que chaque sortie d'une action a un nom unique grâce au DataModel.
>**Note**: ce nom unique l'est dans tout le modèle et pas seulement pour le contexte de l'action, le stage ou le scenario.

Il est ensuite assez facilement compréhensible que chaque sortie peut-être renvoyée à une autre action un peu plus loin dans le process, ceci grâce uniquement à l'unicité du nom de chaque sortie.

Le but est de permettre l'échange de données sans passer par l'action suivante/précédente. Il en résulte la diminution de la consommation RAM du Processing et une facilité de gestion d'action partagée accrue.

>**Exemple**: Une première activité de control avant d'effectuer la transformation des données. Un control peut être de type fonctionnel ou technique comme la gestion de traitement séquentiel.
