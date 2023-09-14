---
title: Exposer des objets en tant que services web
description: "Publiez des objets en tant que services Web afin de les rendre immédiatement disponibles pour votre solution Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: bholtorf
---
# Publier un service Web

Les services web sont un moyen pratique de rendre une fonctionnalité d’application disponible à différents types de systèmes et utilisateurs externes. Par défaut, [!INCLUDE[prod_short](includes/prod_short.md)] expose un certain nombre d’objets en tant que services web pour une meilleure intégration avec d’autres services Microsoft. Vous pouvez ajouter d’autres services web selon les besoins de votre entreprise.  

Configurer un service web dans [!INCLUDE[prod_short](includes/prod_short.md)], puis publiez le service web afin qu’il soit disponible pour les utilisateurs authentifiés. Tous les utilisateurs autorisés peuvent accéder aux métadonnées des services Web, mais seuls les utilisateurs ayant les autorisations nécessaires peuvent accéder aux données réelles.  

## Création et publication d’un service Web

Les étapes suivantes expliquent la procédure de création et de publication d’un service Web.  

### Création et publication d’un service Web  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services Web**, puis choisissez le lien associé.  
2. Sur la page **Services Web**, sélectionnez **Nouveau**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Les types valides pour les services Web SOAP sont **Codeunit** et **Page**. Les types valides pour les services Web OData sont **Page** et **Requête**. À partir de la version 16.3, **Codeunit** est également un type valide pour les services web OData v4, mais aucune URL n’est affichée dans l’interface utilisateur. De même, si la base de données contient plusieurs sociétés, vous pouvez choisir un ID objet qui est spécifique à l’une des sociétés.  
    > Enfin, le nom de service est visible par les clients de votre service Web et sert de base pour identifier et distinguer les services Web, il doit donc être explicite.

3. Activez la case à cocher dans la colonne **Publié**.  

Lorsque vous publiez le service web, les champs **URL OData** et **URL SOAP** affichent les nouvelles URL. Cependant, pour les codeunits exposés en tant qu’actions indépendantes OData v4, les champs URL ne sont pas affichés.  

Vous pouvez tester le service Web immédiatement en choisissant les liens figurant dans les champs **URL OData** et **URL SOAP**. Éventuellement, copiez la valeur du champ et pour l’enregistrer pour une utilisation ultérieure. Pour tester les codeunits exposés en tant qu’actions indépendantes OData v4, suivez les instructions de la section [Vérification de la disponibilité du service web](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) dans le contenu du développeur.

> [!NOTE]
> Si les objets que vous exposez en tant que services Web ne doivent pas être accessibles depuis [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous devez marquer les méthodes exposées dans le code comme `[Scope('OnPrem')]`. Pour plus d’informations, voir [Attribut de portée](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Une fois le service Web publié, il est accessible aux parties externes. Vous pouvez vérifier la disponibilité de ce service web à l’aide d’un navigateur, ou vous pouvez sélectionner le lien dans les champs **URL OData** et **URL SOAP** de la page **Services web**. La procédure suivante indique comment vous pouvez vérifier la disponibilité du service Web pour une utilisation ultérieure.  

### Vérification de la disponibilité d’un service Web  

1. Dans votre navigateur, indiquez l’URL appropriée. Le tableau suivant illustre les types d’URL que vous pouvez entrer pour les différents types de services Web.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaxe|Exemple :|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Le nom de la société respecte la casse.|

2. Examinez les informations affichées dans le navigateur. Vérifiez que vous pouvez visualiser le nom du service Web que vous avez créé.  

Lorsque vous accédez à un service Web, et que vous souhaitez copier des données vers [!INCLUDE[prod_short](includes/prod_short.md)], vous devez spécifier le nom de la société. Vous pouvez spécifier la société en tant que membre de l’URI comme l’indiquent les exemples, sinon, vous pouvez spécifier la société comme partie des paramètres de requête. Par exemple, les URI suivants pointent vers le même service Web OData et qu’ils sont tous deux des URI valides.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## Voir aussi

[Administration](admin-setup-and-administration.md)  
[Services Web Business Central pour les développeurs](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Limites de demande OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]