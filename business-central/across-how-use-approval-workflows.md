---
title: Approuver ou rejeter des documents dans les flux| Microsoft Docs
description: Demander, rejeter, ou déléguer une approbation de, par exemple, un document achat ou vente, dans le cadre d’un flux de travail.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: 46c81fa887af70e7a2f516df38ec003392b1dabd
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079365"
---
# <a name="use-approval-workflows"></a>Utilisation des flux d’approbation

Lorsqu’un enregistrement, tel qu’un document achat ou une fiche client, doit être approuvé par un membre de votre organisation, vous envoyez une approbation demande achat dans le cadre d’un workflow. Selon la configuration du workflow, l’approbateur approprié est informé que l’enregistrement requiert son approbation.

Vous configurez les flux d’approbation sur la page **Flux de travail**. Vous devez également configurer les utilisateurs d’approbation, y compris les limites de montant pertinentes, dans la page **Paramètres utilisateur approbation**. Pour plus d’informations, reportez-vous à [Paramétrage des workflows](across-set-up-workflows.md).  

Outre les flux de travail approbation décrits dans cette rubrique, vous pouvez effectuer diverses autres tâches de flux de travail. Pour plus d’informations, voir [Utiliser des workflows](across-use-workflows.md).

Les flux d’approbation de base pour les documents achat, les documents vente, les feuilles paiement, les fiches client et les fiches article sont prêts à être utilisés dans le cadre de guides. Pour plus d’informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>Faire une demande d’approbation d’un enregistrement

La tâche suivante est effectuée par un utilisateur d’approbation.

1. Sur la page qui affiche l’enregistrement, sélectionnez l’action **Envoyer demande d’approbation**.
2. Pour voir toutes vos demandes d’approbation, choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **instances d’étape de workflow archivées**, puis sélectionnez le lien associé.  

Le statut de l’écriture approbation passe de **Créé** à **Ouvert**. Le statut de l’enregistrement, par exemple une facture achat, est mis à jour du statut **Ouvert** à **Approbation en attente** et reste verrouillé au traitement jusqu’à ce que tous les approbateurs aient approuvé l’enregistrement.

Lorsque l’approbateur a approuvé l’enregistrement, le statut passe à **Validé**. Vous pouvez ensuite effectuer vos tâches avec l’enregistrement.

## <a name="to-cancel-requests-for-approval"></a>Pour annuler des demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Un client peut souhaiter modifier une commande après sa soumission pour approbation. Dans ce cas, vous pouvez annuler le processus d’approbation et apporter les modifications nécessaires à la commande avant de refaire une demande d’approbation.

- Sur la page qui affiche l’enregistrement, sélectionnez l’action **Annuler demande d’approbation**.

Lorsque la demande d’approbation a été annulée, le statut de l’écriture de l’approbation connexe passe à **Annulé**. Le statut de l’enregistrement est mis à jour d’**Approbation en attente** à **Ouvert**. Le processus d’approbation peut alors redémarrer.

## <a name="to-approve-or-reject-requests-for-approval"></a>Pour approuver ou rejeter les demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Vous pouvez traiter les demandes d’approbation sur la page **Demandes à approuver**, par exemple, afin d’approuver plusieurs demandes à la fois. Sinon, vous pouvez traiter chaque demande sur l’enregistrement connexe, par exemple la page **Facture achat**, en sélectionnant le lien dans la notification que vous recevez.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes à approuver**, puis sélectionnez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour l’enregistrement ou les enregistrements que vous voulez approuver ou rejeter.
3. Choisissez l’action **Approuver**, **Rejeter** ou **Déléguer**.

Lorsqu’un enregistrement a été approuvé ou rejeté, le statut d’approbation dans le champ **Statut** passe à **Approuvé** ou **Rejeté**.

Si une hiérarchie d’approbateurs est configurée, le statut enregistrement sera **Approbation en attente** jusqu’à ce que tous les approbateurs aient approuvé l’enregistrement. Le statut de l’enregistrement passe à **Validé**.

Simultanément, le statut d’approbation passe de **Créé** à **Ouvert** dès qu’une demande d’approbation est créée pour l’enregistrement. Si la demande est rejetée, le statut d’approbation passe à **Rejeté**. Le statut reste sur **Ouvert** ou **Rejeté** jusqu’à ce que tous les approbateurs aient approuvé la demande.

## <a name="to-delegate-requests-for-approval"></a>Pour déléguer des demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Pour éviter que des documents ne s’accumulent ou encore bloquent le workflow, l’approbateur et l’administrateur d’approbation peuvent déléguer une demande d’approbation à un approbateur remplaçant. Le remplaçant peut être soit un remplaçant désigné, l’approbateur direct, soit l’administrateur d’approbation, dans cet ordre de priorité. Généralement, cette fonction est utilisée si un approbateur est absent et dans l’impossibilité d’approuver des demandes avant la date d’échéance.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes à approuver**, puis sélectionnez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour les demandes d’approbation à déléguer à un approbateur remplaçant, puis sélectionnez l’action **Déléguer**.

Une notification pour approuver la demande est envoyée à l’approbateur remplaçant.

## <a name="to-manage-overdue-approval-requests"></a>Pour gérer des demandes d’approbation échues

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Vous devez rappeler régulièrement aux utilisateurs du workflow d’approbation qu’ils doivent répondre aux demandes d’approbations échues. Pour cela, utilisez la fonction **Envoyer des notifications d’approbations échues**.

La fonction **Envoyer des notifications d’approbations échues** passe en revue toutes les demandes d’approbation ouvertes qui sont actuellement échues. Chaque approbateur ayant au moins une écriture approbation échue reçoit une notification avec la liste de toutes leurs demandes d’approbation échues. La notification est également envoyée à leur approbateur et à tous les demandeurs des approbations échues. Cela est utile si l’écriture d’approbation échue doit être déléguée à un remplaçant.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes approbations échues**, puis sélectionnez le lien associé.
2. Sur la page **Demandes approbations échues**, sélectionnez l’action **Envoyer les notifications d’approbation échues**.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/use-approval-workflows/)

## <a name="see-also"></a>Voir aussi

[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Ventes](sales-manage-sales.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]