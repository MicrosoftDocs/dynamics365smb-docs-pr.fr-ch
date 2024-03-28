---
title: Utiliser la TVA non déductible
description: Cet article explique comment utiliser et déclarer la TVA non déductible.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Utiliser la TVA non déductible

Cet article explique comment utiliser et déclarer la TVA non déductible.

## Créer une facture achat avec TVA non déductible

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Sélectionnez **Nouveau** pour créer une facture achat, puis saisissez les informations appropriées dans l’en-tête de la facture.
3. Dans la section **Lignes**, créez une nouvelle ligne de n’importe quel type, en fonction du groupe comptabilisation marché TVA et du groupe comptabilisation produit TVA où vous configurez la TVA non déductible.
4. Dans les champs **Quantité** et **Coût unitaire direct**, saisissez les valeurs appropriées.

    Si vous avez activé la case à cocher **Afficher TVA non déductible sur lignes** sur la page **Paramètres TVA**, les montants des champs **Base TVA non déductible** et **Montant TVA non déductible** sont calculés en fonction du champ **% TVA non déductible** sur la page **Paramètres comptabilisation TVA**.

5. Validez la facture.

## Créer une commande achat avec TVA non déductible

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Commandes achat**, puis sélectionnez le lien associé.
2. Sélectionnez **Nouveau** pour créer une commande achat, puis saisissez les informations appropriées dans l’en-tête du document.
3. Dans la section **Lignes**, créez une nouvelle ligne de n’importe quel type, en fonction du groupe comptabilisation marché TVA et du groupe comptabilisation produit TVA où vous configurez la TVA non déductible.
4. Dans les champs **Quantité** et **Coût unitaire direct**, saisissez les valeurs appropriées.

    Si vous avez activé la case à cocher **Afficher TVA non déductible sur lignes** sur la page **Paramètres TVA**, les montants des champs **Base TVA non déductible** et **Montant TVA non déductible** sont calculés en fonction du champ **% TVA non déductible** sur la page **Paramètres comptabilisation TVA**.

5. Validez la commande achat.

## Ajuster les montants de TVA arrondis avant la validation du document

Si les montants de TVA ne sont pas arrondis de la même manière dans votre environnement et dans le système comptable externe (le document de la facture d’origine), vous pouvez ajuster le montant de TVA avant de valider le document. Pour effectuer cet ajustement, suivez ces étapes avant de valider le document.

1. Dans le volet Actions, sélectionnez **Statistique**.
2. Si vous utilisez une facture achat, procédez comme suit :

    1. Dans le raccourci **Lignes**, sélectionnez le montant de TVA ou le montant de TVA non déductible.
    2. Définissez les valeurs nécessaires à partir du document d’origine, puis fermez la page **Statistiques facture achat**.

3.  Si vous utilisez une commande achat, procédez comme suit :

    1. Dans le raccourci **Facturation**, sélectionnez **Nbre de lignes fiscales** pour ouvrir la page **Lignes montants TVA**.
    2. Sélectionnez le montant de TVA ou le montant de TVA non déductible que vous souhaitez corriger.
    3. Saisissez les valeurs nécessaires à partir du document d’origine, fermez la page **Lignes montant TVA**, puis fermez la page **Statistiques commande achat**.

Pour utiliser les ajustements des montants de TVA, vous devez activer les ajustements. Sur la page **Paramètres comptabilité**, dans le champ **Différence TVA max. autorisée**, saisissez le montant de TVA maximum autorisé pour la correction. Ensuite, sur la page **Paramètres achats**, activez la case à cocher **Autoriser différence TVA**.

Vous pouvez ajuster les valeurs des champs **Montant TVA** et **Montant TVA non déductible**. La valeur du champ **Montant TVA déductible** est le résultat de ces deux valeurs. Le montant que vous saisissez dans le champ **Montant TVA non déductible** ne peut pas être supérieur au montant que vous saisissez dans le champ **Montant TVA**. Le champ **Différence TVA max. autorisée** sur la page **Paramètres comptabilité** fonctionne indépendamment pour les montants de TVA déductible et non déductible sur les pages de statistiques lorsque vous souhaitez ajuster les montants de TVA.

> [!IMPORTANT]
> Vous ne pouvez pas utiliser la TVA non déductible sur les factures acompte.

## Voir aussi

[Gestion financière](finance.md)

[Configurer des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md)  

[Paramétrer la TVA non déductible](finance-setup-nondeductible-vat.md)

[Détails de conception sur la TVA non déductible](design-details-nondeductible-vat.md)

[Déclaration de TVA aux autorités fiscales](finance-how-report-vat.md)

[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
