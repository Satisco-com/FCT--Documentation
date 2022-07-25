---
layout: default
title: Function 1
nav_order: 1
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/function1
---


# Function 1

## Présentation

<p align="center"><img src="../../../assets/img/functions/FCT--Framework--Functions--Processing--F1.jpg" width="500"></p>

Vous l'avez compris, la fonction primaire du Processing est de pouvoir executer une ou plusieurs actions à la suite.
C'est à première vue une fonctionalité basique et simple mais qui induit des sous fonctionalités importante.

## Error Handling

<p align="center"><img src="../../../assets/img/functions/FCT--Framework--Functions--Processing--F1--ErrorHandling.jpg" width="500"></p>
En cas d'erreur sur une activité lors de son execution, il est important de savoir quel choix devra être fait:
1. Je continue le flux
2. J'arrête le flux
Si l'on continue, il faudra s'assurer que c'est effectivement possible.
En cas d'arrêt, il faut monitorer tout ce qui est disponible.

## Monitoring

<p align="center"><img src="../../../assets/img/functions/FCT--Framework--Functions--Processing--F1--Monitoring.jpg" width="500"></p>
Ici une des pièces maitresse de **SAI** car l'execution d'une ou plusieurs activités peut se faire sur un ou plusieurs thread dépendamment de la puissance souhaitée et du logiciel du framework.
Dans le cas de **SAIF** (Satisc Application Integration Framework), un thread de Processing correspondra à une ou plusieurs actions dans un seul et même stage. Ceci ayant pour but de garantir un bon équilibre entre performances/maintenance.
>**Attention**: il a été volontairement choisi de ne pas executer plusieurs Stage dans un seul Processing à cause de la complexité du code et donc de sa maintenance avec le produit ITX. Ceci l'exclus pas cette possibilité avec un autre logiciel.

La problématique de **SAIF** est qu'il est difficile de suivre une execution en détail car les outils de base de ITX sont limités. L'idée est de réussir à faire du monitoring presque en temps réel.
