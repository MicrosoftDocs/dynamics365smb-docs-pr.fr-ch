---
title: Assembler des articles
description: Si le champ Système réappro. de la fiche client contient Assemblage, la méthode par défaut d’approvisionnement de l’article consiste à l’assembler à partir des composants définis.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: e9d53a6369e2955e0e097471e70cb83438540539
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607061"
---
# <a name="assemble-items"></a>Assembler des articles

Si le champ **Système réappro.** de la fiche client contient **Assemblage**, la méthode par défaut d’approvisionnement de l’article consiste à l’assembler à partir des composants définis et potentiellement par une ressource définie.  

Les composants et les ressources utilisés dans ce type d’élément d’assemblage doivent être définis dans une nomenclature d’assemblage. Pour plus d’informations, voir [Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md).

Les éléments d’assemblage peuvent être configurés pour deux processus d’assemblage différents :  

- Assembler pour stock.  
- Assembler pour commande.  

En règle générale, vous utilisez la fonction **Assembler pour stock** pour les articles que vous souhaitez assembler avant les ventes (par exemple, pour les préparer pour une campagne de kit et les conserver dans le stock jusqu’à ce qu’ils soient commandés). Ces articles sont généralement des articles standard tels que les kits emballés qui ne peuvent pas être personnalisés en fonction des demandes des clients.  

En règle générale, vous utilisez la fonction **Assembler pour commande** pour les articles que vous ne souhaitez pas stocker parce que vous comptez les personnaliser en fonction des demandes des clients ou parce que vous voulez réduire les frais de transport associés au stock en fournissant ces articles en temps voulu. Pour plus d’informations, reportez-vous à [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

Pour plus d’informations sur le paramétrage d’un élément d’assemblage, voir [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

Ces options de configuration sont les paramètres par défaut qui gèrent le traitement initial des ventes et les lignes d’ordre d’assemblage. Vous pouvez les ignorer et fournir l’élément d’assemblage de la manière la plus optimale lors du traitement d’une vente. Pour plus d’informations, consultez [Vente d’articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) et [Vente simultanée d’articles à assembler pour commande et d’articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Les composants d’assemblage sont gérés d’une manière spéciale dans les configurations entrepôt de base. Pour plus d’informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les prélèvements stock » dans [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).   

Dans cette procédure, vous allez créer et traiter un ordre d’assemblage pour des articles qui sont assemblés pour stock, autrement dit sans commande vente liée. Les étapes incluent le lancement de l’ordre d’assemblage, le traitement des éventuels problèmes de disponibilité des composants et la validation partielle du résultat d’assemblage.

## <a name="to-assemble-an-item"></a>Pour assembler un article

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Ordres d’assemblage**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**. La page **Nouvel ordre d’assemblage** s’ouvre.  
3.  Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Dans le champ **N° article**, sélectionnez l’élément d’assemblage à traiter. Le champ est filtré pour n’afficher que les articles qui sont configurés pour assemblage, ce qui signifie qu’une nomenclature d’assemblage leur est affectée.  
5.  Dans le champ **Quantité**, entrez le nombre d’unités de l’article que vous souhaitez assembler.  

    > [!NOTE]  
    >  Si un ou plusieurs composants ne sont pas disponibles afin de répondre à la quantité d’éléments d’assemblage saisie à la date d’échéance définie, la page **Disponibilité assemblage** s’ouvre automatiquement pour fournir des informations détaillées sur le nombre d’éléments d’assemblage pouvant être assemblés en fonction de la disponibilité des composants. Pour plus d’informations, voir [Voir la disponibilité des articles](inventory-how-availability-overview.md). Lorsque vous fermez la page, l’ordre d’assemblage est créé avec des alertes de disponibilité sur les lignes composant concernées.  

    Les lignes d’ordre d’assemblage sont remplies automatiquement avec le contenu de la nomenclature d’assemblage et les quantités de ligne en fonction de l’en-tête d’ordre d’assemblage.  

    > [!NOTE]  
    >  Si la page **Disponibilité assemblage** s’est ouverte au moment où vous avez renseigné l’en-tête d’ordre d’assemblage, chaque ligne d’ordre d’assemblage affectée contient **Oui** dans le champ **Alerte dispo.** avec un lien vers les informations de disponibilité détaillées. Pour plus d’informations, voir Vérifier disponibilité. Vous pouvez résoudre un problème de disponibilité des composants en reportant la date début, en remplaçant le composant par un autre article, ou en sélectionnant un substitut disponible s’il est défini.  

6.  Dans le champ **Quantité à assembler**, entrez le nombre d’unités de l’élément d’assemblage à valider comme production la prochaine fois que vous validerez l’ordre de assemblage. Cette quantité peut être inférieure à la valeur du champ **Quantité** pour refléter une validation partielle de production.  

    > [!NOTE]  
    >  Pour que la validation de la consommation des composants corresponde à la validation de la production d’éléments d’assemblage, les champs de quantité figurant dans les lignes d’ordre d’assemblage sont ajustées automatiquement au niveau de la valeur que vous entrez dans le champ **Quantité à assembler**.  
7.  Pour les lignes d’ordre d’assemblage de type **Article** ou **Ressource**, dans le champ **Quantité à consommer**, entrez le nombre d’unités à valider en tant qu’unités consommées la prochaine fois que vous validerez l’ordre de assemblage.
8.  Lorsque vous êtes entièrement ou partiellement prêt pour la validation, choisissez l’action **Valider**.  

    > [!NOTE]  
    >  Si des avertissements sont toujours présents dans des lignes ordre d’assemblage, la validation est bloquée. Un message sur le ou les composants en stock s’affiche.  

Une fois la validation réussie, l’élément d’assemblage est validé comme production dans le code magasin et le code emplacement potentiel qui sont définis sur l’ordre de assemblage. Pour les ordres d’assemblage créés manuellement, le magasin peut être copié à partir du champ de configuration **Emplacement par défaut pour les commandes**. Pour les flux d’assemblage pour commande, le code magasin peut être copié à partir de la ligne commande vente.  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
