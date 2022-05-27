---
title: Mise en route du connecteur pour Shopify
description: Premières étapes lors de la configuration de la connexion entre Business Central et Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768246"
---
# <a name="get-started-with-the-shopify-connector"></a>Mise en route du connecteur Shopify

[!INCLUDE [prod_short](../includes/prod_short.md)]vous donne la possibilité de connecter votre magasin (ou vos magasins) Shopify pour accroître la productivité de votre entreprise. Vous pouvez gérer et afficher les informations de votre entreprise et de votre boutique en ligne Shopify comme une seule unité en utilisant le connecteur Shopify. Pour utiliser Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)], vous devez suivre certaines étapes. Cette page sert de guide pour terminer l’intégration de votre magasin Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Conditions préalables pour Shopify

Vous devez disposer :

- D’un compte Shopify
- D’une boutique en ligne Shopify

Pour créer un compte Shopify ou vous inscrire à un essai gratuit de 14 jours, accédez à [Shopify](https://www.shopify.com/). Pour plus d’informations sur la création et la personnalisation de votre boutique en ligne, voir le[Centre d’aide de Shopify](https://help.shopify.com/).
  
- D’autres canaux de vente sont pris en charge, par exemple, le PDV Shopify.

### <a name="recommended-settings"></a>Paramètres recommandés

- Désactivez **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres [**Validation**](https://www.shopify.com/admin/settings/checkout) dans l’**administration Shopify**.

Pour en savoir plus sur les paramètres Shopify pour les scénarios de démonstration et d’essai, voir [Scénarios de test et de formation](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Conditions préalables pour Business Central

- Vérifiez que l’extension **Se connecter à Shopify pour [!INCLUDE[prod_short](../includes/prod_short.md)]** est installée.

L’extension est préinstallée pour toutes les nouvelles inscriptions et tous les essais. Si vous devez installer des extensions à partir de la place de marché, visitez [Installation et désinstallation des extensions](../ui-extensions-install-uninstall.md#install). Suivez les étapes ci-dessous si vous n’avez pas [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Connexion de Business Central à la boutique en ligne Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Code**, saisissez le code voulu.  
4. Dans le champ **URL Shopify**, tapez l’URL de votre boutique en ligne, qui doit être connectée.
5. Activez la bascule **Activé**, lisez et acceptez les conditions générales.
6. Si vous y êtes invité, connectez-vous à votre compte Shopify, passez en revue la confidentialité et les autorisations, puis cliquez sur le bouton **Installer l’application**.

Répétez les étapes 2 à 6 pour toutes les boutiques en ligne que vous voulez connecter.

### <a name="next-steps"></a>Étapes suivantes

Votre boutique en ligne est désormais connectée à [!INCLUDE[prod_short](../includes/prod_short.md)]. Dans les étapes suivantes, vous allez définir comment et quoi synchroniser.

- [Synchroniser les articles](synchronize-items.md)
- [Synchroniser les clients](synchronize-customers.md)
- [Synchroniser les commandes](synchronize-orders.md)

## <a name="see-also"></a>Voir aussi

[Scénarios de test et de formation](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

