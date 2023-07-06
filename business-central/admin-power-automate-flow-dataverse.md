---
title: Utiliser un flux Power Automate pour les alertes aux changements d’entité
description: Découvrez comment créer un flux dans Power Automate qui vous alertera lorsqu’une entité est modifiée dans l’environnement Dataverse.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a><a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a><a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Utiliser un flux Power Automate pour les alertes aux changements d’entité Dataverse

Les administrateurs peuvent créer un flux automatisé dans Power Automate qui avertit votre [!INCLUDE[prod_short](includes/prod_short.md)] sur les modifications apportées aux enregistrements de votre organisation [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

> [!NOTE]
> Cet article suppose que vous avez connecté votre version en ligne de [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE [cds_long_md](includes/cds_long_md.md)] et une synchronisation planifiée entre les deux applications.

## <a name="import-the-flow-template"></a><a name="import-the-flow-template"></a><a name="import-the-flow-template"></a>Importer le modèle de flux

> [!TIP]
> Pour faciliter la configuration du flux, nous avons créé un modèle qui définira pour vous le déclencheur et la condition du flux. Pour utiliser le modèle, suivez les étapes de cette section. Pour créer le flux vous-même, ignorez cette section et commencez par les étapes disponibles dans la section [Définir le déclencheur de flux](#define-the-flow-trigger).

1. Connectez-vous à [Power Automate](https://powerautomate.microsoft.com).
2. Choisissez **Modèles**, puis recherchez **Notifier Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Mots-clés pour trouver le modèle de flux.":::
3. Choisissez le modèle **Notifier Business Central d’un changement de compte**.
4. Continuez avec les étapes indiquées à la section [Notifier Business Central d’un changement](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a><a name="define-the-flow-trigger"></a><a name="define-the-flow-trigger"></a>Définir le déclencheur de flux

1. Connectez-vous à [Power Automate](https://flow.microsoft.com).
2. Créez un flux cloud automatisé qui démarre lorsqu’une ligne pour une entité [!INCLUDE [cds_long_md](includes/cds_long_md.md)] est ajoutée, modifiée ou supprimée. Pour plus d’informations, voir [Déclencher des flux lorsqu’une ligne est ajoutée, modifiée ou supprimée](/power-automate/dataverse/create-update-delete-trigger). Cet exemple utilise l’entité **Comptes**. L’image suivante montre les paramètres de la première étape de la définition d’un déclencheur de flux.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Paramètres du déclencheur du flux":::
3. Utilisez le bouton **AssistEdit (...)** dans le coin supérieur droit pour ajouter la connexion à votre environnement [!INCLUDE [cds_long_md](includes/cds_long_md.md)].
4. Sélectionnez **Afficher les options avancées**, et dans le champ **Filtrer les lignes**, saisissez **customertypecode eq 3** ou **customertypecode eq 11** et **statecode eq 0**. Ces valeurs signifient que le déclencheur ne réagira que lorsque des modifications seront apportées aux comptes actifs du type **client** ou **fournisseur**.

## <a name="define-the-flow-condition"></a><a name="define-the-flow-condition"></a><a name="define-the-flow-condition"></a>Définir la condition du flux

Les données sont synchronisées entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE [cds_long_md](includes/cds_long_md.md)] via un compte utilisateur d’intégration. Pour ignorer les modifications apportées par la synchronisation, créez une étape de condition dans votre flux qui exclut les modifications apportées par le compte d’utilisateur d’intégration.  

1. Ajoutez une étape **Obtenir une ligne de Dataverse par son identificateur** après le déclencheur de flux avec les paramètres suivants. Pour plus d’informations, voir [Obtenir une ligne de Dataverse par son identificateur](/power-automate/dataverse/get-row-id).

    1. Dans le champ **Nom de table**, choisissez **Utilisateurs**
    2. Dans le champ **ID de ligne**, choisissez **Modifié par (valeur)** depuis le déclencheur de flux.  

2. Ajoutez une étape de condition avec ce qui suit **ou** les paramètres pour identifier le compte d’utilisateur d’intégration.
    1. Les utilisateurs **Adresse e-mail principale** contient **contoso.com**
    2. Le **Nom complet** de l’utilisateur contient **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Ajoutez un contrôle Terminer pour arrêter le flux si l’entité a été modifiée par le compte d’utilisateur d’intégration.

L’image suivante montre comment définir le déclencheur de flux et la condition de flux.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Présentation du déclencheur de flux et des paramètres de condition":::

## <a name="notify-business-central-about-a-change"></a><a name="notify-business-central-about-a-change"></a><a name="notify-business-central-about-a-change"></a>Notifier Business Central d’un changement

Si le flux n’est pas arrêté par la condition, vous devez notifier [!INCLUDE[prod_short](includes/prod_short.md)] qu’un changement s’est produit. Utiliser le connecteur [!INCLUDE[prod_short](includes/prod_short.md)] pour ce faire.

1. À l’embranchement **Non** de l’étape de condition, ajoutez une action et recherchez **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Choisissez l’icône du connecteur dans la liste.
2. Sélectionnez l’action **Créer un enregistrement (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Paramètres pour le connecteur [!INCLUDE[prod_short](includes/prod_short.md)]":::

3. Utilisez le bouton **assist edit (...)** dans le coin supérieur droit pour ajouter la connexion à votre environnement [!INCLUDE[prod_short](includes/prod_short.md)].
4. Une fois connecté, remplissez les champs **Nom de l’environnement** et **Nom de l’entreprise**.
5. Dans le champ **Catégorie d’API**, entrez **microsoft/dataverse/v1.0**.
6. Dans le champ **Nom de table**, saisissez **dataverseEntityChanges**.
7. Dans le champ **entityName**, saisissez **account**.
8. Enregistrez le flux.

L’image suivante indique à quoi doit ressembler votre flux.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Vue d’ensemble de tous les paramètres du flux":::

Lorsque vous ajoutez, supprimez ou modifiez un compte dans votre environnement [!INCLUDE [cds_long_md](includes/cds_long_md.md)], ce flux effectue les actions suivantes :

1. Appelez l’environnement [!INCLUDE[prod_short](includes/prod_short.md)] que vous avez spécifié dans le connecteur [!INCLUDE[prod_short](includes/prod_short.md)].
2. Utilisez l’API [!INCLUDE[prod_short](includes/prod_short.md)] pour insérer un enregistrement avec **entityName** défini sur **compte** dans la table **Modification de l’entrée Dataverse**. Ce paramètre est le nom exact de l’entité Dataverse pour laquelle vous créez le flux.
3. [!INCLUDE[prod_short](includes/prod_short.md)] lance l’entrée de la file d’attente des tâches qui synchronise les clients avec les comptes.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Utiliser Business Central dans les flux Power Automate](across-how-use-financials-data-source-flow.md)  
[Configurer des flux de travail automatisés](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Intégration à Microsoft Dataverse](admin-common-data-service.md)  
[Synchronisation des données dans Business Central avec Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
