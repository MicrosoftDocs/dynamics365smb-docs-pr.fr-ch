---
title: "Configurer des lignes standard pour les ventes et achats récurrents| Microsoft"
description: "Vous pouvez définir des lignes vente et des lignes achat que vous utilisez fréquemment et les insérer dans des documents achat et vente pour remplir rapidement les lignes avec des informations standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f8c8f96e73f6ba119e4345c8ba12c895dd212da3
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Créer des lignes ventes et achat récurrentes
Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.  

Les procédures suivantes indiquent comment utiliser des lignes ventes standard sur les factures vente. Cela fonctionne de manière similaire pour tous les documents vente et pour tous les documents achat.  

## <a name="to-set-up-standard-sales-lines"></a>Configurer des lignes ventes standard  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lignes vente standard**, puis choisissez le lien associé.  
2. Sur la page **Lignes vente standard**, cliquez sur l'action **Nouveau**.  
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Dans le raccourci **Lignes**, renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d'utiliser comme lignes récurrentes sur les documents ventes.  

> [!NOTE]
> Vous ne pouvez pas définir des prix sur les lignes vente standard car les prix, les remises, etc. sont calculés sur les documents vente réels après avoir inséré les lignes vente standard.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Pour affecter des lignes vente standard à des clients
Affectez une ou plusieurs lignes vente standard à un client afin qu'elles soient disponibles pour insérer sur les documents vente pour ce client.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la fiche pour un client concerné.
3. Choisissez l'action **Lignes vente récurrentes**.
4. Sur la page **Lignes vente récurrentes**, sélectionnez les codes des lignes vente récurrentes que vous souhaitez pouvoir insérer sur les documents vente du client.
5. Renseignez les champs supplémentaires pour définir quand, comment et où les lignes vente récurrentes doivent être utilisées. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Pour insérer des lignes vente récurrentes dans une facture vente
Si des lignes vente récurrentes existent pour le client, vous pouvez les insérer sur tous les types de documents vente, par exemple une facture vente. Si vous avez activé la notification concernée, vous serez informé si des lignes vente récurrentes existent.
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures**, puis sélectionnez le lien associé.
2. Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.
3. Choisissez l'action **Extraire les lignes vente récurrentes**.
4. Sur la page **Lignes vente récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes vente standard.

    > [!NOTE]
    > Pour utiliser les lignes vente récurrentes définies avec le traitement par lots **Créer des factures vente récurrentes**, vous devez également renseigner les champs **Date début validité** et **Date fin validité** sur la page **Lignes vente récurrentes**. Pour plus d'informations, voir la section « Pour créer plusieurs factures vente basées sur des lignes vente standard ».

5. Cliquez sur le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Pour créer plusieurs factures vente basées sur des lignes vente standard
Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente standard qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans les lignes vente standard.

> [!NOTE]
> Sur la page **Lignes vente récurrentes**, vous pouvez également spécifier un mode et un mandat de prélèvement. Les factures vente qui sont créées avec le traitement par lots **Créer des factures vente récurrentes** incluront ensuite les informations requises pour collecter le paiement pour les factures vente par prélèvement automatique SEPA. Pour plus d'informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Créer des factures vente récurrentes**, puis sélectionnez le lien associé.
2. Sur la page **Créer des factures vente récurrentes**, renseignez les champs selon les besoins.
3. Dans le champ de filtre **Code**, entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.
4. Cliquez sur le bouton **OK**.

Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

