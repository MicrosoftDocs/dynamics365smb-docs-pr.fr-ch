---
title: Configurer des codes prestations standard | Microsoft Docs
description: "Découvrez comment configurer des codes pour les activités de service que vous effectuez souvent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bca816da5473ea3f5f8eab892125e32a045ffec3
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-standard-service-codes"></a>Configurer des codes prestation standard
Lorsque vous exécutez un service courant, il est fréquent que vous deviez créer des documents service qui utilisent des lignes service contenant des informations similaires. Pour faciliter la création de ces lignes, vous pouvez configurer des codes prestation standard avec un ensemble prédéfini de lignes service. Lorsque vous sélectionnez le code sur un document service, les lignes sont saisies automatiquement. Vous pouvez configurer autant de codes prestation standard que vous le souhaitez, et chaque code peut avoir un nombre illimité de lignes service de différents types, notamment l'article, la ressource, le coût ou le texte standard qui lui est associé. Créez des lignes service pour chaque code prestation standard dans la fiche **Code prestation standard**. Vous pouvez ensuite affecter les codes prestation standard à des groupes articles de service dans la page **Codes gpe articles de service standard**. Par la suite, lorsque vous créez un document service, vous pouvez utiliser l'action **Extraire codes prestation std** pour ajouter des lignes service.  
  
> [!Tip]
>  Vous pouvez utiliser le même concept pour créer des lignes dans les documents achat et vente. Pour plus d'informations, voir [Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>Pour configurer un code prestation standard    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Codes prestation standard**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Renseignez les lignes service liées à ce code prestation.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Pour affecter un code prestation standard à un groupe articles de service
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes articles de service**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Renseignez les lignes service liées à ce code prestation.  

## <a name="see-also"></a>Voir aussi
[Gestion des services](service-service.md)