---
title: Traiter les retours ou annulations de ventes
description: 'Décrit comment créer un avoir vente pour traiter un retour, annulation, ou un remboursement pour les articles ou les services qui vous ont déjà été payés.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: edupont
---
# <a name="process-sales-returns-or-cancellations"></a><a name="process-sales-returns-or-cancellations"></a>Traiter les retours ou annulations de ventes

Si votre client souhaite retourner des articles ou obtenir un remboursement pour des articles, ou encore annuler des services, que vous lui avez vendus et pour lesquels vous avez reçu un paiement, vous devez créer et valider un avoir vente qui indique la modification demandée. Pour inclure les informations correctes sur la facture vente, vous pouvez procéder comme suit :  

- Créer l’avoir vente directement à partir de la facture vente enregistrée.
- Créer un avoir vente avec les informations copiées de la facture.

Si vous souhaitez davantage de contrôle sur le processus de retour vente, par exemple les documents entrepôt pour la manutention des articles, ou une meilleure vue d’ensemble lors de la réception d’articles à partir de plusieurs documents vente avec un retour vente, vous pouvez créer des retours vente. Un retour vente émet automatiquement l’avoir vente associé et les autres documents relatifs au retour, comme une commande vente de remplacement, le cas échéant. Pour plus de détails, reportez-vous à la rubrique [Traiter les retours vente](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Si une facture vente validée n’a pas encore été payée, vous pouvez utiliser les fonctions **Corriger** ou **Annuler** sur la facture vente validée pour contrepasser automatiquement les transactions associées. Ces fonctions ne fonctionnent que pour les factures impayées, elles ne prennent pas en charge des retours partiels ou les annulations. Pour plus d’informations, voir [Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md).

Un retour ou un remboursement peut en effet se rapporter uniquement à certains des articles ou des services figurant sur la facture vente initiale. Dans ce cas, vous devez modifier les informations des lignes de l’avoir vente ou du retour vente. Lors de la validation de l’avoir vente ou du retour vente, les documents vente affectés par la modification sont contrepassés et un paiement de remboursement peut être créé pour le client. Pour plus d’informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).  

La validation de l’avoir rétablira également tous les frais annexes affectés au document validé, afin que les écritures valeur de l’article soient identiques à celles précédant l’affectation des frais annexes.

> [!NOTE]
> Les aspects comptables des retours de ventes, tels que les paiements aux clients à titre de remboursement, sont considérés comme des travaux comptables et ne sont pas décrits ici. Pour plus d’informations, reportez-vous à [Gestion des comptes fournisseur](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Pour créer un avoir vente à partir d’une facture vente validée

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sur la page **Factures vente enregistrées**, sélectionnez la facture vente validée que vous souhaitez contrepasser, sélectionnez l’action **Annuler**, puis sélectionnez l’action **Créer un avoir correctif**.

    L’en-tête avoir vente affiche des informations sur la facture vente validée. Vous pouvez les modifier, par exemple avec de nouvelles informations qui reflètent l’accord de retour.  
3. Modifiez les informations des lignes en fonction de l’accord, par exemple le nombre d’articles retournés ou du montant à rembourser.
4. Sélectionnez l’action **Préparer**, puis sélectionnez l’action **Lettrer écritures**.
5. Sur la page **Lettrer écritures client**, sélectionnez la ligne contenant le document vente validé auquel vous souhaitez lettrer l’avoir vente, puis sélectionnez l’action **ID lettrage**.

    L’identifiant de l’avoir vente s’affiche dans le champ **ID lettrage**.
6. Dans le champ **Montant à lettrer**, entrez le montant à lettrer s’il est inférieur au montant initial.  

    Au bas de la page **Lettrer écritures client**, vous pouvez afficher le montant total à lettrer pour contrepasser toutes les écritures concernées, à savoir lorsque la valeur du champ **Solde** est égale à zéro.
7. Cliquez sur le bouton **OK**. Lors de la validation de l’avoir vente, il doit être lettré avec les documents vente validés spécifiés.

    Lorsque vous avez créé les lignes avoir vente nécessaires et qu’un ou plusieurs applications sont spécifiées, vous pouvez procéder à la validation de l’avoir vente.  
8. Choisissez l’action **Validation**, puis sélectionnez l’action **Valider et envoyer**.  

La boîte de dialogue **Valider et envoyer la confirmation** s’ouvre et indique le mode d’envoi par défaut du client. Vous pouvez modifier le mode d’envoi en cliquant sur le bouton de recherche pour le champ **Envoyer le document à**. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).  

Les documents vente validés auxquels vous avez lettré l’avoir sont à présent contrepassés, et un remboursement peut être créé pour le client. L’avoir vente est supprimé et remplacé par un nouveau document dans la liste des avoirs vente validés.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Pour créer un avoir vente en copiant une facture vente validée

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs vente**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau** pour ouvrir un nouvel avoir vente vierge.
3. Dans le champ **Nom client**, entrez le nom d’un client existant.
4. Sélectionnez l’action **Préparer**, puis sélectionnez l’action **Copier document**.
5. Sur la page **Extraire document vente**, dans le champ **Type document**, sélectionnez **Facture enregistrée**.
6. Sélectionnez le champ **N° document** pour ouvrir la page **Factures vente validées**, puis sélectionnez l’enregistrement de facture vente validée qui contient les lignes que vous souhaitez contrepasser.
7. Activez la case à cocher **Recalculer lignes** si vous souhaitez que les lignes facture vente validées copiées soient mises à jour avec les modifications apportées au prix article et au coût unitaire depuis la validation de la facture.
8. Cliquez sur le bouton **OK**. Les lignes facture copiées sont insérées dans l’avoir vente.
9. Remplissez l’avoir vente en vous reportant à [Pour créer un avoir vente à partir d’une facture vente validée](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance"></a><a name="to-create-a-sales-allowance"></a>Pour créer des frais de vente
Vous pouvez envoyer un avoir à un client avec une réduction si le client a reçu des articles légèrement endommagés ou avec du retard.  
Vous pouvez valider ce prix réduit en tant que frais annexes dans un avoir ou un retour et l’affecter à l’expédition validée. Ce qui suit décrit la procédure pour un avoir, mais les mêmes étapes s’appliquent à un retour vente.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs vente**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau** pour ouvrir un nouvel avoir vente vierge.
3. Renseignez l’en-tête avoir avec les informations appropriées sur le client à qui vous accordez un rabais sur ventes.  
4. Dans le champ **Type** du raccourci **Lignes**, sélectionnez **Frais annexes**.  
5. Dans le champ **N°**, sélectionnez la valeur de frais annexes appropriée.  
     Vous pouvez créer un numéro frais annexes spécial pour couvrir les rabais sur ventes.  
6. Dans le champ **Quantité**, saisissez **1**.  
7. Dans le champ **Prix unitaire HT**, saisissez le montant du rabais sur ventes.  
8. Affectez les frais de vente en tant que frais annexes aux articles de l’expédition validée. Pour plus d’informations, voir [Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md). Une fois ce rabais affecté, revenez à la page **Avoir vente**.  

Lorsque vous validez la commande retour vente, le rabais sur la vente est ajouté au montant de l’écriture vente appropriée. De cette manière, vous pouvez maintenir la précision de l’évaluation stock.

## <a name="to-combine-return-receipts"></a><a name="to-combine-return-receipts"></a>Pour regrouper des réceptions retour
Vous pouvez regrouper des réceptions retour si votre client retourne plusieurs articles couverts par différentes commandes retour vente.  

Lorsque vous recevez les articles dans votre entrepôt, validez les retours vente comme concernés comme reçus. Cela crée des réceptions retour validées.  

Lorsque vous êtes prêt à facturer ce client, au lieu de facturer chaque commande retour vente séparément, vous pouvez créer un avoir vente et copier automatiquement les lignes réception retour validées dans ce document. Vous pouvez ensuite valider l’avoir et facturer facilement toutes les commandes retour vente ouvertes en même temps.  

Pour regrouper les réceptions retour, activer la case à cocher **Regrouper les B.L.** sur la page **Fiche client**.  

### <a name="to-manually-combine-return-receipts"></a><a name="to-manually-combine-return-receipts"></a>Pour regrouper manuellement des réceptions retour

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire.  
4. Choisissez l’action **Extraire lignes récept. retour**.  
5. Sélectionnez les lignes réception retour à inclure dans l’avoir :  

    - Pour insérer toutes les lignes, sélectionnez-les toutes et sélectionnez le bouton **OK**.  

    - Pour insérer des lignes spécifiques, sélectionnez-les et sélectionnez le bouton **OK**.  
6.  Si une ligne expédition incorrecte a été sélectionnée ou si vous voulez recommencer, supprimez simplement les lignes de l’avoir, puis exécutez de nouveau la fonction **Extraire lignes récept. retour**.  
7.  Validez la facture.  

### <a name="to-automatically-combine-return-receipts"></a><a name="to-automatically-combine-return-receipts"></a>Pour regrouper automatiquement des réceptions retour

Vous pouvez regrouper automatiquement des réceptions retour et avoir la possibilité de valider automatiquement l’avoir à l’aide de la fonction **Regrouper réceptions retour**.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Regrouper réceptions retour**, puis sélectionnez le lien associé.
2. Sur la page **Regrouper réceptions retour**, renseignez les champs pour choisir les réceptions retour appropriées.
3. Cochez la case **Valider avoirs**. Sinon, vous devrez valider manuellement les avoirs achat qui en résulteront.
4. Cliquez sur le bouton **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a><a name="to-remove-a-received-and-invoiced-return-order"></a>Pour supprimer un retour reçu et facturé

Lorsque vous facturez des réceptions retour de cette manière, les commandes retour à partir desquelles les réceptions retour ont été validées continuent à exister, même si elles ont été entièrement reçues et facturées.  

Lorsque des réceptions retour sont regroupées sur un avoir et validées, un avoir vente enregistré est créé pour la ou les lignes créditées. Le champ **Quantité facturée** dans le retour vente d’origine est mis à jour sur la base de la quantité facturée.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Supprimer retours vente facturé**, puis sélectionnez le lien associé.  
2. Dans le champ de filtre **N°**, spécifiez les retours vente à supprimer.  
3. Cliquez sur le bouton **OK**.  

Vous pouvez également supprimer chacune des commandes retour vente manuellement.  

## <a name="inventory-costing"></a><a name="inventory-costing"></a>Évaluation stock

Pour préserver l’évaluation correcte du stock, vous voudrez généralement remettre les articles retournés dans l’inventaire au coût unitaire auquel ils ont été vendus, et non à leur coût unitaire actuel. On appelle cela une inversion de même coût.

Vous pouvez affecter l’inversion de même coût automatiquement de deux façons :  

|Fonction|Description|  
|------------------|---------------------------------------|  
|Fonction**Afficher des lignes document validées à contrepasser** sur la page **Retour vente**|Copie les lignes d’un ou plusieurs documents validés afin de les contrepasser dans le retour vente. Pour plus d’informations, voir la section [Créer un retour vente à partir d’un ou plusieurs documents vente validés](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Fonction**Copier document** des pages **Avoir vente** et **Retour vente**|Copie l’en-tête et les lignes d’un document validé à contrepasser.<br /><br /> Requiert que la case à cocher **Coût retour identique obligatoire** soit sélectionnée sur la page **Paramètres ventes**.|

Pour réaliser manuellement la contrepassation exacte, sélectionnez **Écriture article à lettrer** sur n’importe quelle ligne de document retour, puis sélectionnez le numéro de l’écriture vente initiale. Cela crée un lien entre l’avoir ou le retour vente et l’écriture vente initiale, et garantit que l’article est évalué sur le coût unitaire initial.

Pour plus d’informations, voir [Détails de conception : Évaluation stock](design-details-inventory-costing.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/return-items-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
