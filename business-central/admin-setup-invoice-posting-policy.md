---
title: Définir une stratégie de validation des factures pour les utilisateurs
description: Utilisez les stratégies de validation des factures pour contrôler si un utilisateur peut valider des factures de vente et d’achat.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# <a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a>Définir une stratégie de validation des factures pour les utilisateurs

Les entreprises ont souvent des processus uniques pour valider les factures de vente et d’achat et les expéditions. Par exemple, les processus peuvent varier d’une personne validant tout sur un bon de commande à plusieurs employés. Vous pouvez empêcher les utilisateurs de valider des factures ou exiger que les factures soient validées avec les expéditions ou les réceptions.

## <a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a>Pour préciser une stratégie de validation

Sur la page **Configuration de l’utilisateur**, dans les champs **Stratégie validation facture vente** et **Stratégie validation facture achat**, choisissez l’une des options suivantes :

* **Autorisé** (Par défaut) : conservez le comportement actuel, où un utilisateur peut choisir l’option de validation à utiliser, comme **Expédier**, **Facturer**, et **Expédier et facturer**. 
* **Interdit** : empêchez l’utilisateur de valider des factures. Business Central affiche une boîte de dialogue de confirmation qui propose uniquement les options **Expédier** ou **Recevoir**.
* **Obligatoire** : autorisez l’utilisateur à valider des factures avec les reçus ou les expéditions. Business Central affiche une boîte de dialogue de confirmation qui propose uniquement les options **Expédier et envoyer** ou **Recevoir et facturer**.

## <a name="effect-on-documents"></a><a name="effect-on-documents"></a>Effet sur les documents

La table suivante décrit comment les stratégies de validation des factures affectent les documents.

|Document | Option 1 : Autoriser <br>Affiche une série d’options| Option 2 : Interdit <br>Boîte de dialogue de confirmation | Option 3 : obligatoire <br>Boîte de dialogue de confirmation|
|--|--|--|--|
|Commande vente |- Expédier <br>- Facturer <br>- Expédier et facturer |Souhaitez-vous valider l’expédition ? |Souhaitez-vous valider l’expédition et la facture ?|
|Ordre de retour vente |- Recevoir <br>- Facturer <br>- Réceptionner et facturer |Souhaitez-vous valider cette réception ? |Souhaitez-vous valider la réception et la facture ?|
|Prélvmt invent |- Expédier <br>- Expédier et facturer |Souhaitez-vous valider l’expédition ? |Souhaitez-vous valider l’expédition et la facture ?|
|Commande achat |- Recevoir <br>- Facturer <br>- Réceptionner et facturer |Souhaitez-vous valider cette réception ? |Souhaitez-vous valider la réception et la facture ?|
|Retour achat |- Expédier <br>- Facturer <br>- Expédier et facturer |Souhaitez-vous valider l’expédition ? |Souhaitez-vous valider l’expédition et la facture ?|
|Rangmt stk invent |- Recevoir <br>- Réceptionner et facturer |Souhaitez-vous valider cette réception ? |Souhaitez-vous valider la réception et la facture ?|
|Expédition entrepôt |- Expédier <br>- Expédier et facturer | Souhaitez-vous valider l’expédition ? |Souhaitez-vous valider l’expédition et la facture ?|

   > [!Note]
   > Le paramètre n’affecte pas la validation des lignes du journal général où vous pouvez sélectionner **Facture** dans le champ **Type de document**.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Facturer des ventes](sales-how-invoice-sales.md)  
[Enregistrer les achats avec les factures achat et les commandes](purchasing-how-record-purchases.md)  
[Acheter des articles pour une vente en créant des factures achat](purchasing-how-purchase-products-sale.md)
[Préparation aux activités commerciales](ui-get-ready-business.md)  
