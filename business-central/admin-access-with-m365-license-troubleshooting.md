---
title: Résoudre les problèmes d’accès avec les licences Microsoft 365
description: Découvrez comment vous pouvez résoudre les problèmes d’accès à Business Central avec seulement une licence Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Résoudre les problèmes d’accès avec les licences Microsoft 365

## Symptômes

Quand vous accédez à un enregistrement dans Teams, un message d’erreur s’affiche sur un onglet ou des détails de carte similaires à :

« Cette page utilise des données de tables associées auxquelles vous n’avez pas accès. Pour utiliser toutes les fonctionnalités de cette page, contactez l’administrateur. »

## Motif

Il vous manque très probablement des autorisations d’objet pour les tables auxquelles la page ou l’enregistrement actuel est lié.

## Symptômes

L’accès a été activé, mais les utilisateurs reçoivent un message d’erreur d’autorisation quand ils accèdent à un enregistrement.

## Motif

Si vous activez l’accès dans le centre d’administration Business Central, mais n’attribuez pas d’autorisations dans la page Configuration de la licence, toute personne qui tente d’accéder aux enregistrements Business Central dans Teams verra son enregistrement utilisateur approvisionné sans autorisation sur aucun objet. Business Central est sécurisé par conception : les administrateurs doivent d’abord configurer les données accessibles dans Teams. 

## Résolution

La personnalisation des autorisations dans la page Configuration de la licence n’affectera que les utilisateurs nouvellement créés. Vous devez également attribuer les autorisations manquantes aux utilisateurs qui ont déjà été créés via la page de liste des utilisateurs. 

## Symptômes

Quand je partage un lien dans Teams, d’autres obtiennent l’erreur « Pendant l’accès à Business Central avec une licence Microsoft 365, vous ne pouvez afficher que les données dans Microsoft Teams ».

## Motif

Pendant le partage d’un lien Business Central vers une conversation instantanée ou des canaux Teams, la navigation avec un lien sortira toujours de Microsoft Teams où les données ne deviennent plus accessibles à une personne ayant une licence Microsoft 365.

## Résolution

Pendant le partage de pages ou d’enregistrements, incluez l’aperçu du lien sous forme de carte ou partagez les données sous forme d’onglet dans la discussion instantanée ou le canal.

## Voir aussi

[Accès à Business Central avec les licences Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configuration de l’accès avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
[Intégration de Business Central et Microsoft Teams](across-teams-overview.md)
[Partage d’enregistrements Business Central et de liens de page dans Microsoft Teams](across-working-with-teams.md)  
[Résoudre les problèmes d’intégration de Teams](admin-teams-troubleshooting.md)  