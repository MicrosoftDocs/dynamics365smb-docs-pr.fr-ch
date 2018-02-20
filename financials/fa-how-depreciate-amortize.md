---
title: "Déprécier ou amortir des immobilisations| Microsoft Docs"
description: "Vous devez définir comment vous allez déprécier ou amortir chacune des immobilisations."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e9edb717c073a3b94d925ac0cc532824a848daf6
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="depreciate-or-amortize-fixed-assets"></a>Amortir des immobilisations
L'amortissement permet de ventiler le coût des immobilisations, telles que les machines et le matériel, sur leur durée d'amortissement. Vous devez définir la méthode d'amortissement de chaque immobilisation.  

 Vous pouvez valider l'amortissement de deux manières :  

* Automatiquement, via l'exécution du traitement par lots **Calculer amortissement**.  
* Manuellement, à l'aide de la feuille validation immobilisation.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] peut calculer l'amortissement sur une base quotidienne, ce qui vous permet de calculer l'amortissement pour n'importe quelle période. Vous pouvez ainsi analyser les résultats d'exploitation en cours sur une période mensuelle, trimestrielle ou annuelle. Le calcul utilise une année standard de 360 jours et un mois standard de 30 jours. Pour en savoir plus, voir [Méthodes d'amortissement](fa-depreciation-methods.md).  

Lorsque plusieurs départements utilisent une immobilisation, vous pouvez affecter automatiquement un amortissement périodique à ces départements d'après une table de ventilation paramétrable.  

Vous pouvez annuler des écritures d'amortissement incorrectes à l'aide du traitement par lots **Annuler écriture comptable immo**. Ensuite, vous pouvez valider le montant correct en exécutant de nouveau le traitement par lots **Calculer amortissement**. Les erreurs que vous résolvez sont validées en tant qu'écritures comptables erreur immobilisation.  

L'actualisation permet d'ajuster des valeurs en fonction de modifications générales de niveau de prix. Vous pouvez utiliser le traitement par lots **Actualiser immobilisation** pour recalculer les montants des amortissements.  

## <a name="to-calculate-depreciation-automatically"></a>Pour calculer automatiquement des amortissements
Une fois par mois, ou à la fréquence de votre choix, vous pouvez lancer le traitement par lots **Calculer amortissement**. Le traitement par lots ignore les immobilisations qui ont été vendues, celles qui ont été bloquées ou qui sont inactives, et celles qui utilisent la méthode d'amortissement manuelle.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Calculer amortissement**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cliquez sur le bouton **OK**.  

    Le traitement par lots calcule l'amortissement et crée des lignes dans la feuille comptabilisation immobilisation.  
4. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille comptabilisation immobilisation**, puis sélectionnez le lien connexe.  

    Dans la fenêtre **Feuille compta. immo**, dans le champ **Nbre jours amort.**, vous pouvez voir le nombre de jours d'amortissement calculé.  
5. Sélectionnez l'action **Valider**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Pour valider un amortissement manuellement à partir d'une feuille validation immobilisation
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille compta. immo.**, puis sélectionnez le lien connexe.  
2. Créez une feuille comptable initiale et complétez les champs, le cas échéant.  
3. Dans le champ **Type compta. immo**, sélectionnez **Amortissement**.  
4. Sélectionnez l'action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de l'amortissement. Pour en savoir plus, voir la section « Pour configurer des groupes de validation d'immobilisation » dans [Configurer des informations d'immobilisation générales pour les immobilisations](fa-how-setup-general.md).  
5. Sous l'onglet **Accueil**, sélectionnez **Valider** pour valider la feuille.  

Si vous avez défini des clés de ventilation immobilisation pour ventiler des montants entre plusieurs départements ou plusieurs projets, les montants sont alloués lors de la validation. Pour en savoir plus, voir [Configurer des informations générales sur les immobilisations](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Pour calculer les ventilations dans la feuille validation immobilisation
Lorsqu'une immobilisation est utilisée par plusieurs départements, vous pouvez affecter automatiquement un amortissement périodique à ces départements d'après une table de ventilation paramétrable.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille compta. immo.**, puis sélectionnez le lien connexe.  
2. Créez une feuille initiale et complétez les champs, le cas échéant.
3. Dans le champ **Type compta. immo**, sélectionnez **Ventilation**.  
4. Sélectionnez l'action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de la ventilation.  
5. Sous l'onglet **Accueil**, sélectionnez **Valider** pour valider la feuille.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Utilisez les listes de duplication pour préparer la validation vers plusieurs lois d'amortissement
Lorsque vous renseignez les lignes feuille à valider dans une loi d'amortissement, vous pouvez dupliquer les lignes dans une autre feuille afin de pouvoir valider dans une autre loi d'amortissement. Pour en savoir plus, voir la section « Pour valider les écritures vers différentes lois d'amortissement ».

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Lois d'amortissement**, puis sélectionnez le lien connexe.  
2. Ouvrez la loi d'amortissement, puis cochez la case **Inclure dans liste duplication**.  

> [!IMPORTANT]  
>   Si le champ **Utiliser liste duplication** est sélectionné, n'utilisez pas de souches de numéros sur la feuille. En effet, les souches de numéros pour la feuille validation immobilisation ne correspondent pas aux souches pour la feuille immobilisation.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Pour valider des écritures dans plusieurs lois d'amortissement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille compta. immo.**, puis sélectionnez le lien connexe.  
2. Dans la feuille avec laquelle vous souhaitez valider l'amortissement, sélectionnez la case **Utiliser liste duplication**.  
3. Renseignez les champs restants selon vos besoins.  
4. Sélectionnez l'action **Valider**.  
5. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille immobilisation**, puis sélectionnez le lien connexe.  

    > [!NOTE]  
>   La fenêtre **Feuille immobilisation** contient de nouvelles lignes pour différentes lois d'amortissement selon la liste de duplication.  
6. Examinez ou modifiez les lignes, puis sélectionnez l'action **Valider**.  

    > [!NOTE]  
>   Pour dupliquer une écriture dans une autre loi, vous pouvez également saisir un code loi d'amortissement dans le champ **Dupliquer dans journaux amort.** lorsque vous renseignez une ligne feuille.  

Vous pouvez copier des écritures d'une loi d'amortissement vers une autre à l'aide du traitement par lots **Copier lois d'amortissement**. Le traitement par lots crée des lignes feuille dans la feuille que vous avez indiquée dans la fenêtre **Param. feuille immo.** pour la loi d'amortissement vers laquelle vous souhaitez réaliser la copie. Pour plus d'informations, voir la procédure suivante.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Pour copier des écritures comptables immobilisation entre les lois d'amortissement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Lois d'amortissement**, puis sélectionnez le lien connexe.  
2. Ouvrez la fiche loi d'amortissement pertinente, puis sélectionnez l'action **Copier loi d'amortissement**.  
3. Dans la fenêtre **Copier loi d'amortissement**, renseignez les champs comme nécessaire.  
4. Cliquez sur le bouton **OK**.  

Les lignes copiées sont créées dans la feuille comptabilisation immobilisation ou la feuille immobilisation, selon que la loi d'amortissement que vous copiez a été intégrée en comptabilité ou non.  

## <a name="see-also"></a>Voir aussi
[Immobilisations](fa-manage.md)  
[Paramétrage d'immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

