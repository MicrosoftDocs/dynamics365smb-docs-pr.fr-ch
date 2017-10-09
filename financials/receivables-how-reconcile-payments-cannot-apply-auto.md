---
title: "Utilisation de la fonction Transférer la différence vers un compte pour rapprocher les paiements | Microsoft Docs'"
description: "Décrit comment traiter les paiements qui ne peuvent pas être lettrés dans un document, par exemple lorsqu'un taux de change entraîne un changement de montants."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 741c46f51c9ffd6e3b7f9d429accfd394684c9ed
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Procédure : rapprocher les paiements qui ne peuvent pas être lettrés automatiquement
Vous serez parfois amené à gérer des paiements sur votre compte bancaire, qui ne peuvent pas être lettrés à un client, un fournisseur ou une écriture comptable compte bancaire ouvertes associées. Les motifs peuvent être qu'il n'existe dans [!INCLUDE[d365fin](includes/d365fin_md.md)] aucun document auquel le paiement puisse être lettré, ou que le document associé dans [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche un montant différent du montant de la transaction, par exemple, en raison du taux de change. Dans la fenêtre **Feuille rapprochement bancaire**, tous les montants de transaction pour les paiements qui n'ont pas encore été lettrés s'affichent dans le champ **Différence**, y compris les montants qui ne peuvent pas être lettrés pour des motifs tels que celui qui précède.

Les paiements qui ne peuvent pas être lettrés peuvent apparaître sur les lignes feuille rapprochement bancaire pour les raisons suivantes :

* La valeur du champ **Différence** est égale à celle du champ **Montant transaction**, ce qui indique qu'aucune partie du paiement ne peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée.
* La valeur du champ **Différence** est inférieure à celle du champ **Montant transaction**, ce qui indique qu'une partie du paiement peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée. La partie restante du paiement ne peut pas être lettrée et doit être rapprochée manuellement ou en la validant directement sur un compte.

Pour rapprocher de tels paiements, vous pouvez cliquer sur le bouton **Transférer la différence vers un compte**, puis spécifier sur quel compte le montant du champ **Différence** sera validé lorsque vous validez la feuille rapprochement bancaire.

> [!TIP]  
>   Il existe une fonctionnalité similaire permettant de configurer le rapprochement automatique des paiements récurrents qui ne peuvent pas être lettrés aux écritures comptables client, fournisseur ou compte bancaire ouvertes associées. Pour plus d'informations, reportez-vous à [Procédure : mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Pour rapprocher les paiements qui ne peuvent pas être lettrés
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille rapprochement bancaire**, puis sélectionnez le lien connexe.
2. Ouvrez une feuille de rapprochement de paiement. Pour plus d'informations, reportez-vous à [Procédure : rapprocher les paiements à l'aide de l'application automatique](receivables-how-reconcile-payments-auto-application.md).
3. Sélectionnez l'action **Transférer la différence vers un compte**. La fenêtre **Transférer la différence vers un compte** s'ouvre.
4. Dans le champ **Type compte**, spécifiez le type de compte sur lequel le montant du paiement sera validé.
5. Dans le champ **N° compte**, spécifiez le compte sur lequel le montant du paiement sera validé.
6. Dans le champ **Description**, spécifiez le texte qui décrit cette validation de prélèvement. Par défaut, le texte du champ **Texte transaction** de la ligne feuille rapprochement bancaire est inséré.
7. Cliquez sur le bouton **OK**.

Si la valeur du champ **Différence** est égale à la valeur du champ **Montant transaction** lorsque vous validez la feuille rapprochement bancaire, l'intégralité du paiement sur la ligne feuille sera validé directement dans le compte contrepartie spécifié.

Si la valeur du champ **Différence** était inférieure à la valeur du champ **Montant transaction**, une ligne feuille supplémentaire est créée avec le même texte et la même date et avec la différence insérée dans le champ **Montant transaction**. Sur la ligne feuille d'origine, la différence est déduite de la valeur du champ **Montant transaction**, et le paiement demeure lettré à son écriture comptable client, fournisseur ou compte bancaire associée. Lorsque vous validez la feuille rapprochement bancaire, une partie du paiement est validée en tant que paiement lettré. L'autre partie du paiement est validée directement dans le compte spécifié.

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

