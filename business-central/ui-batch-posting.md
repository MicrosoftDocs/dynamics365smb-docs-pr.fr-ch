---
title: Comment valider plusieurs documents en même temps | Microsoft Docs
description: Au lieu de valider des documents individuels un par un, vous pouvez sélectionner plusieurs documents non validés dans une liste afin de les valider par lots, soit pour une validation immédiate, soit pour qu’elle soit planifiée, par exemple, à la fin de la journée.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912736"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Valider plusieurs documents en même temps

Au lieu de valider des documents individuels un par un, vous pouvez sélectionner plusieurs documents non validés dans une liste pour une validation immédiate ou une validation par lot, conformément à une planification, à la fin de la journée, par exemple. Cela peut être utile si seul un superviseur peut valider des documents créés par d’autres utilisateurs ou pour éviter des problèmes de performance du système liés à la validation pendant les heures de travail.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Pour valider plusieurs commandes achat immédiatement

La procédure suivante explique comment valider immédiatement plusieurs commandes achat. Les étapes sont similaires pour tous les documents achat et vente.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat** , puis sélectionnez le lien associé.
2. Sur la page **Commandes achat** , sélectionnez toutes les commandes à valider :
3. Dans le champ **N°** , choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage** .
4. Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.
5. Choisissez l’action **Validation** , puis sélectionnez l’action **Valider** .
6. Cliquez sur le bouton **Oui** dans le message de confirmation.

## <a name="to-batch-post-multiple-purchase-orders"></a>Pour valider plusieurs commandes achat par lots

La procédure suivante explique comment valider plusieurs commandes achat par lots. Les étapes sont similaires pour tous les documents d’achat et de vente où l’action **Valider par lots** est disponible.

> [!NOTE]
> La validation par lots de documents se produit en arrière-plan. [!INCLUDE [prodshort](includes/prodshort.md)] en ligne inclut les travaux par défaut pour la publication en arrière-plan et la validation par lots. Pour en savoir plus, consultez [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat** , puis sélectionnez le lien associé.  
2. Sur la page **Commandes achat** , sélectionnez toutes les commandes à valider :
3. Dans le champ **N°** , choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage** .
4. Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.
5. Choisissez l’action **Validation** , puis sélectionnez l’action **Valider par lot** .
6. Sur la page **TPL validation commandes achat** , renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Cliquez sur le bouton **OK** .
8. Pour afficher les problèmes potentiels survenus lors de l’enregistrement par lots de documents, ouvrez la page **Registre des messages d’erreur** .

Les commandes achat seront désormais ajoutées à une entrée de file d’attente de travaux dédiée, qui définit le moment où les documents sont validés. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

Si vous sélectionnez **PDF** dans le champ **Type sortie état** , les bons de commande validés avec succès seront disponibles dans la partie **boîte de réception état** de votre tableau de bord.

## <a name="see-also"></a>Voir aussi

[Validation des documents et des feuilles](ui-post-documents-journals.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Valider les documents validés](across-edit-posted-document.md)  
[Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Recherche de pages et d’informations avec la fonction Tell Me](ui-search.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
