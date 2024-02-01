---
title: Traiter les retours ou annulations
description: Explique comment créer et valider un avoir achat lorsque vous souhaitez retourner des articles à un fournisseur ou annuler des services achetés.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cancel, undo, correct'
ms.search.form: '6640, 6643, 9307, 9309, 9308, 6652, 145, 147'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="process-purchase-returns-or-cancellations"></a>Traiter les retours ou annulations d’achats

Si vous souhaitez retourner des articles à votre fournisseur ou annuler des services que vous avez achetés, vous pouvez créer et valider un avoir achat qui indique la modification demandée par rapport à la facture achat d’origine. Pour inclure les informations de facture achat correctes, vous pouvez créer l’avoir achat à partir de la facture achat enregistrée ou vous pouvez créer un avoir achat avec les informations copiées de la facture.

Si vous souhaitez davantage de contrôle sur le processus de retour achat, par exemple les documents entrepôt pour la manutention des articles ou une meilleure vue d’ensemble lors de la réexpédition d’articles à partir de plusieurs documents achat avec un retour achat, vous pouvez créer des retours achat. Un retour achat émet automatiquement l’avoir achat associé. Pour plus d’informations, voir la section [Pour créer un retour achat à partir d’un ou plusieurs documents achat validés](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Si une facture achat validée n’a pas encore été payée, vous pouvez utiliser les fonctions de **Corriger** ou **Annuler** sur la facture achat validée pour contrepasser automatiquement les transactions associées. Ces fonctions ne fonctionnent que pour les factures impayées, elles ne prennent pas en charge des retours partiels ou les annulations. Vous ne pouvez pas non plus corriger ou annuler les factures achat qui ont été validées avec les reçus de plusieurs commandes achat. Pour plus d’informations, voir [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Généralement, vous pouvez créer un avoir achat ou un retour achat en réaction à un avoir que vous a envoyé un fournisseur. L’avoir achat ou le retour achat tient lieu de documentation interne du processus d’avoir aux fins de comptabilité ou pour contrôler l’expédition des articles concernés.

La modification peut concerner tous les produits figurant sur la facture achat d’origine, ou uniquement certains d’entre eux. Par conséquent, vous pouvez partiellement renvoyer les articles reçus ou demander le remboursement partiel des services reçus. Dans ce cas, vous devez modifier les informations des lignes de l’avoir achat ou du retour achat.

Outre la facture achat validée d’origine, vous pouvez lettrer l’avoir achat ou le retour achat à d’autres documents achat, par exemple une autre facture achat validée, parce que vous renvoyez également des articles livrés avec cette facture.

La validation de l’avoir rétablira également tous les frais annexes affectés au document validé, afin que les écritures valeur de l’article soient identiques à celles précédant l’affectation des frais annexes.

## <a name="inventory-costing"></a>Évaluation stock
Pour préserver l’évaluation correcte du stock, vous voudrez généralement prélever les articles retournés dans l’inventaire au coût unitaire auquel ils ont été achetés, et non à leur coût unitaire actuel. On appelle cela une inversion de même coût.

Vous pouvez affecter l’inversion de même coût automatiquement de deux façons.  

|Fonction|Désignation|  
|------------------|---------------------------------------|  
|Fonction **Afficher des lignes document validées à contrepasser** sur la page **Retour commande achat**|Copie les lignes d’un ou plusieurs documents validés afin de les contrepasser dans le retour achat. Pour plus d’informations, voir la section [Pour créer un retour achat à partir d’un ou plusieurs documents achat validés](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|Fonction **Copier à partir du document** des pages **Avoir achat** et **Retour achat**|Copie l’en-tête et les lignes d’un document validé à contrepasser.<br /><br /> Requiert que la case à cocher **Coût retour identique obligatoire** soit sélectionnée sur la page **Paramètres achats**.|

Pour réaliser manuellement la contrepassation exacte, sélectionnez **Écriture article à lettrer** sur n’importe quelle ligne de document retour, puis sélectionnez le numéro de l’écriture achat initiale. Cela crée un lien entre l’avoir achat ou le retour achat et l’écriture achat initiale, et garantit que l’article est évalué sur le coût unitaire initial.

Pour plus d’informations, voir [Détails de conception : Évaluation stock](design-details-inventory-costing.md).

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Pour créer un avoir achat à partir d’une facture achat validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat validées**, puis sélectionnez le lien associé.  
2. Sur la page **Factures achat enregistrées**, sélectionnez la facture achat validée que vous souhaitez contrepasser, puis sélectionnez l’action **Créer un avoir correctif**.

    La plupart des champs de l’en-tête de l’avoir achat sont renseignés avec les informations de la facture achat validée. Vous pouvez modifier tous les champs, par exemple avec de nouvelles informations qui reflètent l’accord de retour.
3. Modifiez les informations des lignes en fonction de l’accord, par exemple le nombre d’articles retournés ou du montant à rembourser.
4. Sélectionnez l’action **Lettrer écritures**.
5. Sur la page **Lettrer écritures fournisseur**, sélectionnez la ligne contenant le document achat validé auquel vous souhaitez lettrer l’avoir achat, puis sélectionnez l’action **ID lettrage**. Le numéro de l’avoir achat est inséré dans le champ **ID lettrage**.
6. Dans le champ **Montant à lettrer**, entrez le montant à lettrer s’il est inférieur au montant initial.

    Au bas de la page **Lettrer écritures fournisseur**, vous pouvez afficher le montant total à lettrer pour contrepasser toutes les écritures concernées, à savoir lorsque la valeur du champ **Solde** est égale à zéro.
7. Cliquez sur le bouton **OK**. Lorsque vous validez l’avoir achat, il est lettré avec les documents achat validés spécifiés.

    Lorsque vous avez créé ou modifié les lignes avoir achat nécessaires et qu’une ou plusieurs applications sont spécifiées, vous pouvez procéder à la validation de l’avoir achat.
8. Sélectionnez l’action **Valider**.

Les factures achat validées auxquelles vous appliquez l’avoir sont à présent contrepassées. Si vous avez déjà payé la facture initiale, le fournisseur doit maintenant rembourser le paiement en votre faveur. Si l’avoir est uniquement pour une partie du produit dans la facture initiale, vous pouvez payer uniquement le montant restant de la facture achat d’origine pour la clôturer.

L’avoir achat est supprimé et remplacé par un nouveau document dans la liste des avoirs achat validés.

## <a name="to-create-a-purchase-credit-memo-by-copying-a-posted-purchase-invoice"></a>Pour créer un avoir achat en copiant une facture achat validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs achat**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau** pour ouvrir un nouvel avoir achat vierge.
3. Dans le champ **Fournisseur**, entrez le nom d’un fournisseur existant.
4. Sélectionnez l’action **Copier à partir du document**.
5. Sur la page **Extraire document achat**, dans le champ **Type document**, sélectionnez **Facture enregistrée**.
6. Sélectionnez le champ **N° document** pour ouvrir la page **Factures achat validées**, puis sélectionnez la facture achat validée qui contient les lignes que vous souhaitez contrepasser.
7. Activez la case à cocher **Recalculer lignes** si vous souhaitez que les lignes facture achat validées copiées soient mises à jour avec les modifications apportées au prix article et au coût unitaire depuis la validation de la facture.
8. Cliquez sur le bouton **OK**. Les lignes facture copiées sont insérées dans l’avoir achat.
9. Remplissez l’avoir achat en vous reportant à [Pour créer un avoir achat à partir d’une facture achat validée](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## <a name="to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents"></a>Pour créer un retour achat à partir d’un ou plusieurs documents achat validés

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Retours achat**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs dans le raccourci **Général** selon les besoins.
4. Dans le raccourci **Lignes**, renseignez les lignes manuellement, ou copiez des informations d’autres documents pour renseigner les lignes automatiquement :

    - utiliser la fonction  **Extraire lignes document enreg. à contrepasser** pour copier une ou plusieurs lignes de document validées à partir d’un ou plusieurs documents validés. Cette fonction inverse toujours exactement les coûts à partir de la ligne de document validée. Cette fonction est décrite dans les étapes suivantes.    
    - Utilisez la fonction **Copier à partir du document** pour copier un document existant dans le retour. Cette fonction permet de copier l’ensemble du document. Il peut s’agir d’un document validé ou d’un document non encore validé. Cette fonction ne permet l’inversion de même coût que lorsque la case **Inversion de même coût obligatoire** est cochée sur la page **Paramètres ventes**.  

5. Sélectionnez l’action **Afficher des lignes document validées à contrepasser**.
6. Dans le haut de la page **Lignes document achat enreg.**, cochez la case **Afficher uniquement lignes réversibles** si vous voulez n’afficher que les lignes contenant des quantités qui n’ont pas encore été retournées, ou s’il s’agit de lignes achat, vendues ou consommées. Par exemple, si une quantité de facture achat validée a déjà été retournée, il se peut que vous ne vouliez pas intégrer cette quantité dans un nouveau document retour achat.

    > [!NOTE]  
    >  Ce champ ne fonctionne que pour les lignes réception validées et les lignes facture validées, pas pour les lignes retour validées ni les lignes avoir validées.  

    Dans la partie gauche de la page, les différents types de document sont énumérés, et le nombre entre parenthèses est le nombre de documents disponibles de chaque type de document.

7. Dans le champ **Filtre de type de document**, sélectionnez le type de lignes document validées que vous souhaitez utiliser.  
8. Sélectionnez les lignes que vous voulez copier vers le nouveau document.  

    > [!NOTE]  
    >  Si vous utilisez <kbd>Ctrl</kbd>+<kbd>A</kbd> pour sélectionner toutes les lignes, toutes les lignes à l’intérieur du filtre que vous avez défini sont copiées mais le filtre **Afficher uniquement quantité réversible** n’est pas pris en considération. Par exemple, supposons que vous ayez filtré les lignes pour un numéro de document particulier comportant deux lignes, dont l’une a déjà été retournée. Même si le champ **Afficher uniquement quantité réversible** est sélectionné, si vous sélectionnez <kbd>Ctrl</kbd>+<kbd>A</kbd> pour copier toutes les lignes, deux lignes sont copiées au lieu de celle qui n’a pas encore été contrepassée.  

9. Sélectionnez le bouton **OK** pour copier les lignes dans le nouveau document.  

    Les traitements suivants se produisent :  

    - Pour les lignes document validées du type **Article**, une ligne document est créée qui est une copie de la ligne document validée, avec la quantité qui n’a pas encore été contrepassée. Le champ **Écr. article à lettrer** est renseigné correctement avec le numéro de l’écriture comptable article de la ligne document validée.  

    - Pour les lignes document validées qui ne sont pas du type **Article** (telles que les frais annexes), une ligne document est créée qui est une copie de la ligne document validée originale.  

    - Calcule le champ **Coût unitaire DS** sur la nouvelle ligne à partir des coûts des écritures comptables article correspondantes.  

    - Si le document copié est une expédition validée, une réception validée, une réception retour validée ou une expédition retour validée, le prix unitaire est calculé automatiquement à partir de la fiche article.  

    - Si le document copié est une facture ou un avoir validé, le prix unitaire, les remises facture et les remises ligne sont copiés à partir de la ligne document validée.  

    - Si la ligne document validée contient des lignes traçabilité, le champ **Écr. article à lettrer** sur les lignes traçabilité est renseigné à l’aide des numéros d’écriture comptable article appropriés des lignes traçabilité validées.  

     Lors de la copie à partir d’une facture ou d’un avoir enregistré, l’application copie les remises facture et les remises ligne adéquates comme valides au moment de la validation de ce document, de la ligne document validée vers la nouvelle ligne document. Notez toutefois que si l’option **Calculer remise facture** est activée sur la page **Paramètres achats**, la remise facture est de nouveau calculée lorsque vous validez la nouvelle ligne document. Le montant ligne de la nouvelle ligne peut par conséquent être différent du montant ligne de la ligne document validée, en fonction du nouveau calcul de la remise facture.  

    > [!NOTE]  
    >  Si une partie de la quantité de la ligne document validée a déjà été contrepassée ou vendue ou consommée, une ligne n’est créée que pour la quantité restant en stock ou qui n’a pas encore été retournée. Si la quantité totale de la ligne document validée a déjà été contrepassée, aucune ligne document n’est créée.  
    >
    >  Si le flux de biens dans le document validé est identique au flux de biens dans le nouveau document, une copie de la ligne document validée originale est simplement créée dans le nouveau document. Le champ **Écriture article à lettrer** n’est pas renseigné parce que, dans ce cas, l’inversion de même coût n’est pas possible. Par exemple, si vous utilisez la fonction **Afficher des lignes document validées à contrepasser** pour afficher une ligne avoir achat validée pour un nouvel avoir achat, seule la ligne avoir validée originale est copiée dans le nouvel avoir.  

10. Sur la page **Retour achat**, dans le champ **Code motif retour** de chaque ligne, sélectionnez le motif de ce retour.
11. Sélectionnez l’action **Valider**.

## <a name="to-create-a-replacement-purchase-order-from-a-purchase-return-order"></a>Pour créer une commande achat de remplacement à partir d’un retour achat ouvert

Vous pouvez vous accorder avec le fournisseur pour qu’il compense l’achat d’un article en remplaçant cet article. L'article de remplacement peut être identique à l'article d'origine ou il peut être différent. Le fournisseur peut vous avoir livré par erreur le mauvais article.  

1.  Sur la page **Retour achat** pour un processus de retour actif, sur une ligne vide, entrez une écriture négative pour l’article de remplacement en insérant un montant négatif dans le champ **Quantité**.  
2. Sélectionnez l’action **Déplacer lignes négatives**.  
3. Sur la page **Déplacer lignes achat nég.**, renseignez les champs selon vos besoins.
4. Choisissez le bouton **OK**. La ligne négative est effacée du retour achat et une commande achat est créée. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).  

## <a name="to-create-a-purchase-allowance"></a>Pour créer un rabais

Si vous recevez de votre fournisseur des articles que vous ne souhaitez pas, par exemple s’ils sont légèrement endommagés, ou s’ils ne sont pas de la bonne couleur ou de la bonne taille, le fournisseur peut vous proposer un rabais.  

Vous pouvez valider ce coût d’achat réduit en tant que frais annexes sur un avoir ou un retour et le lier à la réception validée. Ce qui suit décrit la procédure pour un retour achat, mais les mêmes étapes s’appliquent à un avoir achat.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs achat**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau** pour ouvrir un nouvel avoir achat vierge.  
3. Renseignez l’en-tête avoir à l’aide des informations relatives au fournisseur qui vous a envoyé le rabais.  
4. Dans le champ **Type** du raccourci **Lignes**, sélectionnez **Frais annexes**.  
5. Dans le champ **N°**, sélectionnez la valeur de frais annexes appropriée.  

    Vous pouvez créer un numéro de frais annexes spécial afin de couvrir les rabais.  
6. Dans le champ **Quantité**, saisissez **1**.  
7. Dans le champ **Coût unitaire direct**, saisissez le montant du rabais.  
8. Affectez le rabais en tant que frais annexes aux articles de la réception validée. Pour plus d’informations, voir [Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md). Une fois ce rabais affecté, revenez à la page **Avoir achat**.

Lorsque vous validez la commande retour achat, le rabais sur l’achat est ajouté au montant de l’écriture achat appropriée. De cette manière, vous pouvez maintenir la précision de l’évaluation stock.  

## <a name="to-combine-return-shipments"></a>Pour regrouper les expéditions retour

Pour retourner des articles couverts par différents retours achat au même fournisseur, vous pouvez utiliser la fonction **Regrouper les expéditions retour**.  

Lorsque vous expédiez ces articles, vous validez les commandes retour achat associées comme étant expédiées, ce qui crée des expéditions retour achat validées.  

Lorsque vous êtes prêt à facturer ces articles, au lieu de facturer séparément chaque retour achat, vous pouvez créer un avoir achat et copier automatiquement dans ce document les lignes expédition retour achat validées. Il vous suffit alors de valider l’avoir achat et de facturer en une fois tous les retours achat ouverts.  

Lorsque des expéditions retour sont regroupées sur un avoir et validées, un avoir achat validé est créé pour les lignes facturées. Le champ **Quantité facturée** sur le retour achat d’origine est mis à jour en fonction de la quantité facturée. Comme ce retour achat d’origine n’est toutefois pas supprimé, même s’il a été entièrement reçu et facturé, vous devez supprimer le retour achat manuellement.

> [!NOTE]  
> Dans la procédure suivante, on suppose qu’il existe plusieurs retours achat pour le fournisseur et qu’ils ont été validés comme étant expédiés.     

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs achat**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire.  
4. Choisissez l’action **Extraire lignes expéd. retour**.  
5. Sélectionnez plusieurs lignes expédition retour que vous souhaitez inclure dans la facture.  

    Si une ligne expédition retour incorrecte a été sélectionnée ou que vous souhaitez recommencer, il vous suffit de supprimer les lignes de l’avoir achat et de réutiliser la fonction **Extraire lignes expédition retour**.  
6. Sélectionnez l’action **Valider**.  

### <a name="to-remove-open-purchase-return-orders-after-combined-return-shipment-posting"></a>Pour supprimer des retours achat ouverts après la validation d’expéditions retour regroupées

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Supprimer retours achat facturé**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.  
3. Vous pouvez également supprimer chacun des retours achat manuellement.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Enregistrement des achats](purchasing-how-record-purchases.md)  
[Correction ou annulation des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
