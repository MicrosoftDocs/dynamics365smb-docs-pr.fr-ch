---
title: Approuver ou rejeter des documents dans les flux| Microsoft Docs
description: "Demander, rejeter, ou déléguer une approbation de, par exemple, un document achat ou vente, dans le cadre d'un flux de travail."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ffeffe725025dc03d2053333f75249679103b6a4
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-approval-workflows"></a>Procédure : utilisation des flux d'approbation
Lorsqu'un enregistrement, tel qu'un document achat ou une fiche client, doit être approuvé par un membre de votre organisation, vous envoyez une approbation demande achat dans le cadre d'un workflow. Selon la configuration du workflow, l'approbateur approprié est informé que l'enregistrement requiert son approbation.

Vous configurez les flux d'approbation dans la fenêtre **Flux de travail**.

Les flux d'approbation de base pour les documents achat, les documents vente, les feuilles paiement, les fiches client et les fiches article sont prêts à être utilisés dans le cadre de la configuration assistée. Pour en savoir plus, voir [Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Faire une demande d'approbation d'un enregistrement
La tâche suivante est effectuée par un utilisateur d'approbation.

1. Dans la fenêtre qui affiche l'enregistrement, sélectionnez l'action **Envoyer demande d'approbation**.
2. Pour afficher toutes vos demandes d'approbation, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Écritures demande d'approbation**, puis sélectionnez le lien connexe.  

Le statut de l’écriture approbation passe de **Créé** à **Ouvert**. Le statut de l'enregistrement, par exemple une facture achat, est mis à jour du statut **Ouvert** à **Approbation en attente** et reste verrouillé au traitement jusqu'à ce que tous les approbateurs aient approuvé l'enregistrement.

Lorsque l'approbateur a approuvé l'enregistrement, le statut passe à **Validé**. Vous pouvez ensuite effectuer vos tâches avec l'enregistrement.

## <a name="to-cancel-requests-for-approval"></a>Pour annuler des demandes d'approbation
La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.

Un client peut souhaiter modifier une commande après sa soumission pour approbation. Dans ce cas, vous pouvez annuler le processus d'approbation et apporter les modifications nécessaires à la commande avant de refaire une demande d'approbation.

- Dans la fenêtre qui affiche l'enregistrement, sélectionnez l'action **Annuler demande d'approbation**.

Lorsque la demande d'approbation a été annulée, le statut de l'écriture de l'approbation connexe passe à **Annulé**. Le statut de l’enregistrement est mis à jour d'**Approbation en attente** à **Ouvert**. Le processus d'approbation peut alors redémarrer.

## <a name="to-make-minor-changes-to-approved-records"></a>Pour apporter des modifications minimes à des enregistrements approuvés
Si vous souhaitez effectuer les modifications minimes à un enregistrement après son approbation, rouvrez l'enregistrement, effectuez les modifications, puis libérez-le. Pour des modifications minimes, effectuez ces opérations avec les boutons **Rouvrir** et **Libérer**

1. Ouvrez la fenêtre qui affiche les enregistrements, par exemple une facture achat, puis sélectionnez l'action **Rouvrir**.

    Le champ **Statut du document** est modifié sur **Ouvrir**.
2. Effectuez les modifications nécessaires à l'enregistrement, comme l'adresse du fournisseur.
3. Sélectionnez l'action **Lancer**.

Lorsque vous rouvrez l'enregistrement source, le statut de l'écriture approuvée associée reste Approuvée dans la fenêtre **Écritures approbation**.

## <a name="to-approve-or-reject-requests-for-approval"></a>Pour approuver ou rejeter les demandes d'approbation
La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.

Vous pouvez traiter les demandes d'approbation dans la fenêtre **Demandes à approuver**, par exemple, afin d'approuver plusieurs demandes à la fois. Sinon, vous pouvez traiter chaque demande sur l'enregistrement connexe, par exemple la fenêtre **Facture achat**, en sélectionnant le lien dans la notification que vous recevez.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Demandes à approuver**, puis choisissez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour l'enregistrement ou les enregistrements que vous voulez approuver ou rejeter.
3. Choisissez l'action **Approuver**, **Rejeter** ou **Déléguer**.

Lorsqu'un enregistrement a été approuvé ou rejeté, le statut d'approbation dans le champ **Statut** passe à **Approuvé** ou **Rejeté**.

Si une hiérarchie d'approbateurs est configurée, le statut enregistrement sera **Approbation en attente** jusqu'à ce que tous les approbateurs aient approuvé l'enregistrement. Le statut de l'enregistrement passe à **Validé**.

Simultanément, le statut d'approbation passe de **Créé** à **Ouvert** dès qu'une demande d'approbation est créée pour l'enregistrement. Si la demande est rejetée, le statut d'approbation passe à **Rejeté**. Le statut reste sur **Ouvert** ou **Rejeté** jusqu'à ce que tous les approbateurs aient approuvé la demande.

## <a name="to-delegate-requests-for-approval"></a>Pour déléguer des demandes d'approbation
La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.

Pour éviter que des documents ne s'accumulent ou encore bloquent le workflow, l'approbateur et l'administrateur d'approbation peuvent déléguer une demande d'approbation à un approbateur remplaçant. Le remplaçant peut être soit un remplaçant désigné, l'approbateur direct, soit l'administrateur d'approbation, dans cet ordre de priorité. Généralement, cette fonction est utilisée si un approbateur est absent et dans l'impossibilité d'approuver des demandes avant la date d'échéance.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Demandes à approuver**, puis choisissez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour les demandes d'approbation à déléguer à un approbateur remplaçant, puis sélectionnez l'action **Déléguer**.

Une notification pour approuver la demande est envoyée à l'approbateur remplaçant.

## <a name="to-manage-overdue-approval-requests"></a>Pour gérer des demandes d'approbation échues
La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.

Vous devez rappeler régulièrement aux utilisateurs du workflow d'approbation qu'ils doivent répondre aux demandes d'approbations échues. Pour cela, utilisez la fonction **Envoyer des notifications d'approbations échues**.

La fonction **Envoyer des notifications d'approbations échues** passe en revue toutes les demandes d'approbation ouvertes qui sont actuellement échues. Chaque approbateur ayant au moins une écriture approbation échue reçoit une notification avec la liste de toutes leurs demandes d'approbation échues. La notification est également envoyée à leur approbateur et à tous les demandeurs des approbations échues. Cela est utile si l'écriture d'approbation échue doit être déléguée à un remplaçant.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Demandes approbation échues**, puis choisissez le lien associé.
2. Dans la fenêtre **Demandes approbations échues**, sélectionnez l'action **Envoyer les notifications d'approbation échues**.

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)    
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

