---
title: Passer à une autre entreprise ou un autre environnement
description: 'Si vous travaillez pour plusieurs organisations, vous pouvez rapidement passer d’un environnement et d’une société à l’autre.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
---

# Passer à une autre entreprise ou un autre environnement

[!INCLUDE [prod_short](includes/prod_short.md)] est disponible dans de nombreux pays différents et prend en charge de nombreux types d’organisations. Votre organisation peut choisir d’organiser le travail dans [!INCLUDE [prod_short](includes/prod_short.md)] en plusieurs *entreprises* et *environnements*. Cet article vous aide à comprendre les principales différences et à les surmonter.

## À propos des sociétés et environnements

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Si vous changez souvent d’entreprise ou utilisez [!INCLUDE[prod_short](includes/prod_short.md)] depuis une autre application comme Microsoft Teams, vous pouvez facilement perdre de vue où vous êtes. Pour vous aider à garder le fil, vous pouvez ajouter un badge qui affichera le nom de la société, afin que vous puissiez rapidement vérifier que vous êtes au bon endroit. Pour en savoir plus, voir [Afficher un badge de société](admin-company-information.md#badge).
> 
> Selon votre navigateur, vous pouvez également épingler les différentes entreprises à votre barre de favoris.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## Fonctionnalités pour basculer d’une société à une autre ou d’un environnement à un autre

Il existe quelques fonctionnalités que vous pouvez utiliser pour changer d’entreprise ou d’environnement pendant que vous travaillez. Le tableau suivant compare les capacités de la fonctionnalité, qui sont expliquées plus en détail dans les sections qui suivent.

|Fonctionnalité|Changer d’entreprise|Changer d’environnement|Basculer dans le nouvel onglet du navigateur| Disponible en local|
|-------|--------------|------------------|-------------------------|----------------------|
|[Sélecteur d’entreprise](#use-the-company-switcher)|![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")|
|[Lanceur d’application](#use-the-app-launcher)||![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")||
|[Mes paramètres](#use-my-settings)|![coche](media/check.png "chèque ;")|||![coche](media/check.png "chèque ;")|
|[Hub Entreprise](#use-company-hub)|![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")|![coche](media/check.png "chèque ;")||

## Utiliser le sélecteur d’entreprise

L’utilisation du sélecteur d’entreprise est probablement le moyen le plus rapide et le plus polyvalent de changer d’entreprise. Le sélecteur d’entreprise est un volet facilement accessible depuis n’importe quelle page. Le volet donne un aperçu de toutes les entreprises dans tous les environnements auxquels vous avez accès et vous permet de passer directement à l’une d’entre elles&mdash; soit dans le même onglet du navigateur, soit dans un nouveau. C’est particulièrement utile lorsque vous travaillez dans de nombreuses entreprises dans différents environnements.

1. Dans le coin supérieur droit, près de l’icône de recherche, vous voyez l’icône standard de l’entreprise, comme ![Lanceur icône de l’entreprise.](media/ui-experience/company-icon.png "Affiche l’icône de changement d’entreprise utilisée lorsqu’il n’y a qu’un seul environnement") et ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Affiche l’icône de changement d’entreprise utilisée lorsqu’il y a plusieurs environnements"), ou un [badge personnalisé](admin-company-information.md#badge) pour l’entreprise avec laquelle vous travaillez actuellement. Sélectionnez l’icône pour ouvrir le volet de changement d’entreprise.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Affiche l’icône de changement de société dans l’en-tête du client Business Central.":::  

   > [!TIP]
   > Vous pouvez également utiliser le raccourci clavier <kbd>Crtl</kbd>+<kbd>O</kbd> pour ouvrir le volet.
2. Dans le volet **Entreprises disponibles**, sélectionnez la société vers laquelle vous souhaitez basculer, sélectionnez la flèche **Changer**, puis choisissez l’une des options suivantes :

   |Option|Désignation|
   |------|-----------|
   |Basculer|Ouvre le tableau de bord de la société sélectionnée dans le même onglet de navigateur que celui dans lequel vous travaillez. La société devient la société par défaut qui s’ouvre dans Business Central, jusqu’à ce que vous changiez à nouveau ou que vous changiez de société à l’aide de **Mes paramètres**. |
   |Ouvrir dans un nouvel onglet|Ouvre le tableau de bord de la société sélectionnée dans un nouvel onglet du navigateur, en gardant la société d’origine ouverte dans l’autre onglet.|
   |Ouvrir dans un nouvel onglet et accéder à la même page|Cette option n’est active que sur les pages de liste, comme les clients, les commandes client ou les articles. Elle ouvre la même liste, mais pour l’entreprise sélectionnée, dans un nouvel onglet du navigateur. |

> [!TIP]
> Appuyez sur <kbd>F5</kbd> pour actualiser la liste des environnements et des entreprises.

## Utiliser le lanceur d’application

Lorsque vous êtes connecté à [!INCLUDE[prod_short](includes/prod_short.md)], les environnements auxquels vous pouvez accéder sont disponibles sur le site Office.com.  

1. Sélectionnez l’icône **Lanceur d’applications** ![Lanceur d’applications.](media/app-launcher-icon.png "Le lanceur d’applications donne accès à plus de fonctionnalités").
2. Dans le volet qui s’ouvre, recherchez et sélectionnez [!INCLUDE[prod_short](includes/prod_short.md)]. Si vous ne voyez pas [!INCLUDE[prod_short](includes/prod_short.md)], choisissez **Toutes les applications**, puis saisissez **Business Central** dans la zone de **recherche**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Lanceur d’applications Microsoft 365 affichant la vignette Business Central.":::  

3. S’il existe plusieurs environnements, il vous sera demandé de choisir l’environnement auquel accéder.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## Utiliser Mes paramètres

Lorsque vous êtes connecté à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez rapidement passer à une autre société dans le même environnement. Après avoir effectué le changement, la société que vous choisissez devient votre société par défaut et s’ouvrira la prochaine fois que vous vous connecterez.

1. Dans le coin supérieur droit, sélectionnez l’icône **Paramètres** ![Paramètres.](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis choisissez l’action **Mes paramètres**.

    > [!TIP]
    > Vous pouvez également utiliser le raccourci clavier <kbd>Alt</kbd>+<kbd>T</kbd> pour ouvrir rapidement la page Mes paramètres.

2. Sur la page **Mes paramètres**, dans le champ **Société**, sélectionnez la société.  
3. Cliquez sur le bouton **OK**.

> [!TIP]
> Une bonne façon d’aller directement à votre société par défaut lorsque vous vous connectez et d’éviter d’avoir à spécifier un environnement consiste à ajouter l’URL à votre liste de favoris après vous être connecté.

## Utiliser le Hub Entreprise

*Hub entreprise* est un centre de rôle hautement spécialisé qui donne un aperçu financier à travers les entreprises et les environnements. Disponible en tant qu’[extension](ui-extensions-company-hub.md), le hub Entreprise fournit un tableau de bord avec des données récapitulatives pour chaque entreprise à laquelle vous avez accès. La page d’accueil affiche les indicateurs clés financiers ainsi qu’un lien direct vers les différents environnements et entreprises. Pour plus d’informations, voir [Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md).

[![Affiche la page Hub Entreprise qui répertorie toutes les entreprises.](media/company-hub.png)](media/company-hub.png#lightbox)  

## Voir aussi

[Création de sociétés dans [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Environnements et des sociétés (en anglais uniquement)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Informations société](admin-company-information.md)  
[Centre d’administration Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
