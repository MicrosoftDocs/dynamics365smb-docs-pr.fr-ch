---
title: Configurer l’affectation des ressources | Microsoft Docs
description: Découvrez comment le système peut vous aider à affecter une personne dotée des compétences requises à la fourniture d’un service.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-resource-allocation" />Configurer l’affectation des ressources
Pour assurer la bonne exécution d’une tâche service, il est important de trouver une ressource qualifiée. Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] de manière à affecter facilement une ressource disposant des compétences appropriées pour le travail. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ce processus est appelé _affectation de ressources_. Vous pouvez affecter des ressources en fonction de leur compétence, de leur disponibilité, ou selon qu’elles se trouvent dans la même zone service que le client. 

Pour utiliser l’affectation des ressources, vous devez définir :  
  
* Les compétences nécessaires à la réparation et la maintenance des articles de service. Vous les affectez aux articles de service et aux ressources.  
* Les régions géographiques, appelées zones, que vous définissez pour votre marché. Par exemple, est, ouest, centre, etc. Vous les affectez aux clients et aux ressources.  
* Si les compétences ressource et les zones doivent être affichées, et si un avertissement doit être affiché si une ressource non qualifiée ou une ressource qui ne figure pas dans la zone du client est sélectionnée.  

## <a name="to-set-up-skills" />Pour configurer des compétences
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Compétences**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources" />Pour affecter des compétences aux articles de service et aux ressources
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles service** ou **Ressources**, puis choisissez le lien associé.  
2. Ouvrez la fiche de l’article de service ou de la ressource, puis sélectionnez l’une des options suivantes :  
  
    * Pour les articles de service, sélectionnez **Compétences ressource**.  
    * Pour les ressources, sélectionnez **Compétences**.  

## <a name="to-set-up-zones" />Pour configurer des zones
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Zones**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources" />Pour affecter des zones aux clients et aux ressources
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients** ou **Ressources**, puis choisissez le lien associé.  
2. Ouvrez la fiche de l’article de service ou de la ressource, puis sélectionnez l’une des options suivantes :  
  
    * Pour les clients, sélectionnez une zone dans le champ **Code zone service**.  
    * Pour les ressources, sélectionnez l’action **Zones service**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen" />Pour spécifier les éléments à afficher lorsqu’une ressource est sélectionnée
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres Gestion des services**, puis choisissez le lien associé. 
2. Dans le champ **Compétences ressources**, sélectionnez l’une des options décrites dans le tableau suivant.  
  
    |**Options**|**Description**|  
    |------------|-------------|  
    |Afficher code seulement | Affiche le code uniquement.|  
    |Utiliser alertes et afficher | Affiche les informations et un avertissement si vous choisissez une ressource qui n’est pas qualifiée.|  
    |Aucun affichage | N’affiche pas ces informations.|  

## <a name="to-update-resource-capacity" />Pour mettre à jour la capacité ressource
Vous devrez peut-être modifier la capacité des ressources.  
  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Capacité ressource**, puis choisissez le lien associé.  
2. Sélectionnez la ressource, puis l’action **Paramétrage capacité ressource**.  
3. Apportez les modifications, puis sélectionnez **Mettre à jour la capacité**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups" />Pour mettre à jour les compétences pour des articles, des articles de service ou des groupes d’articles de service
Vous pouvez modifier les codes compétence affectés à des articles, par exemple de **PC** à **PCS**, pour un article, un article de service ou pour tous les articles d’un groupe articles de service.  
  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, **Article de service** ou **Groupes d’articles de service**, puis sélectionnez le lien associé.  
2. Sélectionnez l’entité à mettre à jour, puis sélectionnez l’action **Compétences ressource**.  
3. Sur la ligne contenant le code à modifier, dans le champ **Code compétence**, sélectionnez le code compétence.  
4.  Si des articles de service sont associés à l’article, une boîte de dialogue incluant les deux options suivantes s’ouvre :  
  
    * Attribue la valeur sélectionnée aux codes compétence : sélectionnez cette option pour remplacer l’ancien code compétence de tous les articles de service associés par le nouveau code.  
    * Supprime les codes compétence ou met à jour leur relation : sélectionnez cette option pour modifier le code compétence de l’article uniquement. Le code compétence des articles de service associés sera réaffecté, c’est-à-dire que le champ **Affecté à partir de** sera mis à jour.  
  
## <a name="see-also" />Voir aussi
[Affecter des ressources](service-how-to-allocate-resources.md)  
[Configurer des heures de travail et des heures de service](service-how-setup-work-service-hours.md)  
[Configurer le reporting panne](service-how-setup-fault-reporting.md)  
[Configurer des codes prestations standards](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]
