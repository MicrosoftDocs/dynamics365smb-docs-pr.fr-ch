---
title: "Personnaliser les signaux visuels à propos de l'activité d'une pile | Microsoft Docs"
description: "Configurez un indicateur en couleur sur une vignette de la pile pour fournir un signal visuel personnalisé de l'activité de la pile."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e4ceaeae1a37a521d2d5bd22ab711757283e6321
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Configurer un indicateur coloré sur des piles
Vous pouvez configurer des piles qui apparaissent sur le Tableau de bord pour inclure un indicateur qui modifie la couleur en fonction des valeurs de données dans les piles.

L'indicateur apparait sous forme d'une barre de couleur le long de la bordure supérieure de la mosaïque Pile. Il offre un signal visuel du statut de l'activité de la pile, ce qui peut indiquer des conditions favorables ou défavorables pour inviter l'utilisateur à prendre des mesures. Par exemple, si une pile affiche les factures vente en cours, vous pouvez définir l'indicateur pour qu'il apparaisse vert (favorable) lorsque le nombre total des factures vente en cours est inférieur à 10, et apparaisse rouge (défavorable) lorsque le total est supérieur à 20.

Dans la fenêtre **Paramètres pile**, vous configurez des indicateurs pour toutes les piles disponibles dans la base de données de la société.

Pour configurer l'indicateur, vous pouvez spécifier jusqu'à deux valeurs de seuil qui définissent trois plages de valeurs de données (basse, moyenne et haute) à laquelle vous pouvez appliquer une couleur différente (ou un style différent).

## <a name="to-set-up-colored-indicators-on-cues"></a>Pour paramétrer des indicateurs colorés sur des piles
1. Sous **Activités** sur votre page Tableau de bord, sélectionnez **Paramétrer piles**.  
   La fenêtre **Paramètres pile** s'affiche. La fenêtre répertorie les indicateurs actuellement paramétrés sur des piles.
2. Pour modifier un indicateur, modifiez les champs et modifiez, par exemple, les valeurs pour des seuils différents.  

Le tableau suivant répertorie les couleurs correspondant aux options des champs **Style bas de gamme**, **Style milieu de gamme** et **Style haut de gamme**.

| Option | Couleur |
| --- | --- |
| **Aucun** |Aucune couleur (même couleur que la mosaïque Pile)|
| **Favorable** |Vert |
| **Défavorable** |Rouge |
| **Ambigu** |Jaune |
| **Subordonné** |Gris |

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

