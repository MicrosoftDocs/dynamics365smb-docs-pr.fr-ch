---
title: Configurer des lignes standard pour les ventes et achats récurrents| Microsoft
description: Vous pouvez définir des lignes vente et des lignes achat que vous utilisez fréquemment et les insérer dans des documents achat et vente pour remplir rapidement les lignes avec des informations standard.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 66a0e679a97bff7071a20197c804143cf11539d2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910495"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Créer des lignes ventes et achat récurrentes
Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.  

Les procédures suivantes indiquent comment utiliser des lignes ventes standard sur les factures vente. Cela fonctionne de manière similaire pour tous les documents vente et pour tous les documents achat.  

## <a name="to-set-up-recurring-sales-lines"></a>Pour configurer des lignes vente récurrentes

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lignes vente récurrentes** , puis sélectionnez le lien associé.  
2. Sur la page **Lignes vente récurrentes** , cliquez sur l’action **Nouveau** .  
3. Sur le raccourci **Général** , complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Dans le raccourci **Lignes** , renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d’utiliser comme lignes récurrentes sur les documents ventes.  

> [!NOTE]
> Vous ne pouvez pas définir des prix sur les lignes vente récurrentes, car les prix, les remises, etc. sont calculés sur les documents vente réels après avoir inséré les lignes vente récurrentes.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Pour affecter des lignes vente récurrentes à un client

Affectez une ou plusieurs lignes vente récurrentes à un client afin qu’elles soient disponibles pour insertion sur les documents vente pour ce client.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients** , puis sélectionnez le lien associé.
2. Ouvrez la fiche pour un client concerné.
3. Choisissez l’action **Lignes vente récurrentes** .
4. Sur la page **Lignes vente récurrentes** , sélectionnez les codes des lignes vente récurrentes que vous souhaitez pouvoir insérer sur les documents vente du client.
5. Renseignez les champs supplémentaires pour définir quand, comment et où les lignes vente récurrentes doivent être utilisées.  

    Si vous prévoyez d’utiliser les lignes vente récurrentes définies avec le traitement par lots **Créer des factures vente récurrentes** , utilisez les champs **Date début validité** et **Date fin validité** pour définir quand les lignes vente récurrentes sont utilisées pour créer des factures. Pour plus d’informations, voir [Pour créer plusieurs factures vente basées sur des lignes vente standard](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Vous pouvez également spécifier un mode et un mandat de prélèvement. Les factures vente qui sont créées avec le traitement par lots **Créer des factures vente récurrentes** incluront ensuite les informations requises pour collecter le paiement par prélèvement automatique SEPA. Pour plus d’informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).

6. Dans les quatre champs où vous sélectionnez la façon dont les lignes sont insérées dans les quatre types de document, sélectionnez l’une des options suivantes :

|Option|Description|
|------|-----------|
|**Manuel**|Vous devez rechercher et insérer manuellement une ligne vente récurrente existante pour le client.|
|**Automatique**|Si plusieurs lignes vente récurrentes existent pour le client, vous recevrez une notification pour vous permettre de sélectionner la ligne à insérer. Si une seule ligne vente récurrente existe, elle sera insérée automatiquement.<br /><br />Notez que cela ne fonctionne que si le nouveau document a été créé à partir d’une liste de documents, par exemple en sélectionnant l’action **Nouveau** sur la page **Commandes vente** . Cela ne fonctionne pas si le document a été créé à partir d’une fiche client, par exemple.|
|**Toujours demander**|Une notification s’affiche et toutes les lignes vente récurrentes existantes sont affichées afin que vous puissiez en sélectionner une.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Pour insérer des lignes vente récurrentes dans une facture vente

Si des lignes vente récurrentes existent pour le client, vous pouvez les insérer ou demander à les insérer sur tous les types de documents vente, par exemple une facture vente. Si vous avez activé les options **Toujours demander** , vous serez informé si des lignes vente récurrentes existent.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures** , puis sélectionnez le lien associé.
2. Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.
3. Choisissez l’action **Extraire les lignes vente récurrentes** .
4. Sur la page **Lignes vente récurrentes** , cliquez sur le bouton de recherche du champ **Code** , puis sélectionnez un ensemble de lignes vente standard.
5. Cliquez sur le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Pour créer plusieurs factures vente à partir de lignes vente récurrentes
Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente standard qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans les lignes vente standard.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Créer des factures vente récurrentes** , puis sélectionnez le lien associé.
2. Sur la page **Créer des factures vente récurrentes** , renseignez les champs selon les besoins.
3. Dans le champ de filtre **Code** , entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.
4. Cliquez sur le bouton **OK** .

Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
