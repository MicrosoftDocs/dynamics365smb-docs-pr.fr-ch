---
title: Afficher le statut des projets de synchronisation | Microsoft Docs
description: Apprenez à afficher l'état après la synchronisation des enregistrements couplés.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 06/13/2019
ms.author: bholtorf
ms.openlocfilehash: 8d7421d5fee1a6498c204730f873c3746aafc637
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726759"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Afficher le statut des projets de synchronisation
Utilisez la page **Erreurs de synchronisation de données couplées** pour afficher l’état des projets de synchronisation exécutés pour les enregistrements couplés dans une intégration [!INCLUDE[crm_md](includes/crm_md.md)]. Cela inclut les projets ayant été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, l'affichage de leur statut est utile lors du dépannage, car il vous donne accès à des informations détaillées sur les erreurs liées aux enregistrements couplés. En règle générale, ces types d'erreur sont provoqués par des actions de l'utilisateur, par exemple lorsque :  

* Deux personnes ont modifié le même enregistrement dans les deux applications professionnelles.
* Une personne a supprimé un enregistrement dans l'une des applications, mais pas les deux.

> [!Note]
> La page **Erreurs de synchronisation de données couplées** affiche des informations sur les projets liés aux enregistrements couplés. Si vous résolvez toutes les erreurs mais que les enregistrements ne sont toujours pas synchronisés, cela peut avoir quelque chose à voir avec un paramètre d'intégration. En règle générale, votre administrateur devra résoudre ces types d’erreurs.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Pour afficher et résoudre les erreurs de synchronisation des enregistrements couplés
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation des données couplées**, puis sélectionnez le lien associé.
2. La page **Erreurs de synchronisation des données couplées** affiche les problèmes qui se produisent lorsque vous avez synchronisé des enregistrements couplés. Le tableau suivant répertorie les actions que vous pouvez utiliser pour résoudre les problèmes un par un :

|Action|Description|
|----|----|
|**Supprimer le couplage**|Découple les enregistrements et ils ne seront plus synchronisés. Pour reprendre la synchronisation des enregistrements, vous devez les coupler à nouveau.|
|**Réessayer**|Pour chaque enregistrement dans lequel une erreur est détectée, la synchronisation est ignorée sauf si vous corrigez le problème manuellement. Un nouvel essai inclura l'enregistrement dans la prochaine synchronisation.|
|**Synchroniser**|L'application tentera de résoudre un conflit lorsqu'un enregistrement a été modifié dans les deux applications professionnelles. Vous pouvez choisir la version de l'enregistrement à utiliser dans les deux applications.|
|**Restaurer des enregistrements** et **Supprimer des enregistrements**|Celles-ci sont utiles lorsqu'un enregistrement a été supprimé dans l'une des applications. Supprimer les enregistrements supprime l'enregistrement dans l'application où il existe toujours. La restauration recrée l'enregistrement dans l'application où elle a été supprimée.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)
1. Ouvrez, par exemple, un client, un article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].
2. Choisissez l'action **Journal de synchronisation** pour afficher le journal de synchronisation pour un enregistrement sélectionné. Par exemple, un client spécifique que vous avez synchronisé manuellement.

## <a name="see-also"></a>Voir aussi  
[Configuration des comptes d'utilisateur pour intégration à Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilisation de Dynamics 365 for Sales depuis Business Central](marketing-integrate-dynamicscrm.md)
