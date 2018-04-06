---
title: "Procédure d'utilisation de l'unité de lot de fabrication | Microsoft Docs"
description: "Si un article est stocké dans une unité mais produit dans une autre, l'ordre de fabrication doit utiliser une unité de lot de fabrication pour calculer la quantité correcte des composants. Une situation dans laquelle un article fabriqué est stocké en pièces mais produit en tonnes est un exemple d'un calcul d'unité de lot de fabrication."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7dafbb96b4ce4f5ad525ab299edd8549c7aa600e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Utiliser les unités de lot de fabrication
Si un article est stocké dans une unité mais produit dans une autre, un ordre de fabrication utilisant une unité de lot de fabrication est créé pour calculer la quantité correcte des composants durant le traitement par lots **Actualiser O.F.**. Une situation dans laquelle un article fabriqué est stocké en pièces mais produit en tonnes est un exemple d'un calcul d'unité de lot de fabrication.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Pour créer une nomenclature de production à l'aide d'une unité de lot  
1.  L'unité de lot de fabrication est configurée comme unité alternative dans la fenêtre **Unités article** pour l'article à produire. L'unité de lot ne remplace pas l'unité de base pour l'article.  
2.  Créez une nomenclature de production pour l'article configuré avec l'unité de lot de fabrication. Pour plus d'informations, reportez-vous à [Créer des nomenclatures de production](production-how-to-create-production-boms.md).  
3.  Dans le champ **Code unité**, sélectionnez l'unité de lot de fabrication.  
4.  Pour chaque ligne de nomenclature de production, dans le champ **Quantité par**, entrez la quantité de cet article composant requise pour créer cette unité de lot.  
5.  Ouvrez la fenêtre **Fiche article** pour l'article en question.  

    Sur le raccourci **Réapprovisionnement**, dans le champ **N° nomenclature production**, sélectionnez la nomenclature de production créée précédemment.  
6.  Créez un en-tête d'ordre de fabrication en utilisant l'article configuré avec l'unité de lot de fabrication. Pour plus d'informations, voir [Créer des ordres de fabrication](production-how-to-create-production-orders.md).  
7.  Choisissez l'action **Actualiser**, puis le bouton **OK**.  

Sur le raccourci **Lignes**, choisissez l'action **Ligne**, puis l'action **Composants** pour afficher le résultat. Le programme calcule la quantité correcte de composants nécessaire pour satisfaire la nomenclature de production, basée sur l'unité de lot de fabrication.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Pour calculer une unité de lot de fabrication sur un ordre de fabrication  
1.  Créez un en-tête d'ordre de fabrication en utilisant l'article configuré avec l'unité de lot de fabrication.  
2.  Dans le champ **N° article** de la ligne ordre de fabrication, tapez le numéro article utilisé dans l'en-tête.  
3.  Dans le champ **Quantité**, entrez la quantité utilisée dans l'en-tête.  
4.  Dans le champ **Code unité**, sélectionnez le code unité de lot de fabrication.  
5.  Sélectionnez l'action **Actualiser**.
6.  Sur le raccourci **Calculer**, désactivez la case à cocher **Lignes**.  
7.  Cliquez sur le bouton **OK**.  
8.  Sur le raccourci **Lignes**, choisissez l'action **Ligne**, puis l'action **Composants** pour afficher le résultat. La quantité correcte de composants nécessaire pour satisfaire la nomenclature de production est calculée sur la base de l'unité de lot de fabrication.  

## <a name="see-also"></a>Voir aussi  
[Créer des gammes](production-how-to-create-routings.md)  
[Créer des nomenclatures de production](production-how-to-create-production-boms.md)     
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[Planifié](production-planning.md)   
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

