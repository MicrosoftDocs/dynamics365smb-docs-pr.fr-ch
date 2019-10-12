---
title: Définition de filtres pour les bases de ventilation dynamique | Microsoft Docs
description: Le mode de ventilation dynamique dépend des valeurs modifiables. Par exemple, le nombre de salariés dans un centre de coûts ou le nombre d'articles vendus d'un coût associé pour une période donnée. Il existe neuf bases de ventilation prédéfinies et douze plages de dates dynamiques. Vous définissez plusieurs filtres en fonction de la base de ventilation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 1ae73e7808db2f0c9ab9bd4c2567b109ef245490
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305563"
---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Définition de filtres pour les bases de ventilation dynamique
Le mode de ventilation dynamique dépend des valeurs modifiables. Par exemple, le nombre de salariés dans un centre de coûts ou le nombre d'articles vendus d'un coût associé pour une période donnée. Il existe neuf bases de ventilation prédéfinies et douze plages de dates dynamiques. Vous définissez plusieurs filtres en fonction de la base de ventilation.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Définition de filtres pour les bases de ventilation dynamique  
 Le tableau suivant affiche les filtres applicables aux diverses bases de ventilation et les valeurs valides dans les champs **Filtre n°** et **Filtre groupe**. Appuyez sur F1 dans le champ **Code filtre date** pour lire les descriptions détaillées.  

|**Base**|**Filtre n°**|**Code filtre date**|**Filtre centre de coûts**|**Filtre coûts associés**|**Filtre groupe**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Écritures comptables|Compte général|Oui|Oui|Oui|N/A|  
|Écritures budget|Compte général|Oui|Oui|Oui|Nom budget comptable|  
|Écritures du type de coût|Type coût|Oui|Oui|Oui|N/A|  
|Écritures budget des coûts|Type coût|Oui|Oui|Oui|Nom du budget|  
|Nombre de salariés|N/A|Oui|Oui|Oui|N/A|  
|Articles vendus (qté)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles achetés (qté)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles vendus (montant)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles achetés (montant)|Nombre d'articles|Oui|Oui|Oui|Groupe compta. stock|  

## <a name="see-also"></a>Voir aussi  
[Définition et répartition des coûts](finance-define-and-allocate-costs.md)
