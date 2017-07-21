---
title: "Aperçu des tâches permettant de gérer vos achats | Microsoft Docs"
description: "Décrit les tâches permettant de gérer vos processus d'achat ou d'approvisionnement, y compris le fonctionnement des factures achat et des commandes achat."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Procédure d'achat
Vous créez une facture achat ou une commande achat pour enregistrer le coût d'achats et suivre les créances. Si vous devez contrôler un stock, les factures achat sont également utilisées pour mettre à jour de manière dynamique les niveaux de stock afin que vous puissiez réduire vos coûts et fournir un meilleur service client. Le prix d'achat, notamment les frais de service, et les valeurs de stocks qui résultent de la validation des factures achat contribuent aux chiffres du profit et à d'autres KPI financiers sur votre page d'accueil.

Vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d'une quantité de commande, par exemple, si la quantité totale n'était pas disponible auprès du fournisseur. Si vous commercialisez des articles en les livrant directement depuis votre fournisseur auprès de votre client, vous devez également utiliser les commandes achat. Pour plus d'informations, voir [Procédure : effectuer des livraisons directes](sales-how-drop-shipment.md). Pour tous les autres aspects, les commandes achat fonctionnent de la même manière que les factures achat.

Les factures achat peuvent être créées automatiquement en utilisant le service de reconnaissance optique de caractères (OCR) pour convertir les factures PDF de vos fournisseurs en documents électroniques qui sont ensuite convertis en factures achat par un flux de travail. Pour utiliser cette fonctionnalité, vous devez d'abord vous inscrire au service OCR, puis effectuer diverses configurations. Pour plus d'informations, reportez vous à [Procédure : traiter les documents entrants](across-process-income-documents.md).      

Les produits peuvent être des articles en stock et des services. Pour plus d'informations, reportez vous à [Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md).

Pour tous les processus d'achat, vous pouvez incorporer un flux de travail d'approbation, par exemple, pour exiger que les achats en grande quantité soient approuvés par le responsable de la comptabilité. Pour plus d'informations, reportez-vous à [Procédure : utilisation des flux d'approbation](across-how-use-approval-workflows.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent. Ces tâches sont répertoriées dans l'ordre de leur exécution en règle générale.

| Pour | Voir |
| --- | --- |
| Créer une facture achat pour enregistrer votre accord avec un fournisseur pour acheter des biens selon certaines conditions de livraison et de paiement. |[Procédure : enregistrer des achats](purchasing-how-record-purchases.md) |
| Créer une facture achat pour toutes les lignes ou pour les lignes sélectionnées sur une facture vente. |[Procédure : acheter des articles pour une vente](purchasing-how-purchase-products-sale.md) |
| Effectuer une action sur une facture achat enregistrée impayée pour créer automatiquement un avoir et soit annuler la facture achat, soit la recréer pour que vous puissiez y apporter des corrections. |[Procédure : corriger ou annuler des factures vente impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Créer un avoir achat pour rembourser une facture achat validée spécifique pour indiquer les produits que vous retournez au fournisseur et le montant règlement que vous récupérez. |[Procédure : traiter les retours ou annulations d'achats](purchasing-how-register-new-vendors.md) |
| Créer une fiche fournisseur pour chaque fournisseur auquel vous achetez des biens. |[Procédure : enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Voir aussi
[Définition des achats](purchasing-setup-purchasing.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Gérer des projets](projects-manage-projects.md)    
[Chaîne d'approvisionnement](madeira-supply-chain.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
