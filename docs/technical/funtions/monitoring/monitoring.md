---
layout: default
title: Monitoring
nav_order: 300
parent: Functionalities
has_children: true
permalink: /docs/functionalities/monitoring
---

# Monitoring

## Presentation

<p align="center"><img src="../../../assets/img/functions/Functions-Processing-1-Monitoring.png" width="400"></p>
Ici une des pièces maitresse de **SAI** car l'execution d'une ou plusieurs activités peut se faire sur un ou plusieurs thread en fonction de la puissance souhaitée et du logiciel du framework.
Dans le cas de **SAIF** (Satisc Application Integration Framework), un thread de Processing correspondra à une ou plusieurs actions dans un seul et même stage. Ceci ayant pour but de garantir un bon équilibre entre performances/maintenance.
>**Attention**: il a été volontairement choisi de ne pas executer plusieurs Stage dans un seul Processing à cause de la complexité du code et donc de sa maintenance avec le produit ITX. Ceci ne l'exclut pas cette possibilité avec un autre logiciel.

La problématique de **SAIF** est qu'il est difficile de suivre une execution en détail car les outils de base de ITX sont limités. L'idée est de réussir à faire du monitoring en temps réel.
Pour cela, il faudra trouver un adapteur capable d'envoyer l'événement de monitoring avant même que le Processing soit fini et donc à chaque fin d'activité.
Il sera ainsi possible de tracer une possible execution trop longue ou tombée sans erreur critique.
>**Note**: La piste de l'utilisation de l'adapteur socket ITX est à creuser.
