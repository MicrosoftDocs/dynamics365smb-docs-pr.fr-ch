---
title: "Paramétrer les prix de vente spéciaux et les remises client | Microsoft Docs"
description: "Décrit comment définir les accords secondaires de tarifs et de remises à appliquer aux documents vente lors de la vente à différents clients."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 41558d6eec29a277db3cf8f156ae476faf315238
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Procédure : enregistrer les prix de vente spéciaux et les remises
Vous devez définir les différents accords de prix et de remise qui s'appliquent lors de la vente à différents clients de sorte que les valeurs et règles convenues s'appliquent aux documents vente crées pour les clients.

Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[d365fin](includes/d365fin_md.md)] s'assure que votre marge pour l'article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article. Pour plus d'informations, voir la section « Calcul du meilleur prix ».

En ce qui concerne les prix, un prix de vente spécial peut être inséré sur les lignes vente s'il existe une certaine combinaison de client, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin.

En ce qui concerne les remises, vous pouvez définir et utiliser deux types de remises vente :

| Type de remise | Description |
| --- | --- |
| **Remise ligne vente** |Une remise sous forme de montant insérée sur les lignes vente s'il existe une certaine combinaison de client, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin. Cela fonctionne de la même manière que pour les prix de vente. |
| **Remise facture** |Une remise en pourcentage qui est soustraite du total du document si la valeur de toutes les lignes d'un document vente dépasse un montant minimal donné. |

Dans la mesure où les prix de vente et les remises ligne vente sont basés sur une combinaison article/client, vous pouvez également mettre en œuvre cette configuration à partir de la fiche article de l'article auquel les règles et valeurs s'appliquent.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Pour définir un prix de vente pour un client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche client appropriée, puis sélectionnez l'action **Prix**.

    Le champ **Type vente** est prérempli avec la valeur **Client** et le champ **Code vente** est prérempli avec le numéro du client.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde un prix de vente spécial au client.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Pour définir une remise ligne vente pour un client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche client appropriée, puis sélectionnez l'action **Remises ligne**.

    Le champ **Type vente** est prérempli avec la valeur **Client** et le champ **Code vente** est prérempli avec le numéro du client.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde une remise ligne vente au client.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Pour configurer une remise facture pour un client
Une fois que vous avez décidé des clients pouvant faire l'objet de remises facture, entrez le code remise facture dans les fiches client et configurez les conditions de chaque code.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche client d'un client pouvant faire l'objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le client.

    > [!NOTE]  
>   Les codes remise facture sont représentés par les fiches client existantes. Cela vous permet d'affecter rapidement les conditions de remise facture aux clients en sélectionnant le nom d'un autre client qui bénéficie des mêmes conditions.

    Configurez de nouvelles conditions de remise facture vente.
4. Dans la fenêtre **Fiche client**, sélectionnez l'action **Remises facture**. La fenêtre **Remises facture client** s'ouvre.
5. Dans le champ **Code devise**, indiquez le code d'une devise à laquelle s'appliquent les conditions de remise facture. Laissez le champ vierge si vous souhaitez configurer des conditions de remise facture en USD.
6. Dans le champ **Montant minimum**, entrez le montant minimal qu'une facture doit présenter pour faire l'objet de la remise.
7. Dans le champ **% remise**, entrez la remise facture sous la forme d'un pourcentage du montant de la facture.
8. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le client recevra une remise facture différente.

La remise facture est désormais configurée et affectée au client concerné. Lorsque vous sélectionnez le code client dans le champ **Code remise facture** dans d'autres fiches client, la même remise facture est affecté à ces clients.

## <a name="sales-invoice-discounts-and-service-charges"></a>Remises facture vente et frais forfaitaires
Lorsque vous utilisez des remises facture, la valeur du montant de la facture détermine celle de la remise accordée.  

Dans la fenêtre **Remises facture client**, vous pouvez également ajouter des frais forfaitaires aux factures supérieures à un montant donné.  

Pour pouvoir utiliser les remises facture avec les ventes, vous devez saisir certaines informations dans le programme. Vous devez décider des éléments suivants  

- les clients qui se verront accorder ce type de remise  
- les pourcentages de remise à utiliser  

Dans la fenêtre Paramètres ventes, vous pouvez indiquer si vous souhaitez que le programme calcule automatiquement les remises facture.  

Pour chaque client, vous pouvez indiquer si vous accordez des remises facture si la condition est remplie (si le montant facture est suffisamment élevé). Vous pouvez définir des conditions pour les remises facture en devise société pour les clients nationaux et en devise pour les clients étrangers.  

Vous liez les pourcentages de remise à des montants de facture spécifiques dans les fenêtres **Remises facture client**. Vous pouvez entrer le nombre de pourcentages de votre choix dans chaque fenêtre. Chaque client peut avoir sa propre fenêtre, ou vous pouvez lier plusieurs clients à la même fenêtre.  

En plus du pourcentage de remise (ou à sa place), vous pouvez lier un montant de frais forfaitaires au montant d'une facture.  

> [!TIP]  
>  Avant de saisir ces informations dans le programme, il est conseillé de préparer la structure de la remise que vous souhaitez utiliser. Ainsi, vous pouvez visualiser plus facilement les clients pouvant être liés à la même fenêtre de remise facture. Plus le nombre de fenêtres à configurer est faible, plus vous pouvez saisir rapidement les informations de base.  

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
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
