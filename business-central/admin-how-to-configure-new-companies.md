---
title: Procédure de configuration de nouvelles sociétés | Microsoft Docs
description: Vous pouvez configurer et personnaliser une nouvelle société que vous avez créée. Pour détailler votre implémentation, vous procédez en trois phases pour terminer votre configuration.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f0964028b7d6e711e48e1361950d1ec6b4e14425
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130815"
---
# <a name="configure-new-companies"></a>Configurer de nouvelles sociétés
Pour configurer une nouvelle société dans votre implémentation de la solution, vous suivez habituellement trois phases. Dans la première phase, vous importez le package configuration, un fichier .rapidstart avec les informations de configuration. Dans la deuxième phase, vous modifiez les informations de configuration, puis vous les appliquez à votre nouvelle société. Dans la phase finale, vous vérifiez et corrigez les erreurs.  

Les procédures suivantes supposent que vous avez créé et enregistré un package configuration. Pour plus d’informations, voir [Préparer un package configuration](admin-how-to-prepare-a-configuration-package.md).  

Les procédures suivantes supposent que vous avez initialisé et ouvert votre nouvelle société et que vous utilisez le tableau de bord Administration.

## <a name="before-you-import-a-configuration-package"></a>Avant d’importer un package de configuration
Avant d’importer un package de configuration, il est judicieux de vérifier que les affirmations suivantes sont respectées. Sinon, vous ou votre client ne pourrez pas importer le package de configuration.

* Votre licence inclut les tables que vous mettez à jour. En cas de doute, la page **Feuille configuration** peut vous aider. Si votre licence inclut les tables, le champ **Table sous licence** est coché.  
* L’utilisateur qui importe le package de configuration dispose des autorisations effectives d’insertion et de modification sur toutes les tables que le package va mettre à jour. Pour plus d’informations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). 

## <a name="to-import-a-configuration-package"></a>Pour importer un package configuration  
1. Ouvrez la nouvelle société dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)].  
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Packages de configuration**, puis sélectionnez le lien associé.  
3. Sélectionnez l’action **Importer package**.  
4. Accédez à l’emplacement où vous avez enregistré le fichier du package de configuration .rapidstart, puis sélectionnez le bouton **Ouvrir**.  
5. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Informations société**, puis choisissez le lien associé. Entrez les informations sur la société dans la fiche Informations société. Incluez des informations, telles que les coordonnées bancaires. Vous pouvez également fournir un logo pour la société.  

Toutes les tables que vous avez désignées pour les inclure à la nouvelle société sont importées. À ce stade, vous pouvez lettrer les données de package dans la base de données, ou ajuster et modifier les données de table pour répondre aux spécifications du client.  

## <a name="to-apply-package-data"></a>Pour appliquer les données de package  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez une table pour laquelle vous souhaitez modifier les données, puis sélectionnez l’action **Appliquer données**. Cliquez sur le bouton **Oui** pour confirmer l’application.
3. Pour confirmer que les données se trouvent maintenant dans la base de données et que l’application a réussi, revenez à la page **Feuille config** et sélectionnez l’action **Données base de données**.  

> [!NOTE]  
>  Après l’application des données, vous pouvez uniquement les visualiser dans la base de données. Elles ne se trouvent plus dans le package.  

## <a name="to-modify-and-apply-package-data"></a>Pour modifier et appliquer les données de package  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez une table pour laquelle vous souhaitez modifier les données, puis sélectionnez l’action **Données package**.  
3. Sur la page **Enregistrements package config.**, effectuez vos modifications. Par exemple, vous pouvez supprimer des options qui ne s’appliquent pas.  
4. Sélectionnez l’action **Appliquer données**, puis le bouton **OK**.  
5. Pour confirmer que les données se trouvent maintenant dans la base de données et que l’application a réussi, revenez à la page **Feuille config** et sélectionnez l’action **Données base de données**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Pour trouver et identifier une erreur de configuration  
Il existe certains types d’erreurs qui surviennent lorsque vous appliquez des données à une base de données. L’erreur la plus commune est que les tables associées requises ne soient pas incluses. Vous corrigez ces erreurs dans la feuille de configuration.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Packages de configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez le package que vous souhaitez examiner, puis sélectionnez l’action **Modifier**.  

    Toute table présentant des erreurs est mise en surbrillance. Le nombre d’erreurs de package est affiché dans le champ **Nombre erreurs package**.  

3. Choisissez le champ **Nombre erreurs package** pour ouvrir la page **Enregistrements package config.**, qui répertorie les enregistrements contenant des erreurs.  

### <a name="to-fix-an-error"></a>Pour corriger une erreur  
1. Ouvrez la société basée sur votre package configuration.  
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille de calcul de configuration**, puis sélectionnez le lien associé.  
3. Corrigez les erreurs, par exemple ajoutez des tables liées manquantes à la feuille.  
4. Ajoutez les tables au package configuration existant, ou créez un package qui contient uniquement les nouvelles tables. Pour plus d’informations, voir [Préparer un package configuration](admin-how-to-prepare-a-configuration-package.md).  
5. Rouvrez la nouvelle société pour laquelle vous implémentez la configuration.  
6. Importez le package configuration.  

    > [!NOTE]  
    >  Si vous importez le même package à nouveau, vous pouvez remplacer toutes les modifications des données que vous avez déjà apportées. Pour ce motif, vous pouvez ajouter toutes les nouvelles tables dans un nouveau package, et les importer.  

7. Appliquez les données dans la base de données, comme décrit dans [Pour modifier et appliquer les données de package](admin-how-to-configure-new-companies.md#to-modify-and-apply-package-data).

## <a name="see-also"></a>Voir aussi  
[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]