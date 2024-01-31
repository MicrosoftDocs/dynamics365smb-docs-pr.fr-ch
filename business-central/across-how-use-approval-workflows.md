---
title: Approuver ou rejeter des documents dans les flux de travail
description: 'Demander, rejeter, ou déléguer une approbation de, par exemple, un document achat ou vente, dans le cadre d’un flux de travail.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procédure : utilisation des flux d’approbation

Lorsqu’un enregistrement, tel qu’un document achat ou une fiche client, doit être approuvé par un membre de votre organisation, vous envoyez une approbation demande achat dans le cadre d’un workflow. Selon la configuration du workflow, l’approbateur approprié est informé que l’enregistrement requiert son approbation.

Vous configurez les flux d’approbation sur la page **Flux de travail**. Vous devez également configurer les utilisateurs d’approbation, y compris les limites de montant pertinentes, dans la page **Paramètres utilisateur approbation**. En savoir plus sur [Configurer des utilisateurs d’approbation](across-set-up-workflows.md).  

Outre les flux de travail approbation décrits dans cet article, vous pouvez effectuer diverses autres tâches de flux de travail. En savoir plus sur [Utiliser des flux de travail approbation](across-use-workflows.md).

Les flux d’approbation de base pour les documents achat, les documents vente, les feuilles paiement, les fiches client et les fiches article sont prêts à être utilisés dans le cadre de guides. En savoir plus, [Préparation aux activités commerciales](ui-get-ready-business.md).

## Demander une approbation d’enregistrement

La tâche suivante est effectuée par un utilisateur d’approbation.

1. Sur la page qui affiche l’enregistrement, sélectionnez l’action **Envoyer demande d’approbation**.
2. Pour voir toutes vos demandes d’approbation, choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez les **écritures demande d’approbation**, puis sélectionnez le lien associé.  

Le statut de l’écriture approbation passe de **Créé** à **Ouvert**. Le statut de l’enregistrement (par exemple, une facture achat), est mis à jour du statut **Ouvert** à **Approbation en attente** et reste verrouillé au traitement jusqu’à ce que tous les approbateurs aient approuvé l’enregistrement.

Lorsque tous les approbateurs ont approuvé l’enregistrement, le statut passe à **Validé**. Vous pouvez ensuite effectuer votre travail avec l’enregistrement.

## Annuler demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Un client peut souhaiter modifier une commande après sa soumission pour approbation. Dans ce cas, vous pouvez annuler le processus d’approbation et apporter les modifications nécessaires à la commande avant de refaire une demande d’approbation.

- Sur la page qui affiche l’enregistrement, sélectionnez l’action **Annuler demande d’approbation**.

Lorsque la demande d’approbation a été annulée, le statut de l’écriture de l’approbation connexe passe à **Annulé**. Le statut de l’enregistrement est mis à jour d’**Approbation en attente** à **Ouvert**. Le processus d’approbation peut alors redémarrer.

## Approuver ou rejeter les demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Vous pouvez traiter les demandes d’approbation sur la page **Demandes à approuver**, par exemple, afin d’approuver plusieurs demandes à la fois. Vous pouvez également approuver des enregistrements individuels en choisissant le lien dans la notification que vous recevez.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes à approuver**, puis sélectionnez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour l’enregistrement ou les enregistrements que vous voulez approuver ou rejeter.
3. Choisissez l’action **Approuver**, **Rejeter** ou **Déléguer**.

Lorsqu’un enregistrement a été approuvé ou rejeté, le statut d’approbation dans le champ **Statut** passe respectivement sur **Approuvé** ou **Rejeté**.

Si une hiérarchie d’approbateurs est configurée, le statut enregistrement sera **Approbation en attente** jusqu’à ce que tous les approbateurs sollicités aient approuvé l’enregistrement. Le statut de l’enregistrement passe à **Validé**.

Simultanément, le statut d’approbation passe de **Créé** à **Ouvert** dès qu’une demande d’approbation est créée pour l’enregistrement. Si la demande est rejetée, le statut d’approbation passe à **Rejeté**. Le statut reste sur **Ouvert** ou **Rejeté** jusqu’à ce que tous les approbateurs aient approuvé la demande.

## Déléguer demandes d’approbation

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

Pour éviter que des enregistrements ne s’accumulent ou encore bloquent le flux de travail, l’approbateur et l’administrateur d’approbation peuvent déléguer une demande d’approbation à un approbateur remplaçant. Le remplaçant peut être soit un remplaçant désigné, l’approbateur direct, soit l’administrateur d’approbation, dans cet ordre de priorité. Généralement, cette fonction est utilisée si un approbateur n’est pas disponible ou dans l’impossibilité d’approuver des demandes avant la date d’échéance.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes à approuver**, puis sélectionnez le lien associé.
2. Sélectionnez une ou plusieurs lignes pour les demandes d’approbation à déléguer à un approbateur remplaçant, puis sélectionnez l’action **Déléguer**.

Une notification pour approuver la demande est envoyée à l’approbateur remplaçant.

## Gérer des demandes d’approbations échues

La tâche suivante est effectuée par un utilisateur d’approbation doté de droits d’approbation.

À intervalles réguliers, vous devrez rappeler aux utilisateurs du flux de travail approbation les demandes d’approbation échues ; vous utiliserez la fonction **Envoyer des notifications d’approbations échues** pour ce faire.

La fonctionnalité **Envoyer des notifications d’approbations échues** passe en revue toutes les demandes d’approbation en cours et actuellement échues. Chaque approbateur ayant au moins une écriture approbation échue reçoit une notification avec la liste de toutes leurs demandes d’approbations échues. La notification est également envoyée à leur approbateur et à tous les demandeurs des approbations échues. Cette dernière étape est utile si l’écriture d’approbation échue doit être déléguée à un remplaçant.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demandes approbations échues**, puis sélectionnez le lien associé.
2. Sur la page **Demandes approbations échues**, sélectionnez l’action **Envoyer les notifications d’approbation échues**.

## Voir aussi

[Utilisation des flux de travail approbation](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  
[Configuration des utilisateurs des approbations](across-how-to-set-up-approval-users.md)  
[Ventes](sales-manage-sales.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
