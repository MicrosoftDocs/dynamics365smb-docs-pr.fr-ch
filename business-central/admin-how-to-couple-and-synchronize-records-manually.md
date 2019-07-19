---
title: Coupler et synchroniser manuellement des enregistrements | Microsoft Docs
description: Synchroniser un mappage de table d'intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de l'entité Dynamics 365 for Sales qui sont couplés.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6d1248ac77208e382c5594af57335df6ff824630
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726782"
---
# <a name="couple-and-synchronize-records-manually"></a>Coupler et synchroniser manuellement des enregistrements
Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)]. Le couplage d'enregistrements permet d'afficher les informations [!INCLUDE[crm_md](includes/crm_md.md)] depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et vice-versa. Le couplage vous permet également de synchroniser les données entre les enregistrements. Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.

> [!Note]
> Le couplage et la synchronisation des données avec [!INCLUDE[crm_md](includes/crm_md.md)] sont disponibles uniquement si votre administrateur système a créé une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l'action **Configurer le couplage**. Si l'action est disponible, les applications sont connectées.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Pour coupler un enregistrement  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  

    Vous pouvez également ouvrir la page de liste et sélectionner l'enregistrement à coupler.  

2.  Choisissez l'action **Configurer le couplage**.  
3.  Renseignez les champs, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record"></a>Pour synchroniser un enregistrement unique  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  
2.  Choisissez l'action **Synchroniser maintenant**.  
3.  Si un enregistrement peut être synchronisé de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)] ou de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'option qui affiche la direction de la mise à jour des données, puis cliquez sur le bouton **OK**.  

## <a name="to-synchronize-multiple-records"></a>Pour synchroniser plusieurs enregistrements  
1.  Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la page de liste pour l'enregistrement, telle que Clients ou Contacts.  
2.  Sélectionnez l'enregistrement à synchroniser, puis l'action **Synchroniser maintenant**.  
3.  Si des enregistrements peuvent être synchronisés de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)] ou de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'option qui affiche la direction de la mise à jour des données, puis cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
[Utilisation de Dynamics 365 for Sales depuis Business Central](marketing-integrate-dynamicscrm.md)
