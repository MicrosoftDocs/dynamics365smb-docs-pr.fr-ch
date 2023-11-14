---
title: Utiliser des états financiers et des aperçus dans Excel
description: En savoir plus sur la manière dont vous pouvez ouvrir des états financiers dans Microsoft Excel à partir de Business Central pour une meilleure analyse.
author: brentholtorf
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: bholtorf
---
# Analyse des états financiers dans Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] fournit des KPI et obtient des aperçus des finances de votre entreprise. Voici des exemples de façons d’analyser les KPI et les aperçus dans Excel :

* Ouvrez des listes dans Excel et analysez les données. 
* Exportez des états financiers volumineux, tels que votre bilan ou vos comptes de gestion vers Excel, analysez les données et imprimez les états.  

> [!TIP]
> Par défaut, les rapports que vous pouvez visualiser dans Excel sont conçus pour vous aider à analyser l’année en cours. Le rapport sur l’exercice comptable fait toutefois exception. Ce rapport vous permet de filtrer les données pour inclure les années précédentes dans vos analyses.

## Affichage de l’aperçu et des détails dans Excel

Dans les tableaux de bord Gestionnaire d’activité et Comptable, l’action **États** vous permet de choisir les états financiers à afficher dans Excel. Lorsque vous sélectionnez un état, il est ouvert dans Excel ou Excel Online. Une macro complémentaire connecte les données à [!INCLUDE [prod_short](includes/prod_short.md)]. Cependant, vous devez vous connecter avec le même compte que celui utilisé avec [!INCLUDE [prod_short](includes/prod_short.md)]. Le tableau suivant répertorie les états et indique où ils sont disponibles.  


|État  |Tableau de bord  |
|---------|---------|
|Bilan                 | Gestionnaire d’activité, Comptable |
|Compte de gestion              | Gestionnaire d’activité, Comptable |
|Déclaration des trésoreries       | Gestionnaire d’activité, Comptable |
|Déclaration des réserves| Gestionnaire d’activité, Comptable |
|Sales Taxes collectées         | Gestionnaire d’activité, Comptable |
|Relevés client           | Gestionnaire d’activité, Comptable |
|Comptabilité fournisseur chronologique         | Comptable |
|Comptabilité client chronologique      | Comptable |

Supposons que vous souhaitiez analyser en profondeur votre trésorerie. Depuis les tableaux de bord Gestionnaire d’activité et Comptable, vous pouvez ouvrir l’état **Déclaration des trésoreries** dans Excel, mais ce qui se produit réellement est que nous exportons les données appropriées pour vous et créons un classeur Excel sur la base d’un modèle prédéfini. Selon votre navigateur, vous pouvez être invité à ouvrir ou enregistrer le classeur.  

Dans Excel, vous pouvez voir un onglet où les données sont présentées sur la première feuille. Toutes les données qui ont été exportées sont également présentes dans d’autres feuilles en cas de besoin. Vous pouvez imprimer l’état immédiatement, ou vous pouvez le modifier jusqu’à ce que vous ayez l’aperçu et les détails que vous souhaitez. Utilisez la macro complémentaire [!INCLUDE [prod_short](includes/prod_short.md)] pour Excel afin de mieux filtrer et analyser les données.  

### Comprendre les modèles Excel

Les états Excel prédéfinis sont basés sur les données de l’entreprise actuelle. Par exemple, la société de démonstration a mis en place le plan comptable pour répertorier trois comptes règlement sous *Actifs actuels* : 10100 **Compte chèque**, 10200 **Compte épargne** et 10300 **Fonds de caisse**. Les comptes ont le champ **Sous-catégorie de compte** défini sur *Espèces*, et c’est leur montant combiné qui apparaît comme *Espèces* dans l’état Excel **Bilan**.  

D’autres feuilles dans le classeur Excel affichent les données derrière l’état. Pour savoir ce qui se cache derrière les regroupements dans les rapports Excel, vous devrez peut-être filtrer les listes dans [!INCLUDE [prod_short](includes/prod_short.md)].  

## Module complémentaire [!INCLUDE [prod_short](includes/prod_short.md)] pour Excel

Votre expérience [!INCLUDE [prod_short](includes/prod_short.md)] inclut une macro complémentaire pour Excel. Selon votre abonnement, vous êtes connecté automatiquement, ou vous devez spécifier les mêmes informations de connexion utilisées pour [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md).  

Le module complémentaire vous permet d’obtenir des données actualisées à partir de [!INCLUDE [prod_short](includes/prod_short.md)] et d’appliquer les modifications à [!INCLUDE [prod_short](includes/prod_short.md)]. Toutefois, la possibilité de transférer les données vers la base de données est désactivée pour les états financiers Excel dans la liste ci-dessus.  

## Voir aussi

[Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
