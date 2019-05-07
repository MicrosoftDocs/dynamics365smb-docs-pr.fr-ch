---
title: Traiter les retours ou annulations de ventes | Microsoft Docs
description: Décrit comment créer un avoir vente, directement ou par l'intermédiaire d'un retour vente, pour traiter un retour, annulation, ou un remboursement pour les articles ou les services qui vous ont déjà été payés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a116dd3394e8aae36661815d72db3a8b13265bcf
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "917782"
---
# <a name="process-sales-returns-or-cancellations"></a>Traiter les retours ou annulations de ventes
Si votre client souhaite retourner des articles ou obtenir un remboursement pour des articles, ou encore annuler des services, que vous lui avez vendus et pour lesquels vous avez reçu un paiement, vous devez créer et valider un avoir vente qui indique la modification demandée. Pour inclure les informations de facture vente correctes, vous pouvez créer l'avoir vente à partir de la facture vente enregistrée ou vous pouvez créer un avoir vente avec les informations copiées de la facture.

Si vous souhaitez davantage de contrôle sur le processus de retour vente, par exemple les documents entrepôt pour la manutention des articles ou une meilleure vue d'ensemble lors de la réception d'articles à partir de plusieurs documents vente avec un retour vente, vous pouvez créer des retours vente. Un retour vente émet automatiquement l'avoir vente associé et les autres documents relatifs au retour, comme une commande vente de remplacement, le cas échéant. Pour plus d'informations, voir la section [Pour créer un retour vente à partir d'un ou plusieurs documents vente validés](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!NOTE]  
>   Si une facture vente validée n'a pas encore été payée, vous pouvez utiliser les fonctions **Corriger** ou **Annuler** sur la facture vente validée pour contrepasser automatiquement les transactions associées. Ces fonctions ne fonctionnent que pour les factures impayées, elles ne prennent pas en charge des retours partiels ou les annulations. Pour plus d'informations, voir [Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md).

Un retour ou un remboursement peut en effet se rapporter uniquement à certains des articles ou des services figurant sur la facture vente initiale. Dans ce cas, vous devez modifier les informations des lignes de l'avoir vente ou du retour vente. Lors de la validation de l'avoir vente ou du retour vente, les documents vente affectés par la modification sont contrepassés et un paiement de remboursement peut être créé pour le client. Pour plus d'informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).  

Outre la facture vente validée d'origine, vous pouvez lettrer l'avoir vente ou le retour vente à d'autres documents vente, par exemple une autre facture vente validée, parce que le client renvoie également des articles livrés avec cette facture.

Vous pouvez envoyer l'avoir vente validé au client pour confirmer le retour ou l'annulation et communiquer que la valeur associée sera remboursée, par exemple lorsque les articles sont renvoyés.

La validation de l'avoir rétablira également tous les frais annexes affectés au document validé, afin que les écritures valeur de l'article soient identiques à celles précédant l'affectation des frais annexes.

## <a name="inventory-costing"></a>Évaluation stock
Pour préserver l'évaluation correcte du stock, vous voudrez généralement remettre les articles retournés dans l'inventaire au coût unitaire auquel ils ont été vendus, et non à leur coût unitaire actuel. On appelle cela une inversion de même coût.

Vous pouvez affecter l'inversion de même coût automatiquement de deux façons.   

|Fonction|Désignation|  
|------------------|---------------------------------------|  
|Fonction**Afficher des lignes document validées à contrepasser** sur la page **Retour vente**|Copie les lignes d'un ou plusieurs documents validés afin de les contrepasser dans le retour vente. Pour plus d'informations, voir la section [Pour créer un retour vente à partir d'un ou plusieurs documents vente validés](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Fonction**Copier document** des pages **Avoir vente** et **Retour vente**|Copie l'en-tête et les lignes d'un document validé à contrepasser.<br /><br /> Requiert que la case à cocher **Coût retour identique obligatoire** soit sélectionnée sur la page **Paramètres ventes**.|

Pour réaliser manuellement la contrepassation exacte, sélectionnez **Écriture article à lettrer** sur n'importe quelle ligne de document retour, puis sélectionnez le numéro de l'écriture vente initiale. Cela crée un lien entre l'avoir ou le retour vente et l'écriture vente initiale, et garantit que l'article est évalué sur le coût unitaire initial.

Pour plus d'informations, voir [Détails de conception : Évaluation stock](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Pour créer un avoir vente à partir d'une facture vente validée
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sur la page **Factures vente enregistrées**, sélectionnez la facture vente validée que vous souhaitez contrepasser, puis sélectionnez l'action **Créer un avoir correctif**.

    L'en-tête avoir vente affiche des informations sur la facture vente validée. Vous pouvez les modifier, par exemple avec de nouvelles informations qui reflètent l'accord de retour.  
3. Modifiez les informations des lignes en fonction de l'accord, par exemple le nombre d'articles retournés ou du montant à rembourser.
4. Sélectionnez l'action **Lettrer écritures**.
5. Sur la page **Lettrer écritures client**, sélectionnez la ligne contenant le document vente validé auquel vous souhaitez lettrer l'avoir vente, puis sélectionnez l'action **ID lettrage**.

    L'identifiant de l'avoir vente s'affiche dans le champ **ID lettrage**.
6. Dans le champ **Montant à lettrer**, entrez le montant à lettrer s'il est inférieur au montant initial.  

    Au bas de la page **Lettrer écritures client**, vous pouvez afficher le montant total à lettrer pour contrepasser toutes les écritures concernées, à savoir lorsque la valeur du champ **Solde** est égale à zéro.
7. Cliquez sur le bouton **OK**. Lors de la validation de l'avoir vente, il doit être lettré avec les documents vente validés spécifiés.

    Lorsque vous avez créé les lignes avoir vente nécessaires et qu'un ou plusieurs applications sont spécifiées, vous pouvez procéder à la validation de l'avoir vente.   
8. Sélectionnez l'action **Valider et envoyer**.  

La boîte de dialogue **Valider et envoyer la confirmation** s'ouvre et indique le mode d'envoi par défaut du client. Vous pouvez modifier le mode d'envoi en cliquant sur le bouton de recherche pour le champ **Envoyer le document à**. Pour plus d'informations, reportez vous à [Configurer des profils d'envoi de documents](sales-how-setup-document-send-profiles.md).  

Les documents vente validés auxquels vous avez lettré l'avoir sont à présent contrepassés, et un remboursement peut être créé pour le client. L'avoir vente est supprimé et remplacé par un nouveau document dans la liste des avoirs vente validés.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Pour créer un avoir vente en copiant une facture vente validée
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Avoirs vente**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau** pour ouvrir un nouvel avoir vente vierge.
3. Dans le champ **Client**, entrez le nom d'un client existant.
4. Sélectionnez l'action **Copier document**.
5. Sur la page **Extraire document vente**, dans le champ **Type document**, sélectionnez **Facture enregistrée**.
6. Sélectionnez le champ **N° document** pour ouvrir la page **Factures vente validées**, puis sélectionnez la facture vente validée qui contient les lignes que vous souhaitez contrepasser.
7. Activez la case à cocher **Recalculer lignes** si vous souhaitez que les lignes facture vente validées copiées soient mises à jour avec les modifications apportées au prix article et au coût unitaire depuis la validation de la facture.
8. Cliquez sur le bouton **OK**. Les lignes facture copiées sont insérées dans l'avoir vente.
9. Remplissez l'avoir vente en vous reportant à [Pour créer un avoir vente à partir d'une facture vente validée](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Créer un retour vente à partir d'un ou plusieurs documents vente validés
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Retours vente**, et sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.  
3. Renseignez les champs dans le raccourci **Général** selon les besoins.
4. Dans le raccourci **Lignes**, renseignez les lignes manuellement, ou copiez des informations d'autres documents pour renseigner les lignes automatiquement :

    - utiliser la fonction  **Extraire lignes document enreg. à contrepasser** pour copier une ou plusieurs lignes de document validées à partir d'un ou plusieurs documents validés. Cette fonction inverse toujours exactement les coûts à partir de la ligne de document validée. Cette fonction est décrite dans les étapes suivantes.    
    - Utilisez la fonction **Copier document** pour copier un document existant dans le retour. Cette fonction permet de copier l'ensemble du document. Il peut s'agir d'un document validé ou d'un document non encore validé. Cette fonction ne permet l'inversion de même coût que lorsque la case **Inversion de même coût obligatoire** est cochée sur la page **Paramètres ventes**.  

5. Sélectionnez l'action **Afficher des lignes document validées à contrepasser**.
6. Dans le haut de la page **Lignes document vente enreg.**, cochez la case **Afficher uniquement lignes réversibles** si vous voulez n'afficher que les lignes contenant des quantités qui n'ont pas encore été retournées, ou s'il s'agit de lignes achat, vendues ou consommées. Par exemple, si une quantité de facture vente validée a déjà été retournée, il se peut que vous ne vouliez pas retourner cette quantité sur un nouveau document retour vente.

    > [!NOTE]  
    >  Ce champ ne fonctionne que pour les lignes livraison validées et les lignes facture validées, pas pour les lignes retour validées ni les lignes avoir validées.

    Dans la partie gauche de la page, les différents types de document sont énumérés, et le nombre entre parenthèses est le nombre de documents disponibles de chaque type de document.

7. Dans le champ **Filtre de type de document**, sélectionnez le type de lignes document validées que vous souhaitez utiliser.  
8. Sélectionnez les lignes que vous voulez copier vers le nouveau document.  

    > [!NOTE]  
    >  Si vous utilisez Ctrl+A pour sélectionner toutes les lignes, toutes les lignes à l'intérieur du filtre que vous avez défini sont copiées mais le filtre **Afficher uniquement quantité réversible** n'est pas pris en considération. Par exemple, supposons que vous ayez filtré les lignes pour un numéro de document particulier comportant deux lignes, dont l'une a déjà été retournée. Même si le champ **Afficher uniquement quantité réversible** est sélectionné, si vous appuyez sur Ctrl+A pour copier toutes les lignes, deux lignes sont copiées au lieu de celle qui n'a pas encore été contrepassée.  

9. Sélectionnez le bouton **OK** pour copier les lignes dans le nouveau document.  

    Les traitements suivants se produisent :  

    -   Pour les lignes document validées du type **Article**, une ligne document est créée qui est une copie de la ligne document validée, avec la quantité qui n'a pas encore été contrepassée. Le champ **Écriture article à lettrer** est renseigné correctement avec le numéro de l'écriture comptable article de la ligne document validée.  

    -   Pour les lignes document validées qui ne sont pas du type **Article** (telles que les frais annexes), une ligne document est créée qui est une copie de la ligne document validée originale.  

    -   Calcule le champ **Coût unitaire DS** sur la nouvelle ligne à partir des coûts des écritures comptables article correspondantes.  

    -   Si le document copié est une expédition validée, une réception validée, une réception retour validée ou une expédition retour validée, le prix unitaire est calculé automatiquement à partir de la fiche article.  

    -   Si le document copié est une facture ou un avoir validé, le prix unitaire, les remises facture et les remises ligne sont copiés à partir de la ligne document validée.  

    -   Si la ligne document validée contient des lignes traçabilité, le champ **Écriture article à lettrer** sur les lignes traçabilité est renseigné à l'aide des numéros d'écriture comptable article appropriés des lignes traçabilité validées.  

     Lors de la copie à partir d'une facture ou d'un avoir enregistré, le programme copie les remises facture et les remises ligne adéquates comme valides au moment de la validation de ce document, de la ligne document validée vers la nouvelle ligne document. Notez toutefois que si l'option **Calculer remise facture** est activée sur la page **Paramètres ventes**, la remise facture est de nouveau calculée lorsque vous validez la nouvelle ligne document. Le montant ligne de la nouvelle ligne peut par conséquent être différent du montant ligne de la ligne document validée, en fonction du nouveau calcul de la remise facture.  

     > [!NOTE]  
     >  Si une partie de la quantité de la ligne document validée a déjà été contrepassée ou vendue ou consommée, une ligne n'est créée que pour la quantité restant en stock ou qui n'a pas encore été retournée. Si la quantité totale de la ligne document validée a déjà été contrepassée, aucune ligne document n'est créée.  
     >   
     >  Si le flux de biens dans le document validé est identique au flux de biens dans le nouveau document, une copie de la ligne document validée originale est simplement créée dans le nouveau document. Le champ **Écriture article à lettrer** n'est pas renseigné parce que, dans ce cas, l'inversion de même coût n'est pas possible. Par exemple, si vous utilisez la fonction **Afficher des lignes document validées à contrepasser** pour afficher une ligne avoir vente validée pour un nouvel avoir vente, seule la ligne avoir vente validée originale est copiée dans le nouvel avoir.  

10. Sur la page **Retour vente**, dans le champ **Code motif retour** de chaque ligne, sélectionnez le motif de ce retour.
11. Sélectionnez l'action **valider**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Pour créer une commande vente de remplacement à partir de la commande retour vente
Vous pouvez décider de compenser la vente d'un article au client en remplaçant cet article. Vous pouvez le remplacer par le même article ou par un autre. Cette situation survient, par exemple, si vous avez par erreur expédié un mauvais article au client.  

1. Sur la page **Retour vente** pour un processus de retour actif, sur une ligne vide, entrez une écriture négative pour l'article de remplacement en insérant un montant négatif dans le champ **Quantité**.  
2. Sélectionnez l'action **Déplacer lignes négatives**.
3. Sur la page **Déplacer lignes vente nég.**, renseignez les champs selon vos besoins.
4. Choisissez le bouton **OK**. La ligne négative pour l'article de remplacement est supprimée de la commande retour vente et insérée sur une nouvelle page **Commande vente**. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Pour créer des documents associés au retour depuis un retour vente
Vous pouvez faire en sorte de créer automatiquement tous les documents de vente, de retour achat et de commande achat de remplacement au cours du processus de retour vente. Cela est utile, par exemple, dans les situations où vous voulez gérer des articles bénéficiant des garanties fournies par les fournisseurs.

1. Sur la page **Retour vente** pour un processus de retour actif, choisissez l'action **Créer documents associés retour**.
2. Dans le champ **N° fournisseur**, saisissez le numéro d'un fournisseur si vous souhaitez créer les documents du fournisseur automatiquement.
3. Si vous devez retourner un article retourné au fournisseur, activez la case à cocher **Créer retour achat**.
4. Si vous devez commander un article retourné au fournisseur, activez la case à cocher **Créer commande achat**.
5. Si vous devez créer une commande vente de remplacement, activez la case à cocher **Créer retour vente**.

## <a name="to-create-a-restock-charge"></a>Pour créer des frais de déstockage
Vous pouvez facturer à votre client les frais de restockage pour couvrir les coûts de manutention physique occasionnés par le retour d'un article. Cela peut arriver si, par exemple, le client commande par erreur le mauvais article ou change d'avis après réception de l'article.

Vous pouvez valider ce prix augmenté en tant que frais annexes dans un avoir ou un retour et l'affecter à l'expédition validée. Ce qui suit décrit la procédure pour un retour vente, mais les mêmes étapes s'appliquent à un avoir vente.

1. Ouvrez la page **Retour vente** pour un processus de retour actif.
2. Sur une nouvelle ligne, dans le champ **Type**, sélectionnez **Frais annexes**.  
3. Renseignez les champs comme pour n'importe quelle ligne frais annexes. Pour plus d'informations, voir [Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md).  

Lorsque vous validez la commande retour vente, les frais de restockage sont ajoutés au montant de l'écriture vente appropriée. De cette manière, vous pouvez maintenir la précision de l'évaluation stock.  

## <a name="to-create-a-sales-allowance"></a>Pour créer des frais de vente
Vous pouvez envoyer un avoir à un client avec une réduction si le client a reçu des articles légèrement endommagés ou avec du retard.  
Vous pouvez valider ce prix réduit en tant que frais annexes dans un avoir ou un retour et l'affecter à l'expédition validée. Ce qui suit décrit la procédure pour un avoir, mais les mêmes étapes s'appliquent à un retour vente.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Avoirs vente**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau** pour ouvrir un nouvel avoir vente vierge.
3. Renseignez l'en-tête avoir avec les informations appropriées sur le client à qui vous accordez un rabais sur ventes.  
4. Dans le champ **Type** du raccourci **Lignes**, sélectionnez **Frais annexes**.  
5.  Dans le champ **N°**, sélectionnez la valeur de frais annexes appropriée.  
     Vous pouvez créer un numéro frais annexes spécial pour couvrir les rabais sur ventes.  
6.  Dans le champ **Quantité**, saisissez **1**.  
7.  Dans le champ **Prix unitaire**, saisissez le montant du rabais sur ventes.  
8.  Affectez les frais de vente en tant que frais annexes aux articles de l'expédition validée. Pour plus d'informations, voir [Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md). Une fois ce rabais affecté, revenez à la page **Avoir vente**.  

Lorsque vous validez la commande retour vente, le rabais sur la vente est ajouté au montant de l'écriture vente appropriée. De cette manière, vous pouvez maintenir la précision de l'évaluation stock.

## <a name="to-combine-return-receipts"></a>Pour regrouper des réceptions retour
Vous pouvez regrouper des réceptions retour si votre client retourne plusieurs articles couverts par différentes commandes retour vente.  

Lorsque vous recevez les articles dans votre entrepôt, validez les retours vente comme concernés comme reçus. Cela crée des réceptions retour validées.  

Lorsque vous êtes prêt à facturer ce client, au lieu de facturer chaque commande retour vente séparément, vous pouvez créer un avoir vente et copier automatiquement les lignes réception retour validées dans ce document. Vous pouvez ensuite valider l'avoir et facturer facilement toutes les commandes retour vente ouvertes en même temps.  

Pour regrouper les réceptions retour, activer la case à cocher **Regrouper les B.L.** sur la page **Fiche client**.  

### <a name="to-manually-combine-return-receipts"></a>Pour regrouper manuellement des réceptions retour  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Avoir vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire.  
4. Choisissez l'action **Extraire lignes récept. retour**.  
5. Sélectionnez les lignes réception retour à inclure dans l'avoir :  

    -   Pour insérer toutes les lignes, sélectionnez-les toutes et sélectionnez le bouton **OK**.  

    -   Pour insérer des lignes spécifiques, sélectionnez-les et sélectionnez le bouton **OK**.  

6.  Si une ligne expédition incorrecte a été sélectionnée ou si vous voulez recommencer, supprimez simplement les lignes de l'avoir, puis exécutez de nouveau la fonction **Extraire lignes récept. retour**.  
7.  Validez la facture.  

### <a name="to-automatically-combine-return-receipts"></a>Pour regrouper automatiquement des réceptions retour  
Vous pouvez regrouper automatiquement des réceptions retour et avoir la possibilité de valider automatiquement l'avoir à l'aide de la fonction **Regrouper réceptions retour**.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Regrouper réceptions retour**, puis sélectionnez le lien associé.
2. Sur la page **Regrouper réceptions retour**, renseignez les champs pour choisir les réceptions retour appropriées.
3. Cochez la case **Valider avoirs**. Sinon, vous devrez valider manuellement les avoirs achat qui en résulteront.
4.  Cliquez sur le bouton **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Pour supprimer un retour reçu et facturé  
Lorsque vous facturez des réceptions retour de cette manière, les commandes retour à partir desquelles les réceptions retour ont été validées continuent à exister, même si elles ont été entièrement reçues et facturées.  

Lorsque des réceptions retour sont regroupées sur un avoir et validées, un avoir vente enregistré est créé pour la ou les lignes créditées. Le champ **Quantité facturée** dans le retour vente d'origine est mis à jour sur la base de la quantité facturée.   
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les retours vente facturés**, puis sélectionnez le lien associé.  
2.  Dans le champ de filtre **N°**, spécifiez les retours vente à supprimer.  
3.  Cliquez sur le bouton **OK**.  

Vous pouvez également supprimer chacune des commandes retour vente manuellement.   

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
