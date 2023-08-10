---
title: Flux d’accès utilisateur pour les licences Microsoft 365
description: Obtenez un aperçu de ce qui se passe quand un utilisateur accède pour la première fois aux données de Business Central à l’aide de sa licence Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a>Flux d’accès utilisateur pour les licences Microsoft 365

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Cet article décrit de ce qui se passe quand un utilisateur accède pour la première fois aux données de Business Central à l’aide de sa licence Microsoft 365. La compréhension de ce flux permet aux administrateurs de planifier leur approche et de configurer Business Central en fonction de leurs besoins métier.

1. Tout d’abord, l’identité de l’utilisateur est authentifiée 
2. Business Central vérifie que tous les [besoins minimaux](admin-access-with-m365-license.md#minimum-requirements) sont satisfaits.
3. Business Central vérifie que cet utilisateur ne dispose pas d’une licence ultérieure telle qu’une licence Business Central ou d’un rôle administratif tel qu’un rôle d’administrateur délégué. 
4. Business Central vérifie si l’utilisateur accède aux données qui appartiennent à un environnement qui a activé l’accès avec les licences Microsoft 365. 
5. L’enregistrement utilisateur est approvisionné dans Business Central, en attribuant le groupe d’utilisateurs, le profil et les ensembles d’autorisations définis sur la page de configuration de la licence Microsoft 365. Par défaut, le groupe Utilisateurs Teams est attribué, le profil Employé est affecté et seul l’ensemble d’autorisations de connexion est attribué. Toute autre valeur par défaut des paramètres utilisateur est également appliquée, tout comme un utilisateur Business Central sous licence. 
6. Le modèle de sécurité complet de Business Central est appliqué pour déterminer si l’utilisateur doit pouvoir accéder à l’enregistrement, à la page, dans la société et l’environnement spécifiés. 

Si toutes les étapes réussissent, l’utilisateur peut désormais afficher ces données Business Central dans Teams. Le service Business Central garantit automatiquement un accès en lecture seule et simplifie l’interface utilisateur. 

Le compte d’utilisateur est maintenant enregistré dans Business Central et peut être géré comme n’importe quel utilisateur de Business Central.

> [!NOTE]
> Les étapes peuvent varier en fonction de la configuration de sécurité supplémentaire que vous avez spécifiée dans Microsoft 365 ou Business Central.

## <a name="see-also"></a>Voir aussi

[Accès à Business Central avec les licences Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configuration de l’accès avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
