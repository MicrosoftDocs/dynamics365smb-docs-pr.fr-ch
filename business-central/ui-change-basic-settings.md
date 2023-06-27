---
title: Modifier les paramètres de base pour l’utilisateur actuel
description: "Découvrez comment modifier certains paramètres de base dans Business\_Central, par exemple, votre rôle et votre centre de rôles, votre entreprise, votre date de travail et vos fuseaux horaires."
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: jswymer
---
# <a name="change-basic-settings" />Modifier les paramètres de base

Sur la page **Mes paramètres**, vous pouvez afficher et modifier les paramètres de base de votre [!INCLUDE[prod_short](includes/prod_short.md)]. Vos modifications affectent uniquement votre espace de travail, et non les espaces de travail des autres utilisateurs.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role" /><a name="role-center"></a>Rôle

Le rôle détermine la page d’accueil, un écran de démarrage conçu pour les exigences d’un rôle spécifique dans une organisation. Selon votre rôle, la page d’accueil ou le tableau de bord donne une vue d’ensemble de l’entreprise, de votre département ou de vos tâches personnelles. Il vous permet également d’accéder à vos tâches quotidiennes et de rechercher les tâches qui vous sont affectées.

* En haut, la navigation vous permet de permuter entre les clients, les fournisseurs, les articles et d’autres listes d’informations importantes. De même, les actions vous permettent de lancer des tâches, comme la création d’une facture vente, directement à partir de la page d’accueil.

* Le tableau de bord contient une zone **Activités** qui affiche les données actuelles, vous pouvez sélectionner pour afficher des informations plus détaillées. Les indicateurs de performance clés peuvent être configurés afin d’afficher un graphique sélectionné pour une représentation visuelle, par exemple, de la trésorerie ou des revenus et des dépenses. Vous pouvez également générer la liste des clients favoris sur la page d’accueil pour les comptes d’entreprise avec lesquels vous travaillez souvent ou auxquels vous devez accorder une attention particulière.

### <a name="change-the-role" />Modifier le rôle

Le rôle par défaut est **Gestionnaire d’activité**, mais vous pouvez sélectionner un autre rôle pour utiliser un Tableau de bord qui correspond mieux à vos besoins.  

1. Dans le coin supérieur droit, sélectionnez l’icône **Paramètres** ![Paramètres.](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis choisissez l’action **Mes paramètres**.
2. Sur la page **Mes paramètres**, dans le champ **Rôle** , sélectionnez le rôle que vous souhaitez utiliser par défaut. Par exemple, sélectionnez **Comptable**.
3. Cliquez sur **OK**.

## <a name="company" /><a name="company"></a>Société

Dans [!INCLUDE[prod_short](includes/prod_short.md)], une société fonctionne comme un conteneur de données. Il peut y avoir plusieurs sociétés dans une seule base de données, mais une seule peut être sélectionnée à la fois. La société par défaut est appelée CRONUS et contient uniquement des données de démonstration.

Le champ **Société** indique l’entreprise où vous travaillez actuellement et vous pouvez l’utiliser pour passer à une autre entreprise. Le nom de la société est toujours affiché dans le coin supérieur gauche et fonctionne comme une action que vous pouvez choisir pour revenir dans le Tableau de bord.

> [!TIP]
> Vous pouvez également changer la société à l’aide du sélecteur de société (Crtl+O). Pour plus d’informations sur cette fonctionnalité et sur les autres façons de changer d’entreprise ou d’environnement, voir [Passer à une autre entreprise ou à un autre environnement](ui-organization-switch.md).

La société par défaut est appelée CRONUS et contient uniquement des données de démonstration. Vous pouvez créer une nouvelle société avec des données personnalisées. Pour plus d’informations, voir [Création de sociétés](about-new-company.md).

<!--
### <a name="to-change-the-company-name" />To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information" /><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date" /><a name="work-date"></a>Date de travail

La date de travail la plus couramment utilisée est la date du jour. Vous pouvez être amené à modifier temporairement la date de travail pour effectuer des tâches telles que l’exécution de transactions à une date différente de la date du jour.

> [!TIP]  
> Dans tous les champs de date, tapez **t** pour entrer rapidement la date du jour et tapez **w** pour entrer rapidement la date de travail, qui est la valeur du champ **Date de travail** sur la page **Mes paramètres**.

> [!IMPORTANT]  
> Une fois la date de travail modifiée, si vous vous déconnectez ou si vous changez de société, les données de travail reviennent par défaut à la date de travail. Ainsi, la prochaine fois que vous vous connecterez ou lorsque vous reviendrez à la société d’origine, vous devrez peut-être redéfinir la date de travail.

### <a name="work-date-indication" />Indication de la date de travail

La date de travail est une information primordiale sur les pages qui peuvent être éditées. Chaque fois que la date de travail n’est pas définie sur la date du jour sur une page modifiable, deux types d’indicateurs apparaissent sur la page :

* Un rappel apparaît en haut de la page pour vous indiquer la date de travail. Le rappel fournit un lien direct vers le paramètre de la date de travail sur la page **Mes paramètres** de sorte que vous pouvez modifier la date si vous voulez. À partir du rappel, vous pouvez également choisir de l’annuler pour le reste de votre session. À moins que vous ne remplaciez la date de travail par « aujourd’hui », le rappel apparaîtra la prochaine fois que vous vous connecterez.

* Si vous refusez le rappel, la date de travail apparaîtra dans le titre de la page.  

Si la date de travail n’est pas définie sur la date actuelle (aujourd’hui), alors la date de travail actuelle s’affiche dans l’angle supérieur gauche sur toutes les pages sur lesquelles vous pouvez modifier les données.

## <a name="region" /><a name="region"></a> Région

Le paramètre **Région** détermine la manière dont les dates, heures, nombres et devises sont affichés ou mis en forme. Il détermine également quel caractère est utilisé comme séparateur décimal lors de l’utilisation d’un clavier numérique pour saisir des données. En savoir plus sur [Saisie de données](ui-enter-data.md#decimal).

## <a name="language" /><a name="language"></a> Langue

Modifie la langue d’affichage. Ce champ s’affiche uniquement lorsque vous avez le choix entre plusieurs langues.

La langue initiale est déterminée par l’administrateur ou par les paramètres de votre navigateur lorsque vous vous inscrivez à [!INCLUDE[prod_short](includes/prod_short.md)]. La langue définie est utilisée sur tous les appareils à partir desquels vous vous connectez, par exemple un téléphone ou une tablette.

Des langues supplémentaires pour [!INCLUDE[prod_short](includes/prod_short.md)] peuvent être installées à partir d’AppSource. Même si toutes les langues d’affichage prises en charge sont affichées dans la liste, l’administrateur doit installer l’application de langue appropriée sur l’abonné avant que les utilisateurs puissent passer à la nouvelle langue dans [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone" />Fuseau horaire

Définit le fuseau horaire dans lequel vous vous trouvez. Lorsque vous vous connectez pour la première fois à [!INCLUDE [prod_short](includes/prod_short.md)], le fuseau horaire est défini en fonction de l’adresse de votre entreprise. Modifiez-le s’il ne correspond pas à votre emplacement physique.  

## <a name="notifications" />Notifications

Sélectionnez le lien *Modifier quand je reçois une notification* pour afficher ou modifier les notifications que vous recevez au sujet de certains événements ou modification de statut, lorsque vous êtes sur le point de facturer un client avec des écritures échues, ou lorsque le stock disponible est inférieur à la quantité que vous êtes sur le point de vendre. En savoir plus sur [Gestion des notifications](ui-smart-notifications.md).

## <a name="teaching-tips" />Conseils d’apprentissage

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/personalize-ui-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Création de sociétés](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
