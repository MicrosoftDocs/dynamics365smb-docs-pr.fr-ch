---
title: 'Procédure : Importer des paiements ESR'
description: Après avoir reçu le paiement d'un client, vous recevez un fichier contenant des informations sur les factures payées. Vous pouvez recevoir ce fichier de votre banque par voie électronique, ou par courrier électronique.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 60f4072ad2b303e3f575e9910b8c2f7f96281c48
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383986"
---
# <a name="import-esr-payments"></a>Importer des paiements ESR
Après avoir reçu le paiement d'un client, vous recevez un fichier contenant des informations sur les factures payées. Vous pouvez recevoir ce fichier de votre banque par voie électronique, ou par courrier électronique.  

Vous pouvez importer les données de facture Einzahlungsschein mit Referenznummer (ESR) issues du fichier, imprimer les données en utilisant l'état ESR de la facture de vente ou le rapport de coupon ESR des ventes, et les vérifier avant de les valider. Pour plus d'informations, reportez-vous à [Imprimer des factures ESR](how-to-print-esr-invoices.md).  

## <a name="to-import-esr-payments"></a>Pour importer des paiements ESR  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles règlement**, puis sélectionnez le lien associé.  
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