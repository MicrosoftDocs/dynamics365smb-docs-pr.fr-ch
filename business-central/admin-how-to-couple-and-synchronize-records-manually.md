---
title: Coupler et synchroniser manuellement des enregistrements | Microsoft Docs
description: Synchroniser un mappage de table d'intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de l'entité Dynamics 365 Sales qui sont couplées.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196678"
---
# <a name="couple-and-synchronize-records-manually"></a>Coupler et synchroniser manuellement des enregistrements
Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des enregistrements dans Common Data Service ou [!INCLUDE[crm_md](includes/crm_md.md)]. Le couplage d'enregistrements permet d'afficher les informations Common Data Service depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et vice-versa. Le couplage vous permet également de synchroniser les données entre les enregistrements. Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.

> [!Note]
> Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Common Data Service ou [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l'action **Configurer le couplage**. Si l'action est disponible, les applications sont connectées.   

## <a name="video-example"></a>Exemple vidéo

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Pour coupler un enregistrement  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  

    Vous pouvez également ouvrir la page de liste et sélectionner l'enregistrement à coupler.  

2.  Choisissez l'action **Configurer le couplage**.  
3.  Renseignez les champs, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record"></a>Pour synchroniser un enregistrement unique  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  
2.  Choisissez l'action **Synchroniser maintenant**.  
3.  Si un enregistrement peut être synchronisé dans une direction, sélectionnez l'option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l'enregistrement que vous souhaitez coupler. Par exemple, le formulaire Fiche Compte ou Fiche Contact.  
2.  Choisissez l'action **[!INCLUDE[d365fin](includes/d365fin_md.md)]** dans le ruban pour ouvrir et coupler l'enregistrement automatiquement.

> [!Note]
> Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l'option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur Bidirectionnelle ou À partir de la table d'intégration sur la page **Mappage de table d'intégration** pour l'enregistrement. Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Pour synchroniser plusieurs enregistrements  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la page de liste pour l'enregistrement, telle que Clients ou Contacts.  
2.  Sélectionnez l'enregistrement à synchroniser, puis l'action **Synchroniser maintenant**.  
3.  Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l'option qui affiche la direction, puis cliquez sur **OK**.  

## <a name="see-also"></a>Voir aussi  
[Utilisation de Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md)
