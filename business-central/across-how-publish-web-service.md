---
title: Exposer des objets en tant que services Web | Microsoft Docs
description: "Publiez des objets en tant que services Web pour les rendre immédiatement disponibles sur le réseau."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: d22de15b3e91897a209a31d03a63fb7d927d2f96
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="publish-a-web-service"></a>Publier un service Web
Les services Web sont un moyen pratique de rendre une fonctionnalité d'application disponible à différents systèmes et utilisateurs externes. [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs objets qui sont exposés par défaut en tant que services Web en raison de l'intégration à d'autres services Microsoft, mais vous pouvez également ajouter d'autres services Web.  

Vous pouvez configurer un service Web dans le client Windows ou le client Web. Vous devez ensuite publier le service Web pour le rendre disponible aux demandes de service sur le réseau. Les utilisateurs peuvent découvrir les services Web en pointant un navigateur sur l'emplacement du serveur et en demandant la liste des services disponibles. Lorsque vous publiez un service Web, il est immédiatement disponible sur le réseau pour les utilisateurs authentifiés. Tous les utilisateurs autorisés peuvent accéder aux métadonnées des services Web, mais seuls les utilisateurs ayant les autorisations nécessaires peuvent accéder aux données réelles.

## <a name="creating-and-publishing-a-web-service"></a>Création et publication d'un service Web  
Les étapes suivantes expliquent la procédure de création et de publication d'un service Web.  

### <a name="to-create-and-publish-a-web-service"></a>Création et publication d'un service Web  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Services Web**, puis sélectionnez le lien connexe.  
2.  Dans la page **Services Web**, sélectionnez **Nouveau**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  Les types valides pour les services Web SOAP sont **Codeunit** et **Page**. Les types valides pour les services Web OData sont **Page** et **Requête**.  
    De même, si la base de données contient plusieurs sociétés, vous pouvez choisir un ID objet qui est spécifique à l'une des sociétés.  
    Enfin, le nom de service est visible par les clients de votre service Web et sert de base pour identifier et distinguer les services Web, il doit donc être explicite.

3.  Activez la case à cocher dans la colonne **Publié**.  

Lorsque vous publiez le service Web, dans les champs **URL OData** et **URL SOAP**, vous pouvez voir les URL générées pour le service Web. Vous pouvez tester le service Web immédiatement en choisissant les liens figurant dans les champs **URL OData** et **URL SOAP**. Éventuellement, vous pouvez copier la valeur du champ et pour l'enregistrer pour une utilisation ultérieure.  

Une fois le service Web publié, il est accessible aux parties externes. Vous pouvez vérifier la disponibilité de ce service Web à l'aide d'un navigateur, ou vous pouvez sélectionner le lien dans les champs **URL OData** et **URL SOAP** de la fenêtre **Services Web**. La procédure suivante indique comment vous pouvez vérifier la disponibilité du service Web pour une utilisation ultérieure.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Vérification de la disponibilité d'un service Web  

1.  Dans votre navigateur, indiquez l'URL appropriée. Le tableau suivant illustre les types d'URL que vous pouvez entrer pour les différents types de services Web.  
> [!div class="mx-tdBreakAll"]
> |Type|Syntaxe|Exemple :|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Le nom de la société respecte la casse.|

2.  Examinez les informations affichées dans le navigateur. Vérifiez que vous pouvez visualiser le nom du service Web que vous avez créé.  

Lorsque vous accédez à un service Web, et que vous souhaitez copier des données vers [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez spécifier le nom de la société. Vous pouvez spécifier la société en tant que membre de l'URI comme l'indiquent les exemples, ou vous pouvez spécifier la société comme partie des paramètres de requête. Par exemple, les URI suivants pointent vers le même service Web OData et qu'ils sont tous deux des URI valides.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Voir aussi  
[Administration](admin-setup-and-administration.md)  

