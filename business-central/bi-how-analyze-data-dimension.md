---
title: Analyse des données par axe analytique
description: Cet article décrit comment analyser les données d’entreprise par axes analytiques pour mieux comprendre votre activité.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# Analyse des données par axe analytique

En analyse financière, un axe correspond à des données que vous ajoutez à une écriture comme une sorte de marqueur. Ces données permettent de regrouper des écritures dotées de caractéristiques similaires, telles que les clients, les régions, les produits et les commerciaux, et de récupérer facilement ces groupes à des fins d’analyse. Les axes peuvent être utilisés sur des écritures de feuilles, de documents et de budgets. 

Chaque « axe » décrit l’objet de l’analyse. Une analyse à deux axes, par exemple, est une analyse des ventes par zone. Si vous utilisez plus de deux axes analytiques lors de la création d’une écriture, vous pouvez mener une analyse plus complexe, telle que des ventes par campagne de vente, par groupe client et par zone. Cela vous permet d’obtenir un meilleur aperçu de votre activité commerciale, comme la mesure du bon fonctionnement de votre société, les domaines dans lesquels elle prospère ou non, et ceux dans lesquels il est nécessaire d’affecter davantage de ressources. Vous pouvez ainsi prendre de meilleures décisions pour mieux progresser. Pour plus d’informations, consultez [Utiliser les dimensions](finance-dimensions.md).

> [!TIP]
> Pour analyser rapidement les données transactionnelles par axe, vous pouvez filtrer les totaux du plan comptable (COA) et les entrées de toutes les pages **Écritures** par axes analytiques. Recherchez l’action **Définir le filtre axe**.

> [!NOTE]
> Si vous découvrez qu’une section analytique incorrecte a été utilisée sur les écritures comptables comptabilisées, vous pouvez la corriger et mettre à jour vos vues d’analyse. Pour plus d’informations, consultez la section [Dépannage et correction des axes analytiques](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Configurer une vue d’analyse

Les vues analytiques utilisent une combinaison sélectionnée d’axes analytiques. Vous stockez, récupérez et mettez à jour cet ensemble d’axes analytiques en créant une fiche **Vue d’analyse**. 

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.  
2. Sur la page **Liste des vues d’analyse**, cliquez sur l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Pour ajouter des codes axe aux quatre codes du raccourci **Axes analytiques**, cliquez sur l’action **Filtre**, renseignez les champs et cliquez sur **OK**.  
5. Pour mettre à jour la vue, choisissez l’action **Mettre à jour**.

## Analyse par axe analytique

Utilisez les vues d’analyse que vous avez déjà configurées avec la matrice **Vues analytiques** pour afficher les montants de votre comptabilité.   

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.  
2. Sélectionnez la vue d’analyse appropriée et choisissez l’action **Vues analytiques**.
3. Sur la page **Analyse vente par axe analytique**, renseignez les champs pour définir les données affichées et leur présentation.
4. Choisissez l’action **Afficher matrice** pour ouvrir la page matricielle respective de la vue d’analyse définie.
5. Pour visualiser la spécification d’un montant affiché sur la page matricielle, sélectionnez le montant à explorer.  

- Les colonnes les plus à gauche contiennent des informations basées sur l’option sélectionnée dans le champ **Afficher lignes** de l’en-tête.  
- Les colonnes les plus à droite contiennent des informations basées sur l’option sélectionnée dans le champ **Afficher colonnes** de l’en-tête.

> [!IMPORTANT]  
> Vous ne pouvez pas sélectionner une période plus courte que celle indiquée en tant que compression date sur la fiche **Vue d’analyse**. Les commandes **Jeu suivant** et **Jeu précédent** sont inactives si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou le champ **Afficher colonnes**.  

> [!NOTE]  
> Vous pouvez utiliser l'état **Axes analytiques - Détail** pour afficher un classement détaillé du mode d'utilisation des axes sur des écritures pour une période donnée. Vous pouvez utiliser l’état **Axes analytiques - Total** pour afficher uniquement les montants totaux.  

> [!TIP]  
> Vous pouvez également modifier la vue en changeant la valeur des champs **Afficher lignes** et **Afficher colonnes**. Pour contrepasser un paramètre de vue, choisissez l’action **Inverser lignes et colonnes**.

## Mettre à jour une vue d’analyse

Les montants affichés sur la page **Vues analytiques** offrent une image de l’état de la société au moment de la dernière mise à jour. Pour obtenir une image de l’état actuel, vous devez actualiser la vue d’analyse en exécutant l’option de mise à jour.

Suivez la procédure suivante pour mettre à jour une vue d’analyse à partir de la page **Vues analytiques**. Les étapes sont similaires à celles de la mise à jour des pages **Fiche vue d’analyse** et **Liste des vues d’analyse**.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Vues d’analyse**, puis sélectionnez le lien associé.
2. Sélectionnez la vue d’analyse appropriée et choisissez l’action **Vues analytiques**.
3. Sur la page **Vues analytiques**, sélectionnez le champ **Code vue analytique**.  
4. Sélectionnez la ligne contenant la vue d’analyse appropriée.  
5. Sur la page **Vues d’analyse**, sélectionnez la vue d’analyse, puis l’action **Mettre à jour**.  

> [!TIP]  
> Si vous activez la case à cocher **Mise à jour à la validation** sur la fiche vue d’analyse, la vue est automatiquement mise à jour lorsqu’une transaction associée est validée.

> [!NOTE]  
> Pour mettre à jour tout ou partie des vues d’analyse en même temps, vous devez utiliser le traitement par lots **Mise à jour vues d’analyse**.  

## Voir aussi

[Business Intelligence financière](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser les axes analytiques](finance-dimensions.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
