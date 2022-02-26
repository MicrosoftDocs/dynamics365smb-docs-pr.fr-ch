---
title: Créer des factures d’acompte
description: Traitez les situations où votre fournisseur ou vous-même exigez un acompte. Utilisez les pourcentages par défaut pour chaque ligne vente ou achat, ou ajustez le montant en fonction si nécessaire.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: ebce3f22b4977b9dfca506ce536abb8c7e5ad46b
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972033"
---
# <a name="create-prepayment-invoices"></a>Créer des factures d’acompte

Si vous demandez à vos clients de soumettre le paiement avant de leur expédier une commande, vous pouvez utiliser la fonctionnalité d’acompte. Il en va de même si votre fournisseur vous demande de soumettre un paiement avant de vous expédier une commande.  

Vous pouvez lancer le traitement de l’acompte lorsque vous créez une commande vente ou achat. Si vous avez un pourcentage acompte par défaut pour un article donné sur la commande ou pour le client ou fournisseur, celui-ci sera automatiquement inclus dans la facture acompte résultante. Vous pouvez également spécifier un pourcentage acompte pour l’ensemble du document.

Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte. Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou ajuster le montant en fonction si nécessaire. Par exemple, vous pouvez spécifier un montant total pour la facture entière.  

La procédure suivante décrit comment facturer un acompte pour une commande vente. La procédure est identique pour des commandes achat.  

## <a name="to-create-a-prepayment-invoice"></a>Pour créer une facture acompte

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Créez une commande vente pour le client approprié. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  

    Sur le raccourci **Acompte**, le champ **% acompte** spécifie le pourcentage à utiliser pour calculer le montant acompte. Si un pourcentage d’acompte par défaut figure sur la fiche client, le champ est renseigné automatiquement. Vous pouvez modifier le pourcentage. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Choisissez le champ **Compresser acompte** si vous souhaitez créer des lignes sur la facture d’acompte qui combinent des lignes de la commande client si :  

    - Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.  
    - Elles sont les mêmes dimensions.  

    Si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d’acompte est associé, alors ne choisissez pas le champ **Compresser acompte**.  

    La date d’échéance de l’acompte est calculée automatiquement en fonction de la valeur du **Code conditions paiement acompte**.

3. Renseignez les lignes vente.  

    Si vous avez spécifié un pourcentage acompte par défaut soit pour le client, soit sur le raccourci **Acompte** sur ce document, cette valeur est copiée sur chaque ligne. Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.  

    > [!TIP]
    > Si vous ne voyez pas le champ **% acompte**, vous pouvez l’ajouter via la personnalisation.  Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

4. Pour visualiser le montant d’acompte total, choisissez l’action **Statistiques**.

    Pour ajuster le montant d’acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la page **Statistiques commande vente**.  

    Si le champ **Prix TVA comprise** est sélectionné, le champ **Montant acompte TTC** est modifiable.  

    Si vous modifiez la valeur du champ **Montant acompte**, le montant est réparti de façon proportionnelle entre toutes les lignes, à l’exception de celles qui contiennent la valeur **0** dans le champ **% acompte**.  

5. Pour effectuer une impression test avant de valider la facture d’acompte, sélectionnez l’action **Acompte**, puis choisissez **Impression test acompte**.  
6. Pour valider la facture d’acompte, sélectionnez l’action **Acompte**, puis l’action **Valider facture acompte**.  

    Pour valider et imprimer la facture acompte, choisissez l’action **Valider et imprimer facture acompte**.  

Vous pouvez émettre des factures acompte supplémentaires pour la commande. Pour ce faire, augmentez le montant d’acompte sur une ou plusieurs lignes, ajustez la date document si nécessaire, puis validez la facture acompte. Une nouvelle facture est créée pour la différence entre les montants d’acompte facturés et le nouveau montant d’acompte.  

> [!NOTE]  
> Si vous êtes situé en Amérique du Nord, vous ne pouvez pas modifier le pourcentage d’acompte après la facture acompte validée. Cela est empêché dans la version nord\-américaine de [!INCLUDE[prod_short](includes/prod_short.md)], car le calcul de la taxe sur les ventes est sinon incorrect.  

 Lorsque vous êtes prêt à valider le reste de la facture, validez-le comme n’importe quelle facture. Le montant d’acompte est automatiquement déduit du montant dû.  

## <a name="see-also"></a>Voir aussi

[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d’acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Personnaliser votre espace de travail](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]