---
title: Familiarisation avec la validation des documents achat | Microsoft Docs
description: Découvrez les différentes fonctions de validation pour valider les documents achat et comment mettre à jour les documents validés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/17/2020
ms.author: sgroespe
ms.openlocfilehash: 2565133adfab4fb5f6febeeccb69c4f3d6f59e71
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991895"
---
# <a name="posting-purchases"></a>Validation des achats
Dans le groupe **Validation** sur un document achat, vous pouvez faire votre choix parmi les fonctions de validation suivantes :

* **Valider**
* **Aperçu compta.**
* **Valider et Imprimer**
* **Impression test**
* **Valider par lot**

Lorsque vous avez renseigné toutes les lignes et saisi toutes les informations de la commande achat, vous pouvez la valider, c'est-à-dire, créer une réception et une facture.

Lorsqu’une commande achat est validée, le compte du fournisseur, les écritures comptables et les écritures comptables article sont mis à jour.

Pour chaque commande achat, une écriture achat est créée dans la table **Ecriture comptable**. Une écriture est également créée dans le compte fournisseur de la table **Ecriture fournisseur** et une autre dans le compte fournisseur approprié. De plus, la validation de la commande peut avoir pour résultat la création d'une écriture TVA et d'une écriture comptable pour le montant de la remise. La validation d'une écriture pour la remise dépend de la valeur du champ **Comptabilisation remises** de la table **Paramètres achats**.

Pour chaque ligne commande achat, une écriture comptable article est créée dans la table **Écriture comptable article** (si les lignes achat contiennent des numéros d'article) ou une écriture est créée dans la table **Écriture comptable** (si les lignes achat contiennent un compte général). En outre, les commandes achat sont toujours enregistrées dans les tables **En-tête réception achat** et **En-tête facture achat**.

Avant de commencer à valider, vous pouvez effectuer une impression test qui contient toutes les informations de la commande achat et indique les erreurs afférentes. Pour imprimer l’état, sélectionnez **Validation**, puis **Impression test**.

> [!IMPORTANT]  
>   Lorsque vous validez une commande, vous pouvez créer une réception et une facture. Celles-ci peuvent être faites simultanément ou séparément. Vous pouvez également créer une réception partielle et une facture partielle en renseignant les champs **Qté à recevoir** et **Qté à facturer** sur chaque ligne commande achat avant la validation. Remarquez que vous ne pouvez pas créer de facture pour un article qui n'a pas été reçu. C'est-à-dire que, avant de pouvoir facturer, vous devez avoir validé une réception, ou vous devez choisir de réceptionner et de facturer en même temps.

Vous pouvez soit valider, soit valider et imprimer. Si vous choisissez de valider et d’imprimer, un rapport est imprimé lorsque la commande est validée. Vous pouvez aussi choisir la fonction **Valider par lot**, qui vous permet de valider plusieurs commandes en même temps. Pour plus d'informations, voir [Valider plusieurs documents en même temps](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Affichage des écritures comptables
Lorsque la validation est terminée, les lignes achat validées sont supprimées de la commande. Un message vous indique lorsque la validation est terminée. Vous pouvez ensuite afficher les écritures validées dans les diverses pages qui contiennent les écritures validées, comme les pages **Écritures comptable fournisseur**, **Écritures comptable**, **Écritures comptable article**, **Réceptions achat enreg.** et **Factures achat enregistrées**.

Dans la plupart des cas, vous pouvez ouvrir des écritures comptables à partir de la fiche ou du document concerné. Par exemple, sur la page **Fiche fournisseur**, sélectionnez l'action **Écritures**.

## <a name="editing-ledger-entries"></a>Modification des écritures comptables
Vous pouvez modifier certains champs dans les documents d'achat validés, tels que le champ **Référence de paiement**. Pour plus d'informations, voir [Modifier les documents validés](across-edit-posted-document.md). Pour les champs plus critiques qui concernent la piste d'audit, vous devez inverser ou annuler la validation. Pour plus d'informations, voir [Inversion d'une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md). 

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Valider les documents validés](across-edit-posted-document.md)  
[Valider plusieurs documents en même temps](ui-batch-posting.md)  
[Achats](purchasing-manage-purchasing.md)  
[Validation des documents et des feuilles](ui-post-documents-journals.md)  
[Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Recherche de pages et d'informations avec Tell Me](ui-search.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
