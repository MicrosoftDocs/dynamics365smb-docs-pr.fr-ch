---
title: Dépannage de la synchronisation entre Shopify et Business Central
description: Découvrez ce qu’il faut faire si une erreur se produit lors de la synchronisation des données entre Shopify et Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ff2e4aca52f479e461dab0d9d0f0ce4958d19353
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808892"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Dépannage de la synchronisation entre Shopify et Business Central

Vous pouvez vous trouver face à des situations où vous devez résoudre des problèmes. Cette page définit les étapes permettant de dépanner certains scénarios courants.

## <a name="logs"></a>Journaux

Si une tâche de synchronisation échoue, vous pouvez activer la journalisation en activant **Activation du journal** dans la page **Fiche magasin Shopify**. Déclenchez manuellement la tâche de synchronisation et consultez les journaux.

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Écritures journal Shopify**, puis choisissez le lien associé.
2. Sélectionnez l’écriture journal associée et ouvrez la fenêtre **Écriture journal Shopify**.
3. Examinez la demande, le code statut et la description, et la réponse.

N’oubliez pas de désactiver la journalisation pour éviter un impact négatif sur les performances et une augmentation de la taille de la base de données.

Dans la fenêtre **Écritures journal Shopify**, vous pouvez déclencher la suppression de toutes les écritures journal ou des écritures antérieures à 7 jours.

## <a name="data-capture"></a>Capture de données

Indépendamment des paramètres **Journal activé**, certaines réponses de Shopify sont toujours journalisées et vous pouvez les inspecter ou les télécharger en utilisant la fenêtre **Liste de capture de données**.

Sélectionnez l’action **Données Shopify récupérées** dans l’une des pages suivantes :

- **Commande Shopify**
- **Exécution des commandes Shopify**
- **Frais de livraison de la commande Shopify**
- **Transactions commande Shopify**
- **Règlements Shopify**
- **Transactions de paiement Shopify**
- **Transactions Shopify**

## <a name="reset-sync"></a>Réinitialiser la synchronisation

Pour des performances optimales, le connecteur importe uniquement les clients, les produits et les commandes créés ou modifiés depuis la dernière synchronisation. Dans la page **Fiche magasin Shopify**, ces fonctions sont disponibles pour modifier la date/l’heure de la dernière synchronisation ou la réinitialiser complètement. Cette fonction garantit que, lors de l’exécution de la synchronisation, toutes les données sont synchronisées et pas uniquement les modifications apportées depuis la dernière synchronisation.

Cette fonction ne s’applique qu’aux synchronisations à partir de Shopify vers [!INCLUDE[prod_short](../includes/prod_short.md)], et peut être utile si vous voulez restaurer des données supprimées, comme les produits, les clients ou les commandes supprimées.

## <a name="update-the-access-token"></a>Mettre à jour le jeton d’accès

Si [!INCLUDE[prod_short](../includes/prod_short.md)] ne parvient pas à se connecter à votre compte Shopify, tentez de réinitialiser le jeton d’accès.

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez obtenir le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
