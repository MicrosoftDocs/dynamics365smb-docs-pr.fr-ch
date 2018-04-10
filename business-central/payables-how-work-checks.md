---
title: "Emettre, imprimer et annuler des chèques| Microsoft Docs"
description: "Décrit comment émettre des chèques à l'aide de la feuille paiement, imprimer des chèques, et annuler ou afficher les écritures comptables chèque dans Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0c1b37616b4aafc9535f2d3fbf60b915c490dd0b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a>Utilisation des chèques
Vous pouvez émettre des chèques par voie électronique et manuelle dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces deux méthodes utilisent la feuille paiement pour émettre des chèques aux fournisseurs. Vous pouvez également annuler des chèques et afficher les écritures comptables chèque.

La procédure d'émission de chèques propose des paiements, crée des écritures comptables et imprime les chèques informatiques.

> [!NOTE]  
>   Pour s'assurer que la banque efface uniquement les chèques et les montants validés, vous pouvez envoyer un fichier contenant des informations de paiement, du chèque et du fournisseur. Pour plus d'informations, voir [Exporter des fichiers Positive Pay](finance-how-positive-pay.md).

Votre imprimante doit être correctement configurée pour les formulaires chèque, et vous devez définir la mise en page de chèque à utiliser. Pour plus d'informations, voir [Définir les mises en page de chèques](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Pour émettre des chèques
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.
2. Remplissez la feuille avec les paiements appropriés, par exemple à l'aide de la fonction Proposer paiements fournisseur. Pour plus d'informations, reportez vous à [Proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).
3. Dans le champ **Mode émission paiement** des lignes feuille pour le paiement que vous souhaitez effectuer avec des chèques, sélectionnez l'une des options suivantes :

   * **Informatique** : sélectionnez cette option si vous souhaitez imprimer un chèque du montant de la ligne feuille paiement. Vous devez imprimer les chèques avant de pouvoir valider les lignes feuille. Vous pouvez uniquement sélectionner **Informatique** si le **Type compte contrepartie** ou le **Type compte** est **Compte bancaire**.
   * **Manuel** : sélectionnez cette option si vous avez créé un chèque manuellement et que vous souhaitez créer une écriture comptable chèque correspondante de ce montant. Si vous utilisez cette option, vous ne pouvez pas imprimer de chèque à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous pouvez uniquement sélectionner **Manuel** si le **Type compte contrepartie** ou le **Type compte** est **Compte bancaire**.

     > [!NOTE]  
     >   Vous devez imprimer les chèques informatiques avant de valider les lignes feuille correspondantes.
4. Dans le cas de chèques informatiques, sélectionnez **Imprimer chèque**.
5. Dans la fenêtre **Chèque**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Cliquez sur le bouton **Imprimer**.

> [!NOTE]  
>   Si vous voulez imprimer des chèques en plusieurs devises sur des comptes bancaires différents, vous devez exécuter le traitement par lots **Imprimer chèque** pour chacune de ces devises et préciser le compte bancaire concerné.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Pour annuler des chèques imprimés qui ne sont pas validés
Vous pouvez annuler des chèques non validés après leur impression par l'intermédiaire de l'action **Annuler chèque** de la fenêtre **Feuille paiement**.

1. Dans la fenêtre **Feuille paiement**, sélectionnez **Annuler chèque**, puis sélectionnez les chèques à annuler.

## <a name="to-void-checks"></a>Pour annuler des chèques
Lorsque des paiements par chèque ont été validés, vous pouvez uniquement annuler des chèques à partir des écritures comptables banque ainsi obtenues.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez le compte bancaire approprié, sélectionnez l'action **Modifier**, puis l'action **Écritures comptables chèque**.
3. Dans la fenêtre **Écritures comptables chèque**, sélectionnez l'action **Annuler chèque**.
4. Cochez la case **Annuler chèque uniquement**.
5. Cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Exporter un fichier Positive Pay](finance-how-positive-pay.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

