---
title: Déprécier ou amortir des immobilisations
description: 'Vous devez définir comment vous allez déprécier ou amortir chacune de vos immobilisations, telles que les machines et l’équipement, tout au long de leur durée d’amortissement.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: bholtorf
---
# Amortir des immobilisations

L’amortissement permet de ventiler le coût des immobilisations, telles que les machines et le matériel, sur leur durée d’amortissement. Vous devez définir la méthode d’amortissement de chaque immobilisation.  

 Vous pouvez valider l’amortissement de deux manières :  

* Automatiquement, via l’exécution du traitement par lots **Calculer amortissement**.  
* Manuellement, à l’aide de la feuille validation immobilisation.  

[!INCLUDE[prod_short](includes/prod_short.md)] peut calculer l’amortissement sur une base quotidienne, ce qui vous permet de calculer l’amortissement pour n’importe quelle période. Vous pouvez ainsi analyser les résultats d’exploitation en cours sur une période mensuelle, trimestrielle ou annuelle. Le calcul utilise une année standard de 360 jours et un mois standard de 30 jours. Pour en savoir plus, voir [Méthodes d’amortissement](fa-depreciation-methods.md).  

Lorsque plusieurs départements utilisent une immobilisation, vous pouvez affecter automatiquement un amortissement périodique à ces départements d’après une table de ventilation paramétrable.  

Vous pouvez annuler des écritures d’amortissement incorrectes à l’aide du traitement par lots **Annuler écriture comptable immo**. Ensuite, vous pouvez valider le montant correct en exécutant de nouveau le traitement par lots **Calculer amortissement**. Les erreurs que vous résolvez sont validées en tant qu’écritures comptables erreur immobilisation.  

L’actualisation permet d’ajuster des valeurs en fonction de modifications générales de niveau de prix. Vous pouvez utiliser le traitement par lots **Actualiser immobilisation** pour recalculer les montants des amortissements.  

## Pour calculer automatiquement des amortissements

Une fois par mois, ou à la fréquence de votre choix, vous pouvez lancer le traitement par lots **Calculer amortissement**. Le traitement par lots ignore les immobilisations qui ont été vendues, celles qui ont été bloquées ou qui sont inactives, et celles qui utilisent la méthode d’amortissement manuelle.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Calculer amortissement**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cliquez sur le bouton **OK**.  

    Le traitement par lots calcule l’amortissement et crée des lignes dans la feuille comptabilisation immobilisation.

4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilisation immobilisation**, puis choisissez le lien associé.  

    Sur la page **Feuille compta. immo**, dans le champ **Nbre jours amort.**, vous pouvez voir le nombre de jours d’amortissement calculé.  
5. Sélectionnez l’action **Valider**.  

> [!NOTE]
> Limitations connues : si vous définissez le champ **Utiliser Forcer nombre de jours** sur Oui, et que le champ **Forcer nombre de jours** est défini sur une valeur où la **Date comptabilisation** moins le **Nombre de jours** a pour résultat une date appartenant à l’année calendaire précédente, le système ne vous permettra pas de valider l’amortissement.
> Vous pouvez éviter cela en réduisant le champ **Forcer nombre de jours** sur une valeur inférieure au nombre de jours calculés jusqu’à la date comptabilisation en utilisant 30 jours/mois OU en définissant l’indicateur **Exercice comptable 365 jours** dans la loi d’amortissement.
> Nous recommandons la première option, car vous ne voudrez peut-être pas modifier l’utilisation de 30 jours/mois pour l’amortissement. Pour plus d’informations, consultez la section [Amortissement via le champ Exercice comptable 365 jours](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## Pour valider un amortissement manuellement à partir d’une feuille validation immobilisation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille compta. immo.**, puis choisissez le lien associé.  
2. Créez une feuille comptable initiale et complétez les champs, le cas échéant.  
3. Dans le champ **Type compta. immo**, sélectionnez **Amortissement**.  
4. Sélectionnez l’action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de l’amortissement. Pour plus d’informations, reportez vous à [Pour configurer des groupes de validation immobilisation](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Choisissez l’action **Valider** pour valider la feuille.  

Le champ **Valeur comptable** dans la page **Fiche immobilisation** est mis à jour en conséquence.

Si vous avez défini des clés de ventilation immobilisation pour ventiler des montants entre plusieurs départements ou plusieurs projets, les montants sont alloués lors de la validation. Pour en savoir plus, voir [Configurer des informations générales sur les immobilisations](fa-how-setup-general.md).  

## Pour gérer la valeur comptable finale

Dans le champ **Valeur comptable finale** de la page **Lois d’amortissement immo.**, vous pouvez spécifier la valeur comptable de votre immobilisation dans la loi d’amortissement actuelle une fois qu’elle a été entièrement amortie. Vous pouvez le faire manuellement ou vous pouvez renseigner le champ **Valeur comptable finale par défaut** dans la page **Loi d’amortissement**, qui est ensuite utilisée pour renseigner automatiquement le champ.

> [!NOTE]
> Si le dernier amortissement entraîne une valeur comptable inférieure à zéro dans le champ **Valeur comptable** de la page **Fiche immobilisation**, ce montant est automatiquement soustrait du dernier amortissement.<br /><br />
> Si la valeur du champ **Valeur comptable** est supérieure à zéro après le dernier amortissement, par exemple à cause d’un arrondi ou d’une valeur résiduelle, la valeur du champ **Valeur comptable finale** dans la page **Lois d’amortissement immo.** est ignorée. Pour plus d’informations, voir [Pour valider la valeur résiduelle ainsi que le coût d’acquisition](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## Pour calculer les ventilations dans la feuille validation immobilisation

Lorsqu’une immobilisation est utilisée par plusieurs départements, vous pouvez affecter automatiquement un amortissement périodique à ces départements d’après une table de ventilation paramétrable.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille compta. immo.**, puis choisissez le lien associé.  
2. Créez une feuille initiale et complétez les champs, le cas échéant.
3. Dans le champ **Type compta. immo**, sélectionnez **Ventilation**.  
4. Sélectionnez l’action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de la ventilation.  
5. Choisissez l’action **Valider** pour valider la feuille.  

## Utilisez les listes de duplication pour préparer la validation vers plusieurs lois d’amortissement

Lorsque vous renseignez les lignes feuille à valider dans une loi d’amortissement, vous pouvez dupliquer les lignes dans une autre feuille afin de pouvoir valider dans une autre loi d’amortissement. Pour en savoir plus, voir [Pour valider les écritures vers différentes lois d’amortissement](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.  
2. Ouvrez la loi d’amortissement, puis cochez la case **Inclure dans liste duplication**.  

> [!IMPORTANT]  
>   Si le champ **Utiliser liste duplication** est sélectionné, n’utilisez pas de souches de numéros sur la feuille. En effet, les souches de numéros pour la feuille validation immobilisation ne correspondent pas aux souches pour la feuille immobilisation.  

## Pour valider des écritures dans plusieurs lois d’amortissement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille compta. immo.**, puis choisissez le lien associé.  
2. Dans la feuille avec laquelle vous souhaitez valider l’amortissement, sélectionnez la case **Utiliser liste duplication**.  
3. Renseignez les champs restants selon vos besoins.  
4. Sélectionnez l’action **Valider**.  
5. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles immobilisation**, puis choisissez le lien associé.  

    > [!NOTE]  
    >   La page **Feuille immobilisation** contient de nouvelles lignes pour différentes lois d’amortissement selon la liste de duplication.  
6. Examinez ou modifiez les lignes, puis sélectionnez l’action **Valider**.  

    > [!NOTE]  
    >   Pour dupliquer une écriture dans une autre loi, vous pouvez également saisir un code loi d’amortissement dans le champ **Dupliquer dans journaux amort.** lorsque vous renseignez une ligne feuille.  

Vous pouvez copier des écritures d’une loi d’amortissement vers une autre à l’aide du traitement par lots **Copier lois d’amortissement**. Le traitement par lots crée des lignes feuille dans la feuille que vous avez indiquée sur la page **Param. feuille immo.** pour la loi d’amortissement vers laquelle vous souhaitez réaliser la copie. Pour plus d’informations, voir la procédure suivante.  

## Pour copier des écritures comptables immobilisation entre les lois d’amortissement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.  
2. Ouvrez la fiche loi d’amortissement pertinente, puis sélectionnez l’action **Copier loi d’amortissement**.  
3. Sur la page **Copier loi d’amortissement**, renseignez les champs comme nécessaire.  
4. Choisissez le bouton **OK**.  

Les lignes copiées sont créées dans la feuille comptabilisation immobilisation ou la feuille immobilisation, selon que la loi d’amortissement que vous copiez a été intégrée en comptabilité ou non.  

## Voir la [formation Microsoft](/training/modules/calculate-post-depreciations/) associée

## Voir aussi

[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d’immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
