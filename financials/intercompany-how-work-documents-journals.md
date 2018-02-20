---
title: "Valider des documents et des feuilles intersociétés | Microsoft Docs"
description: "Utiliser des documents intersociétés pour valider des transactions avec vos partenaires intersociétés."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 98e0d9012dfdd998431aaed8dade02f592af47c8
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-intercompany-documents-and-journals"></a>Utiliser les documents et les feuilles intersociétés
Les documents ou les feuilles intersociétés permettent de valider les transactions effectuées avec vos partenaires intersociétés. Lorsque vous validez un document ou une ligne feuille intersociétés dans votre société, le programme crée le document ou la ligne feuille correspondant dans votre boîte d'envoi intersociétés : vous pouvez le transmettre au partenaire concerné. Celui-ci peut ensuite valider la transaction correspondante dans sa société sans avoir à réentrer les données.

Pour les documents achat et vente, le code partenaire intersociétés du client ou du fournisseur concerné garantit que toutes les commandes et factures générées en relation avec les transactions avec ces sociétés produisent des documents correspondants dans la société partenaire. Il en résulte un équilibrage correct des comptes.

Dans le cas des lignes feuilles comptabilité intersociétés, vous ne devez pas spécifier les comptes pour un ensemble de documents comptables particulier, mais simplement fournir l'identification de la société concernée. Les lignes feuille comptabilité intersociétés correspondantes sont alors créées dans la société partenaire, ce qui entraîne un équilibrage des documents comptables des deux sociétés impliquées dans une transaction.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Pour renseigner et envoyer une commande vente intersociétés
Vous pouvez envoyer les commandes vente et achat, ainsi que les retours avant qu'ils soient validés. En revanche, l'envoi des factures et avoirs est impossible tant qu'ils ne sont pas validés.

La procédure suivante explique comment renseigner et envoyer une commande vente intersociété. Les mêmes étapes s'appliquent aux commandes fournisseur intersociétés et aux retours, ainsi qu'aux factures et avoirs intersociétés validés.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2. Sélectionnez **Nouveau** pour créer une commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vérifiez que le client est un partenaire intersociétés.
5. Pour envoyer la commande vente avant de la valider, choisissez l'action **Envoi commande vente IC**.

> [!NOTE]
> Si vous effectuez l'étape 4, la commande vente est déplacée vers votre boîte d'envoi intersociétés, d'où vous pouvez l'envoyer ultérieurement. Pour plus d'informations, voir [Gérer la boîte de réception et la boîte d'envoi intersociétés](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Pour renseigner et valider une feuille intersociétés
Lorsque vous validez une ligne feuille comptabilité intersociétés dans votre société, le programme crée la ligne feuille correspondante dans votre boîte d'envoi intersociétés : vous pouvez la transmettre au partenaire concerné. Celui-ci peut ensuite valider la transaction correspondante dans sa société sans avoir à réentrer les données.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles comptabilité IC**, puis sélectionnez le lien connexe.  
2. Ouvrez la feuille appropriée. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).
3. Renseignez les champs selon vos besoins.
4. Dans le champ **N° cpte gén partenaire IC**, saisissez le numéro du compte général intersociétés sur lequel le montant sera validé dans la société de votre partenaire.

    > [!NOTE]
    > Ce champ doit être renseigné avec une ligne dont l'un des champs **N° compte** ou  **N° compte contrepartie** contient un compte bancaire ou un compte général.  
5. Sélectionnez l'action **Valider**.

Les écritures associées sont validées dans votre société et une feuille avec les écritures correspondantes est créée dans votre boîte d'envoi intersociétés ; vous pouvez l'envoyer à votre partenaire. Pour plus d'informations, voir [Gérer la boîte de réception et la boîte d'envoi intersociétés](intercompany-how-manage-intercompany-inbox.md). 

## <a name="see-also"></a>Voir aussi
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

