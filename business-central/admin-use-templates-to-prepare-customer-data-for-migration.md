---
title: "Préparer la migration des données client | Microsoft Docs"
description: "Une fois que vous avez importé et appliqué les données de configuration dans la nouvelle base de données, vous pouvez commencer la migration des données de base existantes du client (nom et numéro du client et des articles, par exemple). Pour créer ces données avec rapidité et précision dans la nouvelle société, vous devez utiliser des modèles pour structurer les données."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8724bf11537b384ae88960e40f24f1d9dbbbd484
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Préparer la migration des données client
Une fois que vous avez importé et appliqué les données de configuration dans la nouvelle base de données, vous pouvez commencer la migration des données de base existantes du client (nom et numéro du client et des articles, par exemple). Pour créer ces données avec rapidité et précision dans la nouvelle société, vous devez utiliser des modèles pour structurer les données.  

Généralement, vous pouvez créer des modèles de données pour les tables de données principales suivantes :  

-   **Contact**  
-   **Client**  
-   **Article**  
-   **Fournisseur**  

Vous pouvez toutefois créer une structure de modèle et l'appliquer à une table dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Vous pouvez également utiliser des modèles de données pour les opérations quotidiennes de manière à créer des enregistrements basés sur des modèles. Ces modèles de données ne fonctionnent qu'avec les tables de données principales prises en charge. Pour plus d'informations, reportez vous, par exemple, à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

Lorsque vous importez des données client, comme des articles, à partir d’un fichier, les données de champ obligatoires que vous avez spécifiées sont collectées à partir du modèle de données lié. Lorsque vous créez un article, vous n’entrez que des informations générales (nom article, description et prix) et vous collectez ensuite le reste des données de champ obligatoires à partir d’un modèle de données sélectionné.  

Lorsque vous créez un enregistrement de données de base, par exemple une fiche client, certains champs doivent être obligatoirement renseignés. Vous pouvez regrouper la plupart des champs obligatoires, tels que les groupes de comptabilisation et les conditions de paiement, pour faciliter la création des enregistrements de données de base et les rendre et plus stables. Par exemple, vous pouvez regrouper les champs obligatoires de la table 18 (**Client**) en fonction du type **National**, **International** ou **Exporter**.

## <a name="to-select-a-data-template"></a>Pour sélectionner un modèle de données
Lorsque vous sélectionnez un modèle de données existant, vous devez évaluer si les modèles que vous avez créés pour la nouvelle société sont suffisants pour le client. Consultez les champs et les valeurs indiqués pour déterminer les modèles appropriés pour une nouvelle société.  

> [!TIP]  
>  Vous pouvez également utiliser des modèles de données afin de créer rapidement des enregistrements. Ils vous permettent de créer des données avec une rapidité et une précision accrues. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles configuration**, puis sélectionnez le lien associé.  
2. Dans la fenêtre **Liste modèles config.**, sélectionnez un modèle de données dans la liste, puis choisissez l'action **Modifier**.  

Si les modèles par défaut ne répondent pas à vos besoins, vous pouvez créer de nouveaux modèles ou ajouter des champs à un modèle existant. Si les modèles par défaut sont suffisants, vous pouvez les utiliser pour créer des enregistrements à partir de modèles de données de base.

## <a name="to-create-a-data-template"></a>Pour créer un modèle de données
Vous pouvez créer un nouveau modèle de données si les modèles par défaut ne répondent pas aux besoins de votre société. Si vous en créez plusieurs, il peut être utile d'adopter une convention de dénomination pour le champ **Code**.

Chaque modèle est constitué d'un en-tête et de lignes. Lorsque vous créez un modèle, vous pouvez spécifier les champs à toujours appliquer aux données d’un certain type. Par exemple, vous pouvez créer différents modèles client pour appliquer différents types de client. Lorsque vous créez le client à l’aide d’un modèle, vous pouvez utiliser les données du modèle pour prérenseigner certains champs.

### <a name="to-create-a-data-template-header"></a>Pour créer un en-tête de modèle de données
1. Ouvrez la fenêtre **Liste modèles config**.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **ID table**, entrez la table à laquelle ce modèle s'applique. Le champ **Nom table** est automatiquement renseigné lorsque le champ **ID table** est défini.

### <a name="to-create-a-data-template-line"></a>Pour créer une ligne de modèle de données
1. Sur la première ligne, sélectionnez le champ **Nom champ**. La fenêtre **Liste des champs** affiche la liste des champs de la table.
2. Sélectionnez un champ, puis cliquez sur le bouton **OK**. Le champ **Légende champ** est renseigné avec le nom du champ.
3. Dans le champ **Valeur par défaut**, entrez une valeur appropriée. Dans certains cas, vous pouvez utiliser une valeur qui n’est pas une valeur disponible dans la base de données. Dans ce cas, vous pouvez cocher la case **Ignorer vérification relation** pour permettre le lettrage de données sans erreur.

    > [!TIP]  
    > Dans la mesure où le champ **Valeur par défaut** ne permet pas de rechercher les options de champ [!INCLUDE[d365fin](includes/d365fin_md.md)] correspondantes, vous copiez et collez la valeur requise de la page associée vers le modèle.

    > Activez la case à cocher **Obligatoire**. La case est à titre d’information uniquement. Elle vous indique que les informations doivent être entrées dans le champ par l’utilisateur, mais aucune logique métier n’est appliquée. Par exemple, il n’est pas possible de facturer et valider une commande si les groupes comptabilisation n’ont pas été paramétrés. Étant donné que les groupes comptabilisation sont nécessaires, vous pouvez cocher la case **Obligatoire** pour ces champs.

3. Dans le champ **Référence**, entrez les informations relatives au champ comme vous le souhaitez.
4. Cliquez sur le bouton **OK**.

## <a name="to-export-to-a-template-in-excel"></a>Pour effectuer une exportation vers un modèle dans Excel
Vous pouvez rapidement créer un classeur Excel qui servira de modèle basé sur la structure d’une table de données de base existante. Vous pouvez alors utiliser ce modèle pour rassembler les données du client sous un format cohérent afin de les importer ultérieurement dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille configuration**, puis sélectionnez le lien associé.
2. Ajoutez une table dans la liste ou sélectionnez une table existante. Pour plus d'informations, voir [Gérer la configuration de la société dans une feuille](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Définissez les champs de la table à inclure dans le modèle.
4. Choisissez l'action **Exporter vers modèle**.
5. Nommez et enregistrez le fichier Excel. Le classeur Excel est automatiquement ouvert.

Vous pouvez désormais entrer des données client dans la feuille de calcul Excel. Si vous avez exporté plusieurs tables, chaque table figure sur la feuille correspondante. Enregistrez le classeur avant de passer à la procédure suivante.

> [!NOTE]  
> L’erreur suivante peut se produire lorsque vous exécutez une version anglaise d’Excel, mais que les paramètres régionaux sont configurés pour une langue autre que l’anglais : « Ancien format ou bibliothèque de type non valide ». Pour corriger cette erreur, assurez-vous que le module linguistique de la langue autre que l’anglais est installé.

## <a name="to-import-from-a-template-in-excel"></a>Pour effectuer une importation à partir d’un modèle dans Excel
1. Dans la fenêtre **Feuille config**, sélectionnez l'action **Importer depuis modèle**.
3. Accédez au modèle de feuille que vous avez créé, puis sélectionnez l'action **Ouvrir**.
4. Pour ajouter les données client collectées à la base de données, choisissez l'action **Appliquer données**.

Lorsque vous appliquez des données à partir d’un modèle dans Excel dans une table contenant également un modèle de configuration associé à celles-ci dans le package configuration, les valeurs de champ par défaut du modèle de configuration sont également appliquées.

Tous les enregistrements dont les données sont appliquées de cette manière sont complets, car ils sont composés des données saisies par un utilisateur dans Excel et les valeurs par défaut spécifiées par le modèle de configuration.

## <a name="to-create-a-record-from-a-configuration-template"></a>Pour créer un enregistrement à partir d’un modèle de configuration
Vous pouvez utiliser la structure de données qui est contenue dans les modèles de données pour convertir les informations en enregistrements de la base de données, un par un. Pour ce faire, utilisez la fonction **Créer instance** . Il s'agit d'une version miniature du processus de migration des données et peut être utile pour le prototypage ou le traitement des petites tâches de création de données.  

Les étapes suivantes illustrent la création d'une fiche article d'un modèle données d'article. Vous pouvez créer un enregistrement à partir de n'importe quel modèle de données en utilisant la même procédure.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez le modèle **Article**, puis cliquez sur l'action **Modifier**. Pour plus d’informations, consultez la section « Pour créer un modèle de données ».
3. Sélectionnez l'action **Créer instance**. Une fiche article est créée.  
4. Cliquez sur le bouton **OK**.  
5. Pour vérifier la nouvelle fiche article, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.  
6. Ouvrez la nouvelle fiche article.  
7. Affichez les différents raccourcis, et vérifiez que les informations les concernant ont été créées correctement.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Pour utiliser un modèle de configuration sur un enregistrement
Vous pouvez appliquer un modèle de données à un enregistrement qui figure dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et utiliser cette technique pour modifier un enregistrement. Lorsque vous suivez cette procédure, vous remplacez toutefois les valeurs qui se trouvent dans l'enregistrement par celles du modèle. Vous devez par conséquent rester vigilant lorsque vous appliquez un modèle à des enregistrements existants.

> [!WARNING]  
>  La fonction **Appliquer modèle** remplace les données existantes d'un enregistrement. Si cette fonction est utilisée pour le transfert des données de base, elle remplace les données importées lors de la création d'enregistrements.

La procédure suivante se base sur une nouvelle fiche article.  

1. Créez un client. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).
2. Dans la fenêtre **Fiche client**, sélectionnez l'action **Appliquer modèle**.  
3. Dans la fenêtre **Modèles client**, sélectionnez l'un des modèles, puis cliquez sur le bouton **OK**.  

Les valeurs par défaut du modèle client choisi sont insérées dans la fiche client.

## <a name="see-also"></a>Voir aussi  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)

