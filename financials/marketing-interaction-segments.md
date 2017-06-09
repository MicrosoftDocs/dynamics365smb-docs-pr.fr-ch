---
title: Interactions et segments | Microsoft Docs
description: "Décrit comment utiliser les segments sur les contacts dans Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 39e7f95cb98364a9a4fce44165ae7f9f3e5b7383
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="interactions-and-segments"></a>Interactions et segments
La fenêtre **Segment** est un type de feuille activité dans laquelle vous pouvez effectuer les opérations suivantes :

* Création de segments
* Enregistrement des critères de segmentation utilisés pour sélectionner des contacts.
* Journalisation du segment et enregistrement des interactions impliquant les contacts du segment.

## <a name="segmenting"></a>Segmentation
Il existe plusieurs méthodes de création de segments :

* Sur les lignes segment, vous pouvez saisir manuellement les contacts à inclure dans le segment.
* Vous pouvez sélectionner des contacts.
* Vous pouvez réutiliser un segment journalisé sur la base duquel vous créerez un nouveau segment.
* Vous pouvez réutiliser des critères de segmentation enregistrés.

## <a name="interactions"></a>Interactions
Dans la fenêtre **Segment**, vous pouvez créer simultanément des interactions pour plusieurs contacts. Par exemple, vous pouvez fusionner un segment avec un document Microsoft Word de manière à envoyer une lettre à tous les contacts inclus dans le segment.

Vous pouvez définir des données sur l'interaction pour le segment qui apparaît dans l'en-tête **Segment**. Par exemple, vous pouvez choisir le modèle interaction à utiliser pour tous les contacts, saisir une désignation, définir un type correspondance, et ainsi de suite. Vous pouvez cependant modifier ces données dans la ligne segment de chaque contact, par exemple en saisissant une désignation différente pour un contact. Si vous fusionnez un segment avec un document Microsoft Word, vous pouvez personnaliser le document à envoyer à un ou à plusieurs contacts inclus dans le segment, par exemple en ajoutant au document des commentaires spécifiques.

## <a name="logging"></a>Journalisation
Dans la fenêtre **Segment**, lorsque vous cliquez sur **Journaliser**, l'application enregistre les interactions dans la fenêtre **Ecriture journal interaction** et journalise le segment. Une fois le segment journalisé, il n'apparaît plus que dans la fenêtre **Segments journalisés**.

Dans la fenêtre **Segments journalisés**, vous pouvez choisir de créer un suivi segment contenant les mêmes contacts que le segment que vous avez journalisé.

## <a name="see-also"></a>Voir aussi
[Procédure : créer des segments](marketing-how-create-segment.md)  
[Procédure : créer des interactions pour des segments](marketing-how-create-interactions.md)  
[Gestion des segments](marketing-segments.md)  
[Enregistrement des interactions avec les contacts](marketing-interactions.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Création et gestion des contacts](marketing-contacts.md)  
[Utilisation de Financials](ui-work-product.md)

