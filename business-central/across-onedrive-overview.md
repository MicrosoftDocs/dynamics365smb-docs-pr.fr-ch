---
title: Intégration de Business Central et OneDrive Entreprise
description: Vous pouvez utiliser OneDrive Entreprise pour stocker, gérer et partager des fichiers, tels que des rapports ou des pièces jointes.
author: brentholtorf
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 522bf01d08e77e52b4fbcf32f2652c53208cf8ec
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381844"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Intégration de Business Central et OneDrive Entreprise
OneDrive Entreprise est un service de stockage cloud inclus dans Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] facilite le stockage, la gestion et le partage de fichiers avec d’autres personnes via OneDrive. Lorsqu’un fichier est dans votre OneDrive, vous pouvez profiter des riches expériences collaboratives des versions en ligne des produits Microsoft, telles que Word, Excel et PowerPoint. Par exemple, vous pouvez partager un document Word, puis vous et vos collègues pouvez le modifier ensemble en temps réel. OneDrive vous permet également d’ouvrir d’autres types de fichiers, tels que des fichiers PDF. 

## <a name="getting-started"></a>Mise en route
Nous avons créé un lien entre [!INCLUDE[prod_short](includes/prod_short.md)] en ligne et OneDrive pour faciliter votre démarrage. La seule exigence est que les utilisateurs aient ouvert OneDrive au moins une fois. 

Sur la plupart des pages où les fichiers sont disponibles, comme la Boîte de réception état ou les fichiers joints à des enregistrements, vous trouverez une action **Ouvrir dans OneDrive**.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="L’action Ouvrir dans OneDrive":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Partager des pièces jointes dans OneDrive":::

Lorsque vous utilisez l’action **Ouvrir dans OneDrive** pour la première fois, [!INCLUDE[prod_short](includes/prod_short.md)] fait ce qui suit dans votre OneDrive :

1. Crée un dossier nommé [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. Dans le dossier [!INCLUDE[prod_short](includes/prod_short.md)], il crée un autre dossier portant le même nom que la société dans laquelle vous travaillez. Si vous travaillez dans plusieurs sociétés, il créera un dossier pour la société dans laquelle vous travaillez lorsque vous utilisez l’action **Ouvrir dans OneDrive**. 
3. Place une copie du fichier que vous avez sélectionné dans le dossier, puis ouvre le fichier. La prochaine fois que vous utiliserez l’action, elle ne fera que copier et ouvrir le fichier. 

Le dossier et son contenu sont privés jusqu’à ce que vous décidiez de les partager avec d’autres. Par exemple, vous pouvez décider de partager du contenu avec un ou plusieurs de vos collègues, voire avec des personnes extérieures à votre organisation. Pour plus d’informations, consultez [Partager des fichiers et des dossiers OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Vous pouvez également connecter votre [!INCLUDE[prod_short](includes/prod_short.md)] sur site avec OneDrive. Cependant, il y a quelques choses à faire pour que cela fonctionne. Pour plus d’informations, voir [Configuration de Business Central sur site](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Voir aussi
[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[Ouverture des fichiers Business Central dans OneDrive](across-share-onedrive.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)