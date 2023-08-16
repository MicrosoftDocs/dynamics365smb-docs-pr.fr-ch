---
title: Valider par lots la consommation
description: 'Si la méthode consommation est définie sur Manuel, vous devez valider les composants manuellement à l’aide d’une feuille consommation.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: edupont
---
# Valider par lots la consommation de la production

Si le champ Méthode consommation indique **Manuelle**, utilisez une feuille consommation pour valider les composants manuellement.  

> [!NOTE]
> Si vous avez activé le champ **Prélèvement requis** sur la fiche magasin pour indiquer que le magasin requiert un traitement de prélèvement stock, vous ne devez pas utiliser ce traitement par lots. [!INCLUDE[prod_short](includes/prod_short.md)] gérera la consommation lorsque vous enregistrerez le prélèvement stock. Pour plus d’informations, voir [Prélever pour la fabrication dans les configurations d′entrepôt de base](warehouse-how-to-pick-for-production.md).  

Vous pouvez également configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour valider automatiquement (*consommer*) les composants lorsque vous lancez ou terminez des ordres de fabrication. Pour plus d’informations, voir [Activer la consommation en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md).

## Pour valider la consommation pour une ou plusieurs lignes ordre de fabrication

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille consommation**, puis choisissez le lien associé.  
2. Renseignez les champs en indiquant les données relatives à l’ordre de fabrication et à la consommation. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Utilisez l′action **Calculer consommation** pour générer les lignes feuilles des ordres de fabrication basés sur la production réelle (quantité de produits finis figurant dans l′état) ou sur la production prévue (quantité de produits finis que vous prévoyez de fabriquer).

    > [!NOTE]
    > Si vous avez configuré la fiche magasin pour exiger le traitement des prélèvements en entrepôt, seules les quantités déjà prélevées via une activité entrepôt peuvent être saisies dans le champ **Quantité** de la page **Feuille consommation**, pas la quantité calculée. Pour plus d’informations, consultez [Prélever pour la production ou l’assemblage dans les configurations de stockage avancées](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Choisissez l’action **Valider** pour valider la consommation. Les stocks associés sont réduits.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Voir aussi

[Production](production-manage-manufacturing.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
