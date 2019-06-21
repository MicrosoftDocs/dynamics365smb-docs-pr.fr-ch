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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620899"
---
# <a name="view-the-status-of-a-synchronization"></a>Afficher le statut d'une synchronisation
Vous pouvez visualiser le statut des différents projets de synchronisation qui ont été exécutés pour l'intégration de [!INCLUDE[crm_md](includes/crm_md.md)]. Cela inclut les projets de synchronisation qui ont été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela est utile lors de la résolution des problèmes de synchronisation, car vous pouvez accéder aux détails sur les erreurs spécifiques qui se produisent.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Pour afficher les problèmes de synchronisation des enregistrements couplés
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation des données couplées**, puis sélectionnez le lien associé.
2. La page **Erreurs de synchronisation des données couplées** affiche les problèmes qui se produisent lorsque vous avez synchronisé des enregistrements couplés. Vous pouvez filtrer et trier des enregistrements et effectuer des actions comme **Restaurer** ou **Supprimer des enregistrements** pour résoudre les problèmes un par un.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)
1. Ouvrez, par exemple, un client, un article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.
2. Choisissez l'action **Journal de synchronisation** pour afficher le journal de synchronisation pour un enregistrement sélectionné. Par exemple, un client spécifique que vous avez synchronisé manuellement.

## <a name="see-also"></a>Voir aussi  
[Configuration de l'intégration de Dynamics 365 for Sales dans Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilisation de Dynamics 365 for Sales depuis Business Central](marketing-integrate-dynamicscrm.md)
