---
title: Présentation des informations sur la société
description: 'La page Informations société spécifie les informations de base d’une entité commerciale, telles que le nom, les adresses et les informations d’expédition.'
author: edupont04
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: edupont
---

# Présentation des informations sur la société

[!INCLUDE[prod_short](includes/prod_short.md)] organise les entités commerciales en *sociétés*. Pour chaque société, vous devez remplir certains des détails de base et des informations pertinentes sur la page **Informations société**. Les informations de la page [**Informations société**](https://businesscentral.dynamics.com/?page=1) sont utilisées dans des documents, tels que les en-têtes facture. Vous pouvez paramétrer plusieurs sociétés, par exemple une société mère et une filiale.  

Si les entrepôts de la société sont situés à une adresse différente du siège social, vous pouvez renseigner les divers champs destinataire et le champ **Code magasin** du raccourci **Expédition**. Les informations de ces champs sont alors imprimées sur les commandes achat, afin que les livraisons soient effectuées à la bonne adresse.  

Pour chaque société que vous configurez, vous devez renseigner la page **Informations société**, ainsi que la page **Paramètres comptabilité**. Vous devez également configurer chaque zone dans [!INCLUDE [prod_short](includes/prod_short.md)], comme la page **Paramètres ventes**, pour chaque société. Pour plus d’informations, consultez [Aperçu des tâches permettant de paramétrer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

En fonction de votre pays, la page **Informations société** contient différents champs et raccourcis. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Le tableau suivant décrit les raccourcis les plus couramment utilisés.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Une fois que vous avez terminé de remplir les informations, vous pouvez fermer la page.  

## Travailler avec plusieurs entreprises

Si votre [!INCLUDE [prod_short](includes/prod_short.md)] inclut plusieurs sociétés, vos utilisateurs souhaitent peut-être utiliser des *badges de société* pour identifier rapidement et suivre avec quelle société ils travaillent actuellement. Pour en savoir plus, voir [Afficher un badge de société](#badge).

Il existe quelques fonctionnalités que vous pouvez utiliser pour changer d’entreprise, comme le sélecteur de société (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Pour plus d’informations, consultez [Passer à une autre entreprise ou un autre environnement](ui-organization-switch.md).

## <a name="badge"></a>Afficher un badge de société

Lorsqu’il y a plus d’une société ou d’un environnement, vous verrez le sélecteur d’entreprise sur le côté supérieur droit de la barre d’application, près de l’icône de recherche dans la barre d’application. Par défaut, le sélecteur de société utilise une icône d’entreprise standard, comme le ![Lanceur Icône de l’entreprise.](media/ui-experience/company-icon.png "Affiche l’icône de changement d’entreprise utilisée lorsqu’il n’y a qu’un seul environnement") et ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Affiche l’icône de changement d’entreprise utilisée lorsqu’il y a plusieurs environnements").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Affiche l’icône de changement de société dans l’en-tête du client Business Central.":::  

En utilisant la page **Informations sur la société**, vous pouvez remplacer l’icône standard de l’entreprise par un badge personnalisé pour chaque société si le badge de société permet aux utilisateurs d’identifier plus facilement la société dans laquelle ils travaillent.

1. Sur le raccourci **Badge société**, renseignez les champs, le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Cela fait, actualisez le navigateur (sélectionnez <kbd>Ctrl</kbd>+<kbd>F5</kbd>) pour mettre à jour le badge dans le client.  

> [!NOTE]
> Le sélecteur de société a été introduit dans la 2e vague de lancement 2022, version 21. Dans les versions antérieures, le badge de société n’était pas utilisé pour changer d’entreprise. Il s’affiche dans le coin supérieur droit de la plupart des pages, même lorsqu’il n’y a qu’une seule société. Le sélectionner affichera le nom complet de la société et le nom de l’environnement.

## Modifier le nom d’affichage de la société

Le nom de la société est toujours affiché dans le coin supérieur gauche et fonctionne comme une action que vous pouvez choisir pour revenir dans le Tableau de bord. Vous pouvez changer ce nom sur la page **Informations société**.

1. Choisissez l’icône ![Pignon pour ouvrir le menu Paramètres.](media/ui-experience/settings_icon_small.png) puis choisissez l’action **Informations société**.
2. Dans le champ **Nom**, saisissez le nom de la nouvelle société.
3. Quittez la page. Le système redémarre et affiche la nouvelle société dans le coin supérieur gauche.

## Expérience

L’expérience utilisateur par défaut dans une version d’évaluation de [!INCLUDE [prod_short](includes/prod_short.md)] ne révèle pas toutes les fonctionnalités. Vous pouvez passer à l’expérience complète dans la page **Informations société**. Pour plus d’informations, voir [Modifier les fonctionnalités affichées](ui-experiences.md).  

## Voir la [formation Microsoft](/training/modules/create-new-companies-dynamics-365-business-central/) associée

## Voir aussi

[Aperçu des tâches permettant de paramétrer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Démarrage rapide de Informations société](quick-start-company-information.md)  
[Configurer les informations société en Italie](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Création de sociétés](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
