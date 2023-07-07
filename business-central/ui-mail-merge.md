---
title: Utilisation de modèles Word pour les communications en masse
description: Les modèles Word peuvent faciliter la création groupée de documents personnalisés pour des entités spécifiques.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication"></a>Utiliser des modèles Word pour la communication en masse

Les modèles Microsoft Word peuvent faciliter la communication de masse par documents papier ou e-mails avec des entités telles que les contacts, les clients et les fournisseurs. Par exemple, vous pouvez créer :

* Des brochures pour avertir les clients d’une campagne de vente ;
* Des lettres pour informer les fournisseurs d’une nouvelle politique d’achat ;
* Des invitations pour attirer des contacts à un événement à venir

> [!NOTE]
> Lorsque vous configurez les modèles Word, vous devez utiliser un appareil avec Microsoft Word 2019 ou version ultérieure et sur lesquels le système d’exploitation Windows est installé.

## <a name="set-up-the-source-of-data"></a>Configurer la source de données

Utilisez des entités dans [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données pour le modèle et ajouter des champs de fusion pour personnaliser les documents pour chaque entité. Les champs de fusion proviennent de l’entité dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document.

Sur la page **Modèles Word** , lorsque vous créez un modèle, un guide de configuration assistée vous aide à travers les étapes suivantes :

1. Choisissez une ou plusieurs entités à utiliser comme source des données. Par exemple, si vous souhaitez créer une brochure pour une campagne de vente, vous choisirez probablement l’entité Client comme source.
2. Choisissez d’autres entités comme sources de données supplémentaires. En savoir plus sur [Ajouter des écritures liées ou non à l’entité source](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Téléchargez un modèle vierge. Vous pouvez configurer le modèle dans Word immédiatement, ou vous pouvez télécharger le modèle vierge et terminer le guide. Lorsque votre modèle est prêt, utilisez l’action **Télécharger** sur la page **Modèles Word** pour remplacer le modèle vierge par votre modèle fini. En savoir plus dans [Configurer le modèle dans Word](#set-up-the-template-in-word).
4. Téléchargez le modèle que vous avez préparé.
5. Entrez un code et un nom qui identifient le modèle.

Lorsque vous téléchargez un modèle, vous obtenez un fichier .zip qui comprend deux fichiers.

|Fichier  |Description  |
|---------|---------|
|DataSource.xlsx     | Le fichier de source de données fournit les champs que vous pouvez utiliser dans le modèle. Ne modifiez pas le fichier de source de données. Vous ne pouvez utiliser que le modèle Word et les fichiers de source de données que vous téléchargez et vous devez stocker les fichiers au même emplacement.     |
|Modèle Word     | Un fichier .docx à utiliser comme modèle.        |

Pour en savoir plus sur la configuration d’un modèle dans Word, accédez à [Configurer le modèle dans Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Ajouter des écritures liées ou non à l’entité source

Vous pouvez également fusionner les données d’autres entités. Pour ajouter d’autres entités en tant que sources de données, utilisez l’une des actions suivantes sur la page **Modèles Word** ou lorsque vous utilisez le guide de configuration assistée :

|Action  |Description  |
|---------|---------|
|**Ajouter une entité associée**  | Utilisez les données des entités qui sont liées à l’entité source. Par exemple, pour l’entité Client, vous pouvez également fusionner les données de l’entité Contact. Les entités sont liées lorsqu’un champ d’une entité fait référence à une autre. Un champ sur l’entité Client fait référence à un champ sur l’entité Contact, ils sont donc liés. Le champ partagé est souvent un identifiant tel qu’un nom, un code ou un ID.        |
|**Ajouter une entité non associée**| Utilisez les données des entités qui ne sont pas liées à l’entité source. Par exemple, vous créez un modèle pour l’entité Client. Vous pouvez ajouter l’entité Informations sur la société afin de pouvoir inclure vos coordonnées. Un avantage clé est que si vous modifiez vos informations de contact, elles sont automatiquement mises à jour dans votre modèle. Après avoir ajouté une entité non liée, vous pouvez ajouter des entités qui lui sont liées.         |

Pour les écritures non liées, vous choisissez un enregistrement spécifique. Puisque vous ne pouvez ajouter une entité qu’une seule fois, pour utiliser un enregistrement différent, vous devez supprimer l’entité et l’ajouter à nouveau avec le nouvel enregistrement.

Vous pouvez créer une hiérarchie d’entités, à la fois liées et non liées. La relation est représentée sous forme d’arborescence. Le champ **Relation d’entité** affiche également des informations sur la relation. Pour les entités non liées, le champ affiche l’enregistrement qui crée la relation.

Lorsque vous ajoutez des entités, utilisez le champ **Préfixe du champ** pour spécifier un préfixe pour les noms de champ. Ultérieurement, lorsque vous ajoutez des champs au modèle, le préfixe peut faciliter la distinction entre les champs de l’entité source et les champs des entités associées.

### <a name="select-the-fields-to-include"></a>Sélectionner les champs à inclure

Pour chaque entité, vous pouvez spécifier les champs que vous souhaitez rendre disponibles pour le modèle. Choisissez le nombre dans la colonne  **Nombre de champs sélectionnés** pour accéder à une liste des champs disponibles. Sur la page **Sélection des champs**, utilisez la case à cocher **Inclure** pour spécifier les champs. Pour certaines entités, les champs que les entreprises utilisent généralement sont inclus par défaut. Vous pouvez modifier la liste, par exemple, pour supprimer les champs par défaut. Vos modifications s’appliquent uniquement au modèle sur lequel vous travaillez.

> [!NOTE]
> Le nombre total de champs que vous pouvez ajouter à partir de toutes les entités est de 250.

> [!NOTE]
> Vous ou votre partenaire Microsoft pouvez ajouter des champs personnalisés aux entités. Lorsque vous le faites, nous préfixons le nom des champs avec **CALC** et leur donnons le type de champ **Calculé**. Le type de champ est appelé calculé pour indiquer que le champ peut afficher différents types de valeurs, tels que du texte, des nombres, des dates, etc.

## <a name="to-create-a-word-template-in-business-central"></a>Pour créer un modèle Word dans Business Central

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles Word**, puis choisissez le lien associé.
2. Choisissez **Nouveau**, puis **Créer un modèle**, puis suivez les étapes du guide de configuration assistée. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Vous pouvez également créer un modèle directement depuis la page d’une entité en choisissant l’action **Appliquer le modèle Word** pour ouvrir le guide de configuration assistée, puis **Nouveau modèle**. Lorsque vous faites cela, la source de données est choisie pour vous en fonction du type d’entité.

## <a name="set-up-the-template-in-word"></a>Configurer le modèle dans Word

Lorsque vous configurez un modèle dans Word, sur l’onglet **Publipostage** vous pouvez ajouter des champs de fusion en choisissant **Insérer un champ de fusion**. Les champs de fusion disponibles proviennent du fichier de source de données que vous avez téléchargé pour l’entité. Ils tiennent lieu d’espaces réservés qui indiquent à Word où dans le document placer les informations sur l’entité.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Ajout de champs de fusion dans Microsoft Word":::

## <a name="apply-a-template"></a>Appliquer un modèle

Lorsque votre modèle Word est prêt, sur la page **Modèles Word** vous pouvez choisir **Appliquer** pour générer les documents. Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document. Vous pouvez créer un document contenant des sections pour chaque entité ou sélectionner **Fractionner** pour créer un document pour chaque entité.

Vous pouvez utiliser l’action **Appliquer des modèles Word** pour appliquer les modèles à une ou plusieurs entités du même type, comme un client, directement dans le contexte de cette page pour l’entité. Par exemple, les pages **Client** ou **Fournisseur**.

## <a name="use-word-templates-with-email"></a>Utiliser des modèles Word avec la messagerie

Vous pouvez utiliser des modèles Word pour ajouter du contenu aux messages électroniques. Lorsque vous rédigez un e-mail, vous pouvez choisir l’action **Utiliser un modèle Word** pour appliquer le contenu d’un modèle au message. Vous devez avoir créé des modèles pour l’entité. Vous pouvez utiliser un modèle à la fois et lorsque vous passez d’un modèle à l’autre, le message change pour refléter le contenu du modèle choisi.

De plus, vous pouvez utiliser l’action **Ajouter un fichier à partir d’un modèle Word** pour joindre le contenu du modèle à l’e-mail sous forme de fichier. Le fichier utilisera le format que vous avez spécifié pour la sortie du modèle.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Options d’utilisation du contenu d’un modèle Word dans un e-mail":::

## <a name="edit-a-word-template"></a>Modifier un modèle Word

Vous pouvez apporter les modifications suivantes à vos modèles Word :

* Pour modifier le corps du texte ou les champs de fusion inclus dans le modèle, utilisez l’action **Télécharger**, apportez vos modifications, puis utilisez l’action **Télécharger**
* Pour modifier les sources de données, utilisez l’action **Modifier les entités associées**
* Pour remplacer le modèle Word par un nouveau modèle, utilisez l’action **Télécharger**
* Supprimer le modèle

## <a name="see-also"></a>Voir aussi

[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Configurer la messagerie](admin-how-setup-email.md)  
