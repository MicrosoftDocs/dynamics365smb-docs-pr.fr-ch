---
title: Synchroniser les transactions et les règlements
description: Configurer et exécuter l’importation des transactions et des paiements à partir de Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# <a name="transactions-and-payouts"></a><a name="transactions-and-payouts"></a><a name="transactions-and-payouts"></a>Transactions et règlements

Lorsqu’un client a réglé sa commande dans la boutique en ligne, les informations relatives aux paiements sont enregistrées en tant que **Transaction**. Il peut y avoir plusieurs transactions liées à la commande, par exemple lorsqu’un client utilise une carte cadeau pour payer une partie du coût et utilise ensuite une carte de crédit ou PayPal pour le montant restant.

Si vous utilisez le paiement Shopify comme fournisseur de paiement, en plus des informations sur l’argent reçu du client par le fournisseur de paiement, vous pouvez également visualiser les règlements de Shopify sur votre compte bancaire.

## <a name="transactions"></a><a name="transactions"></a><a name="transactions"></a>Transactions

Les transactions réalisées sur Shopify sont synchronisées avec les commandes et s’affichent dans la page **Commandes Shopify**.

Pour examiner toutes les transactions, sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Transactions**, puis choisissez le lien associé.

Si vous avez configuré le mappage des modes de règlement, un code de mode de règlement est attribué au document de vente créé. En savoir plus dans la section [Mappage du mode de paiement](#payment-method-mapping).

## <a name="payouts"></a><a name="payouts"></a><a name="payouts"></a>Règlements

Si votre magasin utilise Shopify Payments, vous recevez les paiements via **Règlements Shopify** lorsqu’un client paie en utilisant le service Shopify Payments et les règlements accélérés.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les règlements pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les règlements**.

Pour examiner tous les règlements, sélectionnez l’icône en forme ![d’ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Règlements**, puis choisissez le lien associé.

Les **règlements** n’ont qu’une valeur informative et n’ont pas d’impact sur la comptabilité ou le Grand Livre bancaire, bien qu’ils puissent être utiles lorsque vous traitez votre relevé de compte bancaire.

## <a name="payment-method-mapping"></a><a name="payment-method-mapping"></a><a name="payment-method-mapping"></a>Mappage du mode de paiement

Pour remplir le **Code mode de règlement** pour les documents vente importés de Shopify automatiquement, vous devez configurer **Mappage du mode de paiement**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez définir le mappage pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Mappage du mode de paiement**.
4. Dans les champs **Passerelle** et **Société de carte de crédit**, saisissez le nom du mode de paiement Shopify. L’enregistrement est créé automatiquement lorsque vous importez des commandes Shopify.
5. Saisissez le **Code mode de règlement** avec le mode de règlement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Définissez la **Priorité** pour les cas où le client utilise plusieurs moyens de paiement. Le mode de paiement avec la priorité la plus élevée est sélectionné dans le document vente. Si les deux modes de paiement ont la même priorité, le mode de paiement avec le montant le plus élevé est utilisé.

> [!NOTE]  
> Si le mode de règlement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)] a les champs **Type compte contrepartie** et **N° compte contrepartie** renseignés, alors, lors de la validation, le système de facturation créera une écriture contrepartie du type *Règlement* et l’appliquera au type *Facture* dans l’écriture comptable client.

## <a name="use-cases"></a><a name="use-cases"></a><a name="use-cases"></a>Cas d’utilisation
  
Parties :

* Acheteur : personne qui achète des biens dans une boutique en ligne Shopify.
* Commerçant : votre société.
* Fournisseur de service de paiement : entreprise qui facilite le traitement des paiements pour vous. Peut être Shopify Payments ou un tiers.

### <a name="how-money-flows"></a><a name="how-money-flows"></a><a name="how-money-flows"></a>Comment l’argent circule

L’acheteur achète des marchandises dans la boutique en ligne. La dernière étape consiste à traiter le paiement.

>[!NOTE]
> Cet exemple ne couvre pas les cas où le paiement est effectué en dehors de la caisse Shopify, ce qui est valable pour les scénarios B2B.
  
L’acheteur paie par carte de crédit, PayPal ou un mode de paiement local comme MobilePay au Danemark. Le fournisseur de service de paiement prend le montant total à l’acheteur. À ce moment, l’argent des acheteurs est transféré au fournisseur de service de paiement.

Selon le fournisseur de service de paiement, le commerçant peut voir cet argent sur son compte auprès du fournisseur de service de paiement - à la fois les montants reçus et les commissions déduites. Les fournisseurs de service de paiement prélèvent souvent une commission sur chaque transaction et, dans certains cas, ils peuvent également avoir des frais fixes.
  
Selon le fournisseur de service de paiement, le commerçant déclenche manuellement un transfert d’argent sur son compte bancaire (paiement) ou cela se produit automatiquement dans un délai défini - une fois par jour, une fois par mois, etc.
  
Selon la banque, le commerçant peut voir cette transaction entrante sur son compte bancaire via la banque en ligne ou sur le relevé bancaire.

Plusieurs options sur la façon de gérer les transactions de paiement sont disponibles dans [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a><a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a><a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Option 1 : rapprocher les virements entrants vers le compte bancaire avec les factures originales
  
Le commerçant importe la commande client dans [!INCLUDE[prod_short](../includes/prod_short.md)] et valide l’expédition et la facture.

Résultat : le système crée une **Écriture comptable client** de type *Facture* avec le montant total, le champ **En cours** est défini sur Oui. Le **Montant restant** est égal au montant facturé.

Le commerçant importe un relevé bancaire via la feuille rapprochement bancaire.

Problèmes :

1. Cela peut être difficile s’il y a plusieurs factures (et avoirs), mais un seul paiement du fournisseur de service de paiement avec une somme forfaitaire.
2. Le montant ne correspond généralement pas en raison de la commission. Vous pouvez utiliser la tolérance de paiement ou/et les escomptes de paiement pour gérer les frais.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a><a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a><a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Option 2 : rapprocher les virements entrants vers le compte bancaire par rapport au compte d’attente représentant l’argent chez le fournisseur de service de paiement
  
Le commerçant importe la commande client dans [!INCLUDE[prod_short](../includes/prod_short.md)] et valide l’expédition et la facture.
  
Résultat : le système crée une écriture comptable client de type **Facture** avec le montant total, le champ **En cours** est défini sur Oui. Le **Montant restant** est égal au montant facturé.

Cependant, étant donné que la commande client a un code de mode de paiement où les champs **Type compte contrepartie** et **N ° compte contrepartie** sont renseignés, le système crée automatiquement une autre écriture client de type **Paiement** et l’applique à l’écriture client créée précédemment.

>[!NOTE]
> Le système renseigne le champ Code du mode de paiement en fonction du mappage du mode de paiement. En savoir plus dans la section [Mappage du mode de paiement](#payment-method-mapping).
  
Vous pouvez définir des comptes contrepartie pour les modes de paiement de deux manières :

* **Type compte contrepartie** défini sur *Banque*, et **N° compte contrepartie** renseigné dans le compte bancaire spécial qui représente votre compte chez le fournisseur de service de paiement.
* **Type compte contrepartie** défini sur *Compte général** et **N° compte contrepartie** renseigné dans le compte général qui représente votre compte chez le fournisseur de service de paiement.

Il est logique d’utiliser un compte bancaire si le fournisseur de service de paiement exporte une sorte de relevé de compte, que vous pouvez importer dans la feuille rapprochement bancaire.

Le commerçant importe un relevé bancaire via la feuille rapprochement bancaire. Le paiement entrant peut être traité :

* comme un virement d’une autre banque. Si le transfert prend quelques jours ou implique un échange de devises, vous pouvez utiliser un compte général provisoire.
* comme différence sur le compte général qui représente votre compte chez le fournisseur de service de paiement.
  
Le solde restant sur le compte général ou bancaire qui représente votre compte chez le fournisseur de service de paiement peut être annulé en tant que « Frais/Commissions »

Problèmes :

1. Vous pouvez créer plusieurs comptes généraux ou bancaires si vous traitez avec plusieurs fournisseurs de service de paiement. Cependant, les commandes clients dans [!INCLUDE[prod_short](../includes/prod_short.md)] ne prennent en charge qu’un seul code de mode de paiement, ce qui complique la gestion des cas où un acheteur utilise plusieurs modes de paiement pour une commande.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
