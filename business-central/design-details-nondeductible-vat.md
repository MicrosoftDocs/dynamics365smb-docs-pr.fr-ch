---
title: "Détails de conception\_: TVA non déductible"
description: 'Cet article fournit des informations sur la taxe sur la valeur ajoutée (TVA) non déductible qui est la TVA payable par un acheteur, mais qui n’est pas déductible de la propre dette de TVA de l’acheteur.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# Détails de conception : TVA non déductible

La taxe sur la valeur ajoutée (TVA) non déductible est la TVA payable par un acheteur, mais qui n’est pas déductible de la propre dette de TVA de l’acheteur. Comme il peut être difficile de savoir où et comment un article est utilisé, vous devez contacter les autorités fiscales locales de votre pays ou région pour déterminer si un pourcentage spécifié de la TVA est déductible. Même si vous savez qu’un pourcentage spécifique de la TVA n’est pas déductible, il existe différents modèles de gestion des montants non déductibles lorsqu’ils sont liés aux **articles** et **immobilisations**.

## Conditions préalables à l’utilisation de la TVA non déductible

Pour utiliser et valider la TVA non déductible, procédez comme suit.

1. Sur la page **Paramètres TVA**, sélectionnez **Activer la TVA non déductible** pour activer la fonctionnalité.
2. Sur la page **Paramètres comptabilisation TVA**, sélectionnez les groupes comptabilisation TVA qui peuvent utiliser la TVA non déductible.

## Exemples

Pour les exemples suivants, la TVA non déductible est activée et la configuration suivante est terminée :

- Le champ **Groupe compta. produit TVA** est défini sur **NDVAT**.
- Sur la page **Paramètres comptabilisation TVA** :

    - **NDVAT** est défini comme groupe comptabilisation produit TVA et **DOMESTIC** est défini comme groupe comptabilisation marché TVA.
    - La valeur **Identifiant TVA** doit être unique.
    - Le champ **% VAT** est défini sur **25**.
    - Le champ **Autoriser la TVA non déductible** est défini sur **Autoriser**.
    - Le champ **% TVA non déductible** est défini sur **100**.
    - Le champ **Mode calcul TVA** est défini sur **TVA normale**.
    - Seuls le compte TVA vente et le compte TVA achat sont configurés.

Tous les exemples utilisent des articles et des immobilisations où le groupe comptabilisation produit TVA est **NDVAT**.

### Articles

Un nouvel article a **NDVAT** défini comme groupe comptabilisation produit TVA. Dans le document d’achat, **Quantité** = **1** et **Coût unitaire direct HT** = **1 000,00**.

Quelle que soit l’option utilisée, les résultats de l’**écriture TVA** sont les mêmes.

| Type de document | Type | Socle | Montant | Base TVA non déductible | Montant TVA non déductible |
|---|---|---|---|---|---|
| Reste à facturer | Achats |   0.00 |   0.00 | 1,000.00 | 250.00 |

Les détails sont affichés dans les **écritures de valeur**.

> [!NOTE]
> Vous pouvez activer le champ **Utiliser pour le coût de l’article** sur la page **Paramètres TVA**.

#### Utiliser pour le coût de l’article n’est pas activé

| Type écriture comptable article | Type écriture | Montant (réel) | Quantité écriture comptable article |
|---|---|---|---|
| Achats | Coût direct | 1,000.00 | 0 |

#### Utiliser pour le coût de l’article est activé

| Type écriture comptable article | Type écriture | Montant (réel) | Quantité écriture comptable article |
|---|---|---|---|
| Achats | Coût direct | 1,250.00 | 0 |

### Immobilisations

Une nouvelle immobilisation a le compte coût acquisition défini pour utiliser **NDVAT** comme groupe comptabilisation produit TVA. Dans le document d’achat, **Quantité** = **1** et **Coût unitaire direct HT** = **1 000,00**.

Quelle que soit l’option utilisée, les résultats de l’**écriture TVA** sont les mêmes.

| Type de document | Type | Socle | Montant | Base TVA non déductible | Montant TVA non déductible |
|---|---|---|---|---|---|
| Reste à facturer | Achats |   0.00 |   0.00 | 1,000.00 | 250.00 |

Les détails sont affichés dans les **écritures comptables immobilisation**.

> [!NOTE]
> Vous pouvez activer le champ **Utiliser pour le coût de l’immobilisation** sur la page **Paramètres TVA**.

#### Utiliser pour le coût de l’immobilisation n’est pas activé

| Type de document | Type compta. immo. | Montant | Montant TVA |
|---|---|---|---|
| Reste à facturer | Coût acquisition | 1,000.00 | 250.00 |

#### Utiliser pour le coût de l’immobilisation est activé

| Type de document | Type compta. immo. | Montant | Montant TVA |
|---|---|---|---|
| Reste à facturer | Coût acquisition | 1,000.00 | 250.00 |
| Reste à facturer | Coût acquisition | 250.00 |   0.00 |

## Voir aussi

[Configuration de la TVA non déductible](finance-setup-nondeductible-vat.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
