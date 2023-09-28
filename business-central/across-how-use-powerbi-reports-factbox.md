---
title: Afficher les rapports Power BI personnalisés
description: Vous pouvez utiliser le récapitulatif Power BI pour afficher les rapports Power BI et obtenir des informations supplémentaires sur les données des enregistrements dans les listes clés.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/11/2021
ms.author: jswymer
---
# Création d’états Power BI pour afficher les données de liste dans [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] comprend un élément de contrôle Récapitulatif Power BI sur plusieurs pages de liste clé. Le but de ce Récapitulatif est d′afficher des états Power BI liés aux enregistrements dans les listes, fournissant des informations supplémentaires sur les données. L′idée est que lorsque vous vous déplacez entre les lignes de la liste, l’état se met à jour pour l’écriture sélectionnée.

[!INCLUDE[prod_long](includes/prod_long.md)] est livré avec certains de ces états. Vous pouvez également créer vos propres rapports personnalisés qui s′affichent dans ce Récapitulatif. La création de ces rapports est similaire à d′autres rapports. Mais il y a quelques règles de conception que vous devrez suivre pour vous assurer que les rapports s′affichent comme prévu. Ces règles sont expliquées dans cet article.

> [!NOTE]
> Pour des informations générales sur la création et la publication des états Power BI pour Business Central, voir [Création d′états Power BI pour afficher des données [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md). 

## Conditions préalables

- Un compte Power BI.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## Créer un rapport pour une page de liste

1. Lancez Power BI Desktop.
2. Sélectionnez **Obtenir des données** et commencez à choisir la source de données pour le rapport.

    Spécifiez les pages de liste Business Central qui contiennent les données souhaitées dans l′état. Par exemple, pour créer un état pour la liste **Factures vente**, incluez les pages liées aux ventes.

    Pour plus d′informations, suivez les instructions [Ajouter[!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Définissez le filtre d’état.

    Pour mettre à jour les données de l’enregistrement sélectionné dans la liste, vous ajoutez un filtre à l’état. Le filtre doit inclure un champ de la source de données utilisé pour identifier de manière unique chaque enregistrement de la liste. En termes de développeur, ce champ est la *clé primaire*. Dans la plupart des cas, la clé primaire de la liste est **N°** .

    Pour définir le filtre, procédez comme suit :

    1. Dans les **Filtres**, sélectionnez le champ de clé primaire dans la liste des champs disponibles.
    2. Faites glisser le champ vers le volet **Filtres** et déposez-le dans le zone **Filtres sur toutes les pages**.
    3. Définissez le **Type de filtre** sur **Filtrage de base**. Il ne peut pas s’agir d’un filtre de page, visuel ou avancé.

    ![Définition du filtre d’état pour l’état Activités Facture vente.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Concevez la disposition du rapport.

    Créez la disposition en faisant glisser des champs et en ajoutant des visualisations. Pour plus d′informations, voir [Utiliser la vue Rapport dans Power BI Desktop](/power-bi/create-reports/desktop-report-view) dans la documentation Power BI.

5. Consultez les sections suivantes sur le dimensionnement du rapport et l′utilisation de plusieurs pages.

6. Enregistrez et nommez le rapport.

    Attribuez à l′état un nom qui contient le nom de la page de liste associée à l’état, comme dans le client. Le nom n′est cependant pas sensible à la casse. Supposons que l′état concerne la page de liste **Factures vente**. Dans ce cas, incluez les mots **factures vente** dans le nom, par exemple **mes factures vente.pbix** ou **ma_liste_factures_vente.pbix**.

    Cette convention de désignation de nom n’est pas obligatoire. Cependant, il permet de sélectionner plus rapidement des états dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque la page de sélection des états s’ouvre depuis une page de liste, elle est automatiquement filtrée en fonction du nom de la page. Le filtre a la syntaxe suivante : `@*<caption>*` comme `@*Sales Invoices*`. Ce filtrage est effectué pour limiter les états affichés. Vous pouvez aussi effacer le filtre pour obtenir la liste complète des états disponibles dans Power BI.

7. Lorsque vous avez terminé, publiez le rapport comme d′habitude.

    Pour en savoir plus, consultez [Publication d’un état](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Testez le rapport.

    Une fois les états publiés dans votre espace de travail, ils doivent être disponibles à partir du Récapitulatif Power BI sur la page de liste dans [!INCLUDE[prod_short](includes/prod_short.md)].

    Pour le tester, procédez comme suit.

    1. Ouvrez [!INCLUDE[prod_short](includes/prod_short.md)] et allez à la page de liste.
    2. Si vous ne voyez pas le Récapitulatif Power BI, dans la barre d’action, sélectionnez **Actions** > **Afficher** > **Afficher/Masquer les états Power BI**.
    3. Dans le Récapitulatif Power BI, sélectionnez **Sélectionner des rapports**, cochez la case **Activer** pour le rapport, puis sélectionnez **OK**.

    S′il est correctement conçu, le rapport s′affiche.  

## Définissez la taille et la couleur de l’état

La taille de l’état doit être configurée sur 325 pixels par 310 pixels. Cette taille offre une mise à l’échelle appropriée de l’état dans l’espace disponible du contrôle Récapitulatif Power BI dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour définir la taille de l’état, placez le focus en dehors de la zone de présentation d’état, puis choisissez l’icône en forme de rouleau de peinture.

![Définition de la largeur et de la hauteur de l’état pour l’état Activités Facture vente.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Vous pouvez modifier la largeur et la hauteur de l’état en choisissant **Personnalisé** dans le champ **Type**.

Si vous souhaitez que l’arrière-plan de l’état se fonde avec la couleur de l’arrière-plan du contrôle Récapitulatif Power BI, définissez une couleur d’arrière-plan d’état personnalisé de *#FFFFFF* (blanc). 

> [!TIP]
> Utilisez le fichier de thème [!INCLUDE [prod_short](includes/prod_short.md)] pour créer des rapports avec le même style de couleur que les applications [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utiliser le thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).

## États avec plusieurs pages

Avec Power BI, vous pouvez créer un seul état avec plusieurs pages. Cependant, pour les états qui s’affichent avec des pages de liste, nous ne recommandons pas plus d′une seule page. Le Récapitulatif Power BI n’affiche que la première page de votre état.

## Résolution des problèmes

Cette section explique comment résoudre les problèmes que vous pourriez rencontrer en essayant d′afficher un état Power BI pour une page de liste dans [!INCLUDE[prod_short](includes/prod_short.md)].  

### Vous ne pouvez pas voir le Récapitulatif Power BI sur une page de liste

Par défaut, le Récapitulatif Power BI est caché de la vue. Pour afficher le Récapitulatif sur une page, dans la barre d’action, sélectionnez **Actions** > **Afficher** > **Afficher/Masquer les états Power BI**.

### Vous ne pouvez pas voir l’état sur le volet Sélectionner un état

Le nom de l’état ne contient pas le nom de la page de liste affichée. Effacez le filtre pour obtenir la liste complète des états disponibles dans Power BI.  

### L’état est chargé, mais vide, non filtré ou filtré incorrectement

Vérifiez que le filtre de l’état contient la bonne clé primaire. Dans la plupart des cas, il s’agit du champ **N°**, mais dans la table **Écriture comptable**, vous devez utiliser le champ **N° écriture**.

### L’état est chargé, mais il affiche une page à laquelle vous ne vous attendiez pas.

Vérifiez que la page que vous souhaitez afficher est la première page de votre état.  

### L’état apparaît avec des bordures grises non désirées, il est trop petit ou trop grand.

Vérifiez que la taille de l’état est configurée sur 325 pixels x 310 pixels. Enregistrez l’état, puis actualisez la page de liste.  

## Voir aussi

[Activation de vos données métier pour Power BI](admin-powerbi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
