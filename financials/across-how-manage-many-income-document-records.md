---
title: "Définir les documents originaux à afficher | Microsoft Docs"
description: "Ajustez la vue par défaut des documents entrants, tels que des factures électroniques, afin d'améliorer votre vue d'ensemble des enregistrements traités et non-traités."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="manage-many-incoming-document-records"></a>Gérer de nombreux enregistrements document entrant
Lors de la création ou du traitement des enregistrements document, le nombre de lignes dans la fenêtre **Documents entrants** peut croître de telle façon que vous perdez la vue d'ensemble. Par conséquent, vous pouvez définir les enregistrements de documents entrants sur Traité afin de les supprimer de la vue par défaut. Lorsque vous choisissez l'action **Afficher tout**, vous pouvez afficher les enregistrements traités et non traités.

> [!NOTE]  
>   Vous ne pouvez pas modifier les informations, joindre des fichiers, ni exécuter d'autres processus sur des enregistrements de documents entrants définis à Traité. Vous devez d'abord définir le paramètre à Non traité.

La case **Traité** est automatiquement cochée sur les champ est sélectionné sur les enregistrements de documents entrants qui ont été traités, mais vous pouvez également cocher ou décocher cette case manuellement. En fonction de votre processus entreprise, un enregistrement de document entrant peut être traité si un document connexe a été créé pour celui-ci ou qu'un fichier a été joint.

> [!NOTE]  
>   Lorsque vous ouvrez la fenêtre **Documents entrants** avec l'action **Mes documents entrants** sur le Tableau de bord, seuls les enregistrements de documents entrants non traités sont affichés par défaut. Dans cette rubrique, il s'agit de « la vue par défaut ».

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Pour supprimer les enregistrements de documents entrants de la vue par défaut
1. Dans la fenêtre **Documents entrants**, sélectionnez une ou plusieurs lignes pour les enregistrements de documents entrants que vous souhaitez supprimer de la vue par défaut.
2. Sélectionnez l'action **Défini sur Traité**.

    Les enregistrements de documents entrants sont supprimés de la vue par défaut, et la case **Traité** est sélectionnée sur les lignes correspondantes.

> [!NOTE]  
>   Vous pouvez également effectuer cette action pour un enregistrement spécifique dans la fenêtre **Fiche document entrant**.

## <a name="to-view-all-incoming-document-records"></a>Pour afficher tous les enregistrements de documents entrants
1. Dans la fenêtre **Documents entrants**, sélectionnez l'action **Afficher tout**.

Tous les enregistrements de documents entrants sont affichés, y compris ceux pour lesquels la case **Traité** n'est pas cochée.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Pour ajouter des enregistrements de documents entrants à la vue par défaut
1. Dans la fenêtre **Documents entrants**, sélectionnez l'action **Afficher tout**.
2. Sélectionnez un ou plusieurs lignes pour les enregistrements de documents entrants que vous souhaitez voir apparaître dans la vue par défaut.
3. Sélectionnez l'action **Défini sur Non traité**.  

> [!NOTE]  
>   Vous pouvez également effectuer cette action pour un enregistrement spécifique dans la fenêtre **Fiche document entrant**.

## <a name="see-also"></a>Voir aussi
[Traiter les documents entrants](across-process-income-documents.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

