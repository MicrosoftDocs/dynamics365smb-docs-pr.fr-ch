---
title: "Procédure : Créer et imprimer une déclaration de TVA, Suisse"
description: "Selon les informations spécifiées dans la fenêtre **Paramètres compta. TVA**, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] peut créer automatiquement une nouvelle configuration de relevé de TVA pour le report TVA réalisé. Avant de continuer avec les procédures de cette rubrique, assurez-vous que vous avez configuré les paramètres comptabilisation TVA ayant des valeurs spécifiées pour les champs de chiffre d'affaires ventes et achats."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 88f5b0181d6cc676c9afbeb8e14228dd76aa74a1
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-and-print-a-swiss-vat-statement"></a>Créer et imprimer une déclaration de TVA, Suisse
Selon les informations spécifiées dans la fenêtre **Paramètres compta. TVA**, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] peut créer automatiquement une nouvelle configuration de relevé de TVA pour le report TVA réalisé. Avant de continuer avec les procédures de cette rubrique, assurez-vous que vous avez configuré les paramètres comptabilisation TVA ayant des valeurs spécifiées pour les champs de chiffre d'affaires ventes et achats.  

## <a name="to-set-up-a-swiss-vat-statement-template"></a>Pour configurer un modèle de déclaration de TVA suisse  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Mettre à jour le modèle de déclaration de TVA**, puis sélectionnez le lien connexe.  
2.  Sélectionnez un modèle dans le champ **Nom modèle déclaration de TVA**.
3.  Cliquez sur le bouton **OK**. Cliquez sur **Oui** pour confirmer que vous souhaitez créer un modèle.  
4.  Vérifiez la déclaration TVA qui en résulte et ajustez-la autant que nécessaire.  

     La page de déclaration TVA indique le champ **Chiffre de déclaration TVA**, qui indique dans quel zone de la déclaration le résultat sera imprimé. Ce champ est automatiquement renseigné par le traitement par lots selon les informations de la fenêtre **Paramètres compta. TVA**. Le champ peut être modifié, si nécessaire.  

## <a name="to-print-the-swiss-vat-statement"></a>Pour imprimer la déclaration TVA suisse  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Déclaration TVA suisse**, puis sélectionnez le lien connexe.  
2.  Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Date début**|Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état commence.|  
    |**Date fin**|Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état se termine.|  
    |**Clôture avec n° de déclaration de TVA**|Sélectionnez le registre de TVA qui contient la source de comptabilisation des écritures d'ajustement de la TVA. Cette option évalue les périodes comptables qui ont déjà établies. Lorsque vous choisissez cette option, vous ne spécifiez pas les options dans les champs **Inclure écritures TVA** suivants.|  
    |**Inclure écritures TVA**|Sélectionnez l'une des options disponibles.|  
    |**Inclure écritures TVA**|Sélectionnez l'une des options disponibles.|  
    |**% taux normal**|Entrez le taux de TVA standard s'appliquant à la période.|  
    |**% taux réduit**|Saisissez la taxe de TVA réduite pour certains biens et services.|  
    |***% taux hôtel**|Entrez le taux de TVA pour l'hébergement s'appliquant à la période.|  
    |**% normal (autre taux)**|Saisissez un taux TVA secondaire pour des transactions standard s'appliquant à certaines transactions au cours de la période.|  
    |**% réduit (autre taux)**|Saisissez un taux TVA secondaire pour d'autres transactions s'appliquant à certaines transactions au cours de la période.|  
    |**% Hôtel (Autre taux)**|Saisissez un taux TVA secondaire pour l'hébergement s'appliquant à certaines transactions au cours de la période.|  
    |**Afficher montants en devise report**|Choisissez d'afficher les montants dans une devise de report supplémentaire.|  

## <a name="see-also"></a>Voir aussi  
 [Taxe sur la valeur ajoutée, Suisse](swiss-value-added-tax.md)

