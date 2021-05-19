---
title: Mise à niveau d’une intégration à Dynamics 365 Sales
description: Apprenez à déplacer votre intégration Dynamics 365 Business Central avec Dynamics 365 Sales à la dernière version.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025823"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Mise à niveau d’une intégration à Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] s’intègre à [!INCLUDE[prod_short](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même. S’il s’agit de votre toute première intégration, nous vous recommandons de l’effectuer au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Intégration à Dataverse](admin-common-data-service.md).

Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez continuer à synchroniser les données à l’aide de votre configuration. Cependant, si vous mettez à niveau [!INCLUDE[prod_short](includes/prod_short.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] pour la réactiver. 

> [!NOTE]
> La reconnexion au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez. Par exemple, les mappages de table par défaut sont appliqués.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Pour mettre à niveau votre connexion afin d’utiliser Dataverse
1. Ouvrez la page **Paramétrage de la connexion Microsoft Dynamics 365**, puis désactivez le bouton bascule **Activé** pour se déconnecter de [!INCLUDE[crm_md](includes/crm_md.md)].
2. Ouvrez la page **Paramétrage de la connexion Dataverse**, puis choisissez le bouton bascule **Activé** pour activer la connexion à [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans Dataverse.
3. Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.
4. Sur la page **Configuration de la connexion Microsoft Dynamics 365**, choisissez le bouton bascule **Activé** pour activer la reconnexion à [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cela permet l’intégration à des tables dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.
5. Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.
6. Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d’intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!IMPORTANT]
   > En utilisant l′action **Utiliser le paramétrage de synchronisation par défaut**, les mappages de table d′intégration par défaut sont appliqués. Tous les mappages personnalisés sont remplacés. Pour conserver des mappages personnalisés, nous vous recommandons de les exporter vers Excel ou de discuter avec votre partenaire Microsoft des autres moyens permettant de conserver vos mappages personnalisés.    

## <a name="see-also"></a>Voir aussi
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Intégration à Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]