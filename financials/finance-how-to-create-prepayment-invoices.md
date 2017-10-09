---
title: "Procédure : créer des factures d'acompte | Microsoft Docs"
description: "Découvrez comment gérer les situations où votre fournisseur ou vous-même exigez un acompte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a>Procédure : créer des factures d'acompte
Si vous voulez que vos clients fassent des paiements avant de leur expédier une commande ou si votre fournisseur exige que vous fassiez un paiement avant de vous expédier une commande, vous pouvez utiliser la fonctionnalité Acompte.  

Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte. Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou ajuster le montant en fonction si nécessaire. Par exemple, vous pouvez spécifier un montant total pour la facture entière.  

La procédure suivante décrit comment facturer un acompte pour des commandes vente. La procédure est identique pour des commandes achat.  

## <a name="to-create-a-prepayment-invoice"></a>Pour créer une facture acompte  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2. Créez une commande vente. Pour en savoir plus, voir [Procédure : vendre des produits](sales-how-sell-products.md).  

    Sur le raccourci **Acompte** le champ **% acompte** est renseigné automatiquement si un pourcentage d'acompte par défaut figure sur la fiche client. Vous pouvez modifier le contenu du champ. Le pourcentage d'acompte est uniquement copié à partir de l'en-tête vers les lignes qui ne copient pas le pourcentage d'acompte par défaut à partir de l'article.  

    La sélection du champ **Compresser acompte** signifie que les lignes sont combinées sur la facture si :  
    - Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.  
    - Elles sont les mêmes dimensions.  

    Laissez le champ vide si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d'acompte est associé.  

3. Renseignez les lignes vente.  

    Si des pourcentages d'acompte par défaut ont été configurés pour vos articles, ils sont copiés automatiquement dans le champ **% acompte** sur la ligne. Sinon, le pourcentage d'acompte est copié à partir de l'en-tête. Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.  
4. Si vous voulez appliquer un pourcentage d'acompte à la commande entière, modifiez le champ **% acompte** dans l'en\-tête après avoir renseigné les lignes.  
5. Pour visualiser le montant d'acompte total, choisissez l'action **Statistiques**.

    Pour ajuster le montant d'acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la fenêtre **Statistiques commande vente**.  

    Si le champ **Prix TVA comprise** est sélectionné, le champ **Montant acompte TTC** est modifiable.  

    Si vous modifiez la valeur du champ **Montant acompte**, le montant est réparti de façon proportionnelle entre toutes les lignes, à l'exception de celles qui contiennent la valeur **0** dans le champ **% acompte**.  
6. Pour effectuer une impression test avant de valider la facture d'acompte, sélectionnez l'action **Acompte**, puis choisissez **Impression test acompte**.  
7. Pour valider la facture d'acompte, sélectionnez l'action **Acompte**, puis l'action **Valider facture acompte**.  

    Pour valider et imprimer la facture acompte, choisissez l'action **Valider et imprimer facture acompte**.  

Vous pouvez émettre des factures acompte supplémentaires pour la commande. Pour ce faire, augmentez le montant d'acompte sur une ou plusieurs lignes, ajustez la date document si nécessaire, puis validez la facture acompte. Une nouvelle facture est créée pour la différence entre les montants d'acompte facturés et le nouveau montant d'acompte.  

> [!NOTE]  
>  Si vous êtes situé en Amérique du Nord, vous ne pouvez pas modifier le pourcentage d'acompte après la facture acompte validée. Cela est empêché dans la version nord\-américaine de [!INCLUDE[d365fin](includes/d365fin_md.md)], car le calcul de la taxe sur les ventes est sinon incorrect.  

 Lorsque vous êtes prêt à valider le reste de la facture, validez-le comme n'importe quelle facture. Le montant d'acompte est automatiquement déduit du montant dû.  

## <a name="see-also"></a>Voir aussi  
[Facturation d'acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d'acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

