---
title: Paramétrer les prix de vente et les remises client | Microsoft Docs
description: Décrit comment configurer et appliquer des accords de tarification et de remise pour les documents vente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5d03e3c567ed6a2932691cee58685e522814a03f
ms.sourcegitcommit: a6000804ad9a176de5750372d3951547ddb71006
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 11/25/2021
ms.locfileid: "7865561"
---
# <a name="record-sales-prices-and-discounts"></a>Enregistrer les prix de vente et les remises
> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé des processus rationalisés pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge diverses stratégies de tarification, allant des modèles à prix unique où un article est toujours vendu au même prix, aux accords de prix spéciaux avec des clients spécifiques, des groupes de clients ou des offres spéciales lorsque vous menez une campagne de vente. Par exemple, vous pouvez proposer un prix spécial sur une commande client dans les conditions suivantes :

* Pour une quantité minimale
* Pour un certain type d’article  
* En cas de création pendant une période spécifique

Pour utiliser un modèle de tarification de base, il vous suffit de spécifier un prix unitaire pour un article ou une ressource. Ce prix sera toujours utilisé sur les documents vente. Pour les modèles plus avancés, par exemple, lorsque vous lancez une campagne de vente et que vous souhaitez proposer des prix spéciaux, vous pouvez spécifier des critères pour cela sur la page **Prix de vente**. Vous pouvez proposer des prix spéciaux basés sur des combinaisons des éléments suivants : 

* Client
* Article ;
* Unité
* Quantité minimale
* Plages de dates qui définissent la validité des prix

De plus, après avoir défini des prix spéciaux, [!INCLUDE[prod_short](includes/prod_short.md)] peut calculer automatiquement le meilleur prix sur les documents vente et achat, et sur les lignes de travail et les feuilles articles. Pour plus d’informations, voir [Calcul du meilleur prix](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Pour les remises, vous pouvez définir et utiliser les types suivants :

| Type de remise | Description |
| --- | --- |
| **Remise ligne vente** |Montant utilisé sur les lignes vente s’il existe une certaine combinaison de client, d’article, de quantité minimale, d’unité ou de date de début et date de fin. Ces combinaisons fonctionnent de la même manière que pour les prix de vente. |
| **Remise facture** |Pourcentage de remise qui est soustrait du total du document vente si la somme de toutes les lignes du document dépasse un montant minimal donné. |

> [!TIP]  
> Si un article ne doit jamais être vendu avec une remise, laissez les champs de remise de la page article vides, et n’incluez pas l’article dans un quelconque paramétrage de remise ligne.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Pour définir un prix de vente pour un client

Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. Si la mise à jour des fonctionnalités n’est pas activée, suivez les étapes de l’onglet Expérience actuelle. 

## <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience)

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Prix**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde un prix de vente spécial au client.

## <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience)  
Par défaut, l’état des nouvelles listes de prix est Brouillon. Les projets de tarifs ne sont pas inclus dans les calculs de prix. Lorsque vous avez terminé d’ajouter des lignes et que vous souhaitez commencer à utiliser les prix, remplacez le statut par Actif.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Listes prix vente**. 
3. Sélectionnez **Nouveau** pour créer une liste prix vente.
4. Sur les raccourcis **Général** et **Taxes**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Il existe plusieurs méthodes pour ajouter des articles à la liste :
   * Pour ajouter de nombreux éléments, choisissez **Proposer lignes**, puis entrez des critères de filtre pour spécifier les types d’éléments à ajouter. Vous pouvez également saisir d’autres paramètres pour les articles. Ces paramètres sont spécifiques aux tarifs. Si nécessaire, vous pouvez les modifier ultérieurement.
   * Pour copier des articles d’une autre liste de prix, choisissez **Copier lignes**, puis choisissez la liste de prix à copier.
   * Pour ajouter des éléments manuellement, dans le champ **Type de produit** sur une ligne, choisissez le type de produit auquel les tarifs sont destinés. En fonction de votre sélection, renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Pour commencer à utiliser la liste de prix, dans le champ **Statut**, choisissez **Actif**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Utilisation des tarifs de vente et d’achat
> [!NOTE]
> L’utilisation des tarifs nécessite que votre administrateur ait activé la mise à jour de la fonctionnalité **Nouvelle expérience de prix de vente** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Les champs **Type d’application** et **N° doc. lettrage.** vous permettent de choisir à quoi des tarifs s’appliqueront, par exemple au groupe prix client ou au client. Utilisez le champ **Afficher les colonnes pour** pour afficher ou masquer les colonnes pertinentes uniquement pour les prix, les remises ou les prix et remises.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Conversion des prix existants lorsque vous activez la mise à jour de la fonctionnalité de tarification
Lorsque vous activez la mise à jour de la fonctionnalité **Nouvelle expérience de prix de vente** sur la page **Gestion des fonctionnalités**, le guide **Mise à jour des données de fonctionnalité** s’ouvre. Utilisez le bouton de basculement **Utiliser les prix par défaut** comme suit :

* Si vous souhaitez utiliser tous les prix sur une seule page, activez-le. Les prix existants sont convertis en une liste de prix par défaut pour chacun des éléments suivants :

    * Ventes
    * Achats
    * Ventes projet
    * Achats projet 

    Ensuite, vous pouvez modifier tous les prix pour ces zones sur la page **Feuille prix**. Les tarifs par défaut sont définis sur les pages **Configuration des ventes et des comptes clients**, **Paramètres ventes**, et **Paramètres projets**. 

    > [!NOTE]
    > Si les prix sont définis uniquement sur les fiches d’articles ou de ressources, les tarifs par défaut ne seront pas renseignés avec ces prix au moment de la mise à jour des données. Cependant, vous pouvez ouvrir l’une des listes de prix par défaut ou la page Feuille de calcul des prix et utiliser l’action **Suggérer des lignes** pour ajouter les prix fixés sur les fiches article ou ressource. 

* Pour utiliser les tarifs vente, désactivez-le. Les prix existants seront convertis en une nouvelle liste de prix pour chaque combinaison de client, groupe de clients ou campagne, ainsi que les dates de début et de fin, et les devises. Si vous disposez de plusieurs combinaisons, vous aurez plusieurs listes de prix.

Si vous avez déjà activé la nouvelle expérience de tarification, vous pouvez créer manuellement des tarifs par défaut ou spécifier une liste de prix existante par défaut. Pour définir une liste de prix existante par défaut, activez le bouton de basculement **Autoriser la mise à jour des valeurs par défaut** sur la liste de prix. Ensuite, sur les pages **Paramètres vente**, **Paramètres achats**, ou **Paramètres projets**, définissez les tarifs comme valeurs par défaut.

## <a name="editing-active-price-lists"></a>Modification des tarifs actifs
Pour permettre aux utilisateurs de modifier les prix sur les tarifs actifs pour les articles, les ressources, les clients, les fournisseurs ou d’autres entités qui utilisent la tarification, activez le bouton de basculement **Autoriser la modification du prix actif** sur les pages **Paramètres ventes** et **Paramètres achats**. 

Quand le bouton de basculement **Autoriser la modification du prix actif** est désactivé, pour mettre à jour les prix dans une liste de prix, vous devez changer le statut de la liste de prix sur **Brouillon**, effectuer votre modification, puis réactiver la liste de prix.

La page **Vue d’ensemble des prix** fournit un aperçu de tous les prix dans tous les tarifs. Vous pouvez définir des filtres pour affiner la liste. Après avoir modifié les prix, vous devez utiliser l’action **Vérifier les lignes** pour vérifier les prix par rapport à d’autres lignes de tarifs. Par exemple, la vérification des prix permet d’éviter les prix en double ou contradictoires. 

> [!NOTE]
> Lorsque vous modifiez une ligne dans une liste de prix active, le statut de la ligne devient Brouillon et la ligne ne sera pas incluse dans les calculs de prix tant que vous n’aurez pas utilisé l’action **Vérifier les lignes**. Après avoir vérifié le prix, le statut de la ligne devient Actif et il sera utilisé dans les calculs de prix.

Pour ajouter de nouveaux prix, sur la page **Vue d’ensemble des prix**, utilisez l’action **Ajouter de nouvelles lignes**. La page **Feuille de calcul des prix** s’ouvre, où vous ajoutez des lignes de prix des manières suivantes :

* En les proposant selon des critères
* En les copiant à partir d’autres listes de prix
* En les saisissant manuellement. 

Ensuite, vous pouvez utiliser l’action **Implémenter nouveaux prix** pour comparer les nouveaux prix à d’autres tarifs afin d’éviter les doublons.

## <a name="to-copy-sales-prices"></a>Pour copier des prix de vente
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. Si la mise à jour des fonctionnalités n’est pas activée, suivez les étapes de l’onglet Expérience actuelle.

## <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience)  

Pour copier des prix de vente, comme les prix appliqués à un client et qui doivent être appliqués à tout un groupe de clients, vous devez lancer le traitement par lots **Suggérer prix vente**. traitement par lots sur la page **Feuille prix vente**.  

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de prix de vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Suggérer prix vente** .  
3. Sur le raccourci **Prix vente**, renseignez les champs **Type vente** et **Code vente** avec les prix de vente d’origine à copier.  
4. Dans la partie supérieure de la page de demande, indiquez dans les champs **Type vente** et **Code vente** le type et le nom sous lesquels vous souhaitez copier les prix de vente.  
5. Pour que le traitement par lots crée des prix, activez la case à cocher **Créer nouveaux prix**.  
6. Choisissez le bouton **OK** pour renseigner les lignes de la page **Feuille prix vente** avec les nouveaux prix proposés, en précisant qu’ils sont applicables au type vente sélectionné.  

   > [!NOTE]  
   > Ce traitement par lots crée uniquement des propositions ; il n’effectue pas les modifications proposées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les insérer sur la page **Prix vente**, choisissez l’action **Implémenter des modifications de prix**, sur la page **Feuille prix vente**.

## <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience)  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Listes de prix de vente**, puis sélectionnez le lien associé. 
2. Choisissez la liste de prix à copier, puis choisissez **Copier les lignes**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Vous ne pouvez pas avoir deux lignes ayant les mêmes paramètres mais des prix différents. Si cela se produit, un message s’affiche lorsque vous activez une liste de prix. Vous pouvez choisir le prix à utiliser en ouvrant la liste et en supprimant le prix incorrect.  
  
---

## <a name="to-bulk-update-item-prices"></a>Pour mettre à jour en bloc des prix d’articles
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. Si la mise à jour des fonctionnalités n’est pas activée, suivez les étapes de l’onglet Expérience actuelle.

### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience)

Si vous souhaitez mettre à jour en bloc des prix article, tels que l’augmentation de tous les prix article par un certain pourcentage, vous pouvez renseigner la **Feuille prix vente** à l’aide des traitements par lots suivants :

* **Suggérez prix article** suggère des modifications en appliquant un facteur d’ajustement aux prix de vente existants ou en copiant les accords de prix de vente existants vers d’autres clients, groupes de prix client ou campagnes de vente.
* **Suggérez prix article** suggère des modifications en appliquant un facteur d’ajustement aux prix unitaires existants sur les fiches article, ou en suggérant des prix pour de nouvelles combinaisons de devises, d’unités de mesure, etc. Les prix unitaires des articles ne sont pas modifiés.    

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de prix de vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Suggérer prix article** .  
3. Sur le raccourci **Article**, renseignez le champ **N°**, ou **Groupe comptabilisation de stock** ou d’autres champs avec les prix article d’origine à mettre à jour.  
4. Dans la partie supérieure de la page de demande, indiquez dans les champs **Type vente** et **Code vente** le type et le nom sous lesquels vous souhaitez copier les prix de vente.
5. Si vous souhaitez que le traitement par lots ajuste automatiquement le prix article proposés, saisissez l’ajustement dans le champ **Facteur appliqué**. Par exemple, vous devez entrer **1,15** dans **Facteur appliqué** pour une augmentation de **15 %** des prix unitaires.  
6. Pour que le traitement par lots crée des prix, activez le bouton de basculement **Créer prix**.  
7. Choisissez **OK** pour remplir les lignes sur la page **Feuille prix vente** avec les nouveaux prix suggérés.
8. Pour mettre en œuvre les suggestions, utilisez l’action **Implémenter nouveaux prix**. Le traitement par lots crée des suggestions mais ne les implémente pas.

## <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience)

Pour mettre à jour les prix de plusieurs articles, vous devez créer une nouvelle liste de prix, puis copier les lignes d’une liste de prix existante. Lorsque vous copiez les lignes, vous pouvez utiliser des filtres pour spécifier les éléments à copier, et vous pouvez spécifier un nombre entier ou décimal dans le champ **Facteur appliqué** pour augmenter ou diminuer les prix. Le statut de la liste de prix doit être **Brouillon**. Si nécessaire, vous pouvez alors désactiver l’ancienne liste de prix.

> [!NOTE]
> Vous ne pouvez pas avoir deux lignes ayant les mêmes paramètres mais des prix différents. Si cela se produit, un message s’affiche lorsque vous activez une liste de prix. Vous pouvez choisir le prix à utiliser en ouvrant la liste et en supprimant le prix incorrect.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Remises facture vente et frais forfaitaires
Lorsque vous utilisez des remises facture, le montant total de la facture détermine celui de la remise accordée. Dans la page **Remises facture client**, vous pouvez également ajouter des frais forfaitaires aux factures supérieures à un montant donné.  

Sur la page **Paramètres ventes**, activez le bouton de basculement **Calculer remise facture** pour que les remises facture soient calculées automatiquement.  

Pour chaque client, vous pouvez spécifier si vous offrirez des remises facture si les critères sont remplis. Par exemple, si le montant de la facture est suffisamment important. Vous pouvez définir des conditions pour les remises facture en devise société pour les clients nationaux et en devise pour les clients étrangers.  

Vous pouvez associer les pourcentages remise à des montants de facture spécifiques sur la page **Remises facture client** pour chaque client. Vous pouvez entrer le nombre de pourcentages de votre choix. Chaque client peut avoir sa propre page, ou vous pouvez lier plusieurs clients à la même page.  

En plus du pourcentage de remise (ou à sa place), vous pouvez lier un montant de frais forfaitaires au montant d’une facture.  

Pour la formation sur les remises sur les ventes, voir [Configurer des remises pour vos clients](/learn/modules/customer-discounts-dynamics-365-business-central/index) sur Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcul de remises facture pour des ventes

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Pour définir une remise ligne vente pour un client
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes**. Si la mise à jour des fonctionnalités n’est pas activée, suivez les étapes de l’onglet Expérience actuelle.

## <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience)  

1. Choisissez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la fiche client appropriée, puis sélectionnez l’action **Remises ligne**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Renseignez une ligne pour chaque combinaison qui accorde une remise ligne vente au client.

> [!Note]
> Lorsque vous ouvrez les pages **Prix de vente** et **Remises ligne vente** à partir d’un client spécifique, les champs **Filtre type vente** et **Filtre code vente** sont définis pour le client et ne peuvent pas être modifiés ou supprimés.
>
> Pour configurer des prix ou des remises ligne pour tous les clients, un groupe de prix client ou une campagne, vous devez ouvrir les pages à partir d’une fiche article. Sinon, pour les prix de vente, utilisez la page **Feuille prix vente**. Pour plus d’informations, voir [Mettre à jour en bloc des prix d’articles](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience)  

1. Choisissez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.
2. Choisissez le client, puis sélectionnez l’action **Listes prix vente**.
3. Ouvrez la liste de prix pour laquelle vous souhaitez spécifier la remise ligne.
4. Créez une nouvelle ligne ou choisissez une ligne existante, puis remplissez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Dans le champ **Définit**, choisissez soit **Prix et remise**, ou juste **Remise**. 
6. Dans le champ **% remise ligne**, spécifiez le pourcentage remise.

   > [!TIP]
   > Filtrez les lignes en choisissant l’option appropriée dans le champ **Afficher les colonnes pour**.   
  
   > [!NOTE]
   > Les codes remise facture sont représentés par les fiches client existantes. L’utilisation de noms de clients en guise de codes vous permet d’affecter rapidement les conditions de remise facture aux clients en sélectionnant le nom d’un autre client qui bénéficie des mêmes conditions. Pour configurer des conditions de remise sur facture spécifiques au client, définissez le champ **Code remise facture** au code client du client, puis passez à l’étape suivante.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Pour configurer une remise facture pour un client
Une fois que vous avez décidé des clients pouvant faire l’objet de remises facture, entrez le code remise facture dans les fiches client et configurez les conditions de chaque code.

1. Choisissez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la page client d’un client pouvant faire l’objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le client. 

> [!NOTE]  
> Les codes remise facture sont représentés par les fiches client existantes. L’utilisation de noms de clients en guise de codes vous permet d’affecter rapidement les conditions de remise facture aux clients en sélectionnant le nom d’un autre client qui bénéficie des mêmes conditions.

À présent, configurez des conditions de remise facture vente.

1. Sur la page **Clients**, sélectionnez l’action **Remises facture**. La page **Remises facture client** s’ouvre.
2. Dans le champ **Code devise**, indiquez le code d’une devise à laquelle s’appliquent les conditions de remise facture. Laissez le champ vierge si vous souhaitez configurer des conditions de remise facture en EUR.
3. Dans le champ **Montant minimum**, entrez le montant minimal qu’une facture doit présenter pour faire l’objet de la remise.
4. Dans le champ **% remise**, entrez la remise facture sous la forme d’un pourcentage du montant de la facture.
5. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le client recevra une remise facture différente.

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