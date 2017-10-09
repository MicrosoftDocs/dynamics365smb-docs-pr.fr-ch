---
title: "Enregistrer les frais ou des revenus directement dans la comptabilité| Microsoft Docs"
description: "Pour les activités économiques qui ne sont pas représentés par un document, comme de plus petits frais ou règlements, vous pouvez créer les transactions associées en validant des lignes de feuille dans la fenêtre Feuille comptabilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 43065620f34a7ef02e5247e78acf306500f82d90
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Procédure : Valider les transactions directement vers la comptabilité
La plupart des transactions financières sont validées en comptabilité via les documents commerciaux dédiés, tels que des factures achat et des commandes vente. Pour les activités économiques qui ne sont pas représentés par un document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], comme de plus petits frais ou règlements, vous pouvez créer les transactions associées en validant des lignes de feuille dans la fenêtre **Feuille comptabilité**.

Une utilisation classique de la feuille comptabilité est de valider les dépenses des salariés avec leurs fonds propres au cours des activités commerciales, pour un remboursement ultérieur. Pour plus d'informations, voir [Procédure : enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).

Les feuilles comptabilité valident les transactions financières dans les comptes généraux et d'autres comptes tels que les comptes bancaires, clients, fournisseurs et employés. La validation avec une feuille comptabilité crée toujours des écritures dans les comptes généraux. C'est le cas même lorsque, par exemple, vous validez une ligne feuille dans un compte client, parce qu'une écriture est validée dans un compte client de la comptabilité via un groupe comptabilisation. Vous pouvez personnaliser votre version d'une feuille comptabilité en configurant un nom de feuille ou un modèle feuille. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).

Contrairement aux écritures qui sont validées avec des documents qui nécessitent un processus d'avoir, vous pouvez correctement contrepasser les écritures validées avec la feuille comptabilité. Pour plus d'informations, reportez-vous à [Procédure : inversion d'une validation](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Pour valider une transaction directement vers la comptabilité
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles comptabilité**, puis sélectionnez le lien connexe.
2. Ouvrez la feuille comptabilité appropriée. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).
3. Sur une nouvelle ligne feuille, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Répétez l'étape 3 pour toutes les transactions distinctes que vous souhaitez valider.

    > [!TIP]  
    > Si vous souhaitez saisir les lignes de transaction au-dessus d'une ligne compte contrepartie, par exemple, pour un compte bancaire, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot dans la fenêtre **Noms feuilles comptabilité**. Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les transactions.
5. Choisissez l'action **Valider** pour enregistrer les transactions sur les comptes généraux spécifiés.

## <a name="see-also"></a>Voir aussi
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Procédure : enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md)  
[Procédure : inversion d'une validation](finance-how-reverse-journal-posting.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

