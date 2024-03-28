---
title: Résoudre les problèmes d’accès avec les licences Microsoft 365
description: Découvrez comment vous pouvez résoudre les problèmes d’accès à Business Central avec seulement une licence Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Résoudre les problèmes d’accès avec les licences Microsoft 365

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message"></a>Message d’erreur « Cette page utilise des données de tables associées auxquelles vous n’avez pas accès. »

### <a name="symptoms"></a>Symptômes

Quand vous accédez à un enregistrement dans Teams, un message d’erreur s’affiche sur un onglet ou des détails de carte similaires à :

« Cette page utilise des données de tables associées auxquelles vous n’avez pas accès. Pour utiliser toutes les fonctionnalités de cette page, contactez l’administrateur. »

### <a name="cause"></a>Motif

Il vous manque très probablement des autorisations d’objet pour les tables auxquelles la page ou l’enregistrement actuel est lié.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error"></a>L’accès Microsoft 365 a été activé, mais les utilisateurs reçoivent un message d’erreur d’autorisation

### <a name="symptoms-1"></a>Symptômes

L’accès avec Microsoft 365 a été activé dans le centre d’administration Business Central, mais les utilisateurs reçoivent un message d’erreur d’autorisation quand ils accèdent à un enregistrement.

### <a name="cause-1"></a>Motif

Si vous activez l’accès dans le centre d’administration Business Central, mais n’attribuez pas d’autorisations dans la page **Configuration de la licence**, toute personne qui tente d’accéder aux enregistrements Business Central dans Teams verra son enregistrement utilisateur approvisionné sans autorisation sur aucun objet. Business Central est sécurisé par conception : les administrateurs doivent d’abord configurer les données accessibles dans Teams. 

### <a name="resolution"></a>Résolution

La personnalisation des autorisations dans la page Configuration de la licence n’affectera que les utilisateurs nouvellement créés. Vous devez également attribuer les autorisations manquantes aux utilisateurs qui ont déjà été créés via la page de liste des utilisateurs. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data"></a>Vous avez partagé un lien dans Teams, mais les utilisateurs reçoivent un message indiquant qu’ils ne peuvent afficher que les données

### <a name="symptoms-2"></a>Symptômes

Quand vous partagez un lien dans Teams, en tant qu’utilisateur Business Central, d’autres obtiennent l’erreur « Pendant l’accès à Business Central avec une licence Microsoft 365, vous ne pouvez afficher que les données dans Microsoft Teams ».

### <a name="cause-2"></a>Motif

Pendant le partage d’un lien Business Central vers une conversation instantanée ou des canaux Teams, la navigation avec un lien sortira toujours de Microsoft Teams où les données ne deviennent plus accessibles à une personne ayant une licence Microsoft 365.

### <a name="resolution-1"></a>Résolution

Pendant le partage de pages ou d’enregistrements, incluez l’aperçu du lien sous forme de carte ou partagez les données sous forme d’onglet dans la discussion instantanée ou le canal.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button"></a>La carte du lien partagé est minimale et n’inclut pas le bouton Détails

### <a name="symptoms-3"></a>Symptômes

Lorsqu’un titulaire de licences Microsoft 365 sans licence Business Central partage un lien Business Central dans Teams, il se développe automatiquement en une carte qui ne contient aucune information utile et affiche uniquement Business Central sans bouton **Détails**.

### <a name="cause-3"></a>Motif

Les utilisateurs qui ont une licence Microsoft 365, mais pas de licence Business Central ne sont pas autorisés à partager des liens sous forme de cartes. Si l’utilisateur a installé l’application Business Central pour Teams et colle un lien dans la zone de rédaction, seule une carte minimale s’affiche. 

## <a name="see-also"></a>Voir aussi

[Accès à Business Central avec les licences Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configuration de l’accès avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
[Intégration de Business Central et Microsoft Teams](across-teams-overview.md)
[Partage d’enregistrements Business Central et de liens de page dans Microsoft Teams](across-working-with-teams.md)  
[Résoudre les problèmes d’intégration de Teams](admin-teams-troubleshooting.md)  
