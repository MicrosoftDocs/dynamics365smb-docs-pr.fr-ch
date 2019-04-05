---
title: Migrer des données client | Microsoft Docs
description: Vous pouvez migrer les données client existantes d'un système ERP existant vers Business Central à l'aide de RapidStart Services. Vous pouvez utiliser des fichiers Excel (.xlsx) comme supports d’informations. Vous pouvez également déplacer manuellement les données en les entrant directement dans la société.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4dae4dbfc06b5040eba09df94fe13e7fce7b1940
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820219"
---
# <a name="migrate-customer-data"></a>Migrer des données client
Vous pouvez migrer des données client existantes d'un système ERP existant vers [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des outils de migration de données de RapidStart Services. Vous pouvez utiliser des fichiers Excel comme supports d’informations. Vous pouvez également déplacer manuellement les données en les entrant directement dans la société.

Les pages **Aperçu migration** et **Feuille config.** permettent d’accéder aux fonctionnalités et aux vues pour exécuter toutes les tâches associées à la migration des données. Il est recommandé de migrer une table à la fois, afin de gérer les dépendances dans vos données. Lors de la migration, vous toucherez également aux tables de données principales, contenant des informations relatives aux clients, fournisseurs, articles, contacts et à la comptabilité.  

## <a name="to-import-configuration-packages"></a>Pour importer des packages de configuration
Lorsque vous créez une société, vous pouvez importer les paramètres d'une société dans la nouvelle la société. Vous importez les paramètres à partir d'un fichier .rapidstart, qui fournit le contenu du package sous un format compressé. Un ensemble correspondant de tables de migration de données par défaut sont importées. L'ensemble de données contient des tables de données principales et les tables de données de configuration. Lors d'une migration de données, la première tâche consiste à déterminer si la configuration de la migration par défaut répond aux besoins de la nouvelle société.

> [!NOTE]  
>  Vous ne pouvez pas renommer un fichier qui n'est pas déjà un package de configuration RapidStart Services comme fichier de package de configuration .rapidstart puis tenter de l'importer. Si vous essayez de faire cela, un message d'erreur vous parviendra.  

Avant de commencer, vérifiez que vous vous trouvez dans le tableau de bord Responsable de l'implémentation de RapidStart Services.

> [!IMPORTANT]  
>  Lorsque vous exportez et importez des packages de configuration entre deux bases de données de votre société, les bases de données doivent avoir le même schéma pour garantir la réussite du transfert de toutes les données. Cela signifie que les bases de données doivent avoir la même table et structure de champ, dans lesquelles les tables ont les mêmes clés primaires et les champs ont les mêmes codes et types de données.  
>   
>  Vous pouvez importer un package de configuration qui a été exporté d'une base de données qui a un schéma différent que cette base de donnée cible. Toutefois, tous les tables ou champs du package de configuration manquants dans la base de données cible ne seront pas importés.
>   
> Les tables dont les clés primaires sont différents et les champs dont les types de données sont différents ne seront pas importés avec succès. Par exemple, si le package de configuration inclut une table **Client 50000** dont la clé primaire est **Code20** et que la base de données dans laquelle vous importez le package inclut la table **Compte bancaire client 50000** dont la clé primaire est **Code20 + Code 20**, les données ne seront pas importées.  

1. Ouvrez la nouvelle société.  
2. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.  
3. Sélectionnez l'action **Importer package**. Accédez au fichier de package .rapidstart à importer, puis sélectionnez l'action **Ouvrir**. Lors de l'importation, le contenu du package est décompressé et l'enregistrement de package est créé.  

    Lorsque l'importation est terminée, vous pouvez visualiser le nombre de tables de configuration qui ont été importées dans le champ **Nombre de tables**.  
4. Pour consulter la liste des tables de configuration, choisissez l'action **Afficher**.  
5. Pour appliquer le package, choisissez l'action **Appliquer package**.  

    > [!NOTE]  
    >  Les informations de migration de données sont basées sur les modèles de configuration, si vous en spécifiez un. Vous devez mettre à jour le modèle d’abord pour modifier la liste des champs.  

6.  Pour consulter les sélections de champ, sélectionnez une table, puis sous l'onglet **Lignes**, choisissez l'action **Champs**. Étudier et comparer le nombre de champs disponibles au nombre de champs dont les données ont été lettrées.  

Si la sélection de tables ne répond pas à vos besoins, vous pouvez créer un ou plusieurs fichiers de migration de données. Si les fichiers suffisent, vous pouvez continuer avec la migration de données à l’aide des fichiers Excel ou XML.

## <a name="to-create-a-data-migration-file"></a>Pour créer un fichier de migration de données
Vous pouvez créer de nouveaux fichiers de migration de données et les personnaliser pour prendre en charge les processus de l'entreprise. Notez qu'un fichier peut uniquement être utilisé pour migrer un champ dont la propriété **FieldClass** est définie sur **Normal**.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Package configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez et ouvrez le package que vous souhaitez utiliser pour migrer les données, puis sélectionnez l'action **Extraire tables**. La page **Extraire tables package** s’ouvre.  
3. Dans le champ **TableID**, entrez un numéro de table ou sélectionnez une table dans la liste, par exemple, la table 18, **Client**. Le champ **Nom table** est automatiquement renseigné.  
4. Sélectionnez la nouvelle table de migration, puis sous l'onglet **Tables**, choisissez l'action **Champs**. La page **Champs migration** s'ouvre.  
5. Désactivez la case à cocher **Inclure champ** pour tout champ que vous ne souhaitez pas importer, puis choisissez l'action **Définir inclus** ou **Effacer inclus**.  

> [!IMPORTANT]  
>  Si la case à cocher **Inclure champ** est activée par défaut, ce champ fait partie de la clé primaire. Elle ne doit pas être désactivée, car des erreurs se produiraient alors et il ne serait pas possible d'importer les enregistrements.  
>
>  Si vous incluez un champ qui a une relation avec une autre table, la case à cocher **Champ Valider** est automatiquement activée. La validation peut entraîner la mise à jour d'autres champs de cette table ou d'autres tables et elle est exécutée dans l'ordre des numéros de champs.  

Une nouvelle table de migration est créée.  

## <a name="to-export-data-migration-files"></a>Pour exporter les fichiers de migration de données
Lorsque vous avez déterminé les tables vers lesquelles vous souhaitez transférer les données client, vous exportez les fichiers.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez et ouvrez le package à utiliser pour l’exportation.
3. Sélectionnez la ou les tables que vous souhaitez exporter, puis sélectionnez l'action **Exporter vers Excel**.
4. Enregistrez le fichier Excel exporté.  
5. Répétez cette procédure pour toutes les tables de migration de données appropriées. Si vous sélectionnez plusieurs tables simultanément, leurs données sont exportées dans un classeur commun.  

Si la table est vide, le fichier de migration de données obtenu contient des cellules vides pour les champs que vous avez sélectionnés lors de la sélection ou la création des tables de migration pour votre société. Si la table de migration de données sélectionnée contient des données, elle sera exportée.  

## <a name="to-map-values-to-be-used-during-import"></a>Pour mapper les valeurs à utiliser lors de l'importation
Lorsque vous appliquez les données que vous avez importées d'Excel ou d'un package RapidStart, [!INCLUDE[d365fin](includes/d365fin_md.md)] traite et gère le mappage en fonction des relations de table :  

- Si vous définissez un mappage directement pour un champ dans un tableau, [!INCLUDE[d365fin](includes/d365fin_md.md)] l'utilise.  

- Si le champ a un rapport avec un autre tableau, [!INCLUDE[d365fin](includes/d365fin_md.md)] recherche le mappage défini pour le champ de clé primaire dans le tableau lié. Le tableau lié, cependant, doit faire partie du lot de configuration.  

- Si les informations de mappage sont définies dans les deux fenêtres, pour le champ directement et pour la clé primaire de le tableau associé, [!INCLUDE[d365fin](includes/d365fin_md.md)] cherchera le mappage aux deux emplacements.  

- Si les mêmes mappages sont définis directement pour un champ et dans le tableau lié, mais possèdent de nouvelles valeurs différentes, le mappage défini directement pour le champ est prioritaire sur le mappage défini pour le tableau que le champ référence.  

Dans les procédures suivantes, vous devez rechercher à l'avance les valeurs que vous souhaitez conserver lors du processus de migration. Pour effectuer la procédure suivante, vous avez besoin des fichiers de migration des données (.xlsx) que vous avez exportés depuis [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, reportez vous à [Pour exporter les fichiers de migration de données](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.
2. Ouvrez le package pour la société concernée.  
3. Sélectionnez la table pour laquelle vous souhaitez associer des valeurs, puis, sous l'onglet **Tables**, sélectionnez l'action **Champs**.  
4. Pour chaque champ à associer, choisissez l'action **Correspondance**.  
5. Dans le champ **Ancienne valeur**, saisissez la valeur que vous souhaitez modifier. Dans le champ **Nouvelle valeur**, saisissez la valeur dont vous souhaitez qu'elle remplace l'ancienne valeur. Choisissez le bouton **OK**.  
6. Importez les données client. Pour plus d'informations, voir [Pour importer les données client](admin-migrate-customer-data.md#to-import-customer-data).
7. Dans le champ **N° d'erreurs de lot**, vérifiez si des erreurs ont été signalées. S'il y en a, examinez les erreurs de près. La page **Enregistrements package config.** s'ouvre.
8. Choisissez l'action **Afficher erreur**. Vous recevrez l'erreur suivante : **<option> n'est pas une option valide. Les options valides sont <valid option list>**. Cliquez sur le bouton **OK**.  
9. Pour appliquer le mappage que vous avez paramétré, sélectionnez l'action **Appliquer données**.  

### <a name="mapping-example"></a>Exemple de mappage  
L'exemple suivant illustre comment [!INCLUDE[d365fin](includes/d365fin_md.md)] met en œuvre les définitions de mappage.  

1. Créez une table de configuration contenant une table **Vendeur/Acheteur**. Définissez un mappage pour le champ **Code**.  
2. Ajoutez des tables supplémentaires au package, par exemple **Client** et **Fournisseur**. Ces tableaux référencent la table **Vendeur/Acheteur** au moyen des champs **Code vendeur** et **Code acheteur**, respectivement.  
3. Lorsque vous appliquez des données, le mappage que vous avez fourni pour le champ **Code** dans la table **Vendeur/Acheteur** est également pris en compte lors du traitement des champs **Code vendeur** et **Code acheteur**.

## <a name="to-add-additional-values-to-included365finincludesd365finmdmd"></a>Pour ajouter des valeurs supplémentaires à [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez la table pour laquelle vous souhaitez ajouter des valeurs supplémentaires, puis sous l'onglet **Tables**, sélectionnez l'action **Champs**.  
3. Pour les champs pour lesquels vous souhaitez que [!INCLUDE[d365fin](includes/d365fin_md.md)] autorise des valeurs supplémentaires lors de la migration, cochez la case **Créer codes manquants**.  
4. Importez les données client. Pour plus d'informations, voir [Pour importer les données client](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Pour nettoyer et traiter les données avant d'appliquer les données
Dans certains cas, vous pouvez vouloir nettoyer les données du client et les traiter avant de les appliquer à la base de données. Pour ce faire, vous pouvez utiliser le traitement par lots **Package config. - Traitement** pour résoudre les problèmes, par exemple :  

- Convertissez les dates et les chiffres au format requis par les paramètres régionaux sur l'ordinateur d'un utilisateur.  
- Supprimez les espaces précédents/suivants ou les caractères spéciaux.  

Lorsque vous avez exécuté le traitement par lots, utilisez la procédure suivante pour traiter les données.  

1. Ouvrez le package de configuration pour la société.  
2. Choisissez l'action **Traiter les données**.  
3. Pour appliquer le mappage que vous avez paramétré, sélectionnez l'action **Appliquer données**.

## <a name="to-migrate-customer-data"></a>Pour migrer des données client
Lorsque vous avez exporté une table de migration, l'étape suivante consiste à entrer les données héritées du client. Pour simplifier vos tâches, vous pouvez mettre à profit les outils de gestion XML qui sont intégrés à Excel. Vous pouvez également utiliser les fonctions intégrées d'Excel pour procéder au formatage des données et placer des données dans la cellule qui convient.

Pour obtenir de l'aide concernant XML, activez l'onglet **Développeur** du ruban Excel, puis sélectionnez l'action **Source** pour afficher le schéma XML de votre table de migration représentée dans Excel.

La procédure suivante est basée sur une feuille de calcul Excel que vous avez créée pour la migration. Pour plus d'informations, reportez vous à [Pour exporter les fichiers de migration de données](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> Ne modifiez pas les colonnes dans les feuilles de calcul Excel. Si elles sont déplacées, modifiées ou supprimées, la feuille de calcul ne peut pas être importée dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Sous Excel, ouvrez le fichier de données exportées. Il existe une feuille avec le nom de la table.
2. Renommez Feuille1 de manière à indiquer que la feuille de calcul sera utilisée pour convertir les données. Copiez la ligne d'en-tête sans sa mise en forme, de la table exportée dans la nouvelle feuille de calcul.
3. Sur une troisième feuille de calcul, copiez toutes les données client. Renommez la feuille en « Données héritées ».
4. Créez une formule Excel permettant d'associer les données de la feuille de calcul de transformation (entre les champs de la feuille de calcul exportée et les données héritées du client).
5. Lorsque vous avez associé toutes les données, copiez la plage de données dans la feuille de calcul de la table.
6. Enregistrez le fichier en veillant à ne pas modifier le type de fichier.

Vous êtes maintenant prêt à importer les fichiers de migration de données qui contiennent les données héritées du client dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Pour importer les données client
Lorsque les données client ont été entrées dans les fichiers de migration de données de format Excel, vous importez ces fichiers dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Ouvrez la page **Fiche package config**.
2. Sélectionnez la table pour laquelle vous souhaitez importer des données, puis sous l'onglet **Tables**, sélectionnez l'action **Importer d'Excel**.
3. Recherchez et ouvrez le fichier à partir duquel vous voulez importer les données dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Les données du fichier sont importées dans les tables de package configuration. Vous pouvez consulter le nombre d'enregistrements package qui ont été importés dans le champ **Nombre enregistrements package**. Le nombre d'erreurs de migration est également indiqué.

## <a name="to-validate-customer-data"></a>Pour valider des données client
Les données client doivent être validées avant d'appliquer les enregistrements à la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Le plus souvent, les données invalides ne sont pas créées dans la base de données. Toutefois, l'application peut de temps à autre être bloquée si une table migration importée comporte des erreurs.  

1. Sur la page **Aperçu migration**, examinez le champ **Nombre de erreurs de migration** pour vérifier si des erreurs se sont produites lors de l'importation.  
2. S’il existe des erreurs, sélectionnez la table de migration, puis sous l'onglet **Tables**, sélectionnez l'action **Erreurs**. Le champ à cocher **Non valide** est sélectionné pour chaque enregistrement qui comporte une erreur.  
3. Pour examiner les erreurs, sélectionnez une ligne, puis choisissez l'action **Afficher erreur**.  

    Le champ **Texte erreur** indique le motif de l'erreur. Le champ **Légende champ** comprend le libellé du champ qui contient l'erreur.  
4.  Pour corriger une erreur ou effectuer une mise à jour, sur la page **Aperçu migration**, choisissez l'action **Enregistrement de migration**, puis sur la page **Enregistrement de migration**, corrigez l'enregistrement contenant l'erreur.  

Lorsque vous effectuez une correction, l'enregistrement est supprimé de la liste des enregistrements sur la page **Erreurs de migration des données**.  

Vous êtes maintenant prêt à appliquer les informations du client dans la base de données.  

## <a name="to-apply-customer-data"></a>Pour appliquer des données client
Lorsque vous avez importé tous les enregistrements de migration de données valides et sans erreurs, vous pouvez les appliquer à la base de données de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Ouvrez la page **Packages configuration**.  
2. Sélectionnez la table pour le fichier de migration des données à appliquer, puis sélectionnez l'action **Appliquer données**.

Vous pouvez consulter le nombre d'enregistrements de base de données qui ont été créés dans le champ **Nombre enregistrements base de données**. Vous pouvez vérifier que les enregistrements corrects ont été créés en cliquant sur le lien dans le champ **Nombre enregistrements base de données**.  

La base de données de la société du client est maintenant configurée et les données de base sont importées. Dans le processus d'implémentation, les étapes suivantes consistent à former les utilisateurs, définir des processus, créer d'autres données, personnaliser des états, etc.

## <a name="see-also"></a>Voir aussi  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
