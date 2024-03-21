---
title: Corriger ou annuler des factures achat impayées (contient une vidéo)
description: Explique comment corriger ou annuler une facture achat validée et créer automatiquement un avoir achat.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Corriger ou annuler des factures achat impayées

Vous pouvez corriger ou annuler une facture achat validée. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si vous souhaitez modifier l’achat assez tôt dans le processus de commande.

Si vous avez déjà payé des produits sur la facture achat validée, vous ne pouvez pas la corriger ni l’annuler à partir de la facture achat validée elle-même. Au lieu de cela, vous devez créer manuellement un avoir achat pour contrepasser l’achat, éventuellement géré à l’aide d’un retour achat. Il en va de même si vous souhaitez modifier une facture achat validée basée sur des réceptions achat combinées. Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md).

Sur la page **Facture achat enregistrée**, vous pouvez cliquer sur le bouton **Corriger** ou **Annuler**. Lorsque vous corrigez ou annulez une facture achat enregistrée, l’avoir achat de correction est appliqué à toutes les écritures comptables de la comptabilité et de l’inventaire créées lors de la validation de la facture achat initiale. Cette action contrepasse la facture achat validée dans vos enregistrements financiers et laisse l’avoir achat validé de correction pour votre piste d’audit. L’utilisation des boutons **Corriger** et **Annuler** est décrite ci-après.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Pour corriger une facture achat validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat validées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à corriger.  

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas corriger la facture achat validée car elle l’a déjà été, ou a été annulée.
3. Sur la page **Facture achat enregistrée** sélectionnez **Corriger**.

    Une nouvelle facture achat avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md). La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l’avoir achat validé qui annule la facture achat validée initiale.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Pour annuler une facture achat validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat validées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à annuler.

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas annuler la facture achat validée car elle l’a déjà été, ou a été corrigée.
3. Sur la page **Facture achat enregistrée** sélectionnez **Annuler**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale. La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l’avoir achat validé qui annule la facture achat validée initiale.

### <a name="partial-invoice-posting-also-supported"></a>Validation partielle de facture également prise en charge

Si l’annulation est liée à une validation de facture partielle, la ligne de commande d’achat d’origine est mise à jour pour refléter la quantité facturée annulée. Les champs **Qté à facturer** et **Qté facturée** de la ligne de commande d’achat associée sont réinitialisés aux valeurs avant l’enregistrement partiel.

## <a name="see-also"></a>Voir aussi

[Achats](purchasing-manage-purchasing.md)  
[Enregistrement des achats](purchasing-how-record-purchases.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
