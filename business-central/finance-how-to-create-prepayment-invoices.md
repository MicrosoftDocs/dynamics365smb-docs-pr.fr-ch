---
title: "Procédure : créer des factures d'acompte | Microsoft Docs"
description: Découvrez comment gérer les situations où votre fournisseur ou vous-même exigez un acompte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 43dd2b3a2a0fe6b7995db511bf9482b7102ed0ef
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183419"
---
# <a name="create-prepayment-invoices"></a>Créer des factures d'acompte
Si vous voulez que vos clients fassent des paiements avant de leur expédier une commande ou si votre fournisseur exige que vous fassiez un paiement avant de vous expédier une commande, vous pouvez utiliser la fonctionnalité Acompte.  

Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte. Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou ajuster le montant en fonction si nécessaire. Par exemple, vous pouvez spécifier un montant total pour la facture entière.  

La procédure suivante décrit comment facturer un acompte pour des commandes vente. La procédure est identique pour des commandes achat.  

## <a name="to-create-a-prepayment-invoice"></a>Pour créer une facture acompte  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Créez une commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  

    Sur le raccourci **Acompte** le champ **% acompte** est renseigné automatiquement si un pourcentage d'acompte par défaut figure sur la fiche client. Vous pouvez modifier le contenu du champ. Le pourcentage d'acompte est uniquement copié à partir de l'en-tête vers les lignes qui ne copient pas le pourcentage d'acompte par défaut à partir de l'article.  

    La sélection du champ **Compresser acompte** signifie que les lignes sont combinées sur la facture si :  
    - Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.  
    - Elles sont les mêmes dimensions.  

    Laissez le champ vide si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d'acompte est associé.  

3. Renseignez les lignes vente.  

    Si des pourcentages d'acompte par défaut ont été configurés pour vos articles, ils sont copiés automatiquement dans le champ **% acompte** sur la ligne. Sinon, le pourcentage d'acompte est copié à partir de l'en-tête. Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.  
4. Si vous voulez appliquer un pourcentage d'acompte à la commande entière, modifiez le champ **% acompte** dans l'en\-tête après avoir renseigné les lignes.  
5. Pour visualiser le montant d'acompte total, choisissez l'action **Statistiques**.

    Pour ajuster le montant d'acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la page **Statistiques commande vente**.  

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
