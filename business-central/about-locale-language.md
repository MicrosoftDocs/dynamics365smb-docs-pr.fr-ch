---
title: Multilingue et localisation
description: Découvrez comment la langue et la région influencent votre expérience dans Business Central. Modifier la langue de l’interface utilisateur dans Mes paramètres.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'language, locale, localization, culture, region, regional settings'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Modification de la langue et de la région

[!INCLUDE[prod_short](includes/prod_short.md)] est disponible dans plusieurs marchés et langues à travers le monde. Sur les marchés où [!INCLUDE[prod_short](includes/prod_short.md)] est disponible, des fonctionnalités réglementaires sont disponibles pour aider les entreprises avec des charges réglementaires. [!INCLUDE[prod_short](includes/prod_short.md)] peut s’afficher dans différentes langues. Vous pouvez même changer la langue utilisée pour afficher les textes. La modification est immédiate une fois que vous avez été automatiquement déconnecté et reconnecté. Le paramètre ne s’applique qu’à vous et non aux autres utilisateurs de votre société.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Par exemple, vous utilisez la version canadienne de [!INCLUDE[prod_short](includes/prod_short.md)]. Cela signifie que vous pouvez voir l’interface utilisateur en anglais, allemand, français ou une autre langue, mais il s’agit toujours de la version canadienne de [!INCLUDE[prod_short](includes/prod_short.md)]. Ce n’est pas la même chose que [!INCLUDE[prod_short](includes/prod_short.md)] en allemand où la fonctionnalité a été adaptée aux exigences de ce marché.  

Pour modifier la langue de l’interface utilisateur, accédez à la page **Mes paramètres**. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Le choix des langues sera réinitialisé à votre réglage sur votre profil Microsoft 365 si votre administrateur synchronise les utilisateurs de Microsoft 365 à [!INCLUDE[prod_short](includes/prod_short.md)].

Vous ne pouvez pas modifier les textes stockés en tant que données d’application. Il s’agit par exemple de textes tels que le nom des articles du stock ou les commentaires concernant un client. En d’autres termes, ces types de texte ne sont pas traduits.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] ne prend en charge qu’un jeu de caractères unique pour les données. Aussi, il se peut que certains caractères ne soient pas pris en charge dans votre environnement et vous pouvez rencontrer des problèmes de récupération des données saisies à l’aide d’un autre jeu de caractères. Par exemple, votre environnement peut prendre en charge les caractères anglais et russes uniquement. Dans ce cas, si vous entrez des données dans une autre langue, il se peut que celles-ci ne soient pas stockées correctement. Vous devez contacter votre administrateur système pour connaître les langues prises en charge pour votre client [!INCLUDE[prod_short](includes/prod_short.md)].  

## Modification de votre paramètre de région

La région diffère des exigences linguistiques et légales des marchés locaux. La région détermine la manière dont vos données s’affichent, comme le séparateur de décimales, et la manière dont le texte est aligné à gauche ou à droite. La région détermine également certains éléments du système dans le navigateur, comme l’action pour créer un élément dans une liste.  

Vous pouvez modifier la région dans l’onglet du navigateur que vous utilisez pour travailler dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les modifications ne s’appliquent qu’à vous et non aux autres utilisateurs de votre société.  Le choix de la région sera réinitialisé à votre réglage sur votre profil Microsoft 365 si votre administrateur synchronise les utilisateurs de Microsoft 365 à [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> Lorsque vous modifiez la région, une longue liste de langues et de régions s’affiche. Cependant, la langue n’est pas influencée par le choix de la région.  

Pour modifier la région, accédez à la page **Mes paramètres**. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).  

## Modification du paramètre de région pour les clients, les contacts et les fournisseurs

Certaines entreprises utilisent un service externe qui valide les informations d’adresse dans leur pays ou leur région. Cependant, lorsque vous devez mettre à jour les informations d’adresse, l’approche structurée utilisée par ces services peut ne pas toujours convenir à certains scénarios. Business Central offre un moyen plus flexible de saisir les détails de l’adresse.

Sur la page **Paramètres comptabilité**, si vous activez le bouton à bascule **Exiger un code pays/région dans l’adresse**, les modifications apportées au champ **Code pays/région** des adresses des clients, des contacts ou des fournisseurs réinitialiseront les valeurs des autres champs d’adresse.

## Version de l’application

Dans la page **Aide et support**, vous pouvez voir quelle version de [!INCLUDE[prod_short](includes/prod_short.md)] utilise votre entreprise. Si vous souhaitez baser une entreprise sur une version différente, votre administrateur peut créer un nouvel environnement de production. Pour plus d’informations, voir [Créer un nouvel environnement de production](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) dans le contenu pour les développeurs et les professionnels de l’informatique.  

## Langues de l’aide de [!INCLUDE[prod_short](includes/prod_short.md)]

Le contenu de l’aide de la version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)] publié sur Microsoft Learn. Le contenu est disponible dans différentes langues. Si vous accédez à la documentation à partir de [!INCLUDE[prod_short](includes/prod_short.md)], le contenu s’affichera dans votre langue. Par défaut, si une page spécifique n’est pas encore disponible dans votre langue, elle s’affichera en anglais.

### Comment changer la langue du site Microsoft Learn ?

C’est simple - accédez au bas de la page du navigateur et choisissez le symbole de globe dans le coin inférieur gauche.

> [!NOTE]  
> La liste indique toutes les langues qui sont prises en charge par le site Microsoft Learn. [!INCLUDE[prod_short](includes/prod_short.md)] est disponible dans un nombre limité de pays/régions, et le contenu de l’aide [!INCLUDE [prod_short](includes/prod_short.md)] n’est pas disponible dans toutes les langues prises en charge par le site Microsoft Learn.

## Voir aussi

[Ressources pour l’Aide et le support](product-help-and-support.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]