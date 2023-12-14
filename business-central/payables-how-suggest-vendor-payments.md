---
title: Proposer paiements fournisseur
description: Utilisez le traitement par lots Proposer paiements fournisseur pour créer des lignes de paiement pour vos fournisseurs en fonction des dates d’échéance et des escomptes sur paiement.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 12/04/2023
ms.custom: bap-template
---
# Proposer paiements fournisseur

Sur la page **Feuille paiement**, vous pouvez utiliser le traitement par lots **Proposer paiements fournisseur** pour proposer des lignes paiement. En fonction de vos paramètres, [!INCLUDE [prod_short](includes/prod_short.md)] suggère des lignes pour :

- Paiements bientôt dus.
- Paiements pour lesquels un escompte est disponible.

Pour bénéficier pleinement des suggestions de paiement, vous devez attribuer une priorité à vos fournisseurs. Pour en savoir plus sur la priorisation des fournisseurs, rendez-vous sur [Prioriser les fournisseurs](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Le traitement par lots exclut les écritures comptables fournisseur qui sont **En attente** ou qui sont déjà lettrées et ont une valeur dans le **ID applicable** champ.  

> [!IMPORTANT]  
> Si vous souhaitez profiter d’escomptes et que vous avez saisi un montant disponible, ce montant est d’abord utilisé pour :  
>
> * Les écritures fournisseur échues et prioritaires, par ordre de priorité.
> * Les écritures fournisseur échues et non prioritaires.  
> * Les écritures fournisseur ouvertes donnant lieu à un escompte. Les écritures sont classées dans l’ordre des numéros des fournisseurs.  

## Utilisez l’action Proposer paiements fournisseur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles paiement**, puis Sélectionner le lien associé.  
2. Ouvrez la feuille, puis sélectionnez l’action **Proposer paiements fournisseur**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Cliquez sur le bouton **OK**.  

## Insérer la date d’échéance comme date comptabilisation sur les lignes feuille paiement

Lorsque vous utilisez le traitement par lots **Proposer paiements fournisseur** pour créer des lignes de paiement pour vos fournisseurs, vous pouvez remplir deux champs spéciaux pour vérifier que les lignes générées utilisent la date d’échéance pour calculer la date comptabilisation. Ces champs sont **Calculer la date comptabilisation à partir de la date d’échéance doc. lettrage** et **Décalage date d’échéance doc. lettrage**.  

> [!IMPORTANT]  
> Vous ne pouvez pas utiliser le champ **Calculer la date comptabilisation à partir de la date d’échéance doc. lettrage** avec le champ **Rechercher les escomptes** ou le champ **Totaliser par fournisseur**. Si la date comptabilisation est basée sur la date d’échéance, des escomptes fournisseur risquent de ne pas être calculés correctement, parce que la date comptabilisation peut se trouver après la date d’escompte.  

De plus, si la date comptabilisation calculée se trouve dans le passé, la date de comptabilisation est déplacée à la date de travail, et un message d’avertissement s’affiche.  

Vous pouvez aussi créer manuellement des lignes de paiement à l’aide de la date d’échéance pour calculer la date comptabilisation. Une fois que vous avez appliqué les écritures comptables fournisseur, vous pouvez utiliser l’option **Calculer date comptabilisation** pour mettre à jour la date comptabilisation de la ligne feuille à la date d’échéance de la facture achat associée. Pour en savoir plus sur ce processus manuel, accédez à [Lettrer manuellement les transactions d’achat](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Si la facture achat est en retard, la date comptabilisation est définie sur la date de travail et la police de la ligne passe à rouge.  

## Voir aussi

- [Gestion des comptes fournisseur](payables-manage-payables.md)  
- [Effectuer des paiements](payables-make-payments.md)  
- [Utilisation des feuilles comptabilité](ui-work-general-journals.md)  
- [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
