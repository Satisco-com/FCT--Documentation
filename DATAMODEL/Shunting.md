# Shunting #

[Home Page](../README.md)

## Getting Started ##

<p align="center"><img src="FCT--Framework--DataModel--Shunting.png" width="200"></p>

C'est la table __primaire du Shunting__, elle autorise jusqu'à __5 clés de filtrage__ basiques appelées __SHUNTER_KEY__.
Ceci ne signifie pas qu'il ne sera pas possible de filtrer au dela de 5 clés, mais plutôt que ces __5 clés__ représentent un __filtrage plus rapide__.
L'__IHM__ de FCT sera utilisée avec la fonctionnalité de __Generic Codes__ afin de customiser le __nom des clés__ en fonction de __l'utilisateur__.
> Ex: Chez CMA-CGM, nous avons Sender, Receiver, ShipcompCode, TradingPartner et MessageCode

La __priorité__ a pour but d'__augmenter les performances__ du Shunter car il est possible qu'un channel transmette plusieurs type de messages, il est donc préférable de mettre en __priorité 1__, les __messages__ les plus __nombreux__ selon les __statistiques__ afin d'éviter trop de __calcul inutile__.

En toute bonne __gare de triage__, cette table aura le plus de __liens__ avec les autres. Elle sera __centrale au modèle__.
Il sera donc possible de passer d'un __Channel à un Scenario__, d'une __Data à un Stage__ ou d'une __Data à un Channel__.

> **Note**
> la gestion d'un mode transfer sans passer par aucune action
