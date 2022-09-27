---
title: Enregistrer les achats avec les factures achat (contient une vidéo)
description: Décrit comment acheter des stocks, des articles hors stock ou des ressources en créant et en validant des factures ou commandes achat.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: daedfacb3e496fa668095916b07caa7488765a83
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535515"
---
# <a name="record-purchases-with-purchase-invoices"></a>Enregistrer les achats avec les factures achat

Vous créez une facture achat ou une commande achat pour enregistrer le coût d’achats et suivre les créances. Si vous devez contrôler un stock, les factures achat et les commandes achat sont également utilisées pour mettre à jour de manière dynamique les niveaux de stock afin que vous puissiez réduire vos coûts et fournir un meilleur service client. Le prix d’achat, notamment les frais de service, et les valeurs d’inventaire qui résultent de la validation des factures achat ou des commandes contribuent aux chiffres du profit et à d’autres KPI financiers sur votre Tableau de bord.

## <a name="create-purchase-invoices"></a>Créer des factures achat

Outre l’achat d’articles physiques (type d’article **Stock**) qui affectent l’évaluation du stock, vous pouvez acheter des services représentés par des unités de temps. Vous pouvez le faire avec le type d’article **Service** ou le type de ligne **Ressource**.

Lorsque vous réceptionnez des articles de stock ou lorsque le service acheté est terminé, vous validez la facture ou commande achat pour mettre à jour le stock et les enregistrements financiers et activer le paiement au fournisseur selon les conditions de paiement. En savoir plus sur [Valider des achats](ui-post-purchases.md), [Recevoir des articles](warehouse-how-receive-items.md), et [Effectuer des paiements](payables-make-payments.md).

> [!CAUTION]  
> Ne validez pas une facture achat pour des articles physiques tant que vous n’avez pas reçu les articles et que vous ne connaissez pas le coût total de l’achat, frais supplémentaires compris. Sinon, la valeur du stock et les chiffres du profit peuvent être biaisés.

### <a name="create-a-purchase-invoice"></a>Créer une facture achat

Ce qui suit décrit comment créer une facture achat. La procédure est identique pour une commande achat. La principale différence est que les commandes achat ont des champs et des actions supplémentaires pour la manutention des articles.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Dans le champ **Fournisseur**, entrez le nom d’un fournisseur existant.

    D’autres champs de la page **Facture achat** sont désormais renseignés avec les informations standard sur le fournisseur sélectionné. Si le fournisseur n’est pas enregistré, procédez comme suit :

    1. Dans le champ **Fournisseur**, entrez le nom du nouveau fournisseur.
    2. Dans la boîte de dialogue d’enregistrement du nouveau fournisseur, cliquez sur le bouton **Oui**.
    3. Pour en savoir plus sur la façon de remplir la carte du fournisseur, consultez [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).  
    4. Une fois que vous avez terminé la fiche fournisseur, cliquez sur le bouton **OK** pour revenir à la page **Facture achat**.

3. Renseignez les champs restants de la page **Facture achat**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Vous êtes maintenant prêt à renseigner les lignes facture achat avec les articles ou ressources que vous avez achetés au fournisseur.

    > [!NOTE]  
    > Si vous avez défini des lignes achat récurrentes pour le fournisseur, par exemple un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la facture par l’intermédiaire de l’action **Extraire les lignes achat récurrentes**.
4. Dans le raccourci **Lignes**, dans le champ **N° article**, entrez le numéro d’un article de stock ou d’un service.
5. Dans le champ **Quantité**, indiquez le nombre d’articles à acheter.

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Coût unitaire direct** multipliée par la valeur du champ **Quantité**.

    Le prix et le montant ligne sont affichés avec ou sans la Sales Tax en fonction de ce que vous avez sélectionné dans le champ **Prix incluant les taxes** de la fiche fournisseur.

    Les champs totaux sous les lignes sont automatiquement mises à jour comme vous créez ou modifiez des lignes pour afficher les montants qui seront validés en comptabilité.

6. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC** au bas de la facture.

    > [!NOTE]  
    > Si vous avez défini des remises facture pour le fournisseur, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture fournisseur** si les critères sont réunis. Le montant remise calculé est alors inséré dans le champ **Montant remise facture**.
7. Lorsque vous recevez les articles ou services achetés, sélectionnez **Valider**.

L’achat est désormais visible dans le stock, les écritures ressource et les enregistrements financiers, et le paiement fournisseur est activé. La facture achat est supprimée de la liste des factures achat et remplacée par un nouveau document dans la liste des factures achat validées.  

> [!NOTE]
> Dans de rares cas, les montants validés peuvent différer de ce qui est affiché dans les champs des totaux. Cela est généralement dû aux calculs d’arrondi par rapport à la TVA ou à la taxe sur les ventes.
>
> Pour vérifier les montants qui seront réellement validés, utilisez la page **Statistiques**, qui tient compte des calculs d’arrondi. Aussi, si vous choisissez l’action **Lancer**, les champs de totaux seront mis à jour pour inclure les calculs d’arrondi.

## <a name="when-to-use-purchase-orders"></a>Quand utiliser les commandes achat

Vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d’une quantité de commande, par exemple, si la quantité totale n’était pas disponible auprès du fournisseur. Si vous commercialisez des articles en les livrant directement depuis votre fournisseur auprès de votre client, vous devez également utiliser les commandes achat. En savoir plus sur [Créer des livraisons directes](sales-how-drop-shipment.md).

Pour tous les autres aspects, les commandes achat fonctionnent de la même manière que les factures achat. La procédure suivante se base sur une facture achat. La procédure est identique pour une commande achat.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="purchasing-non-inventory-items"></a>Acheter des articles hors stock

Les lignes d’une facture d’achat peuvent être de type **Ressource** ou **Article**. Les fiches article peuvent être classées comme étant de type **Stock**, **Service** ou **Hors stock** pour spécifier si l’article est une unité de stock physique, une unité de temps de travail (applicable pour les ressources) ou une unité physique qui n’est pas suivie dans le stock. En savoir plus sur [Enregistrer de nouveaux articles](inventory-how-register-new-items.md). Le processus de facture achat est identique pour tous les types mentionnés.

> [!NOTE]
> Avec le type de ligne achat **Ressource**, vous pouvez également acheter des ressources externes, par exemple pour facturer un fournisseur pour le travail livré. En savoir plus sur [Configurer les ressources](projects-how-setup-resources.md).
>
> Pour utiliser une ressource achetée, vous devrez peut-être définir la capacité de la ressource et l’affecter manuellement à un projet. L’achat d’une ressource crée une écriture comptable ressource. Cependant, les écritures comptables ressource ne sont pas suivies pour la quantité et la valeur comme le sont les articles, par exemple. Si le suivi de la quantité et de la valeur est requis, envisagez d’utiliser d’autres types d’élément de ligne.

## <a name="posted-invoices"></a>Factures enregistrées

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Vous pouvez facilement corriger ou annuler une facture achat validée avant de payer le fournisseur. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si vous souhaitez modifier l’achat assez tôt dans le processus de commande. En savoir plus, [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) Si vous avez déjà payé des articles ou services sur la facture achat validée, vous devez créer un avoir achat pour contrepasser l’achat. En savoir plus, [Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md)

[Ouvrir la liste des **factures achat validées**](https://businesscentral.dynamics.com/?page=146) dans [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Numéro de document externe

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/processing-invoices-dynamics-365-business-central/index) associée

## <a name="see-also"></a>Voir aussi

[Validation des achats](ui-post-purchases.md)  
[Réceptionner des articles](warehouse-how-receive-items.md)  
[Demander des devis](purchasing-how-request-quotes.md)  
[Acheter des articles pour une vente](purchasing-how-purchase-products-sale.md)  
[Préparer des livraisons directes](sales-how-drop-shipment.md)  
[Achats](purchasing-manage-purchasing.md)  
[Définition des achats](purchasing-setup-purchasing.md)  
[Paramétrer des ressources](projects-how-setup-resources.md)  
[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
