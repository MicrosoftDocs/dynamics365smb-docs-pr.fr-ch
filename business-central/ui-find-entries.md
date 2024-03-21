---
title: Rechercher les écritures associées aux documents
description: 'Découvrez comment rechercher des documents, des contacts professionnels et des écritures d’éléments associés entre eux.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Rechercher les écritures associées aux documents

Découvrez comment rechercher des documents et des écritures qui sont associés entre eux en fonction d’informations communes, notamment :

- Numéro de document ou date de comptabilisation.
- Type de contact professionnel, numéro ou numéro de document externe.
- Numéro de série ou de lot d’article.

Cette fonctionnalité est très utile pour rechercher les écritures comptables qui résultent de certaines transactions. Lors de la recherche par numéro de document, vous pouvez imprimer la synthèse à partir du rapport **Écritures de documents**.

## Mise en route

La fonction de recherche d’écritures est facilement disponible à partir de presque toutes les pages en appuyant sur les touches <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd>. À partir des pages qui affichent spécifiquement les documents validés ou les écritures validées&mdash;pour les listes et les cartes&mdash;, vous pouvez également ouvrir la fonctionnalité en sélectionnant l’action **Rechercher des écritures**.

La page **Rechercher des écritures** inclut l’ensemble des écritures et documents associés en fonction du numéro de document et de la date de comptabilisation. La page est divisée en trois sections :

- La section supérieure affiche les champs et les actions que vous utilisez pour filtrer votre recherche.
- La section du milieu affiche les documents associés en fonction de la recherche.
- La section inférieure affiche des informations sur le document source qui a été trouvé lors de la recherche.

## Rechercher des écritures

Vous pouvez rechercher des écritures en fonction des informations relatives au document, au contact professionnel ou à la référence d’article. Dans la section supérieure, sélectionnez l’une des options suivantes en fonction du type d’informations dont vous disposez :

|Action|Désignation|
|------|-----------|
| **Rechercher des documents** | Affichez les écritures en fonction d’un numéro de document ou d’une date comptabilisation spécifique. |
| **Rechercher des contacts professionnels** | Affichez les écritures en fonction d’un type de contact, d’un numéro de contact et/ou d’un numéro de document externe spécifique. Cette dernière option vous permet de rechercher des documents d’un fournisseur ou d’un client en utilisant le numéro affecté par le contact. |
| **Rechercher des références dְ’articles** | Affichez les écritures en fonction d’un numéro de série ou de lot. Vous pouvez spécifier le n° de série ou lot, ou un filtre sur le n° de série ou lot à rechercher. Cette action est utile pour voir où un numéro de traçabilité spécifique a été utilisé, de quel vendeur il provient ou à quel client il a été vendu. |

Après avoir fait un choix, entrez les informations de recherche pertinentes dans les champs en haut de la page. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Lorsque vous avez terminé, sélectionnez **Trouver** pour commencer la recherche. Si vous modifiez l’un des filtres, vous devez cliquer sur **Rechercher** à nouveau.

> [!TIP]
> Pour des exemples d’utilisation de **Rechercher des écritures**, voir [Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md) et [Guide pas-à-pas : Suivi des numéros de série/lot](walkthrough-tracing-serial-lot-numbers.md).

## Voir aussi

[Traçabilité – Articles suivis](inventory-how-to-trace-item-tracked-items.md)  
[Recherche des documents validés sans enregistrements de document entrant](across-how-find-posted-documents-without-income-document-records.md)  
[Accessibilité et raccourcis clavier](ui-accessibility.md)  
[Utiliser Business Central](ui-work-product.md)  
[Ajouter une action de page à votre Tableau de bord](ui-bookmarks.md)  
[Rechercher des pages et des informations avec Tell Me](ui-search.md)  
[Rechercher des pages avec l’explorateur de rôles](ui-role-explorer.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
