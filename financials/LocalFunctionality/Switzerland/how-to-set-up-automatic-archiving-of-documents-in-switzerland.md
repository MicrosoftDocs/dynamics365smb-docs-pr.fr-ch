---
title: "Procédure : Paramétrer l'archivage automatique des documents en Suisse"
description: Vous pouvez configurer l'archivage automatique des documents vente et achat, tels que des devis ou des commandes ouvertes, avant de supprimer des documents.
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
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 09fca5cba94bed83b862cd8bb9d4b5be895c509d
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-automatic-archiving-of-documents-in-switzerland"></a>Paramétrer l'archivage automatique des documents en Suisse
Vous pouvez configurer l'archivage automatique des documents vente et achat, tels que des devis ou des commandes ouvertes, avant de supprimer des documents.  

La procédure suivante décrit comment configurer l'archivage automatique des documents vente, mais les mêmes étapes s'appliquent également aux documents achat.  

## <a name="to-set-up-automatic-archiving-of-documents"></a>Pour configurer l'archivage automatique des documents  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône"), entrez **Paramètres ventes**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **Paramètres &ventes**, sur le raccourci **Archivage**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Archivage des devis**|**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés.<br /><br /> -ou-<br /><br /> **Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés.<br /><br /> -ou-<br /><br /> **Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.|  
    |**Archivage des commandes vente ouvertes**|Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.|  
    |**Arch. commandes et retours**|Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.|  
    |**Journal interaction automatique**|Sélectionnez cette option pour créer automatiquement une écriture pour le contact dans le journal interaction lorsqu'une commande vente ou une livraison partielle est enregistrée ou lorsqu'un devis est converti en commande vente. **Remarque :** Ce champ n'est pas disponible sur la page **Paramètres achats**.|  

3.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [Documents vente et Documents achat, Suisse](swiss-purchase-documents-and-sales-documents.md)   
 [Importer les codes postaux suisses](how-to-import-swiss-post-codes.md)   
 [Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [Imprimer les commandes achat et vente lors d'une validation par lots](how-to-print-sales-and-purchase-orders-during-batch-posting.md)

