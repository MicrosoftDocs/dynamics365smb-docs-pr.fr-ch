---
title: Détails de conception - Équilibrage la demande et de l'approvisionnement | Microsoft Docs
description: Pour comprendre comment fonctionne le système de planification, il est nécessaire de comprendre les objectifs priorisés du système de planification, dont les plus importants sont de s'assurer que toute demande est satisfaite par suffisamment d'approvisionnement et n'importe quel approvisionnement atteint un but.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 30c78ba04d58a2e2c2227ec638724c85cb1236c7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917566"
---
# <a name="design-details-balancing-demand-and-supply"></a>Détails de conception : équilibrage de la demande et de l'approvisionnement
Pour comprendre comment fonctionne le système de planification, il est nécessaire de comprendre les objectifs priorisés du système de planification, dont les plus importants sont de s'assurer que :  

- La demande sera satisfaite par une offre suffisante.  
- Tout approvisionnement répond à une finalité.  

 En général, ces objectifs sont atteints en équilibrant l'approvisionnement avec la demande.  

## <a name="demand-and-supply"></a>Offre et demande
 Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication. En outre, l'application permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.  

  Approvisionnement est le terme courant utilisé pour désigner toute sorte de quantité positive ou d'entrée, telle qu'un stock, des achats, un assemblage, une production ou des transferts d'enlogement. De plus, un retour vente peut également représenter un approvisionnement.  

  Pour trier les nombreuses sources de demande et d'approvisionnement, le système de planification les organise sur deux chronologies appelées profils de stock. Un profil contient des événements de demande, ainsi l'autre contient les événements d'approvisionnement correspondants. Chaque événement représente une entité réseau de commande, par exemple une ligne commande vente, une écriture comptable article ou une ligne O.F.  

  Lorsque les profils de stock sont chargés, les différents ensembles demande-approvisionnement sont équilibrés pour produire un plan d'approvisionnement répondant aux objectifs répertoriés.  

  Les paramètres de planification et les niveaux de stock sont d'autres types de demande et d'approvisionnement respectivement, qui subissent un équilibrage intégré pour réapprovisionner les articles en stock. Pour plus d'informations, voir [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Le concept d'équilibrage en bref
  La demande est faite par les clients d'une société. L'approvisionnement est ce que la société peut créer et supprimer pour établir l'équilibre. Le système de planification commence avec la demande indépendante et effectue une traçabilité en amont jusqu'à l'approvisionnement.  

   Les profils de stock sont utilisés pour contenir des informations sur les demandes et les approvisionnements, les quantités et les délais. Ces profils constituent essentiellement les deux côtés de l'échelle de contrepartie.  

   L'objectif du mécanisme de planification est d'équilibrer la demande et l'approvisionnement d'un article pour s'assurer que l'approvisionnement correspond à la demande de manière faisable, telle qu'elle est définie par les paramètres et les règles de planification.  

   ![Vue d'ensemble de l'équilibrage de la demande et de l'approvisionnement](media/nav_app_supply_planning_2_balancing.png "Vue d'ensemble de l'équilibrage de la demande et de l'approvisionnement")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Traiter les commandes avant la date début de la planification
Pour éviter qu'un programme d'approvisionnement affiche des suggestions impossibles et donc inutiles, le système de planification considère la période jusqu'à la date de début de la planification comme une zone gelée pour laquelle rien n'est programmé. La règle suivante s'applique à la zone gelée :  

L'ensemble de l'offre et de la demande antérieur à la date de début de la période de planification sera considéré comme faisant partie du stock ou comme étant expédié.  

Par conséquent, le système de planification, à quelques exceptions près, ne va suggérer aucune modification des commandes approvisionnement de la zone gelée. Par ailleurs, aucun lien de chaînage n'est créé ou mis à jour pour cette période.  

Les exceptions à cette règle sont les suivantes :  

   * Si le stock disponible projeté, y compris la somme de la demande et de l'approvisionnement dans la zone gelée, est inférieur à zéro.  
   * Si les numéros de série/lot sont nécessaires sur la ou les commandes antidatées.  
   * Si l'ensemble demande-approvisionnement est lié par une stratégie ordre pour ordre.  

Si le stock disponible d'origine est inférieur à zéro, le système de planification suggère une commande approvisionnement d'urgence la veille de la période de planification pour couvrir la quantité manquante. Par conséquent, le stock disponible projeté est toujours au moins à zéro lorsque la planification de la période future commence. La ligne planning de cette commande approvisionnement affiche une icône d'avertissement Urgence et des informations supplémentaires sont fournies lors de la recherche.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Les numéros de série et/ou de lot et les liens ordre pour ordre sont exempts de la zone gelée  
   Si les numéros de série/lot sont requis ou si un lien ordre pour ordre existe, le système de planification ignore la zone gelée et incorpore ces quantités antidatées à partir de la date début et propose éventuellement des actions de correction si la demande et l'approvisionnement ne sont pas synchronisés. La raison commerciale de ce principe est que ces ensembles approvisionnement-demande spécifiques doivent correspondre pour garantir que cette demande spécifique soit satisfaite.

## <a name="loading-the-inventory-profiles"></a>Chargement des profils de stock
Pour trier les nombreuses sources de demande et d'approvisionnement, le système de planification les organise sur deux chronologies appelées profils de stock.  

Les types normaux de demande et d'approvisionnement dont les dates d'échéance correspondent ou sont ultérieures à la date du début de la planification sont chargés dans chaque profil de stock. Une fois chargés, les différents types de demande et d'approvisionnement sont triés en fonction des priorités générales, comme la date d'échéance, les codes bas niveau, le magasin et la variante. De plus, des priorités d'ordre s'appliquent aux différents types pour s'assurer que la demande la plus importante est satisfaite en premier. Pour en savoir plus, voir [Affecter une priorité aux commandes](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Comme indiqué précédemment, la demande peut également être négative. Cela signifie qu'il doit être traité comme approvisionnement ;, toutefois, contrairement aux types courants d'approvisionnement, la demande négative est considérée comme approvisionnement fixe. Le système de planification peut la prendre en compte, mais ne proposera en aucun cas de la modifier.  

Généralement le système de planification tient compte de toutes les commandes approvisionnement après la date de début de la planification comme susceptibles de changer pour répondre à une demande. Toutefois, dès qu'une quantité est validée à partir d'une commande approvisionnement, elle ne peut plus être modifiée par le système de planification. Par conséquent, les différents ordres suivants ne peuvent pas être replanifiés :  

- Ordres de fabrication lancés où la consommation ou la production a été validée.  
- Ordres d'assemblage où la consommation ou la production a été validée.  
- Transférez les ordres où l'expédition a été validée.  
- Commandes achat dans lesquelles la réception a été validée.  

Outre le chargement des types d'offre et de demande, certains types sont chargés en fonction de règles et de dépendances spéciales décrites ci-après.  

### <a name="item-dimensions-are-separated"></a>Les axes article sont distincts  
Le programme d'approvisionnement doit être calculé par combinaison des dimensions d'article, comme la variante et le magasin. Toutefois, il n'y a pas de raison de calculer des combinaisons théoriques. Seules ces combinaisons contenant une demande et/ou un approvisionnement doivent être calculées.  

Le système de planification contrôle cela en s'exécutant via le profil de stock. Lorsqu'une nouvelle combinaison est trouvée, l'application crée un enregistrement de contrôle interne qui contient les informations de combinaison réelles. L'application insère le point de stock comme enregistrement de contrôle, ou boucle externe. Par conséquent, les paramètres de planification appropriés en fonction d'une combinaison de variante et de magasin sont définis, et l'application peut passer à la boucle interne.  

> [!NOTE]  
>  L'application ne requiert pas que l'utilisateur saisisse un enregistrement de points de stock en entrant la demande et/ou l'approvisionnement pour une combinaison particulière de variante et de magasin. Par conséquent, si un point de stock n'existe pas pour une combinaison donnée, l'application crée son propre bilan de point de stock temporaire sur les données de fiche article. Si Magasin obligatoire a la valeur Oui sur la page Paramètres stock, un point de stock doit être créé ou Mag. composant par déf doit avoir la valeur Oui. Pour plus d'informations, voir [Détails de conception : demande à un magasin vide.](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Les numéros de série/lot sont chargés en fonction du niveau de détail  
Les attributs sous forme de numéros de série/lot sont chargés dans le profil de stock avec l'offre et la demande auxquels ils sont affectés.  

Les attributs de demande et d'approvisionnement sont réorganisés par priorité de commande ainsi que par leur niveau de spécification. Comme le numéro de série/lot reflète le niveau de la spécification, la demande plus spécifique, par exemple un numéro de lot sélectionné spécifiquement pour une ligne vente, recherche une correspondance avant une demande moins spécifique, par exemple une vente à partir de n'importe quel numéro de lot sélectionné.  

> [!NOTE]  
>  Il n'existe pas de règles de priorité dédiées pour les demandes et approvisionnements avec numéros de lot/série autres que le niveau de spécification défini leurs combinaisons numéro de série et de lot et les paramètres de suivi des articles associés.  

Lors de l'équilibrage, le système de planification considère un approvisionnement qui porte des numéros de série/lot comme non flexible et n'essaie pas d'augmenter ou de replanifier de telles commandes approvisionnement (à moins qu'elles ne soient utilisées dans une relation ordre pour ordre). Voir les liens ordre pour ordre ne sont jamais rompus). Cela évite que l'approvisionnement ne reçoive plusieurs messages d'action, possiblement contradictoires, lorsqu'un approvisionnement comporte des attributs divers, comme une collection de différents numéros de série.  

Il existe une autre raison pour laquelle un approvisionnement portant des numéros de série/lot est considéré comme non flexible. Dans la mesure où les numéros de série/lot sont généralement affectés très tard au cours du processus, cela représenterait une source de confusion si des modifications étaient proposées.  

L'équilibrage des numéros de série/lot ne tient pas compte de la *zone gelée* . Si la demande et l'approvisionnement ne sont pas synchronisés, le système de planification proposera des modifications ou suggère de nouvelles commandes, quelle que soit la date de début de la planification.  

### <a name="order-to-order-links-are-never-broken"></a>Les Liens ordre pour ordre ne sont jamais rompus  
Lors de la planification d'un article commande-à-commande, l'approvisionnement lié ne doit pas être utilisé pour toute demande autre que ce à quoi il était prévu à l'origine. La demande liée ne doit pas être couverte par un autre approvisionnement aléatoire, même si, dans sa situation actuelle, il est disponible en termes de délai et de quantité. Par exemple, un ordre d'assemblage lié à une commande vente dans un scénario assembler pour commande ne peut pas être utilisé pour couvrir l'autre demande.  

La demande et l'approvisionnement ordre pour ordre doivent être équilibrées exactement. Le système de planification assure l'approvisionnement en toutes circonstances sans tenir compte des paramètres de taille de commande, des modificateurs, ni des quantités dans le stock (autres que les quantités liées aux commandes). Pour le même motif, le système suggère de diminuer les approvisionnements excédentaires si la demande liée est réduite.  

Cet équilibre affecte également le temps. L'horizon limité accordé par l'intervalle de planification n'est pas pris en compte ; l'approvisionnement sera replanifié si le délai de la demande a été modifié. Cependant, le seuil sera respecté et empêchera que des approvisionnements ordre pour ordre soient planifiés en sortie, sauf pour les approvisionnements internes d'un O.F. multi-niveau (O.F. projet).  

> [!NOTE]  
>  Les numéros de série/lot peuvent également être spécifiés sur la demande ordre pour ordre. Dans ce cas, l'approvisionnement n'est pas considéré comme inflexible par défaut, comme c'est habituellement le cas pour les numéros de série/lot. Dans ce cas, le système augmentera/diminuera en fonction des modifications de la demande. En outre, si une demande contient différents numéros de série/lot, par exemple plusieurs numéros de lot, une commande approvisionnement est proposée par lot.  

> [!NOTE]  
>  Les prévisions ne doivent pas entraîner la création de commandes approvisionnement liées par un lien ordre pour ordre. Si la prévision est utilisée, elle doit être utilisée comme générateur d'une demande dépendante dans un environnement de fabrication.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Besoin composant est chargé en fonction des modifications d'ordre de fabrication  
Lors de la gestion des ordres de fabrication, le système de planification doit contrôler les composants nécessaires avant de les charger dans le profil de demande. Les lignes composant qui résultent d'un ordre de fabrication modifié remplaceront celles de la commande originale. Cela garantit que le système de planification fait en sorte que les lignes de planification pour les besoins de composant ne sont jamais dupliquées.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Le stock de sécurité peut être consommé  
Le stock de sécurité est surtout un type de demande et est donc chargé dans le profil de stock à la date de début de la planification.  

Le stock de sécurité est une quantité en stock mise de côté pour compenser les incertitudes de la demande pendant le délai de réapprovisionnement. Toutefois, il peut être consommé s'il s'avère nécessaire de l'utiliser pour répondre à une demande. Le système de planification assure dans ce cas le remplacement rapide du stock de sécurité en suggérant un ordre d'approvisionnement permettant le réapprovisionnement de la quantité du stock de sécurité à sa date de consommation. Cette ligne planning affiche une icône d'avertissement Exception qui indique au gestionnaire que le stock de sécurité est partiellement ou entièrement consommé via une commande d'exception de la quantité manquante.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>La demande de prévision est réduite par les commandes vente  
La prévision de la demande exprime une future demande anticipée. Lorsqu'une demande réelle est saisie, généralement comme commandes vente pour les articles produits, elle consomme la prévision.  

La prévision proprement dite n'est pas réellement réduite par les commandes vente ; elle reste la même. Cependant, les quantités prévues utilisées dans le calcul de planification sont réduites (par les quantités de commande vente) avant que la quantité restante, le cas échéant, soit saisie dans le profil du stock de demande. Lorsque le système de planification examine les vente réelles pendant une période, les commandes vente ouvertes et les écritures comptables article des ventes expédiées sont incluses, à moins que elles ne proviennent d'une commande ouverte.  

Un utilisateur doit définir une période de prévision valide. La date de la quantité prévue définit le début de la période, et la date de la prévision suivante définit la fin de la période.  

La prévision pour les périodes antérieures à la période de planification n'est pas utilisée, qu'elle soit consommée ou non. Le premier chiffre de prévision intéressant est la date même ou la date la plus proche précédant la date du début de la planification.  

La prévision peut être pour une demande indépendante, telle que des commandes vente, ou une demande dépendante, comme des composants O.F. (prévision module). Un article peut avoir deux types de prévision. Lors de la planification, la consommation a lieu séparément, d'abord pour une demande indépendante puis pour une demande dépendante.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>La demande de commande ouverte est réduite par les commandes vente  
Des prévisions sont renseignées par la commande ouverte vente comme moyen de spécifier une future demande pour un client spécifique. Comme pour la prévision (non spécifiée), les ventes réelles doivent consommer la demande prévue, et la quantité restante doit être entrée dans le profil du stock de demande. À nouveau, la consommation ne réduit pas réellement la commande ouverte.  

Le calcul de planification tient compte des commandes vente ouvertes liées à la ligne spécifique de la commande ouverte, mais ne tient compte d'aucune période valide. Il ne prend pas non plus en compte les commandes validées, étant donné que la procédure de validation a déjà réduit la quantité restante de commande ouverte.

## <a name="prioritizing-orders"></a>Hiérarchisation des commandes
Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée ; la demande du jour doit être traitée avant la demande de la semaine suivante. Mais en plus de cette priorité générale, le système de planification suggère également que le type de demande doit être rempli avant de répondre à une autre demande. De même, il suggère que la source d'approvisionnement soit lettrée avant d'appliquer d'autres sources d'approvisionnement. Ceci est effectué en fonction des priorités de la commande.  

La demande et l'approvisionnement chargés contribuent à un profil pour le stock prévisionnel en fonction des priorités suivantes :  

### <a name="priorities-on-the-demand-side"></a>Priorités du côté de la demande  
1. Déjà expédié : écriture comptable article  
2. Retour achat  
3. Ecriture réservation  
4. Commande service  
5. Besoin de composants de production  
6. Ligne d'ordre d'assemblage  
7. Commande désenlogement transfert  
8. Commande ouverte (qui n'a pas déjà été consommée par les commandes vente associées)  
9. Prévision (qui n'a pas déjà été consommée par d'autres commandes vente)  

> [!NOTE]  
>  Les retours achat ne sont généralement pas impliqués dans la planification d'approvisionnement ; ils doivent toujours être réservés à partir du lot qui va être retourné. S'il ne sont pas réservés, les retours achat jouent un rôle dans la disponibilité et sont classés en priorité élevée pour éviter que le système de planification suggère une commande approvisionnement uniquement pour servir un retour achat.  

### <a name="priorities-on-the-supply-side"></a>Priorités du côté de l'approvisionnement  
1. Déjà dans le stock : écriture comptable article (Flexibilité planification = Aucune)  
2. Retour vente (flexibilité de planification = aucune)  
3. Enlogement transfert  
4. Ordre de fabrication  
5. Ordre d'assemblage  
6. Commande achat  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorité liée à l'état de la demande et de l'approvisionnement  
Outre les priorités accordées par le type d'offre et de demande, l'état actuel des commandes dans le processus d'exécution définit également une priorité. Par exemple, les activités entrepôt ont un effet et le statut des commandes vente, des commandes achat, des ordres de transfert, des ordres d'assemblage et des ordres de fabrication est pris en compte :  

1. En partie géré (flexibilité de planification = Aucune)  
2. Déjà en cours de traitement dans l'entrepôt (Flexibilité planification = Aucune)  
3. Lancé - tous types de commande (flexibilité de planification = illimitée)  
4. Ordre de fabrication planifié ferme (flexibilité de planification = illimitée)  
5. Planifié/ouvert - tous types de commande (flexibilité de planification = illimitée)

## <a name="balancing-supply-with-demand"></a>Équilibrage de l'approvisionnement avec la demande
L'élément principal du système de planification implique l'équilibrage de l'approvisionnement et de la demande en proposant des actions utilisateur pour rectifier les commandes approvisionnement en cas de déséquilibre. Cela est opéré par combinaison de variante et magasin.  

Imaginez que chaque profil de stock contient une chaîne d'événements de demande (triés par date et par priorité) et une chaîne correspondante d'événements d'approvisionnement. Chaque événement fait référence à son type origine et à son identification. Les règles pour équilibrer l'article sont simples. Quatre exemples de correspondance entre demande et approvisionnement peuvent apparaître à tout moment dans le processus :  

1. Aucune demande ou offre n'existe pour l'article => la planification est terminée (ou ne doit pas démarrer).  
2. La demande existe mais il n'y a pas d'offre => une offre doit être proposée.  
3. L'offre existe mais il n'y a pas de demande correspondante => l'offre doit être annulée.  
4. L'offre et la demande existent => les questions doivent être posées et résolues pour que le système puisse garantir que la demande sera satisfaite et que l'offre est suffisante.  

    Si le délai de l'approvisionnement n'est pas approprié, l'approvisionnement peut être replanifié par exemple comme suit :  

    1.  Si l'approvisionnement est placé avant la demande, l'approvisionnement peut éventuellement être replanifié en sortie pour que le stock soit le plus bas possible.  
    2.  Si l'approvisionnement est placé après la demande, l'approvisionnement peut éventuellement être replanifié en entrée. Sinon, le système suggère un nouvel approvisionnement.  
    3.  Si l'approvisionnement satisfait la demande à la date, le système de planification peut continuer à chercher si la quantité de l'approvisionnement peut couvrir la demande.  

    Une fois que le délai est en place, la quantité appropriée à approvisionner peut être calculée comme suit :  

    1.  Si la quantité d'approvisionnement est inférieure à la demande, il est possible que la quantité d'approvisionnement puisse être augmentée (ou pas, si limitée par une stratégie de quantité maximum).  
    2.  Si la quantité d'approvisionnement est supérieure à la demande, il est possible que la quantité d'approvisionnement puisse être diminuée (ou pas, si limitée par une stratégie de quantité minimum).  

    A ce stade, l'une de ces deux situations existe :  

    1.  La demande actuelle peut être couverte, dans ce cas, elle peut être clôturée et la planification des demandes suivantes peut commencer.  
    2.  L'approvisionnement a atteint son maximum, en laissant une partie de la quantité de demande non couverte. Dans ce cas, le système de planification peut clôturer l'approvisionnement actif et passer au suivant.  

 La procédure recommence à la demande suivante et à l'approvisionnement actif ou vice versa. L'approvisionnement actif peut peut-être couvrir cette demande suivante également, ou la demande actuelle n'a pas encore été entièrement couverte.  

### <a name="rules-concerning-actions-for-supply-events"></a>Règles en ce qui concerne les actions pour les événements d'approvisionnement  
Lorsque le système de planification effectue un calcul hiérarchisé dans lequel l'approvisionnement doit répondre à la demande, la demande est considérée comme sûre, c'est-à-dire qu'elle se trouve en dehors du contrôle du système de planification. Cependant, le côté approvisionnement peut être géré. Par conséquent, le système de planification suggère de créer de nouvelles commandes approvisionnement, reprogrammant celles existantes et/ou modifiant la quantité de commande. Si une commande approvisionnement existante devient superflue, le système de planification suggère à l'utilisateur de l'annuler.  

Si l'utilisateur souhaite exclure une commande approvisionnement existante des propositions planning, il peut déclarer qu'il n'y a pas de flexibilité de planification (flexibilité de planification = Aucune). Ensuite, l'approvisionnement excédentaire à partir de cette commande est utilisé pour répondre à la demande, mais aucune action n'est suggérée.  

En général, tous les approvisionnements ont une flexibilité de planification qui est limitée par les conditions de chacune des mesures suggérées.  

-   **Replanifier en dehors**  : La date à partir d'une commande approvisionnement existante peut être planifiée en dehors pour satisfaire la date d'échéance de demande à moins que :  

    -   Il représente le stock (toujours au jour zéro).  
    -   Elle a un ordre pour ordre lié à une autre demande.  
    -   Il se trouve hors de la page de replanification définie avant l'intervalle de planification.  
    -   Il existe un approvisionnement plus proche qui peut être utilisé.  
    -   Par ailleurs, l'utilisateur peut choisir de ne pas replanifier pour les raisons suivantes :  
    -   La commande approvisionnement a déjà été liée à une autre demande à une date précédente.  
    -   La replanification nécessaire est si minime que l'utilisateur la trouve négligeable.  

-   **Replanifier dans**  : La date à partir d'une commande approvisionnement existante peut être replanifiée dans, sauf dans les conditions suivantes :  

    -   Elle est directement liée à une autre demande.  
    -   Il se trouve hors de la page de replanification définie avant l'intervalle de planification.  

> [!NOTE]  
>  Lors de la planification d'un article utilisant un point de commande, la commande approvisionnement peut toujours être planifiée si nécessaire. Ceci est courant dans les commandes approvisionnement planifiées déclenchées par un point de commande.  

-   **Augmenter la quantité**  : il est possible d'augmenter la quantité d'une commande approvisionnement existante pour répondre à la demande sauf si la commande approvisionnement est directement liée à une demande par un lien ordre pour ordre.  

> [!NOTE]  
>  Bien qu'il soit possible d'augmenter la commande approvisionnement, elle peut être limité en raison d'une quantité maximum commande définie par l'utilisateur.  

-   **Diminuer la quantité**  : une commande approvisionnement existante avec un excédent par rapport à la demande existante peut être diminuée pour répondre à la demande.  

> [!NOTE]  
>  Bien que la quantité puisse être diminuée, il peut y avoir encore des excédents par rapport à la demande en raison d'une quantité minimum commande définie ou d'une valeur Commandé par.  

-   **Annuler**  : comme un incident spécial de l'action de diminuer la quantité, la commande approvisionnement peut être annulée si elle a été diminuée à zéro.  
-   **Nouveau**  : si aucune commande approvisionnement n'existe déjà, ou si une existante ne peut pas être modifiée pour satisfaire la quantité nécessaire à la date d'échéance demandée, une nouvelle commande approvisionnement est suggérée.  

### <a name="determining-the-supply-quantity"></a>Déterminer la quantité d'approvisionnement  
Les paramètres de planification définis par l'utilisateur contrôlent la quantité suggérée de chaque commande approvisionnement.  

Lorsque le système de planification calcule la quantité d'une nouvelle commande approvisionnement ou la modification de quantité d'une commande existante, la quantité proposée n'est pas forcément identique à ce qui est vraiment demandé.  

Si un stock maximum ou une quantité de commande fixe sont sélectionnés, la quantité proposée peut être augmentée pour répondre à cette quantité fixe ou au stock maximum. Si une méthode de réapprovisionnement utilise un point de commande, la quantité peut être augmentée au moins pour répondre au point de commande.  

 La quantité proposée peut être modifiée dans cette séquence :  

1. Diminuer à la quantité maximum commande (le cas échéant).  
2. Jusqu'à la quantité de commande minimale.  
3. Jusqu'à répondre à la commande multiple la plus proche. (Si des paramètres sont erronés, cela peut enfreindre la quantité de commande maximale).  

### <a name="order-tracking-links-during-planning"></a>Liens de chaînage lors de la planification  
En ce qui concerne le chaînage lors de la planification, il est important de mentionner que le système de planification réarrange les liens de chaînage créés de façon dynamique pour les combinaisons de article/variante/magasin.  

Deux raisons expliquent cela :  

-   Le système de planification doit pouvoir justifier ses propositions ; que toute demande a été couverte, et qu'aucune commande approvisionnement n'est superflue.  
-   Les liens de chaînage créés de façon dynamique doivent être rééquilibrés régulièrement.  

Avec le temps, les liens de chaînage dynamiques deviennent déséquilibrés puisque le réseau de chaînage entier n'est pas réorganisé tant qu'un événement de demande ou d'approvisionnement n'est pas réellement clôturé.  

Avant d'équilibrer un approvisionnement par demande, l'application supprime les liens de chaînage existants. Puis au cours de la procédure de contrepartie, lorsqu'un événement de demande ou d'approvisionnement est clôturé, il crée de nouveaux liens de suivi de commande entre la demande et l'approvisionnement.  

> [!NOTE]  
>  Même si l'article n'est pas configuré pour le chaînage dynamique, le système planifié crée des liens de chaînage équilibrés comme expliqué ci-dessus.
## <a name="closing-demand-and-supply"></a>Clôture de l'offre et de la demande
Lorsque les procédures d'équilibre d'approvisionnement ont été réalisées, il existe trois situations de fin possibles :  

* La quantité et la date requises des événements de demande ont été respectées et leur planification peut être clôturée. L'événement d'approvisionnement est encore ouvert et peut couvrir la demande suivante, donc la procédure de contrepartie peut recommencer avec l'événement d'approvisionnement actif et la demande suivante.  
* La commande approvisionnement ne peut pas être modifiée pour couvrir l'ensemble de la demande. L'événement demande est encore ouvert, avec une certaine quantité non couverte qui peut être couverte par l'événement suivant d'approvisionnement. Ainsi, l'événement d'approvisionnement actuel est fermé, donc l'acte d'équilibrage peut recommencer avec la demande actuelle et l'événement d'approvisionnement suivant.  
* L'ensemble de la demande a été couvert ; il n'existe aucune demande suivante (ou il n'y a pas de demande du tout). S'il y a un approvisionnement excédentaire, il peut être diminué (ou annulé), puis être clôturé. Il est possible que des événements d'approvisionnement supplémentaires existent plus loin dans la chaîne, et ils doivent également être annulés.  

Enfin, le système de planification crée un lien de chaînage entre l'approvisionnement et la demande.  

### <a name="creating-the-planning-line-suggested-action"></a>Création de la ligne planning (action suggérée)  
Si une action quelconque (Nouveau, Changer qté, Replanifier, Replanifier et changer qté ou Annuler) est suggérée pour modifier la commande approvisionnement, le système de planification crée une ligne planning dans la feuille planning. En raison du chaînage, la ligne planification est créée non seulement lorsque l'événement d'approvisionnement est clôturé, mais également si l'événement de demande est clôturé, même si l'événement d'approvisionnement est encore ouvert et qu'il peut être soumis à des modifications supplémentaires lorsque l'événement de demande suivant est traité. Cela signifie qu'après sa création, la ligne de planification peut être modifiée à nouveau.  

Pour réduire l'accès aux bases de données lors du traitement des ordres de fabrication, la ligne de planification peut être maintenue dans trois niveaux, tout en visant à effectuer le niveau de maintenance le moins exigeant :  

* Créer uniquement la ligne planning avec la date d'échéance et la quantité actuelles mais sans gamme et composants.  
* Inclure la gamme : la gamme planifiée est présentée avec le calcul des dates et heures de début et de fin. Ceci est exigeant en termes d'accès aux bases de données. Pour déterminer les dates de fin et d'échéance, il peut être nécessaire de calculer ceci même si l'événement d'approvisionnement n'a pas été clôturé (dans le cas d'une planification en aval).  
* Inclure l'éclatement de la nomenclature : ceci peut attendre juste avant que l'événement approvisionnement soit clôturé.  

Cela conclut les descriptions de la manière dont la demande et l'approvisionnement sont chargés, priorisés et équilibrés par le système de planification. En association avec cette activité de planification des approvisionnements, le système doit veiller à ce que le niveau de stock requis de chaque article soit maintenu en fonction de ses méthodes de réapprovisionnement.

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
 [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
