---
title: "Procédure : réviser ou lettrer les paiements manuellement après un lettrage automatique| Microsoft Docs"
description: "Procédure : réviser ou lettrer les paiements manuellement après un lettrage automatique"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d5515a3814d2fbd4dfb7accc16d9f8ffda44317
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-review-or-apply-payments-manually-after-automatic-application"></a>Procédure : réviser ou lettrer les paiements manuellement après un lettrage automatique
Pour chaque ligne feuille représentant un paiement dans la fenêtre **Feuille rapprochement bancaire**, vous pouvez ouvrir la fenêtre **Lettrage paiement** pour afficher toutes les écritures ouvertes candidates au paiement et les informations détaillées pour chaque écriture sur la correspondance des données sur laquelle un lettrage de paiement est basé. Ici, vous pouvez appliquer les paiements manuellement ou réappliquer les paiements qui ont été automatiquement appliqués à une écriture incorrecte. Pour plus d'informations sur le lettrage automatique, reportez-vous à [Procédure : rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

**Important**: lorsque le compte bancaire pour lequel vous rapprochez des paiements est configuré pour la devise locale, la fenêtre **Lettrage paiement** affiche toutes les écritures ouvertes dans la devise locale, y compris les écritures ouvertes pour les documents qui ont été initialement facturés en devise étrangère. Les paiements appliqués aux écritures avec devises converties peuvent donc être validés avec différents montants que celui qui figure sur le document d'origine en raison des taux de change potentiellement différents utilisés respectivement par la banque et [!INCLUDE[d365fin](includes/d365fin_md.md)].

Par conséquent, nous vous recommandons de rechercher les codes devise étrangère dans le champ **Code devise** de la fenêtre **Lettrage paiement** pour vérifier si les lettrages sont basés sur des devises converties. Pour réviser le montant du document d'origine dans la devise étrangère et afficher le taux de change utilisé, sélectionnez le champ **N° séquence lettrage** puis, dans le menu contextuel, cliquez sur le bouton de zoom pour ouvrir la fenêtre **Écritures comptables client** ou **Écritures comptables fournisseur**.

Aucun ajustement profits et pertes requis en raison de conversions de devise n'est géré automatiquement par [!INCLUDE[d365fin](includes/d365fin_md.md)]..

**Remarque**: vous ne pouvez pas appliquer d'écritures avec un signe différent du signe figurant sur le paiement. Par exemple, pour clôturer un avoir négatif et sa facture positive liée, vous devez d'abord appliquer l'avoir à la facture, puis appliquer le paiement à la facture avec le montant ouvert réduit.

**Avertissement** : si vous utilisez des escomptes, et si la date de paiement est antérieure à la date d'échéance de paiement, le champ **Montant ouvert remise incl.** de la fenêtre **Lettrage paiement** sera utilisé pour la correspondance. Sinon, la valeur du champ **Montant ouvert** sera utilisée. Si le paiement a été effectué avec un montant escompté après la date d'échéance du paiement, ou si le montant total a été payé mais qu'une remise a été accordée, le montant ne correspondra pas.

**Remarque**: vous ne pouvez appliquer un paiement qu'à un seul compte. Si vous souhaitez diviser l'application sur plusieurs écritures ouvertes, par exemple pour appliquer un paiement fixe, les écritures ouvertes doivent être pour le même compte. Pour plus d'informations, reportez-vous aux étapes 7 et 8 de la procédure de cette rubrique.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Pour examiner ou lettrer les paiements après le lettrage automatique
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuilles rapprochement bancaire**, puis sélectionnez le lien associé.
2. Ouvrez la feuille de rapprochement de paiement pour un compte bancaire pour lequel vous souhaitez rapprocher les paiements. Pour plus d'informations, reportez-vous à [Procédure : rapprocher les paiements à l'aide de l'application automatique](receivables-how-reconcile-payments-auto-application.md).
3. Dans la fenêtre **Feuille rapprochement bancaire**, sélectionnez un paiement que vous souhaitez réviser ou lettrer manuellement à une ou plusieurs écritures ouvertes, puis sélectionnez l'action **Lettrer manuellement**.
4. Cochez la case **Lettré** sur la ligne de l'écriture ouverte à laquelle vous voulez lettrer le paiement.
5. Le montant du paiement, qui est également indiqué dans le champ **Montant transaction** de la fenêtre **Lettrage paiement** est inséré dans le champ **Montant lettré**, mais vous pouvez modifier la valeur du champ, par exemple si vous souhaitez lettrer le montant à plusieurs écritures ouvertes.
6. Pour lettrer une partie du montant payé à une autre écriture ouverte pour le compte, par exemple pour lettrer un paiement forfaitaire, cochez la case **Lettré** pour la ligne. Le montant appliqué est automatiquement déduit du montant des transactions pour refléter la répartition sur les écritures ouvertes.
7. Pour lettrer une partie d'un paiement à une ou plusieurs écritures ouvertes qui n'existent pas dans la base de données, créez une ligne sous la ligne pour le même compte. Dans le champ **Montant lettré**, entrez le montant à lettrer sur la nouvelle ligne, puis ajustez la valeur du champ **Montant lettré** de la ligne existante.
8. Répétez les étapes 5, 6 ou 7 pour les autres écritures ouvertes auxquelles vous souhaitez lettrer un paiement complet ou partiel.
9. Lorsque vous avez révisé un lettrage de paiement ou lettré manuellement une ou plusieurs écritures ouvertes, sélectionnez l'action **Accepter le lettrage**.

La fenêtre **Lettrage paiement** se ferme puis, dans la fenêtre **Feuille rapprochement bancaire**, la valeur du champ **Fiabilité correspondance** est modifiée et définie sur **Accepté** pour vous indiquer que vous avez révisé ou lettré manuellement le paiement.

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

