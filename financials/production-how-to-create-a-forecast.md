---
title: "Procédure de création d'une prévision production | Microsoft Docs"
description: "Vous pouvez créer des prévisions de vente et de production à l'aide de la fenêtre **Prévision production**."
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
ms.openlocfilehash: 5dea483395e64eb0635879b5c8821428512481ba
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-a-production-forecast"></a>Procédure : créer une prévision production
Vous pouvez créer des prévisions de vente et de production à l'aide de la fenêtre **Prévision production**.  

La fonctionnalité de prévision permet de créer une demande anticipée ; la demande réelle est créée à partir de commandes vente et fabrication. Lors de la génération de la planification de production principale (PDP), la prévision est ajustée par rapport aux commandes vente et fabrication. L'option *Composant* sur la prévision détermine le type d'exigences à prendre en considération dans le processus d'ajustement. Si la prévision a trait à un article vente, seules les commandes vente ajustent la prévision. Si elle concerne les composants, seule la demande dépendante des composants O.F. ajuste la prévision.  

Les prévisions permettent à votre société de créer des scénarios basés sur des hypothèses, de planifier et de répondre à la demande de façon efficace et rentable. Des prévisions précises peuvent faire la différence au niveau de la satisfaction de la clientèle en relation avec les dates promesse des livraisons et la ponctualité de ces dernières.  

## <a name="sales-forecasts-and-production-forecasts"></a>Prévisions de vente et de fabrication  
La fonctionnalité de prévision du programme permet de générer des prévisions de vente ou de fabrication, de façon combinée ou indépendante. Par exemple, la plupart des sociétés qui fabriquent à la commande ne gèrent pas un stock de produits finis parce que chaque article est produit au moment de la commande. L'anticipation sur les commandes (prévision de vente) est essentielle pour aboutit à un délai de production raisonnable des produits finis (prévision de production). À titre d'exemple, les composants nécessitant un délai de livraison important, s'il ne sont pas en commande ou en stock, peuvent retarder la fabrication.  

-   La prévision de vente est le meilleur indicateur du service commercial en relation avec les ventes futures et est spécifiée par article et par période. Toutefois, la prévision de vente n'est pas toujours appropriée pour la fabrication.  
-   La prévision de production est l'estimation par le gestionnaire de production du nombre d'articles finis et de produits semi-finis à produire dans des périodes données afin de satisfaire les prévisions de vente.  

Dès lors, le plus souvent, le gestionnaire de production modifie la prévision de vente pour l'adapter aux conditions de production, tout en satisfaisant à la prévision de vente.  

Vous créez des prévisions manuellement dans la fenêtre **Prévision production**. Plusieurs prévisions peuvent exister dans le système, qui se différencient par leur nom et leur type. Vous pouvez copier et modifier les prévisions si nécessaire. Notez qu'il ne peut y avoir qu'une seule prévision valide à la fois en relation avec le planning.  

La prévision consiste en un certain nombre d'enregistrements indiquant un numéro d'article, une date prévision et une quantité prévision. La prévision d'un article couvre une période qui est définie par la date prévision et la date prévision de l'enregistrement prévision suivant. Du point de vue du planning, la quantité prévue doit être disponible au début de la période de demande.  

Vous devez désigner une prévision comme *Article vente*, *Composant* ou *Les deux*. Le type prévision *Article vente* est utilisé pour la prévision de vente. La prévision de production est créée à l'aide du type *Composant*. Le type de prévision *Les deux* n'est utilisé que pour donner au gestionnaire un aperçu de la prévision de vente et de la prévision de production. Avec cette option, les écritures prévisions ne sont pas modifiables. En désignant ces types de prévision ici, vous pouvez utiliser la même feuille pour entrer une prévision de vente que pour une prévision de production, ainsi qu'utiliser la même feuille pour afficher les deux prévisions simultanément. Notez que le système traite les différentes entrées (vente et production) de façon différente lors du calcul du planning, en fonction de la configuration de l'article, de la fabrication et de la production.  

## <a name="component-forecast"></a>Prévision composant  
La prévision composant peut être considérée comme une prévision d'option en relation avec un article parent. Cela peut, par exemple, être utile si le gestionnaire peut estimer la demande pour le composant.  

Comme la prévision composant sert à définir des options pour un article parent, la valeur de prévision composant doit être inférieure ou égale à la quantité de vente d'article prévue. Si la valeur de prévision composant est supérieure à la prévision de vente d'article, le système traite la différence entre ces deux types de prévision comme une demande indépendante.  

## <a name="forecasting-periods"></a>Périodes de prévision  
 La période de prévision est valide de la date début jusqu'à la date de début de la prévision suivante. La fenêtre d'intervalle de temps offre plusieurs choix pour insérer la demande à une date spécifique dans une période. Il est donc recommandé de ne pas modifier l'étendue de la période de prévision à moins de déplacer toutes les écritures de prévision à la date début de cette période.  

## <a name="forecast-by-locations"></a>Prévision par magasin  
Vous pouvez indiquer, dans les paramètres production, si. Notez cependant que si les prévisions basées sur le magasin sont consultées isolément, il se peut que la prévision globale ne soit pas représentative.

## <a name="to-create-a-production-forecast"></a>Pour créer une prévision production

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Prévision production**, puis sélectionnez le lien connexe.  
2.  Sur le raccourci **Général**, choisissez une prévision dans le champ **Nom prévision production**. Plusieurs prévisions peuvent exister, qui se différencient par leur nom et leur type.  
3.  Dans le champ **Filtre magasin**, sélectionnez le magasin auquel s'applique la prévision.  
4.  Dans le champ **Type prévision**, choisissez **Article vente**, **Composant** ou **Les deux**. Si vous sélectionnez **Article vente** ou **Composant**, vous pouvez modifier la quantité par période. Si vous sélectionnez **Les deux**, vous ne pouvez pas modifier la quantité mais vous pouvez choisir le bouton flèche déroulante afin de visualiser les écritures prévision production.  
5.  Spécifiez un **filtre date** si vous voulez limiter la quantité de données affichées.  
6.  Sur le raccourci **Matrice Prévision production**, entrez les quantités prévues d'**Article vente** ou la prévision **Composant** pour les différentes périodes.  
7.  Sur le raccourci **Options matrice**, définissez l'intervalle de temps dans le champ **Afficher par** pour changer la période affichée dans chaque colonne. Vous pouvez choisir entre les intervalles suivants : **Jour**, **Semaine**, **Mois**, **Trimestre**, **Année**, ou **Période comptable**, telle qu'elle est paramétrée dans Gestion financière.  

    > [!NOTE]  
    >  Vous devez choisir l'intervalle de temps que vous voulez utiliser pour les prévisions futures de façon à ce qu'il soit toujours cohérent. Lorsque vous entrez une quantité prévision, elle vaut dès le premier jour de l'intervalle de temps que vous sélectionnez. Par exemple, si vous sélectionnez un mois, vous devez entrer la quantité prévision au premier jour du mois. Si vous sélectionnez un trimestre, vous devez entrer la quantité prévision au premier jour du premier mois du trimestre.  

8.  Dans le champ **Afficher en tant que**, sélectionnez la manière dont seront affichées les quantités prévision pour l'intervalle de temps. Si vous sélectionnez **Solde période**, le solde période est affiché pour l'intervalle de temps. Si vous sélectionnez **Solde au**, la fenêtre affiche le solde au dernier jour de l'intervalle de temps.  

> [!NOTE]  
>  Vous pouvez également modifier une prévision existante. Dans la fenêtre **Matrice Prévision production**, choisissez l'action **Copier prévision production** et renseignez la fenêtre **Prévision production** à l'aide de la prévision existante. Vous pouvez alors modifier les quantités en fonction des besoins.  

## <a name="see-also"></a>Voir aussi  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

