---
title: Connecter vos données avec Flow| Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305058"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé
Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.

> [!NOTE]
> En plus de Microsoft Flow, vous pouvez utiliser la fonctionnalité de flux de travail dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Remarquez que bien qu'il s'agisse de deux systèmes de flux de travail distincts, tous les modèles Flow que vous créez dans Microsoft Flow sont ajoutés à la liste des modèles de flux de travail dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow
1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Il existe 3 façons de créer un flux : **Commencer à partir du modèle**, **Commencer à partir de rien**, et **Commencer à partir d'un connecteur**. Un modèle est un flux prédéfini créé pour vous. Pour utiliser un modèle, il suffit de le sélectionner et de créer une connexion pour chaque service qu'il utilise. Avec les options **Commencer à partir de rien** et **Commencer à partir d'un connecteur**, vous pouvez créer un flux à partir de zéro.
4. Pour créer à partir de rien, sur la page **Mes flux**, cliquez sur les options **Commencer à partir de rien** et **Flux automatisé**.
5. Recherchez un connecteur **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Définissez un nom et choisissez le déclencheur que vous souhaitez utiliser pour votre flux.
7. Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles :  
    
    *Lorsque l'approbation d'un fournisseur est exigée*,    
    *Lorsque l'approbation d'une ligne feuille comptabilité est exigée*,    
    *Lors de la suppression d'un enregistrement*,    
    *Lors de la modification d'un enregistrement*,    
    *Lorsqu'un enregistrement est créé*,    
    *Lorsqu'un enregistrement est modifié*,    
    *Lorsque l'approbation d'un nom feuille comptabilité est exigée*,   
    *Lorsque l'approbation d'un client est exigée*,   
    *Lorsque l'approbation d'un article est exigée*,    
    *Lorsque l'approbation d'un document achat est exigée* ou     
     *Lorsque l'approbation d'un document vente est exigée*.
     
8. Flow vous invite à sélectionner un environnement et une société dans votre abonné [!INCLUDE[d365fin](includes/d365fin_md.md)], ainsi que les conditions que vous souhaitez surveiller dans vos données.

> [!NOTE]  
>   Le connecteur [!INCLUDE[d365fin](includes/d365fin_md.md)] pour Microsoft Flow prend en charge plusieurs environnements de production et sandbox. Si vous n'avez pas créé plusieurs environnements de production ou sandbox, **Production** est la seule option que vous pouvez choisir. 

À ce stade, vous êtes connecté à vos données Business Central et vous êtes prêt à générer votre flux.

9. Pour créer à partir d'un modèle, choisissez l'option **Commencer à partir du modèle**.
10. Recherchez des modèles **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
11. Sélectionnez l'un des modèles dans la liste des modèles disponibles, puis choisissez **Créer**.  

    *Demander l'approbation pour les commandes vente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les devis vente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les factures vente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les avoirs vente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les clients Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les commandes achat Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les factures achat Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les avoirs achat Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les articles Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les fournisseurs Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les noms feuille comptabilité Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]* ou    
    *Demander l'approbation pour les lignes feuille comptabilité Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*.  
12. Flow affiche la liste des services utilisés dans le modèle Flow et tente de se connecter automatiquement à ces services. Si vous ne vous êtes pas déjà connecté à un service, vous serez invité à vous connecter à chacun des services auxquels vous devez vous connecter. Une coche verte apparaît à côté de chaque service une fois la connexion établie. Sélectionnez **Continuer**.
13. Flow vous invite à sélectionner un environnement et une société dans le cadre de votre abonnement à [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Comme chaque étape du flux est indépendante de la suivante, vous devrez peut-être définir plusieurs fois l'environnement et la société lorsque vous utilisez un modèle [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow.

Pour plus d'informations, voir [Documentation Flow](/flow/getting-started).

## <a name="see-also"></a>Voir aussi
[Mise en route](product-get-started.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)   
[Gérer les flux de travail [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Paramètres utilisateur approbation](across-how-to-set-up-approval-users.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
