---
title: 'Procédure : Imprimer les informations liées aux paramètres comptabilité'
description: Avant d'utiliser Business Central dans les affaires quotidiennes, vous pouvez exécuter le rapport Informations de configuration Comptabilité pour afficher les données de base que vous avez définies.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1c39ebde2206524d81f9beccecc80b1b385cc6ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776559"
---
# <a name="print-general-ledger-setup-information"></a>Imprimer les informations liées aux paramètres comptabilité
Avant d'utiliser [!INCLUDE[prod_short](../../includes/prod_short.md)] dans les affaires quotidiennes, vous pouvez exécuter le rapport **Informations de configuration Comptabilité** pour afficher les données de base que vous avez définies. Vous pouvez consulter ces données de base pour disposer d'une base de comparaison, puis vérifier que vous avez correctement configuré les groupes de validation, par exemple.  

## <a name="to-print-general-ledger-setup-information"></a>Pour imprimer les informations liées aux paramètres comptabilité  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Informations de configuration Comptabilité**, puis sélectionnez le lien associé.  
2.  Dans le raccourci **Options**, dans le champ **Informations de configuration**, sélectionnez la zone de données de base comme décrit dans le tableau suivant.  

    |Option|Désignation|  
    |-------------------------------------|---------------------------------------|  
    |**Configuration comptabilité - Données de la société - Consolidation**|Affiche les tables pour la configuration des paramètres comptabilité (en général), les informations sur la société et les centres de profit.|  
    |**Groupes comptabilisation**|Affiche les tables de groupes de comptabilisation des clients, les tables de groupes de comptabilisation des fournisseurs, les tables de groupes de comptabilisation des stocks et les tables de groupes de comptabilisation des comptes bancaires.|  
    |**Validation matrice**|Affiche les tables de groupes comptabilisation marché généraux, les tables de groupes de validation de produits généraux et les tables de groupes de validations générales.|  
    |**Paramètres TVA**|Affiche les tables de groupes comptabilisation marché TVA, les tables de groupes de validation de produits TVA et les tables de groupes de validations TVA.|  
    |**Code journal - Code motif**|Affiche les tables Source, les tables Code journal et les tables Codes motif.|  
    |**Vérifier les souches de numéros**|Sélectionnez cette option pour donner un aperçu de l'utilisation des souches de numéros afin de pouvoir identifier les souches de numéros problématiques pour l'exportation de données dans le cadre du Grundsätze zum Datenzugriff und zur Prüfbarkeit digitaler Unterlagen (GDPdU). L'état indique les souches de numéros avec l'un des problèmes suivants :<br /><br /> -   Les souches de numéros autorisent les numéros de document manuels.<br />-   Les souches de numéros ne sont pas chronologiques.<br />-   Les souches de numéros sont utilisées dans plusieurs tables ou champs.|  

3.  Sélectionnez le bouton **Imprimer** pour imprimer l'état ou le bouton **Aperçu** pour l'afficher à l'écran.  

## <a name="see-also"></a>Voir aussi  
[Configuration de Finance](../../finance-setup-finance.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]