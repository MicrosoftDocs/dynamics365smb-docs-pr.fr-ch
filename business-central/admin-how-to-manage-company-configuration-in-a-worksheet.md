---
title: Procédure de gestion de la configuration de la société dans une feuille | Microsoft Docs
description: La feuille configuration est l’emplacement principal dans lequel vous pouvez planifier, suivre et effectuer votre travail de configuration. Vous pouvez créer une feuille pour chaque société avec laquelle vous travaillez ou créer une feuille configuration standard qui peut être utilisée pour configurer plusieurs sociétés identiques.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e90d17b2892744c768cd0383f91962fe51d2a0de
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752665"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>Gérer la configuration de la société dans une feuille
La feuille configuration est l’emplacement principal dans lequel vous pouvez planifier, suivre et effectuer votre travail de configuration. Vous pouvez créer une feuille pour chaque société avec laquelle vous travaillez ou créer une feuille configuration standard qui peut être utilisée pour configurer plusieurs sociétés identiques.  

La première étape de la préparation d’un package configuration est de sélectionner une société que vous avez déjà paramétrée et modifiée pour l’adapter à la plupart des besoins de votre solution. Cette société sert de base à votre travail de configuration pour les nouvelles sociétés. Dans la feuille, vous indiquez les tables que vous souhaitez que votre configuration contrôle et traite. Étant donné que la plupart des tables de [!INCLUDE[prod_short](includes/prod_short.md)] ont des relations et des dépendances avec d’autres tables, vous devez également inclure ces tables liées en cas de besoin. Ensemble, ces tables serviront ensuite de structure à partir de laquelle vous établirez une nouvelle société. La procédure suivante vous permet de créer un package, puis de déployer votre configuration.  

Pour vous aider à suivre et à consulter votre travail, utilisez le récapitulatif **Table package config.** pour visualiser les informations sur les enregistrements. Utilisez le récapitulatif **Config. Related Tables** pour contrôler les relations de table.  

Les procédures suivantes expliquent comment ajouter et personnaliser les informations de table pour votre configuration.  

## <a name="to-open-the-configuration-worksheet"></a>Pour ouvrir la feuille configuration  
1.  Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la société qui sert de base pour la configuration, puis ouvrez son tableau de bord Responsable de l’implémentation de RapidStart Services.  
2.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille configuration**, puis choisissez le lien associé.  

## <a name="to-add-a-table-to-the-worksheet"></a>Pour ajouter une table à la feuille  
1.  Sur la page **Feuille config.**, sélectionnez l’action **Modifier la liste**.  
2.  Sur la première ligne, dans le champ **Type ligne**, sélectionnez **Table**.  
4.  Dans le champ **ID table**, sélectionnez la table que vous souhaitez ajouter à votre configuration.  
5.  Dans le champ **ID page**, entrez l’ID de la page associée à la table. Pour les tables standard, cette valeur est automatiquement insérée. Pour les tables personnalisées, vous devez fournir l’ID.
6.  Dans le champ **Référence**, entrez l’URL d’une page de documentation, par exemple dans l’aide, qui fournit des informations sur les recommandations ou des instructions sur le paramétrage de la table.  
7.  Pour ajouter des tables associées, choisissez l’action **Extraire tables associées**.  

    > [!NOTE]  
    > Des tables connexes ne sont pas ajoutées à l’aide de l’action **Extraire les tables liées** si l’une des conditions suivantes est vraie :
    > - La relation est conditionnelle.  
    > Exemple : si vous obtenez des tables liées pour la table **Client**, la table **Magasin** n’est pas ajoutée, car elle est uniquement liée conditionnellement à la table **Client**, à savoir si le champ **Code magasin** dans la table **Client** est renseigné.  
    > - La table liée est filtrée.  
    > Exemple : un champ dans la table liée a une clause WHERE. La raison pour cela est que les informations des relations associées sont stockées dans la table système **Champ**, qui n’est pas totalement accessible à l’application.  
    > Vous devez ajouter de tels types de tableaux manuellement en suivant l’étape 4 dans cette procédure.  

8.  Pour modifier la liste des tables résultantes, sélectionnez une table que vous souhaitez supprimer, puis sélectionnez l’action **Supprimer**.  
9. Répétez les étapes pour chaque table que vous souhaitez ajouter à la configuration.  
10. Pour supprimer les informations de table en doublon, qui peuvent résulter de l’action **Extraire tables associées**, sélectionnez l’action **Supprimer les lignes en doublon**. Cette action supprime les tables en doublon ayant le même code de lot.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Pour ajouter plusieurs tables à la feuille configuration  
1. Sélectionnez l’action **Extraire tables**. La page de traitement par lots **Extraire table config.** s’ouvre.  
2. Sur le raccourci **Options**, spécifiez les types de tables à ajouter à la configuration, comme décrit dans le tableau suivant.

    |Option|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Inclure avec des données uniquement**|Activez la case à cocher pour n’inclure que les tables qui contiennent des données. Par exemple, vous souhaitez inclure une table qui définit déjà les conditions de paiement prises en charge par votre solution.|  
    |**Inclure les tables liées**|Activez cette case à cocher pour inclure toutes les tables liées. Pour ajouter un sous-ensemble de tables liées, reportez-vous à l’étape 3 dans cette procédure.|  
    |**Inclure les tables d’axes analytiques**|Cochez cette case pour inclure les tables axe analytique.|  
    |**Inclure les tables autorisées uniquement**|Activez la case à cocher pour n’inclure que les tables auxquelles la licence de création de la feuille vous permet d’accéder.|

3. Sur le raccourci **Objet**, définissez des filtres de manière appropriée pour spécifier les types de tables que vous souhaitez inclure ou exclure.  
4. Cliquez sur le bouton **OK**. Les tables [!INCLUDE[prod_short](includes/prod_short.md)] sont ajoutées à la feuille. Chaque écriture dans la liste a un type **Table**.  
5. Pour supprimer les informations de table en doublon, qui peuvent résulter de l’action **Extraire tables**, sélectionnez l’action **Supprimer les lignes en doublon**. Cette action supprime les tables en doublon ayant le même code de lot.  
6. Vous pouvez ajouter à la feuille des tables liées à une table que vous avez sélectionnée. Relisez les informations dans le récapitulatif **Tables associées** pour voir si des tables sont manquantes. Pour ajouter des tables liées pour une table spécifique, sélectionnez la table dans la liste, puis sélectionnez l’action **Extraire tables associées**.  

    > [!NOTE]  
    > Des tables connexes ne sont pas ajoutées à l’aide de l’action **Extraire les tables liées** si l’une des conditions suivantes est vraie :
    > - La relation est conditionnelle.  
    > Exemple : si vous obtenez des tables liées pour la table **Client**, la table **Magasin** n’est pas ajoutée, car elle est uniquement liée conditionnellement à la table **Client**, à savoir si le champ **Code magasin** dans la table **Client** est renseigné.  
    > - La table liée est filtrée.  
    > Exemple : un champ dans la table liée a une clause WHERE. La raison en est que les informations des relations associées sont stockées dans la table virtuelle **Champ** et ne sont pas disponibles sur des pages telles que la feuille de configuration, pour des raisons de performances.  
    > Vous devez ajouter des tables associées avec ces relations complexes manuellement en suivant l’étape 4 dans [Pour ajouter une table à la feuille](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).

7. Pour supprimer des tables dans la liste des tables résultantes, sélectionnez une table à supprimer, puis sélectionnez l’action **Supprimer**.  

La procédure ci-dessous permet de spécifier les champs de la table à inclure. Après que vous avez effectué cette spécification, vous pouvez exporter la table vers Excel et utiliser la structure de la table en tant que modèle pour réunir les données client. Pour plus d’informations, voir [Préparer la migration des données client](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Pour spécifier un ensemble de champs et d’enregistrements pour une table de configuration  
1. Sélectionnez une table dans la liste des tables de configuration, puis sélectionnez l’action **Modifier la liste**.  
2. Sélectionnez une table pour laquelle vous souhaitez spécifier des données de champ, puis sélectionnez l’action **Champs**.  
3. Pour sélectionner uniquement les champs que vous souhaitez inclure, sélectionnez l’action **Effacer Inclus**. Pour ajouter tous les champs, choisissez l’action **Définir inclus**.  
4. Pour indiquer que les données de champ ne doivent pas être validées, désactivez la case à cocher **Valider champ** pour le champ.  
5. Cliquez sur le bouton **OK**.  
6. Pour filtrer un certain ensemble d’enregistrements à inclure dans la feuille configuration, sélectionnez l’action **Filtres**, puis spécifiez les valeurs de filtre appropriées.

Vous pouvez créer des modules de fonctionnalités et des groupes de tables dans la feuille, afin de regrouper les fonctionnalités similaires. Par exemple, en paramétrant le plan comptable pour votre configuration, vous pouvez choisir de créer un groupe de tables de validation. En général, les zones sont utilisées pour regrouper un ensemble de tables correspondant à un module fonctionnel. Chaque zone peut contenir des groupes. Un groupe permet d’organiser les tables ayant une signification commune.  

La procédure suivante décrit comment ajouter des désignations de zone et de groupe, après avoir créé la liste de tables initiale. Après avoir ajouté ces catégories, vous pouvez continuer pour ajouter et modifier votre liste de tables.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Pour octroyer une catégorie et regrouper la fonctionnalité de la feuille  
1. Au début d’une zone, insérez une nouvelle ligne dans la feuille.  
2. Dans le champ **Type ligne**, choisissez **Zone**. Dans le champ **Nom**, entrez un nom pour la zone.  
3. Au début d’un regroupement de tables, insérez une nouvelle ligne dans la feuille.  
4. Dans le champ **Type ligne**, choisissez **Groupe**. Dans le champ **Nom**, entrez un nom pour la zone. Le nom du groupe est automatiquement indenté.  
5. Pour déplacer des tables vers la catégorie appropriée, sélectionnez une table à déplacer, puis choisissez l’action **Déplacer vers le haut** ou **Déplacer vers le bas**. Sinon, vous pouvez supprimer une ligne feuille et insérer la table à nouveau dans le magasin requis.  

Certaines tables [!INCLUDE[prod_short](includes/prod_short.md)] sont standard et les données qu’elles contiennent ne sont pas susceptibles d’être modifiées d’une implémentation à l’autre. Par conséquent, pour aider votre client à se concentrer, vous pouvez supprimer ces tables de la feuille une fois que vous les avez incluses dans le package configuration. Une fois ajoutées, les tables demeurent une partie des packages configuration.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Pour supprimer une table standard dans la feuille  
Après avoir ajouté toutes les tables nécessaires à un package configuration, déterminez quelles tables ne requerront pas l’attention du client.  
1.  Sélectionnez les tables, puis supprimez-les en choisissant l’action **Supprimer**.  

    > [!NOTE]  
    >  Les tables restent dans le package même si elles soient supprimées de la feuille.  

## <a name="to-review-and-customize-existing-database-data"></a>Pour vérifier et personnaliser les données existantes de base de données
Lors de la création d’un package configuration pour une solution, vous pouvez consulter et personnaliser les données de base de données disponibles pour les adapter aux besoins de votre client. La table de base de données doit être associée à une page.  

## <a name="to-customize-data-in-the-database"></a>Pour personnaliser des données dans la base de données  

1.  Sur la page **Feuille de configuration**, identifiez les tables dont vous souhaitez afficher ou personnaliser les données.  

    > [!NOTE]  
    >  Assurez-vous que chaque table dispose d’un ID page qui lui est affecté. Pour les tables [!INCLUDE[prod_short](includes/prod_short.md)] standard, cette valeur est automatiquement insérée. Pour les tables personnalisées, vous devez fournir l’ID.  

2.  Choisissez l’action **Données base de données**.  

     La page [!INCLUDE[prod_short](includes/prod_short.md)] pour la page s’ouvre.  

3.  Révisez les informations disponibles. Modifiez-les selon vos besoins en supprimant les enregistrements qui ne sont pas appropriés ou en ajoutant de nouveaux enregistrements.

## <a name="see-also"></a>Voir aussi  
[Configurer une société](admin-set-up-company-configuration.md)  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
