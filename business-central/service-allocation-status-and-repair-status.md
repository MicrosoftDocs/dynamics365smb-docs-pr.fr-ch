---
title: Statut affectation et statut réparation | Microsoft Docs
description: Découvrez la relation entre le statut réparation des articles de service et le statut affectation des écritures d’affectation associées.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocation-status-and-repair-status-of-service-items"></a><a name="allocation-status-and-repair-status-of-service-items"></a><a name="allocation-status-and-repair-status-of-service-items"></a>Statut affectation et statut réparation des articles de service
L’état réparation des articles de service et l’état affectation des écritures affectation des articles de service sont liés dans le module Gestion des services. L’état affectation change lorsque vous modifiez l’état réparation de l’article de service en **Terminé** ou **Service en partie réalisé**, et lorsque vous convertissez un devis service en commande service. L’état réparation de l’article de service change lorsque vous annulez l’affectation de l’article de service, ou que vous réaffectez l’article à une autre ressource. Vous pouvez visualiser l’état réparation des articles de service sur la page **Tâches service** et vous pouvez mettre à jour l’état réparation dans le champ **Code état réparation** de la page **Feuille activité article de service**. Vous pouvez visualiser l’état affectation dans le champ **Statut** de la page **Affectations ressources**.  
  
## <a name="changing-repair-status"></a><a name="changing-repair-status"></a><a name="changing-repair-status"></a>Modification de l’état réparation
Lorsque vous modifiez l’état réparation d’un article de service sur une ligne article de service, lune recherche est effectuée d’ une écriture affectation équivalente pour cet article de service, présentant le statut **Actif**. Si une écriture de ce type est détectée, le statut est mis à jour de l’une des manières suivantes :  
  
* Si vous modifiez l’état réparation en **Terminé**, l’état affectation est modifié de **Active** en **Terminée**.  
* Si vous modifiez l’état réparation en **Service en partie réalisé**, càd une partie du service a été effectuée, ou en **Expertisé**, càd aucun service n’a été effectué, l’état affectation est transformé de **Active** en **Réaffectation nécessaire**.  
* Lors de la création d’une écriture affectation commande service, qui indique qu’aucune ressource n’a été affectée, le champ **Statut** sur la page **Affectation ressources** passe sur **Non actif**.  
* Le statut de l’écriture affectation est défini sur **Annulé** lorsque vous réaffectez l’article de service appelé dans l’écriture affectation commande service, ce qui indique la ressource ou le groupe de ressources affecté n’a pas tenté la tâche service.  
  
L’état affectation indique la fin du processus de maintenance ou le besoin d’une autre ressource pour terminer la maintenance de l’article de service.  
  
## <a name="converting-service-quotes-to-service-orders"></a><a name="converting-service-quotes-to-service-orders"></a><a name="converting-service-quotes-to-service-orders"></a>Conversion des devis service en commandes service
Lorsque vous convertissez un devis service en commande service, la commande service, les articles service de la commande et leurs écritures affectation sont mis à jour de la manière suivante :  
  
* L’état réparation des articles de service est paramétré sur **Initial**.  
* Le statut de commande service est changé en **Suspendu**.  
* Une recherche d’écritures affectation de tous les articles de service de la commande service qui présentent le statut **Actif** est effectuée. s’il en est trouvé, leur état affectation passe de **Actif** à **Réaffectation nécessaire**.  
  
## <a name="canceling-allocations"></a><a name="canceling-allocations"></a><a name="canceling-allocations"></a>Annulation d’affectations
Lorsque vous annulez une affectation d’un article de service, [!INCLUDE[prod_short](includes/prod_short.md)] met à jour l’état affectation de l’écriture affectation correspondante de **Actif** à **Réaffectation nécessaire**.

L’état réparation de l’article de service de l’écriture affectation est mis à jour comme suit :  
  
* Si l’état réparation est **Initial**, il est modifié en **Expertisé** (aucune maintenance n’a été lancée).  
* Si l’état réparation est **En cours**, il est modifié en **Service en partie réalisé** (la maintenance a été partiellement effectuée).  
  
## <a name="reallocating-an-active-allocation-entry"></a><a name="reallocating-an-active-allocation-entry"></a><a name="reallocating-an-active-allocation-entry"></a>Réaffectation d’une écriture affectation active
Lorsque vous réaffectez un article de service à une écriture affectation dont le statut est **active**, l’écriture affectation est mise à jour comme suit :  
  
* Si la maintenance a débuté quand l’affectation était **Active** (c’est-à-dire, si l’état réparation de l’article de service de l’écriture est passé à **En cours**), l’état affectation est passé de **Active** à **Terminée**.  
* Si la maintenance n’a pas débuté lorsque l’affectation était **Active**,l’état affectation est passé de **Active** à **Annulée**.  
  
L’état réparation de l’article de service de l’écriture affectation est mis à jour de la même manière que si vous aviez annulé l’affectation :  
  
* Si l’état réparation est **Initial**, il est modifié en **Expertisé** (aucune maintenance n’a été lancée).  
* Si l’état réparation est **En cours**, il est modifié en **Service en partie réalisé** (la maintenance a été partiellement effectuée).  
  
Une nouvelle écriture affectation comportant la nouvelle ressource est créée et présente le statut **Actif**.  
  
## <a name="reallocating-a-service-item"></a><a name="reallocating-a-service-item"></a><a name="reallocating-a-service-item"></a>Réaffectation d’un article de service
Lorsque vous réaffectez un article de service sur une écriture affectation qui a le statut **Réaffectation nécessaire**, l’écriture affectation est mise à jour comme suit :  
  
* Si la maintenance a débuté quand l’affectation était **Active** (c’est-à-dire, si l’état réparation de l’article de service de l’écriture est passé à **En cours**), l’état affectation est passé de **réallocation nécessaire** à **Terminée**.  
* Si la maintenance n’a pas débuté lorsque l’affectation était **Active**,l’état affectation est passé de **Réallocation nécessaire** à **Annulée**.  
  
Une nouvelle écriture affectation comportant la nouvelle ressource est créée et présente le statut **Actif**.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Configurer l’affectation des ressources](service-how-setup-resource-allocation.md)  
[Affecter des ressources](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
