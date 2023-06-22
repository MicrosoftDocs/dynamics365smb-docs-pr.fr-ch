---
title: Création et configuration d’un compte Shopify
description: Découvrez comment obtenir un compte Shopify afin de pouvoir démontrer le workflow d’intégration Shopify et Business Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Création et configuration d’un compte Shopify

Si vous envisagez d’utiliser Shopify comme solution d’e-commerce et avez besoin d’un compte Shopify pour valider le workflow intégré, vous disposez des options suivantes :

- Obtenir une version d’essai. C’est le point de départ typique pour les utilisateurs finaux.  
- Créer des magasins de développement. Cette approche est destinée aux partenaires qui font des démonstrations récurrentes, des formations et fournissent une assistance.

## Essai (utilisateur final)

Accédez au [site web Shopify](https://www.shopify.com) et utilisez votre compte de messagerie pour le compte administrateur afin de vous inscrire pour un essai gratuit. Pour plus d’informations sur la création et la personnalisation de votre boutique en ligne, voir le [Centre d’aide de Shopify](https://help.shopify.com/).

Dans **Administration de Shopify** de la boutique créée, appliquez les **Paramètres** suivants :

- Désactivez **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres [**Validation**](https://www.shopify.com/admin/settings/checkout) dans l’**administration Shopify**.
- Envisagez d’activer *Afficher le lien de connexion dans la vitrine et le paiement* dans la section **Paramètres du compte client** des paramètres de paiement.
- Envisagez de sélectionner l’option *Nom de l’entreprise – Facultatif* dans la section **Informations client** des paramètres de paiement.
- Activez l’option **Afficher les options de pourboire au moment du paiement** dans la section **Pourboire** des paramètres de paiement, si vous prévoyez de démontrer pourboire.
- Activez les paiements tests. Deux options s’offrent à vous. Commencez par accéder aux paramètres [**Paiements**](https://www.shopify.com/admin/settings/payments) :  
  1. *(pour les tests) Bogus Gateway*. Pour plus d’informations, voir [Activer Bogus Gateway pour les tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* en mode Test. Pour plus d’informations, voir [Test Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Sélectionnez un plan dans les paramètres [**Plan**](https://www.shopify.com/admin/settings/plan) pour pouvoir tester le processus de paiement.

> [!Important]  
> Pour éviter les paiements, n’oubliez pas d’annuler votre essai Shopify.

## Magasin de développement

Commencez par rejoindre le [programme Fournisseur Shopify](https://help.shopify.com/partners/about). Ensuite, utilisez le **tableau de bord des partenaires** pour créer la boutique de développement. Pour plus d’informations, consultez [Création des boutiques de développement](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Après la création de la boutique dans **Administration de Shopify** de la boutique créée, appliquez les **Paramètres** suivants :

- Désactivez **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres [**Validation**](https://www.shopify.com/admin/settings/checkout) dans l’**administration Shopify**.
- Envisagez d’activer *Afficher le lien de connexion dans la vitrine et le paiement* dans la section **Paramètres du compte client** des paramètres de paiement.
- Envisagez de sélectionner l’option *Nom de l’entreprise – Facultatif* dans la section **Informations client** des paramètres de paiement.
- Si vous prévoyez de démontrer pourboire, activez l’option **Afficher les options de pourboire au moment du paiement** dans la section **Pourboire** des paramètres de paiement.
- Activez les paiements tests. Deux options s’offrent à vous. Commencez par accéder aux paramètres [**Paiements**](https://www.shopify.com/admin/settings/payments) :  
  1. *(pour les tests) Bogus Gateway*. Pour plus d’informations, voir [Activer Bogus Gateway pour les tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* en mode Test. En savoir plus sur la [Test de Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Les magasins de développement sont généralement protégées par un mot de passe. Lorsque vous essayez d’ouvrir une page spécifique de votre boutique en ligne à partir de [!INCLUDE [prod_short](../includes/prod_short.md)], par exemple pour accéder à un produit ou à une commande spécifique, vous devrez saisir votre mot de passe. Pendant que vous testez, pour éviter d’avoir à entrer votre mot de passe, connectez-vous à votre administrateur Shopify  et ouvrez votre magasin à partir de là. Vous n’aurez pas besoin d’entrer le mot de passe du magasin jusqu’à ce que vous fermiez votre navigateur ou que votre session expire.  

## Voir aussi

[Mise en route avec le connecteur Shopify](get-started.md)  
[Procédure pas à pas : configurer et utiliser le connecteur Shopify](walkthrough-setting-up-and-using-shopify.md)
