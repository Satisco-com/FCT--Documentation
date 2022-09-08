---
layout: default
title: Techref
nav_order: 3
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/techref
---


# Techref

## Présentation

<p align="center"><img src="../../../assets/img/functions/" width="400"></p>

Le Processing permettera l'utilisation de **Technical References** qui devront respecter le format suivant:

<div align="center">"[" + Technical Reference Name + "]"</div>

Une techref pouvant être soit fournis par SAIF, et dans ce cas elle est disponible pour tout scénario, soit créé par une action dans le scénario, ce qui la rend disponible uniquement durant l'execution du scénario.

>**Exemple**: [AUDITLOG] force l'activation de l'audit log ITX

>**Exemple**: [SAIB] est remplacée par la chaine de connexion complète ITX vers la database SAI

>**Exemple**: [Counter] est remplacée par la valeur d'un compteur courant géré dans les actions
