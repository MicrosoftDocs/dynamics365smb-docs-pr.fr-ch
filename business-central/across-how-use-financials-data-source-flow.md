---
title: Connecter vos données avec Power Automate| Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 62718df1c80cb419501b72bcbdb6d7a6f9f18402
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518482"
---
# <a name="use-prod_short-in-an-automated-workflow"></a>Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans un flux automatisé

Vous pouvez utiliser vos données [!INCLUDE[prod_short](includes/prod_short.md)] en tant que partie du flux de travail dans Microsoft Power Automate.

> [!NOTE]
> En plus de Power Automate, vous pouvez utiliser la fonctionnalité de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Remarquez que bien qu’il s’agisse de deux systèmes de flux de travail distincts, tous les modèles de flux de travail que vous créez dans Power Automate sont ajoutés à la liste des modèles de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> Vous devez disposer d’un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et avec Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power Automate

1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Il existe 3 façons de créer un flux : **Commencer à partir du modèle**, **Commencer à partir de rien**, et **Commencer à partir d’un connecteur**. Un modèle est un flux prédéfini créé pour vous. Pour utiliser un modèle, sélectionnez-le et créez une connexion pour chaque service qu’il utilise. Avec les options **Commencer à partir de rien** et **Commencer à partir d’un connecteur**, vous pouvez créer un flux à partir de zéro.
4. Pour créer à partir de rien, sur la page **Mes flux**, cliquez sur les options **Commencer à partir de rien** et **Flux automatisé**.
5. Recherchez un connecteur **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Définissez un nom et choisissez le déclencheur que vous souhaitez utiliser pour votre flux.
7. Dans la liste des déclencheurs disponibles, sélectionnez l’un des déclencheurs [!INCLUDE[prod_short](includes/prod_short.md)] disponibles :  

    - *Lorsque l’approbation d’un fournisseur est exigée*  
    - *Lorsque l’approbation d’une ligne feuille comptabilité est exigée* 
    - *Lors de la suppression d’un enregistrement*
    - *Lors de la modification d’un enregistrement*
    - *Lorsqu’un enregistrement est créé*
    - *Lorsqu’un enregistrement est modifié*
    - *Lorsque l’approbation d’un nom feuille comptabilité est exigée* 
    - *Lorsque l’approbation d’un client est exigée*
    - *Lorsque l’approbation d’un article est exigée*
    - *Lorsque l’approbation d’un document achat est exigée*
    - *Lorsque l’approbation d’un document vente est exigée*

8. Power Automate vous invite à sélectionner un environnement et une société dans votre abonné [!INCLUDE[prod_short](includes/prod_short.md)], plus les conditions que vous souhaitez surveiller dans vos données.

    > [!NOTE]
    > Le connecteur [!INCLUDE[prod_short](includes/prod_short.md)] pour Power Automate prend en charge plusieurs environnements de production et sandbox. Si vous n’avez pas créé plusieurs environnements de production ou sandbox, **Production** est la seule option que vous pouvez choisir.  

    À ce stade, vous êtes connecté à vos données Business Central[!INCLUDE[prod_short](includes/prod_short.md)] et vous êtes prêt à générer votre flux.

9. Pour créer à partir d’un modèle, choisissez l’option **Commencer à partir du modèle**.
10. Recherchez des modèles **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. Sélectionnez l’un des modèles dans la liste des modèles disponibles, puis choisissez **Créer**.  

    - *Demander l’approbation pour les commandes vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les devis vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les factures vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les avoirs vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les clients Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les commandes achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les factures achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les avoirs achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Demander l’approbation pour les articles Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les fournisseurs Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Demander l’approbation pour les noms feuille comptabilité Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Demander l’approbation pour les lignes feuille comptabilité Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
12. Power Automate affiche la liste des services utilisés dans le modèle de flux et tente de se connecter automatiquement à ces services. Si vous ne vous êtes pas déjà connecté à un service, vous serez invité à vous connecter à chacun des services auxquels vous devez vous connecter. Une coche verte apparaît à côté de chaque service une fois la connexion établie. Sélectionnez **Continuer**.
13. Power Automate vous invite à sélectionner un environnement et une société dans le cadre de votre abonnement [!INCLUDE[prod_short](includes/prod_short.md)]. Comme chaque étape du flux est indépendante de la suivante, vous devrez peut-être définir plusieurs fois l’environnement et la société lorsque vous utilisez un modèle [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate.

Pour plus d’informations, voir la [documentation Power Automate](/power-automate/getting-started).

## <a name="troubleshooting"></a>Incident

### <a name="entity-set-not-found-error"></a>Erreur « Ensemble d’entités introuvable »

#### <a name="problem"></a>Problème

Lors de la création d’un nouveau flux Power Automate à l’aide d’un déclencheur d’approbation [!INCLUDE[prod_short](includes/prod_short.md)], comme *Lorsque l’approbation d’un document achat est exigée*, vous recevez un message d’erreur similaire à :

**Ensemble d’entités introuvable : \<name\>**

où **\<name\>** est le nom du service Web manquant, comme **workflowWebhookSubscriptions** ou **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Cause possible

L’utilisation de Power Automate pour l’intégration avec vos approbations [!INCLUDE[prod_short](includes/prod_short.md)] nécessite que certains objets de page et de codeunit soient publiés en tant que services Web. Par défaut, la plupart des objets requis sont publiés en tant que services Web pour vous. Mais dans certains cas, votre environnement a peut-être été personnalisé pour que ces objets ne soient plus publiés.

#### <a name="fix"></a>Corriger

Allez à la page **Services Web** et assurez-vous que les objets suivants sont publiés en tant que services Web. Il devrait y avoir une entrée dans la liste pour chaque objet, avec la case **Publié** cochée. 

|Type d’objet|ID d’objet|Nom de l’objet|Nom du service|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Page|  6408|   workflowCustomers|  workflowCustomers|
|Page   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Page   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Page   |6409   |workflowItems| workflowItems|
|Page   |6405   |Entité de ligne document achat|workflowPurchaseDocumentLines|
|Page|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Page|  6403    |Entité de ligne document vente |workflowSalesDocumentLines|
|Page|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Page|  6410    |workflowVendors|   workflowVendors|
|Page|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> La valeur **Nom du service** doit être exactement comme indiqué dans le tableau. Ne modifiez ni ne traduisez le nom du service.

Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

## <a name="see-also"></a>Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les flux de travail [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Paramètres utilisateur approbation](across-how-to-set-up-approval-users.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]