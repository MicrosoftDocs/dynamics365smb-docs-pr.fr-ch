---
title: Recherche d’écritures
description: Cet article décrit comment accéder aux documents et écritures liés
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a577e4723f7880b9e94babd645b7f35324e7d1ea
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2022
ms.locfileid: "8654802"
---
# <a name="finding-related-entries-for-posted-documents"></a>Recherche d’écritures associées pour les documents validés 

Dans cet article, vous apprenez à rechercher des documents et des écritures liés les uns aux autres en fonction d’informations communes, telles que :

- Un numéro de document ou une date comptabilisation
- Type de contact professionnel, numéro ou numéro de document externe
- Numéro de série ou numéro de lot de l’article

Cette fonctionnalité est très utile pour rechercher les écritures comptables qui résultent de certaines transactions. Lors d’une recherche par numéros de document, vous pouvez imprimer le résumé à partir de l’état Écritures document.

## <a name="get-started"></a>Démarrer

La fonctionnalité de recherche d’écritures est facilement disponible sur la plupart des pages qui affichent des documents validés ou des écritures de documents validés, pour les listes et les fiches. La première étape consiste donc à ouvrir l’une de ces pages. Ensuite, choisissez l’action **Rechercher des écritures** ou appuyez sur les touches Ctrl+Alt+G.

La page **Rechercher des écritures** comprend tous les documents et écritures liés basés sur le n° document et la date comptabilisation. La page est divisée en trois sections :

- La section supérieure affiche les champs et les actions que vous utilisez pour filtrer votre recherche.
- La section du milieu affiche les documents associés en fonction de la recherche.
- La section inférieure affiche des informations sur le document source qui a été trouvé lors de la recherche.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Rechercher des écritures

Vous pouvez rechercher des écritures en fonction des informations relatives au document, au contact professionnel ou à la référence d’article. Pour modifier la recherche, sélectionnez **Actions**, **Rechercher par**, puis l’une des actions suivantes :

|Action|Description|
|------|-----------|
|Rechercher par document|Affichez les écritures en fonction d’un numéro de document ou d’une date comptabilisation spécifique.|
|Contact professionnel |Affichez les écritures en fonction d’un type de contact spécifique, d’un numéro de contact, et/ou d’un numéro de document externe. Vous pouvez saisir des informations qui ont été affectées par un fournisseur ou un client. Utilisez les champs disponibles pour rechercher des documents du fournisseur en utilisant les numéros que le fournisseur a affecté aux documents.|
|Référence d’article|Afficher les écritures en fonction d’un n° de série ou d’un n° lot. Vous pouvez spécifier le n° de série ou lot, ou un filtre sur le n° de série ou lot à rechercher. Cette action est utile pour voir où un numéro de traçabilité spécifique a été utilisé, de quel vendeur il provient ou à quel client il a été vendu.|

Après avoir effectué une sélection, entrez les informations de recherche pertinentes dans les champs d’en haut. Utilisez les info-bulles sur les champs pour vous aider. Lorsque vous avez terminé, choisissez **Rechercher** pour lancer la recherche. Si vous modifiez l’un des filtres, vous devez cliquer sur **Rechercher** à nouveau.

> [!TIP]
> Pour consulter quelques exemples d’utilisation de **Recherche des écritures**, voir [Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md) <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Utiliser Business Central](ui-work-product.md)  
[Ajouter une action de page à votre Tableau de bord](ui-bookmarks.md)  
[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
