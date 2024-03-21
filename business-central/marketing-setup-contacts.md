---
title: Configurer les informations pour les contacts| Microsoft Docs
description: 'Décrit les tâches pour spécifier les informations et les codes, par exemple, sur les secteurs d’activité et les relations d’affaires, avant de paramétrer des contacts.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-contacts"></a>Configurer les contacts
Lors de la création de contacts, vous pouvez saisir des informations spécifiques, telles que le secteur d’activité du contact et votre relation d’affaires avec elles.

Avant de créer des contacts et d’enregistrer les détails de vos relations d’affaires, vous devez configurer les différents codes que vous utiliserez pour affecter ces informations aux sociétés et personnes contact. Les codes peuvent être configurés pour les groupes de distribution, les secteurs d’activité, les relations d’affaires, les sources Web, les niveaux hiérarchiques et les responsabilités. Vous pouvez les configurer en choisissant l’action **Nouveau** comme lorsque vous recherchez des listes depuis la fiche contact.  

Grâce à la configuration de ces informations, la création de contacts est beaucoup plus organisée et la recherche de contacts selon un groupe particulier plus efficace. Tous les groupes de votre société pourront trouver ces informations qui permettent d’améliorer la communication avec les contacts.

## <a name="to-assign-industry-groups-to-a-contact"></a>Pour affecter des secteurs d’activité à un contact
Les secteurs d’activité vous permettent d’indiquer le type de secteur auquel vos contacts appartiennent, par exemple la grande distribution et l’industrie automobile.

> [!NOTE]
> Cela s’applique uniquement aux contacts de type **Société**.

Le code secteur d’activité définit le type ou la catégorie du groupe, par exemple PUB pour la publicité, ou PRESSE pour la télévision et la radio. Vous pouvez disposer de plusieurs codes secteur d’activité. Pour définir les secteurs d’activité, utilisez la page **Secteurs d’activité**.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Société**, puis l’action **Secteurs d’activité**. La page **Secteurs d’activité contact** s’affiche.
3. Dans le champ **Code secteurs d’activité**, sélectionnez le secteur d’activité à affecter.

Répétez ces étapes pour chaque secteur d’activité à affecter. Vous pouvez également affecter des secteurs d’activité à partir de la liste des contacts en suivant la même procédure.

Le nombre de secteurs d’activité que vous avez affectés au contact s’affiche dans le champ **Nbre secteurs d’activité** de la section **Segmentation** de la page **Fiche Contact**.

Une fois que vous avez affecté des secteurs d’activité à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d’informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="to-assign-mailing-groups-to-a-contact"></a>Pour affecter des groupes de distribution à un contact
Les groupes distribution vous permettent d’identifier les groupes de contacts qui doivent recevoir les mêmes informations. Par exemple, vous pouvez configurer un groupe de distribution pour les contacts auxquels vous souhaitez envoyer un avis de déménagement, ou un autre groupe auquel envoyer des cadeaux pour les fêtes de fin d’année.

Le code groupe de distribution définit le type ou la catégorie du groupe, telles que DÉMÉNAGEMENT pour un déménagement des bureaux, ou CADEAU pour le cadeau de fêtes de fin d’année. Vous pouvez disposer de plusieurs codes secteur d’activité. Pour définir les groupes de distribution, utilisez la page **Groupes de distribution**.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Groupes de distribution**. La sur la page **Groupes distribution contact** s’affiche.
3. Dans le champ **Code groupes de distribution**, sélectionnez le groupe de distribution à affecter.

Répétez ces étapes pour chaque groupe de distribution à affecter. Vous pouvez également affecter des groupes de distribution à partir de la liste des contacts en suivant la même procédure.

Le nombre de groupes de distribution affectés au contact s’affiche dans le champ **Nbre groupes de distribution** de la section **Segmentation** de la page **Fiche Contact**.

Une fois que vous avez affecté des groupes de distribution à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d’informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="to-define-a-contacts-alternate-address"></a>Pour définir l’adresse secondaire d’un contact
Vous pouvez affecter une adresse secondaire pour l’envoi de messages et d’informations à votre contact, par exemple sa résidence secondaire. Vous pouvez aussi affecter une ou plusieurs plages de dates aux adresses secondaires saisies pour vos contacts afin de spécifier les plages de dates de validité de ces adresses.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Adresse secondaire**, puis sélectionnez l’action **Fiche**.

    Pour définir que l’adresse secondaire s’applique pour une période précise, cliquez sur l’action **Plage de dates** à la place.
3. Sur la page **Liste adresses sec. contact**, entrez une nouvelle adresse secondaire et renseignez les champs de la page **Adresse secondaire du contact**.

Répétez ces étapes pour chaque adresse secondaire à affecter. Pour chaque adresse secondaire, vous pouvez indiquer une ou plusieurs plages de dates.

## <a name="to-assign-job-responsibilities-to-a-contact"></a>Pour affecter des responsabilités à un contact
Vous pouvez ajouter des informations relatives aux responsabilités des personnes contact afin d’indiquer les tâches dont une personne contact est responsable au sein de sa société, par exemple, l’informatique, la gestion ou la production. Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.

> [!NOTE]
> Cela s’applique uniquement aux contacts de type **Personne**.

Le code responsabilité définit le type ou la catégorie du projet, par exemple MARKETING ou ACHAT. Vous pouvez disposer de plusieurs codes responsabilité. La page **Responsabilités** vous permet de définir la responsabilité.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Personne**, puis sélectionnez l’action **Responsabilités**. La page **Responsabilités contact** s’affiche.
3. Dans le champ **Code responsabilité**, sélectionnez la responsabilité que vous souhaitez affecter.

Répétez ces étapes pour chaque responsabilité à affecter. Vous pouvez également affecter des responsabilités à partir de la liste des contacts en suivant la même procédure.

Le nombre de responsabilités affectées au contact s’affiche dans le champ **Nbre responsabilités** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d’informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="to-assign-organizational-levels-to-a-contact"></a>Pour affecter des niveaux hiérarchiques à un contact
Vous pouvez utiliser les niveaux hiérarchiques sur vos contacts pour qu’ils précisent leur position au sein de la société, par exemple, la direction générale. Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.

> [!NOTE]
> Cela s’applique uniquement aux contacts de type **Personne**.

Le code de niveau hiérarchique définit le type ou la catégorie du niveau hiérarchique, par exemple PDG ou DF. Vous pouvez disposer de plusieurs codes de niveau hiérarchique. Pour définir le niveau hiérarchique, vous utilisez la page **Niveaux organisationnels**.

1. Ouvrez la fiche contact appropriée.
2. Dans le champ **Niveaux organisationnels**, sélectionnez le code à affecter.

Une fois que vous avez affecté des niveaux hiérarchiques à vos contacts, vous pouvez utiliser ces données pour créer des segments.

Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d’informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="to-assign-web-sources-to-a-contact"></a>Pour affecter des ressources Web à un contact
Vous pouvez utiliser les recherches Web avec vos sociétés contact afin d’identifier, par exemple, des moteurs de recherche et des sites Web que vous souhaitez utiliser pour rechercher des informations relatives aux contacts. Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l’application doit utiliser pour trouver les données demandées.

> [!NOTE]
> Cela s’applique uniquement aux contacts de type **Société**.

Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l’application doit utiliser pour trouver les données demandées.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Société**, puis l’action **Recherche Web**. La page **Recherche contact Web** s’affiche.
3. Dans le champ **Code recherche web**, sélectionnez la recherche Web à affecter.
4. Dans le champ **Mot recherché**, saisissez le mot recherché à utiliser pour trouver les données.

Répétez ces étapes pour chaque recherche Web à affecter.

## <a name="to-assign-business-relations-to-a-contact"></a>Pour affecter des relations d’affaires à un contact
Les relations d’affaires vous permettent d’indiquer les rapports établis avec vos contacts, tels que les prospects, les banques, les consultants, les prestataires de services, et ainsi de suite.

> [!NOTE]
> Cela s’applique uniquement aux contacts de type **Société**.

1. Ouvrez la fiche contact appropriée.
2. Sélectionnez l’action **Société**, puis l’action **Relations d’affaires**.
3. Sur la page **Relations d’affaires contact**, dans le champ **Code relation d’affaires**, sélectionnez la relation d’affaires à affecter.

Répétez ces étapes pour chaque relation d’affaires à affecter.

Le nombre de relations d’affaires que vous avez affectées au contact s’affiche dans le champ **Nbre relations d’affaires** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des relations d’affaires à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d’informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Copie automatique des informations spécifiques des sociétés contact vers les personnes contact
Une partie des données relatives aux sociétés contact sont identiques aux données sur les personnes contact qui travaillent dans ces sociétés, comme l’adresse. Sur l’organisateur **Héritage** de la page **Paramètres marketing**, vous pouvez définir des champs de la fiche contact d’une société à copier vers la fiche contact d’une personne chaque fois que vous créez une personne contact pour une société contact.

Lorsque vous modifiez l’un des champs dans la fiche société contact, les mêmes champs de la fiche personne contact sont mis à jour, sauf si vous avez modifié ce champ manuellement.

Pour plus d’informations, reportez-vous à [Créer des contacts](marketing-create-contact-companies.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Utiliser des paramètres par défaut prédéfinis sur les nouveaux contacts
Vous pouvez configurer l’application pour qu’elle affecte automatiquement des codes langue, secteur, vendeur et pays/région par défaut à chaque nouveau contact. Vous pouvez également entrer un code cycle de vente par défaut que l’application affecte automatiquement à chaque nouvelle opportunité. Vous définissez cela à partir de l’organisateur **Valeurs par défaut** sur la page **Paramètres marketing**

Les valeurs héritées des champs sont prioritaires sur les valeurs par défaut que vous avez définies. Par exemple, si vous avez choisi le français comme langue par défaut alors que la langue de la société contact est l’allemand, l’application affecte automatiquement le code langue de l’allemand aux personnes contact enregistrées pour cette société.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires
Pour synchroniser la fiche contact avec un client, fournisseur, ou la fiche compte bancaire liée, vous devez renseigner le champ approprié de la section **Code relation d’affaires pour** sur l’organisateur **Interactions** sur la page **Paramètres marketing**.  

Pour plus d’informations, reportez-vous à [Procédure de synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

## <a name="searching-for-duplicate-contacts"></a>Recherche de doublons de contacts
Vous pouvez configurer l’application pour qu’il recherche automatiquement les doublons chaque fois que vous créez un contact ou vous pouvez choisir d’effectuer une recherche manuelle lorsque les contacts sont créés. Vous pouvez également configurer l’application pour qu’il mette automatiquement à jour les chaînes de recherche chaque fois que vous modifiez les données de contact ou que vous créez un contact. Vous pouvez choisir le pourcentage de chaînes communes, c’est-à-dire le pourcentage de chaînes qui doivent être identiques dans deux contacts pour que l’application les considère comme des doublons. Vous définissez cela à partir de l’organisateur **Doublons** sur la page **Paramètres marketing**.

Une fois que vous avez trouvé un doublon de contact, vous pouvez utiliser la page **Fusionner le doublon** pour le fusionner en un enregistrement de contact existant que vous souhaitez conserver. Pour en savoir plus, reportez-vous à la rubrique [Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md).

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Créer des contacts](marketing-create-contact-companies.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
