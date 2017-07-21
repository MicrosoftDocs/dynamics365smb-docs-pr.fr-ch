---
title: Configuration des campagnes marketing dans Financials | Microsoft Docs
description: "Décrit la manière dont vous pouvez configurer et mener des campagnes marketing dans Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 05/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 92c5fb75f4f3d3180ba67b89481beed2e58c3dbe
ms.openlocfilehash: 68359d2dd2c2e07463babda91d86d47998f0912a
ms.contentlocale: fr-ch
ms.lasthandoff: 05/31/2017


---
# <a name="managing-marketing-campaigns"></a>Gestion de campagnes marketing
Disposer d'une solide stratégie marketing permet d'identifier, d'attirer et de fidéliser les clients. Une stratégie marketing est composée de diverses campagnes ainsi que d'interactions en relation avec vos activités de vente et de marketing. Lors de la planification d'une campagne, vous devez choisir les contacts à cibler, le type de campagne (salon, courrier direct) et le vendeur chargé de chaque tâche.

Chaque campagne est composée de diverses activités ou actions. Vous pouvez combiner plusieurs tâches, par exemple les tâches qui représentent chacune une étape, dans les activités. Les tâches d'activité sont liées entre elles par une formule de date. Les tâches individuelles peuvent être affectées uniquement à des vendeurs. Les activités peuvent être affectées aux opportunités, vendeurs, groupes de vendeurs et contacts. Pour plus d'informations, voir [Procédure : configurer des cycles de vente opportunité et des étapes de cycle](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Définition de campagnes individuelles
Pour pouvoir créer une campagne, vous devez configurer des *codes statut campagne*. Ceux-ci permettent de gérer vos campagnes en affectant un statut à la campagne. Lorsque vous travaillez sur les étapes d'une campagne, vous pouvez voir où en est la campagne et visualiser l'étape suivante. Vous devez configurer des codes statut campagne dans la fenêtre **Statut campagne**.

Vous pouvez créer une fiche campagne pour toutes les campagnes que vous voulez suivre. Vous pouvez également afficher les fiches campagne pour visualiser des informations générales sur les campagnes.
Vous pouvez supprimer des écritures campagne, par exemple si elles font état d'une action qui a été annulée. Vous ne pouvez supprimer que les écritures campagne annulées.

### <a name="selecting-the-target-audience"></a>Sélection du public cible
Après avoir créé une campagne, vous pouvez commencer à créer les segments qui spécifient le public cible de la campagne. Pour plus d'informations, voir [Gestion des segments](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Enregistrement des pourcentages de remise
Lorsque vous avez défini votre campagne, que vous avez déterminé les segments que la campagne doit couvrir et défini les dates début et dates de fin, vous enregistrez le pourcentage de la remise auquel le client a droit pour chaque article dans les lignes de la fenêtre **Remises ligne vente**. Vous pouvez également enregistrer les prix de vente pour des articles individuels sur les lignes de la fenêtre **Prix vente**. Vous pouvez accéder aux deux fenêtres à partir de la fiche campagne.

 Lorsque vous avez défini les prix vente/remises ligne et les segments dans la fiche campagne, vous devez les activer afin que les lignes reflètent les prix/remises de la campagne.

**Remarque** : afin que vous puissiez activer les prix vente/remises ligne, vous devez spécifier si le segment entier ou une partie seulement des contacts sont des cibles de la campagne. Si les prix vente/remises ligne couvrent tous les contacts du segment, sélectionnez le champ **Cible campagne** sur le raccourci **Campagne** de la fiche **Segment**.
Si les prix vente/remises ligne ne sont pas offerts à tous les contacts du segment, vous pouvez désélectionner le champ **Cible campagne** pour les contacts appropriés. Si vous ne pouvez pas visualiser ce champ, vous pouvez l'ajouter à votre affichage. Pour plus d'informations, voir [Personnalisation utilisateur](ui-user-personalization.md).

## <a name="conducting-campaigns"></a>Mise en place de campagnes
Au cours de la campagne, toutes les interactions avec vos contacts (segments) sont enregistrées afin que vous puissiez obtenir des statistiques et autres informations sur les coûts et taux de réussite la concernant.

Les campagnes sont conduites par les vendeurs, vous devez créer des activités pour représenter chaque tâche et les affecter aux vendeurs appropriés. Pour plus d'informations, voir [Procédure : configurer des cycles de vente opportunité et des étapes de cycle](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Gestion des segments](marketing-segments.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utilisation de Financials](ui-work-product.md)  

