---
title: Valider des documents et des feuilles intersociétés
description: Cette rubrique explique comment vous pouvez utiliser les documents ou les feuilles intersociétés pour valider les transactions effectuées avec vos partenaires intersociétés.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
ms.service: dynamics-365-business-central
---
# Utiliser les documents et les feuilles intersociétés

Utilisez les documents ou les feuilles intersociétés pour valider les transactions effectuées avec vos partenaires intersociétés. Vous pouvez publier des transactions sur des comptes généraux et, si vous avez configuré des comptes bancaires intersociétés, vous pouvez également publier des transactions de banque à banque. Pour en savoir plus sur la configuration des comptes bancaires intersociétés, accédez à [Spécifier les comptes bancaires à utiliser pour les partenaires intersociétés](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Lorsque vous validez un document ou une ligne feuille intersociétés dans votre société, le programme crée le document ou la ligne feuille correspondant dans votre boîte d’envoi intersociétés. Vous transférez la ligne de votre boîte d’envoi à votre partenaire. Celui-ci peut ensuite valider la transaction correspondante dans sa société sans avoir à réentrer les données.

Pour les documents achat et vente, le code partenaire intersociétés du client ou du fournisseur concerné garantit que toutes les commandes et factures générées en relation avec les transactions entre les partenaires produisent des documents correspondants dans les sociétés partenaires. Les comptes de la société s’équilibrent correctement.

Il en est de même pour les lignes feuille comptabilité intersociétés. Vous n’avez pas besoin de spécifier de comptes, il vous suffit de choisir l’entreprise partenaire. Les lignes feuille comptabilité inter-sociétés correspondantes sont ensuite créées dans la société partenaire.

## Renseigner et envoyer une commande vente intersociétés

Vous pouvez envoyer les commandes vente et achat, ainsi que les retours avant qu’ils soient validés. En revanche, l’envoi des factures et avoirs est impossible tant qu’ils ne sont pas validés.

La procédure suivante explique comment renseigner et envoyer une commande vente intersociété. Les mêmes étapes s’appliquent aux commandes fournisseur intersociétés et aux retours, ainsi qu’aux factures et avoirs intersociétés validés.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Sélectionnez **Nouveau** pour créer une commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vérifiez que le client est un partenaire intersociétés.
5. Pour envoyer la commande vente avant de la valider, choisissez l’action **Envoi commande vente IC**.

> [!NOTE]
> Si vous effectuez l’étape 5, la commande vente est déplacée vers votre boîte d’envoi intersociétés, d’où vous pouvez l’envoyer ultérieurement. Pour en savoir plus sur la boîte de réception et la boîte d’envoi intersociétés, accédez à [Gérer la boîte de réception et la boîte d’envoi intersociétés](intercompany-how-manage-intercompany-inbox.md).

## Renseigner et valider une feuille intersociétés

Lorsque vous validez une ligne feuille comptabilité intersociétés dans votre société, le programme crée la ligne feuille correspondante dans votre boîte d’envoi intersociétés : vous pouvez la transmettre au partenaire concerné. Avec la 1re vague de lancement 2022, vous pouvez également configurer la société afin que soient créées automatiquement les transactions intersociétés reçues des partenaires intersociétés, validées via les feuilles comptabilité intersociétés. Celui-ci peut ensuite valider la transaction correspondante dans sa société sans avoir à réentrer les données.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuilles intracom.**, puis sélectionnez le lien associé.  
2. Ouvrez la feuille. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).
3. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Dans le champ **N° cpte gén partenaire IC**, saisissez le numéro du compte général intersociétés sur lequel le montant sera validé dans la société de votre partenaire.

    > [!NOTE]
    > Ce champ doit être renseigné avec une ligne dont l’un des champs **N° compte** ou **N° compte contrepartie** contient un compte bancaire ou un compte général.  
5. Sélectionnez l’action **Valider**.

Les écritures sont validées dans votre société et une feuille avec les écritures correspondantes est créée dans votre boîte d’envoi intersociétés ; vous pouvez l’envoyer à votre partenaire.

## Voir aussi

[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]