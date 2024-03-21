---
title: Création des interactions sur les contacts et les segments
description: Découvrez comment créer des interactions dans Business Central pour les communications avec vos contacts et segments.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.reviewer: ivkoleti
ms.date: 12/13/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
ms.service: dynamics-365-business-central
---
# Création des interactions sur les contacts et les segments

Vous pouvez créer des interactions pour suivre les communications avec un seul contact ou avec plusieurs contacts dans vos segments. Pour faciliter la création d’interactions, [!INCLUDE [prod_short](includes/prod_short.md)] fournit le guide de configuration assistée **Créer une interaction**. Le guide vous aide à capturer les détails importants sur l’interaction.

Cependant, avant de pouvoir créer des interactions, vous devez configurer des modèles interaction. Pour en savoir plus sur les modèles interaction, consultez [Configurer les modèles interaction](marketing-interactions.md).

## Pour créer une interaction avec un contact

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Contacts**, **Vendeur** ou **Écriture journal interaction**, puis choisissez le lien associé.
2. Sélectionnez l’action **Créer interaction**.
3. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si vous devez arrêter avant d’avoir terminé l’interaction, vous pouvez choisir **Annuler**, puis spécifier si vous souhaitez enregistrer vos paramètres afin de pouvoir continuer plus tard. Pour en savoir plus sur les interactions reportées, consultez [Pour terminer la configuration d’une interaction reportée](#to-finish-setting-up-a-postponed-interaction).

## Pour créer une interaction sur un segment

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Segments**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Créer interaction**.
3. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Après avoir attribué une interaction à un segment, vous pouvez effectuer plusieurs autres actions sur la page **Segment** :
>
> * Personnalisez l’interaction pour chaque contact particulier au sein du segment, par exemple en sélectionnant un autre modèle interaction sur les lignes.  
>* Journalisez le segment et les interactions en choisissant l’action **Journaliser** pour ouvrir la page **Journaliser segment**.
> * Créez un segment contenant les mêmes contacts en choisissant la case à cocher **Créer segment suivi**. Ce paramètre nécessite qu’une série de numéros soit spécifiée pour les segments sur la page **Configuration marketing**.

Une interaction est enregistrée pour chaque contact inclus dans le segment dans la table **Ecriture journal interaction**, et le segment est journalisé. Les segments journalisés sont disponibles sur la page **Segments journalisés**.

## Pour terminer la configuration d’une interaction reportée

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Interactions reportées**, puis choisissez le lien associé.
2. Choisissez l’interaction que vous souhaitez terminer, puis sélectionnez l’action **Reprendre**.

## Voir aussi

[Enregistrement d’interactions](marketing-interactions.md)  
[Gestion de contacts](marketing-contacts.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utiliser Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]