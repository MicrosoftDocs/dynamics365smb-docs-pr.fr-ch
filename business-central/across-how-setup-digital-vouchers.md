---
title: Configuration des pièces justificatives numériques
description: Cet article explique comment configurer et utiliser des bons numériques obligatoires dans Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# Configuration des pièces justificatives numériques

Les administrateurs peuvent utiliser la fonctionnalité de bon numérique pour exiger que les documents soient joints à des transactions spécifiques lors de leur publication. Par conséquent, cette fonctionnalité permet une approche basée sur la source et fournit une meilleure piste d’audit. Différents types de contrôle peuvent être configurés à cet effet, en fonction des documents ou des types de journaux.

Le terme *pièce justificative numérique* fait référence à une forme numérique ou électronique d’une pièce justificative traditionnelle en comptabilité. Un bon est un document utilisé pour soutenir et autoriser les transactions financières. En comptabilité, une pièce justificative sert généralement de preuve d’une dépense ou d’une réception de fonds. Le bon peut inclure des détails tels que la date de la transaction, une description, le montant et toutes les signatures d’autorisation.

> [!IMPORTANT]
> Dans certains pays et régions, il se peut que vous ne puissiez pas configurer certaines options, car des configurations spécifiques peuvent être imposées par des exigences légales. Si vous rencontrez ces restrictions, recherchez une explication détaillée sur la page de documentation de votre pays ou région.

## Activer les pièces justificatives numériques

Suivez ces étapes pour activer la fonctionnalité de bon numérique.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les pièces justificatives numériques**, puis sélectionnez le lien associé.
2. Cochez la case **Activé**.

## Configuration des pièces justificatives numériques

Vous pouvez utiliser différentes configurations pour les documents et journaux suivants.

| Type écriture | Désignation |
|------------|-------------|
| Document vente | Spécifie les écritures complétées à partir des documents ventes. |
| Document achat | Spécifie les écritures complétées à partir des documents achats. |
| Feuille comptabilité | Spécifie les validations effectuées à partir du journal général pour tous les types de comptes, à l’exception de ceux liés au client et au fournisseur. Si vous sélectionnez l’un de ces types de comptes, vous modifiez le contrôle du processus de comptabilisation. Si vous sélectionnez **Client** comme type de compte, le système vérifie votre configuration liée à la feuille ventes. Si vous sélectionnez **Fournisseur** comme type de compte, le système vérifie votre configuration liée à la feuille achats. |
| Feuille vente | Spécifie les écritures complétées à partir de la feuille ventes et de la feuille comptabilité où **Client** est sélectionné comme type de compte. |
| Feuille achat | Spécifie les écritures complétées à partir de la feuille ventes et de la feuille achats où **Fournisseur** est sélectionné comme type de compte. |

Suivez ces étapes pour définir la manière dont votre organisation utilise les bons numériques obligatoires.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer l’écriture des pièces justificatives numériques**, puis sélectionnez le lien associé. Alternativement, sur le **Configuration du bon numérique** page, sélectionnez **Configuration de l’écriture**.
2. Dans le **Type d’écriture** colonne, sélectionnez une option.
3. Dans le **Type de contrôle** colonne, sélectionnez une option de mise en application. Si vous sélectionnez **Aucun**, vous pouvez publier le type d’écriture sélectionné sans bon numérique. Si vous sélectionnez **Pièce jointe**, l’écriture doit inclure une pièce jointe. Si vous sélectionnez **Pièce jointe ou note**, vous pouvez inclure une pièce jointe ou une note pour l’écriture. 
4. Cochez la case **Générer automatiquement** pour générer automatiquement le bon numérique. Par exemple, si vous ne souhaitez pas ajouter manuellement une facture de vente à votre transaction, cochez cette case. Ensuite, il vous suffit de publier le document. Le système crée automatiquement le document, en fonction de la présentation de votre rapport, et le joint à la transaction.
5. Sélectionnez le **Ignorer si ajouté manuellement** case à cocher si vous ne souhaitez pas ajouter de bon numérique généré automatiquement si l’utilisateur a déjà ajouté une pièce jointe manuelle.

### Utiliser les codes sources pour la configuration

Pour utiliser l’application pour les feuilles, mais pas pour tous les types de transactions, connectez le code source spécifique pour identifier le type d’écriture : feuille comptabilité, feuille ventes ou feuille achats.

Pour configurer des codes sources spécifiques pour les bons numériques, procédez comme suit.

1. Sur le **Configuration de l’écriture du bon numérique** page, sélectionnez **Codes sources**.
2. Sur le **Codes sources d’écriture du bon** , sélectionnez les codes sources que vous souhaitez configurer.
3. Fermez la page.

## Utiliser la fonctionnalité

Ouvrez un document d’achat ou de vente et saisissez les informations dans les champs obligatoires. Avant de publier le document, vous devez suivre ces étapes pour joindre un bon numérique.

1. Dans le récapitulatif **Fichiers de documents entrants**, sélectionnez **Pièce jointe**.
2. Faites glisser un fichier directement sur le **Insérer un fichier** ou accédez au fichier à partir de cette page.

Le document est joint au Récapitulatif **Fichiers du document entrant**. Pour chaque ligne, vous pouvez trouver le nom et le type du document.

Si vous joignez accidentellement le mauvais bon, suivez ces étapes pour le supprimer avant de publier le document.

1. Dans le Récapitulatif **Fichiers de documents entrants** dans la ligne du document, sélectionnez **Document entrant**.
2. Sur le **Document entrant**, sélectionnez **Supprimer**.

> [!NOTE]
> Si la pièce jointe d’un justificatif numérique est configurée comme obligatoire et que vous essayez de valider des documents ou des feuilles sans joindre un justificatif, le système vous empêche de valider. Vous recevez le message d’erreur suivant : "Impossible de valider sans joindre le bon numérique. »

### Rechercher les bons joints dans les transactions

Vous pouvez trouver le justificatif ci-joint à partir du document publié ou de la page **Écritures comptables** en consultant le Récapitulatif **Fichiers de documents entrants**.

Vous ne pouvez pas supprimer un document joint une fois la publication terminée. Cependant, vous pouvez ajouter d’autres pièces jointes une fois la publication terminée.

## Voir aussi

[Gestion financière](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
