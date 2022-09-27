---
title: Analyse des données par axe analytique
description: Cette rubrique décrit comment analyser les diverses données métier par axe analytique. Les dimensions vous donnent un meilleur aperçu de votre entreprise afin que vous puissiez évaluer les informations.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 545, 555, 556, 557, 558, 9372, 9370, 9371
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: b18bd7f224988f0e5357aa68088ea311ea0cd965
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530691"
---
#  <a name="analyze-data-by-dimensions"></a>Analyse des données par axe analytique
En analyse financière, un axe correspond à des données que vous pouvez ajouter à une écriture comme une sorte de marqueur. Ces données permettent de regrouper des écritures dotées de caractéristiques similaires, telles que les clients, les régions, les produits et les commerciaux, et de récupérer facilement ces groupes à des fins d'analyse. Les axes peuvent être utilisés sur des écritures de feuilles, de documents et de budgets. Le terme Axe décrit la manière dont l'analyse est effectuée. Une analyse à deux axes, par exemple, est une analyse des ventes par zone. Cependant, si vous utilisez plus de deux axes analytiques lors de la création d’une écriture, vous pouvez mener une analyse plus complexe, telle que des ventes par campagne de vente, par groupe client et par zone. Pour plus d’informations, voir [Utiliser des axes analytiques](finance-dimensions.md).

L’analyse de données par axes vous permet d’obtenir un meilleur aperçu de votre activité commerciale, ce qui vous permet d’évaluer les informations, telles que la mesure du bon fonctionnement de votre société, les domaines dans lesquels elle prospère ou non, et ceux dans lesquels il est nécessaire d’affecter davantage de ressources.

> [!TIP]
> Pour analyser rapidement les données transactionnelles par dimensions, vous pouvez filtrer les totaux du plan comptable et les entrées de toutes les pages **Entrées** par dimensions. Recherchez l’action **Définir le filtre axe**.

> [!NOTE]
> Si vous découvrez qu′une dimension incorrecte a été utilisée sur les écritures comptables comptabilisées, vous pouvez corriger les valeurs d′axe analytique et mettre à jour vos vues d′analyse. Pour plus d’informations, voir [Dépannage et correction des axes analytiques](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="to-set-up-an-analysis-view"></a>Pour configurer une vue d’analyse :  
Les vues analytiques affichent une combinaison sélectionnée d’axes analytiques. Vous pouvez stocker et récupérer chaque analyse que vous avez configurée. Les informations de configuration des vues analytiques sont stockées sur des fiches **Vue d’analyse** afin de simplifier une éventuelle analyse ultérieure.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.  
2. Sur la page **Liste des vues d’analyse**, cliquez sur l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Pour ajouter des codes axe aux quatre codes du raccourci **Axes analytiques**, cliquez sur **Filtre**, renseignez les champs et cliquez sur **OK**.  
5. Pour mettre à jour la vue, choisissez l’action **Mettre à jour**.

## <a name="to-analyze-by-dimensions"></a>Pour effectuer une analyse par axe analytique
La matrice **Vues analytiques** peut vous permettre de consulter les montants de votre comptabilité à l’aide des vues d’analyse que vous avez déjà configurées. Complétez la page **Vues analytiques** pour définir les éléments affichés dans la matrice, puis choisissez l’action **Afficher matrice** pour afficher la matrice.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.  
2. Sélectionnez la vue d’analyse appropriée et choisissez l’action **Vues analytiques**.
3. Sur la page **Analyse vente par axe analytique**, renseignez les champs pour définir les données affichées et leur présentation.
4. Choisissez l’action **Afficher matrice** pour ouvrir la page matricielle respective de la vue d’analyse définie.
5. Pour visualiser la spécification d’un montant affiché sur la page matricielle, sélectionnez le montant à explorer.  

- Les colonnes les plus à gauche contiennent des informations basées sur l’option sélectionnée dans le champ **Afficher lignes** de l’en-tête.  
- Les colonnes les plus à droite contiennent des informations basées sur l’option sélectionnée dans le champ **Afficher colonnes** de l’en-tête.

> [!IMPORTANT]  
>   Vous ne pouvez pas sélectionner une période plus courte que celle indiquée en tant que compression date sur la fiche **Vue d’analyse**. Les commandes **Jeu suivant** et **Jeu précédent** ne sont pas actives si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**.  

> [!NOTE]  
>   Vous pouvez utiliser l’état **Axes analytiques - Détail** pour répertorier de manière détaillée les différentes utilisations des axes analytiques sur les écritures au cours d’une période. Vous pouvez utiliser l’état **Axes analytiques - Total** pour afficher uniquement les montants totaux.  

> [!TIP]  
>   Vous pouvez également modifier la vue en changeant la valeur des champs **Afficher lignes** et **Afficher colonnes**. Pour contrepasser un paramètre de vue, choisissez l’action **Inverser lignes et colonnes**.

## <a name="to-update-an-analysis-view"></a>Pour mettre à jour une vue d’analyse  
Les montants affichés sur la page **Vues analytiques** offrent une image de l’état de la société au moment de la dernière mise à jour. Pour obtenir une image de l’état actuel, vous devez actualiser la vue d’analyse en exécutant l’option de mise à jour.

La procédure suivante permet de mettre à jour une vue d’analyse à partir de la page **Vues analytiques**. Les étapes sont similaires entre les pages **Fiche vue d’analyse** et les pages **Liste des vues d’analyse**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.
2. Sélectionnez la vue d’analyse appropriée et choisissez l’action **Vues analytiques**.
2. Sur la page **Vues analytiques**, sélectionnez le champ **Code vue analytique**.  
3. Sélectionnez la ligne contenant la vue d’analyse appropriée.  
4. Sur la page **Vues analytiques**, sélectionnez la vue d’analyse, puis l’action **Mettre à jour**.  

> [!TIP]  
>   Si vous activez la case à cocher **Mise à jour à la validation** sur la fiche vue d’analyse, la vue est automatiquement mise à jour lorsqu’une transaction concernée est validée.

> [!NOTE]  
>   Pour mettre à jour tout ou partie des vues d’analyse en même temps, vous devez utiliser le traitement par lots **Mise à jour vues d’analyse**.  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/dimensions-financial-reports-dynamics-365-business-central/index) associée

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser les axes analytiques](finance-dimensions.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
