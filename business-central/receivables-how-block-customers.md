---
title: Comment bloquer les ventes de clients
description: 'Si nécessaire, vous pouvez empêcher qu’un client soit ajouté aux documents de vente et d’autres transactions de vente.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="block-customers" />Bloquer des clients
Vous pouvez bloquer un client, par exemple à cause de son insolvabilité, afin que le client ne puisse pas être ajouté aux documents vente ou afin d’empêcher que d’autres transactions soient validées pour ce client.

En plus de bloquer un client, vous pouvez définir des transactions Comptabilité client pour le client soit en attente en association avec les relances. Pour plus d’informations, voir [Collecte des soldes restants](receivables-collect-outstanding-balances.md).   

Le tableau suivant décrit les options pour bloquer des clients.  

|Option|Description|  
|--------------------|------------|  
|**Vide**|Les transactions sont autorisés pour ce client.|
|**Expédier**|Vous ne pouvez pas créer des commandes et des expéditions pour ce client. Vous pouvez facturer les expéditions existantes qui ne l’ont pas encore été.|  
|**Facture**|Vous ne pouvez pas créer de commandes, d’expéditions ni de factures pour ce client. Vous ne pouvez pas facturer les expéditions existantes qui ne l’ont pas encore été. Vous pouvez toujours envoyer des rappels et des factures d’intérêts au client.|  
|**Tous**|Ce client n’est autorisé à effectuer aucune transaction, pas même un paiement.|  

## <a name="to-block-a-customer" />Pour bloquer un client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Sélectionnez un client, puis cliquez sur **Modifier**.
3. Dans le champ **Bloqué**, choisissez ce que vous souhaitez bloquer, comme décrit dans le tableau ci-dessus.

## <a name="see-also" />Voir aussi
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
[Collecte des soldes restants](receivables-collect-outstanding-balances.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
