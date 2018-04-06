---
title: "Définition des ventilations statiques en fonction du ratio d'affectation | Microsoft Docs"
description: "Le mode de ventilation statique dépend d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4."
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
ms.openlocfilehash: 8b4d26e3cb8a1364745dd25ca5341635c49a5718
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Exemple de scénario : Définition des ventilations statiques en fonction du ratio d'affectation
Le mode de ventilation statique dépend d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.  

Cette rubrique décrit comment définir trois nouveaux coûts associés pour la cibles d'affectation pour le centre de coûts PROD de la source d'affectation à l'aide d'un ratio de ventilation prédéfini, comme 5:2:4. Les trois coûts associés cibles sont ACCESSO, PEINTURE et ACCESSOIRES.  

> [!NOTE]  
>  L'exemple utilise les données de démonstration dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Pour définir le centre de coûts PROD de la source d'affectation sur le raccourci Général  

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Affectation des coûts**, puis choisissez le lien associé.  
2.  Dans la fenêtre **Affectation des coûts**, sélectionnez l'action **Nouveau**.  
3.  Dans le champ **ID**, appuyez sur Entrée ou saisissez un ID.  
4.  Dans le champ **Niveau**, saisissez **1**.  
5.  Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6.  Dans le champ **Code centre de coûts**, entrez **PROD**.  
7.  Dans le champ **Type de crédit\\\/coût**, entrez le type de coût **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Pour définir les coûts associés de la cible d'affectation sur le raccourci Lignes  

1.  Sur la première ligne facture, dans le champ **Type coût cible**, saisissez **9903**.  
2.  Sur la première ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSO**.  
3.  Sur la première ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
4.  Sur la première ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
5.  Sur la première ligne, dans le champ **Part**, saisissez le ratio d'affectation **5**.  
6.  Sur la deuxième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
7.  Sur la deuxième ligne, dans le champ **Coûts associés cibles**, saisissez **PEINTURE**.  
8.  Sur la deuxième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
9. Sur la deuxième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
10. Sur la deuxième ligne, dans le champ **Part**, saisissez le ratio d'affectation **2**.  
11. Sur la troisième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
12. Sur la troisième ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSOIRES**.  
13. Sur la troisième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
14. Sur la troisième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
15. Sur la troisième ligne, dans le champ **Part**, saisissez le ratio d'affectation **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automatiquement le champ **Pour cent** à l'aide d'un pourcentage qui dépend de ces trois ratios d'affectation saisis dans le champ **Part** pour chacune des trois lignes.  

## <a name="see-also"></a>Voir aussi  
[Configurer la source d'affectation et ses cibles](finance-how-to-set-up-allocation-source-and-targets.md)   
[Définition et répartition des coûts](finance-define-and-allocate-costs.md)   
[Exemple de scénario : définition des ventilations dynamiques sur la base des articles vendus](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Définition et répartition des coûts](finance-define-and-allocate-costs.md)

