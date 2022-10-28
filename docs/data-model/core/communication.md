---
layout: default
title: Blue - Communication
parent: Core Model
grand_parent: 5-Data Model
nav_order: 4
---

# Communication #

## Introduction
<p align="center"><img src="../../assets/img/data-model/Communication.png" width="500"></p>

La partie Communication Settings représente ce qu’on appellera dans le futur les Connector In et Connector Out du Framework.

Ces settings représenterons tout type de connectivité à SSB. Des échanges interne MQ à un partner externe en SFTP.

## Node
Le Node est un point central de la connectivité, il représente un point de connection ainsi qu’une méthode.

C’est par exemple l’adresse 10.0.0.1 en FTP avec l’utilisateur admin et mot de passe password.

## Channel
Un channel est une route vers un Node, c’est par exemple le dossier facture sous le précédemment expliqué.

## Protocol & Attributes References
Le protocol est lié au Node et représente la méthode de connection, par exemple FTP.

Au protocol seront liés des Attributes Reference qui permettrons de pré-définir et limiter les paramètres d’un protocol.

Ainsi, tous les Nodes et Channels FTP auront accès aux mêmes paramètres. Un changement dans ces références comme l’ajout ou la suppression d’un paramètre s’appliquer donc à tous les Nodes et Chanels liés.

## Attributes Values
C’est une partie un peu particulière car elle peut être liée à soit un Node soit un Channel car les Attributes d’un Node ne sont pas disponible pour un Channel et l’inverse est vrai aussi.
