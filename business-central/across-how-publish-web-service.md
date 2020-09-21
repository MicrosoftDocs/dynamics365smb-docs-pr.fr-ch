---
title: Exposer des objets en tant que services Web | Microsoft Docs
description: Publiez des objets en tant que services Web afin de les rendre immédiatement disponibles pour votre solution Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: 230f3a7fc11e19813d77da2ff15388433642c744
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697662"
---
# <a name="publish-a-web-service"></a>Publier un service Web

Les services Web sont un moyen pratique de rendre une fonctionnalité d'application disponible à différents systèmes et utilisateurs externes. [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs objets qui sont exposés par défaut en tant que services Web en raison de l'intégration à d'autres services Microsoft, mais vous pouvez également ajouter d'autres services Web.  

Vous devez configurer un service Web dans le client [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous devez ensuite publier le service Web pour le rendre disponible aux demandes de service sur le réseau. Les utilisateurs peuvent découvrir les services Web en pointant un navigateur sur l'emplacement du serveur et en demandant la liste des services disponibles. Lorsque vous publiez un service Web, il est immédiatement disponible sur le réseau pour les utilisateurs authentifiés. Tous les utilisateurs autorisés peuvent accéder aux métadonnées des services Web, mais seuls les utilisateurs ayant les autorisations nécessaires peuvent accéder aux données réelles.

## <a name="creating-and-publishing-a-web-service"></a>Création et publication d'un service Web

Les étapes suivantes expliquent la procédure de création et de publication d'un service Web.  

<!--
    You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead. Choose one of the following methods:

      - Use the **Create Data Set** action on the **Web Services** page
      - Use the **Set Up Reporting** Assisted Setup guide
      - Choose the **Edit in Excel** action in any lists
    -->

### <a name="to-create-and-publish-a-web-service"></a>Création et publication d'un service Web  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services Web**, puis sélectionnez le lien associé.  
2. Sur la page **Services Web**, sélectionnez **Nouveau**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Les types valides pour les services Web SOAP sont **Codeunit** et **Page**. Les types valides pour les services Web OData sont **Page** et **Requête**.  
    > De même, si la base de données contient plusieurs sociétés, vous pouvez choisir un ID objet qui est spécifique à l'une des sociétés.  
    > Enfin, le nom de service est visible par les clients de votre service Web et sert de base pour identifier et distinguer les services Web, il doit donc être explicite.

3. Activez la case à cocher dans la colonne **Publié**.  

Lorsque vous publiez le service Web, dans les champs **URL OData** et **URL SOAP**, vous pouvez voir les URL générées pour le service Web. Vous pouvez tester le service Web immédiatement en choisissant les liens figurant dans les champs **URL OData** et **URL SOAP**. Éventuellement, vous pouvez copier la valeur du champ et pour l'enregistrer pour une utilisation ultérieure.  

> [!NOTE]
> Si les objets que vous exposez en tant que services Web ne doivent pas être accessibles depuis [!INCLUDE[prodshort](includes/prodshort.md)] en ligne, vous devez marquer les méthodes exposées dans le code comme `[Scope('OnPrem')]`. Pour plus d'informations, voir [Attribut de portée](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Une fois le service Web publié, il est accessible aux parties externes. Vous pouvez vérifier la disponibilité de ce service Web à l'aide d'un navigateur, ou vous pouvez sélectionner le lien dans les champs **URL OData** et **URL SOAP** de la page **Services Web**. La procédure suivante indique comment vous pouvez vérifier la disponibilité du service Web pour une utilisation ultérieure.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Vérification de la disponibilité d'un service Web  

1. Dans votre navigateur, indiquez l'URL appropriée. Le tableau suivant illustre les types d'URL que vous pouvez entrer pour les différents types de services Web.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaxe|Exemple :|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Le nom de la société respecte la casse.|

2. Examinez les informations affichées dans le navigateur. Vérifiez que vous pouvez visualiser le nom du service Web que vous avez créé.  

Lorsque vous accédez à un service Web, et que vous souhaitez copier des données vers [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez spécifier le nom de la société. Vous pouvez spécifier la société en tant que membre de l'URI comme l'indiquent les exemples, ou vous pouvez spécifier la société comme partie des paramètres de requête. Par exemple, les URI suivants pointent vers le même service Web OData et qu'ils sont tous deux des URI valides.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Voir aussi

[Administration](admin-setup-and-administration.md)  
[Services Web Business Central pour les développeurs](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Limites de demande OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
