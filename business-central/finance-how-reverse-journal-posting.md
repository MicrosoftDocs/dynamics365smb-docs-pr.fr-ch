---
title: Annuler une validation en validant une écriture opposée
description: 'Si vous trouvez une erreur dans une feuille comptabilité validée, vous pouvez utiliser l’action de contrepassation de transaction pour annuler la validation avec une piste d’audit correcte.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a><a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Contrepasser une validation feuille et annuler les réceptions/envois

La contrepassation des validations feuille est utile, par exemple, pour corriger les erreurs et pour effacer une ancienne écriture de régularisation avant d’en saisir une nouvelle. Une écriture contrepassée est identique à l’entrée d’origine, mais a un signe opposé dans le champ **Montant**. L’écriture contrepassée doit avoir le même numéro de document et la même date de publication que l’entrée d’origine. Une fois l’écriture contrepassée, créez l’écriture correcte.

Vous pouvez uniquement inverser les écritures validées à partir d’une ligne feuille comptabilité. Une écriture ne peut être contrepassée qu’une fois.

Pour annuler un accusé de réception ou un envoi d’expédition, vous pouvez utiliser la fonction **Annuler** sur le document validé. Vous pouvez annuler des quantités de type **Article** et **Ressource**.

Si vous avez effectué une validation de quantité négative incorrecte, comme une commande achat avec, par exemple, un nombre d’articles incorrect et que vous l’avez validée comme étant reçue (mais non facturée), vous pouvez annuler cette validation.

Si vous avez effectué une validation de quantité positive incorrecte, comme une expédition vente ou une expédition retour achat avec un nombre d’articles incorrect et que vous l’avez validée comme étant livrée (mais non facturée), vous pouvez annuler cette validation.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pour contrepasser la validation feuille d’une écriture comptable

Vous pouvez inverser des écritures sur toutes les pages **Écritures comptables**. La procédure suivante se base sur la page **Écritures comptables**.

> [!NOTE]
> L’écriture doit être émise depuis une validation feuille.
>
> En outre, vous ne pouvez pas contrepasser des écritures qui ont été validées avec des informations provenant d’un travail ou qui présentent des gains et pertes réalisés au sein de la même transaction.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures comptables**, puis sélectionnez le lien associé.
2. Sélectionnez l’écriture à contrepasser, puis cliquez sur l’action **Contrepasser la transaction**.
3. Sur la page **Contrepasser les écritures de transaction**, choisissez l’action **Contrepasser**.
4. Cliquez sur **Oui** pour confirmer la contrepassation.

## <a name="to-post-a-negative-entry"></a><a name="to-post-a-negative-entry"></a>Pour valider une écriture négative

Utilisez le champ **Correction** pour valider un débit négatif au lieu d’un crédit, ou pour valider un crédit négatif au lieu d’un débit sur un compte. Par défaut, le champ est disponible dans toutes les feuilles. Les champs **Montant débit** et **Montant crédit** comprennent l’écriture initiale et l’écriture corrigée. Ces champs n’ont aucune incidence sur le solde du compte.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilité**, puis choisissez le lien associé.  
2. Dans le champ **Nom de la feuille**, sélectionnez le nom de feuille requis.  
3. Entrez les informations dans les champs pertinents.  
4. Dans la ligne feuille que vous souhaitez activer pour les écritures négatives, sélectionnez la case à cocher **Correction**.  
5. Pour valider la feuille, sélectionnez l’action **Valider**, puis le bouton **Oui**.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a><a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a>Pour annuler une validation de quantité sur une réception d’achat enregistrée

Les étapes suivantes décrivent comment annuler une réception validée d’articles ou de ressources est décrite ci-après. La procédure est identique pour des livraison validées.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réceptions achat enregistrées**, puis sélectionnez le lien associé.  
2. Ouvrez la réception enregistrée à annuler.  
3. Sélectionnez la ligne ou les lignes à annuler.  
4. Choisissez l’action **Annuler réception**.

Une ligne de correction est ajoutée sous la ligne de la réception sélectionnée. Si la quantité a été reçue dans une réception entrepôt, une ligne de correction est ajoutée sur la réception entrepôt validée.  

Les champs **Quantité reçue** et **Qté reçue non facturée** de la commande achat associée sont remis à zéro.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Pour annuler, puis effectuer à nouveau la validation de quantité sur les expéditions retour enregistrées

Les étapes suivantes décrivent comment :

* Annuler une expédition de retour d’articles ou de ressources validée.
* Reportez à nouveau le retour sur achat avec une nouvelle quantité.

La procédure est identique pour les réceptions retour enregistrées.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expéditions retour enreg.**, puis sélectionnez le lien associé.  
2. Ouvrez l’expédition retour validée à annuler.
3. Sélectionnez la ligne ou les lignes à annuler.  

4. Choisissez l’action **Annuler expédition retour**.  

    Une ligne de correction est insérée dans le document validé et les champs **Qté retour expédiée** et **Expédition retour non facturée** du retour sont remis à zéro.  

    Retournez à présent au retour achat pour une nouvelle validation.  

5. Sur la page **Expédition retour enregistrée**, notez le numéro situé dans le champ **N° retour** .  
6. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Retours achat**, puis sélectionnez le lien associé.  
7. Ouvrez la commande retour concernée, puis sélectionnez l’action **Rouvrir**.  
8. Corrigez l’écriture dans le champ **Quantité** et publiez à nouveau le retour achat.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Annuler la validation d’assemblage](assembly-how-to-undo-assembly-posting.md)  
[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
