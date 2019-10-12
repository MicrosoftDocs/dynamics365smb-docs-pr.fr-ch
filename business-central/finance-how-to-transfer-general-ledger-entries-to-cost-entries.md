---
title: 'Procédure : transférer les écritures comptables vers les écritures de coûts | Microsoft Docs'
description: Vous pouvez transférer les écritures comptables aux écritures de coûts.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c6eace42d460432df8ab4b72964408469fa0b563
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305895"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transférer les écritures comptables vers les écritures de coûts
Vous pouvez transférer les écritures comptables aux écritures de coûts.  

Avant d'exécuter le transfert des écritures comptables vers des écritures de coûts, vous devez vous y préparer pour éviter toute validation manuelle de correction.  

## <a name="to-prepare-the-transfer"></a>Pour préparer le transfert  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres comptabilité analytique**, puis sélectionnez le lien associé.  
2.  Sur la page **Paramètres comptabilité analytique**, vérifiez que le champ **Date début pour transfert comptabilité** est défini sur la valeur appropriée.  
3.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable des types de coûts**, puis sélectionnez le lien associé.  
4.  Sur la page **Fiche type de coût**, vérifiez que le champ **Plage compte général** est lié correctement de sorte que chaque type de coût récupère les écritures de la comptabilité.  
5.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.  
6.  Pour chaque compte général approprié, sur la page **Fiche compte général**, dans le raccourci Comptabilité analytique, vérifiez que le champ **N° type coût** est lié correctement à un type de coût. Pour plus d'informations, voir [Configuration du contrôle de gestion](finance-set-up-cost-accounting.md).  
7.  Vérifiez que toutes les écritures comptables appropriées comprennent des sections analytiques correspondant à un centre de coûts et à un coût associé.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Pour transférer les écritures comptables vers les écritures de coûts  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien associé.  
2.  Cliquez sur le bouton **Oui** pour démarrer le transfert. Le processus transfère toutes les écritures comptables qui n'ont pas déjà été transférées.  

    Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**. Cela permet d'identifier l'origine des écritures de coûts.  

## <a name="see-also"></a>Voir aussi  
[Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)   
