---
title: Affecter un niveau de priorité à un fournisseur (contient une vidéo)
description: "Vous pouvez affecter des numéros à vos fournisseurs pour les classer par ordre de priorité et faciliter des propositions de paiement dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'supplier, payment priority'
ms.search.form: '26, 27'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="prioritize-vendors"></a>Octroyer une priorité aux fournisseurs

[!INCLUDE[prod_short](includes/prod_short.md)] peut proposer différents paiements aux fournisseurs, par exemple les paiements arrivant à échéance ou les paiements donnant lieu à un escompte. Pour plus d’informations, reportez vous à [Proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).

Tout d’abord, vous devez attribuer une priorité à vos fournisseurs en leur affectant des numéros.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Pour octroyer une priorité à des fournisseurs

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Sélectionnez le fournisseur approprié, puis sélectionnez **Modifier**.
3. Dans le champ **Priorité**, entrez un numéro.

[!INCLUDE[prod_short](includes/prod_short.md)] donne le degré de priorité le plus élevé au chiffre le plus bas, excepté 0. Ainsi, si vous utilisez 1, 2 et 3, le chiffre 1 a le degré de priorité le plus élevé.

Si vous ne souhaitez pas attribuer de priorité à un fournisseur, laissez le champ **Priorité** blanc. Par la suite, lorsque vous utilisez la fonction de proposition de paiements, ce fournisseur est répertorié après tous les fournisseurs possédant un numéro prioritaire. Vous pouvez saisir autant de niveaux de priorité que nécessaire.

## <a name="see-also"></a>Voir aussi

[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Définition des achats](purchasing-setup-purchasing.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
