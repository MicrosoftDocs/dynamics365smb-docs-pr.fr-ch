---
title: Paramétrer les prix de vente spéciaux et les remises client | Microsoft Docs
description: Décrit comment définir les accords secondaires de tarifs et de remises à appliquer aux documents vente lors de la vente à différents clients.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d358afec4689a3543245295427d5fae992dd680
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436791"
---
# <a name="record-special-sales-prices-and-discounts"></a>Enregistrer les prix de vente spéciaux et les remises
> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé des processus rationalisés pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Vous devez définir les accords de prix et de remise qui s’appliquent lors de la vente à des clients de sorte que les valeurs et règles convenues s’appliquent aux documents vente.

Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[prod_short](includes/prod_short.md)] s’assure que votre marge pour l’article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article. Pour plus d’informations, voir [Calcul du meilleur prix](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

En ce qui concerne les prix, un prix de vente spécial peut être inséré sur les lignes vente s’il existe une certaine combinaison de client, d’article, de quantité minimum, d’unité de mesure ou de date de début/date de fin. Pour plus d’informations, consultez les sections [Pour définir un prix de vente pour un client](#to-set-up-a-sales-price-for-a-customer) et [Calcul du meilleur prix](#best-price-calculation).  

En ce qui concerne les remises, vous pouvez définir et utiliser deux types de remises vente :

| Type de remise | Description |
| --- | --- |
| **Remise ligne vente** |Une remise sous forme de montant insérée sur les lignes vente s’il existe une certaine combinaison de client, d’article, de quantité minimum, d’unité de mesure ou de date de début/date de fin. Cela fonctionne de la même manière que pour les prix de vente. |
| **Remise facture** |Pourcentage de remise qui est soustrait du total du document vente si la somme de toutes les lignes du document dépasse un montant minimal donné. |

Dans la mesure où les prix de vente et les remises ligne vente sont basés sur une combinaison article/client, vous pouvez également mettre en œuvre cette configuration à partir de la page article de l’article auquel les règles et valeurs s’appliquent.

> [!TIP]  
> Si un article ne doit jamais être vendu avec une remise, laissez les champs de remise de la page article vides, et n’incluez pas l’article dans un quelconque paramétrage de remise ligne.

**Type d’application** et **N° doc. lettrage.** Les champs vous permettent de choisir à quoi cette liste de prix s’appliquera, par exemple au groupe prix client ou au client. À l’aide de **Afficher les colonnes pour**, vous pouvez afficher ou masquer les colonnes pertinentes pour la définition des prix, des remises ou des prix et remises.

Vous pouvez configurer des lignes de liste de prix manuellement, ou vous pouvez utiliser, par exemple, l’action **Proposer lignes** pour créer de nouveaux prix pour les articles sélectionnés, les groupes remises article, les ressources et d’autres types de produits. Si vous choisissez Proposer lignes, la page Lignes de prix - Créer un nouveau vous permet de définir des filtres pour sélectionner les produits pour lesquels vous souhaitez créer de nouvelles lignes de prix. Vous pouvez également indiquer s’il faut prendre en compte une quantité minimale lors du calcul des prix, le facteur d’ajustement à appliquer pour les nouvelles lignes de liste de prix et la méthode d’arrondi à appliquer aux prix. L’action **Copier les lignes** vous permet de copier les lignes de liste de prix existantes entre les listes de prix.

Par défaut, l’état des nouvelles listes de prix est Brouillon. Lorsque vous avez terminé d’ajouter des lignes et que vous souhaitez que le moteur de calcul de prix les inclue, vous pouvez remplacer le statut par Actif.

Pour consulter les listes de prix et les prix qui s’appliquent à des clients ou fournisseurs spécifiques, sur la page **Client**, choisissez l’action **Listes de prix vente** ou, sur la page **Fournisseur**, choisissez **Listes de prix achat**. Vous pouvez afficher les lignes de liste de prix de plusieurs listes de prix en choisissant **Prix de vente** ou **Prix d’achat** sur les pages **Article** et **Ressource**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Pour définir un prix de vente pour un client

Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**.  

#### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience/)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Prix**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde un prix de vente spécial au client.

#### <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience/)  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Listes prix vente**. 
3. Sélectionnez **Nouveau** pour créer une liste prix vente.
4. Sur les raccourcis **Général** et **Taxes**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Pour ajouter des éléments à la liste, effectuez l’une des opérations suivantes :
   * Pour ajouter de nombreux éléments, choisissez **Proposer lignes**, puis entrez des critères de filtre pour spécifier les types d’éléments à ajouter. Si vous le souhaitez, vous pouvez également saisir des paramètres supplémentaires pour les articles spécifiques à la liste de prix. Si nécessaire, vous pouvez les modifier ultérieurement.
   * Pour copier des articles d’une autre liste de prix, choisissez **Copier lignes**, puis choisissez la liste de prix à copier.
   * Pour ajouter des éléments manuellement, dans la grille, dans le champ **Type de produit**, choisissez le type de produit auquel la liste de prix est destinée. En fonction de votre sélection, renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Pour commencer à utiliser la liste de prix, dans le champ **Statut**, choisissez **Actif**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Remises facture vente et frais forfaitaires
Lorsque vous utilisez des remises facture, le montant total de la facture détermine celui de la remise accordée. Dans la page **Remises facture client**, vous pouvez également ajouter des frais forfaitaires aux factures supérieures à un montant donné.  

Pour pouvoir utiliser les remises facture avec les ventes, vous devez spécifier certaines informations. Vous devez décider ce qui suit :  

- les clients qui se verront accorder ce type de remise  
- les pourcentages de remise à utiliser  

Sur la page **Paramètres ventes**, vous pouvez spécifier si les remises facture doivent être calculées automatiquement.  

Pour chaque client, vous pouvez indiquer si vous accordez des remises facture si la condition est remplie (si le montant facture est suffisamment élevé). Vous pouvez définir des conditions pour les remises facture en devise société pour les clients nationaux et en devise pour les clients étrangers.  

Vous pouvez associer les pourcentages remise à des montants de facture spécifiques sur la page **Remises facture client** pour chaque client. Vous pouvez entrer le nombre de pourcentages de votre choix. Chaque client peut avoir sa propre page, ou vous pouvez lier plusieurs clients à la même page.  

En plus du pourcentage de remise (ou à sa place), vous pouvez lier un montant de frais forfaitaires au montant d’une facture.  

> [!TIP]  
> Avant de saisir ces informations, il est conseillé de préparer la structure de la remise que vous souhaitez utiliser. Ainsi, vous pouvez visualiser plus facilement les clients pouvant être liés à la même page de remise facture. Plus le nombre de pages à configurer est faible, plus vous pouvez saisir rapidement les informations de base.

Pour la formation sur les remises sur les ventes, voir [Configurer des remises pour vos clients](/learn/modules/customer-discounts-dynamics-365-business-central/index) sur Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcul de remises facture pour des ventes

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Pour définir une remise ligne vente pour un client
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. 

#### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience/)  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la fiche client appropriée, puis sélectionnez l’action **Remises ligne**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde une remise ligne vente au client.

> [!Note]
> Lorsque vous ouvrez les pages **Prix de vente** et **Remises ligne vente** à partir d’un client spécifique, les champs **Filtre type vente** et **Filtre code vente** sont définis pour le client et ne peuvent pas être modifiés ou supprimés.
>
> Pour configurer des prix ou des remises ligne pour tous les clients, un groupe de prix client ou une campagne, vous devez ouvrir les pages à partir d’une fiche article. Sinon, pour les prix de vente, utilisez la page **Feuille prix vente**. Pour plus d’informations, voir [Mettre à jour en bloc des prix d’articles](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience/)  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Listes prix vente**.
3. Ouvrez la liste de prix pour laquelle vous souhaitez spécifier la remise ligne.
4. Activez le bouton bascule **Autoriser remise ligne**.
5. Créez une nouvelle ligne ou choisissez une ligne existante, puis remplissez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Dans le champ **Définit**, choisissez soit **Prix et remise**, ou juste **Remise**. 
7. Dans le champ **% remise ligne**, spécifiez le pourcentage remise.

    > [!TIP]
    > Si vous modifiez une ligne existante, vous pouvez filtrer les lignes en choisissant l’option appropriée dans le champ **Afficher les colonnes pour**.

    > [!NOTE]  
    > Les codes remise facture sont représentés par les fiches client existantes. Cela vous permet d’affecter rapidement les conditions de remise facture aux clients en sélectionnant le nom d’un autre client qui bénéficie des mêmes conditions. Pour configurer des conditions de remise sur facture spécifiques au client, définissez le champ **Code remise facture** au code client du client, puis passez à l’étape suivante.

8. Sur la page **Fiche client**, sélectionnez l’action **Remises facture**. La page **Remises facture client** s’ouvre.
9. Dans le champ **Code devise**, indiquez le code d’une devise à laquelle s’appliquent les conditions de remise facture. Laissez le champ vide pour configurer des conditions de remise facture en devise société.
10. Sinon, dans le champ **Montant minimum**, entrez le montant minimal qu’une facture doit présenter pour faire l’objet de la remise.
11. Dans le champ **% remise**, entrez la remise facture sous la forme d’un pourcentage du montant de la facture.
12. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le client recevra une remise facture différente.

La remise facture est désormais configurée et affectée au client. Lorsque vous sélectionnez le code client dans le champ **Code remise facture** dans d’autres fiches client, la même remise facture est affecté à ces clients.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Pour configurer une remise facture pour un client
Une fois que vous avez décidé des clients pouvant faire l’objet de remises facture, entrez le code remise facture dans les fiches client et configurez les conditions de chaque code.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la page client d’un client pouvant faire l’objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le client. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Les codes remise facture sont représentés par les fiches client existantes. Cela vous permet d’affecter rapidement les conditions de remise facture aux clients en sélectionnant le nom d’un autre client qui bénéficie des mêmes conditions.

Configurez de nouvelles conditions de remise facture vente.

1. Sur la page **Clients**, sélectionnez l’action **Remises facture**. La page **Remises facture client** s’ouvre.
2. Dans le champ **Code devise**, indiquez le code d’une devise à laquelle s’appliquent les conditions de remise facture. Laissez le champ vide pour configurer des conditions de remise facture en devise société.
3. Dans le champ **Montant minimum**, entrez le montant minimal qu’une facture doit présenter pour faire l’objet de la remise.
4. Dans le champ **% remise**, entrez la remise facture sous la forme d’un pourcentage du montant de la facture.
5. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le client recevra une remise facture différente.

## <a name="to-copy-sales-prices"></a>Pour copier des prix de vente
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. 

#### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience/)  

Pour copier des prix de vente, comme les prix appliqués à un client et qui doivent être appliqués à tout un groupe de clients, vous devez lancer le traitement par lots **Suggérer prix vente**. traitement par lots sur la page **Feuille prix vente**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de prix de vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Suggérer prix vente** .  
3. Sur le raccourci **Prix vente**, renseignez les champs **Type vente** et **Code vente** avec les prix de vente d’origine à copier.  
4. Dans la partie supérieure de la page de demande, indiquez dans les champs **Type vente** et **Code vente** le type et le nom sous lesquels vous souhaitez copier les prix de vente.  
5. Pour que le traitement par lots crée des prix, activez la case à cocher **Créer nouveaux prix**.  
6. Choisissez le bouton **OK** pour renseigner les lignes de la page **Feuille prix vente** avec les nouveaux prix proposés, en précisant qu’ils sont applicables au type vente sélectionné.  

   > [!NOTE]  
   > Ce traitement par lots crée uniquement des propositions ; il n’effectue pas les modifications proposées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les insérer sur la page **Prix vente**, choisissez l’action **Implémenter des modifications de prix**, sur la page **Feuille prix vente**.

#### <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience/)  

Le statut de la liste de prix doit être **Brouillon**. 

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Listes de prix de vente**, puis sélectionnez le lien associé. 
2. Choisissez la liste de prix à copier, puis choisissez **Copier les lignes**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Vous ne pouvez pas avoir deux lignes ayant les mêmes paramètres mais des prix différents. Si cela se produit, un message s’affiche lorsque vous activez une liste de prix. Vous pouvez choisir le prix à utiliser en ouvrant la liste et en supprimant le prix incorrect.  
  
---

## <a name="to-bulk-update-item-prices"></a>Pour mettre à jour en bloc des prix d’articles
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. 

#### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience/)

Si vous souhaitez mettre à jour en bloc des prix article, tels que l’augmentation de tous les prix article par un certain pourcentage, vous devez exécuter **Suggérer prix article**. traitement par lots . Vous pouvez rechercher un lien vers le traitement par lots sur la page **Feuille prix vente**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de prix de vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Suggérer prix article** .  
3. Sur le raccourci **Article**, renseignez le champ **N°**, ou **Groupe comptabilisation de stock** ou d’autres champs avec les prix article d’origine à mettre à jour.  
4. Dans la partie supérieure de la page de demande, indiquez dans les champs **Type vente** et **Code vente** le type et le nom sous lesquels vous souhaitez copier les prix de vente.
5. Si vous souhaitez que le traitement par lots ajuste automatiquement le prix article proposés, saisissez l’ajustement dans le champ **Facteur appliqué**. Par exemple, vous devez entrer 1,15 dans **Facteur appliqué** pour une augmentation de 15 % des prix unitaires.  
6. Pour que le traitement par lots crée des prix, sélectionnez le champ **Créer nouveaux prix**.  
7. Choisissez le bouton **OK** pour renseigner les lignes de la page **Feuille prix vente** avec les nouveaux prix proposés, en précisant qu’ils sont applicables au l’**article** sélectionné.  

> [!NOTE]
> Ce traitement par lots crée uniquement des propositions ; il n’effectue pas les modifications proposées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les insérer dans la table **Prix vente**, vous pouvez utiliser le traitement par lots **Implémenter nouveaux prix**, accessible via l’onglet **Actions**, dans le groupe **Fonctions**, sur la page **Feuille prix vente**.

#### <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience/)

Pour mettre à jour les prix de plusieurs articles, vous devez créer une nouvelle liste de prix, puis copier les lignes d’une liste de prix existante. Lorsque vous copiez les lignes, vous pouvez utiliser des filtres pour spécifier les éléments à copier, et vous pouvez spécifier un nombre entier ou décimal dans le champ **Facteur appliqué** pour augmenter ou diminuer les prix. Le statut de la liste de prix doit être **Brouillon**. Si nécessaire, vous pouvez alors désactiver l’ancienne liste de prix.

> [!NOTE]
> Vous ne pouvez pas avoir deux lignes ayant les mêmes paramètres mais des prix différents. Si cela se produit, un message s’affiche lorsque vous activez une liste de prix. Vous pouvez choisir le prix à utiliser en ouvrant la liste et en supprimant le prix incorrect.  

---

## <a name="best-price-calculation"></a>Calcul du meilleur prix
Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[d365fin](includes/d365fin_md.md)] s’assure que votre marge pour l’article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article.

Le meilleur prix est le prix le plus bas autorisé associé à la remise de ligne la plus élevée autorisée à une date donnée. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automatiquement cette valeur lorsqu’il insère le prix unitaire et le pourcentage de remise de ligne pour des articles dans le nouveau document et les lignes feuille.

> [!NOTE]  
> Voici une description du calcul du meilleur prix pour la vente. Le calcul est le même pour les achats.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie la combinaison client facturé et article, et calcule le prix unitaire applicable et le pourcentage remise de ligne à l’aide des critères suivants :

    - Ce client a-t-il un accord pour des prix ou des remises ou appartient-il à un groupe bénéficiant d’un tel accord ?
    - L’article ou le groupe remises article est-il sur la ligne incluse dans l’un ou l’autre de ces accords prix/remise ?
    - La date de commande (ou la date de validation pour la facture et l’avoir) est-elle comprise entre les dates de début et de fin de l’accord prix/remise ?
    - Un code unité est-il spécifié ? Si c’est le cas, [!INCLUDE[d365fin](includes/d365fin_md.md)] recherche des prix/remises possédant le même code unité, et des prix/remises sans code unité.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si des accords prix/remise s’appliquent à des informations sur le document ou la ligne feuille, puis insère le prix unitaire applicable et le pourcentage remise de ligne, à l’aide des critères suivants :

    - Existe-t-il une quantité minimum à respecter dans l’accord de prix/remises ?
    - Existe-t-il une exigence en matière de devise à respecter dans l’accord de prix/remises ? Si c’est le cas, le prix le plus bas et la remise de ligne la plus élevée pour cette devise sont insérés, même si la devise société permettrait d’offrir un meilleur prix. S’il n’existe aucun accord de prix/remise dans le code devise indiqué, [!INCLUDE[d365fin](includes/d365fin_md.md)] insère le prix le plus bas et la remise de ligne la plus élevée en devise société.

Si aucun prix spécial ne peut être calculé pour l’article de la ligne, alors soit le coût unitaire direct, soit le prix unitaire à partir de la fiche article est inséré.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]