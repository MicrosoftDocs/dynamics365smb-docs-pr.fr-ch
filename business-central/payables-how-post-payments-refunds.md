---
title: Lettrer des paiements à des documents connexes et les valider| Microsoft Docs
description: Décrit comment enregistrer les paiements effectués aux fournisseurs et les remboursements effectués aux clients.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 353b2074edf80ddba705004e62a86e47943a4366
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916791"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Enregistrer les paiements et remboursements dans la feuille paiement

Sur la page **Feuille paiement** , vous enregistrez les paiements effectués aux fournisseurs et les remboursements effectués aux clients. Lorsque vous validez une ligne feuille paiement, le montant payé est enregistré sur le compte bancaire système spécifié. Vous devez ensuite effectuer des actions pour procéder au transfert d’argent réel à partir du compte bancaire associé.  

La feuille paiement est une feuille comptabilité qui est optimisée pour effectuer les paiements. Vous pouvez rapidement ajouter des lignes manuellement, vous pouvez laisser [!INCLUDE[d365fin](includes/d365fin_md.md)] proposer des paiements fournisseur, et vous pouvez lettrer le paiement dans les documents validés. Bien que vous effectuiez des paiements, vous entrez un montant positif dans le champ **Montant du document** . Selon le type de document de la ligne feuille, ce montant est ensuite converti en montant négatif dans les transactions sous-jacentes. Ainsi, il est plus rapide pour vous avez d’ajouter des lignes feuille manuellement. Si vous préférez saisir des montants négatifs, vous pouvez personnaliser la feuille paiement pour afficher le champ **Montant** à la place.  

- Lettrer des paiements dans des factures ou des avoirs

    Si vous renseignez le champ **N° doc. lettrage** avec la facture ou l’avoir qui doit être payé ou remboursé, le document en question est défini sur Payé lorsque vous validez la feuille. C’est ce qu’on appelle « lettré ». Outre le lettrage lors de la validation du paiement, vous pouvez utiliser la page **Lettrer écritures fournisseur** et **Lettrer écritures client** après avoir validé le paiement. Pou plus d’informations, voir par exemple [Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md).  

- Obtenir des suggestions de paiements aux fournisseurs ou aux salariés

    Les fonctions **Proposer paiements fournisseur** et **Proposer paiements aux salariés** peuvent vous aider à renseigner automatiquement les lignes feuille paiement en fonction de la priorité des fournisseurs et des dates d’échéance. Pour plus d’informations, reportez vous à [Proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md). Avec cette fonction, le champ **N° doc. lettrage** est toujours renseigné.  

- Imprimer des chèques et envoyer des paiements électroniques à votre banque

    Outre l’enregistrement du paiement, vous pouvez également utiliser la page **Feuille paiement** pour générer le paiement à des fins de traitement par votre banque. Pour plus d’informations, voir [Effectuer des paiements par chèque](payables-how-work-checks.md) et [Effectuer des paiements électroniques](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Pour effectuer des paiements dans la feuille paiement

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles paiement** , puis sélectionnez le lien associé.
2. Ouvrez la feuille dédiée aux paiements.
3. Si vous savez qui payer ou rembourser, renseignez les champs manuellement. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Pour lettrer également le paiement à la facture ou l’avoir associé, sélectionnez le champ **N° doc. lettrage** , sur la page **Lettrer écritures fournisseur** , sélectionnez la facture ou l’avoir approprié, puis cliquez sur le bouton **OK** .

    De nombreux champs, tels que **Montant du document** et **Date d’échéance** , sont maintenant renseignés avec les informations du document sélectionné.
5. Sinon, utilisez la fonction **Proposer paiements fournisseur** . Tous les montants et informations de lettrage sont également saisis sur les lignes feuille. Pour plus d’informations, reportez vous à [Proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).

    Les messages vous aident à renseigner correctement les champs obligatoires.
6.  Lorsque toutes les lignes feuille paiement sont renseignées, cliquez sur **Valider** .

## <a name="see-also"></a>Voir aussi
[Effectuer des paiements par chèque](payables-how-work-checks.md)  
[Effectuer des paiements électroniques](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Exporter un fichier Positive Pay](finance-how-positive-pay.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Personnaliser votre espace de travail](ui-personalization-user.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
