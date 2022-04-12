---
title: Ouverture des fichiers Business Central dans OneDrive
description: Découvrez comment partager des données Business Central via OneDrive Entreprise.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516436"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Ouverture et partage de fichiers Business Central dans OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] facilite le stockage, la gestion et le partage de fichiers avec d’autres personnes via OneDrive Entreprise. Sur la plupart des pages où les fichiers sont disponibles, comme la Boîte de réception état ou les fichiers joints à des enregistrements, vous trouverez une action **Ouvrir dans OneDrive** et **Partager**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les rapports":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les documents joints":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Ouvrir dans OneDrive

L’action **Ouvrir dans OneDrive** copie le fichier sur votre OneDrive et ouvre le fichier dans son application en ligne, comme Excel Online, Word Online et PowerPoint Online. 

<!--## Working with Different Types of Files-->

Lorsque vous choisissez **Ouvrir dans OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifie les fichiers Excel, Word et PowerPoint et les ouvre dans leurs applications en ligne, c’est-à-dire Excel Online, Word Online et PowerPoint Online. Vous pouvez annoter, modifier et collaborer avec d’autres sans quitter le navigateur.

Pour les autres types de fichiers courants, tels que les fichiers PDF, les fichiers texte et les images, OneDrive fournit des visionneuses de fichiers qui offrent des fonctionnalités d’impression, de partage, etc. Si un fichier ne peut pas être affiché dans OneDrive, vous serez peut-être invité à le télécharger.

## <a name="share"></a>Part

L’action **Partager** copie le fichier sur votre OneDrive et vous permet de le partager avec d’autres personnes et de voir les personnes avec qui vous avez déjà partagé le fichier. Lorsque vous sélectionnez l’action **Partager**, la page suivante s’ouvre.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Partager un fichier dans OneDrive":::

Si vous êtes familiarisé avec OneDrive, vous reconnaîtrez peut-être la page. Deux options s’offrent à vous pour partager le fichier : **Envoyer le lien** et **Copier le lien**.

- **Envoyer le lien** vous permet de partager les fichiers avec des personnes spécifiques. Les personnes avec qui vous partagez le fichier recevront un e-mail avec un lien vers le fichier. Le fichier apparaîtra également dans la section **Partagé** de leur OneDrive. Commencez par saisir les adresses e-mail ou les noms des contacts dans le champ **Nom, groupe ou e-mail**.

- **Copier le lien** copie un lien vers le fichier sur votre OneDrive afin que vous puissiez utiliser le lien dans d’autres endroits comme Facebook, Twitter ou les e-mails. 

Avant d’envoyer ou de copier le lien, définissez l’autorisation que vous souhaitez attribuer aux personnes pour le fichier. Vous pouvez voir le paramètre actuel sous **Envoyer le lien** et **Copier le lien**. Dans la plupart des cas, ce sera **Toute personne disposant du lien peut modifier pour ouvrir le lien**, selon les paramètres définis par votre administrateur. Pour modifier les autorisations, sélectionnez le lien et apportez des modifications sur la page **Paramètres du lien**.

La fonctionnalité de partage dans Business Central est basée sur OneDrive. Pour en savoir plus sur le partage et les autorisations, voir [Partager des fichiers et des dossiers OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> L’action **Partager** n’est pas disponible dans l’application Business Central pour les appareils mobiles.

## <a name="first-time-sign-in-from-business-central"></a>Première connexion à partir de Business Central

Lorsque vous utilisez l’action **Ouvrir dans OneDrive** ou **Partager** pour la première fois, [!INCLUDE[prod_short](includes/prod_short.md)] effectue les actions suivantes :

1. Ouvre la page **Consulter les conditions générales**. Lisez la page et, si vous êtes d’accord avec les conditions générales, sélectionnez **Accepter** pour continuer.
2. Ouvre la page **Choisir un compte**. Sélectionnez votre compte ou **utilisez un autre compte** si vous ne voyez pas le vôtre, puis saisissez le nom d’utilisateur et le mot de passe lorsque vous y êtes invité.
3. Crée un dossier nommé [!INCLUDE[prod_short](includes/prod_short.md)] dans OneDrive. 
4. Dans le dossier [!INCLUDE[prod_short](includes/prod_short.md)], il crée un autre dossier portant le même nom que la société dans laquelle vous travaillez. Si vous travaillez dans plusieurs sociétés, un dossier est créé pour la société dans laquelle vous travaillez lorsque vous utilisez les actions **Ouvrir dans OneDrive** et **Partager**. 
5. Place une copie du fichier que vous avez sélectionné dans le dossier, puis ouvre le fichier. La prochaine fois que vous utiliserez l’action, elle ne fera que copier et ouvrir le fichier. 

## <a name="managing-multiple-copies-of-a-file"></a>Gestion de plusieurs copies d’un fichier

Lorsque vous choisissez **Ouvrir dans OneDrive** ou **Partager**, le fichier est copié depuis [!INCLUDE[prod_short](includes/prod_short.md)] dans votre dossier dans OneDrive. Si vous modifiez le fichier dans OneDrive, les copies du fichier seront différentes. Mettre à jour [!INCLUDE[prod_short](includes/prod_short.md)] avec le dernier fichier, supprimez le fichier existant de [!INCLUDE[prod_short](includes/prod_short.md)] puis téléchargez la dernière copie.

De plus, lorsqu’un fichier portant le même nom existe déjà dans OneDrive, [!INCLUDE[prod_short](includes/prod_short.md)] offrira le choix de remplacer le fichier ou de conserver les deux fichiers. Si vous choisissez de conserver les deux fichiers, le nouveau fichier est copié dans OneDrive et un nom de fichier avec un numéro de suffixe, par exemple « Articles (2).xlsx », lui est attribué. Le fichier d’origine n’est pas modifié. 

Si vous choisissez de remplacer le fichier, le nouveau fichier est ajouté à l’historique des versions de ce fichier. Le fichier d’origine n’est pas perdu et vous pouvez afficher ou restaurer les versions précédentes du fichier. 

## <a name="about-your-business-central-folder-on-onedrive"></a>À propos de votre dossier Business Central sur OneDrive

Le dossier et son contenu sont privés jusqu’à ce que vous décidiez de les partager avec d’autres. Par exemple, vous pouvez décider de partager du contenu avec un ou plusieurs de vos collègues, voire avec des personnes extérieures à votre organisation. Vous pouvez accéder à votre OneDrive depuis la page **Mes paramètres** en choisissant le lien dans le champ **Stockage cloud**. Pour plus d’informations, consultez [Partager des fichiers et des dossiers OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Le champ Stockage cloud dans Mes paramètres":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Voir aussi
[Intégration de Business Central et OneDrive](across-onedrive-overview.md)  
[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)