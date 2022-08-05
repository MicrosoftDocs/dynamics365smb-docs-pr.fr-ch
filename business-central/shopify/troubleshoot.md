---
title: Dépannage de la synchronisation entre Shopify et Business Central
description: Découvrez ce qu’il faut faire si une erreur se produit lors de la synchronisation des données entre Shopify et Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bebdf73fd1b01a3c750a3d91496a8f5bb87f8db4
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129656"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Dépannage de la synchronisation entre Shopify et Business Central

Vous pouvez vous trouver face à des situations où vous devez résoudre des problèmes lors de la synchronisation de données entre Shopify et [!INCLUDE[prod_short](../includes/prod_short.md)]. Cette page définit les étapes permettant de dépanner certains scénarios courants.

## <a name="logs"></a>Journaux

Si une tâche de synchronisation échoue, vous pouvez activer la journalisation en activant le bouton à bascule **Activation du journal** dans la page **Fiche magasin Shopify**. Déclenchez manuellement la tâche de synchronisation et consultez les journaux.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Écritures journal Shopify**, puis choisissez le lien associé.
2. Sélectionnez l’écriture journal associée et ouvrez la fenêtre **Écriture journal Shopify**.
3. Examinez la demande, le code statut et la description, et la réponse.

N’oubliez pas de désactiver la journalisation ultérieurement pour éviter un impact négatif sur les performances et une augmentation de la taille de la base de données.

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

## <a name="request-the-access-token"></a>Demander le jeton d’accès

Si [!INCLUDE[prod_short](../includes/prod_short.md)] ne parvient pas à se connecter à votre compte Shopify, tentez de réinitialiser le jeton d’accès auprès de Shopify. Cette demande peut être nécessaire en cas de rotation des clés de sécurité ou de modification des autorisations requises (étendues).

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez obtenir le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify.

Le bouton à bascule **A une clé d’accès** sera activé.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Vérifier et activer les autorisations pour effectuer des requêtes HTTP lors de l’exécution dans un environnement hors production

Pour fonctionner correctement, l’extension de connecteur Shopify nécessite une autorisation pour effectuer des requêtes HTTP. Lors des tests en sandbox, les requêtes HTTP sont interdites pour toutes les extensions.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des extensions**, puis sélectionnez le lien associé.
2. Sélectionnez l’extension *Connecteur Shopify*.
3. Choisissez l’action **Configurer** pour ouvrir la page **Paramètres de l’extension**.
4. Assurez-vous que le bouton à bascule **Autoriser les requêtes HTTPClient** est activé.

## <a name="rotate-the-shopify-access-key"></a>Faites tourner la clé d’accès Shopify

Les procédures suivantes décrivent comment faire tourner le jeton d’accès utilisé par le connecteur Shopify pour accéder à votre magasin en ligne Shopify.

### <a name="in-shopify"></a>Dans Shopify

1. Depuis votre **Administration Shopify**, accédez à [Applications](https://www.shopify.com/admin/apps).
2. Dans la ligne avec l’application **Dynamics 365 Business Central**, sélectionnez **Effacer**.
3. Dans le message qui s’affiche, sélectionnez **Supprimer**.

### <a name="in-prod_short"></a>Dans [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez faire tourner le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify, passez en revue la confidentialité et les autorisations, puis cliquez sur le bouton **Installer l’application**.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  