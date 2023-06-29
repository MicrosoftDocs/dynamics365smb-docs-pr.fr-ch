---
title: Environnements Sandbox
description: 'Découvrez comment un environnement dédié peut vous aider à explorer, apprendre, démontrer, développer, résoudre les problèmes et tester Business Central en toute sécurité.'
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sandbox, demo, develop'
ms.date: 12/20/2021
ms.author: solsen
---
# <a name="sandbox-environments-in-"></a><a name="sandbox-environments-in-"></a>Environnements Sandbox dans [!INCLUDE[prod_short](includes/prod_short.md)]

Avec [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous pouvez facilement obtenir un environnement sûr dans lequel vous pouvez tester, former ou résoudre les problèmes sans perturber les processus de travail ou les données métier de votre société. Cet environnement hors production est appelé *sandbox*. Isolé de la production, un environnement Sandbox est l’emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.  

> [!TIP]
> Avez-vous atterri sur cet article après avoir choisi le nom de votre environnement [!INCLUDE [prod_short](includes/prod_short.md)] dans la barre du haut ? Actuellement, vous ne pouvez pas modifier le nom ou l’environnement de cette façon. Au lieu de cela, vous devez demander à votre administrateur de modifier le nom ou lui demander de partager le lien vers un autre environnement.

Votre administrateur gère les environnements sandbox dans le [centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Par exemple, si vous souhaitez créer un environnement sandbox à des fins d’évaluation, votre administrateur peut créer un environnement dédié dans le centre d’administration. Pour plus d’informations, voir [Environnements de production et sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types) dans le contenu pour développeurs et administrateurs.  

Vous pouvez également utiliser les environnements sandbox en toute sécurité pour la formation, par exemple pour suivre un parcours d’apprentissage de la [formation Microsoft](/training/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), car c’est un environnement sûr pour l’expérimentation. Si un problème se produit, supprimez simplement l’environnement sandbox et recommencez.  

Une fois que vous avez terminé, vous pouvez supprimer l’environnement sandbox, en utilisant le centre d’administration.  

> [!NOTE]
> Techniquement, les environnements sandbox sont très différents des environnements de production. Votre administrateur peut créer un sandbox qui inclut des données de production, mais qui demeure un sandbox, et vous ne pourrez pas demander une exportation de la base de données, par exemple. Pour plus d’informations, voir [Environnements sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) dans le contenu pour développeurs et administrateurs.

L’environnement sandbox n’est pas moins utile, car il comprend quelques fonctionnalités pratiques :

* [Expérience utilisateur avancée](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Concepteur](#designer)  

## <a name="advanced-user-experience"></a><a name="advanced-user-experience"></a>Expérience utilisateur avancée

Il est possible d’activer et de tester la fonctionnalité complète de la version standard de [!INCLUDE[prod_short](includes/prod_short.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société** sur *Premium*. Trouvez la page **Informations société** dans le menu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Icône Paramètres."::: .  

Après avoir activé l’expérience utilisateur *Premium*, vous avez accès à tous les profils (rôles) et tableaux de bord standard dans la version standard. Vous pouvez également contacter un partenaire revendeur pour une démonstration des fonctionnalités. Pour plus d’informations, voir [Comment trouver un partenaire revendeur ?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a><a name="complete-sample-data"></a>Exemples de données complets

Pour les situations où vous avez besoin d’exemples de données supplémentaires, veuillez vous adresser à votre partenaire revendeur.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a><a name="designer"></a>Concepteur

Dans un environnement sandbox, la fonctionnalité **Concepteur** est activée. Vous pouvez activer Concepteur en sélectionnant l’icône de conception ![Concepteur.](./media/across-sandbox/sandbox-inclient-design-icon.png) sur une page, ou en choisissant l’élément de menu **Conception** dans le menu ![Paramètres](media/ui-experience/settings_icon_small.png).  

Pour plus d’informations, voir [Utiliser le concepteur](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) dans le contenu dédié à l’équipe Administration et aux développeurs (en anglais uniquement).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/admin-online-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Versions d’évaluation et abonnements [!INCLUDE[prod_long](includes/prod_long.md)]](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions)  
[Gestion des environnements dans le centre d’administration de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Environnements de production et sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
