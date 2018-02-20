---
title: Configurer des processus incident | Microsoft Docs
description: "Découvrez comment configurer des processus qui aident les conseillers du service clientèle à identifier et à résoudre les problèmes liés aux articles de service."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5876bf5d959d106eefb9b0f765e42e74dd13ab07
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---

# <a name="setting-up-troubleshooting-for-service-items"></a>Configuration des processus incident pour les articles de service
Vous pouvez configurer des instructions incident qui aident les conseillers du service clientèle à résoudre les problèmes lors de la fourniture de services. Par exemple, les instructions peuvent être une liste d'étapes pour effectuer une réparation, ou une série de questions à poser sur les articles. Une fois que vous avez configuré les instructions incident, vous pouvez les affecter à des groupes articles de service, des articles de service et des articles. Il existe une hiérarchie d'héritage pour les instructions. Si vous les affectez à un groupe articles de service, les articles inclus dans le groupe héritent des instructions sauf si vous les spécifiez pour les articles. De même, les articles de service héritent des instructions des articles.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Pour configurer des instructions incident
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Incident**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>Pour affecter des instructions incident à des articles, des articles de service ou des groupes articles de service
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Articles**, **Articles de service** ou **Groupe articles de service**, puis sélectionnez le lien connexe.  
2. Sélectionnez l'entité appropriée, puis l'action **Incident**.  

## <a name="see-also"></a>Voir aussi
[Gestion des services](service-service.md)
