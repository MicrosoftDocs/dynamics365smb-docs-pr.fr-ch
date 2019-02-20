---
title: Configurer les informations pour les contacts| Microsoft Docs
description: "Décrit les tâches pour spécifier les informations et les codes, par exemple, sur les secteurs d'activité et les relations d'affaires, avant de paramétrer des contacts."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: fr-ch
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Paramétrage des contacts
Lors de la création de contacts, vous pouvez saisir des informations spécifiques, telles que le secteur d'activité des sociétés contact et votre relation d'affaires avec elles.

Avant de créer des contacts et d'enregistrer les détails de vos relations d'affaires, vous devez configurer les différents codes que vous utiliserez pour affecter ces informations aux sociétés et personnes contact. Les codes peuvent être configurés pour les groupes de distribution, les secteurs d'activité, les relations d'affaires, les sources Web, les niveaux hiérarchiques et les responsabilités.

Grâce à la configuration de ces informations, la création de contacts est beaucoup plus organisée et la recherche de contacts selon un groupe particulier plus efficace. Tous les groupes de votre société pourront trouver ces informations qui permettent d'améliorer la communication avec les contacts.

En plus de configurer vos contacts, vous devez configurer les rapport établis avec vos contacts, tels que les clients potentiels, les banques, les consultants et les prestataires de services. Pour plus d'informations, voir [Configuration des relations d'affaires sur des sociétés contact](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Configuration des secteurs d'activité pour des sociétés contact
Les secteurs d'activité vous permettent d'indiquer le type de secteur auquel vos contacts appartiennent, par exemple la grande distribution et l'industrie automobile.

L'utilisation secteurs d'activité sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code secteur d'activité. Vous ne devez effectuer cette étape qu'une seule fois pour chaque secteur d'activité. Une fois que vous disposez d'un code secteur d'activité, vous pouvez commencer à affecter le code aux sociétés contact.

> [!NOTE]  
>   Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.

### <a name="to-define-an-industry-group-code"></a>Pour définir un code secteur d'activité
Le code secteur d'activité définit le type ou la catégorie du groupe, par exemple PUB pour la publicité, ou PRESSE pour la télévision et la radio. Vous pouvez disposer de plusieurs codes secteur d'activité. Pour définir les secteurs d'activité, utilisez la page **Secteurs d'activité**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Secteurs d'activité**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

### <a name="AssignIndustryGroupContact"></a> Pour affecter des secteurs d'activité à un contact
Vous ne pouvez pas affecter de secteurs d'activité à une personne contact, mais uniquement à des sociétés.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Secteurs d'activité**. La page **Secteurs d'activité contact** s'affiche.
3. Dans le champ **Code secteurs d'activité**, sélectionnez le secteur d'activité à affecter.

Répétez ces étapes pour chaque secteur d'activité à affecter. Vous pouvez également affecter des secteurs d'activité à partir de la liste des contacts en suivant la même procédure.

Le nombre de secteurs d'activité que vous avez affectés au contact s'affiche dans le champ **Nbre secteurs d'activité** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des secteurs d'activité à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Configuration des groupes de distribution pour les contacts
Les groupes distribution vous permettent d'identifier les groupes de contacts qui doivent recevoir les mêmes informations. Par exemple, vous pouvez configurer un groupe de distribution pour les contacts auxquels vous souhaitez envoyer un avis de déménagement, ou un autre groupe auquel envoyer des cadeaux pour les fêtes de fin d'année.

L'utilisation des groupes de distribution sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code groupe de distribution. Vous ne devez effectuer cette étape qu'une seule fois pour chaque groupe de distribution. Une fois que vous disposez d'un code groupe de distribution, vous pouvez commencer à affecter ce code aux sociétés contact.

### <a name="to-define-mailing-group-codes"></a>Pour définir des codes groupe de distribution
Le code groupe de distribution définit le type ou la catégorie du groupe, telles que DÉMÉNAGEMENT pour un déménagement des bureaux, ou CADEAU pour le cadeau de fêtes de fin d'année. Vous pouvez disposer de plusieurs codes secteur d'activité. Pour définir les groupes de distribution, utilisez la page **Groupes de distribution**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes de distribution**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

### <a name="AssignMailGroupContact"></a> Pour affecter des groupes de distribution à un contact
1. Ouvrez le contact.
2. Sélectionnez l'action **Groupes de distribution**. La sur la page **Groupes distribution contact** s'affiche.
3. Dans le champ **Code groupes de distribution**, sélectionnez le groupe de distribution à affecter.

Répétez ces étapes pour chaque groupe de distribution à affecter. Vous pouvez également affecter des groupes de distribution à partir de la liste des contacts en suivant la même procédure.

Le nombre de groupes de distribution affectés au contact s'affiche dans le champ **Nbre groupes de distribution** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des groupes de distribution à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Configuration d'adresses secondaires pour des contacts
Vous pouvez affecter une adresse secondaire pour l'envoi de messages et d'informations à vos contacts, par exemple leur résidence secondaire. Vous pouvez aussi affecter une ou plusieurs plages de dates aux adresses secondaires saisies pour vos contacts afin de spécifier les plages de dates de validité de ces adresses.

### <a name="to-assign-an-alternate-address"></a>Pour affecter une adresse secondaire
1. Ouvrez le contact.
2. Sélectionnez l'action **Adresse secondaire**, puis sélectionnez **Fiche**. La page **Liste adresses sec. contact** s'ouvre.
3. Entrez une nouvelle adresse secondaire et renseignez les champs de la page **Adresse secondaire du contact**.

Répétez ces étapes pour chaque adresse secondaire à affecter. Pour chaque adresse secondaire, vous pouvez indiquer une ou plusieurs plages de dates.

Vous pouvez également affecter des adresses secondaires à partir de la page de liste des contacts en suivant la même procédure.

### <a name="to-assign-an-alternate-address-date-range"></a>Pour affecter des plages de dates pour les adresses secondaires
1. Ouvrez le contact.
2. Sélectionnez l'action **Adresse secondaire**, puis sélectionnez **Plage de dates**. La page **Plage dates adr. sec. contact** s'ouvre.
3. Sélectionnez l'action **Nouveau**.
4. Dans le champ **Code adresse contact secondaire**, sélectionnez une adresse secondaire pour ce contact, puis renseignez les champs **Date de début** et **Date de fin** .

Répétez ces étapes pour chaque plage de dates à affecter.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Configuration des responsabilités pour les personnes contact
Vous pouvez ajouter des informations relatives aux responsabilités des personnes contact afin d'indiquer les tâches dont une personne contact est responsable au sein de sa société, par exemple, l'informatique, la gestion ou la production. Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.

L'utilisation des responsabilités sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code responsabilité. Vous ne devez effectuer cette étape qu'une seule fois pour chaque responsabilité. Une fois que vous disposez d'un code responsabilité, vous pouvez commencer à affecter ce code aux personnes contact.

### <a name="to-define-a-job-responsibility-code"></a>Pour définir un code de responsabilité
Le code responsabilité définit le type ou la catégorie du projet, par exemple MARKETING ou ACHAT. Vous pouvez disposer de plusieurs codes responsabilité. La page **Responsabilités** vous permet de définir la responsabilité.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Responsabilités**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Pour affecter des responsabilités à vos contacts
Vous ne pouvez pas affecter de responsabilités aux sociétés contact.

1. Ouvrez la fiche de la personne contact.
2. Sélectionnez l'action **Personne**, puis sélectionnez l'action **Responsabilités**. La page **Responsabilités contact** s'affiche.
3. Dans le champ **Code responsabilité**, sélectionnez la responsabilité que vous souhaitez affecter.

Répétez ces étapes pour chaque responsabilité à affecter. Vous pouvez également affecter des responsabilités à partir de la liste des contacts en suivant la même procédure.

Le nombre de responsabilités affectées au contact s'affiche dans le champ **Nbre responsabilités** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Configuration des niveaux hiérarchiques pour les personnes à contacter
Vous pouvez utiliser les niveaux hiérarchiques sur vos contacts pour qu'ils précisent leur position au sein de la société, par exemple, la direction générale. Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.

L'utilisation de niveaux hiérarchiques sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code de niveau hiérarchique. Vous ne devez effectuer cette étape qu'une seule fois pour niveau hiérarchique. Une fois que vous disposez d'un code de niveau hiérarchique, vous pouvez commencer à affecter ce code aux personnes contact.

### <a name="to-define-an-organizational-level-code"></a>Pour définir un code de niveau hiérarchique
Le code de niveau hiérarchique définit le type ou la catégorie du niveau hiérarchique, par exemple PDG ou DF. Vous pouvez disposer de plusieurs codes de niveau hiérarchique. Pour définir le niveau hiérarchique, vous utilisez la page **Niveaux organisationnels**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Niveaux hiérarchiques**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Pour affecter des niveaux hiérarchiques à une personne contact
Vous pouvez affecter des niveaux hiérarchiques aux personnes contact, mais pas aux sociétés contact. Vous ne pouvez affecter qu'un niveau hiérarchique par contact.

1. Ouvrez le contact.
2. Dans le champ **Niveaux organisationnels**, sélectionnez le code à affecter.

Une fois que vous avez affecté des niveaux hiérarchiques à vos contacts, vous pouvez utiliser ces données pour créer des segments.

Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Configuration de recherches Web pour des sociétés contact
Vous pouvez utiliser les recherches Web avec vos sociétés contact afin d'identifier, par exemple, des moteurs de recherche et des sites Web que vous souhaitez utiliser pour rechercher des informations relatives aux contacts. Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

L'utilisation des recherches Web au niveau des contacts est un processus en deux étapes. Tout d'abord, vous définissez le code recherche Web. Vous ne devez effectuer cette étape qu'une seule fois pour chaque recherche Web. Une fois que vous disposez d'un code recherche Web, vous pouvez commencer à affecter ce code aux personnes contact.

### <a name="to-define-a-web-source-code"></a>Pour définir un code recherche Web
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Recherche Web**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs **Code**, **Désignation** et **URL**.

    Tapez %1 dans le champ **URL** pour insérer un espace réservé correspondant au mot recherché dans l'URL. Lorsque vous lancez la recherche Web à partir d'un contact, le %1 est automatiquement remplacé par le mot recherché (par exemple le nom de la société) que vous avez saisi sur la page **Recherche contacts Web**.

Répétez ces étapes pour chaque recherche Web à configurer.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Pour affecter une recherche Web à une société contact
Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Recherche Web**. La page **Recherche contact Web** s'affiche.
3. Dans le champ **Code recherche web**, sélectionnez la recherche Web à affecter.
4. Dans le champ **Mot recherché**, saisissez le mot recherché à utiliser pour trouver les données.

Répétez ces étapes pour chaque recherche Web à affecter.

Vous pouvez également affecter des recherches web à partir de la page **Liste des contacts** en suivant la même procédure.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

