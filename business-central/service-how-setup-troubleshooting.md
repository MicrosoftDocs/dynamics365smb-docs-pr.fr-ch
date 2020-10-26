---
title: Configurer des processus incident | Microsoft Docs
description: Découvrez comment configurer des processus qui aident les conseillers du service clientèle à identifier et à résoudre les problèmes liés aux articles de service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ea836775e8dc32107620d90d67fbf4a614c5d9b8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910245"
---
# <a name="setting-up-troubleshooting-for-service-items"></a>Configuration des processus incident pour les articles de service
Vous pouvez configurer des instructions incident qui aident les conseillers du service clientèle à résoudre les problèmes lors de la fourniture de services. Par exemple, les instructions peuvent être une liste d’étapes pour effectuer une réparation, ou une série de questions à poser sur les articles. Une fois que vous avez configuré les instructions incident, vous pouvez les affecter à des groupes articles de service, des articles de service et des articles. Il existe une hiérarchie d’héritage pour les instructions. Si vous les affectez à un groupe articles de service, les articles inclus dans le groupe héritent des instructions sauf si vous les spécifiez pour les articles. De même, les articles de service héritent des instructions des articles.  

## <a name="to-set-up-troubleshooting-guidelines"></a>Pour configurer des instructions incident
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Incident** , puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a>Pour affecter des instructions incident à des articles, des articles de service ou des groupes articles de service
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , **Articles de service** ou **Groupes articles de service** , puis sélectionnez le lien associé.  
2. Sélectionnez l’entité appropriée, puis l’action **Incident** .  

## <a name="see-also"></a>Voir aussi
[Gestion des services](service-service.md)