---
title: "Définition des centres de coûts et des coûts associés pour le plan comptable | Microsoft Docs"
description: "Vous pouvez transférer automatiquement les écritures de dépenses et de revenus à partir de la comptabilité générale vers la comptabilité analytique, que ce soit pour la validation comptable ou avec un traitement par lots. Lors du transfert, le système transfère uniquement les écritures déjà liées à un centre de coûts ou aux coûts associés. Pour préparer un transfert pertinent, assurez-vous que les centres de coûts et les coûts associés sont définis correctement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5da3967e99bf8a1d5628159a542885ffd1113a02
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Définition des centres de coûts et des coûts associés pour le plan comptable
Vous pouvez transférer automatiquement les écritures de dépenses et de revenus à partir de la comptabilité générale vers la comptabilité analytique, que ce soit pour la validation comptable ou avec un traitement par lots. Lors du transfert, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfère uniquement les écritures déjà liées à un centre de coûts ou aux coûts associés. Pour préparer un transfert pertinent, assurez-vous que les centres de coûts et les coûts associés sont définis correctement.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Définition des sections analytiques par défaut pour des comptes généraux  
Pour chaque compte général, vous pouvez définir des sections analytiques par défaut dans la table **Affectation analytique**. L'exemple suivant décrit la configuration requise pour avoir un centre de coût DÉPARTEMENT sans jamais avoir de coûts associés PROJET lors de la validation d'un compte général.  

|**Code axe analytique**|**Contrôle validation**|  
|------------------------------------------|-----------------------------------------|  
|Département|Code obligatoire|  
|Dossier|Pas de code|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Définition des sections analytiques pour les frais généraux et les coûts directs  
 Vous pouvez transférer des frais généraux à un centre de coûts, et des coûts directs aux coûts associés. Le tableau suivant décrit comment optimiser la combinaison des valeurs de paramétrage des axes analytiques.  

|Transférer vers|Validation du centre de coûts|Validation des coûts associés|  
|-----------------|-------------------------|-------------------------|  
|Centre de coûts|Code obligatoire|Pas de code|  
|Coûts associés|Pas de code|Code obligatoire|  

> [!NOTE]  
>  Pour vous assurer que le centre de coûts et les coûts associés prédéfinis et configurés en comptabilité générale sont reportés automatiquement dans la comptabilité analytique, cochez la case **Vérifier validations compta** dans la fenêtre Paramètres comptabilité analytique.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Configuration des centres de coûts](finance-how-to-set-up-cost-centers.md)   
[Configurer les coûts associés](finance-how-to-set-up-cost-objects.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

