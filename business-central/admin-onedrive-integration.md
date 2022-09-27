---
title: Gestion de l’intégration de OneDrive avec Business Central
description: Découvrez ce que vous pouvez faire pour gérer une intégration entre Business Central et OneDrive Entreprise.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: c55abae59196d896b48a7b656e7fb7c4c7734fa8
ms.sourcegitcommit: 2396dd27e7886918d59c5e8e13b8f7a39a97075d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524557"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Gestion de l’intégration de OneDrive avec Business Central

Cet article fournit un aperçu de ce que peut faire un administrateur pour contrôler l’intégration de OneDrive Entreprise avec [!INCLUDE[prod_short](includes/prod_short.md)]. Les clients en ligne de [!INCLUDE[prod_short](includes/prod_short.md)] bénéficient d’une intégration automatique, sans configuration supplémentaire requise, pour utiliser ces fonctionnalités. 

## <a name="minimum-requirements"></a>Configuration minimale requise

* Chaque utilisateur doit avoir une licence pour [!INCLUDE[prod_short](includes/prod_short.md)] et OneDrive dans le cadre d’un plan Microsoft 365.
* OneDrive doit être configuré pour chaque utilisateur.

## <a name="governance"></a>Gouvernance

Le centre d’administration SharePoint offre un contrôle étendu sur les politiques qui régissent l’utilisation de OneDrive dans toute l’organisation. Les administrateurs généraux ou les utilisateurs qui ont le rôle d’administrateur de SharePoint peuvent configurer des politiques qui déterminent qui peut accéder à OneDrive, quel est le lieu de résidence des données, le cycle de vie du contenu et bien plus encore. Les liens suivants fournissent des informations sur les fonctionnalités et les paramètres souvent utilisés qui peuvent améliorer votre intégration avec [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Gérer les paramètres de partage](/sharepoint/turn-external-sharing-on-or-off)
* [Utiliser des barrières d’information avec SharePoint](/sharepoint/information-barriers)
* [En savoir plus sur la prévention des pertes de données](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Définir l’espace de stockage par défaut pour les utilisateurs de OneDrive](/onedrive/set-default-storage-space)
* [Ajouter et supprimer des administrateurs pour le OneDrive d’un utilisateur](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Désactiver la création OneDrive pour certains utilisateurs](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Fonctionnalités multi-régions dans OneDrive et SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Certaines fonctionnalités peuvent être disponibles uniquement pour certains plans.

## <a name="managing-privacy"></a>Gestion de la confidentialité

Les administrateurs et les utilisateurs finaux contrôlent le contenu stocké dans OneDrive, et ces données appartiennent uniquement à votre organisation. Pour plus d’informations, consultez [Comment SharePoint et OneDrive protègent vos données dans le cloud](/sharepoint/safeguarding-your-data). Vous pouvez également consulter notre [Déclaration de confidentialité de Microsoft](https://privacy.microsoft.com/en-us/privacystatement), qui explique les données que Microsoft traite, comment Microsoft les traite, et à quelles fins.

## <a name="restoring-onedrive-and-prod_short"></a>Restauration de OneDrive et [!INCLUDE[prod_short](includes/prod_short.md)]

Dans le cadre d’un exercice de reprise après sinistre, les administrateurs peuvent avoir besoin de restaurer un environnement [!INCLUDE[prod_short](includes/prod_short.md)] conformément à une sauvegarde d’un moment passé et de synchroniser le stockage OneDrive sur ce même moment. OneDrive fournit divers outils pour cela, tels que la restauration du OneDrive d’un utilisateur à un moment antérieur, la restauration d’une version antérieure d’un fichier individuel, ou la restauration de fichiers supprimés. Pour en savoir plus, consultez les articles suivants :

* Pour [!INCLUDE[prod_short](includes/prod_short.md)], consultez [Restauration d’un environnement dans le centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Pour OneDrive, consultez [Restauration de votre OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Configuration de Business Central local

Un administrateur doit établir la connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] sur site et OneDrive. Contrairement à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, la connexion n’est pas automatique. Si la connexion n’est pas configurée, les utilisateurs ne peuvent pas utiliser les fonctionnalités pour OneDrive.

[!INCLUDE[prod_short](includes/prod_short.md)] sur site ne peut être connecté qu’à un OneDrive hébergé par Microsoft dans le cloud. La connexion de [!INCLUDE[prod_short](includes/prod_short.md)] sur site au référentiel Mes sites du serveur SharePoint n’est pas prise en charge.

> [!IMPORTANT]
> En configurant cette fonctionnalité, vous activez également les fonctionnalités héritées qui envoient des fichiers à OneDrive.  
>
>* La fonction Ouvrir dans Excel copiera automatiquement le fichier Excel dans OneDrive, puis l’ouvrira dans Excel Online. 
>* L’exportation de tout rapport vers un fichier copiera automatiquement le fichier dans OneDrive, puis l’ouvrira dans Excel Online, Word Online ou OneDrive. 
>* D’autres fonctionnalités peuvent également s’ouvrir automatiquement dans OneDrive.

### <a name="prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Préparer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour se connecter à OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Ajoutez une application enregistrée pour Business Central dans votre locataire Azure AD de votre plan Microsoft 365. Comme d′autres services Azure qui fonctionnent avec Business Central, OneDrive nécessite une inscription d′application dans Azure Active Directory (Azure AD). L’enregistrement de l’application fournit des services d’authentification et d’autorisation entre Business Central et SharePoint, qui sont utilisés par OneDrive.

Configurez l’application enregistrée avec les autorisations suivantes déléguées à l’API SharePoint :

- AllSites.FullControl
- User.ReadWrite.All 

Pour la 2e vague de lancement 2021 de Business Central (version 19), définissez plutôt les autorisations suivantes :

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Vous effectuez ce travail dans le portail Azure. Assurez-vous de copier l’ID d’application (client) et le secret client utilisés par l’application enregistrée. Vous aurez besoin de ces informations dans la tâche suivante.

Pour plus d’informations sur la configuration requise d’un compte, l’enregistrement d’une application et la configuration des autorisations, consultez [Enregistrer une application dans Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) dans l’Aide destinée aux développeurs et aux professionnels de l’informatique.

> [!TIP]
> Si vous avez déjà enregistré une application dans le cadre d’une intégration avec un autre produit Microsoft, tel que Power BI, vous pouvez alors réutiliser cet enregistrement d’application. Dans ce cas, vous n’aurez qu’à définir les autorisations SharePoint.

### <a name="set-up-the-connection-in-prod_short-on-premises"></a>Établir la connexion dans [!INCLUDE[prod_short](includes/prod_short.md)] sur site

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion à Microsoft SharePoint**, puis choisissez le lien associé.
2. Dans le champ **Description**, saisissez une description de la connexion, telle que **OneDrive**.
3. Dans le champ **Dossier**, entrez **Business Central**.
4. Dans le champ **Emplacement**, entrez l’URL de votre OneDrive.

    L’URL d’un OneDrive est généralement au format suivant :`https://<tenant name>-my.sharepoint.com`. Pour plus d’informations, consultez [URL OneDrive des utilisateurs de votre organisation](/onedrive/list-onedrive-urls) dans la documentation OneDrive.
5. Dans le champ **ID client**, entrez l’ID client de votre enregistrement d’application.
6. Dans le champ **Secret client**, entrez le secret client de votre enregistrement d’application. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> La page Configuration de la connexion SharePoint est utilisée pour configurer plusieurs fonctionnalités héritées. La section **Général** configure la connexion à OneDrive, et la section **Documents partagés** redirige les fichiers vers SharePoint. L’ancienne fonctionnalité SharePoint sera obsolète dans un proche avenir. Nous vous recommandons de ne pas configurer la section **Documents partagés**.

## <a name="see-also"></a>Voir aussi

[Intégration de Business Central et OneDrive Entreprise](across-onedrive-overview.md)  
[Ouverture des fichiers Business Central dans OneDrive](across-share-onedrive.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
