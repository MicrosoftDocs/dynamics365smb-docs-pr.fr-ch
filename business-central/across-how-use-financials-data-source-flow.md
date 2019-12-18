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
ms.date: 11/20/2019
ms.author: bmeier
ms.openlocfilehash: 24ca66c2d533f4a3e30eb1ebaca817915b95c370
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832037"
---
# <a name="using-includeprodshortincludesprodshortmd-in-an-automated-workflow"></a>Utilisation de [!INCLUDE[prodshort](includes/prodshort.md)] dans un flux automatisé

Vous pouvez utiliser vos données [!INCLUDE[prodshort](includes/prodshort.md)] dans le cadre d'un flux de travail dans Microsoft Power Automate.

> [!NOTE]
> En plus de Power Automate, vous pouvez utiliser la fonctionnalité de flux de travail dans [!INCLUDE[prodshort](includes/prodshort.md)]. Remarquez que bien qu'il s'agisse de deux systèmes de flux de travail distincts, tous les modèles de flux de travail que vous créez dans Power Automate sont ajoutés à la liste des modèles de flux de travail dans [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power Automate.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-automate"></a>Pour ajouter [!INCLUDE[prodshort](includes/prodshort.md)] comme source de données dans Power Automate

1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Il existe 3 façons de créer un flux : **Commencer à partir du modèle**, **Commencer à partir de rien**, et **Commencer à partir d'un connecteur**. Un modèle est un flux prédéfini créé pour vous. Pour utiliser un modèle, il suffit de le sélectionner et de créer une connexion pour chaque service qu'il utilise. Avec les options **Commencer à partir de rien** et **Commencer à partir d'un connecteur**, vous pouvez créer un flux à partir de zéro.
4. Pour créer à partir de rien, sur la page **Mes flux**, cliquez sur les options **Commencer à partir de rien** et **Flux automatisé**.
5. Recherchez un connecteur **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**.
6. Définissez un nom et choisissez le déclencheur que vous souhaitez utiliser pour votre flux.
7. Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[prodshort](includes/prodshort.md)] disponibles :  

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

8. Power Automate vous invite à sélectionner un environnement et une société dans votre abonné [!INCLUDE[prodshort](includes/prodshort.md)], ainsi que les conditions que vous souhaitez surveiller dans vos données.

    > [!NOTE]
    > Le connecteur [!INCLUDE[prodshort](includes/prodshort.md)] pour Power Automate prend en charge plusieurs environnements de production et sandbox. Si vous n'avez pas créé plusieurs environnements de production ou sandbox, **Production** est la seule option que vous pouvez choisir.  

    À ce stade, vous êtes connecté à vos données Business Central[!INCLUDE [prodshort](includes/prodshort.md)] et vous êtes prêt à générer votre flux.

9. Pour créer à partir d'un modèle, choisissez l'option **Commencer à partir du modèle**.
10. Recherchez des modèles **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**.
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
12. Power Automate affiche la liste des services utilisés dans le modèle de flux et tente de se connecter automatiquement à ces services. Si vous ne vous êtes pas déjà connecté à un service, vous serez invité à vous connecter à chacun des services auxquels vous devez vous connecter. Une coche verte apparaît à côté de chaque service une fois la connexion établie. Sélectionnez **Continuer**.
13. Power Automate vous invite à sélectionner un environnement et une société dans le cadre de votre abonnement [!INCLUDE[prodshort](includes/prodshort.md)]. Comme chaque étape du flux est indépendante de la suivante, vous devrez peut-être définir plusieurs fois l'environnement et la société lorsque vous utilisez un modèle [!INCLUDE[prodshort](includes/prodshort.md)] Power Automate.

Pour plus d'informations, voir la [documentation Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Voir aussi

[Mise en route](product-get-started.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les flux de travail [!INCLUDE[prodlong](includes/prodlong.md)]](across-use-workflows.md)  
[Paramètres utilisateur approbation](across-how-to-set-up-approval-users.md)  
[Configuration de [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Finances](finance.md)  
