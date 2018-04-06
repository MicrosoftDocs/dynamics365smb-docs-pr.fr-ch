---
title: "Procédure : transférer les écritures comptables vers les écritures de coûts | Microsoft Docs"
description: "Vous pouvez transférer les écritures comptables aux écritures de coûts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 592f42f53593735526ccbd3ddaa69bb0778de0ac
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transférer les écritures comptables vers les écritures de coûts
Vous pouvez transférer les écritures comptables aux écritures de coûts.  

Avant d'exécuter le transfert des écritures comptables vers des écritures de coûts, vous devez vous y préparer pour éviter toute validation manuelle de correction.  

## <a name="to-prepare-the-transfer"></a>Pour préparer le transfert  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres comptabilité analytique**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **Paramètres comptabilité analytique**, vérifiez que le champ **Date début pour transfert comptabilité** est défini sur la valeur appropriée.  
3.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable des types de coûts**, puis sélectionnez le lien connexe.  
4.  Dans la fenêtre **Fiche type de coût**, vérifiez que le champ **Plage compte général** est lié correctement de sorte que chaque type de coût récupère les écritures de la comptabilité.  
5.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.  
6.  Pour chaque compte général approprié, dans la fenêtre **Fiche compte général**, dans le raccourci Comptabilité analytique, vérifiez que le champ **N° type coût** est lié correctement à un type de coût. Pour plus d'informations, voir [Définition de la relation entre les types de coûts et les comptes généraux](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Vérifiez que toutes les écritures comptables appropriées comprennent des sections analytiques correspondant à un centre de coûts et à un coût associé.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Pour transférer les écritures comptables vers les écritures de coûts  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien connexe.  
2.  Cliquez sur le bouton **Oui** pour démarrer le transfert. Le processus transfère toutes les écritures comptables qui n'ont pas déjà été transférées.  

    Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**. Cela permet d'identifier l'origine des écritures de coûts.  

## <a name="see-also"></a>Voir aussi  
 [Critères de transfert des écritures comptables vers les écritures de coûts](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Transfert automatique et écritures combinées](finance-automatic-transfer-combined-entries.md)   
 [Résultats du transfert](finance-results-of-the-transfer.md)   
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
 [Définition de la relation entre les types de coûts et les comptes généraux](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

