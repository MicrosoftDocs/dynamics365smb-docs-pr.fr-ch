---
title: Paramétrer des lois d’amortissement
description: "Diverses méthodes d’amortissement sont disponibles. Dans Business\_Central, vous définissez la méthode d’amortissement d’un actif sur la page **Fiche immobilisation**."
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
---

# Configurer un amortissement immobilisation

Vous pouvez utiliser plusieurs méthodes d’amortissement pour préparer les états financiers et les déclarations de revenus. De nombreuses sociétés de grande taille utilisent la méthode de l’amortissement linéaire dans leurs états financiers car elle permet généralement la déclaration des bénéfices supérieurs. Aux fins de l’impôt sur le revenu, cependant, de nombreuses entreprises utilisent une méthode d’amortissement accélérée, comme l’amortissement dégressif. Vous définissez la méthode d’amortissement d’un actif avec le champ **Méthode d’amortissement** sur la page **Fiche immobilisation**. Pour plus d’informations sur les fonctions des différentes méthodes, consultez [Méthodes d’amortissement](fa-depreciation-methods.md).

Vous paramétrez des lois d’amortissement lorsque vous définissez les différentes manières dont l’amortissement doit être calculé pour vos différents types d’immobilisation. Chaque loi d’amortissement spécifie des conditions d’amortissement individuelles. Par exemple, vous pouvez spécifier qu’une immobilisation doit être amortie sur une période de trois ans dans une loi et sur une période de cinq ans dans une autre loi.

Lorsque vous avez créé les lois d’amortissement nécessaires, vous devez en attribuer au moins une à chaque immobilisation. La loi d’amortissement attribuée à une immobilisation est désignée comme loi d’amortissement immobilisation. Vous pouvez créer un nombre illimité de lois d’amortissement pour une immobilisation.  

## Pour créer une loi d’amortissement

Dans une loi d’amortissement immobilisation, vous spécifiez comment les immobilisations sont amorties. Pour prendre en charge plusieurs méthodes d’amortissement, vous pouvez paramétrer plusieurs lois d’amortissement.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.
2. Sur la page **Liste des lois d’amortissement**, sélectionnez l’action **Nouveau**.
3. Sur la page **Fiche loi d’amortissement**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Vous pouvez enregistrer les transactions immobilisation sur la page **Feuille compta. immo.** ou sur la page **Feuille immo.**, selon que les transactions sont destinées pour des rapports financiers ou pour la gestion interne. Procédez comme suit pour définir quel type de feuille est utilisé pour les différentes activités immobilisation par défaut.
4. Sur le raccourci **Intégration**, cochez la case pour chaque activité immobilisation dont vous souhaitez valider les transactions via la page **Feuille compta. immo.**.
5. Répétez les étapes 2 à 4 pour chaque méthode d’amortissement ou méthode de validation que vous souhaitez attribuer à des immobilisations en tant que loi d’amortissement.

> [!IMPORTANT]
> Choisissez le champ **Utiliser arrondi dans amort.** pour arrondir les montants d’amortissement périodique calculés à des nombres entiers. Par exemple, si votre entreprise utilise également l’arrondi facture à des nombres entiers dans la page **Paramètres comptabilité**, arrondir également les montants d’amortissement à des nombres entiers peut aider à assurer la transparence.

Par exemple, si vous disposez d’une immobilisation dont les lois d’amortissement ne spécifient pas d’arrondi, mais que les paramètres comptabilité de votre entreprise nécessitent un arrondi, alors, lorsque vous cédez l’immobilisation, vous verrez un message d’erreur indiquant qu’un montant doit être arrondi sur une écriture comptable.  

## Pour attribuer une loi d’amortissement à une immobilisation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez configurer une loi d’amortissement.
3. Sur le raccourci **Loi d’amortissement**, renseignez les champs, le cas échéant.
4. Si vous devez assigner plus d’une loi d’amortissement à l’immobilisation, sélectionnez l’action **Ajouter davantage de lois d’amortissement**.
5. Sinon, sélectionnez l’action **Lois d’amortissement** pour spécifier une, voire plusieurs lois d’amortissement immobilisation.

    > [!NOTE]  
    >   Lorsque vous utilisez la méthode manuelle d’amortissement, vous devez saisir l’amortissement manuellement dans la feuille comptabilisation immobilisation. La fonction **Calculer amortissement** ignore les immobilisations qui utilisent la méthode d’amortissement manuelle. Vous pouvez recourir à cette méthode pour les immobilisations qui ne font pas l’objet d’un amortissement, par exemple les terrains.

    > [!NOTE]  
    > Lorsque vous utilisez la méthode d’amortissement définie par l’utilisateur, vous devez affecter le livre d’amortissement d’une manière différente. Pour plus d’informations, consultez [Configurer la méthode d’amortissement définie par l’utilisateur](fa-how-setup-user-defined-depreciation-method.md).

## Pour attribuer une loi d’amortissement à plusieurs immobilisations avec un traitement par lots

Si vous voulez associer une loi d’amortissement à plusieurs immobilisations, vous pouvez utiliser le traitement par lots **Créer plans amortissement** pour créer des lois d’amortissement d’immobilisation.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation à laquelle vous souhaitez attribuer une loi d’amortissement, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche livre d’amortissement**, sélectionnez l’action **Créer plans amortissement**.
4. Sur la page **Créer plans amortissement immo.**, renseignez le champ **Loi d’amortissement**.
5. Choisissez le champ **Copier immo. n°**, puis sélectionnez le numéro de l’immobilisation à utiliser comme base pour créer de nouvelles lois d’amortissement d’immobilisation.

    Si vous renseignez ce champ, les champs d’amortissement des nouvelles lois d’amortissement d’immobilisation contiennent les mêmes informations que ceux de la loi d’amortissement d’immobilisation que vous copiez. N’entrez rien dans ce champ si vous souhaitez créer de nouvelles lois d’amortissement d’immobilisation avec des champs d’amortissement vides.  
6. Sur le raccourci **Immo.**, vous pouvez positionner un filtre afin de sélectionner les immobilisations pour lesquelles vous souhaitez créer des lois d’amortissement immobilisation.
7. Cliquez sur le bouton **OK**.

## Pour configurer les types de validation amortissement

Pour chaque loi d’amortissement, vous devez définir la manière dont vous souhaitez que [!INCLUDE[prod_short](includes/prod_short.md)] gère les différents types de validation. Par exemple, vous devez indiquer s’il s’agit d’un débit ou d’un crédit et si le type de validation doit être inclus dans la base d’amortissement.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.  
2. Sélectionnez la loi d’amortissement que vous souhaitez configurer, puis sélectionnez l’action **Type paramètre compta. immo.**.
3. Sur la page **Type paramètre compta. immo.**, renseignez les champs, le cas échéant.

    > [!NOTE]  
    >   Vous ne pouvez pas insérer ni supprimer de lignes sur la page **Type paramètre compta. immo**. Vous ne pouvez modifier que les lignes existantes.

Il est recommandé de ne pas modifier les paramètres des lois d’amortissement pour lesquelles des écritures ont déjà été validées. Les modifications apportées n’ont pas d’incidence sur les écritures déjà validées, ce qui rendrait les statistiques des lois d’amortissement inexactes.

## Pour configurer les modèles par défaut et les lots pour l’amortissement immobilisation

Pour chaque loi d’amortissement, vous définissez une configuration par défaut de modèles et de feuilles. Vous devez utiliser ces valeurs par défaut pour dupliquer les lignes d’une feuille vers une autre, créer des lignes feuille à l’aide du traitement par lots **Calculer amortissement** ou **Actualiser immobilisations**, dupliquer des coûts d’acquisition dans la feuille assurance.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.  
2. Sélectionnez la loi d’amortissement pour laquelle vous souhaitez définir les feuilles par défaut, puis sélectionnez l’action **Configuration feuille immo.**.  
3. Pour avoir une configuration par défaut pour chaque utilisateur, choisissez le champ **Code utilisateur** à sélectionner à partir de la page **Utilisateurs**.  
4. Dans les autres champs, sélectionnez le modèle feuille ou la feuille qui doit être utilisé(e) par défaut.  

## Amortissement via le champ Exercice fiscal 365 jours

Lorsque le traitement par lots Calculer amortissement calcule les amortissements, il utilise normalement une année normalisée de 360 jours, dans laquelle chacun des 12 mois compte 30 jours.

Si vous activez ce champ, le traitement par lots Calculer amortissement utilise l’année civile de 365 jours, où chaque mois est calculé avec le même nombre de jours que le calendrier. La seule exception est le mois de février des années bissextiles, que le traitement par lots traitera comme ayant 28 jours et non 29. Pour cette raison, toutes les années, également les années bissextiles, sont considérées comme ayant 365 jours.

## Voir la [formation Microsoft](/training/modules/configure-depreciation-books/) associée

## Voir aussi

[Paramétrage d’immobilisations](fa-setup.md)  
[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
