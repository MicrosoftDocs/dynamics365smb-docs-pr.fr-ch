---
title: "Exemple de scénario - Définition des ventilations dynamique sur la base des articles vendus | Microsoft Docs"
description: "Cette rubrique explique comment définir les affectations à l'aide du mode de ventilation dynamique."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 85d58264b14d191389bdf23a792dff7ad30bf9c3
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Exemple de scénario : Définition des ventilations dynamique sur la base des articles vendus
Cette rubrique explique comment définir les affectations à l'aide du mode de ventilation dynamique. Dans l'exemple, vous modifiez la ventilation dynamique des coûts pour que le centre de coûts VENTES prenne en charge le nouveau ÉQUIPEMENT IT de coûts associés. Les packages ÉQUIPEMENT IT ont des numéros d'articles dont la plage s'échelonne entre 8904-W et 8924-W. Vous pouvez utiliser les chiffres de ventes de l'exercice précédent pour en calculer la part. La ventilation est validée en fonction du type de coût 9903.  

> [!NOTE]  
>  L'exemple utilise les données de démonstration dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Pour définir les ventilations dynamique en fonction des articles vendus de l'exercice précédent  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Affectations des coûts**, puis choisissez le lien associé.  
2.  Dans la fenêtre **Affectation des coûts**, sélectionnez l'action **Nouveau**.  
3.  Dans le champ **ID**, appuyez sur Entrée ou saisissez un ID.  
4.  Dans le champ **Niveau**, saisissez **1**.  
5.  Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6.  Dans le champ **Code centre de coûts**, entrez **VENTES**.  
7.  Dans le champ **Type de crédit/coût**, entrez le type de coût **9903**.  
8.  Dans le champ **Type coût cible**, entrez le type de coût **9903**.  
9. Dans le champ **Objet de coûts cible**, sélectionnez **Nouveau** pour créer un nouvel objet de coût ÉQUIPEMENT IT et renseigner les champs, le cas échéant. Sélectionnez **ÉQUIPEMENT IT**. Laissez le champ **Centre de coûts cible** vide.  
10. Dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
11. Dans le champ **Base**, sélectionnez la base de ventilation **Articles vendus (Montant)**.  
12. Dans le champ **Filtre n°**, entrez **8904-W..8924-W**.  
13. Dans le champ **Code filtre date**, entrez **Année précédente**.  
14. Choisissez l'action **Calculer la clé de ventilation** pour calculer la part.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] utilise les chiffres de ventes des exercices précédents pour calculer une part de 1596,50 DS avec 100 % alloués pour les packages ÉQUIPEMENT IT. Cela signifie que tous les articles vendus au cours de l'exercice précédent seront affectés au ÉQUIPEMENT IT des coûts associés.  

## <a name="see-also"></a>Voir aussi  
 [Définition de filtres pour les bases de ventilation dynamique](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Configurer la source d'affectation et ses cibles](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Définition et répartition des coûts](finance-define-and-allocate-costs.md)   
 [Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)   
 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)

