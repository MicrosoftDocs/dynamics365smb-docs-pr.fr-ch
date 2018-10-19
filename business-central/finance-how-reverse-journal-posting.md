---
title: "Annuler une validation en validant une écriture opposée| Microsoft Docs"
description: "Si vous avez effectué une validation erronée dans la feuille comptabilité, vous pouvez utiliser la fonction de contrepassation de transaction pour annuler la validation avec une piste d'audit correcte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: beed335b93ef9211e4fc53c25f97b3fed6137348
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="reverse-postings"></a>Inversion d'une validation
Pour annuler une validation feuille erronée, sélectionnez l'écriture et créez une écriture inverse (écritures identiques aux écritures originales mais avec le signe opposé) portant les mêmes numéro de document et date comptabilisation que l'écriture d'origine. Une fois l'écriture contrepassée, créez l'écriture correcte.

Vous pouvez uniquement inverser les écritures validées à partir d'une ligne feuille comptabilité. Une écriture ne peut être contrepassée qu'une fois.

Pour plus d'informations sur la validation d'une feuille comptabilité, voir [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).

Si vous avez effectué une validation de quantité négative incorrecte, comme une commande achat avec, par exemple, un nombre d'articles incorrect et que vous l'avez validée comme étant reçue (mais non facturée), vous pouvez annuler cette validation.

Si vous avez effectué une validation de quantité positive incorrecte, comme une commande retour achat avec, par exemple, un nombre d'articles incorrect et que vous l'avez validée comme étant livrée (mais non facturée), vous pouvez annuler cette validation.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pour contrepasser la validation feuille d'une écriture comptable
Vous pouvez inverser des écritures dans toutes les fenêtres **Écritures comptables**. La procédure suivante se base dans la fenêtre **Écritures comptables**.
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures comptables**, puis sélectionnez le lien associé.
2. Sélectionnez l'écriture à contrepasser, puis cliquez sur l'action **Contrepasser la transaction**. Notez que cela doit être émis depuis une validation feuille.
3. Dans la fenêtre **Contrepasser les écritures de transaction**, sélectionnez l'écriture voulue, puis sélectionnez l'action **Contrepasser**.
4. Cliquez sur le bouton **Oui** dans le message de confirmation.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Pour annuler une validation de quantité sur une réception d'achat enregistrée  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Réceptions achat enregistrées**, puis sélectionnez le lien associé.  
2.  Ouvrez la réception enregistrée à annuler.  
3.  Sélectionnez la ligne ou les lignes à annuler.  
4.  Choisissez l'action **Annuler réception**.

    Une ligne de correction est insérée sous la ligne de la réception sélectionnée.  

    Si la quantité a été reçue dans une réception entrepôt, une ligne de correction est insérée dans la réception entrepôt enregistrée.  

    Les champs **Quantité reçue** et **Qté reçue non facturée** de la commande achat associée sont remis à zéro.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Pour annuler, puis effectuer à nouveau la validation de quantité sur les expéditions retour enregistrées

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Expéditions retour enreg.**, puis sélectionnez le lien associé.  
2.  Ouvrez l'expédition retour validée à annuler.
3. Sélectionnez la ligne ou les lignes à annuler.  

4.  Choisissez l'action **Annuler expédition retour**.  

    Une ligne de correction est insérée dans le document validé et les champs **Qté retour expédiée** et **Expédition retour non facturée** du retour sont remis à zéro.  

    Retournez à présent au retour achat pour une nouvelle validation.  

5.  Dans la fenêtre **Expédition retour enregistrée**, notez le numéro situé dans le champ **N° retour** .  
6.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Retours achat**, et sélectionnez le lien associé.  
7.  Ouvrez la commande retour concernée, puis sélectionnez l'action **Rouvrir**.  
8.  Corrigez l'écriture dans le champ **Quantité** et publiez à nouveau le retour achat.  

## <a name="to-post-a-negative-entry"></a>Pour valider une écriture négative  
Vous pouvez utiliser le champ **Correction** pour valider un débit négatif au lieu d'un crédit, ou pour valider un crédit négatif au lieu d'un débit sur un compte. Pour répondre aux exigences légales, ce champ est visible par défaut sur toutes les feuilles. Les champs **Montant débit** et **Montant crédit** comprennent l'écriture initiale et l'écriture corrigée. Ces champs n'ont aucune incidence sur le solde du compte.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé  
2.  Dans le champ **Nom de la feuille**, sélectionnez le nom de feuille requis.  
3.  Entrez les informations dans les champs pertinents.  
4.  Dans la ligne feuille que vous souhaitez activer pour les écritures négatives, sélectionnez la case à cocher **Correction**.  
5.  Pour valider la feuille, sélectionnez l'action **Valider**, puis le bouton **Oui**.

## <a name="see-also"></a>Voir aussi
[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

