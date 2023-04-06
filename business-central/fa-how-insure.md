---
title: Assurer les immobilisations
description: Vous pouvez attribuer une ou plusieurs immobilisations à une police d’assurance lors de la validation sur les écritures couverture assurance à partir de la page **Feuille assurance**.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 06/29/2021
ms.author: edupont
---
# Assurer les immobilisations
Une police d’assurance pour une immobilisation est représentée par une fiche assurance. Vous pouvez attribuer une immobilisation ou plusieurs immobilisations à une police d’assurance.

Vous attribuez une immobilisation à une police d’assurance lors de la validation sur les écritures couverture assurance à partir de la page **Feuille assurance**.

En outre, vous pouvez attribuer une immobilisation à une police d’assurance et créer des écritures comptables de couverture lorsque vous validez son coût d’acquisition. Pour ce faire, validez un coût d’acquisition à partir de la feuille immobilisation où le champ **N° assurance** rempli. La case **Compta. assurance auto.** de la page **Paramètres immobilisations** doit être cochée. Pour en savoir plus, voir [Pour valider manuellement une acquisition d’immobilisation avec la feuille validation immobilisation](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Si la case **Compta. assurance auto.** n’est pas cochée sur la page **Paramètres immobilisations**, la validation des acquisitions à partir de la feuille immobilisation créera des lignes sur la page **Feuille assurance**, que vous devrez ensuite valider manuellement.

> [!WARNING]  
>   Si vous ne cochez pas la case **Compta. assurance auto.** sur la page **Paramètres immobilisations**, votre feuille assurance devrait être basée sur un modèle feuille sans souche de numéros. En effet, les numéros de document insérés à partir de la ligne feuille immobilisation entreront sinon en conflit avec les souches de numéros de la feuille assurance. Pour en savoir plus concernant les modèles feuille et lots, voir [Configurer les informations générales relatives aux immobilisations](fa-how-setup-general.md).

Après avoir attribué une immobilisation à une police d’assurance, la case **Assuré** est cochée sur la fiche immobilisation. Lors de la vente de l’immobilisation, la case est automatiquement décochée.

## Pour créer ou modifier une fiche assurance
Une police d’assurance pour une immobilisation doit être représentée par une fiche assurance.

Lorsque vous recevez des informations concernant les modifications du montant de la couverture, vous devez saisir les nouvelles informations sur la page **Fiche assurance** pour vous assurer que vous avez analysé correctement la couverture de la police d’assurance.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Assurance**, puis choisissez le lien associé.
2. Choisissez l’action **Nouveau** pour créer une fiche pour une police d’assurance. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sinon, sélectionnez la police d’assurance que vous souhaitez modifier, puis sélectionnez l’action **Modifier**.

## Pour affecter une immobilisation à une police d’assurance en effectuant une validation à partir de la feuille assurance
Vous affectez une immobilisation à une police d’assurance en validant sur les écritures couverture assurance.  

La procédure suivante explique comment créer une ligne feuille assurance manuellement. Si la case **Compta. assurance auto.** est cochée sur la page **Paramètres immobilisations**, les lignes feuille assurance sont ensuite créées automatiquement lorsque vous validez des coûts d’acquisition. Dans ce cas, tout ce que vous avez à faire consiste à valider la feuille.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille assurance**, puis choisissez le lien associé.  
2. Ouvrez la feuille pertinente, puis complétez les lignes feuille, le cas échéant.  
3. Pour affecter plusieurs immobilisations à une police d’assurance, créez des lignes feuille avec la même valeur dans le champ **N° assurance** et d’autres valeurs du champ **N° immo.**.  
4. Sélectionnez l’action **Valider**.  

    > [!NOTE]  
    >   Les écritures d’une feuille assurance sont uniquement validées en écritures couverture assurance.  

## Pour mettre à jour la valeur assurance d’une immobilisation
Vous pouvez utiliser le traitement par lots **Réévaluer assurance** pour mettre à jour la valeur des immobilisations couvertes.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réévaluer assurance**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins.

    > [!NOTE]  
    >   Dans le champ **Taux de réévaluation**, vous saisissez une baisse de 5 %, par exemple, soit 95, tout en saisissant une hausse de 2 %, soit 102.  
3. Cliquez sur le bouton **OK**.  

   Le traitement par lots calcule le nouveau montant en tant que pourcentage de la valeur totale assurée à partir de la page **Statistiques assurance**, puis crée une ligne dans la feuille assurance.  
4. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille assurance**, puis choisissez le lien associé.  
5. Ouvrez la feuille assurance pertinente, examinez les valeurs créées, puis validez-les sur les écritures couverture assurance.  

## Pour surveiller la couverture assurance
[!INCLUDE[prod_short](includes/prod_short.md)] fournit des rapports dédiés et des pages de statistiques à utiliser pour analyser les polices d’assurance et si vos immobilisations sont sur- ou sous-assurées.  

### Aperçu des polices d’assurance
Pour obtenir un aperçu de vos polices d’assurance, afficher un aperçu ou imprimer l’état **Assurances - Liste**. L’état indique toutes les polices et les champs les plus importants des fiches assurance.  

### Couverture d’assurance
Pour visualiser les immobilisations couvertes par une assurance et à quelle hauteur, vous pouvez afficher l’aperçu ou imprimer l’état **Assurances - Valeur totale**.  

### Sur-assurance et sous-assurance
Vous pouvez vérifier si les immobilisations sont sur- ou sous-assurées comme suit :  

* La page **Statistiques assurance**. Un montant positif dans le champ **Sur/Sous-assuré** signifie que l’immobilisation est sur-assurée. Un montant négatif signifie qu’elle est sous-assurée.  
* La page **Statistiques immobilisation**. Choisissez le champ **Valeur totale assurée** pour afficher la page **Écritures comptables couverture assur.**.  
* L’état **Sur-assurance et sous-assurance**.  
* L’état **Assurance - Analyse**.  

### Immobilisations non assurées
Pour vérifier que toutes les immobilisations sont attribuées à une police d’assurance, vous pouvez imprimer ou afficher l’aperçu de l’état **Assurances - Immo. non assurées**. Cet état affiche les immobilisations pour lesquelles aucun montant n’a été validé sur des écritures couverture d’assurance.  

## Pour visualiser des écritures comptables couverture assurance
Vous pouvez visualiser les écritures comptables couverture assurance que vous avez créées.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Assurance**, puis choisissez le lien associé.  
2. Sélectionnez la police d’assurance appropriée, puis sélectionnez l’action **Écritures comptables couverture**.  

## Pour afficher la valeur d’assurance totale des immobilisations
Une page de matrice dédiée affiche les valeurs d’assurance qui sont enregistrées pour chaque police d’assurance pour chaque immobilisation suite aux montants d’assurance que vous avez validés.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Assurance**, puis choisissez le lien associé.  
2. Sélectionnez la police d’assurance appropriée, puis sélectionnez l’action **Valeur totale assurée par immo.**.  
3. Renseignez les champs selon vos besoins.  
4. Choisissez l’action **Afficher matrice**.  
5. Pour visualiser les écritures comptables couverture d’assurance, sélectionnez une valeur dans la matrice.  

## Pour corriger des écritures couverture assurance
Si une immobilisation a été jointe à la mauvaise police d’assurance, vous pouvez y remédier en créant deux écritures de reclassement à partir de la feuille assurance.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille assurance**, puis choisissez le lien associé.  
2. Créez une ligne feuille pour l’immobilisation et la police d’assurance appropriée lorsque la valeur du champ **Montant** est positive.  
3. Créez une autre ligne feuille pour l’immobilisation et la police d’assurance incorrecte lorsque la valeur du champ **Montant** est négative.  
4. Sélectionnez l’action **Valider**.  

L’immobilisation sera détachée de la police d’assurance incorrecte, sur la seconde ligne, et rattachée à la police d’assurance correcte, sur la première ligne.  

## Voir aussi
[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d’immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]