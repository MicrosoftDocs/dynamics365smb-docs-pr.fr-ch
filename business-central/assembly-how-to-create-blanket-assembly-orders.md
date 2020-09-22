---
title: "Procédure : créer des ordres d'assemblage permanents | Microsoft Docs"
description: Créez des commandes vente en cours pour les éléments d'assemblage personnalisés avant d'effectuer régulièrement les commandes vente réelles en fonction du contrat commande ouverte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9a0f3c81aad31eb51d282479e56acbfc935bf1dd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786086"
---
# <a name="create-blanket-assembly-orders"></a>Création d'ordres d'assemblage permanents
Vous pouvez utiliser la gestion nomenclature d'assemblage pour personnaliser un élément d'assemblage sur la demande d'un client au cours du processus de vente. Pour plus d'informations, reportez-vous à [Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

 Comme pour tout autre type d'article, vous pouvez également créer des commandes ouvertes vente pour les éléments d'assemblage personnalisés avant d'effectuer régulièrement les commandes vente réelles en fonction du contrat commande ouverte. Ce processus implique plusieurs étapes supplémentaires lorsque vous le comparer à la création d'une commande ouverte classique et il recourt à une modification d'un ordre d'assemblage associé, qui est un ordre d'assemblage ouvert.

> [!NOTE]  
>  Comme toutes les commandes ouvertes, les quantités des ordres d'assemblage ouverts sont uniquement des prévisions et ne sont pas opérationnelles avant d'être converties en ordres d'assemblage réels. Par conséquent, la fonctionnalité commande, comme le calcul de disponibilité, la réservation et la traçabilité des articles, n'est pas active sur les ordres d'assemblage ouverts.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Pour créer un ordre d'assemblage ouvert pour un article à assembler pour commande  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes cadres vente**, puis sélectionnez le lien associé.  
2. Créez une commande vente ouverte avec une ligne pour un élément d'assemblage. Pour plus de détails, reportez-vous à la rubrique [Créer des commandes ouvertes vente](sales-how-to-create-blanket-sales-orders.md).  
3. Dans le champ **Qté vers Assembler pour commande** de la ligne d'ordre d'assemblage ouvert, saisissez la quantité entière.

    > [!NOTE]  
    >  Vous ne devez pas créer de contrats commande ouverte pour une quantité partielle. Par conséquent, vous devez entrer la même quantité que vous avez saisie dans le champ **Quantité** de la ligne commande ouverte vente.  

4. Choisissez l'action **Assembler pour commande**, puis choisissez l'action **Lignes Assembler pour commande**. Sinon, choisissez le champ **Quantité à assembler pour commande** sur la ligne.  
5. Sur la page **Lignes Assembler pour commande**, vérifiez ou modifiez les lignes d'ordre d'assemblage en fonction de l'accord commande ouverte que vous avez passé avec le client. Des informations supplémentaires sont disponibles en choisissant **Afficher document** pour ouvrir l'ordre d'assemblage permanent complet. Vous ne pouvez pas modifier le contenu de la plupart des champs, et vous ne pouvez pas valider.  
6. Lorsque vous avez ajusté les lignes d'ordre d'assemblage en fonction de l'accord commande ouverte, fermez la page **Lignes Assembler pour commande** pour revenir à la page **Commande ouverte vente**.  
7. Lorsque les clients souhaitent créer une commande vente en fonction de la commande ouverte vente convenue, créez une commande vente pour l'élément ou les éléments d'assemblage convenus. Pour plus de détails, reportez-vous à la rubrique [Créer des commandes ouvertes vente](sales-how-to-create-blanket-sales-orders.md).

L'ordre d'assemblage ouvert associé et toutes les personnalisations sont liées à cette nouvelle commande vente à préparer pour l'assemblage de l'article ou des articles à vendre.  

## <a name="see-also"></a>Voir aussi
[Créer des commandes vente ouvertes](sales-how-to-create-blanket-sales-orders.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[Stock](inventory-manage-inventory.md)  
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
