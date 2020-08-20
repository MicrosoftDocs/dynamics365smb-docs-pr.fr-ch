---
title: Modifier les documents vente et achat validés | Microsoft Docs
description: Découvrez les différentes fonctions de validation pour valider les documents achat et comment mettre à jour les documents validés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 07/21/2020
ms.author: sgroespe
ms.openlocfilehash: 58cbec2b697a0fdabd5749000ea94145d07fc62f
ms.sourcegitcommit: bdb6d18d512aa76d8d4f477d73ccfb284b0047fc
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/21/2020
ms.locfileid: "3611524"
---
# <a name="edit-posted-documents"></a>Valider les documents validés

Parfois, vous devez mettre à jour un document validé, car les informations pertinentes pour le document ont été modifiées. Sur un document de vente validé, il peut s'agir du numéro de suivi du colis du transporteur, par exemple. Sur un document d'achat validé, il peut s'agir d'un texte de référence de paiement.

Vous effectuez la modification sur une version modifiable du document d'origine, indiquée par «  **- Mettre à jour** » dans le titre de la page. La page contient un sous-ensemble des champs sur le document d'origine, dont certains sont des champs non modifiables affichés uniquement à titre d'information.

La fonctionnalité est disponible pour les documents suivants dans tous les marchés pris en charge :

- Expédition vente enregistrée
- Facture achat enregistrée
- Expédition retour enregistrée
- Réception retour enregistrée

Les documents supplémentaires suivants peuvent être modifiés dans les pays ou régions spécifiés :

- ES : facture vente enregistrée, avoir vente enregistré, avoir achat validé
- APAC : avoir vente enregistré, avoir achat validé
- RU : avoir vente enregistré
- IT : expédition de transfert validée, expédition de service validée

## <a name="to-edit-a-posted-sales-shipment"></a>Pour modifier une expédition vente enregistrée

Ce qui suit explique comment modifier une expédition vente enregistrée Les étapes sont similaires pour les autres documents pris en charge.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Expéditions vente enregistrées**, puis sélectionnez le lien associé.
2. Sélectionnez le document que vous souhaitez modifier, puis sélectionnez l'action **Mettre à jour le document**. Sinon, ouvrez le document, puis choisissez l'action.
3. Sur la page **Expédition vente enregistrée - Mettre à jour**, modifiez le champ **N° de suivi du colis** par exemple.
4. Cliquez sur le bouton **OK**.

L'expédition vente enregistrée est mise à jour.

## <a name="see-also"></a>Voir aussi

[Fonctionnalités marché](ui-across-business-areas.md)  
[Achats](purchasing-manage-purchasing.md)  
[Validation des documents et des feuilles](ui-post-documents-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
