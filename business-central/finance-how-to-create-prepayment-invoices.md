---
title: Créer des factures d’acompte
description: 'Traitez les situations où votre fournisseur ou vous-même exigez un acompte. Utilisez les pourcentages par défaut pour chaque ligne vente ou achat, ou ajustez le montant en fonction si nécessaire.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 10/04/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a>Créer des factures d’acompte

Si vous demandez aux clients de payer avant d’expédier leur commande, vous pouvez utiliser les fonctionnalités de prépaiement. Il en va de même si votre fournisseur vous demande de paiement avant de vous expédier une commande.  

Vous pouvez lancer le traitement de l’acompte lorsque vous créez une commande vente ou achat. Le pourcentage acompte par défaut pour un article donné sur la commande, ou pour le client ou le fournisseur, sera automatiquement inclus dans la facture acompte résultante. Vous pouvez également spécifier un pourcentage acompte pour l’ensemble du document.

Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte. Utilisez les pourcentages par défaut pour chaque ligne vente ou achat, ou ajustez le montant en fonction si nécessaire. Par exemple, vous pouvez spécifier un montant total pour la commande entière.  

La procédure suivante décrit comment facturer un acompte pour une commande vente. La procédure est identique pour des commandes achat.  

## <a name="to-create-a-prepayment-invoice"></a>Pour créer une facture acompte

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Créez une commande vente pour le client approprié. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  

    Sur le raccourci **Acompte**, le champ **% acompte** spécifie le pourcentage à utiliser pour calculer le montant acompte. Si un pourcentage d’acompte par défaut figure sur la fiche client, le champ est renseigné automatiquement. Vous pouvez modifier le pourcentage. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Choisissez le champ **Compresser acompte** si vous souhaitez créer des lignes sur la facture d’acompte qui combinent des lignes de la commande client si :  

    - Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.  
    - Elles sont les mêmes dimensions.  

    Si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d’acompte est associé, alors ne choisissez pas le champ **Compresser acompte**.  

    La date d’échéance de l’acompte est calculée automatiquement en fonction de la valeur du **Code conditions paiement acompte**.

    > [!NOTE]
    > Lorsque certaines lignes d’une facture nécessitent un acompte de 100 % et d’autres non, et qu’il y a de la TVA sur le compte d’acompte, le montant arrondi peut entraîner une erreur lorsque vous créez une facture d’acompte. L’erreur se produit car le montant de la facture d’acompte est supérieur aux montants des lignes du document. Pour résoudre le problème, modifiez les montants d’une ou de toutes les lignes nécessitant un acompte de 100 %. Le changement recalculera l’arrondi du montant de la TVA et utilisera la différence d’arrondi cumulée sur la dernière ligne modifiée.
    >
    > Deux autres façons de résoudre le problème sont les suivantes :
    >
    > * Créez un groupe comptabilisation produit TVA et des paramètres comptabilisation TVA distincts avec un identifiant de TVA distinct, et utilisez-les pour les articles ou les lignes qui nécessitent un acompte de 100 %. L’arrondi est effectué pour chaque identifiant de TVA, de sorte qu’un arrondi séparé sera effectué pour les articles affectés au groupe comptabilisation produit TVA.
    > * Utilisez une facture distincte pour les articles ou les lignes nécessitant ou non des acomptes à 100 %.

3. Renseignez les lignes vente.  

    Si vous avez spécifié un pourcentage acompte par défaut soit pour le client, soit sur le raccourci **Acompte** sur ce document, cette valeur est copiée sur chaque ligne. Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.  

    > [!TIP]
    > Si vous ne voyez pas le champ **% acompte**, vous pouvez l’ajouter via la personnalisation.  Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

4. Pour visualiser le montant d’acompte total, choisissez l’action **Statistiques**.

    Pour ajuster le montant d’acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la page **Statistiques commande vente**.  

    Si le champ **Prix TVA comprise** est sélectionné, le champ **Montant acompte TTC** est modifiable.  

    Si vous modifiez la valeur du champ **Montant acompte**, le montant est réparti de façon proportionnelle entre toutes les lignes, à l’exception de celles qui contiennent la valeur **0** dans le champ **% acompte**.  

5. Pour effectuer une impression test avant de valider la facture d’acompte, sélectionnez l’action **Acompte**, puis choisissez **Impression test acompte**.  
6. Pour valider la facture d’acompte, sélectionnez l’action **Acompte**, puis l’action **Valider facture acompte**.  

    Pour valider et imprimer la facture acompte, choisissez l’action **Valider et imprimer facture acompte**.  

Vous pouvez émettre des factures acompte supplémentaires pour la commande. Pour émettre une autre facture, augmentez le montant d’acompte sur une ou plusieurs lignes, ajustez la date document si nécessaire, puis validez la facture acompte. Une nouvelle facture est créée pour la différence entre les montants d’acompte facturés et le nouveau montant d’acompte.  

> [!NOTE]  
> Si vous êtes situé en Amérique du Nord, vous ne pouvez pas modifier le pourcentage d’acompte après la facture acompte validée. Cela est empêché dans la version nord\-américaine de [!INCLUDE[prod_short](includes/prod_short.md)], car le calcul de la taxe sur les ventes est sinon incorrect.  

 Lorsque vous êtes prêt à valider le reste de la facture, validez-le comme n’importe quelle facture. Le montant d’acompte est automatiquement déduit du montant dû.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Mettre à jour automatiquement le statut des commandes prépayées et des factures

Vous pouvez accélérer le traitement des commandes et des factures en configurant des entrées de file d’attente qui mettent automatiquement à jour le statut de ces documents. Lorsqu’une facture d’acompte est payée, les entrées de la file d’attente des travaux peuvent changer automatiquement le statut du document de **Acompte en attente** sur **Validé**. Lorsque vous configurez les entrées de la file d’attente des travaux, les unités de code que vous devrez utiliser sont **384 Mise à jour En attente Acompte Ventes** et **384 Mise à jour En attente Acompte Achats**. Nous vous recommandons de programmer les entrées pour qu’elles s’exécutent fréquemment, par exemple, toutes les minutes. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Voir aussi

[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d’acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Personnaliser votre espace de travail](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
