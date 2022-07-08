---
title: Comment ranger des articles avec le rangement entrepôt | Microsoft Docs
description: Découvrez les différentes manières de ranger des articles dans Business Central avec les tâches de rangement d’entrepôt suivantes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 3e638e00fc648a720d09520fb62aa3ad25324673
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078299"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Ranger des articles avec le rangement entrepôt

Lorsque l’entrepôt est configuré pour appeler un traitement de rangement entrepôt et un traitement de réception entrepôt, vous pouvez utiliser la fonction documents rangement entrepôt pour contrôler le rangement des articles.  

Lorsque vous validez une réception entrepôt, les documents origine, tels que commandes achat, enlogement transfert ou commandes retour vente sont mis à jour, la quantité reçue dans les écritures article est validée et les lignes relatives aux articles reçus à la fonction de rangement de l’entrepôt sont transmises. En cas de rangement et de prélèvement internes, des lignes rangement peuvent également être créées dans le cadre du rangement interne.  

En fonction de la configuration de l’entrepôt, ces lignes sont mises à disposition de la feuille rangement ou utilisées pour créer immédiatement des instructions de rangement. Pour plus d’informations, voir [Planifier des rangements dans la feuille](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Outre les méthodes standard pour créer les rangements entrepôt qui sont décrits dans cette rubrique, vous pouvez créer le rangement à partir de la réception entrepôt validée associée. Cela est utile si vous avez supprimé des lignes rangement ou si vous utilisez le prélèvement et le rangement suggérés et avez décidé de ne pas utiliser la feuille rangement, car vous pouvez créer ou recréer des instructions de rangement à partir des lignes réception validées.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Rangement d’articles en l’absence de prélèvement et de rangement suggérés

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangements**, puis sélectionnez le lien associé.  
2.  Ouvrez le rangement entrepôt qui est prêt à être traité.  

    Vous pouvez optimiser le processus de rangement en triant les lignes en fonction de critères divers, tels que l’article, le numéro emplacement ou le délai.  
3.  Sur chaque ligne, dans le champ **Quantité à traiter**, entrez la quantité à ranger.  
4.  Une fois le rangement des articles terminé, choisissez l’action **Enregistrer rangement** pour enregistrer l’achèvement de l’activité et rendre les articles disponibles pour le prélèvement.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Rangement d’articles dans le cadre d’un prélèvement et d’un rangement suggérés

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangements**, puis sélectionnez le lien associé.
    Si des instructions de rangement ont été créées, un rangement entrepôt apparaît.  
2.  Ouvrez le rangement entrepôt que vous souhaitez utiliser.  
3.  Entrez votre code utilisateur sur le raccourci **Général** lorsque vous commencez à travailler sur un rangement particulier.  
4.  Effectuez les actions de prélèvement et de placement indiquées sur les lignes dans le champ **Type action**.  

    Notez que chaque ligne réception donne lieu à deux lignes au moins dans le rangement entrepôt :  

    -   la première ligne, correspondant au champ **Type action** **Prélèvement**, indique l’endroit où se trouvent les articles dans la zone de réception. Vous ne pouvez pas modifier le champ de la zone et de l’emplacement de cette ligne.  
    -   La ligne suivante, avec **Emplacement** dans le champ **Type d’action**, indique l’endroit où vous devez placer les articles dans le stockage en entrepôt. Si l’entrepôt a reçu un grand nombre d’articles sur une ligne réception, ils peuvent devoir être rangés dans plusieurs emplacements, pour qu’il y ait une ligne Emplacement pour chaque emplacement.  

        Si les lignes prélèvement et emplacement de chaque ligne réception ne se suivent pas directement et que vous souhaitez qu’elles se suivent, vous pouvez trier ces lignes en sélectionnant **Article** dans le champ **Méthode de tri** du raccourci **Général**.  

        Si l’organisation de l’entrepôt reflète le classement des emplacements, vous pouvez utiliser la méthode de tri **N° emplacement** pour préparer une opération de rangement en réduisant au minimum vos déplacements dans l’entrepôt.  

5.  Après avoir placé tous les articles dans des emplacements selon les instructions, choisissez l’action **Enregistrer rangement**.  

Dans des magasins qui sont configurés pour utiliser le prélèvement et rangement dirigé, les paramètres suivants sont des conditions préalables à la procédure ci-dessus :  

- Un modèle de rangement est configuré. Pour plus d’informations, voir [Configurer des modèles rangement](warehouse-how-to-set-up-put-away-templates.md).  
- Le poids, le cubage et les exigences particulières de stockage de l’article ou du point de stock sont définis. Pour plus d’informations, voir Poids brut.  
- La capacité, le type et le classement des emplacements. Pour plus d’informations, voir Priorité emplacement.  

La priorité emplacement est prise en compte lorsque plusieurs emplacements correspondent aux critères du modèle rangement. Si les critères du modèle rangement et la priorité emplacement coïncident pour plusieurs emplacements, l’emplacement dont le numéro est le plus élevé est alors sélectionné.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Pour créer un rangement à partir d’une réception validée

 Si votre magasin utilise à la fois le traitement par rangement et par réception et que vous avez supprimé des lignes rangement ou si vous utilisez le prélèvement et le rangement suggérés et avez décidé de ne pas utiliser la feuille rangement, vous pouvez créer ou recréer des instructions de rangement pour les lignes réception validées.

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réceptions entrep. enreg.**, puis cliquez sur le lien associé.  
2.  Sélectionnez une réception validée pouvant nécessiter un rangement.  
3.  Sélectionnez l’action **Fiche**.  

    Si le champ **Statut document** est blanc, la réception n’a pas été rangée. Sinon, le champ indique que la réception est partiellement rangée ou entièrement rangée.  

4.  Si la réception est partiellement rangée ou n’est pas rangée du tout, choisissez l’action **Créer rangement**.  
5.  Renseignez la page de demande de traitement par lots pour créer le rangement comme vous le souhaitez, puis sélectionnez le bouton **OK**.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/receive-put-away-items/)

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]