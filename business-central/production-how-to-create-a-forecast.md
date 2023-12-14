---
title: Créer une prévision de la demande
description: Découvrez les fonctionnalités de prévision de la demande et comment créer des prévisions de vente et de production.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9245, 99000919, 99000921, 99000922'
ms.date: 03/11/2022
ms.author: bholtorf
---
# Créer une prévision de la demande

Vous pouvez créer des prévisions de vente et de production à l’aide de la page de liste **Prévisions de demande**. Ensuite, pour chaque prévision, vous devez spécifier divers paramètres dans la page **Aperçu prévision demande**.  

La fonctionnalité de prévision permet de créer une demande anticipée ; la demande réelle est créée à partir de commandes vente et fabrication. Lors de la génération de la planification de production principale (PDP), la prévision est ajustée par rapport aux commandes vente et fabrication. Le champ **Type prévision** sur la prévision détermine le type d’exigences à prendre en considération dans le processus d’ajustement. Si la prévision concerne un *article vente*, seules les commandes vente ajustent la prévision. Si elle concerne les *composants*, seule la demande dépendante des composants O.F. ajuste la prévision.  

Les prévisions permettent à votre société de créer des scénarios basés sur des hypothèses, de planifier et de répondre à la demande de façon efficace et rentable. Des prévisions précises peuvent faire la différence au niveau de la satisfaction de la clientèle en relation avec les dates promesse des livraisons et la ponctualité de ces dernières.  

Avec la 1re vague de lancement 2022, vous pouvez aussi définir le niveau de détails souhaité dans les champs **Prévision par magasin** et **Prévision par variante** sur la page **Aperçu prévision demande**. Les filtres et autres paramètres sont stockés dans la table **Nom prévision demande**. Ainsi, vous pouvez facilement arrêter votre travail et le reprendre ultérieurement. Si votre organisation a effectué la mise à jour lors de la 1re vague de lancement 2022, vous devez activer la nouvelle expérience dans la page [Gestion des fonctionnalités](admin-feature-management.md).  

## Prévisions de vente et de fabrication

La fonctionnalité de prévision de l’application permet de générer des prévisions de vente ou de fabrication, de façon combinée ou indépendante. Par exemple, la plupart des sociétés qui fabriquent à la commande ne gèrent pas un stock de produits finis parce que chaque article est produit au moment de la commande. L’anticipation sur les commandes (prévision de vente) est essentielle pour aboutit à un délai de production raisonnable des produits finis (prévision de production). À titre d’exemple, les composants nécessitant un délai de livraison important, s’ils ne sont pas en commande ou en stock, peuvent retarder la fabrication.  

- La prévision de vente est le meilleur indicateur du service commercial en relation avec les ventes futures et est spécifiée par article et par période. Toutefois, la prévision de vente n’est pas toujours appropriée pour la fabrication.  
- La prévision de production est l’estimation par le gestionnaire de production du nombre d’articles finis et de produits semi-finis à produire dans des périodes données afin de satisfaire les prévisions de vente.  

Dès lors, le plus souvent, le gestionnaire de production modifie la prévision de vente pour l’adapter aux conditions de production, tout en satisfaisant à la prévision de vente.  

Vous créez des prévisions manuellement sur la page **Prévision demande**. Plusieurs prévisions peuvent exister dans le système, qui se différencient par leur nom et leur type. Vous pouvez copier et modifier les prévisions si nécessaire. 

> [!NOTE]
> Il ne peut y avoir qu’une seule prévision valide à la fois en relation avec le planning.

La prévision consiste en un certain nombre d’enregistrements indiquant un numéro d’article, une date prévision et une quantité prévision. La prévision d’un article couvre une période qui est définie par la date prévision et la date prévision de l’enregistrement prévision suivant. Du point de vue du planning, la quantité prévue doit être disponible au début de la période de demande.  

Vous devez désigner une prévision comme *Article vente*, *Composant* ou *Les deux*. Le type prévision *Article vente* est utilisé pour la prévision de vente. La prévision de production est créée à l’aide du type *Composant*. Le type de prévision *Les deux* n’est utilisé que pour donner au gestionnaire un aperçu de la prévision de vente et de la prévision de production. Avec cette option, les écritures prévisions ne sont pas modifiables. En désignant ces types de prévision ici, vous pouvez utiliser la même feuille pour entrer une prévision de vente que pour une prévision de production, ainsi qu’utiliser la même feuille pour afficher les deux prévisions simultanément. Notez que le système traite les différentes entrées (vente et production) de façon différente lors du calcul du planning, en fonction de la configuration de l’article, de la fabrication et de la production.  

## Prévision composant

La prévision composant peut être considérée comme une prévision d’option en relation avec un article parent. Cela peut, par exemple, être utile si le gestionnaire peut estimer la demande pour le composant.  

Du fait que la prévision composant sert à définir des options pour un article parent, la valeur de prévision composant doit être inférieure ou égale à la quantité de vente d’article prévue. Si la valeur de prévision composant est supérieure à la prévision de vente d’article, le système traite la différence entre ces deux types de prévisions comme une demande indépendante.  

## Périodes de prévision

La période de prévision est valide de la date début jusqu’à la date de début de la prévision suivante. La page d’intervalle de temps offre plusieurs choix pour insérer la demande à une date spécifique dans une période. Il est donc recommandé de ne pas modifier l’étendue de la période de prévision à moins de déplacer toutes les écritures de prévision à la date début de cette période.  

## Prévision par magasin

Sur la page **Paramètres production**, vous pouvez spécifier la manière dont vous voulez prendre en compte les emplacements définis dans les prévisions lorsque vous calculez des plans. 

### Prévision sur magasin

Si vous activez le bouton de basculement **Prévision sur magasin**, [!INCLUDE[prod_short](includes/prod_short.md)] respectera tous les codes magasin spécifiés pour chaque écriture de prévision de la demande et calculera la prévision restante pour chaque magasin.  

Prenons cet exemple : votre entreprise achète et vend des articles dans deux magasins : EST et OUEST. Pour les deux magasins, vous avez configuré une politique de réorganisation de lot à lot. Vous créez une prévision pour les deux magasins :

- 10 pièces pour le magasin EST
- 4 pièces pour le magasin OUEST

Ensuite, vous créez une commande client avec une quantité de 12 sur le magasin OUEST. Le système de planification vous suggérera de faire ce qui suit :

- Reconstituez 10 pièces pour le magasin EST, en fonction des données des prévisions.  
- Reconstituez 12 pièces pour le magasin OUEST, en fonction de la commande client. Les 4 pièces spécifiées dans la prévision sont entièrement consommées par la demande réelle de la commande client. Pour plus d’informations, reportez-vous à la section [La demande de prévision est réduite par les commandes vente](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Si les prévisions basées sur le magasin sont consultées isolément, il se peut que la prévision globale ne soit pas représentative.

### Ne pas utiliser Prévision sur magasin

Si vous désactivez le bouton de basculement **Prévision sur magasin**, [!INCLUDE[prod_short](includes/prod_short.md)] ignorera les codes magasin spécifiés pour chaque écriture de prévision de la demande et agrègera les prévisions en une prévision pour les magasins vides.  

Prenons cet exemple : votre entreprise achète et vend des articles dans deux magasins : EST et OUEST. Pour les deux magasins, vous avez configuré une politique de réorganisation de lot à lot. Vous créez une prévision pour les deux magasins :

- 10 pièces pour le magasin EST
- 4 pièces pour le magasin OUEST

Ensuite, vous créez une commande client avec une quantité de 12 sur le magasin OUEST. Le système de planification vous suggérera de faire ce qui suit :

- Reconstituez 12 pièces pour le magasin OUEST, en fonction de la commande client.  
- Reconstituez 2 pièces pour le magasin vide. Les 10 et 4 pièces spécifiées dans la prévision sont partiellement consommées par la demande réelle de la commande client. [!INCLUDE[prod_short](includes/prod_short.md)] a ignoré les codes magasin spécifiés par l’utilisateur et utilise à la place un magasin vide.  

> [!NOTE]  
> Vous pouvez définir un filtre par emplacement, mais les résultats basés sur l’emplacement peuvent ne pas correspondre aux résultats de planification sans filtres.

## Pour créer une prévision de la demande

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prévision de la demande**, puis sélectionnez le lien associé.  
2. Sur le raccourci **Général**, choisissez une prévision dans le champ **Nom prévision demande**. Plusieurs prévisions peuvent exister, qui se différencient par leur nom et leur type.  
3. Dans le champ **Filtre magasin**, sélectionnez le magasin auquel s’applique la prévision.
4. Dans le champ **Afficher par** pour modifier la période affichée dans chaque colonne. Vous pouvez choisir entre les intervalles suivants : **Jour**, **Semaine**, **Mois**, **Trimestre**, **Année** ou **Période comptable**, tel que paramétré dans votre espace financier.

> [!NOTE]  
> Vous devez choisir l’intervalle de temps que vous voulez utiliser pour les prévisions futures de façon à ce qu’il soit toujours cohérent. Lorsque vous entrez une quantité prévision, elle vaut dès le premier jour de l’intervalle de temps que vous sélectionnez. Par exemple, si vous sélectionnez un mois, vous devez entrer la quantité prévision au premier jour du mois. Si vous sélectionnez un trimestre, vous devez entrer la quantité prévision au premier jour du premier mois du trimestre.

5. Dans le champ **Afficher en tant que**, sélectionnez la manière dont seront affichées les quantités prévision pour l’intervalle de temps. Si vous sélectionnez **Solde période**, le solde période est affiché pour l’intervalle de temps. Si vous sélectionnez **Solde au**, la page affiche le solde au dernier jour de l’intervalle de temps.  
6. Dans le champ **Type prévision**, choisissez **Article vente**, **Composant** ou **Les deux**. Si vous sélectionnez **Article vente** ou **Composant**, vous pouvez modifier la quantité par période. Si vous sélectionnez **Les deux**, vous ne pouvez pas modifier la quantité mais vous pouvez choisir le bouton flèche déroulante afin de visualiser les écritures prévision demande.  
7. Spécifiez un **filtre date** si vous voulez limiter la quantité de données affichées.  
8. Sur le raccourci **Matrice Prévision demande**, entrez les quantités prévues en saisissant une quantité dans la cellule représentant un article à une date ou une période particulière. Notez que dans les cellules vides, le bouton de recherche ouvre une page vide indiquant que vous devez saisir manuellement une valeur.   

> [!NOTE]  
> Vous pouvez également modifier une prévision existante. Sur la page **Matrice Prévision demande**, choisissez l’action **Copier prévision demande** et renseignez la page **Prévision demande** à l’aide de la prévision existante. Vous pouvez alors modifier les quantités en fonction des besoins.  

## Voir aussi

[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
