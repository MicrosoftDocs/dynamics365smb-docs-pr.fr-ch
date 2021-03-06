---
title: 'Procédure : imprimer des rapports contenant les listes de paiements fournisseurs'
description: Le rapport Liste de paiements fournisseur fournit la liste des paiements pour chaque fournisseur. Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a9c3c80fcbca4c948543c3cf6f78f31df25d1469
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776547"
---
# <a name="print-vendor-payments-list-reports"></a>Imprimer des rapports contenant les listes de paiements fournisseurs

Le rapport **Liste de paiements fournisseur** fournit la liste des paiements pour chaque fournisseur. Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.  

> [!NOTE]
> Le rapport **Liste de paiements fournisseurs** est disponible dans les marchés suivants : Autriche, Allemagne, Suisse.

## <a name="to-print-the-vendor-payments-list-report"></a>Pour imprimer des rapports contenant les listes de paiements fournisseurs  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste de paiements fournisseur**, puis sélectionnez le lien associé.  
2. Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Tri**|Spécifie l'ordre de tri. Vous pouvez effectuer un tri par fournisseur ou de façon chronologique. Si vous effectuez un tri par fournisseur, vous verrez un sous-total pour chaque fournisseur. Si vous effectuez un tri chronologique, vous ne pourrez pas voir les sous-totaux.|  
    |**Mise en page**|Spécifie la mise en page du rapport.<br /><br /> Les résultats peuvent être affichés dans les présentations suivantes :<br /><br /> **Standard**<br /> Affiche le numéro du fournisseur et le nom du fournisseur, ainsi que les détails de la validation, tels que le numéro du document et le montant en devise locale.<br /><br /> **Montants DE**<br /> Affiche le numéro du fournisseur, le nom du fournisseur, le numéro du document, le statut du paiement (O pour ouvert, PP pour paiement partiel et C pour clôturé) et le montant du paiement.<br /><br /> **Informations de validation**<br /> Affiche le numéro du fournisseur, le nom du fournisseur, le centre de coûts, les coûts associés, le code utilisateur et le montant règlement.|  

 À la fin du rapport, le nombre de paiements traités est affiché.  

## <a name="see-also"></a>Voir aussi

[Effectuer des paiements](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]