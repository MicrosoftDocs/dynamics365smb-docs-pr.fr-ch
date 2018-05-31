---
title: "Connecter vos données avec Flow| Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de données sources et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé
Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow
1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Il existe 2 façons de créer un flux ; **Créer à partir d'un modèle** et **Créer à partir de rien**. Un modèle est un flux prédéfini créé pour vous.  Pour utiliser un modèle, il suffit de le sélectionner et de créer une connexion pour chaque service qu'il utilise. Un modèle vide vous permet de créer un flux complètement nouveau. 
4. Pour créer à partir de rien, dans la fenêtre **Mes flux**, cliquez sur l'option **Créer à partir de rien**.
5. Recherchez un connecteur **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles :  
    *Lorsque l'approbation d'un client est exigée*,  
    *Lorsque l'approbation d'un nom feuille comptabilité est exigée*,  
    *Lorsque l'approbation d'une ligne feuille comptabilité est exigée*,  
    *Lorsque l'approbation d'un article est exigée*,  
    *Lorsque l'approbation d'un document achat est exigée*,  
    *Lorsque l'approbation d'un document vente est exigée*, ou  
    *Quand l'approbation d'un fournisseur est-elle exigée* ?
7. Flow vous invite à sélectionner une société dans votre abonné [!INCLUDE[d365fin](includes/d365fin_md.md)], ainsi que les conditions que vous souhaitez surveiller dans vos données. 

À ce stade, vous êtes connecté à vos données Business Central et vous êtes prêt à générer votre flux. 

8. Pour créer à partir d'un modèle, choisissez l'option **Créer à partir d'un modèle**.
9. Recherchez des modèles **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**. 
10. Sélectionnez l'un des modèles dans la liste des modèles disponibles :  
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
    *Demander l'approbation pour les noms feuille comptabilité Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Demander l'approbation pour les lignes feuille comptabilité Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*.  
11. Flow vous invite à sélectionner une société dans votre abonné [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Comme chaque étape de Flow est indépendante de la suivante, vous devrez peut-être définir plusieurs fois la société lorsque vous utilisez un modèle [!INCLUDE[d365fin_md](includes/d365fin_md.md)].
12. Le modèle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] s'intègre avec le moteur de flux de travail principal dans Microsoft[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Cela signifie, que chaque fois que vous utilisez l'un de ces modèles pour créer un flux, un flux correspondant est créé au sein de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Reportez-vous à la documentation sur le flux de travail pour Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Pour plus d'informations, voir [Documentation Flow](https://docs.microsoft.com/en-us/flow/getting-started).

Pour résoudre les problèmes avec Microsoft Flow, voir [Résolution des problèmes : Intégration à Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Voir aussi
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)   
[Gérer les flux de travail [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Paramètres utilisateur approbation](across-how-to-set-up-approval-users.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
