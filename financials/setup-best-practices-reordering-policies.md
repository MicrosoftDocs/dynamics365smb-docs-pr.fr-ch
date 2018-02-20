---
title: "Pratiques de configuration recommandées : méthodes de réapprovisionnement | Microsoft Docs"
description: "Sur les fiches article, le champ **Méthode réapprovisionnement** propose quatre méthodes de planification différentes qui déterminent le mode d'interaction de chacun des paramètres de planification."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0041dcd1e1c7b4eda2d000c8c387bc8b751d4212
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="setup-best-practices-reordering-policies"></a>Pratiques de configuration recommandées : méthodes de réapprovisionnement
Sur les fiches article, le champ **Méthode réapprovisionnement** propose quatre méthodes de planification différentes qui déterminent le mode d'interaction de chacun des paramètres de planification.  

Pour sélectionner une méthode de réapprovisionnement, la classification ABC de l'article est particulièrement recommandée. Lorsque vous utilisez la classification ABC pour le contrôle du stock et la planification de l'approvisionnement, les articles sont gérés en fonction de trois classes différentes d'après leur valeur et leur volume par rapport au stock total. La répartition valeur-volume des trois classes est indiquée dans le tableau suivant.

|Classe|Pourcentage du volume du stock total|Pourcentage de la valeur du stock total|
|-----|-----------------------------|----------------------------|
|A|10 à 20|50 à 70|
|B|20|20|
|C|60 à 70|10 à 30|

La classification ABC révèle qu'il est possible de réduire les efforts et de réaliser des économies en appliquant aux articles de faible valeur-volume un contrôle moins strict qu'aux articles ayant une valeur ou un volume élevé. La figure ci-après indique quelle méthode de réapprovisionnement dans [!INCLUDE[d365fin](includes/d365fin_md.md)] est la mieux adaptée aux articles A, B et C, respectivement.

![Classification ABC](media/abc_classification.png "abc_classification")

Le tableau suivant propose des recommandations pour effectuer son choix parmi ces quatre méthodes.  

|Option de configuration|Meilleure pratique|Commentaires|  
|------------------|-------------------|-------------|  
|**Commande**|À utiliser avec des articles A.<br /><br /> À utiliser avec des articles fabriqués à la commande.<br /><br /> Au stade fabrication, à utiliser avec des articles de niveau supérieur et avec des composants et des produits semi-finis coûteux.<br /><br /> À utiliser avec des articles qui sont achetés sous forme de livraisons directes et de commandes spéciales.<br /><br /> Ne pas utiliser si vous n'acceptez pas la réservation automatique.|Les articles A (canapés en cuir dans un magasin de meubles, par exemple) sont des articles de grande valeur dont les commandes sont peu nombreuses et irrégulières excluant de fait leur stockage ou dont les attributs requis sont variables. La meilleure méthode de réapprovisionnement consiste par conséquent à procéder à une planification spécifique pour chaque demande.|  
|**Lot pour lot**|À utiliser avec des articles B.<br /><br /> Au stade fabrication, à utiliser avec des composants qui interviennent dans plusieurs nomenclatures. Cela permet de regrouper des commandes achat auprès d'un même fournisseur et de négocier les meilleurs prix.<br /><br /> À utiliser si vous hésitez sur la méthode de réapprovisionnement à sélectionner.|Les articles B (chaises de salon, par exemple) sont des articles dont les commandes sont assez nombreuses et régulières, mais dont les frais de transport sont élevés. La meilleure méthode de réapprovisionnement pour les articles B doit par conséquent être économique en regroupant la demande lors du réapprovisionnement.<br /><br /> Cette méthode peut être utilisée avec 80 % des articles.<br /><br /> Elle peut être utilisée avec efficacité sans paramètres de planification.|  
|**Qté fixe de commande.**|À utiliser avec des articles C.<br /><br /> À associer à des paramètres de point de commande.<br /><br /> Au stade fabrication, à utiliser avec des composants de niveau inférieur.<br /><br /> Ne pas utiliser si l'article est souvent réservé.|Les articles C (tasses à thé, par exemple) sont des articles présentant peu de valeur dont les commandes sont nombreuses et régulières. La meilleure méthode de réapprovisionnement pour les articles C doit par conséquent garantir une disponibilité constante en restant toujours au-dessus du point de commande.<br /><br /> Si l'utilisateur réserve une quantité en prévision d'une demande quelque peu lointaine, la planification s'en trouvera perturbée. Même si le niveau de stock prévisionnel est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles en raison de la réservation.|  
|**Qté maximum**|À utiliser avec des articles C dont les frais de transport sont élevés et les capacités de stockage limitées.<br /><br /> À associer à un ou plusieurs modificateurs d'ordre (Qté minimum commande, Qté maximum commande ou Commandé par).|Les articles C (tasses à thé, par exemple) sont des articles présentant peu de valeur dont les commandes sont nombreuses et régulières. La meilleure méthode de réapprovisionnement pour les articles C doit par conséquent garantir une disponibilité constante en restant toujours au-dessus du point de commande, mais en dessous de la capacité de stockage maximum.<br /><br /> Pour modifier la commande suggérée, vous pouvez réduire la quantité commande jusqu'à une quantité commande maximum spécifiée, l'augmenter jusqu'à une quantité commande minimum spécifiée ou l'arrondir pour qu'elle corresponde à un nombre de commandes spécifié. **Note :** en cas d'utilisation avec un point de commande, le stock doit rester entre le point de commande et la quantité maximum.|  

## <a name="see-also"></a>Voir aussi  
 [Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)   
 [Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
 [Détails de conception : commande](design-details-order.md)   
 [Détails de conception : lot pour lot](design-details-lot-for-lot.md)   
 [Détails de conception : qté fixe de commande.](design-details-fixed-reorder-qty.md)   
 [Détails de conception : qté maximum.](design-details-maximum-qty.md)   
 [Configurer les modules complexes à l'aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

