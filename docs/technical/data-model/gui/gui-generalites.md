---
layout: default
title: Blue - GUI Generalites
parent: GUI Model
grand_parent: Data Model
nav_order: 1
---

# Communication #

## Introduction
<p align="center"><img src="../../../../assets/img/gui-model/GuiModel-v0.0.0.png" width="500"></p>

Le GUI est l'interface graphique d'administration et configuration. Elle devrait intégrer le monitoring mais ce n'est pas un pré-requis.

## Roles

Parlant d'une interface de configuration et administration, il est nécessaire de parler des rôles des utilisateurs qui vont interagir avec cette interface.

## Ecrans

## Securité

La connexion est gérée via une paire username/password, qui sont mémorisés dans la base de données (chiffrage du mot de passe bien sûr).

Les utilisateurs sont groupés par profil, un profil étant l'équivalent d'un groupe. Les droits sont accordés à un groupe.

## Droits d'accès

Les droits d'accès sont gérés via :
	- 3 tables de définition permettant de déclarer les fenêtres, boutons et champs
	- 2 tables d'accès permettant de définir si un profil donné a accès à un bouton ou un champ.
	- Pour les champs, un drapeau permet de gérer l'autorisation de modification

Ceci permet de créer des profils de visualisation ou de mise à jour.

## Historisation

La mise à jour de règles est systématiquement capturée par un journal qui permet d'identifier l'auteur et le moment d'une action.

## Déploiement

Le rôle du GUI pour l'exécution s'arrête au moment où un utilisateur autorisé clique le bouton "déployer", génèrant ainsi le fichier de règle utilisé par le moteur d'exécution pour effectuer son routage.
