---
title: Gérer la personnalisation en tant qu'administrateur dans Business Central | Microsoft Docs
description: Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250610"
---
# <a name="managing-personalization-as-an-administrator"></a>Gérer la personnalisation en tant qu'administrateur

 Les utilisateurs peuvent personnaliser leur espace de travail en fonction de leurs propres préférences. En tant qu'administrateur, vous contrôlez et gérez la personnalisation comme suit :

-   En activant ou désactivant la personnalisation pour l'intégralité de l'application (installation locale uniquement).
-   En activant ou désactivant la personnalisation pour les utilisateurs d'un profil spécifique.
-   En annulant toute personnalisation de page effectuée par les utilisateurs.

## <a name="EnablePersonalization"></a>Pour activer ou désactiver la personnalisation (en local uniquement)

Par défaut, la personnalisation n'est pas activée dans le client. Vous activez ou désactivez la personnalisation en modifiant le fichier de configuration (navesttings.json) de l'instance du serveur Web Business Central qui dessert les clients.

1. Pour activer la personnalisation, ajoutez la ligne suivante dans le fichier navsettings.json :

    ```
    "PersonalizationEnabled": "true"
    ```

    Pour désactiver la personnalisation, supprimez cette ligne ou changez-la avec :

    ```
    "PersonalizationEnabled": "false"
    ```

    Pour plus d'informations sur la procédure visant à modifier le fichier navsettings.json, reportez-vous à la rubrique [Modifier directement le fichier navsettings.json](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)

2. Générez et téléchargez les symboles d'application.

    Cette étape est facultative, et non requise pour activer la personnalisation. Toutefois, elle veille à ce que les nouvelles pages qui sont créées par les développeurs puissent être personnalisées.

    1. Tout d'abord, vous générez les symboles en exécutant finsql.exe avec la commande `generatesymbolreference`. Le fichier finsql.exe se situe dans le dossier d'installation pour le [!INCLUDE[server](includes/server.md)] et Dynamics NAV Development Environment (CSIDE). Pour générer les symboles, ouvrez une invite de commande, passez au répertoire où est enregistré le fichier, et exécutez la commande suivante :

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Par exemple :

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Pour plus d'informations, reportez-vous à la rubrique [Exécution de C/SIDE et d'AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Configurez l'instance [!INCLUDE[nav_server_md](includes/nav_server_md.md)] sur **Activer l'importation des références de symbole d'application au démarrage du serveur** (EnableSymbolLoadingAtServerStartup). Pour plus d'informations, reportez-vous à la rubrique [Configuration de Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Pour désactiver la personnalisation pour un profil

Vous pouvez empêcher tous les utilisateurs appartenant à un profil spécifique de personnaliser leurs pages.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Profils**, puis sélectionnez le lien associé.
2. Sélectionnez dans la liste le profil à modifier.
3. Activez la case à cocher **Désactiver la personnalisation**, puis cliquez sur le bouton **OK**.

## <a name="to-clear-user-personalizations"></a>Pour annuler les personnalisations des utilisateurs

L'effacement de la personnalisation de la page rétablit la page à sa disposition d'origine, antérieure à toute personnalisation. Il y a deux méthodes pour effacer les personnalisations de page effectuées par les utilisateurs : en utilisant la page **Supprimer la personnalisation utilisateur** et en utilisant la page **Fiche de personnalisation utilisateur**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Pour annuler les personnalisations effectuées par les utilisateurs à l'aide de la page Supprimer la personnalisation utilisateur

La page **Supprimer la personnalisation utilisateur** permet d'effacer les personnalisations par page et par utilisateur individuellement.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer la personnalisation utilisateur**, puis sélectionnez le lien associé.

    La page répertorie toutes les pages qui ont été personnalisées et l'utilisateur auquel elles appartiennent.

    >[!NOTE]
    > Une coche dans la colonne **Personnalisation héritée** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[d365fin](includes/d365fin_md.md)], qui a traité la personnalisation de manière différente. Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu'ils ne choisissent de déverrouiller la page. Pour plus d'informations, voir [Pourquoi la personnalisation d'une page est bloquée](ui-personalization-locked.md).

2. Sélectionnez l'écriture à supprimer, puis sélectionnez l'action **Supprimer**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Pour annuler les personnalisations utilisateur à l'aide de la page Fiche de personnalisation utilisateur

La page **Fiche de personnalisation utilisateur** permet d'effacer la personnalisation de toutes les pages d'un utilisateur spécifique. Cela nécessite l'autorisation d'écriture dans la table 2000000072 **Profil**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Personnalisation utilisateur**, puis sélectionnez le lien associé.

    La page **Personnalisation utilisateur** répertorie tous les utilisateurs qui ont potentiellement des pages personnalisées. Si vous ne trouvez pas un utilisateur dans la liste, cela signifie qu'ils n'a aucune page personnalisée.

2. Sélectionnez l'utilisateur dans la liste, puis sélectionnez l'action **Modifier**.

3. Sous l'onglet **Actions**, choisissez **Effacer les pages personnalisées**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

## <a name="see-also"></a>Voir aussi
[Personnalisation de votre espace de travail](ui-personalization-user.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
