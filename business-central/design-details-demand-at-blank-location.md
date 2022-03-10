---
title: Détails de conception - Demande et approvisionnement | Microsoft Docs
description: Cette rubrique présente le concept de demande, qui désigne toute sorte de demande brute, par exemple une commande vente et un besoin composant d’un ordre de fabrication.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 3b5f390343f74bc559cce48b2037edd125f829ca
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143649"
---
# <a name="design-details-demand-at-blank-location"></a>Détails de conception : demande à un magasin vide
Quand un utilisateur créé un événement de demande, comme une ligne de commande vente, le programme permet à l’utilisateur de spécifier parfois un code magasin et d’autres fois non, utilisant un magasin vide.

Pour la demande avec ou sans code magasin, le système de planification opère directement lorsque :

- Les lignes demande indiquent systématiquement le code magasin et le système exploite intégralement les points de stock, y compris le paramètre de magasin pertinent.
- Les lignes demande n’indiquent jamais le code magasin et le système n’utilise ni les points de stock ni le paramètre de magasin (reportez-vous au dernier cas de figure dans la section suivante).

Toutefois, si les événements de demande indiquent parfois le code magasin, mais pas de manière systématique, le système de planification suit certaines règles en fonction de la configuration.

## <a name="demand-at-location"></a>Demande dans le magasin
Lorsque le système de planification détecte une demande dans un magasin, il peut procéder de plusieurs manières en fonction de trois valeurs critiques. Lors de l’exécution de la planification, le système recherche ces trois paramètres l’un après l’autre et effectue la planification en conséquence.

1. Le champ **Magasin obligatoire** est-il activé ?

    Si oui :

2. Existe-t-il un point de stock pour l’article ?

    Si oui :

    L’article est planifié en fonction des paramètres de planification de la fiche point de stock.

    Si non :

3. Le champ Mag. composant par déf contient-il le code magasin demandé ?

  Si oui :

  L’article est planifié en fonction des paramètres de planification de la fiche article.

  Si non :

  L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour lot, Inclure stock = Oui. Tous les autres paramètres de planification doivent avoir la valeur Vide. (Les articles pour lesquels Méthode réapprovisionnement = Commande continuent à utiliser Commande, tout comme les autres paramètres.)

> [!NOTE]
> La configuration de planification exceptionnelle produite en dernière réaction à l’étape 3 ci-dessus est appelée dans ce qui suit « solution minimale ». Cette configuration de planification couvre strictement la demande, et tous les autres paramètres de planification sont ignorés.

Pour plus d’informations sur les variations de cette logique de planification, voir la section Scénarios ci-dessous.

## <a name="demand-at-blank-location"></a>Demande dans un magasin blanc
Même si le champ **Magasin obligatoire** est sélectionné, le programme autorise la création de lignes demande sans code magasin, ce que l’on appelle également magasin blanc. Il s’agit d’un écart pour le système car il a plusieurs valeurs de paramétrage accordées pour gérez les emplacements (voir ci-dessus) et, par conséquent, le moteur de planification ne crée pas de ligne planning pour une telle ligne demande.

Si le champ **Magasin obligatoire** n’est pas activé mais que des valeurs de configuration de magasin ont été paramétrées, cela est également considéré comme un écart et le système de planification réagira en utilisant la « solution minimale » : l’article est planifié comme suit : Méthode réapprovisionnement = Lot pour lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui, Tous les autres paramètres de planification ont la valeur Vide.

## <a name="scenarios"></a>Cas de figure
Les scénarios suivants décrivent les variations de la demande au magasin vide et la manière dont le système de planification se décide pour la « solution minimale ».

### <a name="setup-1"></a>Configuration 1 :
Magasin obligatoire = Oui

Le point de stock a pour valeur ROUGE

Mag. composant par déf. = BLEU

#### <a name="case-11-demand-is-at-red-location"></a>Situation 1.1 : la demande concerne un magasin ROUGE.
L’article est planifié en fonction des paramètres de planification de la fiche point de stock.

#### <a name="case-12-demand-is-at-blue-location"></a>Situation 1.2 : la demande concerne un magasin BLEU.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

#### <a name="case-13-demand-is-at-green-location"></a>Situation 1.3 : la demande concerne un magasin VERT.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

#### <a name="case-14-demand-is-at-blank-location"></a>Situation 1.4 : la demande concerne un magasin BLANC.
L’article n’est pas planifié car aucun magasin n’est défini sur la ligne demande.

### <a name="setup-2"></a>Configuration 2 :
Magasin obligatoire = Oui

Il n ’existe pas de point de stock.

Mag. composant par déf. = BLEU

#### <a name="case-21-demand-is-at-red-location"></a>Situation 2.1 : la demande concerne un magasin ROUGE.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

#### <a name="case-22-demand-is-at-blue-location"></a>Situation 2.2 : la demande concerne un magasin BLEU.
L’article est planifié en fonction des paramètres de planification de la fiche article.

### <a name="setup-3"></a>Configuration 3 :
Magasin obligatoire = Non

Il n ’existe pas de point de stock.

Mag. composant par déf. = BLEU

#### <a name="case-31-demand-is-at-red-location"></a>Situation 3.1 : la demande concerne un magasin ROUGE.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

#### <a name="case-32-demand-is-at-blue-location"></a>Situation 3.2 : la demande concerne un magasin BLEU.
L’article est planifié en fonction des paramètres de planification de la fiche article.

#### <a name="case-33-demand-is-at-blank-location"></a>Situation 3.3 : la demande concerne un magasin BLANC.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

### <a name="setup-4"></a>Configuration 4 :
Magasin obligatoire = Non

Il n ’existe pas de point de stock.

Mag. composant par déf. = BLANC

#### <a name="case-41-demand-is-at-blue-location"></a>Situation 4.1 : la demande concerne un magasin BLEU.
L’article est planifié comme suit : Méthode réapprovisionnement = Lot pour Lot (l’ordre conserve la valeur Ordre), Inclure stock = Oui. Tous les autres paramètres de planification ont la valeur Vide.

#### <a name="case-42-demand-is-at-blank-location"></a>Situation 4.2 : la demande concerne un magasin BLANC.
L’article est planifié en fonction des paramètres de planification de la fiche article.

Comme indiqué au dernier cas de figure, le seul moyen d’obtenir des résultats corrects pour une ligne demande sans code magasin consiste à désactiver toutes les valeurs de configuration relatives aux magasins. De la même manière, le seul moyen d’obtenir des résultats de planification stables pour les demandes dans des magasins consiste à utiliser des points de stock. Par conséquent, si les sociétés planifient souvent des demandes dans des magasins, il leur est fortement recommandé d’utiliser le module des points de stock.

## <a name="see-also"></a>Voir aussi  
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]