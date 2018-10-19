---
title: "Procédure : transférer les écritures comptables vers les écritures de coûts | Microsoft Docs"
description: "Vous pouvez transférer les écritures comptables aux écritures de coûts."
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
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transférer les écritures comptables vers les écritures de coûts
Vous pouvez transférer les écritures comptables aux écritures de coûts.  

Avant d'exécuter le transfert des écritures comptables vers des écritures de coûts, vous devez vous y préparer pour éviter toute validation manuelle de correction.  

## <a name="to-prepare-the-transfer"></a>Pour préparer le transfert  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres comptabilité analytique**, puis sélectionnez le lien associé.  
2.  Dans la fenêtre **Paramètres comptabilité analytique**, vérifiez que le champ **Date début pour transfert comptabilité** est défini sur la valeur appropriée.  
3.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable des types de coûts**, puis sélectionnez le lien associé.  
4.  Dans la fenêtre **Fiche type de coût**, vérifiez que le champ **Plage compte général** est lié correctement de sorte que chaque type de coût récupère les écritures de la comptabilité.  
5.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.  
6.  Pour chaque compte général approprié, dans la fenêtre **Fiche compte général**, dans le raccourci Comptabilité analytique, vérifiez que le champ **N° type coût** est lié correctement à un type de coût. Pour plus d'informations, voir [Définition de la relation entre les types de coûts et les comptes généraux](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Vérifiez que toutes les écritures comptables appropriées comprennent des sections analytiques correspondant à un centre de coûts et à un coût associé.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Pour transférer les écritures comptables vers les écritures de coûts  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien associé.  
2.  Cliquez sur le bouton **Oui** pour démarrer le transfert. Le processus transfère toutes les écritures comptables qui n'ont pas déjà été transférées.  

    Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**. Cela permet d'identifier l'origine des écritures de coûts.  

## <a name="see-also"></a>Voir aussi  
 [Critères de transfert des écritures comptables vers les écritures de coûts](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Transfert automatique et écritures combinées](finance-automatic-transfer-combined-entries.md)   
 [Résultats du transfert](finance-results-of-the-transfer.md)   
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
 [Définition de la relation entre les types de coûts et les comptes généraux](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

