---
title: Connecter vos données avec Power Automate| Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f44b727a353208d1b2b8f5d918400de1687acc52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754557"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] dans un flux automatisé

Vous pouvez utiliser vos données [!INCLUDE[prod_short](includes/prod_short.md)] dans le cadre d’un flux de travail dans Microsoft Power Automate.

> [!NOTE]
> En plus de Power Automate, vous pouvez utiliser la fonctionnalité de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Remarquez que bien qu’il s’agisse de deux systèmes de flux de travail distincts, tous les modèles de flux de travail que vous créez dans Power Automate sont ajoutés à la liste des modèles de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> Vous devez disposer d’un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et avec Power Automate.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>Pour ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power Automate

1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Il existe 3 façons de créer un flux : **Commencer à partir du modèle**, **Commencer à partir de rien**, et **Commencer à partir d’un connecteur**. Un modèle est un flux prédéfini créé pour vous. Pour utiliser un modèle, il suffit de le sélectionner et de créer une connexion pour chaque service qu’il utilise. Avec les options **Commencer à partir de rien** et **Commencer à partir d’un connecteur**, vous pouvez créer un flux à partir de zéro.
4. Pour créer à partir de rien, sur la page **Mes flux**, cliquez sur les options **Commencer à partir de rien** et **Flux automatisé**.
5. Recherchez un connecteur **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Définissez un nom et choisissez le déclencheur que vous souhaitez utiliser pour votre flux.
7. Dans la liste des déclencheurs disponibles, sélectionnez l’un des déclencheurs [!INCLUDE[prod_short](includes/prod_short.md)] disponibles :  

    *Lorsque l’approbation d’un fournisseur est exigée*,  
    *Lorsque l’approbation d’une ligne feuille comptabilité est exigée*,  
    *Lors de la suppression d’un enregistrement*,  
    *Lors de la modification d’un enregistrement*,  
    *Lorsqu’un enregistrement est créé*,  
    *Lorsqu’un enregistrement est modifié*,  
    *Lorsque l’approbation d’un nom feuille comptabilité est exigée*,  
    *Lorsque l’approbation d’un client est exigée*,  
    *Lorsque l’approbation d’un article est exigée*,  
    *Lorsque l’approbation d’un document achat est exigée* ou  
    *Lorsque l’approbation d’un document vente est exigée*.

8. Power Automate vous invite à sélectionner un environnement et une société dans votre abonné [!INCLUDE[prod_short](includes/prod_short.md)], ainsi que les conditions que vous souhaitez surveiller dans vos données.

    > [!NOTE]
    > Le connecteur [!INCLUDE[prod_short](includes/prod_short.md)] pour Power Automate prend en charge plusieurs environnements de production et sandbox. Si vous n’avez pas créé plusieurs environnements de production ou sandbox, **Production** est la seule option que vous pouvez choisir.  

    À ce stade, vous êtes connecté à vos données Business Central[!INCLUDE[prod_short](includes/prod_short.md)] et vous êtes prêt à générer votre flux.

9. Pour créer à partir d’un modèle, choisissez l’option **Commencer à partir du modèle**.
10. Recherchez des modèles **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. Sélectionnez l’un des modèles dans la liste des modèles disponibles, puis choisissez **Créer**.  

    *Demander l’approbation pour les commandes vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les devis vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les factures vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les avoirs vente Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les clients Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les commandes achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les factures achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les avoirs achat Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les articles Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les fournisseurs Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Demander l’approbation pour les noms feuille comptabilité Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]* ou    
    *Demander l’approbation pour les lignes feuille comptabilité Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*.  
12. Power Automate affiche la liste des services utilisés dans le modèle de flux et tente de se connecter automatiquement à ces services. Si vous ne vous êtes pas déjà connecté à un service, vous serez invité à vous connecter à chacun des services auxquels vous devez vous connecter. Une coche verte apparaît à côté de chaque service une fois la connexion établie. Sélectionnez **Continuer**.
13. Power Automate vous invite à sélectionner un environnement et une société dans le cadre de votre abonnement [!INCLUDE[prod_short](includes/prod_short.md)]. Comme chaque étape du flux est indépendante de la suivante, vous devrez peut-être définir plusieurs fois l’environnement et la société lorsque vous utilisez un modèle [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate.

Pour plus d’informations, voir la [documentation Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Voir aussi

[Mise en route](product-get-started.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les flux de travail [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Paramètres utilisateur approbation](across-how-to-set-up-approval-users.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  
