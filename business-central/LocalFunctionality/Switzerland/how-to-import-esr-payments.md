---
title: Importer des paiements ESR [CH]
description: Après avoir reçu le paiement d'un client, vous pouvez recevoir le fichier ESR contenant des informations sur les factures payées par votre banque par voie électronique.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 3010531, 3010532
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 9fda75d72844cf332a898c99ccecaeda5b31201d
ms.sourcegitcommit: f7e46d0f7b16d3b41e751aa9f337da18d37c11db
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/28/2021
ms.locfileid: "7947183"
---
# <a name="import-esr-payments-in-the-swiss-version"></a>Importer des paiements ESR dans la version suisse
Après avoir reçu le paiement d'un client, vous recevez un fichier contenant des informations sur les factures payées. Vous pouvez recevoir ce fichier de votre banque par voie électronique, ou par courrier électronique.  

Vous pouvez importer les données de facture Einzahlungsschein mit Referenznummer (ESR) issues du fichier, imprimer les données en utilisant l'état ESR de la facture de vente ou le rapport de coupon ESR des ventes, et les vérifier avant de les valider. Pour plus d'informations, reportez-vous à [Imprimer des factures ESR](how-to-print-esr-invoices.md).  

## <a name="to-import-esr-payments"></a>Pour importer des paiements ESR  

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Feuilles règlement**, puis sélectionnez le lien associé.  
2.  Dans le champ **Nom de la feuille**, sélectionnez le nom de feuille comptabilité requis.  

    > [!NOTE]  
    >  La feuille doit être vide avant l'importation du fichier ESR. Vous ne pouvez pas importer plusieurs fichiers ESR dans la même feuille règlement.  

3.  Choisissez l'action **Lire le fichier ESR**.  

    > [!NOTE]  
    >  Si vous avez défini plusieurs banques ESR, un message d'avertissement s'affiche pour vous inviter à choisir la banque concernée. Pour plus d'informations, voir la table Configuration ESR.  

4.  Cliquez sur le bouton **Oui**, puis sur le bouton **OK**.  

Les informations sur le paiement sont importées vers les lignes feuille. Les paiements sont automatiquement appliqués aux factures respectives selon des numéros de référence ESR uniques.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de ESR, Suisse](swiss-electronic-payments-using-esr.md)   
 [Imprimer des factures ESR](how-to-print-esr-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]