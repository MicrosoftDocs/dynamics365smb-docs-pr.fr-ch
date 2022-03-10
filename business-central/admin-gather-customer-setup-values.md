---
title: Collecter les valeurs de configuration client
description: Le questionnaire de configuration permet de réduire la mise en œuvre en rationalisant la création de nouvelles entreprises et en proposant aux clients un fichier Excel ou XML.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: d26fb334462ad52a14058e8d5f6b9f86088ad3d7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145985"
---
# <a name="gather-customer-setup-values"></a>Collecter les valeurs de configuration client
Vous pouvez utiliser le questionnaire de configuration pour réduire la charge de travail d’implémentation en rationalisant la tâche de configuration de la nouvelle société. Vous pouvez générer le questionnaire de configuration dans [!INCLUDE[prod_short](includes/prod_short.md)], puis le fournir à votre client sous forme de fichier Excel ou XML.  

Vous pouvez modifier toutes les valeurs par défaut d’un questionnaire afin qu’elles correspondent plus étroitement aux besoins du client.  

> [!TIP]  
>  Pour plus d’informations sur la définition des valeurs de paramétrage dans les champs de planification de l’approvisionnement, reportez\-vous à [Configurer des recommandations : planification de l’approvisionnement](setup-best-practices-supply-planning.md).  

Lorsque le client remplit le questionnaire, vous importez le fichier dans la nouvelle société [!INCLUDE[prod_short](includes/prod_short.md)] du client. Votre client et vous-même devez valider les réponses au questionnaire avant de les appliquer à la société.

## <a name="to-create-a-configuration-questionnaire"></a>Pour créer un questionnaire de configuration
Vous pouvez utiliser un questionnaire pour vous aider à déterminer la portée et les besoins de la configuration. Vous pouvez créer un questionnaire ou modifier un questionnaire existant en y ajoutant de nouvelles questions ou zones de questions.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company information. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Vous pouvez créer des questionnaires uniquement pour les tables de type paramétrage. Par exemple, vous pouvez utiliser cet outil pour entrer des informations dans les pages suivantes :  

-   Informations société  
-   Paramètres immobilisations  
-   Paramètres comptabilité  
-   Paramètres stock  
-   Paramètres d’assemblage
-   Paramètres production  
-   Paramètres achats  
-   Paramètres marketing  
-   Paramètres services  
-   Paramètres ventes  
-   Paramètres entrepôt  

> [!NOTE]  
>  Pour voir une liste complète des tables de configuration, choisissez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configurer**, puis choisissez le lien associé. Pour déterminer la portée de la migration des données d’enregistrements, utilisez la fonctionnalité de migration. Pour plus d’informations, voir [Migration des données client](admin-migrate-customer-data.md).  

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Questionnaire de configuration**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.   
3. Sur la page **Questionnaire configuration**, dans le champ **Code**, saisissez... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[prod_short](includes/prod_short.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Sélectionnez l’action **Zones question**. La page **Zones question** s’ouvre.  
4. Sélectionnez l’action **Nouveau**. La page **Zones question config.** s’ouvre.  
5. Dans le champ **ID table**, sélectionnez l’ID de la table pour laquelle vous souhaitez collecter des informations. Le champ **Nom table** est automatiquement renseigné.  
6. Sélectionnez l’action **Mettre à jour questions**. Chaque champ de la table est ajouté au questionnaire avec un point d’interrogation à la suite de son étiquette.

Vous pouvez reformuler l’étiquette de manière à indiquer clairement comment répondre à la question. Par exemple, vous pouvez modifier un champ intitulé « Nom » en « Quel est le nom de \<data being collected\> ». Vous pouvez également fournir des instructions dans le champ **Référence**, notamment une URL vers une page qui fournit des informations supplémentaires.  

Vous pouvez également supprimer les questions que vous souhaitez exclure du questionnaire.  

> [!NOTE]  
>  Le champ **Option de réponse** décrit le type et le format de la réponse en fonction des données. Le champ **Réponse** contient les informations entrées par l’utilisateur.  
>   
>  Si nécessaire, vous pouvez également définir des réponses par défaut dans le champ **Réponse**. Ces valeurs sont utilisées par défaut pour la configuration personnalisée. La personne qui remplit le questionnaire peut toutefois modifier et mettre à jour la réponse.  

## <a name="to-complete-the-configuration-questionnaire"></a>Pour remplir le questionnaire de configuration
Utilisez le questionnaire de configuration pour structurer et documenter une discussion détaillée sur les besoins spécifiques du client. Vous l’utilisez également pour recueillir les données de configuration du client afin de paramétrer les tables de configuration [!INCLUDE[prod_short](includes/prod_short.md)] appropriées, telles que les écritures comptables, le stock et les clients.  

> [!NOTE]  
>  Vous pouvez également créer votre propre de questionnaire de configuration afin qu’il corresponde à vos besoins.  

1. Ouvrez la société pour laquelle vous souhaitez remplir le questionnaire.
2. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Questionnaire de configuration**, puis sélectionnez le lien associé.  
3. Sélectionnez le questionnaire pour la société, puis choisissez l’action **Exporter vers Excel**, ou éventuellement l’action **Exporter vers un fichier XML**.
4. Demandez au client de remplir le questionnaire de configuration en saisissant les réponses dans le classeur Excel. Il existe des feuilles pour chacune des zones question qui ont été créées pour le questionnaire.   
5. Enregistrez le classeur Excel sous *Données XML*. Sélectionnez l’action **Importer d’un fichier XML**, puis sélectionnez le fichier .xms avec les réponses du client.
6. Sélectionnez l’action **Zones question** pour démarrer le processus de validation et d’application des réponses au questionnaire de configuration.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Pour remplir un questionnaire à partir de la feuille configuration  
La procédure suivante fournit un autre moyen d’accéder aux questionnaires de configuration. Elle est basée sur l’hypothèse que le package configuration qui a été envoyé inclut des questionnaires.  

1. Après avoir importé un package configuration, ouvrez la feuille configuration.  
2. Pour chaque table pour laquelle il existe une zone de question, sélectionnez l’action **Questions**. La page de questionnaire s’ouvre.  
3. Répondez aux questions, puis sélectionnez l’action **Appliquer réponses**.  
4. Cliquez sur le bouton **OK** pour fermer le questionnaire.

## <a name="to-validate-the-configuration-questionnaire"></a>Pour valider le questionnaire de configuration
Il est important de valider le questionnaire de configuration avant de l’appliquer au format [!INCLUDE[prod_short](includes/prod_short.md)]. C’est aussi un moyen de s’assurer que le formatage de données est conservé lors de l’importation à partir d’Excel.  

Une tâche de validation courante consiste à vérifier qu’aucune chaîne de caractères n’a été entrée dans les champs de date. Ce processus de révision est nécessaire, car le format des réponses du questionnaire n’est pas validé automatiquement lorsque vous exécutez la fonction **Appliquer réponses**.  

> [!NOTE]  
>  En général, la validation du questionnaire de configuration est un processus manuel. Toutefois, il existe également des vérifications pour les incohérences de formatage des paramètres régionaux. En outre, des erreurs seront détectées si la structure de la base de données [!INCLUDE[prod_short](includes/prod_short.md)] ne correspond pas à celle de la base de données de migration.  

1. Sur la page **Questionnaire configuration**, sélectionnez le questionnaire approprié, puis sélectionnez l’action **Zones question**.  
2. Ouvrez la zone de question appropriée.  
3. Pour chaque question, vérifiez que la valeur du champ **Réponse** correspond au format indiqué dans le champ **Option de réponse**. Par exemple, assurez-vous que l’adresse d’une société est au format texte.  
4. Si vous détectez des erreurs, vous pouvez les résoudre et apporter les corrections nécessaires dans Excel en exportant le questionnaire, puis en le réimportant. Vous pouvez également corriger les erreurs directement dans [!INCLUDE[prod_short](includes/prod_short.md)] tandis que vous passez en revue les réponses sur la page **Zone question config**.  
5. Répétez ces étapes pour chaque zone question.  

Une fois la validation terminée, les données peuvent être appliquées à la base de données.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Pour appliquer des réponses à partir du questionnaire de configuration
Après avoir importé et validé les informations à partir d’un questionnaire de configuration, vous pouvez transférer ou appliquer les données de configuration dans les tables correspondantes de la base de données [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 4.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Questionnaire de configuration**, puis sélectionnez le lien associé. La page **Questionnaire config.** s’ouvre.  
2. Sélectionnez un questionnaire de configuration dans la liste, puis sélectionnez l’action **Modifier la liste**.  
3. Vous pouvez appliquer les réponses de deux manières différentes.  

- Pour appliquer l’ensemble du questionnaire, sélectionnez **Appliquer réponses**.  
- Pour appliquer les réponses d’une **Zone question** spécifique, sélectionnez l’action **Zones question**, sélectionnez une **Zone question** dans la liste, puis sélectionnez l’action **Appliquer réponses**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Pour vérifier que les réponses ont été correctement appliquées

1. Vérifiez les pages de paramétrage des différents modules de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour localiser la page, choisissez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 5](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez le nom de la page de configuration, puis sélectionnez le lien associé.  
2. Vérifiez que les champs ont été renseignés à l’aide des données appropriées à partir des diverses zones de questions du questionnaire de configuration.  

Vous avez maintenant effectué le paramétrage à l’aide des informations commerciales et des règles du client.

## <a name="see-also"></a>Voir aussi  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]