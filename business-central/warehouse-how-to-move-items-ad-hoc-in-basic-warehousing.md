---
title: Déplacer des articles ad hoc dans les configurations de stockage de base
description: Cette rubrique explique les mouvements ad hoc effectués lorsque vous devez déplacer des articles entre des emplacements internes sans une demande spécifique d’un document source.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 393, 7382
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 46b6cbd88cf23974e5fd11453c328c1669c8e19c
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534442"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Déplacer des articles ad hoc dans les configurations de stockage de base

Vous pouvez être amené à déplacer des articles d’un emplacement interne vers un autre (et non vers des emplacements de réception ou d’expédition) sans demande spécifique issue d’un document origine. Vous pouvez exécuter ces mouvements ad hoc, par exemple, pour réorganiser l’entrepôt, pour acheminer des articles vers une zone d’inspection, ou pour déplacer des articles supplémentaires vers et depuis une zone de production sans qu’il existe une relation système avec le document origine de l’ordre de fabrication.  

Dans les configurations d’entrepôt de base, où les magasins utilisent le champ de configuration **Emplacement obligatoire** et éventuellement les champs **Prélèvement requis** et **Rangement requis**, vous pouvez enregistrer des mouvements ad hoc sans documents origine en procédant comme suit :  

- À l’aide de la page **Mouvement interne**.  
- Avec la page **Feuille reclassement article**.  

> [!NOTE]  
>  Dans les configurations d’entrepôt avancées, où les magasins utilisent le champ de configuration **Prélèv. et rangement suggérés**, vous utilisez la page **Feuille mouvement** ou les pages **Prélèvement interne entrepôt** ou **Rangement interne entrepôt** pour déplacer des articles ad hoc entre différents emplacements.  

## <a name="to-move-items-as-an-internal-movement"></a>Pour déplacer des articles en tant que mouvement interne

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mouvement interne**, puis sélectionnez le lien associé.  
2.  Sur le raccourci **Général**, renseignez le champ **N°**. en le laissant tel quel ou en cliquant sur le bouton **AssistEdit** pour effectuer une sélection parmi la souche de numéros.  
3.  Dans le champ **Code magasin**, entrez le magasin où le mouvement a lieu.  

    Si le magasin est configuré comme votre magasin par défaut en tant que magasinier, le code magasin est inséré automatiquement.  
4.  Dans le champ **Vers code emplacement**, entrez le code de l’emplacement vers lequel vous souhaitez déplacer l’article. Pour la production, il s’agit du code emplacement des consommations ou du code emplacement atelier ouvert, par exemple, tel qu’il est défini sur la fiche magasin ou dans le centre de charge.  
5.  Dans le champ **Date d’échéance**, entrez la date à laquelle le mouvement doit être terminé.  
6.  Sur le raccourci **Lignes**, cliquez sur le champ **N° article** pour ouvrir la page **Liste contenus emplacement**, puis sélectionnez l’article à déplacer sur la base de sa disponibilité dans les emplacements. Vous pouvez également choisir l’action **Extraire contenu emplacement** pour renseigner les lignes mouvement internes sur la base des filtres. Pour plus d’informations, voir l’info-bulles pour l’action **Extraire contenu emplacement**.  

    Lorsque vous avez sélectionné l’article, le champ **Du code emplacement** est renseigné automatiquement en fonction du contenu d’emplacement sélectionné, mais vous pouvez le remplacer par un autre emplacement dans lequel l’article est disponible.  

    > [!NOTE]  
    >  Étant donné que le champ **N° article** et le champ **Du code emplacement** sont liés, leur valeur peut changer de manière interdépendante lorsque vous modifiez l’un ou l’autre de ces champs.  

    Le champ **Vers code emplacement** est renseigné avec la valeur que vous avez entrée dans l’en-tête, mais vous pouvez la remplacer sur la ligne par n’importe quel autre code emplacement qui n’est pas bloqué ou dédié à des cas particuliers. Pour plus d’informations sur la création d’emplacements dédiés, reportez\-vous à Dédié.  
7.  Lorsque vous avez défini les emplacements depuis/vers lesquels que vous souhaitez déplacer l’article, entrez la quantité à déplacer dans le champ **Quantité**.  

    > [!NOTE]  
    >  La quantité doit être disponible dans le champ Du code emplacement.  

8.  Lorsque vous êtes prêt à traiter le mouvement interne, choisissez l’action **Créer mouvement de stock**.  

    > [!NOTE]  
    >  Lorsque vous avez créé le mouvement de stock, les lignes mouvement interne sont supprimées.  

    Vous effectuez le reste du mouvement ad hoc sur la page **Mouvement de stock** de la même manière que pour un mouvement basé sur des documents origine. Pour plus d’informations, voir par exemple [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Pour déplacer des articles avec la feuille reclassement article

Au lieu d’utiliser des documents mouvement entrepôt, vous pouvez enregistrer le déplacement d’articles en reclassant leurs codes emplacement. Pour plus d’informations, voir [Inventaire, ajustement et reclassement du stock avec les journaux](inventory-how-count-adjust-reclassify.md).

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille reclassement article**, puis choisissez le lien associé.  
2.  Sur chaque ligne feuille, définissez les emplacements depuis et vers lesquels vous souhaitez déplacer des articles en renseignant les champs **Code emplacement** et **Nouveau code emplacement**.  

    1.  Pour déplacer tout le contenu d’un emplacement à un autre, choisissez l’action **Extraire contenu emplacement**.  
    2.  Renseignez les filtres pour rechercher l’emplacement dont vous souhaitez déplacer le contenu, puis sélectionnez le bouton **OK**. Les lignes feuille sont renseignées avec le contenu de l’emplacement.  
3.  Renseignez les autres champs de chaque ligne feuille.   
4.  Valider la feuille reclassement.  

    > [!NOTE]  
    >  Contrairement aux documents mouvement, un mouvement validé avec la feuille reclassement ne crée pas de demande entrepôt pour effectuer la tâche physique.  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/manage-internal-warehouse-processes/) associée

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
