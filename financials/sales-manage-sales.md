---
title: "Aperçu des tâches permettant de gérer la comptabilité fournisseur | Microsoft Docs"
description: "Décrit comment gérer les activités des ventes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 06/30/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ebdcfc8c2be94398c1ebd7d5268a94b568e3b23b
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="sales"></a>Ventes
Vous créez une facture vente ou une commande vente pour enregistrer votre accord avec un client pour vendre certains produits selon certaines conditions de livraison et de paiement.

Vous devez utiliser des commandes vente si votre processus de vente requiert que vous expédiiez des parties d'une quantité de commande, par exemple, si la quantité totale est pas disponible d'un coup. Si vous commercialisez des articles en les livrant directement du fournisseur au client, vous devez également utiliser les commandes vente. Pour tous les autres aspects, les commandes vente fonctionnent de la même manière que les factures vente.

Les pratiques recommandées en matière de vente et de marketing reposent toutes sur la prise de décisions appropriées au bon moment. La fonctionnalité Marketing de [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit une vue d'ensemble précise et opportune de vos informations de contact afin d'offrir des services à vos prospects de manière plus efficace et d'accroître la satisfaction de la clientèle. Pour plus d'informations, reportez-vous à [Gestion des relations](marketing-relationship-management.md).

Vous pouvez négocier avec le client en créant d'abord un devis, que vous pouvez convertir en facture vente lorsque vous êtes d'accord sur la vente. Une fois que le client a confirmé l'accord, par exemple après une procédure de devis, vous pouvez envoyer une confirmation de commande pour enregistrer votre obligation de fournir les produits comme convenu.

Lorsque vous fournissez les produits, entièrement ou partiellement, vous validez la facture vente ou la commande vente comme étant expédiée ou expédiée et facturée pour créer l'article et les écritures comptables client associés dans votre système.

Dans les environnements d'entreprise où le client doit payer avant la livraison des produits vendus (par exemple la vente au détail), vous devez attendre la réception du paiement avant de fournir les produits. Dans la plupart des cas, vous traitez les paiements entrants plusieurs semaines après la livraison en lettrant les paiements à leurs factures vente validées et impayées associées. Pour plus d'informations, reportez-vous à [Procédure : rapprocher les paiements à l'aide de l'application automatique](receivables-how-reconcile-payments-auto-application.md).

Vous pouvez facilement corriger ou annuler une facture vente validée avant qu'elle ne soit payée. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si le client demande une modification tôt dans le processus de commande. Si la facture vente validée est payée, vous devez créer un avoir vente pour contrepasser la vente.

Les documents vente peuvent être envoyés sous forme de fichiers PDF joints à l'e-mail. Le corps du message contient alors un extrait du document vente, comme les produits, le montant total et un lien vers le site Paypal. Pour plus d'informations, reportez vous à [Procédure : envoyer des documents par e-mail](ui-how-send-documents-email.md).

Pour tous les processus de vente, vous pouvez incorporer un flux de travail d'approbation, par exemple, pour exiger que les ventes en grande quantité à certains clients soient approuvés par le responsable de la comptabilité. Pour plus d'informations, reportez-vous à [Utilisation des flux d'approbation](across-how-use-approval-workflows.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Créer un devis dans lequel vous proposer des biens selon des conditions négociables avant de convertir le devis en facture vente. |[Procédure : créer des offres](sales-how-make-offers.md) |
| Créer une facture vente pour enregistrer votre accord avec un client pour vendre des biens selon certaines conditions de livraison et de paiement. |[Procédure : facturer des ventes](sales-how-invoice-sales.md) |
| Traiter une commande vente qui implique un envoi partiel ou un envoi direct. |[Procédure : vendre des produits](sales-how-sell-products.md) |
|Paramétrez les lignes vente ou achat standard que vous pouvez rapidement insérer dans les documents, par exemple, pour les ordres de réapprovisionnement récurrents.|[Procédure : Créer des lignes ventes et achat récurrentes](sales-how-work-standard-lines.md)|  
| Lier une commande vente à un bon de commande pour vendre un article qui sera livré directement par votre fournisseur à votre client. |[Procédure : effectuer des livraisons directes](sales-how-drop-shipment.md) |
| Effectuer une action sur une facture vente enregistrée impayée pour créer automatiquement un avoir et soit annuler la facture vente, soit la recréer pour que vous puissiez y apporter des corrections. |[Procédure : corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md) |
| Créer un avoir vente pour rembourser une facture vente validée spécifique pour indiquer les produits que retourné par le client et le montant règlement que vous remboursez. |[Procédure : traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md) |
| Créer une fiche client pour chaque client auquel vous vendez des éléments. |[Procédure : enregistrer de nouveaux clients](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Voir aussi
[Définition des ventes](sales-setup-sales.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Gestion des comptes fournisseur](payables-manage-payables.MD)  
[Gestion de projets](projects-manage-projects.md)    
[Chaîne d'approvisionnement](madeira-supply-chain.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

