---
layout: default
title: Test Parts
nav_order: 6
permalink: /docs/test-parts
---

# Test Parts

## Presentation

Ici nous allons documenter l'intégralité des tests qui seront créés pour SAI.
Chaque fonctionalité SAI pourra résulter un ou plusieurs tests afin de garantir que SAI répond au besoin décrit.

Le regroupement de ces tests permettera aussi de valider toute possiblité de regression lors d'un nouveau developpement.
Chaque test devra être executer dans un contexte stable et constant, ainsi que son résultat.
La comparaison se fera sur le maximum de valeur possible mais certaines comme la date du jour où certains ID ne le pourront pas.


## Normalisation

Afin de bien documenter les tests et ainsi faciliter les échanges à ce sujet, une convention de nommage sera défini comme suit:
- "TPT" pour indiquer un test part
- "-" en séparateur
- "[A-Z]{3}" 3 lettres majuscules pour le nom du composant SAIF
- "-" en séparateur
- "[A-Z]{5}" 5 lettres majuscule pour la fonctionalité SAIF
- "-" en séparateur
- "[0-9]{5}" 5 chiffres pour le numéro du test

## Liste

| Test MIACT ID   	| Description  	| Lesson Learned  	| Initial Date  	|
|---	|---	|---	|
| TPT_PRG_MIACT_00001  	| Execute one action  	|    | 16 Sept 2022  	|
| TPT_PRG-MIACT_00002  	| Map not found  	| CER-ITX-IEXEC-00003   | 16 Sept 2022  	|
| TPT_PRG-MIACT_00003  	| Map failed  	| CER-ITX-IEXEC-00076   | 16 Sept 2022  	|
| TPT_PRG-MIACT_00004  	| Invalid command  	| CER-ITX-IEXEC-00065   | 16 Sept 2022  	|
| TPT_PRG-MIACT_00005  	| Action not found  	| CER-PRG-MIACT-00001   | 16 Sept 2022  	|
| TPT_PRG-MIACT_00006  	| Map warning  	| CWG-ITX-IEXEC-00021   | 17 Sept 2022  	|
| TPT_PRG-MIACT_00007  	| Stage not found  	| CER-PRG-MIACT-00002   | 17 Sept 2022  	|
| TPT_PRG-MIACT_00008  	| Execute two actions  	|    | 17 Sept 2022  	|
| TPT_PRG-MIACT_00009  	| Execute ten actions  	|    | 20 Sept 2022  	|
| TPT_PRG-MIACT_00010  	| Execute from action 3  	|    | 20 Sept 2022  	|


| Test DAOUT ID   	| Description  	| Lesson Learned  	| Initial Date  	|
|---	|---	|---	|
| TPT_PRG_DAOUT_00001  	| One Output Data  	|    | 22 Sept 2022  	|
| TPT_PRG_DAOUT_00002  	| One empty Output Data and optional  	| CWG-PRG-TEREF-00001   | 22 Sept 2022  	|
| TPT_PRG_DAOUT_00003  	| One empty Output Data and mandatory  	| CER-PRG-TEREF-00003   | 26 Sept 2022  	|
| TPT-PRG_DAOUT_00004  	| Output Action 1 to input Action 2  	|    | 27 Sept 2022  	|
| TPT-PRG_DAOUT_00005  	| Output Action 1 to input Action 3  	|    | 28 Sept 2022  	|


| Test TEREF ID   	| Description  	| Lesson Learned  	| Initial Date  	|
|---	|---	|---	|
| TPT_PRG_TEREF_00001  	| Fail on Warn Control Option  	| CER-ITX-IEXEC-00021   | 21 Sept 2022  	|
| TPT_PRG_TEREF_00002  	| Trace Control Option  	|    | 21 Sept 2022  	|
| TPT_PRG_TEREF_00003  	| AuditLog Control Option  	|    | 22 Sept 2022  	|
| TPT_PRG_TEREF_00004  	| Data Audit Settings Control Option  	|    | 22 Sept 2022  	|
