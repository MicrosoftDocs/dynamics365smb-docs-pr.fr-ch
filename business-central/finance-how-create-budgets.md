---
title: Création de budgets comptabilité
description: Décrit la création de budgets comptabilité pour prévoir différentes activités financières et affecter des axes analytiques à des fins de veille économique.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# Créer des budgets comptabilité

Vous pouvez avoir plusieurs budgets pour des périodes identiques en les créant sous des noms différents. Vous indiquez d’abord le nom du budget et entrez les chiffres correspondants. Le nom du budget est ensuite inclus sur toutes les écritures budget que vous créez.  

Lorsque vous créez un budget, vous pouvez définir quatre axes analytiques spécifiques au budget, appelées axes budget, pour chaque budget. Vous sélectionnez les axes budget pour chaque budget parmi ceux que vous avez déjà configurés. Les axes budget peuvent être utilisés pour positionner des filtres sur un budget et pour ajouter des informations analytiques aux écritures budget. Pour plus d’informations, consultez [Utiliser les dimensions](finance-dimensions.md).

Les budgets jouent un rôle important dans la veille économique. Par exemple dans une déclaration financière basée sur des états financiers incluant des écritures budget, ou lors de l’analyse des montants budgétés et des montants réels dans le plan comptable. Pour plus d’informations, consultez [Veille économique](bi.md).

En comptabilité analytique, vous travaillez avec des budgets de coûts de manière similaire. Pour plus d’informations, consultez [Création des budgets des coûts](finance-create-cost-budgets.md).  

## Pour créer un budget comptabilité

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Budgets comptables**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Modifier la liste**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sélectionnez **Modifier budget**.
4. En haut de la page **Budget**, renseignez les champs nécessaires pour définir ce qui est affiché.  

    Seules les écritures contenant le nom du budget entré dans le champ **Nom budget** s’affichent. Étant donné que le nom du budget vient juste d’être créé, aucune écriture ne correspond au filtre. Par conséquent, la page est vide.  
5. Pour entrer un montant, choisissez la cellule appropriée de la matrice. La page **Écritures budget** s’ouvre.  
6. Créez une ligne et renseignez le champ **Montant**. Fermez la page **Écritures budget**.  
7. Répétez les étapes 5 et 6 jusqu’à ce que vous ayez entré tous les montant du budget.  

> [!NOTE]  
> Sur le raccourci **Filtres**, vous pouvez filtrer les informations sur le budget selon les axes budget configurés sous le nom du budget.

## Exportation et importation de budgets comptables vers Excel

Comme pour la majorité des autres pages, vous pouvez exporter des données des pages de budget vers Microsoft Excel pour les traiter ou les analyser ultérieurement. Pour plus d’informations, consultez [Exportation de vos données métier vers Excel](about-export-data.md).

> [!NOTE]
> Le plan comptable, sur lequel les budgets comptables sont basés, comportent des lignes de type de compte En-tête qui contiennent le total des lignes sous ceux-ci. Lorsque vous exportez un budget comptable, les données de toutes les lignes sont exportées quel que soit le type de compte. Cependant, seules les données sur les lignes du type de compte Validation peuvent être réimportées. 

En conséquence, lorsque vous importez un budget comptable, toutes les valeurs qui existaient sur les lignes En-têtes seront supprimées. Cette fonctionnalité permet d’éviter des totaux erronés après l’importation de données créées ou modifiées dans Excel.

### Scénario

Vous savez que le nouveau coût des salaires budgétisé sera de 1 200 000 en devise locale (DS). Vous souhaitez permettre au département Paies de budgétiser trois lignes spécifiques (du type de compte Validation) pour les salariés à temps plein, les salariés à temps partiel et les intérimaires. Les trois lignes sont regroupées sous une ligne d’en-tête Paies.

Vous saisissez 1 200 000 sur la ligne d’en-tête, exportez le budget vers Excel, puis l’envoyez au département Paies, en leur indiquant de distribuer les 1 200 000 en devise société.

Le département Paies distribue le montant des trois comptes de validation. Lorsque vous réimportez le budget comptable, les trois comptes sont renseignés avec les nouvelles données Excel, pour une somme de 1 200 000 en devise société, et la ligne d’en-tête est vide.

## Voir la [formation Microsoft](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index) associée

## Voir aussi

[Exportation de vos données métier vers Excel](about-export-data.md)  
[Finances](finance.md)  
[Veille économique](bi.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
