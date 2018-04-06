---
title: Comment restreindre et autoriser l'utilisation d'un enregistrement | Microsoft Docs
description: "Si vous souhaitez restreindre l'utilisation d'un enregistrement à certaines activités, par exemple, jusqu'à ce qu'il ait été approuvé, vous pouvez incorporer deux réponses de flux de travail dans un flux de travail qui contrôle l'utilisation de l'enregistrement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a>Restreindre et autoriser l'utilisation d'un enregistrement
Si vous souhaitez restreindre l'utilisation d'un enregistrement à certaines activités, par exemple, jusqu'à ce qu'il ait été approuvé, vous pouvez incorporer deux réponses de flux de travail dans un flux de travail qui contrôle l'utilisation de l'enregistrement. Une réponse de flux de travail limitera l'utilisation de l'enregistrement telle que définie par l'événement et les conditions du flux de travail. Une autre réponse de flux de travail autorisera l'utilisation de l'enregistrement telle que définie par l'événement et les conditions du flux de travail. Deux réponses existent dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] à cet effet : **Restreindre l'utilisation d'un enregistrement** et **Autoriser l'utilisation d'un enregistrement**.

> [!NOTE]  
>  La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] permet de restreindre la validation d'un enregistrement, son exportation pour paiement, et l'impression sous la forme d'un chèque. Pour prendre en charge d'autres restrictions, un partenaire Microsoft doit personnaliser le code de l'application.  

> [!NOTE]  
>  La fonctionnalité de flux de travail pour restreindre et autoriser l'utilisation d'un enregistrement n'est pas liée à la fonctionnalité de blocage de la validation d'un enregistrement d'article, de client et de fournisseur.

La procédure suivante explique comment restreindre la validation de commandes d'achat tant qu'elles n'ont pas été approuvées. Le nouveau flux de travail sera basé sur le modèle de Flux de travail approbation facture achat existant.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Pour créer une étape de flux de travail qui limite la validation de commandes d'achat non approuvées  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Flux de travail**, créez un flux de travail nommé Flux de travail approbation commande achat. Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  
3. Choisissez l'action **Copier à partir du modèle de flux de travail**.  
4. Cliquez sur le champ **Code flux de travail origine**, puis, dans la fenêtre **Modèles flux de travail**, sélectionnez le modèle Flux de travail approbation facture achat.  

     Remarquez que les deux premières étapes du flux de travail concernent la restriction, puis l'autorisation de l'utilisation des factures d'achat. Modifiez la condition d'événement de la première étape du nouveau flux de travail pour indiquer qu'il s'applique aux commandes d'achat.  
5. Dans le raccourci **Étapes du flux de travail**, cliquez sur le champ **Conditions d'événement**, puis, pour le filtre **Type document**, sélectionnez **Commande**.  
6. Modifiez, supprimez ou ajoutez d'autres étapes de flux de travail pour prendre en charge un processus entreprise qui commence par restreindre la validation des commandes achat non approuvées.  

## <a name="see-also"></a>Voir aussi  
[Créer des workflows](across-how-to-create-workflows.md)   
[Flux de travail](across-workflow.md)   

