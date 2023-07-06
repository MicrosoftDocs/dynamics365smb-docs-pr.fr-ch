---
title: Intégration de Business Central et OneDrive Entreprise
description: 'Vous pouvez utiliser OneDrive Entreprise pour stocker, gérer et partager des fichiers, tels que des rapports ou des pièces jointes. Cela fonctionne aussi si vous tapez One Drive.'
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
---

# <a name="business-central-and-onedrive-for-business-integration"></a><a name="business-central-and-onedrive-for-business-integration"></a><a name="business-central-and-onedrive-for-business-integration"></a>Intégration de Business Central et OneDrive Entreprise

OneDrive Entreprise est un service de stockage cloud inclus dans Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] facilite le stockage, la gestion et le partage de fichiers avec d’autres personnes via OneDrive. Lorsqu’un fichier est dans votre OneDrive, vous pouvez profiter des riches expériences collaboratives des versions en ligne des produits Microsoft, telles que Word, Excel et PowerPoint. Par exemple, vous pouvez partager un document Word, puis vous et vos collègues pouvez le modifier ensemble en temps réel. OneDrive vous permet également d’ouvrir d’autres types de fichiers, tels que des fichiers PDF. 

## <a name="get-started-with-onedrive-features"></a><a name="get-started-with-onedrive-features"></a><a name="get-started-with-onedrive-features"></a>Prise en main des fonctionnalités de OneDrive

Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] Online, nous avons déjà créé le lien entre [!INCLUDE[prod_short](includes/prod_short.md)] Online et OneDrive pour faciliter votre démarrage. La seule exigence est que les utilisateurs aient ouvert OneDrive au moins une fois. Avec [!INCLUDE[prod_short](includes/prod_short.md)] sur site, un administrateur doit configurer la connexion avant que vous ne puissiez commencer. Pour plus d’informations, consultez [Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### <a name="open-and-share-in-onedrive"></a><a name="open-and-share-in-onedrive"></a><a name="open-and-share-in-onedrive"></a>Ouvrir et partager dans OneDrive

Sur la plupart des pages où les fichiers sont disponibles, comme la Boîte de réception état ou les fichiers joints à des enregistrements, vous trouverez des actions **Ouvrir dans OneDrive** et **Partager**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les rapports":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les documents joints":::

|Sélectionnez...|Pour...|Voir plus d’informations...|
|---------|-----|----------------|
|Ouvrir dans OneDrive|Copiez le fichier dans un dossier Business Central de votre OneDrive et ouvrez le fichier.|[Ouvrir dans OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Part|Copiez le fichier sur votre OneDrive et partagez-le avec d’autres personnes.|[Partager dans OneDrive](across-share-onedrive.md#share) |

### <a name="save-excel-workbooks-and-report-files-in-onedrive"></a><a name="save-excel-workbooks-and-report-files-in-onedrive"></a><a name="save-excel-workbooks-and-report-files-in-onedrive"></a>Enregistrer des classeurs Excel et des fichiers d’état dansOneDrive

Avec la configuration de l’intégration OneDrive, quelques autres fonctionnalités familières utiliseront automatiquement OneDrive pour enregistrer les fichiers au lieu de les enregistrer sur votre appareil :

- Les fonctions **Ouvrir dans Excel** et **Modifier dans Excel** sur les pages de liste copient automatiquement le fichier Excel dans OneDrive, puis l’ouvrent dans Excel Online. Pour plus d’informations, voir [Affichage et édition dans Excel](across-work-with-excel.md).
- L’envoi de tout rapport vers un fichier Excel ou Word copie automatiquement le fichier dans OneDrive, puis l’ouvrira dans Excel ou Word Online. Pour en savoir plus, consultez [Enregistrer un rapport dans un fichier](ui-work-report.md#saving-a-report-to-a-file).

Ces fonctionnalités ne sont pas activées par défaut. Mais en tant qu’administrateur, vous pouvez facilement les activer en utilisant le guide de configuration assistée **Configuration de OneDrive**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Vous pouvez également connecter votre [!INCLUDE[prod_short](includes/prod_short.md)] sur site avec OneDrive. Cependant, il y a quelques choses à faire pour que cela fonctionne. Pour plus d’informations, consultez [Configuration de Business Central sur site](admin-onedrive-integration-onpremises.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[Ouverture des fichiers Business Central dans OneDrive](across-share-onedrive.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)  
