---
title: Gestion de l’intégration de OneDrive avec Business Central
description: Découvrez ce que vous pouvez faire pour gérer une intégration entre Business Central et OneDrive Entreprise.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a>Gestion de l’intégration de OneDrive avec Business Central

Cet article fournit un aperçu de ce que peut faire un administrateur pour contrôler l’intégration de OneDrive Entreprise avec [!INCLUDE[prod_short](includes/prod_short.md)]. Les clients en ligne de [!INCLUDE[prod_short](includes/prod_short.md)] bénéficient d’une intégration automatique, sans configuration supplémentaire requise, pour utiliser les fonctionnalités d’uverture et de partage de OneDrive. Avec le guide de configuration assistée **Configuration de OneDrive**, vous pouvez donner aux utilisateurs l’accès à encore plus de fonctionnalités de OneDrive, comme l’ouverture d’un fichier Excel dans OneDrive (ou vous pouvez même désactiver toutes les fonctionnalités).  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Configurer OneDrive pour l’intégration avec Business Central

Cette section traite des exigences qui doivent être satisfaites dans OneDrive Entreprise pour configurer l’intégration avec Business Central et la tâche que vous pouvez effectuer pour gérer l’intégration.

### <a name="minimum-requirements"></a>Configuration minimale requise

* Chaque utilisateur doit avoir une licence pour [!INCLUDE[prod_short](includes/prod_short.md)] et OneDrive dans le cadre d’un plan Microsoft 365.
* OneDrive doit être configuré pour chaque utilisateur.

### <a name="managing-privacy"></a>Gestion de la confidentialité

> [!IMPORTANT]
> Si vous avez choisi de déployer Business Central et OneDrive dans différents pays ou régions, les fichiers générés par Business Central et placés dans OneDrive peuvent franchir les limites de résidence des données. Assurez-vous de vérifier les politiques de votre organisation et les exigences de conformité de votre gouvernement concernant la résidence des données avant d’activer la connexion à OneDrive.

Les administrateurs et les utilisateurs finaux contrôlent le contenu stocké dans OneDrive, et ces données appartiennent uniquement à votre organisation. Pour plus d’informations, consultez [Comment SharePoint et OneDrive protègent vos données dans le cloud](/sharepoint/safeguarding-your-data). Vous pouvez également consulter notre [Déclaration de confidentialité de Microsoft](https://privacy.microsoft.com/en-us/privacystatement), qui explique les données que Microsoft traite, comment Microsoft les traite, et à quelles fins.

En activant cette connexion de service, vous acceptez :

(a) de partager les données de Dynamics 365 Business Central avec le fournisseur de services, qui les utilisera conformément à ses conditions et à sa politique de confidentialité ; (b) les niveaux de conformité du fournisseur de services peuvent être différents de ceux de Dynamics 365 Business Central ; et (c) Microsoft peut partager vos coordonnées avec ce fournisseur de services si c’est nécessaire au fonctionnement et à la résolution des problèmes du service.

## <a name="configure-business-central"></a>Configurer Business central

Avec Business Central Online, la connexion entre Business Central et OneDrive est automatiquement configurée pour vous, et les fonctionnalités de OneDrive sont facilement accessibles aux utilisateurs par défaut. Si vous souhaitez désactiver certaines ou toutes les fonctionnalités, vous pouvez utiliser le guide de configuration assistée **Configuration de OneDrive** dans le client Business Central.

La configuration de Business Central sur site est différente, car la connexion entre Business Central et OneDrive n’est pas configurée pour vous. Vous devrez le faire manuellement. Pour plus d’informations, consultez [Configurer l’intégration de OneDrive avec Business Central sur site](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>À propos des environnements multiples

L’intégration de OneDrive est configurée par environnement, c’est-à-dire que vos paramètres s’appliqueront à toutes les entreprises de cet environnement. Si votre organisation possède plusieurs environnements, vous devrez configurer l’intégration de OneDrive pour chacun.

### <a name="prerequisites"></a>Conditions préalables

- Autorisation indirecte de modification et de suppression (imd) sur la table **Scénario de service de documents** au minimum

### <a name="configure-onedrive-using-onedrive-setup"></a>Configurer OneDrive à l’aide de la Configuration de OneDrive

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configurer OneDrive**, puis choisissez le lien associé. 
2. La première fois que vous exécutez la configuration assistée, vous verrez **Votre vie privée**. Lisez les informations de la page et, si vous êtes d’accord avec les conditions générales, sélectionnez **Accepter** pour continuer.
3. Sur la page **Configurer la gestion des fichiers**, vous avez le choix entre les options suivantes :

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Sélectionnez **Suivant**>**Terminé**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Passer à la nouvelle intégration de OneDrive après la mise à niveau

La configuration assistée **Configuration de OneDrive** a été introduite dans la version 21.0 de la 2e vague de lancement 2022. Auparavant, l’intégration de OneDrive utilisait la **Configuration de la connexion SharePoint**, qui est obsolète et sera supprimée dans la deuxième vague de lancement 2023, version 23.0. Après avoir effectué la mise à niveau vers la version 21,OneDrive fonctionnera toujours comme avant. Mais nous vous recommandons de passer à la nouvelle intégration de OneDrive. Faire ce changement maintenant facilitera la tâche lorsque la **Configuration de la connexion SharePoint** sera finalement supprimé. De plus, cela vous permettra d’utiliser le guide de configuration assistée **Configuration de OneDrive** pour gérer les fonctionnalités OneDrive accessibles aux utilisateurs. La configuration assistée **Configuration de OneDrive** rend la transition entre l’ancienne configuration de SharePoint et la nouvelle simple et transparente.

Pour passer de l’un à l’autre, il suffit d’ouvrir et d’exécuter la configuration assistée **Configuration de OneDrive**, ou d’ouvrir la page **Configuration de la connexion SharePoint** et de sélectionner **Accéder à la nouvelle configuration de OneDrive** dans la notification en haut de la page. Suivez le guide de configuration, comme décrit dans la section précédente.

## <a name="restoring-onedrive-and-"></a>Restauration de OneDrive et [!INCLUDE[prod_short](includes/prod_short.md)]

Dans le cadre d’un exercice de reprise après sinistre, les administrateurs peuvent avoir besoin de restaurer un environnement [!INCLUDE[prod_short](includes/prod_short.md)] Online conformément à une sauvegarde d’un moment passé et de synchroniser le stockage OneDrive sur ce même moment. OneDrive fournit divers outils de récupération, tels que la restauration du OneDrive d’un utilisateur à un moment antérieur, la restauration d’une version antérieure d’un fichier individuel, ou la restauration de fichiers supprimés. Pour en savoir plus, consultez les articles suivants :

* Pour [!INCLUDE[prod_short](includes/prod_short.md)], consultez [Restauration d’un environnement dans le centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Pour OneDrive, consultez [Restauration de votre OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

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

## <a name="see-also"></a>Voir aussi

[Intégration de Business Central et OneDrive Entreprise](across-onedrive-overview.md)  
[Ouverture des fichiers Business Central dans OneDrive](across-share-onedrive.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
