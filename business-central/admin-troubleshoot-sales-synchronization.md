---
title: Dépannage des erreurs de synchronisation | Microsoft Docs
description: Fournit des indications pour identifier et résoudre les erreurs de synchronisation.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304299"
---
# <a name="troubleshooting-synchronization-errors"></a>Résolution des erreurs de synchronisation
Il y a beaucoup de pièces mobiles impliquées dans l'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] avec [!INCLUDE[crm_md](includes/crm_md.md)], et parfois les choses ne se passent pas bien. Cette rubrique répertorie certaines des erreurs types qui se produisent et donne des indications sur la manière de les résoudre.

Les erreurs se produisent souvent à cause de quelque chose qu'un utilisateur a fait pour coupler des enregistrements ou parce que la configuration de l'intégration est fausse. Pour les erreurs liées aux enregistrements couplés, les utilisateurs peuvent les résoudre eux-mêmes. Ces erreurs sont causées par des actions telles que la suppression d'un enregistrement dans l'une des applications métier mais pas les deux, puis la synchronisation. Pour plus d'informations, voir [Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Les erreurs liées à la configuration de l'intégration nécessitent généralement l'attention de l'administrateur. Vous pouvez voir ces erreurs sur la page **Erreurs de synchronisation d'intégration**. Voici des exemples de problèmes classiques :  
  
* Les autorisations et les rôles attribués aux utilisateurs ne sont pas corrects.  
* Le compte administrateur a été spécifié en tant qu'utilisateur d'intégration.  
* Le mot de passe de l'utilisateur d'intégration est défini pour nécessiter une modification lorsque l'utilisateur se connecte.  
* Les taux de change pour les devises ne sont pas spécifiés dans l'une ou l'autre application.  
  
Vous devez résoudre manuellement les erreurs, mais la page vous aide de plusieurs manières. Par exemple :  

* Les champs **Source** et **Destination** peuvent contenir des liens vers l'enregistrement où l'erreur a été trouvée. Cliquez sur le lien pour ouvrir l'enregistrement et recherchez l'erreur.  
* Les actions **Supprimer les écritures ultérieures à 7 jours** et **Supprimer toutes les écritures** vont nettoyer la liste. En règle générale, vous utilisez ces actions après avoir résolu la cause d'une erreur affectant de nombreux enregistrements. Faites attention, cependant. Ces actions peuvent supprimer des erreurs toujours pertinentes.

## <a name="see-also"></a>Voir aussi
[Intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuration des comptes d'utilisateur pour intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)  
[Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md)  