---
title: "Lettrer des écritures comptables client pour rapprocher manuellement les paiements client | Microsoft Docs"
description: "Décrit comment lettrer des règlements ou des remboursements client dans une ou plusieurs écritures comptables client ouvertes et rapprocher les paiements client."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ccef6a35b1632bd94f64c5e9ad56ecd3bacbfd06
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-customer-payments-manually"></a>Procédure : rapprocher les paiements client manuellement
Lorsque vous recevez le règlement d'un client ou que vous effectuez un remboursement, vous devez décider si vous souhaitez lettrer le paiement ou le remboursement pour clôturer une ou plusieurs écritures débit ou crédit. Vous pouvez indiquer le montant que vous souhaitez appliquer. Par exemple, vous pouvez appliquer des paiements partiels aux écritures comptables client. La clôture des écritures comptables client permet de garantir que des informations telles que les statistiques clients, les relevés bancaires et les intérêts de retard sont corrects.

> [!NOTE]  
>   Dans la fenêtre **Écritures comptables client**, le rouge signifie que le paiement associé a dépassé sa date d'échéance.

Vous pouvez lettrer les écritures comptables client de plusieurs manières :

* En entrant des informations dans les fenêtres dédiées, telles que la fenêtre **Feuille règlement** et la fenêtre **Feuille rapprochement bancaire**.
* À partir des documents avoir vente.
* À partir des écritures comptables client une fois que les documents vente sont validés mais non lettrés.

> [!NOTE]  
>   Si le champ **Mode de lettrage** de la fiche client contient **Au plus ancien**, les paiements sont automatiquement lettrés avec l'écriture de crédit ouverte la plus ancienne sauf si vous spécifiez une écriture manuellement. Si le mode de lettrage pour un fournisseur est **Manuel**, vous devez toujours lettrer les écritures manuellement.

Vous pouvez lettrer les paiements des clients manuellement dans la fenêtre **Feuille règlement**. La feuille règlement est un type de feuille comptabilité, de sorte que vous pouvez l'utiliser pour valider des transactions sur des comptes généraux, bancaires, client, fournisseur et immobilisations. Vous pouvez lettrer le règlement sur une ou plusieurs écritures débit lorsque vous validez le règlement ou lettrer à partir des écritures validées ultérieurement.

Vous pouvez également lettrer les paiements client et fournisseur dans la fenêtre **Feuille rapprochement bancaire** à l'aide des fonctions dédiées à l'importation de relevés bancaires, le lettrage automatique et le rapprochement bancaire. Pour plus d'informations, reportez-vous à [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md). Sinon, vous pouvez rapprocher les paiements client en fonction de la liste des documents vente échus dans la fenêtre **Enregistrement de paiement**. Pour plus d'informations, reportez-vous à [Procédure : Rapprocher les paiements client dans une liste des documents vente échus](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Pour renseigner et valider une feuille règlement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille règlement**, puis sélectionnez le lien connexe.
2. Sélectionnez **Modifier journal**.
3. Sélectionnez le nom de traitement par lots souhaité dans le champ **Nom de la feuille**.
4. Renseignez le champ **Date comptabilisation**.  
5. Dans le champ **Type document**, sélectionnez **Paiement**.

    Le champ **N° document** contient les souches de numéros affectées au lot.  
6. Utilisez le champ **N° doc. externe** pour stocker un identifiant, tel que le numéro de chèque du client.
7. Dans le champ **Type compte**, sélectionnez **Client**.
8. Dans le champ **N° compte**, sélectionnez le compte général approprié.
9. Si vous souhaitez valider l'application en même temps que la feuille, suivez l'un des exemples ci-dessous.
10. Dans le champ **Type compte contrepartie**, sélectionnez **Compte général** pour les règlements et **Compte bancaire** pour les autres paiements.
11. Dans le champ **N° compte contrepartie**, sélectionnez le compte pour les règlements ou le compte bancaire approprié pour d'autres paiements.
12. Validez la feuille.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Pour lettrer un paiement avec une seule écriture comptable client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille règlement**, puis sélectionnez le lien connexe.
2. Sélectionnez **Modifier journal**.
3. Dans la première ligne feuille, saisissez les informations appropriées sur l'écriture à lettrer.
4. Dans le champ **Type document**, entrez **Paiement**.
5. Dans le champ **Type compte**, entrez **Client**.
6. Dans le champ **Type compte contrepartie**, entrez **Compte bancaire.**
7. Dans le champ **N° doc. lettrage**, sélectionnez le champ permettant d'ouvrir la fenêtre **Lettrer écritures client**.
8. Dans la fenêtre **Lettrer écritures client**, sélectionnez l'écriture à laquelle lettrer le paiement.
9. Dans le champ **Montant à lettrer**, entrez le montant à lettrer à l'écriture. Si vous n'entrez aucun montant, le montant maximal est lettré.

    Au bas de la fenêtre **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
10. Cliquez sur le bouton **OK**. La fenêtre **Feuille règlement** affiche désormais l'écriture que vous avez saisie dans les champs **Type doc. lettrage** et **N° doc. lettrage**.
11. Validez la feuille règlement.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Pour lettrer un paiement avec plusieurs écritures client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille règlement**, puis sélectionnez le lien connexe.
2. Sélectionnez **Modifier journal**.
3. Dans la première ligne feuille, saisissez les informations appropriées sur l'écriture à lettrer.
4. Dans le champ **Type document**, entrez **Paiement**.
5. Dans le champ **Type compte**, entrez **Client**.
6. Dans le champ **Type compte contrepartie**, entrez **Compte bancaire.**
7. Dans le champ **Montant**, entrez le paiement complet sous forme de montant négatif.
8. Pour lettrer le paiement avec plusieurs écritures comptables client lors de la validation, sélectionnez l'action **Lettrer écritures**.  
9. Sélectionnez les lignes correspondant aux écritures avec lesquelles l'écriture lettrage doit être lettrée, puis sélectionnez l'action **Lettrer**.  
10. Sur chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l'écriture. Si vous n'entrez aucun montant, le montant maximal est lettré.

    Au bas de la fenêtre **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
11. Cliquez sur le bouton **OK**.
12. Validez la feuille règlement.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Pour lettrer un avoir avec une seule écriture comptable client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Avoirs vente**, puis sélectionnez le lien connexe.
2. Ouvrez l'avoir vente souhaité.
3. Pour lettrer l'avoir avec une seule écriture comptable client lors de la validation, dans le champ **N° doc. lettrage**, sélectionnez l'écriture avec laquelle lettrer le paiement.
4. Sur la ligne du champ **Montant à lettrer**, entrez le montant à lettrer avec l'écriture.  

    Si vous n'entrez aucun montant, le programme lettre automatiquement le montant maximal. Au bas de la fenêtre **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.    
5. Cliquez sur le bouton **OK**. La fenêtre **Avoir vente** affiche désormais l'écriture que vous avez saisie dans les champs **Type doc. lettrage** et **N° doc. lettrage**. Et le montant de l'avoir à valider, escomptes éventuels déduits.
6. Valider l'avoir.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Pour lettrer un avoir avec plusieurs écritures comptables client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Avoirs vente**, puis sélectionnez le lien connexe.
2. Ouvrez l'avoir vente souhaité.
3. Pour lettrer l'avoir avec plusieurs écritures comptables client lors de la validation, sélectionnez l'action **Lettrer écritures**.
4. Sélectionnez les lignes correspondant aux écritures avec lesquelles l'écriture lettrage doit être lettrée, puis sélectionnez l'action **Lettrer**.
5. Sur chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l'écriture. Si vous n'entrez aucun montant, le montant maximal est lettré.  

    Au bas de la fenêtre **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
6. Cliquez sur le bouton **OK**. La fenêtre **Avoir vente** affiche désormais le montant de l'avoir à valider, escomptes éventuels déduits.
7. Valider l'avoir.

## <a name="to-apply-posted-customer-ledger-entries"></a>Pour lettrer des écritures comptables client validées
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche du client possédant les écritures que vous souhaitez lettrer.
3. Sélectionnez l'action **Écritures comptables**, puis sélectionnez la ligne où figure l'écriture qui sera l'écriture lettrage.
4. Sélectionnez l'action **Lettrer écritures**. La fenêtre **Lettrer écritures client** s'ouvre et affiche les écritures ouvertes de ce client.
5. Sélectionnez les lignes correspondant aux écritures avec lesquelles l'écriture lettrage doit être lettrée, puis sélectionnez l'action **Lettrer** .
6. Pour chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l'écriture. Si vous n'entrez aucun montant, le montant maximal est lettré.  

    Au bas de la fenêtre **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré**.  
7. Sélectionnez l'action **Valider le lettrage**. La fenêtre **Valider le lettrage** s'ouvre et affiche le numéro de document de l'écriture lettrage et la date comptabilisation de l'écriture ayant la date comptabilisation la plus récente.  
8. Cliquez sur **OK** pour valider le lettrage.

    Si le lettrage validé génère des écritures comptables client lettrées, ces écritures comptables ne sont plus activées dans le champ **Ouvert**.    
9. Pour afficher les écritures comptables, choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe. Accédez à la fiche du client approprié pour afficher les écritures comptables.  

Dans la liste écritures comptables, sur la ligne contenant l'écriture comptable totalement lettrée vous constatez que la case **Ouvert** n'est pas cochée.  

> [!NOTE]  
>   Une fois que vous avez sélectionné une écriture de la fenêtre **Lettrer écritures client**, ou plusieurs écritures avec l'**ID lettrage**, le champ **Montant lettré** de la ligne feuille contient la somme des montants restants des écritures validées que vous avez sélectionnées, cela à moins que le champ ne soit déjà renseigné. Si vous sélectionnez **Au plus ancien** dans le champ **Mode de lettrage** sur la fiche client, le lettrage intervient automatiquement.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Pour lettrer des écritures comptables client avec d'autres écritures dans différentes devises
Si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez toujours lettrer la facture avec le paiement.  

Si vous lettrez une écriture (Écriture 1) dans une devise avec une autre écriture (Écriture 2) dont la devise est différente, la date de comptabilisation de l'Écriture 1 est utilisée pour trouver le taux de change adéquat et convertir les montants de l'Écriture 2. Le taux de change approprié se trouve dans la fenêtre **Taux de change devise**.  

Le lettrage d'écritures comptables client en devises différentes doit être activé. Pour en savoir plus, voir [Procédure : activer le lettrage d'écritures comptables client en devises différentes](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille règlement**, puis sélectionnez le lien connexe.
2. Ouvrez la feuille que vous souhaitez, puis renseignez la première ligne vide de la feuille à l'aide d'un code devise.
3. Sélectionnez l'action **Lettrer écritures**.
4. Sélectionnez la ligne comportant l'écriture à lettrer avec l'écriture de la feuille règlement. Sélectionnez ensuite l'action **Lettrer**, puis sélectionnez l'écriture sur laquelle le lettrage doit être effectué.
5. Cliquez sur le bouton **OK** pour revenir à la feuille règlement.
6. Validez la feuille ventes.  

> [!IMPORTANT]  
>   Lorsque vous lettrez des écritures en devises différentes, les écritures sont converties en USD. Bien que le taux de change des deux devises concernées soit fixe, comme entre le USD et l'EUR, leur conversion en USD peut donner un petit montant résiduel. Le programme valide ces petits montants résiduels en tant que gains et pertes dans le compte défini dans les champs **Cpte gains constatés report** ou **Cpte pertes constatées report** de la fenêtre **Devises**. La valeur du champ **Montant (USD)** est également ajustée sur les écritures comptables fournisseur.  

## <a name="to-correct-an-application-of-customer-entries"></a>Pour créer un lettrage des écritures client
Lorsque vous corrigez une application, des écritures de correction (écritures identiques à l'écriture originale mais avec le signe opposé dans le champ du montant) sont créées et validées pour toutes les écritures comportant des validations comptables issues du lettrage, comme les escomptes et les pertes et gains en devise. Les écritures qui sont fermées par l'application sont rouvertes.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche client appropriée.
3. Sélectionnez l'action **Écritures comptables**.
4. Sélectionnez l'écriture comptable appropriée, puis sélectionnez l'action **Délettrer les écritures**.
5. Sinon, sélectionnez l'action **Écritures comptables détaillées**.
6. Sélectionnez l'écriture de lettrage appropriée, puis sélectionnez l'action **Délettrer les écritures**.
7. Renseignez les champs de l'en-tête, puis sélectionnez l'action **Délettrer**.  

> [!IMPORTANT]  
>   Si une écriture a été lettrée par plusieurs écritures lettrage, vous devez commencer par délettrer la dernière écriture lettrage.  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

