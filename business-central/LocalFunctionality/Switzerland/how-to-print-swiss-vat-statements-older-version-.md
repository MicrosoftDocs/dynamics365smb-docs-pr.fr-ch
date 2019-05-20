---
title: 'Procédure : Imprimer les relevés de TVA suisse (ancienne version)'
description: La Déclaration TVA suisse est l'état de calcul standard pour la réalisation de la TVA. Vous pouvez imprimer cet état et l'utiliser avec la déclaration de taxe trimestrielle.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 63d16ae6f310a72b8c3767f2db1c73d36415f37d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245615"
---
# <a name="print-swiss-vat-statements-older-version"></a>Imprimer les relevés de TVA suisse (ancienne version)

> [!NOTE]  
>  Cette rubrique est conservée pour une rétrocompatibilité avec l'état **Déclaration TVA suisse**. Pour plus d'informations sur l'utilisation de la dernière déclaration TVA suisse, voir Déclaration de TVA en Suisse.  

La **Déclaration TVA suisse** est l'état de calcul standard pour la réalisation de la TVA. Vous pouvez imprimer cet état et l'utiliser avec la déclaration de taxe trimestrielle. La **Déclaration TVA suisse** inclut les points suivants :  

- Écriture TVA  
- Écritures d'ajustement de la TVA  
- Feuille de comptabilité  

## <a name="to-print-the-swiss-vat-statement"></a>Pour imprimer la déclaration TVA suisse  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Déclaration TVA suisse**, puis sélectionnez le lien connexe.  

    > [!NOTE]  
    >  Vous recevrez un message indiquant que **Déclaration TVA suisse** s'ouvre dans la langue locale.  

2.  Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Clôturé avec n° feuille**|Sélectionnez les feuilles grand livre contenant la source de comptabilisation des écritures d'ajustement de la TVA. Ce champ évalue les périodes comptables qui ont déjà établies.|  
    |**Ouvrir jusqu'à la date**|Sélectionnez la dernière date pour régler les écritures TVA ouvertes ou non définies.|  
    |**Afficher les validations**|Spécifie si toutes les écritures TVA pour chaque groupe sont imprimées.|  
    |**Afficher rétrofacturation**|Indique si les écritures TVA et les écritures comptables avec des résumés fermés ou des taxes republiées seront imprimées.|  
    |**% TVA taux normal**|Sélectionnez les taux de TVA courants actuels utilisés pour affecter les tarifs corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.|  
    |**% TVA taux réduit**|Sélectionnez les taux d'imposition réduits actuels utilisés pour affecter les taux corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.|  
    |**% TVA Taux spécial**|Sélectionnez les taux d'imposition spéciaux actuels utilisés pour affecter les taux corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.|  
    |**Compte général TVA achat investissements/opérations**|Sélectionnez le compte général TVA.|  
    |**Groupe activités consom. perso.**|Sélectionnez le groupe d'activités et de produits pour votre propre consommation.|  
    |**Groupe activ. serv. étrang.**|Sélectionnez le groupe d'activités de service et de produits étrangers.|  
    |**Groupe activ. export.**|Sélectionnez le groupe d'activités et de produits pour les exportations.|  

3.  Sélectionnez le bouton **Imprimer** pour imprimer la déclaration de TVA, ou le bouton **Aperçu** pour l'afficher à l'écran.  

## <a name="see-also"></a>Voir aussi  
 [Taxe sur la valeur ajoutée, Suisse](swiss-value-added-tax.md)   
 [Taux de TVA pour la Suisse](vat-rates-for-switzerland.md)
