---
title: Afficher le statut d'une synchronisation | Microsoft Docs
description: Découvrez comment afficher le statut d'un projet de synchronisation individuelle.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245700"
---
# <a name="view-the-status-of-a-synchronization"></a>Afficher le statut d'une synchronisation
Vous pouvez visualiser le statut des différents projets de synchronisation qui ont été exécutés pour l'intégration de [!INCLUDE[crm_md](includes/crm_md.md)]. Cela inclut les projets de synchronisation qui ont été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela est utile lors de la résolution des problèmes de synchronisation, car vous pouvez accéder aux détails sur les erreurs spécifiques qui se produisent.

### <a name="to-view-all-synchronization-issues"></a>Pour visualiser tous les problèmes de synchronisation
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation des données couplées**, puis sélectionnez le lien associé.
2. Sur la page **Erreurs de synchronisation des données couplées**, affichez la vue de tous les problèmes survenus lors de la synchronisation des données entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrez et triez les enregistrements dans la page par table, message d'erreur et sélectionnez des options telles que **Réessayer** ou **Supprimer le couplage** pour résoudre les problèmes tour à tour ou en bloc.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)
1. Ouvrez, par exemple, le client, l'article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.
2. Sélectionnez l'action **Journal de synchronisation** pour afficher le journal de synchronisation pour l'enregistrement sélectionné, par exemple, le client spécifique que vous avez synchronisé manuellement.

## <a name="see-also"></a>Voir aussi  
[Configuration de l'intégration de Dynamics 365 for Sales dans Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilisation de Dynamics 365 for Sales depuis Business Central](marketing-integrate-dynamicscrm.md)
