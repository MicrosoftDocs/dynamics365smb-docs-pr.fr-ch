---
title: Planification avec/sans magasin.
description: "Dans cette rubrique, découvrez la production et la fabrication, y compris la planification des approvisionnements, dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
---
# Planification avec/sans magasin.

Avant de commencer à utiliser le moteur de planification, nous vous recommandons de décider d’utiliser ou non les magasins. Il existe deux principaux moyens simples :

* Les lignes demande indiquent systématiquement le code magasin et le système exploite intégralement les points de stock, y compris le paramètre de magasin pertinent. En savoir plus sur [Demande dans le magasin](#demand-at-location).  
* Les lignes de demande ne comportent jamais de codes d’emplacement et le système utilise la fiche article. Voir le scénario [Demande dans un « magasin vide »](#demand-at-blank-location) ci-dessous.

## Demande dans le magasin  

Lorsque le système de planification détecte une demande dans un magasin (identifiée par une ligne dotée d’un code magasin), il peut procéder de plusieurs manières en fonction de 2 valeurs critiques.  

Lors de l’exécution de la planification, le système recherche ces 2 paramètres l’un après l’autre et effectue la planification en conséquence :  

1. Existe-t-il une référence pour l’article au magasin demandé ?  

    Si oui :  

    L’article est planifié en fonction des paramètres de planification de la fiche point de stock.  

    Si non :  

2. Le champ **Mag. composant par déf.** de la page **Paramètres production** contient-il le code magasin demandé ?  

    Si oui :  

    L’article est planifié en fonction des paramètres de planification de la fiche article.  

    Si non :  

    L’article est planifié selon « l’alternative minimale » qui couvre la demande exacte. Les paramètres de planification sont définis comme suit : Méthode réapprovisionnement = *Lot pour Lot*, Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide. (Les articles qui suivent l’*ordre* de la méthode réapprovisionnement continuent à *le* suivre, tout comme les autres paramètres.)

> [!TIP]
> Si vous planifiez souvent des demandes dans différents magasins, nous vous recommandons d’utiliser la fonction Points de stock et d’éviter toute demande dans un magasin vide. En savoir plus sur [Configurer les points de stock](inventory-how-to-set-up-stockkeeping-units.md)

Consultez les variantes des [cas de figure ci-dessous](#scenarios).

> [!NOTE]
> Ce champ **Mag. composant par déf.** sur la page **Paramètres production** jouent un rôle fondamental quant à la manière de régir la gestion des lignes demande, avec ou sans codes magasin.
>
> Concernant l’ordre de fabrication, [!INCLUDE [prod_short](includes/prod_short.md)] utilise pour le sous-ensemble et les composants le magasin mentionné sur l’ordre de fabrication. Toutefois, en complétant ce champ, vous pouvez rediriger le sous-ensemble et les composants vers un autre magasin.
>
> Vous pouvez également définir ceci pour un point de stock précis en sélectionnant un code magasin différent dans le champ **Mag. composant par déf** de la fiche point de stock. Remarquez toutefois que cette action est rarement utilisée, comme la logique planning peut être altérée lors de la planification pour le composant point de stock.

## Demande dans un « magasin vide »

En général, lorsque le système de planification détecte une demande à un emplacement vide (une ligne sans code emplacement), l’article est planifié en fonction des paramètres de planification de la fiche article.

Le champ **Magasin obligatoire** de la page **Paramètres stock** et le champ **Mag. composant par déf.** de la page **Paramètres production** ou les points de stock régissent la façon dont le système de planification traite les lignes de demande avec ou sans codes magasin. Si une des instructions suivantes est vraie, la demande dans le magasin vide est également considérée comme un écart et le système de planification réagira en utilisant la « solution minimale » : l’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*, Tous les autres paramètres de planification ont la valeur Vide.

* Sur le champ **Paramètres production**, le champ **Mag. composant par déf.** est défini sur une valeur.
* Indique qu’un point de stock existe pour l’article planifié.
* Le champ **Magasin obligatoire** est sélectionné.

## Cas de figure

Consultez les variantes des scénarios de configuration ci-dessous.

### Configuration 1

* Magasin obligatoire = *Oui*  
* Le point de stock a pour valeur *OUEST*  
* Mag. composant par déf = *EST*  

#### Situation 1.1 : la demande concerne un magasin *OUEST*

L’article est planifié en fonction des paramètres de planification de la fiche point de stock (y compris, un éventuel transfert).

#### Situation 1.2 : la demande concerne un magasin *EST*

L’article est planifié en fonction des paramètres de planification de la fiche article.

#### Situation 1.3 : la demande concerne un magasin *NORD*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

#### Situation 1.4 : la demande concerne un magasin *VIDE*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

### Configuration 2

* Magasin obligatoire = *Oui*  
* Il n ’existe pas de point de stock.  
* Mag. composant par déf = *EST*  

#### Situation 2.1 : la demande concerne un magasin *OUEST*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

#### Situation 2.2 : la demande concerne un magasin *EST*

L’article est planifié en fonction des paramètres de planification de la fiche article.  

### Configuration 3

* Magasin obligatoire = *Non*  
* Il n ’existe pas de point de stock.  
* Mag. composant par déf = *EST*  

#### Situation 3.1 : la demande concerne un magasin *OUEST*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

#### Situation 3.2 : la demande concerne un magasin *EST*

L’article est planifié en fonction des paramètres de planification de la fiche article.  

#### Situation 3.3 : la demande concerne un magasin *VIDE*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

### Configuration 4

* Magasin obligatoire = *Non*  
* Il n ’existe pas de point de stock.  
* Mag. composant par déf = *VIDE*  

#### Situation 4.1 : la demande concerne un magasin *EST*

L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot* (l’*ordre* conserve la valeur *Ordre*), Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.

#### Situation 4.2 : la demande concerne un magasin *VIDE*

L’article est planifié en fonction des paramètres de planification de la fiche article.

Comme vous pouvez le voir au dernier cas de figure, le seul moyen d’obtenir des résultats corrects pour une ligne demande sans code magasin consiste à désactiver toutes les valeurs de configuration relatives aux magasins. De la même manière, le seul moyen d’obtenir des résultats de planification stables pour les demandes dans des magasins consiste à utiliser des points de stock.  

Par conséquent, si vous planifiez souvent des demandes dans des magasins, nous vous recommandons d’utiliser la fonction Points de stock.

## Voir la formation associée sur [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## Voir aussi

[Planifié](production-planning.md)  
[Configurer la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Stock](inventory-manage-inventory.md)  
[Configurer des points de stock](inventory-how-to-set-up-stockkeeping-units.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
