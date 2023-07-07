---
title: Enregistrer les prix d’achat spéciaux et les remises
description: Vous pouvez définir des accords de prix et de remises différents ou secondaires et les lettrer dans les documents achat pour les fournisseurs.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="record-special-purchase-prices-and-discounts"></a>Enregistrer les prix d’achat spéciaux et les remises

> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé des processus rationalisés pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Vous devez définir les différents accords de prix et de remise qui s’appliquent lors d’achats effectués auprès de plusieurs fournisseurs de sorte que les valeurs et règles convenues s’appliquent aux documents achat créés à l’intention des fournisseurs.

Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[prod_short](includes/prod_short.md)] s’assure que votre marge pour l’article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article. Pour plus d’informations, voir [Calcul du meilleur prix](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

En ce qui concerne les prix, un prix d’achat spécial peut être inséré sur les lignes achat s’il existe une certaine combinaison de fournisseur, d’article, de quantité minimum, d’unité de mesure ou de date de début/date de fin.

En ce qui concerne les remises, vous pouvez définir et utiliser deux types de remises achat :

| Type de remise | Description |
| --- | --- |
| **Remise ligne achat** |Une remise sous forme de montant insérée sur les lignes achat s’il existe une certaine combinaison de fournisseur, d’article, de quantité minimum, d’unité de mesure ou de date de début/date de fin. Ce type fonctionne de la même manière que pour les prix d’achat. |
| **Remise facture** |Une remise en pourcentage qui est soustraite du total du document si la valeur de toutes les lignes d’un document achat dépasse un montant minimal donné. |

Dans la mesure où les remises ligne achat et les prix achat sont basés sur une combinaison article/fournisseur, vous pouvez également effectuer cette configuration à partir de la fiche article dans laquelle sont définies les règles et valeurs. Pour plus d’informations, reportez-vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Pour configurer un prix d’achat spécial pour un fournisseur

#### [Expérience actuelle](#tab/current-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l’action **Prix**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde une remise ligne achat.

#### [Nouvelle expérience](#tab/new-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Choisissez le fournisseur, puis sélectionnez l’action **Listes prix vente**.
3. Sélectionnez **Nouveau** pour créer une liste prix achat.
4. Sur les raccourcis **Général** et **Taxes**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Pour ajouter des éléments à la liste, effectuez l’une des opérations suivantes :
   * Pour ajouter de nombreux éléments, choisissez **Proposer lignes**, puis entrez des critères de filtre pour spécifier les types d’éléments à ajouter. Si vous le souhaitez, vous pouvez également saisir des paramètres supplémentaires pour les articles spécifiques à la liste de prix. Si nécessaire, vous pouvez les modifier ultérieurement.
   * Pour copier des articles d’une autre liste de prix, choisissez **Copier lignes**, puis choisissez la liste de prix à copier.
   * Pour ajouter des éléments manuellement, dans la grille, dans le champ **Type de produit**, choisissez le type de produit auquel la liste de prix est destinée. En fonction de votre sélection, renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Pour commencer à utiliser la liste de prix, dans le champ **Statut**, choisissez **Actif**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Pour configurer une remise ligne pour un fournisseur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l’action **Remises ligne**.

   Le champ **N° fournisseur** est prérempli avec le numéro du fournisseur.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde une remise ligne achat.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Pour configurer une remise facture pour un fournisseur

Une fois que vos fournisseurs vous ont informé des remises facture qu’ils accordent, entrez le code remise facture sur la fiche fournisseur et configurez les conditions pour chaque code.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur d’un fournisseur pouvant faire l’objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le fournisseur.

    > [!NOTE]  
    > Les codes remise facture sont représentés par les fiches fournisseur existantes. Cela vous permet d’affecter rapidement les conditions de remise facture aux fournisseurs en sélectionnant le nom d’autres fournisseurs qui bénéficient des mêmes conditions.

    Configurez de nouvelles conditions de remise facture pour les achats.
4. Sur la page **Fiche fournisseur**, sélectionnez l’action **Remises facture**. La page **Remises facture fournisseur** s’ouvre.
5. Dans le champ **Code devise**, indiquez le code d’une devise à laquelle s’appliquent les conditions de remise facture. Laissez le champ vierge si vous souhaitez configurer des conditions de remise facture en EUR.
6. Dans le champ **Montant minimum**, entrez le montant minimal qu’une facture doit présenter pour faire l’objet de la remise.
7. Dans le champ **% remise**, entrez la remise facture sous la forme d’un pourcentage du montant de la facture.
8. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le fournisseur recevra une remise facture différente.

La remise facture est désormais configurée et affectée au fournisseur concerné. Lorsque vous sélectionnez le code fournisseur dans le champ **Code remise facture** dans d’autres fiches fournisseur, la même remise facture est affecté à ces fournisseurs.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Pour sélectionner un principe de validation des remises à l’achat

Lorsque vous validez une facture achat qui comprend une ou plusieurs remises, vous pouvez choisir entre deux principes de validation des montants remise. Vous pouvez valider des remises indépendamment ou les soustraire des remises facture.  

Avant cela, vous devez avoir configuré les comptes nécessaires pour valider des montants remise dans le plan comptable. Vous devez également vérifier que vous avez entré les numéros de compte corrects dans les paramètres comptabilisation des champs **Compte remise ligne achat** et **Compte remise fact. achat**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres achat**, puis choisissez le lien associé.
2. Dans le champ **Comptabilisation remise**, sélectionnez l’un des principes de validation des remises suivants.

|**Principe de validation des remises**|**Remise facture**|**Remise ligne**|  
|------------------------------------|--------------------------|-----------------------|  
|**Toutes remises**|Validation séparée|Validation séparée|  
|**Remises facture**|Validation séparée|Soustraction|  
|**Remises ligne**|Soustraction|Validation séparée|  
|**Remises déduites**|Soustraction|Soustraction|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Remises facture achat et frais forfaitaires

Si vous avez défini des conditions pour les remises facture avec des fournisseurs, vous pouvez les saisir dans le système. Le programme peut ensuite calculer la remise lorsque vous renseignez une facture achat.  

Avant d’utiliser les remises facture pour les achats, vous devez spécifier les fournisseurs qui vous offriront les remises.  

Vous pouvez associer les pourcentages remise à des montants de facture spécifiques sur les pages **Remises facture fournisseur**. Vous pouvez entrer le nombre de pourcentages de votre choix sur chaque page. Chaque fournisseur peut disposer de sa propre page ou vous pouvez associer plusieurs fournisseurs à une même page.  

En plus du pourcentage de remise, vous pouvez lier un montant de frais forfaitaires au montant d’une facture.  

Vous pouvez définir des conditions pour les remises facture en devise société pour les fournisseurs nationaux et en devise pour les fournisseurs étrangers.  

Vous avez la possibilité de choisir si [!INCLUDE[prod_short](includes/prod_short.md)] doit calculer automatiquement les montants de facture pour les devis, les commandes ouvertes, les commandes, les factures ou les avoirs.  

> [!TIP]  
> Avant de saisir ces informations dans le programme, il est conseillé de préparer la structure de la remise à utiliser. Ainsi, vous pouvez visualiser plus facilement les fournisseurs pouvant être liés à la même page de remise facture. Plus le nombre de page à configurer est faible, plus vous pouvez saisir rapidement les informations de base.

## <a name="best-price-calculation"></a>Calcul du meilleur prix

Lorsque vous avez enregistré des prix spéciaux et des remises de ligne pour les ventes et les achats, [!INCLUDE[prod_short](includes/prod_short.md)] s’assure que votre marge pour l’article est toujours optimale en calculant automatiquement le meilleur prix dans les documents achat et vente, sur le projet et les lignes feuille article.

Le meilleur prix est le prix le plus bas autorisé associé à la remise de ligne la plus élevée autorisée à une date donnée. [!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement ce prix lorsqu’il insère le prix unitaire et le pourcentage de remise de ligne pour des articles dans le nouveau document et les lignes feuille.

> [!NOTE]  
> Voici une description du calcul du meilleur prix pour la vente. Le calcul est le même pour les achats.

1. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie la combinaison client facturé et article, et calcule le prix unitaire applicable et le pourcentage remise de ligne à l’aide des critères suivants :

    - Ce client a-t-il un accord pour des prix ou des remises ou appartient-il à un groupe bénéficiant d’un tel accord ?
    - L’article ou le groupe remises article est-il sur la ligne incluse dans l’un ou l’autre de ces accords prix/remise ?
    - La date de commande (ou la date de validation pour la facture et l’avoir) est-elle comprise entre les dates de début et de fin de l’accord prix/remise ?
    - Un code unité est-il spécifié ? Si c’est le cas, [!INCLUDE[prod_short](includes/prod_short.md)] recherche des prix/remises possédant le même code unité, et des prix/remises sans code unité.

2. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie si des accords prix/remise s’appliquent à des informations sur le document ou la ligne feuille, puis insère le prix unitaire applicable et le pourcentage remise de ligne, à l’aide des critères suivants :

    - Existe-t-il une quantité minimum à respecter dans l’accord de prix/remises ?
    - Existe-t-il une exigence en matière de devise à respecter dans l’accord de prix/remises ? Si c’est le cas, le prix le plus bas et la remise de ligne la plus élevée pour cette devise sont insérés, même si la devise société permettrait d’offrir un meilleur prix. S’il n’existe aucun accord de prix/remise dans le code devise indiqué, [!INCLUDE[prod_short](includes/prod_short.md)] insère le prix le plus bas et la remise de ligne la plus élevée en DS.

Si aucun prix spécial ne peut être calculé pour l’article de la ligne, alors soit le coût unitaire direct, soit le prix unitaire à partir de la fiche article est inséré.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/set-up-prices-discounts-dynamics-365-business-central/index) associée

## <a name="see-also"></a>Voir aussi

[Définition des achats](purchasing-setup-purchasing.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
