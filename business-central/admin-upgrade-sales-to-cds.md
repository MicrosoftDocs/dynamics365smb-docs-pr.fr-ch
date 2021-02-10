---
title: Mise à niveau d’une intégration à Dynamics 365 Sales
description: Apprenez à déplacer votre intégration Dynamics 365 Business Central avec Dynamics 365 Sales à la dernière version.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6528a05d0d2b43d39f0f2fafa26d71b03d0d2511
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013732"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Mise à niveau d’une intégration à Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] s’intègre à [!INCLUDE[prod_short](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même. S’il s’agit de votre toute première intégration, nous vous recommandons de l’effectuer au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Intégration à Dataverse](admin-common-data-service.md).

Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez continuer à synchroniser les données à l’aide de votre configuration. Cependant, si vous mettez à niveau [!INCLUDE[prod_short](includes/prod_short.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] pour la réactiver. 

> [!NOTE]
> La reconnexion au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez. Par exemple, les mappages de table par défaut sont appliqués.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Pour mettre à niveau votre connexion afin d’utiliser Dataverse
1. Ouvrez la page **Paramétrage de la connexion Microsoft Dynamics 365**, puis désactivez le bouton bascule **Activé** pour se déconnecter de [!INCLUDE[crm_md](includes/crm_md.md)].
2. Ouvrez la page **Paramétrage de la connexion Dataverse**, puis choisissez le bouton bascule **Activé** pour activer la connexion à [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans Dataverse.
3. Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.
4. Sur la page **Configuration de la connexion Microsoft Dynamics 365**, choisissez le bouton bascule **Activé** pour activer la reconnexion à [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Cela permet l’intégration à des tables dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.
5. Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d’intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Voir aussi
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Intégration à Microsoft Dataverse](admin-common-data-service.md)
