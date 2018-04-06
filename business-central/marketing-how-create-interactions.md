---
title: "Créer des interactions sur les contacts et les segments| Microsoft Docs"
description: "Décrit comment créer des interactions pour les communications que vous avez avec vos contacts et segments dans Business Central, par exemple le courrier direct."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: aa6be34f1b43dfe0b1f82cbb6a2cefd06edb0f83
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-interactions-on-contacts-and-segments"></a>Créer des interactions sur les contacts et les segments
Vous pouvez créer des interactions pour enregistrer toutes les interactions et toutes les communications que vous entretenez avec vos contacts et segments, par exemple le courrier direct.

Pour pouvoir créer des interactions, vous devez configurer des modèles interaction. Pour plus d'informations, reportez vous à [Configurer des modèles interaction](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Pour créer une interaction
1. Ouvrez le contact, le vendeur, ou l'écriture journal interaction.
2. Sélectionnez l'action **Créer interaction**.
3. Renseignez les champs, puis cliquez sur le bouton **OK**.

> [!NOTE]  
>   Si vous devez effectuer une autre tâche avant de terminer l'interaction, vous pouvez cliquer sur **Annuler** et choisir de terminer l'interaction à une date ultérieure. Cela permet de reporter l'interaction à plus tard.

## <a name="to-finish-and-delete-postponed-interactions"></a>Pour terminer et supprimer les interactions reportées
1. Ouvrez le contact, le vendeur, ou l'écriture journal interaction.
2. Sélectionnez **Interactions reportées**.
3. Sélectionnez l'interaction que vous souhaitez terminer, puis sélectionnez l'action **Reprendre**.

## <a name="to-create-an-interaction-on-a-segment"></a>Pour créer une interaction sur un segment
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Segments**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Segment**, dans la section **Interaction**, renseignez les champs pour définir l'interaction à affecter au segment.

    Après avoir affecté une interaction au segment, vous pouvez personnaliser l'interaction pour chaque contact au sein du segment, par exemple en sélectionnant un autre modèle interaction sur les lignes de la fenêtre **Segment**.  
3. Pour journaliser le segment et les interactions, sélectionnez l'action **Journal**. La fenêtre **Journaliser segment** s’affiche.
4. Si vous souhaitez créer un segment contenant les mêmes contacts, activez la case à cocher **Créer suivi segment**. Pour créer un suivi segment, vous devez avoir indiqué une souche de numéros pour les segments dans la fenêtre **Paramètres Marketing**.

Une interaction est enregistrée pour chaque contact inclus dans le segment dans la table **Ecriture journal interaction**, et le segment est journalisé. Vous pouvez consulter les segments journalisés dans la fenêtre **Segments journalisés**.

Si vous avez activé la case à cocher **Créer suivi segment**, le programme crée automatiquement un segment contenant les mêmes contacts que le segment journalisé.

## <a name="see-also"></a>Voir aussi
[Enregistrement d'interactions](marketing-interactions.md)  
[Gestion de contacts](marketing-contacts.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Paramétrage de la Gestion des relations](marketing-setup-marketing.md)  
[Utilisation de Business Central](ui-work-product.md)

