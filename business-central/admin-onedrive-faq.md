---
title: FAQ sur OneDrive Entreprise
description: "Obtenez des réponses à certaines questions courantes sur l’utilisation de OneDrive Entreprise et de Business\_Central."
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
---
# <a name="onedrive-for-business-faq" />FAQ sur OneDrive Entreprise

[!INCLUDE [online_only](includes/online_only.md)]

Cet article répond à certaines des questions que vous pourriez vous poser sur l’utilisation de OneDrive et [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all--clients" />Est-ce que ça marche avec tous mes clients [!INCLUDE[prod_short](includes/prod_short.md)] ?

Oui. Vous pouvez ouvrir des fichiers dans OneDrive depuis les applications mobiles [!INCLUDE[prod_short](includes/prod_short.md)], lors de l’affichage des détails de carte dans Microsoft Teams, ou même à partir du complément Outlook.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files" />Est-ce que OneDrive est identique à SharePoint pour stocker des fichiers ?

Dans le cadre de votre abonnement Microsoft 365, votre organisation vous fournit OneDrive, votre stockage de fichiers dans le cloud. OneDrive est privé par défaut ; vous y organisez votre contenu et choisissez quels fichiers ou dossiers partager, et avec qui. D’autre part, SharePoint fournit un référentiel de fichiers dans le cloud qui est partagé avec d’autres personnes de votre organisation.  

## <a name="does--support-consumer-onedrive" />Est-ce que [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge OneDrive pour le grand public ?

Non. Cette intégration est exclusivement destinée à OneDrive Entreprise et ne prend en charge que votre compte professionnel. 

## <a name="are-all-onedrive-for-business-plans-supported" />Tous les abonnements OneDrive Entreprise sont-ils pris en charge ?

[!INCLUDE[prod_short](includes/prod_short.md)] ne prend pas en charge les plans autonomes pour OneDrive Entreprise. OneDrive doit être acheté dans le cadre d’un plan Microsoft 365 professionnel ou d’entreprise. Pour plus d’informations, consultez [Comparer les plans et les tarifs du stockage cloud OneDrive](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health" />Où puis-je voir l’intégrité des services OneDrive ?

Les administrateurs peuvent accéder au tableau de bord d’intégrité des services dans le cadre du centre d’administration Microsoft 365. Ce tableau de bord comprend la disponibilité des services OneDrive. Accédez à [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## <a name="is-onedrive-integration-available-to--on-premises" />Est-ce que l’intégration de OneDrive est disponible pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site ?

Oui, mais contrairement à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, elle nécessite une configuration supplémentaire. Pour plus d’informations, consultez [Configuration de Business Central sur site](admin-onedrive-integration-onpremises.md).  

## <a name="does--on-premises-connect-with-sharepoint-server" />Est-ce que [!INCLUDE[prod_short](includes/prod_short.md)] sur site se connecte avec SharePoint Server ?

Non Cette combinaison de déploiement n’est pas prise en charge, même si SharePoint Server a activé Mes sites.  

## <a name="does--online-connect-with-sharepoint-server" />Est-ce que [!INCLUDE[prod_short](includes/prod_short.md)] en ligne se connecte avec SharePoint Server ?

Non Cette combinaison de déploiement n’est pas prise en charge, même si SharePoint Server a activé Mes sites.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments" />Comment cela fonctionne-t-il dans une organisation avec plusieurs environnements ?

L’intégration suppose que les noms d’entreprise sont uniques dans tous les environnements [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque les noms d’entreprise sont uniques dans l’ensemble de l’organisation, l’ouverture d’un fichier dans OneDrive copie le fichier dans un dossier nommé d’après la société actuelle. Si les noms d’entreprise ne sont pas uniques dans tous les environnements, les fichiers pouvant provenir de noms d’entreprise identiques seront placés ensemble dans le même dossier.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files" />Nous avons changé le nom de notre société. Qu’advient-il de mes fichiers précédents ?

[!INCLUDE[prod_short](includes/prod_short.md)] ne migre pas automatiquement les fichiers que vous avez ouverts plus tôt dans OneDrive vers le nouveau dossier. Après avoir renommé votre entreprise, l’action Ouvrir dans OneDrive copiera les fichiers dans un dossier portant le nouveau nom de l’entreprise.   

## <a name="when-attaching-files-to--how-do-i-pick-a-file-from-onedrive" />Lorsque je joins des fichiers à [!INCLUDE[prod_short](includes/prod_short.md)], comment puis-je choisir un fichier à partir de OneDrive ?

[!INCLUDE[prod_short](includes/prod_short.md)] ne fournit pas de sélecteur de fichiers cloud. Vous devez télécharger le fichier de OneDrive sur votre appareil, puis le charger dans [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this" />Je veux ouvrir des fichiers dans SharePoint à la place. Comment puis-je faire cela ?

[!INCLUDE[prod_short](includes/prod_short.md)] ne fournit pas de fonctionnalités pour copier des fichiers vers SharePoint et les ouvrir à partir d’une bibliothèque SharePoint. Contactez votre partenaire Microsoft pour connaître vos options ou recherchez des applications dans AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive" />Comment désactiver l’intégration à OneDrive ?

Exécutez le guide de configuration assistée **Configuration de OneDrive** et désactivez les boutons à bascule **Utiliser les fonctionnalités de OneDrive pour l’application** et **Utiliser les fonctionnalités de OneDrive pour le système**. 

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint" />Dois-je utiliser la Page de configuration de la connexion SharePoint pour me connecter à SharePoint ?

Il s’agit d’une fonctionnalité héritée où tous les fichiers [!INCLUDE[prod_short](includes/prod_short.md)] de tous les utilisateurs sont envoyés à un seul dossier SharePoint. Nous vous recommandons de ne pas configurer le raccourci Documents partagés sur la page **Configuration de la connexion SharePoint** parce que cette page est [obsolète](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) et sera supprimée dans la deuxième vague de lancement 2023, version 23.0.  Nous vous recommandons d’utiliser plutôt la **Configuration de OneDrive**.  

## <a name="which-version-of--supports-onedrive" />Quelle version de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge OneDrive ?

L’intégration à OneDrive est devenue disponible dans la 2e vague de lancement 2021.  

## <a name="which-features-are-affected-by-onedrive-integration" /><a name="features"></a>Quelles fonctionnalités sont affectées par l’intégration de OneDrive ?

Dans le guide de configuration assistée **Configuration de OneDrive** pour configurer l’intégration de OneDrive, vous pouvez activer ou désactiver les fonctionnalités de gestion des fichiers Business Central dans OneDrive. Les fonctionnalités sont réparties entre deux options :

|Option|Désignation|
|------|----------|
|**Utiliser les fonctionnalités de OneDrive pour l’application**|Si vous activez cette option, les actions **Ouvrir dans OneDrive** et **Partager** sont rendues disponibles sur les fichiers dans Business Central, comme les fichiers joints aux documents ou dans la Boîte de réception état. Ces actions permettent aux utilisateurs de copier, d’ouvrir et de partager des fichiers dans OneDrive. Pour plus d’informations, consultez [Ouvrir et partager les fichiers Business Central dans OneDrive](across-share-onedrive.md).
|**Utiliser OneDrive pour les fonctionnalités du système**|L’activation de cette option active les fonctionnalités suivantes :<ul><li> Les fonctions **Ouvrir dans Excel** et **Modifier dans Excel** sur les pages de liste copient automatiquement le fichier Excel dans OneDrive, puis l’ouvrent dans Excel Online. Pour plus d’informations, voir [Affichage et édition dans Excel](across-work-with-excel.md).</li><li> L’envoi de tout rapport vers un fichier Excel ou Word copie automatiquement le fichier dans OneDrive, puis l’ouvrira dans Excel ou Word Online. Pour en savoir plus, consultez [Enregistrer un rapport dans un fichier](ui-work-report.md#saving-a-report-to-a-file).|

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive" />Microsoft continuera-t-il à améliorer l’intégration à OneDrive ?

Chez Microsoft, nous écoutons constamment les commentaires de notre communauté diverse d’utilisateurs et prenons les mesures nécessaires pour agir sur les principales propositions de la communauté. Pour en savoir plus sur les prochaines intégrations avec les applications Microsoft 365, consultez le [Programme de lancement de Dynamics 365](/dynamics365-release-plan/2021wave1).  

Si vous souhaitez participer à l’amélioration de l’intégration à OneDrive, ou avez une idée qui améliorerait le partage de fichiers et la collaboration dans [!INCLUDE[prod_short](includes/prod_short.md)], ajoutez une idée ou votez pour des idées existantes sur [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting" />Incident

Cette section fournit des informations sur la façon d’identifier et de résoudre les problèmes que vous pourriez rencontrer lors de l’utilisation de OneDrive avec [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="business-central-cant-find-my-onedrive" />Business Central ne trouve pas mon OneDrive

Lorsque ce message s’affiche, « Impossible de déterminer l’emplacement de votre OneDrive Entreprise ; contactez votre partenaire pour le configurer. », vérifiez si l’utilisateur a accédé à son OneDrive au moins une fois. Si ce n’est pas le cas, demandez à la personne d’aller sur portal.office.com/onedrive pour le configurer. Cela peut prendre un certain temps. Si le message s’affiche toujours après 24 heures, contactez l’assistance.  
 
### <a name="im-having-problems-sharing-from-outlook" />J’ai des problèmes de partage depuis Outlook

Consultez [Impossible de partager des fichiers OneDrive depuis Outlook.com](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) sur le support Microsoft.

### <a name="actions-open-in-onedrive-and-share-are-missing" />Les actions Ouvrir dans OneDrive et Partager sont absentes

Voici quelques éléments à vérifier :

- Vérifiez que les fonctionnalités de l’application pour OneDrive sont activées dans le guide de configuration assistée **Configuration de OneDrive**. Consultez [Configurer OneDrive à l’aide de la Configuration de OneDrive](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Vérifiez que Microsoft OneDrive est réglé sur **Accepté** sur la page **Statut des avis de confidentialité**. Consultez [Statut des avis de confidentialité](privacy-notices-status.md).

## <a name="see-also" />Voir aussi

[Intégration de Business Central et OneDrive](across-onedrive-overview.md)  
[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[Ouverture des fichiers Business Central dans OneDrive](across-share-onedrive.md)  
