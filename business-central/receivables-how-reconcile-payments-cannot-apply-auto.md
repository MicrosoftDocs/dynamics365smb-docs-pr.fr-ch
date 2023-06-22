---
title: Utilisation de la fonction Transférer la différence vers un compte pour rapprocher les paiements
description: 'Décrit comment traiter les paiements qui ne peuvent pas être lettrés dans un document, par exemple lorsqu’un taux de change entraîne un changement de montants.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically" />Rapprocher les paiements qui ne peuvent pas être lettrés automatiquement
Vous serez parfois amené à gérer des paiements sur votre compte bancaire, qui ne peuvent pas être lettrés à un client, un fournisseur ou une écriture comptable compte bancaire ouvertes associées. Les motifs peuvent être qu’il n’existe dans [!INCLUDE[prod_short](includes/prod_short.md)] aucun document auquel le paiement puisse être lettré, ou que le document associé dans [!INCLUDE[prod_short](includes/prod_short.md)] affiche un montant différent du montant de la transaction, par exemple, en raison du taux de change. Sur la page **Feuille rapprochement bancaire**, tous les montants de transaction pour les paiements qui n’ont pas encore été lettrés s’affichent dans le champ **Différence**, y compris les montants qui ne peuvent pas être lettrés pour des motifs tels que celui qui précède.

Méthodes de résolution de ces types de paiements non lettrés :
* Lettrer manuellement
* Utiliser le mappage de texte à compte
* Transférez un montant excédentaire vers une ligne feuille pour créer et valider l’écriture requise, comme le remboursement d’un trop-perçu.

Les paiements qui ne peuvent pas être lettrés peuvent apparaître sur les lignes feuille rapprochement bancaire pour les raisons suivantes :

* La valeur du champ **Différence** est égale à celle du champ **Montant transaction**, ce qui indique qu’aucune partie du paiement ne peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée.
* La valeur du champ **Différence** est inférieure à celle du champ **Montant transaction**, ce qui indique qu’une partie du paiement peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée. La partie restante du paiement ne peut pas être lettrée et doit être rapprochée manuellement ou en la validant directement sur un compte.

Pour rapprocher de tels paiements, vous pouvez choisir l’action **Transférer la différence vers un compte**, puis spécifier sur quel compte le montant du champ **Différence** sera validé lorsque vous validez la feuille rapprochement bancaire. Vous pouvez le faire soit à partir de la page **Feuille rapprochement bancaire** ou à partir de la page **Révision lettrage paiement** que vous ouvrez en choisissant la valeur dans le champ **Fiabilité correspondance** ou en choisissant le champ **Différence**.

> [!TIP]  
>   Il existe une fonctionnalité similaire permettant de configurer le rapprochement automatique des paiements récurrents qui ne peuvent pas être lettrés aux écritures comptables client, fournisseur ou compte bancaire ouvertes associées. Pour plus d’informations, reportez-vous à [Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically" />Pour rapprocher les paiements qui ne peuvent pas être lettrés automatiquement
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles rapprochement bancaire**, puis sélectionnez le lien associé.
2. Ouvrez une feuille de rapprochement de paiement. Pour plus d’informations, voir [Rapprocher les paiements à l’aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).
3. Sélectionnez l’action **Transférer la différence vers un compte**. La page **Transférer la différence vers un compte** s’ouvre.
4. Dans le champ **Type compte**, spécifiez le type de compte sur lequel le montant du paiement sera validé.
5. Dans le champ **N° compte**, spécifiez le compte sur lequel le montant du paiement sera validé.
6. Dans le champ **Description**, spécifiez le texte qui décrit cette validation de prélèvement. Par défaut, le texte du champ **Texte transaction** de la ligne feuille rapprochement bancaire est inséré.
7. Cliquez sur le bouton **OK**.

Si la valeur du champ **Différence** est égale à la valeur du champ **Montant transaction** lorsque vous validez la feuille rapprochement bancaire, l’intégralité du paiement sur la ligne feuille sera validé directement dans le compte contrepartie spécifié.

Si la valeur du champ **Différence** était inférieure à la valeur du champ **Montant transaction**, une ligne feuille supplémentaire est créée avec le même texte et la même date et avec la différence insérée dans le champ **Montant transaction**. Sur la ligne feuille d’origine, la différence est déduite de la valeur du champ **Montant transaction**, et le paiement demeure lettré à son écriture comptable client, fournisseur ou compte bancaire associée. Lorsque vous validez la feuille rapprochement bancaire, une partie du paiement est validée en tant que paiement lettré. L’autre partie du paiement est validée directement dans le compte spécifié.

## <a name="see-also" />Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
