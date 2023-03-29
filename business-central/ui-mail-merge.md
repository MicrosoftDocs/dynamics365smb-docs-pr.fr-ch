---
title: Utilisation de modèles Word pour les communications en masse | Microsoft Docs
description: Les modèles Word peuvent faciliter la création groupée de documents personnalisés pour des entités spécifiques.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'document, mail, merge, Word, template, email'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Utiliser des modèles Word pour la communication en masse
Les modèles Microsoft Word peuvent faciliter la communication de masse par documents papier ou e-mails avec des entités telles que les contacts, les clients et les fournisseurs. Par exemple, vous pouvez créer des brochures pour alerter les clients sur une campagne de vente, des lettres pour informer les fournisseurs d’une nouvelle politique d’achat ou des invitations à attirer des contacts pour un événement à venir.

> [!NOTE]
> Vous pouvez utiliser les modèles Word uniquement sur les appareils avec Microsoft Word 2019 et sur lesquels le système d’exploitation Windows est installé.

Vous pouvez utiliser des entités dans [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données pour le modèle et ajouter des champs de fusion pour personnaliser les documents pour chaque entité. Les champs de fusion proviennent de l’entité dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document.

Sur la page **Modèles Word**, lorsque vous créez un nouveau modèle, vous pouvez utiliser un guide de configuration assistée pour télécharger un fichier ZIP contenant un fichier DataSource.txt et un fichier de modèle Word pour l’entité. Le fichier de source de données fournit les champs que vous pouvez utiliser dans le modèle. Ne modifiez pas le fichier de source de données. Vous ne pouvez utiliser que le modèle Word et les fichiers de source de données que vous téléchargez à partir de [!INCLUDE[prod_short](includes/prod_short.md)] et vous devez stocker les fichiers au même emplacement.

Après avoir configuré le modèle et ajouté des champs de fusion, vous utilisez le même guide pour charger le modèle.

## Configuration du modèle dans Word
Lorsque vous configurez un modèle dans Word, sur l’onglet **Publipostage** vous pouvez ajouter des champs de fusion en choisissant **Insérer un champ de fusion**. Les champs de fusion disponibles proviennent du fichier de source de données que vous avez téléchargé pour l’entité. Ils tiennent lieu d’espaces réservés qui indiquent à Word où dans le document placer les informations sur l’entité. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Ajout de champs de fusion dans Microsoft Word":::

## Ajout d’entités associées
En plus d’ajouter des données pour l’entité source, c’est-à-dire l’entité pour laquelle vous créez le modèle, vous pouvez également fusionner les données des entités qui lui sont associées. Par exemple, si la source est l’entité Client, vous pouvez également fusionner les données des champs de l’entité Client/Acheteur car les deux entités ont un champ en commun.

Les entités associées partagent un champ, qui est souvent un identifiant tel qu’un nom, un code ou un ID, avec l’entité source. Lorsque vous configurez un modèle, il existe des options simples et avancées pour choisir les entités associées :

* Simple : ajoutez des relations connues rendues disponibles par défaut par [!INCLUDE[prod_short](includes/prod_short.md)].
* Avancé : ajoutez des relations non standard, telles que celles qui ont été ajoutées par des extensions ou des personnalisations. Cela nécessite que vous connaissiez les champs que les entités partagent.

Lorsque vous ajoutez une entité associée, vous devez spécifier un préfixe pour le nom du champ. Lorsque vous ajoutez des champs au modèle, le préfixe peut faciliter la distinction entre les champs de l’entité source et les champs des entités associées.

## Pour créer un modèle Word dans Business Central
1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles Word**, puis choisissez le lien associé.
2. Choisissez **Nouveau**, puis **Créer un modèle**, puis suivez les étapes du guide de configuration assistée. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Vous pouvez également créer un modèle directement depuis la page d’une entité en choisissant l’action **Appliquer le modèle Word** pour ouvrir le guide de configuration assistée, puis **Nouveau modèle**. Lorsque vous faites cela, la source de données est choisie pour vous en fonction du type d’entité.

## Application d’un modèle
Lorsque votre modèle Word est prêt, sur la page **Modèles Word** vous pouvez choisir **Appliquer** pour générer les documents. Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document. Vous pouvez créer un document contenant des sections pour chaque entité ou sélectionner **Fractionner** pour créer un document pour chaque entité.

Vous pouvez appliquer des modèles à une ou plusieurs entités du même type, comme un contact, directement dans le contexte de cette page ou à partir de la page Modèles Word pour appliquer le modèle à toutes les entités de ce type.

## Utiliser des modèles Word avec la messagerie
Vous pouvez utiliser des modèles Word pour ajouter du contenu aux messages électroniques. Lorsque vous rédigez un e-mail, vous pouvez choisir l’action **Utiliser un modèle Word** pour appliquer le contenu d’un modèle au message. Cela nécessite que vous ayez créé un ou plusieurs modèles pour l’entité. Vous pouvez utiliser un modèle à la fois et lorsque vous passez d’un modèle à l’autre, le message change pour refléter le contenu du modèle choisi.

De plus, vous pouvez utiliser l’action **Ajouter un fichier à partir d’un modèle Word** pour joindre le contenu du modèle à l’e-mail sous forme de fichier. Le fichier utilisera le format que vous avez spécifié pour la sortie du modèle.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Options d’utilisation du contenu d’un modèle Word dans un e-mail":::

## Voir aussi
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
