---
title: Planification avec/sans magasin | Microsoft Docs
description: il est important de comprendre le fonctionnement de la planification avec/sans codes magasin sur les lignes demande.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 964bcd38897e676baa993399fe772b8ccfdc9ea0
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="planning-with-or-without-locations"></a>Planification avec/sans magasin.
En ce qui concerne la planification avec ou sans code magasin sur les lignes demande, le système opère directement lorsque :  

-   Les lignes demande indiquent systématiquement le code magasin et le système exploite intégralement les points de stock, y compris le paramètre de magasin pertinent.  
-   Les lignes demande n'indiquent jamais le code magasin et le système n'utilise ni les points stock ni le paramètre de magasin (reportez-vous au dernier cas de figure ci-dessous).  

Toutefois, si les lignes demande indiquent parfois le code magasin, mais pas de manière systématique, le système de planification suit certaines règles en fonction de la configuration.  

## <a name="demand-at-location"></a>Demande dans le magasin  
Lorsque le système de planification détecte une demande dans un magasin (identifiée par une ligne dotée d'un code magasin), il peut procéder de plusieurs manières en fonction de 3 valeurs critiques.  

Lors de l'exécution de la planification, le système recherche ces 3 paramètres l'un après l'autre et effectue la planification en conséquence :  

1.  Le champ **Magasin obligatoire** est-il activé ?  

    Si oui :  

2.  Existe-t-il un point de stock pour l'article ?  

    Si oui :  

    L'article est planifié en fonction des paramètres de planification de la fiche point de stock.  

    Si non :  

3.  Le champ **Mag. composant par déf** contient-il le code magasin demandé ?  

    Si oui :  

    L'article est planifié en fonction des paramètres de planification de la fiche article.  

    Si non :  

    L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot*, Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide. (Les articles qui suivent l’*ordre* de la méthode réapprovisionnement continuent à  *le* suivre, tout comme les autres paramètres.)  

> [!NOTE]  
>  Cette solution minimale couvre strictement la demande. Tout paramètre de planification défini est ignoré.  

Consultez les variantes des cas de figure ci-dessous.  

## <a name="demand-at-blank-location"></a>Demande dans un magasin blanc  
Même si la case à cocher **Magasin obligatoire** est activée, le système autorise la création de lignes demande sans code magasin, ce que l'on appelle également « magasin *VIDE* ». Il s'agit d'un écart pour le système car il a plusieurs valeurs de paramétrage accordées pour gérez les emplacements (voir ci-dessus) et, par conséquent, le moteur de planification ne crée pas de ligne planning pour une telle ligne demande. Si le champ **Magasin obligatoire** n'est pas sélectionné mais si une des valeurs d'emplacement existe, c'est également considéré comme un écart et le système de planification réagira en proposant la « solution minimale » :   
L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour lot* (l' *ordre* conserve la valeur *Ordre)*, Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

Consultez les variantes des scénarios de configuration ci-dessous.  

### <a name="setup-1"></a>Configuration 1 :  

-   Magasin obligatoire = *Oui*  
-   Le point de stock a pour valeur  *ROUGE*  
-   Mag. composant par déf =  *BLEU*  

#### <a name="case-11-demand-is-at--red-location"></a>Situation 1.1 : la demande concerne un magasin  *ROUGE*.  

L'article est planifié en fonction des paramètres de planification de la fiche point de stock (y compris, un éventuel transfert).  

#### <a name="case-12-demand-is-at--blue-location"></a>Situation 1.2 : la demande concerne un magasin  *BLEU*.  

L'article est planifié en fonction des paramètres de planification de la fiche article.  

#### <a name="case-13-demand-is-at--green-location"></a>Situation 1.3 : la demande concerne un magasin  *VERT*.  

L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

#### <a name="case-14-demand-is-at--blank-location"></a>Situation 1.4 : la demande concerne un magasin  *BLANC*.  

L'article n'est pas planifié car aucun magasin n'est défini sur la ligne demande.  

### <a name="setup-2"></a>Configuration 2 :  

-   Magasin obligatoire = *Oui*  
-   Il n 'existe pas de point de stock.  
-   Mag. composant par déf =  *BLEU*  

#### <a name="case-21-demand-is-at--red-location"></a>Situation 2.1 : la demande concerne un magasin  *ROUGE*.  

L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

#### <a name="case-22-demand-is-at--blue-location"></a>Situation 2.2 : la demande concerne un magasin  *BLEU*.  

L'article est planifié en fonction des paramètres de planification de la fiche article.  

### <a name="setup-3"></a>Configuration 3 :  

-   Magasin obligatoire = *Non*  
-   Il n 'existe pas de point de stock.  
-   Mag. composant par déf =  *BLEU*  

#### <a name="case-31-demand-is-at--red-location"></a>Situation 3.1 : la demande concerne un magasin  *ROUGE*.  

L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

#### <a name="case-32-demand-is-at--blue-location"></a>Situation 3.2 : la demande concerne un magasin  *BLEU*.  

L'article est planifié en fonction des paramètres de planification de la fiche article.  

#### <a name="case-33-demand-is-at--blank-location"></a>Situation 3.3 : la demande concerne un magasin  *BLANC*.  

L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

### <a name="setup-4"></a>Configuration 4 :  

-   Magasin obligatoire = *Non*  
-   Il n 'existe pas de point de stock.  
-   Mag. composant par déf =  *VIDE*  

#### <a name="case-41-demand-is-at--blue-location"></a>Situation 4.1 : la demande concerne un magasin  *BLEU*.  

L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.  

#### <a name="case-42-demand-is-at--blank-location"></a>Situation 4.2 : la demande concerne un magasin  *BLANC*.  

L'article est planifié en fonction des paramètres de planification de la fiche article.  

Comme vous pouvez le voir au dernier cas de figure, le seul moyen d'obtenir des résultats corrects pour une ligne demande sans code magasin consiste à désactiver toutes les valeurs de configuration relatives aux magasins. De la même manière, le seul moyen d'obtenir des résultats de planification stables pour les demandes dans des magasins consiste à utiliser des points de stock.  

Par conséquent, si vous planifiez souvent des demandes dans des magasins, il est fortement recommandé d'utiliser la fonctionnalité des points de stock.  

## <a name="see-also"></a>Voir aussi
[Planifié](production-planning.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

