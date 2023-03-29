---
title: Champ statut sur les documents
description: "En savoir plus sur le statut «\_En cours\_» et «\_Lancé\_» figurant sur les documents de devis, de commande ou d’avoir."
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# Champ statut sur les documents

Lorsque vous créez un devis, un ordre ou un avoir, le champ **Statut** sur l’en-tête du document indique par défaut le statut **En cours**.

Après avoir renseigné le document, vous pouvez le lancer et [!INCLUDE[prod_short](includes/prod_short.md)] modifie la valeur du champ **Statut** en **Lancé**. Cet état indique que la commande est prête pour l’étape de traitement suivante avant qu’elle soit validée.

| Statut | Désignation |
| ------ | ----------- |
| Ouvrir   | Vous pouvez apporter des modifications à ce document. |
| Lancé | Le document a été lancé vers l’étape suivante du traitement et vous ne pouvez pas modifier les lignes de type *Article* et *Immobilisation*.<br /><br />Vous pouvez rouvrir un document lancé pour le modifier. Pour transférer le document modifié vers l’étape suivante du traitement, vous devez le lancer une nouvelle fois. |
| Approbation suspendue   | Le document est en attente d’approbation. |
| Acompte en attente | Une facture acompte a été validée pour ce document. |

## Traitement des versions

Vous pouvez utiliser le processus de lancement de différentes manières afin de faciliter le flux de travail normal, et de suivre, par exemple, les procédures de la société concernant les approbations ou l’état des activités entrepôt.

### Procédures d’approbation

Votre société peut utiliser la procédure de lancement pour indiquer qu’un autre utilisateur a approuvé le document, ou qu’un contact externe peut répondre aux spécifications du document, comme l’indiquent les exemples suivants :

* Vous pouvez uniquement lancer une commande achat lorsque le fournisseur vous a indiqué qu’il est en mesure d’y répondre.
* Vous créez un ordre et un deuxième utilisateur doit l’approuver (par exemple, pour des raisons de sécurité) avant que vous soyez autorisé à le lancer.
* L’avoir que vous avez créé doit être lancé par le responsable chargé d’approuver tous les remboursements.

En savoir plus sur les flux de travail approbation sur [Utiliser les flux de travail](across-use-workflows.md).

### Activités entrepôt

Si le statut de l’ordre est **En cours**, l’entrepôt ne commence pas à préparer l’expédition et ne prévoit pas de recevoir les articles d’une commande achat. Lorsque vous lancez l’ordre, vous indiquez qu’il est terminé et que l’entrepôt peut l’inclure dans ses activités.

## Réouverture d’un ordre lancé

Vous pouvez modifier un ordre lancé en le rouvrant. Cependant, vous pouvez uniquement augmenter la quantité de lignes déjà traitées par l’entrepôt.

Lorsque vous avez modifié l’ordre et que vous le relancez, [!INCLUDE [prod_short](includes/prod_short.md)] calcule à nouveau la TVA et la remise facture.

Si vous apportez des modifications à un ordre lancé, vous devez les notifier à l’entrepôt.

> [!NOTE]
> Si vous souhaitez valider un seul ordre ouvert ou un avoir sans le lancer au préalable, [!INCLUDE [prod_short](includes/prod_short.md)] lance automatiquement le document lorsque vous le validez. Si vous validez des ordres ou des avoirs à l’aide de la fonction **Valider par lot**, vous pouvez uniquement valider ceux que vous avez lancés.

## Voir aussi

[Vente de produits avec une commande vente client](sales-how-sell-products.md)  
[Enregistrer les achats avec les factures achat](purchasing-how-record-purchases.md)  
[Expédier des articles](warehouse-how-ship-items.md)  
[Réceptionner des articles](warehouse-how-receive-items.md)  
[Utilisation des flux d’approbation](across-how-use-approval-workflows.md)  
[Tri, recherche et filtrage de listes](ui-enter-criteria-filters.md)  
[Archiver des documents](across-how-to-archive-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
