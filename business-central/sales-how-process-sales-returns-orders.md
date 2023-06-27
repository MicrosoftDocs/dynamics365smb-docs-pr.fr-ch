---
title: Traitement des retours vente
description: 'Décrit comment créer un retour vente pour traiter un retour, une annulation, ou un remboursement pour les articles ou les services qui vous ont déjà été payés.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders" />Traitement des retours vente

Si vous souhaitez davantage de contrôle sur le processus de retour vente, par exemple les documents entrepôt pour la manutention des articles, ou une meilleure vue d’ensemble lors de la réception d’articles à partir de plusieurs documents vente avec un retour vente, vous pouvez créer des retours vente. Un retour vente émet automatiquement l’avoir vente associé et les autres documents relatifs au retour, comme une commande vente de remplacement, le cas échéant.

Outre la facture vente validée d’origine, vous pouvez lettrer l’avoir vente ou le retour vente à d’autres documents vente, par exemple une autre facture vente validée, parce que le client renvoie également des articles livrés avec cette facture.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents" />Créer un retour vente à partir d’un ou plusieurs documents vente validés

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Retours vente**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs dans le raccourci **Général** selon les besoins.
4. Dans le raccourci **Lignes**, renseignez les lignes manuellement, ou copiez des informations d’autres documents pour renseigner les lignes automatiquement :

    - utiliser la fonction  **Extraire lignes document enreg. à contrepasser** pour copier une ou plusieurs lignes de document validées à partir d’un ou plusieurs documents validés. Cette fonction inverse toujours exactement les coûts à partir de la ligne de document validée. Cette fonction est décrite dans les étapes suivantes.    
    - Utilisez la fonction **Copier à partir du document** pour copier un document existant dans le retour. Cette fonction permet de copier l’ensemble du document. Il peut s’agir d’un document validé ou d’un document non encore validé. Cette fonction ne permet l’inversion de même coût que lorsque la case **Inversion de même coût obligatoire** est cochée sur la page **Paramètres ventes**.  

5. Choisissez l’action **Traiter**, puis choisissez l’action **Afficher des lignes document validées à contrepasser**.
6. Dans le haut de la page **Lignes document vente enreg.**, cochez la case **Afficher uniquement lignes réversibles** si vous voulez n’afficher que les lignes contenant des quantités qui n’ont pas encore été retournées, ou s’il s’agit de lignes achat, vendues ou consommées. Par exemple, si une quantité de facture vente validée a déjà été retournée, il se peut que vous ne vouliez pas retourner cette quantité sur un nouveau document retour vente.

    > [!NOTE]  
    >  Ce champ ne fonctionne que pour les lignes livraison validées et les lignes facture validées, pas pour les lignes retour validées ni les lignes avoir validées.

    Dans la partie gauche de la page, les différents types de document sont énumérés, et le nombre entre parenthèses est le nombre de documents disponibles de chaque type de document.

7. Dans le champ **Filtre de type de document**, sélectionnez le type de lignes document validées que vous souhaitez utiliser.  
8. Sélectionnez les lignes que vous voulez copier vers le nouveau document.  

    > [!NOTE]  
    >  Si vous utilisez <kbd>Ctrl</kbd>+<kbd>A</kbd> pour sélectionner toutes les lignes, toutes les lignes à l’intérieur du filtre que vous avez défini sont copiées mais le filtre **Afficher uniquement quantité réversible** n’est pas pris en considération. Par exemple, supposons que vous ayez filtré les lignes pour un numéro de document particulier comportant deux lignes, dont l’une a déjà été retournée. Même si le champ **Afficher uniquement quantité réversible** est sélectionné, si vous sélectionnez <kbd>Ctrl</kbd>+<kbd>A</kbd> pour copier toutes les lignes, deux lignes sont copiées au lieu de celle qui n’a pas encore été contrepassée.  

9. Sélectionnez le bouton **OK** pour copier les lignes dans le nouveau document.  

    Les traitements suivants se produisent :  

    -   Pour les lignes document validées du type **Article**, une ligne document est créée qui est une copie de la ligne document validée, avec la quantité qui n’a pas encore été contrepassée. Le champ **Écriture article à lettrer** est renseigné correctement avec le numéro de l’écriture comptable article de la ligne document validée.  

    -   Pour les lignes document validées qui ne sont pas du type **Article** (telles que les frais annexes), une ligne document est créée qui est une copie de la ligne document validée originale.  

    -   Calcule le champ **Coût unitaire DS** sur la nouvelle ligne à partir des coûts des écritures comptables article correspondantes.  

    -   Si le document copié est une expédition validée, une réception validée, une réception retour validée ou une expédition retour validée, le prix unitaire est calculé automatiquement à partir de la fiche article.  

    -   Si le document copié est une facture ou un avoir validé, le prix unitaire, les remises facture et les remises ligne sont copiés à partir de la ligne document validée.  

    -   Si la ligne document validée contient des lignes traçabilité, le champ **Écriture article à lettrer** sur les lignes traçabilité est renseigné à l’aide des numéros d’écriture comptable article appropriés des lignes traçabilité validées.  

     Lors de la copie à partir d’une facture ou d’un avoir enregistré, l’application copie les remises facture et les remises ligne adéquates comme valides au moment de la validation de ce document, de la ligne document validée vers la nouvelle ligne document. Notez toutefois que si l’option **Calculer remise facture** est activée sur la page **Paramètres ventes**, la remise facture est de nouveau calculée lorsque vous validez la nouvelle ligne document. Le montant ligne de la nouvelle ligne peut par conséquent être différent du montant ligne de la ligne document validée, en fonction du nouveau calcul de la remise facture.  

     > [!NOTE]  
     >  Si une partie de la quantité de la ligne document validée a déjà été contrepassée ou vendue ou consommée, une ligne n’est créée que pour la quantité restant en stock ou qui n’a pas encore été retournée. Si la quantité totale de la ligne document validée a déjà été contrepassée, aucune ligne document n’est créée.  
     >   
     >  Si le flux de biens dans le document validé est identique au flux de biens dans le nouveau document, une copie de la ligne document validée originale est simplement créée dans le nouveau document. Le champ **Écriture article à lettrer** n’est pas renseigné parce que, dans ce cas, l’inversion de même coût n’est pas possible. Par exemple, si vous utilisez la fonction **Afficher des lignes document validées à contrepasser** pour afficher une ligne avoir vente validée pour un nouvel avoir vente, seule la ligne avoir vente validée originale est copiée dans le nouvel avoir.  

10. Sur la page **Retour vente**, dans le champ **Code motif retour** de chaque ligne, sélectionnez le motif de ce retour.
11. Sélectionnez l’action **valider**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order" />Pour créer une commande vente de remplacement à partir de la commande retour vente
Vous pouvez décider de compenser la vente d’un article au client en remplaçant cet article. Vous pouvez le remplacer par le même article ou par un autre. Cette situation survient, par exemple, si vous avez par erreur expédié un mauvais article au client.  

1. Sur la page **Retour vente** pour un processus de retour actif, sur une ligne vide, entrez une écriture négative pour l’article de remplacement en insérant un montant négatif dans le champ **Quantité**.  
2. Sélectionnez l’action **Déplacer lignes négatives**.
3. Sur la page **Déplacer lignes vente nég.**, renseignez les champs selon vos besoins.
4. Choisissez le bouton **OK**. La ligne négative pour l’article de remplacement est supprimée de la commande retour vente et insérée sur une nouvelle page **Commande vente**. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order" />Pour créer des documents associés au retour depuis un retour vente
Vous pouvez faire en sorte de créer automatiquement tous les documents de vente, de retour achat et de commande achat de remplacement au cours du processus de retour vente. Cela est utile, par exemple, dans les situations où vous voulez gérer des articles bénéficiant des garanties fournies par les fournisseurs.

1. Sur la page **Retour vente** pour un processus de retour actif, choisissez l’action **Créer documents associés retour**.
2. Dans le champ **N° fournisseur**, saisissez le numéro d’un fournisseur si vous souhaitez créer les documents du fournisseur automatiquement.
3. Si vous devez retourner un article retourné au fournisseur, activez la case à cocher **Créer retour achat**.
4. Si vous devez commander un article retourné au fournisseur, activez la case à cocher **Créer commande achat**.
5. Si vous devez créer une commande vente de remplacement, activez la case à cocher **Créer retour vente**.

## <a name="to-create-a-restock-charge" />Pour créer des frais de déstockage
Vous pouvez facturer à votre client les frais de restockage pour couvrir les coûts de manutention physique occasionnés par le retour d’un article. Cela peut arriver si, par exemple, le client commande par erreur le mauvais article ou change d’avis après réception de l’article.

Vous pouvez valider ce prix augmenté en tant que frais annexes dans un avoir ou un retour et l’affecter à l’expédition validée. Ce qui suit décrit cette procédure pour un retour vente, mais les mêmes étapes s’appliquent à un avoir vente.

1. Ouvrez la page **Retour vente** pour un processus de retour actif.
2. Sur une nouvelle ligne, dans le champ **Type**, sélectionnez **Frais annexes**.  
3. Renseignez les champs comme pour n’importe quelle ligne frais annexes. Pour plus d’informations, voir [Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md).  

Lorsque vous validez la commande retour vente, les frais de restockage sont ajoutés au montant de l’écriture vente appropriée. De cette manière, vous pouvez maintenir la précision de l’évaluation stock.  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/paths/return-items-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
