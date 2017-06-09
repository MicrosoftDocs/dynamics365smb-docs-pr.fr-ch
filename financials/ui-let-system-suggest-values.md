---
title: "Laisser Dynamics 365 for Financials suggérer des valeurs | Microsoft Docs"
description: "Décrit comment faire en sorte que le système renseigner automatiquement les champs sélectionnés avec des valeurs que vous devriez sinon calculer et renseigner manuellement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 785ad537f81b8388aa14654f375599a13b66e3c5
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>Laisser Dynamics 365 for Financials suggérer des valeurs
[!INCLUDE[d365fin](includes/d365fin_md.md)] peut vous aider à effectuer ces tâches plus rapidement et précisément en préremplissant les champs ou en complétant les lignes avec des données que vous devriez sinon calculer et saisir vous-même. Bien qu'une telle saisie de données automatisée soit toujours correcte, vous pouvez la modifier par la suite si vous le souhaitez.

La fonctionnalité qui saisit les valeurs de champ pour vous est en général proposée pour les tâches qui demandent la saisie de volumes importants de données transactionnelles et pour lesquelles vous souhaitez éviter les erreurs et gagner du temps. Cette rubrique contient une sélection de ces fonctionnalités. Davantage de sections seront ajoutées dans les prochaines mises à jour de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>La case à cocher **Suggérer le montant contrepartie** dans la fenêtre **Noms feuille comptabilité**
Lorsque, par exemple, vous saisissez des lignes feuille comptabilité pour plusieurs frais qui doivent tous être validés dans le même compte bancaire, chaque fois que vous saisissez une nouvelle ligne feuille pour les frais, vous pouvez faire en sorte que le champ **Montant** de la ligne compte bancaire soit automatiquement mis à jour avec le montant qui équilibre les frais. Pour plus d'informations sur l'utilisation des feuilles comptabilité, reportez-vous à [Utilisation des feuilles comptabilité](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Pour que le champ **Montant** sur les lignes feuille comptabilité contrepartie soit renseigné automatiquement
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuilles comptabilité**, puis sélectionnez le lien associé.
2. Sur la ligne du nom de votre feuille comptabilité favorite, cochez la case **Suggérer le montant contrepartie**.
3. Ouvrez la feuille comptabilité commencez à enregistrer et valider des transactions en utilisant la fonctionnalité décrite pour la saisie automatique d'une valeur de champ.       

Pour plus d'informations sur la procédure permettant de configurer un nom de feuille comptabilité personnel, par exemple pour la gestion des frais, reportez-vous à [Utilisation des feuilles comptabilité](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Le champ **Renseigner automatiquement la date de réception** de la fenêtre **Enregistrement de paiement**
La fenêtre **Enregistrement de paiement** affiche les arriérés de paiement entrants sous la forme de lignes représentant les documents vente pour lesquels un montant doit être payé. Pour plus d'informations sur le lettrage des paiements client, reportez-vous à [Procédure : rapprocher les paiements client manuellement à partir de la liste des documents vente échus](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Vos tâches principales dans cette fenêtre consistent à cocher la case **Paiement effectué** et à renseigner le champ **Date de réception**. Vous pouvez définir [!INCLUDE[d365fin](includes/d365fin_md.md)] de sorte à saisir automatiquement la date de travail dans le champ **Date de réception** lorsque vous cochez la case **Paiement effectué**.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Pour que le champ **Date de réception** de la fenêtre **Enregistrement de paiement** soit automatiquement renseigné
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramétrage de l'enregistrement de paiement**, puis sélectionnez le lien associé.
2. Cochez la case **Renseigner automatiquement la date de réception**.
3. Ouvrez la fenêtre **Enregistrement de paiement** et commencer à traiter les paiements client entrants à l'aide de la fonctionnalité décrite pour la saisie automatique d'une valeur de champ.

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finance](Finance.md)


