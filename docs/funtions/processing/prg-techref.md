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


Le Processing permettera l'utilisation de **Technical References** qui devront respecter le format suivant:

<div align="center">"[" + Technical Reference Name + "]"</div>

Une techref pouvant être soit fournis par SAIF, et dans ce cas elle est disponible pour tout scénario, soit créé par une action dans le scénario, ce qui la rend disponible uniquement durant l'execution du scénario.

>**Exemple**: [AUDITLOG] force l'activation de l'audit log ITX

>**Exemple**: [SAIB] est remplacée par la chaine de connexion complète ITX vers la database SAI

>**Exemple**: [Counter] est remplacée par la valeur d'un compteur courant géré dans les actions


Il sera bon de définir un standard à respecter dans la casse du nom des technical references.
En MAJUSCULES, les technical references de base fournies par SAIF uniquement.
Toutes les autres, en minuscule ou avec la première lettre en majuscule, seront considérées comme des technical reference de flux.

>**Note**: C'est une limite qu'il faudra tenter de mettre en place même si son application sera tout de même difficile.


## SAIF

|Technical Reference   	| Description  	|
|---	|---	|
| MSGID  	| SAI Message ID  	|
| DOCID  	| SAI Document ID  	|
