---
title: Rangement d’articles | Microsoft Docs
description: L’activité entrepôt consistant à ranger les articles une fois reçus ou fabriqués s’exécute différemment selon la configuration des fonctionnalités du module Gestion d’entrepôt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6fbd192b5999d566271163c9653c3bcdfe0dbba1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755782"
---
# <a name="putting-items-away"></a>Rangement des articles
L’activité entrepôt consistant à ranger les articles une fois reçus ou fabriqués s’exécute différemment selon la configuration des fonctionnalités du module Gestion d’entrepôt. Le niveau de complexité du paramétrage varie : aucune fonctionnalité entrepôt, configurations de stockage de base pour le traitement par commande dans une ou plusieurs activités uniquement, configurations avancées dans lesquelles toutes les activités entrepôt doivent être exécutées dans un flux suggéré. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Si vous décidez d’organiser et d’enregistrer vos informations de rangement avec des documents entrepôt, activez le champ **Rangement requis** dans la fiche magasin. Ceci indique à l’application que, lorsque vous avez des articles qui entrent dans l’entrepôt via un document origine entrant, vous souhaitez que le rangement de ces articles soit contrôlé par le système. Un document origine entrant peut être une commande achat, un retour vente, un enlogement transfert ou un ordre de fabrication dont la fabrication est prête à être rangée.  

Si votre magasin est configuré pour nécessiter un traitement des rangements, mais pas un traitement des réceptions, vous utilisez la page **Rangement stock** pour organiser les informations de rangement, les imprimer, entrer le résultat du rangement effectif et valider les informations de rangement, ce qui valide les informations de réception pour le document source. En cas d’ordre de fabrication, le processus de validation valide la production de l’ordre et termine l’ordre de fabrication.

Si votre magasin est configuré pour exiger à la fois le traitement des réceptions et des rangements, de sorte que vous ayez activé les deux champs **Réception requise** et **Rangement requis** dans la fiche magasin, le rangement des articles exige un processus différent. Dans ce cas, vous utilisez la page **Rangement entrepôt** pour traiter le rangement. Le rangement entrepôt fonctionne comme le rangement stock, si ce n’est qu’au lieu de valider les informations, vous enregistrez le rangement. Remarquez que l’enregistrement du rangement entrepôt ne valide pas la réception des articles. Il met simplement à jour le contenu de l’emplacement. En tant qu’administrateur entrepôt, vous pouvez utiliser des feuilles rangement pour organiser les informations de rangement avant de créer des instructions de rangement entrepôt.

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Valider la réception d’articles directement à partir du document commande entrante et donc enregistrer le rangement, car aucune fonctionnalité entrepôt n’existe.|[Réceptionner des articles](warehouse-how-receive-items.md)|  
|Ranger les articles par commande et valider la réception dans la même activité dans une configuration entrepôt de base.|[Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Ranger les articles de plusieurs commandes dans une configuration entrepôt avancée.|[Ranger des articles avec le rangement entrepôt](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Ranger les articles fabriqués ou assemblés dans une configuration de stockage de base ou avancée.|[Rangement du résultat de fabrication ou d’assemblage](warehouse-how-to-put-away-production-output.md)|
|Planifier des instructions de rangement optimisées pour plusieurs réceptions entrepôt validées. Dans ce cas, les magasiniers n’ont pas à agir directement sur les réceptions.|[Planifier des rangements dans la feuille](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Replacer les articles prélevés techniquement à l’aide d’un prélèvement interne, par exemple dans le cadre d’un ordre de fabrication pour lequel la quantité prévue n’a pas été consommée.|[Prélever et ranger sans document origine](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Répartir une ligne rangement pour placer une partie de la quantité rangée dans les emplacements disponibles en raison du remplissage de l’emplacement désigné.|[Répartir des lignes activité entrepôt](warehouse-how-to-split-warehouse-activity-lines.md)|
|Accéder immédiatement aux rangements qui vous ont été affectés en tant que magasinier.|[Trouver vos affectations d’entrepôt](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
