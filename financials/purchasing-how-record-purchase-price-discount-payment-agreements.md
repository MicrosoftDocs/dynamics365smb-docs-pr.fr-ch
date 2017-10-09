---
title: "Paramétrer des tarifs et remises spéciaux et secondaires pour les fournisseurs | Microsoft Docs"
description: "Vous pouvez définir des accords de prix et de remises différents ou secondaires et les lettrer dans les documents achat pour les fournisseurs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 8f2d66064a2ab62cc8a0303b70cd1ae74517f8eb
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Procédure : enregistrer les prix d'achat spéciaux et les remises
Vous devez définir les différents accords de prix et de remise qui s'appliquent lors d'achats effectués auprès de plusieurs fournisseurs de sorte que les valeurs et règles convenues s'appliquent aux documents achat créés à l'intention des fournisseurs.

Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[d365fin](includes/d365fin_md.md)] s'assure que votre marge pour l'article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article. Pour plus d'informations, voir la section « Calcul du meilleur prix ».

En ce qui concerne les prix, un prix d'achat spécial peut être inséré sur les lignes achat s'il existe une certaine combinaison de fournisseur, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin.

En ce qui concerne les remises, vous pouvez définir et utiliser deux types de remises achat :

| Type de remise | Description |
| --- | --- |
| **Remise ligne achat** |Une remise sous forme de montant insérée sur les lignes achat s'il existe une certaine combinaison de fournisseur, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin. Cela fonctionne de la même manière que pour les prix d'achat. |
| **Remise facture** |Une remise en pourcentage qui est soustraite du total du document si la valeur de toutes les lignes d'un document achat dépasse un montant minimal donné. |

Dans la mesure où les remises ligne achat et les prix achat sont basés sur une combinaison article/fournisseur, vous pouvez également effectuer cette configuration à partir de la fiche article dans laquelle sont définies les règles et valeurs. Pour plus d'informations, reportez vous à [Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Pour configurer un prix d'achat spécial pour un fournisseur
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l'action **Prix**.

    Le champ **Type d'achat** est prérempli avec **Fournisseur** et le champ **Code achat** est prérempli avec le numéro du fournisseur.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde une remise ligne achat.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Pour configurer une remise ligne pour un fournisseur
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l'action **Remises ligne**.

    Le champ **Type d'achat** est prérempli avec **Fournisseur** et le champ **Code achat** est prérempli avec le numéro du fournisseur.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde une remise ligne achat.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Pour configurer une remise facture pour un fournisseur
Une fois que vos fournisseurs vous ont informé des remises facture qu'ils accordent, entrez le code remise facture sur la fiche fournisseur et configurez les conditions pour chaque code.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche fournisseur d'un fournisseur pouvant faire l'objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le fournisseur.

    > [!NOTE]  
>   Les codes remise facture sont représentés par les fiches fournisseur existantes. Cela vous permet d'affecter rapidement les conditions de remise facture aux fournisseurs en sélectionnant le nom d'autres fournisseurs qui bénéficient des mêmes conditions.

    Configurez de nouvelles conditions de remise facture pour les achats.
4. Dans la fenêtre **Fiche fournisseur**, sélectionnez l'action **Remises facture**. La fenêtre **Remises facture fournisseur** s'ouvre.
5. Dans le champ **Code devise**, indiquez le code d'une devise à laquelle s'appliquent les conditions de remise facture. Laissez le champ vierge si vous souhaitez configurer des conditions de remise facture en USD.
6. Dans le champ **Montant minimum**, entrez le montant minimal qu'une facture doit présenter pour faire l'objet de la remise.
7. Dans le champ **% remise**, entrez la remise facture sous la forme d'un pourcentage du montant de la facture.
8. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le fournisseur recevra une remise facture différente.

La remise facture est désormais configurée et affectée au fournisseur concerné. Lorsque vous sélectionnez le code fournisseur dans le champ **Code remise facture** dans d'autres fiches fournisseur, la même remise facture est affecté à ces fournisseurs.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Pour sélectionner un principe de validation des remises à l'achat  
Lorsque vous validez une facture achat qui comprend une ou plusieurs remises, vous pouvez choisir entre deux principes de validation des montants remise. Vous pouvez valider des remises indépendamment ou les soustraire des remises facture.  

Avant cela, vous devez avoir configuré les comptes nécessaires pour valider des montants remise dans le plan comptable. Vous devez également vérifier que vous avez entré les numéros de compte corrects dans les paramètres comptabilisation des champs **Compte remise ligne achat** et **Compte remise fact. achat**.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.
2. Dans le champ **Comptabilisation remise**, sélectionnez l'un des principes de validation des remises suivants.

|**Principe de validation des remises**|**Remise facture**|**Remise ligne**|  
|------------------------------------|--------------------------|-----------------------|  
|**Toutes remises**|Validation séparée|Validation séparée|  
|**Remises facture**|Validation séparée|Soustraction|  
|**Remises ligne**|Soustraction|Validation séparée|  
|**Remises déduites**|Soustraction|Soustraction|  

# <a name="purchase-invoice-discounts-and-service-charges"></a>Remises facture achat et frais forfaitaires
Si vous avez défini des conditions pour les remises facture avec des fournisseurs, vous pouvez les saisir dans le système. Le programme peut ensuite calculer la remise lorsque vous renseignez une facture achat.  

 Avant d'utiliser les remises facture pour les achats, vous devez spécifier les fournisseurs qui vous offriront les remises.  

 Vous pouvez associer les pourcentages remise à des montants de facture spécifiques dans les fenêtres **Remises facture fournisseur**. Vous pouvez entrer le nombre de pourcentages de votre choix dans chaque fenêtre. Chaque fournisseur peut disposer de sa propre fenêtre ou vous pouvez associer plusieurs fournisseurs à une même fenêtre.  

 En plus du pourcentage de remise, vous pouvez lier un montant de frais forfaitaires au montant d'une facture.  

 Vous pouvez définir des conditions pour les remises facture en devise société pour les fournisseurs nationaux et en devise pour les fournisseurs étrangers.  

 Vous avez la possibilité de choisir si [!INCLUDE[d365fin](includes/d365fin_md.md)] doit calculer automatiquement les montants de facture pour les devis, les commandes ouvertes, les commandes, les factures ou les avoirs.  

> [!TIP]  
>  Avant de saisir ces informations dans le programme, il est conseillé de préparer la structure de la remise à utiliser. Ainsi, vous pouvez visualiser plus facilement les fournisseurs pouvant être liés à la même fenêtre de remise facture. Plus le nombre de fenêtres à configurer est faible, plus vous pouvez saisir rapidement les informations de base.

## <a name="best-price-calculation"></a>Calcul du meilleur prix
Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[d365fin](includes/d365fin_md.md)] s'assure que votre marge pour l'article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article.

Le meilleur prix est le prix le plus bas autorisé associé à la remise de ligne la plus élevée autorisée à une date donnée. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automatiquement cette valeur lorsqu'il insère le prix unitaire et le pourcentage de remise de ligne pour des articles dans le nouveau document et les lignes feuille.

> [!NOTE]  
>   Voici une description du calcul du meilleur prix pour la vente. Le calcul est le même pour les achats.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie la combinaison client facturé et article, et calcule le prix unitaire applicable et le pourcentage remise de ligne à l'aide des critères suivants :

    - Ce client a-t-il un accord pour des prix ou des remises ou appartient-il à un groupe bénéficiant d'un tel accord ?
    - L'article ou le groupe remises article est-il sur la ligne incluse dans l'un ou l'autre de ces accords prix/remise ?
    - La date de commande (ou la date de validation pour la facture et l'avoir) est-elle comprise entre les dates de début et de fin de l'accord prix/remise ?
    - Un code unité est-il spécifié ? Si c'est le cas, [!INCLUDE[d365fin](includes/d365fin_md.md)] recherche des prix/remises possédant le même code unité, et des prix/remises sans code unité.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si des accords prix/remise s'appliquent à des informations sur le document ou la ligne feuille, puis insère le prix unitaire applicable et le pourcentage remise de ligne, à l'aide des critères suivants :

    - Existe-t-il une quantité minimum à respecter dans l'accord de prix/remises ?
    - Existe-t-il une exigence en matière de devise à respecter dans l'accord de prix/remises ? Si c'est le cas, le prix le plus bas et la remise de ligne la plus élevée pour cette devise sont insérés, même si la devise société permettrait d'offrir un meilleur prix. S'il n'existe aucun accord de prix/remise dans le code devise indiqué, [!INCLUDE[d365fin](includes/d365fin_md.md)] insère le prix le plus bas et la remise de ligne la plus élevée en DS.

Si aucun prix spécial ne peut être calculé pour l'article de la ligne, alors soit le coût unitaire direct, soit le prix unitaire à partir de la fiche article est inséré.

## <a name="see-also"></a>Voir aussi
[Définition des achats](purchasing-setup-purchasing.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

