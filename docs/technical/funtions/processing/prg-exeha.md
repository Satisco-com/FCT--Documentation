---
layout: default
title: EXEHA
nav_order: 400
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/exeha
---


# EXEPA

## Présentation


Pour chaque action, il sera possible de définir une ou plusieurs sortie via la table DAT_DATA.
Chacune de ces sorties pourra avoir un impact sur l'execution du flux.

Il sera par exemple possible d'arrêter le flux, de le router vers un autre flux ou encore de mettre le message *attente* pour un besoin business.
Une telle solution peut avoir un impact important en fonction de la technologie utilisée car le fait d'attendre induit la question de savoir si l'on met en pause la tâche mais celle-ci reste en sommeil, ou encore si l'on arrête la tâche pour plus tard mais dans ce cas, comment la reprendre au bon endroit?

En utilisant ITX et MQ, il est possible d'obtenir une solution fiable avec des délais variables sans impacter les performances.
Il s'agit tout simplement de l'EXPIRY et du BACKOUT qui sont deux fonctionalités interne à MQ.
Fonctionnellement, un message arrive dans une queue avec une date d'expiration et sa destination après son expiration.
Il suffit ensuite d'utiliser une queue tampon standalone pour renvoyer les messages à l'endroit souhaité.
Côté ITX cela demande l'utilisation des header MQ et c'est tout.

Ceci permettera de définir des temps complètement variables en secondes et ainsi donnera une grande liberté au développeur.
>**Exemple**: l'appel d'une API de génération de PDF qui indique que le PDF n'est pas encore prêt. L'action sort une data indiquant un wait time de 15secondes.

En couplant cette fonctionalité avec les technical reference, il devient possible de définir un nombre maximum d'essai voir un wait variable en fonction du business ou du nombre d'essaie.




Gestion des EVENT/KO/CODE

La base est un code retour ITX (12) lié à une DATA et un EXEC IMPACT STOP
Code générique ERROR avec un exec impact STOP
