---
title: "Procédure : Établissement d'un devis de vente Assembler pour commande | Microsoft Docs"
description: "Vous pouvez utiliser la gestion nomenclature d'assemblage pour personnaliser un élément d'assemblage sur la demande d'un client au cours du processus de vente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b91b8a0ee359c1dc8dc4507cade6b635dace644
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Établissement d'un devis de vente Assembler pour commande
Vous pouvez utiliser la gestion nomenclature d'assemblage pour personnaliser un élément d'assemblage sur la demande d'un client au cours du processus de vente. Pour plus d'informations, reportez-vous à [Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

Lorsque vous vendez tout autre type d'article, vous pouvez également créer un devis pour un élément d'assemblage personnalisé avant de le convertir en commande vente. Ce processus implique plusieurs étapes supplémentaires lorsque vous le comparez à la création d'un devis normal et il recourt à une variation d'un ordre d'assemblage associé, qui est un devis d'assemblage.

> [!NOTE]  
>  Comme tous les types de devis, les quantités sur les devis d'assemblage ne sont pas utilisées en termes de disponibilité, planification ou réservations.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Créer un devis pour un article à assembler pour commande  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Devis**, puis sélectionnez le lien connexe.  
2.  Créez une ligne devis avec une ligne pour un élément d'assemblage. Pour plus d'informations, voir [Créer des offres](sales-how-make-offers.md).  
3.  Dans le champ **Quantité à assembler pour commande**, entrez la quantité entière.

    > [!NOTE]  
    >  Vous ne devez pas établir un devis pour une quantité partielle. Par conséquent, vous devez entrer la même quantité que vous avez saisie dans le champ **Quantité** de la ligne devis.  

4.  Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande** et **Lignes d'assemblage pour commande**. Sinon, choisissez le champ **Quantité à assembler pour commande** sur la ligne.  
5.  Dans la fenêtre **Lignes d'assemblage pour commande**, vérifiez ou modifiez les lignes d'assemblage pour commande en fonction du devis demandé par le client. Des informations supplémentaires sont disponibles en choisissant **Afficher document** pour ouvrir la commande devis ouverte complète. Vous ne pouvez pas modifier le contenu de la plupart des champs, et vous ne pouvez pas valider.  
6.  Lorsque vous avez ajusté les lignes d'ordre d'assemblage en fonction du devis, fermez la fenêtre **Lignes d'assemblage pour commande** pour revenir à la fenêtre **Devis**.  
7.  Si le client accepte le devis, créez une commande vente pour l'élément d'assemblage qui a fait l'objet du devis. Pour plus d'informations, voir [Créer des offres](sales-how-make-offers.md). Le devis d'assemblage associé et toutes les personnalisations sont liées à cette nouvelle commande vente à préparer pour l'assemblage de l'article ou des articles à vendre.  

## <a name="see-also"></a>Voir aussi  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

