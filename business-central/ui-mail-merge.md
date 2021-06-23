---
title: Utilisation de modèles Word pour les communications en masse | Microsoft Docs
description: Les modèles Word peuvent faciliter la création groupée de documents personnalisés pour des entités spécifiques.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110969"
---
# <a name="using-word-templates-for-bulk-communication"></a>Utilisation de modèles Word pour la communication en masse
Les modèles Microsoft Word peuvent faciliter la communication de masse avec des entités telles que les clients et les fournisseurs. Par exemple, vous pouvez créer des brochures pour alerter les clients sur une campagne de vente, des lettres pour informer les fournisseurs d'une nouvelle politique d'achat ou des invitations à attirer des contacts pour un événement à venir.

> [!NOTE]
> Vous pouvez utiliser les modèles Word uniquement sur les appareils avec Microsoft Word 2019 et sur lesquels le système d’exploitation Windows est installé.

Vous pouvez utiliser des entités dans [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données pour le modèle et ajouter des champs de fusion pour personnaliser les documents pour chaque entité. Les champs de fusion proviennent de l'entité dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document.

Sur la page **Modèles Word**, vous pouvez utiliser un guide de configuration assistée pour télécharger un fichier ZIP contenant un DataSource.txt et un fichier de modèle Word pour une entité. Après avoir configuré le modèle et ajouté des champs de fusion, vous utilisez le même guide pour charger le modèle. Vous ne pouvez utiliser que le modèle Word et les fichiers de source de données que vous téléchargez à partir de [!INCLUDE[prod_short](includes/prod_short.md)] et vous devez stocker les fichiers au même emplacement.

> [!NOTE]
> Lorsque vous choisissez une entité pour laquelle créer un modèle, la liste affiche toutes les entités dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cependant, vous ne pouvez pas créer de modèles pour toutes les entités. Si le nom d'une entité contient des caractères spéciaux, tels que **/**, **.**, **_**, ou **-**, vous ne pouvez pas créer de modèle pour celui-ci. Le nom de l'entité est indiqué dans la colonne **Légende de l'objet**.

Lorsque vous configurez le modèle dans Word, sur l'onglet **Publipostage** vous pouvez ajouter des champs de fusion en choisissant **Insérer un champ de fusion**.

> [!NOTE]
> Vous ne pouvez pas utiliser de champs de fusion si le nom du champ contient 40 caractères ou plus. Par exemple, vous ne pouvez pas utiliser le champ Company__Information_Customs_Permit_Date car il comporte 40 caractères. 

Lorsque votre modèle Word est prêt, sur la page **Modèles Word** vous pouvez choisir **Appliquer** pour générer les documents. Vous pouvez créer un document contenant des sections pour chaque entité ou fractionner l'opération pour créer un document pour chaque entité.

## <a name="to-create-a-word-template"></a>Pour créer un modèle Word
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modèles Word**, puis choisissez le lien associé.
2. Suivez les étapes du guide de configuration assistée. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Voir aussi
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
