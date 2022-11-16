---
layout: default
title: DAOUT
nav_order: 300
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/daout
---


# Data Output

## Presentation

<p align="center"><img src="../../../assets/img/functions/Functions-Processing-2.png" width="400"></p>

{: style="text-align: justify" }
**Executer une ou plusieurs actions**, c'est **LA** fonctionalité primaire de SAI.
Son but est de pouvoir executer une ou plusieurs actions à la suite, c'est à dire dans une seule et même execution de Processing.

## Présentation


Il est ici question d'une fonctionalité assez inédite n'existant pas encore.
Il faut tout d'abord noter que chaque sortie d'une action a un nom unique grâce au DataModel.
>**Note**: ce nom unique l'est dans tout le modèle et pas seulement pour le contexte de l'action, le stage ou le scenario.

Il est ensuite assez facilement compréhensible que chaque sortie peut-être renvoyée à une autre action un peu plus loin dans le process, ceci grâce uniquement à l'unicité du nom de chaque sortie.

Le but est de permettre l'échange de données sans passer par l'action suivante/précédente. Il en résulte la diminution de la consommation RAM du Processing et une facilité de gestion d'action partagée accrue.

>**Exemple**: Une première activité de contrôle avant d'effectuer la transformation des données. Un contrôlee peut être de type fonctionnel ou technique comme la gestion de traitement séquentiel.


## SAI Identifier

{: style="text-align: justify" }
Cette fonctionalité sera identifier plus tard sous le nom de **DAOUT**. Tout ce qui concerne donc les test parts, les codes error ou warning et tous liens avec celle-ci seront docn mentionnés avec **DAOUT**.
