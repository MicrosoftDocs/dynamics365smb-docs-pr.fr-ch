---
title: Ouverture des fichiers Business Central dans OneDrive
description: Découvrez comment partager des données Business Central via OneDrive Entreprise.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Ouverture et partage de fichiers Business Central dans Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] facilite le stockage, la gestion et le partage de fichiers avec d’autres personnes via Microsoft OneDrive Entreprise. Sur la plupart des pages où des fichiers sont disponibles, comme la Boîte de réception état, ou lorsque des fichiers sont joints à des enregistrements, vous trouverez des actions **Ouvrir dans OneDrive** et **Partager**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les rapports":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Actions Ouvrir dans OneDrive et Partager pour les documents joints":::


## <a name="open-in-onedrive"></a>Ouvrir dans OneDrive

L’action **Ouvrir dans OneDrive** copie le fichier dans votre OneDrive, puis ouvre le fichier dans une application telle que Microsoft Excel Online, Microsoft Word Online ou Microsoft PowerPoint Online. 

<!--## Working with different types of files-->

Lorsque vous choisissez **Ouvrir dans OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifie les fichiers Excel, Word et PowerPoint et les ouvre dans leurs applications en ligne, c’est-à-dire Excel Online, Word Online et PowerPoint Online. 

En utilisant les versions en ligne de ces applications, vous pouvez annoter, modifier et collaborer avec d’autres sans quitter le navigateur.

Pour les autres types de fichiers courants, tels que les fichiers PDF, les fichiers texte et les images, OneDrive fournit des visionneuses de fichiers qui offrent des fonctionnalités d’impression, de partage, etc. Si un fichier ne peut pas être affiché dans OneDrive, vous serez peut-être invité à le télécharger.

## <a name="share"></a>Partager

L’action **Partager** copie le fichier sur votre OneDrive et vous permet de voir avec qui vous l’avez déjà partagé, ainsi que de le partager avec d’autres personnes. Lorsque vous sélectionnez l’action **Partager**, la page suivante s’ouvre.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Partager un fichier dans OneDrive":::

Si vous êtes familiarisé avec OneDrive, vous reconnaîtrez peut-être la page illustrée ci-dessus. Deux options s’offrent à vous pour partager le fichier : **Envoyer le lien** et **Copier le lien**.

- **Envoyer le lien** vous permet de partager les fichiers avec des personnes spécifiques. Les personnes avec qui vous partagez le fichier recevront un e-mail avec un lien vers le fichier. Le fichier apparaîtra également dans la section **Partagé** de leur OneDrive. Commencez par saisir les adresses e-mail ou les noms des contacts dans le champ **Nom, groupe ou e-mail**. Incluez un message sous le champ **Nom, groupe ou adresse e-mail**, si vous le souhaitez.

  > [!TIP]
  > Si vous voulez composer votre message dans Outlook, sélectionnez le bouton **Outlook**. Le lien sera inséré dans un brouillon d’e-mail et toutes les personnes avec lesquelles vous avez indiqué le partage seront dans la liste **À**. Avec cette option, vous pouvez créer des e-mails en utilisant toutes les fonctionnalités d’Outlook, y compris la mise en forme du texte, l’ajout d’autres pièces jointes, l’insertion d’images ou de tableaux et l’ajout de destinataires CC ou BCC.

- **Copier le lien** copie un lien vers le fichier que vous pouvez utiliser pour partager le fichier via des applications telles que Facebook, Twitter ou une messagerie. 

Avant d’envoyer ou de copier un lien de fichier, définissez le niveau d’autorisation que vous souhaitez attribuer aux personnes. Vous pouvez voir le paramètre actuel sous **Envoyer le lien** ou **Copier le lien**. Dans la plupart des cas, ce sera **Toute personne disposant du lien peut modifier**, selon les paramètres définis par votre administrateur. Pour modifier les autorisations, sélectionnez le lien et apportez des modifications sur la page **Paramètres du lien**.

La fonctionnalité de partage dans Business Central est basée sur OneDrive. Découvrez plus d’informations sur le partage et les autorisations de OneDrive dans la section [Partager des fichiers et des dossiers OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> L’action **Partager** n’est pas disponible dans l’application Business Central pour les appareils mobiles.

## <a name="first-time-sign-in-from-business-central"></a>Première connexion à partir de Business Central

Lorsque vous utilisez l’action **Ouvrir dans OneDrive** ou **Partager** pour la première fois, [!INCLUDE[prod_short](includes/prod_short.md)] effectue les actions suivantes :

1. Ouvre la page **Consulter les conditions générales**. Lisez la page et, si vous êtes d’accord avec les conditions générales, sélectionnez **Accepter** pour continuer.
2. Crée un dossier nommé [!INCLUDE[prod_short](includes/prod_short.md)] dans OneDrive. 
3. Dans le dossier [!INCLUDE[prod_short](includes/prod_short.md)], il crée un dossier portant le même nom que la société dans laquelle vous travaillez. Si vous travaillez dans plusieurs sociétés, [!INCLUDE[prod_short](includes/prod_short.md)] crée un dossier pour chaque société où vous travaillez quand vous utilisez l’action **Ouvrir dans OneDrive** ou **Partager**. 
4. Place une copie du fichier que vous avez sélectionné dans le dossier au nom de la société, puis ouvre le fichier. 

La prochaine fois que vous utiliserez l’action **Ouvrir dans OneDrive** ou **Partager**, [!INCLUDE[prod_short](includes/prod_short.md)] ne fera que copier et ouvrir le fichier. 

## <a name="managing-multiple-copies-of-a-file"></a>Gestion de plusieurs copies d’un fichier

Lorsque vous choisissez **Ouvrir dans OneDrive** ou **Partager**, le fichier est copié depuis [!INCLUDE[prod_short](includes/prod_short.md)] dans votre dossier dans OneDrive. Si vous modifiez le fichier dans OneDrive, ce fichier sera différent du fichier [!INCLUDE[prod_short](includes/prod_short.md)]. Pour mettre à jour [!INCLUDE[prod_short](includes/prod_short.md)] avec la dernière version du fichier, supprimez le fichier existant de [!INCLUDE[prod_short](includes/prod_short.md)], puis chargez la dernière copie.

Si un fichier portant le même nom existe déjà dans OneDrive, vous aurez les choix suivants :

- **Utiliser existant**

  Cette option ouvre ou partage le fichier qui est déjà stocké dans OneDrive, au lieu de copier le fichier depuis Business Central.
  
- **Remplacer**
  
  Cette option remplace le fichier existant dans OneDrive par le fichier que vous avez sélectionné dans Business Central. Le fichier d’origine n’est pas perdu&mdash;vous pouvez le voir et le restaurer en utilisant l’historique des versions dans OneDrive. Pour plus d’informations, consultez [Restaurer une version précédente d’un fichier stocké dans OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive-159cad6d-d76e-4981-88ef-de6e96c93893).

- **Conserver les deux**

  Cette option conserve le fichier existant tel quel et enregistre le fichier que vous avez sélectionné dans Business Central sous un nom différent. Le nouveau nom est similaire au nom existant, à l’exception d’un numéro de suffixe tel que « Articles (2).xlsx ».

## <a name="about-your-business-central-folder-on-onedrive"></a>À propos de votre dossier Business Central sur OneDrive

Le dossier et son contenu sont privés jusqu’à ce que vous décidiez de les partager avec d’autres. Ainsi, vous pouvez décider de partager du contenu avec un ou plusieurs de vos collègues, voire avec des personnes extérieures à votre organisation. 

Vous pouvez accéder à votre OneDrive depuis la page **Mes paramètres** en choisissant le lien dans le champ **Stockage cloud**. Pour plus d’informations, consultez [Partager des fichiers et dossiers OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Le champ Stockage cloud dans Mes paramètres":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Voir aussi

[Intégration de Business Central et OneDrive](across-onedrive-overview.md)  
[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)
