---
title: Configuration de la TVA sur encaissement | Microsoft Docs
description: "Si vous utilisez la comptabilité basée sur la trésorerie, vous pouvez spécifier comment gérer la TVA sur encaissement pour les ventes et les achats."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 5e505f1942aba554bfa83a0fb81ace0db209b102
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Configurer la TVA sur encaissement pour la comptabilité basée sur la trésorerie
Si vous utilisez des méthodes comptables basées sur la trésorerie, vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour gérer la TVA sur encaissement.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Pour utiliser les comptes généraux pour la TVA sur encaissement
Vous pouvez choisir de calculer et de valider les montants de TVA dans un compte général temporaire lorsqu'une facture est validée, puis de les valider dans le compte général approprié et de les inclure dans des déclarations de TVA lorsque le paiement réel de la facture est validé. Pour cela, vous devez définir des paramètres validation TVA.

Pour utiliser les comptes pour la TVA sur encaissement, procédez comme suit :
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), et saisissez **Paramètres comptabilité**.
2. Sur la fenêtre **Paramètres comptabilité**, sous le raccourci **Général**, sélectionnez **Afficher plus**, puis activez la case à cocher **TVA sur encaissement**.
3. Fermez la page.
4. Choisissez l'icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), et saisissez **Paramètres compta. TVA**.
5. Sur la fenêtre **Paramètres compta. TVA**, sélectionnez le groupe comptabilisation TVA, puis sélectionnez **Modifier**.
6. Dans le champ **Type TVA sur encaissement**, choisissez une option pour spécifier comment ventiler des paiements sur le montant de la facture (hors TVA) et le montant TVA, et comment transférer les montants TVA du compte TVA sur encaissement vers le compte réalisée. Le tableau suivant décrit les options.

| Option | Désignation |
| --- | --- |
| Vide | Sélectionnez cette option si vous ne souhaitez pas utiliser la fonction TVA sur encaissement. |
| Pourcentage | Les paiements couvrent à la fois la TVA et le montant de la facture proportionnellement au pourcentage de paiement du total de la facture. Le montant de TVA payé est transféré du compte TVA sur encaissement vers le compte TVA réalisé. |
| Premier | Les paiements couvrent d'abord la TVA puis le montant de la facture. Dans ce cas, le montant transféré du compte TVA sur encaissement vers le compte TVA est égal au montant du paiement jusqu'à ce que toute la TVA soit payée. |
| Dernier | Les paiements couvrent d'abord le montant de la facture puis la TVA. Dans ce cas, aucun montant n'est transféré du compte TVA sur encaissement vers le compte TVA jusqu'à ce que le montant total de la facture, hors TVA, soit payé. |
| Premier (Payé entièrement) | Les paiements couvrent d'abord la TVA (comme pour _Premier_), mais aucun montant n'est transféré vers le compte TVA jusqu'à ce que le montant total de la TVA soit payé. |
| Dernier (Payé entièrement) | Les paiements couvrent d'abord le montant de la facture (comme pour _Dernier_), mais aucun montant n'est transféré sur le compte TVA jusqu'à ce que le montant total de la TVA soit payé. |

6. Dans le champ **Cpte TVA/encaissement vente**, choisissez le compte de la TVA sur encaissement vente.

    > [!NOTE]  
    > Le montant de la TVA est validé sur ce compte jusqu'à ce que le paiement de la facture soit validé. Le montant est alors transféré sur le compte pour la TVA vente.
7. Dans le champ **Cpte TVA/décaissement achat**, entrez le compte général de la TVA sur décaissement achat.

> [!NOTE]  
> Le montant de la TVA est validé sur ce compte jusqu'à ce que le paiement de la facture soit validé. Le montant est alors transféré sur le compte pour la TVA achat.

## <a name="see-also"></a>Voir aussi
[Configuration de la TVA](finance-setup-vat.md)

