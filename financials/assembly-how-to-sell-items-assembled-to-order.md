---
title: "Procédure : Vente d'articles à assembler pour commande | Microsoft Docs"
description: "Si l'article est paramétré pour l'assemblage pour commande, alors l'article ne devrait pas être en stock, et doit être assemblé spécifiquement à une commande vente. Lorsque vous entrez l'article dans une ligne commande vente, un ordre d'assemblage est automatiquement créé et lié à la commande vente."
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
ms.openlocfilehash: ca8cf74ca844b2ec0119497e79ccfc7cc7df5026
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="sell-items-assembled-to-order"></a>Vente d'articles à assembler pour commande
Si le champ **Stratégie d'assemblage** de la fiche article d'un élément d'assemblage est **Assembler pour commande**, alors l'article n'est pas supposé être en stock et doit être assemblé spécifiquement dans une commande vente. Lorsque vous entrez l'article dans une ligne commande vente, un ordre d'assemblage est automatiquement créé et lié à la commande vente.  

> [!NOTE]  
>  Si certains articles à assembler pour commande sont déjà en stock, vous pouvez déduire cette quantité de l'ordre d'assemblage et la réserver dans le stock. Pour plus d’informations, voir [Vente d'articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Dans cette procédure, vous effectuez la vente d'un article que vous assemblez selon les spécifications qui sont demandées par le client. Les étapes consistent à initier la ligne commande vente, personnaliser l'élément d'assemblage en modifiant ses composants et ressources, vérifier la disponibilité pour établir une date de livraison et lancer la commande vente à assembler et livrer immédiatement.  

> [!NOTE]  
>  La procédure suivante n'inclut pas les étapes standard de commande vente avant l'étape où vous entrez l'article à assembler pour commande dans une ligne commande vente.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Vendre un article qui est assemblé pour commande  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2.  Créez une commande client. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  
3.  Dans le champ **N°**, , entrez un article qui est configuré pour l'assemblage pour commande.  
4.  Dans le champ **Code magasin**, définissez le magasin à partir duquel l'article sera vendu. Le processus d'assemblage a lieu dans ce magasin.  
5.  Dans le champ **Quantité**, entrez le nombre d'unités à vendre.  

    > [!NOTE]  
    >  Si un ou plusieurs composants de la quantité d'éléments d'assemblage demandée ne sont pas disponibles, une fenêtre détaillée d'avertissement de disponibilité s'ouvre. Pour plus d'informations, voir Disponibilité assemblage.  

    Un ordre d'assemblage est maintenant automatiquement créé et est lié à la ligne commande vente. La date d'échéance de cet ordre d'assemblage est synchronisée avec la date d'expédition de la ligne commande vente.  

    La quantité à vendre est copiée dans le champ **Quantité à assembler pour commande**, ce qui indique que d'après la configuration la quantité totale de la ligne vente doit être assemblée à la commande. Vous pouvez réduire la quantité à assembler pour commande, par exemple si vous savez que certains articles sont déjà disponibles. Pour plus d’informations, voir [Vente d'articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Pour indiquer que le client souhaite un article supplémentaire dans un kit, sur le raccourci **Lignes**, sélectionnez l'action **Ligne**, sélectionnez l'action **Assembler pour commande**, puis sélectionnez l'action **Lignes d'assemblage pour commande** pour visualiser et modifier les composants d'assemblage standard. Sinon, choisissez le champ **Quantité à assembler pour commande**.  
7.  Dans la fenêtre **Lignes d'assemblage pour commande**, créez une nouvelle ligne de type **Article** pour le contenu du kit supplémentaire demandé. La ligne représente un composant supplémentaire d'assemblage.  

    Vous pouvez également personnaliser la commande en augmentant la quantité d'un article standard dans le kit. Vous pouvez effectuer cette opération en augmentant la valeur du champ **Quantité par** de la ligne d'ordre d'assemblage spécifique.  

    > [!NOTE]  
    >  La fenêtre **Lignes d'assemblage pour commande** contient seulement les champs de base qu'un vendeur est supposé utiliser pour personnaliser la liste de composants, ajouter des numéros de traçabilité ou pour résoudre des problèmes de disponibilité des composants. Pour plus d'informations en matière d'ordre d'assemblage, telles que la date de début d'ordre d'assemblage, choisissez l'action **Afficher documents**. Ceci ouvre l'affichage complet de l'ordre d'assemblage lié à la ligne commande vente. Vous ne pouvez pas modifier les contenus de la plupart des champs de l'en-tête d'ordre d'assemblage et vous ne pouvez pas valider les résultats d'assemblage parce que vous devez utiliser la validation d'expédition de la ligne commande vente.  
    >   
    >  Sur l'en-tête des ordres d'assemblage associé, seul le champ **Date début** peut être modifié pour permettre aux employés d'assemblage de spécifier une date antérieure à la date d'échéance lorsqu'ils commencent le processus. Tous les champs des lignes de l'ordre d'assemblage associé peuvent être modifiés afin que les magasiniers puissent entrer les chiffres de consommation pendant le processus.  

8.  Examinez les problèmes de disponibilité des composants ou réagissez face à eux. Par exemple, sélectionnez un article de substitution disponible ou définissez une date d'échéance ultérieure.  
9. Fermez la fenêtre **Lignes d'assemblage pour commande**. L'ordre d'assemblage lié est maintenant prêt à commencer à assembler les articles personnalisés au plus tard à la date d'échéance.  
10. Sur la commande vente, choisissez l'action **Lancer** pour informer le département d’assemblage que le processus d’assemblage peut démarrer.  
11. Dans le département d'assemblage, suivez la procédure d'assemblage des articles qui sont vendus au cours de cette procédure. Pour plus d'informations, voir [Assembler des articles](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Voir aussi  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

