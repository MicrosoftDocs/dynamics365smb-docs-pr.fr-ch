---
title: Mise à niveau d'une intégration à Dynamics 365 Sales | Microsoft Docs
description: Découvrez comment préparer Dynamics 365 Business Central pour l'intégrer à Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410683"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Mise à niveau d'une intégration à Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] s'intègre à [!INCLUDE[d365fin](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d'autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même. S'il s'agit de votre toute première intégration, nous vous recommandons de l'effectuer au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Intégration à Common Data Service](admin-common-data-service.md).

Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez continuer à synchroniser les données à l'aide de votre configuration. Cependant, si vous mettez à niveau [!INCLUDE[d365fin](includes/d365fin_md.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] pour la réactiver. 

> [!NOTE]
> La reconnexion au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez. Par exemple, les mappages de table par défaut sont appliqués.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Pour mettre à niveau votre connexion afin d'utiliser Common Data Service
1. Ouvrez la page **Paramètres de la connexion Microsoft Dynamics 365**, puis choisissez le bouton bascule **Activer** pour désactiver votre connexion existante à [!INCLUDE[crm_md](includes/crm_md.md)].
2. Ouvrez la page **Paramétrage de la connexion Common Data Service**, puis choisissez le bouton bascule **Activer** pour activer la connexion.
  
   Après avoir activé la connexion CDS, la solution d'intégration de base Business Central CDS est déployée dans Common Data Service.
3. Désinstallez la solution Intégration de Microsoft Dynamics 365 Business Central de votre Dynamics 365 Sales en suivant la rubrique [Désinstaller ou supprimer une solution](/powerapps/developer/common-data-service/uninstall-delete-solution) 

4. Sur la page Paramètres de la connexion Microsoft Dynamics 365, choisissez le bouton bascule Activer pour activer la connexion à [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Après avoir activé la connexion Sales, la solution d'intégration Business Central est déployée dans Sales. Cela permet l'intégration à des entités dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.
5. Choisissez **Redéployer la solution d'intégration** pour installer et configurer la solution d'intégration Business Central mise à niveau.
6. Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d'intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Voir aussi
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Intégration à Common Data Service](admin-common-data-service.md)
