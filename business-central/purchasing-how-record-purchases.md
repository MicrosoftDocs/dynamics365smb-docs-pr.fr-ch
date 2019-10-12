---
title: Créer une facture achat et enregistrer les achats | Microsoft Docs
description: Décrit comment acheter des articles stock ou service en créant et en validant des factures ou des commandes achat.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1ad25642cdbfd9367b1533f1a39d178fe08ebb2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312475"
---
# <a name="record-purchases"></a>Enregistrer des achats
Vous créez une facture achat ou une commande achat pour enregistrer le coût d'achats et suivre les créances. Si vous devez contrôler un stock, les factures achat et les commandes achat sont également utilisées pour mettre à jour de manière dynamique les niveaux de stock afin que vous puissiez réduire vos coûts et fournir un meilleur service client. Le prix d'achat, notamment les frais de service, et les valeurs d'inventaire qui résultent de la validation des factures achat ou des commandes contribuent aux chiffres du profit et à d'autres KPI financiers sur votre Tableau de bord.

> [!NOTE]  
>   Vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d'une quantité de commande, par exemple, si la quantité totale n'était pas disponible auprès du fournisseur. Si vous commercialisez des articles en les livrant directement depuis votre fournisseur auprès de votre client, vous devez également utiliser les commandes achat. Pour plus d'informations, voir [Effectuer des livraisons directes](sales-how-drop-shipment.md). Pour tous les autres aspects, les commandes achat fonctionnent de la même manière que les factures achat. La procédure suivante se base sur une facture achat. La procédure est identique pour une commande achat.

Lorsque vous recevez des articles de stock, ou lorsque le service acheté est terminé, vous validez la facture ou une commande achat pour mettre à jour le stock et les enregistrements financiers et pour activer le paiement au fournisseur selon les conditions de paiement. Pour plus d'informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).

> [!CAUTION]  
>   Ne validez pas une facture achat tant que vous n'avez pas reçu les articles et que vous ne connaissez pas le coût total de l'achat, frais supplémentaires compris. Sinon, la valeur du stock et les chiffres du profit peuvent être biaisés.

Vous pouvez facilement corriger ou annuler une facture achat validée avant de payer le fournisseur. Cela est utile si vous souhaitez corriger une erreur de saisie ou si vous souhaitez modifier l'achat assez tôt dans le processus de commande. Pour plus d'informations, voir [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Si vous avez déjà payé des articles sur la facture achat validée, vous devez créer un avoir achat pour contrepasser l'achat. Pour plus d'informations, reportez-vous à [Traiter les retours ou annulations d'achats](purchasing-how-process-purchase-returns-cancellations.md).

La fiche article peut être de type **Stock**, **Service** et **Hors stock** pour spécifier si l'article est une unité de stock physique, une unité de temps de travail ou une unité physique qui n'est pas conservée dans le stock. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md). Le processus de facture achat est identique pour les trois types d'article.

Vous pouvez remplir les champs relatifs au fournisseur sur la facture achat de deux façons selon que le fournisseur est déjà enregistré ou non.

## <a name="to-create-a-purchase-invoice"></a>Pour créer une facture achat
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat**, puis sélectionnez le lien associé.  
2. Dans le champ **Fournisseur**, entrez le nom d'un fournisseur existant.

    D'autres champs de la page **Facture achat** sont désormais renseignés avec les informations standard sur le fournisseur sélectionné. Si le fournisseur n'est pas enregistré, procédez comme suit :
3. Dans le champ **Fournisseur**, entrez le nom du nouveau fournisseur.
4. Dans la boîte de dialogue d'enregistrement du nouveau fournisseur, cliquez sur le bouton **Oui**.
5. Sur la page **Sélectionnez un modèle pour un nouveau fournisseur**, sélectionnez un modèle sur lequel baser la nouvelle fiche fournisseur, puis cliquez sur le bouton **OK**.
6. Une nouvelle fiche fournisseur préremplie avec les informations sur le modèle fournisseur sélectionné s'ouvre. Le champ **Nom** est prérempli avec le nom du nouveau fournisseur que vous avez saisi sur la facture achat.
7. Renseignez les autres champs de la fiche fournisseur. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).  
8. Une fois que vous avez terminé la fiche fournisseur, cliquez sur le bouton **OK** pour revenir à la page **Facture achat**.

    Plusieurs champs de la page **Facture achat** sont renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche fournisseur.
9. Renseignez les champs restants de la page **Facture achat**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Vous êtes maintenant prêt à renseigner les lignes facture achat avec les articles en stock ou les services que vous avez achetés au fournisseur.

    > [!NOTE]  
    >   Si vous avez défini des lignes achat récurrentes pour le fournisseur, par exemple un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la facture par l'intermédiaire de l'action **Extraire les lignes achat récurrentes**.
10. Dans le raccourci **Lignes**, dans le champ **N° article**, entrez le numéro d'un article de stock ou d'un service.
11. Dans le champ **Quantité**, indiquez le nombre d'articles à acheter.

    > [!NOTE]  
    >   Pour les articles de type **Service**, la quantité est une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne.

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Coût unitaire direct** multipliée par la valeur du champ **Quantité**.

    Le prix et le montant ligne sont affichés avec ou sans la Sales Tax en fonction de ce que vous avez sélectionné dans le champ **Prix incluant les taxes** de la fiche fournisseur.

    Les champs totaux sous les lignes sont automatiquement mises à jour comme vous créez ou modifiez des lignes pour afficher les montants qui seront validés en comptabilité.

    > [!NOTE]
    > Dans de très rares cas, les montants validés peuvent différer de ce qui est affiché dans les champs des totaux. Cela est généralement dû aux calculs d'arrondi par rapport à la TVA ou à la taxe sur les ventes.<br /><br />Pour vérifier les montants qui seront réellement validés, vous pouvez utiliser la page **Statistiques**, qui tient compte des calculs d'arrondi. Aussi, si vous choisissez l'action **Lancer**, les champs de totaux seront mis à jour pour inclure les calculs d’arrondi.

12. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC** au bas de la facture.

    > [!NOTE]  
    >   Si vous avez défini des remises facture pour le fournisseur, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture fournisseur** si les critères sont réunis, et le montant associé est inséré dans le champ **Montant remise facture**.
13. Lorsque vous recevez les articles ou services achetés, sélectionnez **Valider**.

L'achat est désormais visible dans le stock et les enregistrements financiers, et le paiement fournisseur est activé. La facture achat est supprimée de la liste des factures achat et remplacée par un nouveau document dans la liste des factures achat validées.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Définition des achats](purchasing-setup-purchasing.md)  
[Demander des devis](purchasing-how-request-quotes.md)  
[Acheter des articles pour une vente](purchasing-how-purchase-products-sale.md)  
[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Préparer des livraisons directes](sales-how-drop-shipment.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
