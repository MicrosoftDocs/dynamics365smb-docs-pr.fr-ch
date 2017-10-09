---
title: "Echelonner les recettes et les dépenses| Microsoft Docs"
description: "Pour identifier des recettes ou des dépenses dans des période autres que la période de validation de la transaction, vous pouvez utiliser la fonctionnalité pour les échelonner ou les reporter automatiquement selon un calendrier précis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 40db0f3018bcf9575f80aa858bd9febd7bf0846a
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-defer-revenues-and-expenses"></a>Procédure : Échelonner les recettes et les dépenses
Pour identifier une recette ou une dépense dans une période autre que la période de validation de la transaction, vous pouvez utiliser la fonctionnalité pour échelonner automatiquement les recettes et les dépenses selon un calendrier précis.

Pour répartir les recettes et les dépenses sur les périodes comptables concernées, configurez un modèle d'échelonnement pour la ressource, l'article ou le compte général pour lequel/laquelle les recettes ou les dépenses seront validées. Lorsque vous validez le document vente ou achat concerné, les recettes ou les dépenses sont échelonnées sur les périodes comptables concernées, selon un tableau d'échelonnement régi par des paramètres dans le modèle d'échelonnement et la date de validation.

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-set-up-a-gl-account-for-deferral"></a>Pour configurer un compte général pour échelonnement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs comme nécessaire afin de créer un compte général pour les recettes échelonnées. Pour plus d'informations, reportez-vous à [Les écritures comptables et le plan comptable](finance-general-ledger.md).
4. Répétez les étapes 2 et 3 pour créer un nouveau compte général pour les dépenses échelonnées.

Pour les deux types d'échelonnement, sélectionnez **Bilan** dans le champ **Type** et nommez les comptes en conséquence, comme « Revenus comptabilisés d'avance » pour les recettes différées et « Dépenses impayées » pour les dépenses différées.

## <a name="to-set-up-a-deferral-template"></a>Pour configurer un modèle d'échelonnement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Modèles échelonnement**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins.
4. Dans le champ **Méthode de calcul**, précisez comment le champ **Montant** est calculé pour chaque période dans la fenêtre **Tableau d'échelonnement**. Les options suivantes vous sont proposées :

   * **Linéaire** : les montants d'échelonnement périodique sont calculés selon le nombre de périodes, réparties en fonction de la durée de la période.
   * **Égal par période** : les montants d'échelonnement périodique sont calculés selon le nombre de périodes, réparties de façon uniforme sur les périodes.
   * **Jours par période** : les montants d'échelonnement périodique sont calculés selon le nombre de jours dans la période.
   * **Défini par l'utilisateur** : les sommes d'échelonnement périodique ne sont pas calculées. Vous devez renseigner manuellement le champ **Montant** pour chaque période dans la fenêtre Tableau d'échelonnement. Pour en savoir plus, voir la section « Pour modifier un tableau d'échelonnement à partir d'une facture vente ».
5. Dans le champ **Description période**, spécifiez une description affichée sur les écritures pour la validation de l'échelonnement. Vous pouvez saisir les codes d'espace réservé suivants pour les valeurs générales, qui seront insérés automatiquement lorsque la description de la période s'affiche.

   * %1 = le numéro du jour de la date de comptabilisation de la période
   * %2 = le numéro de la semaine de la date de comptabilisation de la période
   * %3 = le numéro du mois de la date de comptabilisation de la période
   * %4 = le nom du mois de la date de comptabilisation de la période
   * %5 = le nom de la période comptable de la date de comptabilisation de la période
   * %6 = l'exercice de la date de comptabilisation de la période

Exemple : la date de comptabilisation est le 06/02/2016. Si vous saisissez « Dépenses échelonnées pour %4 %6 », la description affichée sera « Dépenses échelonnées pour février 2016 ».

## <a name="to-assign-a-deferral-template-to-an-item"></a>Pour affecter un modèle d'échelonnement à un article
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Modèles échelonnement**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche de l'article pour lequel les recettes ou les dépenses doivent être échelonnées selon les périodes comptables lorsque l'article a été vendu ou acheté.
3. Dans le champ **Modèle échelonnement par défaut**, sélectionnez le modèle d'échelonnement pertinent.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Pour modifier un calendrier d'échelonnement à partir d'une facture vente
> [!NOTE]  
>   Les étapes de cette procédure sont identiques lorsque vous modifiez un calendrier d'échelonnement, pour les dépenses, à partir d'une facture achat.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures vente**, puis sélectionnez le lien connexe.
2. Créez une facture vente pour un article ayant un modèle d'échelonnement attribué. Pour plus d'informations, reportez-vous à [Procédure : facturer des ventes](sales-how-invoice-sales.md).

    Notez que dès que vous saisissez l'article (ou la ressource ou le compte général) sur la ligne de facture, le champ **Code d'échelonnement** est complété avec le code du modèle d'échelonnement attribué.
3. Sélectionnez l'action **Tableau d'échelonnement**.
4. Dans la fenêtre **Tableau d'échelonnement**, modifiez les paramètres sur l'en-tête ou les valeurs des lignes, par exemple afin d'échelonner le montant sur une autre période comptable.
5. Sélectionnez l'action **Calculer tableau**.
6. Cliquez sur le bouton **OK**. Le tableau d'échelonnement est mis à jour pour la facture vente. Le modèle d'échelonnement associé reste inchangé.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Pour obtenir un aperçu de la façon dont les recettes et les dépenses seront validées en comptabilité
> [!NOTE]  
>   Les étapes de cette procédure sont identiques lorsque vous prévisualisez la manière dont les échelonnements des dépenses sont validés.

1. Dans la fenêtre **Facture vente enregistrée** sélectionnez l'action **Aperçu compta.**.
2. Dans la fenêtre **Aperçu compta.**, sélectionnez l'action **Écriture comptable**, puis sélectionnez l'action **Afficher écritures associées**.

Les écritures comptables à valider vers le compte d'échelonnement spécifié, par exemple, les Revenus comptabilisés d'avance, sont désignées par la description que vous avez saisie dans le champ **Description de la période** du modèle d'échelonnement, par exemple « Dépenses échelonnées pour février 2016 ».

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Pour examiner les échelonnements validés dans l'état Résumé échelonnement ventes
> [!NOTE]  
>   Les étapes de cette procédure sont identiques lorsque vous prévisualisez l'état Résumé échelonnement achats.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Résumé échelonnement ventes**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Résumé échelonnement ventes**, dans le champ **Balance au**, saisissez la date à laquelle vous souhaitez voir les recettes échelonnées.
3. Cliquez sur le bouton **Aperçu**.

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

