---
title: Configurer des modèles d’API
description: Décrit la procédure à suivre pour configurer des modèles d’API pour Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'API templates, configuring templates'
ms.search.form: 5469
ms.date: 06/07/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="configure-api-templates"></a>Configurer des modèles d’API

La bibliothèque d’API de [!INCLUDE[prod_short_md](includes/prod_short.md)] fournit une représentation simplifiée des entités sous-jacentes. Toutes les propriétés de l’application ne sont pas exposées via l’API associée. La page **Paramètres API** permet de définir des modèles qui sont utilisés pour remplir les propriétés vides d’une entité lorsque vous créez une action POST via l’API. 

Par exemple, si un modèle de configuration est défini pour l’entité article, lorsqu’un nouvel enregistrement d’article est créé via l’API de l’article, les propriétés du nouvel article qui ne sont pas définies dans l’appel de l’API sont remplies à partir du modèle sélectionné. Si, par exemple, aucune valeur n’est définie pour le champ **Groupe compta. produit** via l’API, mais une valeur est définie dans le modèle sélectionné, la valeur du groupe comptabilisation définie dans le modèle est appliquée au nouvel article. 

## <a name="setting-up-the-entity-template"></a>Configuration du modèle d’entité

Pour utiliser les modèles avec la bibliothèque d’API, vous devez d’abord configurer et définir les propriétés des modèles. Vous pouvez configurer ces modèles sur la page **Modèles configuration**. Pour plus d’informations, voir [Migrer des données locales vers Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) (en anglais uniquement) dans le contenu d’administration.  

## <a name="assign-the-template-to-an-api"></a>Affecter le modèle à une API

Pour affecter un modèle à une API, vous devez effectuer les actions suivantes.

> [!NOTE]  
> Les modèles d’API ne peuvent être configurés qu’avec les pages d’API suivantes : contacts, countriesRegions, currencies, customers, employees, itemCategories, paymentMethods, paymentTerms, shipmentMethods, unitsOfMeasure et vendors.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration API**, puis choisissez le lien associé.
2. Choisissez **Nouveau**, puis la valeur **Ordre** pour l’enregistrement.  

    Si plusieurs modèles sont sélectionnés pour une API (ID page), les modèles sont appliqués dans l’ordre défini dans la colonne **Ordre**.  

    Lorsque chaque modèle est appliqué, les valeurs de champ définies dans le modèle sont uniquement appliquées aux champs sans valeur déjà définie, soit explicitement dans l’API ou dans un modèle précédemment appliqué dans l’ordre.  
3. Sélectionnez une valeur **ID page**.  

    Il s’agit de la page de l’API à laquelle le modèle est appliqué. La recherche **ID page** fournit la liste de toutes les API disponibles dans la bibliothèque.
4. Sélectionnez une valeur dans le champ **Code modèle**.  

    Le code modèle est le code du modèle qui a été défini sur la page **Modèles configuration**. Les valeurs de modèle définies sont appliquées à l’API.  
5. Dans le champ **Conditions**, spécifiez le modèle à appliquer.  

    Le modèle défini est appliqué à un nouvel enregistrement créé via l’API si, et seulement si, les conditions définies dans le champ **Conditions** sont remplies par les valeurs déjà définies pour la nouvelle instance de l’entité.

## <a name="see-also"></a>Voir aussi

[Documentation sur les API](/dynamics-nav/fin-graph)  
[Développer les Connect Apps pour [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Activation des API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Points de terminaison des API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Administration](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
