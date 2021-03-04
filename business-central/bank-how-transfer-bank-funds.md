---
title: Transférer des fonds à la banque| Microsoft Docs
description: Vous pouvez transférer des montants d’un compte bancaire à un autre, y compris dans différentes devises, en validant la transaction dans la feuille comptabilité.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 934124d419e19c1dc8180f11fcae748cd2afd15d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752370"
---
# <a name="transfer-bank-funds"></a>Transfert de fonds à la banque
Il peut vous arriver de devoir transférer un montant d’un compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] vers un autre. Pour ce faire, vous devez valider une transaction sur la page **Feuille comptabilité**. La tâche varie selon que les comptes bancaires utilisent la même devise ou des devises différentes.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Pour valider un transfert entre comptes bancaires avec le même code devise
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilité**, puis sélectionnez le lien associé.
2. Dans une ligne feuille, renseignez les champs **Date comptabilisation** et **N° document** .
3. Cliquez sur le champ **Type compte**, sélectionnez le **Compte bancaire**.
4. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
5. Dans le champ **Montant**, entrez le total à transférer.
6. Choisissez l’action **Afficher plus de colonnes** pour afficher tous les champs disponibles.
7. Dans le champ **Type compte contrepartie**, sélectionnez **Compte bancaire**.
8. Dans le champ **N° compte contrepartie**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
9. Validez la feuille.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Pour valider des transferts entre comptes bancaires dotés de codes devise différents
Pour transférer des fonds entre des comptes bancaires qui utilisent des devises différentes, vous devez valider deux lignes feuille comptabilité.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilité**, puis sélectionnez le lien associé.
2. Créez deux lignes feuille, et renseignez les champs **Date comptabilisation** et **N° document**.
3. Sur la première ligne feuille, dans le champ **Type**, sélectionnez **Compte bancaire**.
4. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
5. Dans le champ **Montant**, saisissez le montant dans la devise du compte bancaire. Entrez les montants de crédit précédés du signe moins. Entrez les montants de débit sans signe moins.
6. Dans le champ **Type compte contrepartie**, sélectionnez **Compte bancaire**.
7. Dans le champ **N° compte contrepartie**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
8. Sur la seconde ligne feuille, dans le champ **Type**, sélectionnez **Compte bancaire**.
9. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
10. Dans le champ **Montant**, saisissez le montant dans la devise du compte bancaire. Entrez les montants de crédit précédés du signe moins. Entrez les montants de débit sans signe moins.
11. Dans le champ **Type compte contrepartie**, sélectionnez **Compte bancaire**.  
12. Dans le champ **N° compte contrepartie**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.

    > [!NOTE]  
    > Si les taux de change utilisés dans la feuille sont différents des taux de change qui s’affichent sur la page **Taux de change devise**, entrez alors une troisième ligne pour les pertes ou gains liés au taux de change. Entrez **Compte général** dans le champ **Type compte**. Entrez le numéro de compte général pour les gains ou les pertes liés au taux de change dans le champ **N° compte**. Saisissez les gains ou les pertes liés au taux de change dans le champ **Montant** avec ou sans signe moins pour les crédits et les débits, respectivement.
13. Validez la feuille.

## <a name="see-also"></a>Voir aussi
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]