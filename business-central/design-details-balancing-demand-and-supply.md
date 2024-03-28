---
title: "Détails de conception\_: équilibrage de la demande et de l’offre"
description: Cet article décrit comment hiérarchiser les objectifs en équilibrant l’offre et la demande.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a>Détails de conception : équilibrage de la demande et de l’offre

Pour comprendre le fonctionnement du système de planification, il est important de comprendre ses objectifs prioritaires :  

* La demande sera satisfaite par une offre suffisante.  
* Tout approvisionnement répond à une finalité.  

En général, ces objectifs sont atteints en équilibrant l’offre avec la demande.  

## <a name="supply-and-demand"></a>Offre et demande

Le terme *offre* fait référence à tout type de quantité positive ou entrante, telle que :

* Stock
* Achats
* Assemblage
* Fabrication
* Enlogements transfert
* Retours sur ventes  

Le terme *demande* fait référence à tout type de demande brute, telle que :

* Un article pour une commande vente
* Un composant pour un ordre de fabrication

[!INCLUDE [prod_short](includes/prod_short.md)] vous permet également d’utiliser d’autres types techniques de demande, tels que le stock négatif et les retours achat.

Pour trier les sources de demande et d’offre, le système de planification les organise sur deux chronologies appelées profils de stock. Un profil concerne les événements de demande, et l’autre concerne les événements d’approvisionnement correspondants. Chaque événement d’approvisionnement représente une entité sur une commande, par exemple :

* Une ligne de commande vente
* Une écriture comptable article
* Une ligne d’ordre de fabrication

Lorsque les profils de stock sont chargés, les ensembles demande-approvisionnement sont équilibrés pour produire un plan d’approvisionnement répondant aux objectifs répertoriés.

Les niveaux de stock et les paramètres de planification sont d’autres types d’offre et de demande. Ces types subissent un équilibrage intégré pour réapprovisionner les articles en stock. Pour plus d’informations, consultez [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Le concept d’équilibrage en bref

La demande vient de vos clients. L’approvisionnement est ce que vous créez et supprimez pour établir l’équilibre. Le système de planification commence avec la demande et effectue une traçabilité en amont jusqu’à l’approvisionnement.  

Les profils de stock contiennent des informations sur les demandes et les approvisionnements, les quantités et les délais. Ces profils constituent les deux côtés de l’échelle de contrepartie.  

L’objectif de la planification est d’équilibrer l’offre et demande d’un article pour s’assurer que l’approvisionnement correspond à la demande, telle qu’elle est définie par les paramètres et les règles de planification.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Vue d’ensemble de l’équilibrage de l’offre et demande.":::

## <a name="process-orders-before-the-planning-start-date"></a>Traiter les commandes avant la date de début de la planification

Pour éviter qu’un plan d’approvisionnement n’affiche des suggestions déraisonnables, le système de planification ne planifiera rien dans la période précédant la date de début de la planification. La règle suivante s’applique à cette période :

* L’ensemble de l’offre et de la demande antérieur à la date de début de la période de planification est considéré comme faisant partie du stock ou comme étant expédié.  

À quelques exceptions près, le système de planification ne suggérera aucune modification des commandes approvisionnement de la période, ni ne créera de liens de chaînage dynamique pour cette période. Les exceptions à cette règle sont les suivantes :  

* Le stock disponible projeté comme étant disponible, y compris la somme de l’offre et de la demande sur la période, est inférieur à zéro.  
* Les commandes antidatées nécessitent des numéros de série ou de lot.  
* L’ensemble offre-demande est lié par une stratégie ordre pour ordre. 

Si le stock disponible d’origine est inférieur à zéro, le système de planification suggère une commande approvisionnement d’urgence la veille de la période de planification pour couvrir la quantité manquante. Par conséquent, le stock disponible et projeté est toujours au moins à zéro lorsque la planification de la période future commence. La ligne planning de cette commande approvisionnement affiche une icône d’avertissement Urgence et fournit des informations supplémentaires.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Les numéros de série et de lot et les liens ordre pour ordre sont exempts de la période précédente.

Si des numéros de série ou de lot sont requis ou si un lien ordre pour ordre existe, le système de planification ne tient pas compte de la règle relative à la période précédente. Il inclura des quantités antidatées à partir de la date de début et pourrait suggérer des actions correctives si l’offre et la demande ne sont pas synchronisées. Ces ensembles demande-offre doivent correspondre pour s’assurer qu’une demande spécifique est satisfaite.

## <a name="load-inventory-profiles"></a>Charger les profils de stock

Pour trier les sources de demande et d’offre, le système de planification les organise sur deux chronologies appelées profils de stock.  

L’offre et la demande assorties de dates d’échéance correspondant ou ultérieures à la date du début de la planification sont chargées dans chaque profil de stock. Une fois chargés, les types d’offre et de demande sont triés en fonction de priorités générales, telles que :

* Date d’échéance
* Codes plus bas niveau
* Magasin
* Variante

Les priorités de commande sont appliquées aux différents types pour satisfaire la demande la plus importante en premier. Pour plus d’informations, voir [Hiérarchisation des commandes](design-details-balancing-demand-and-supply.md#prioritize-orders).  

La demande peut également être négative. Traitez la demande négative comme une offre. Cependant, contrairement à l’offre normale, la demande négative est considérée comme une offre fixe. Le système de planification peut la prendre en compte, mais ne proposera en aucun cas de la modifier.  

Généralement le système de planification tient compte de toutes les commandes approvisionnement après la date de début de la planification comme susceptibles de changer pour répondre à une demande. Toutefois, après qu’une quantité a été validée à partir d’une commande approvisionnement, le système de planification ne peut pas la changer. Les commandes suivantes ne peuvent pas être replanifiées :  

* Ordres de fabrication lancés où la consommation ou la production a été validée.  
* Ordres d’assemblage où la consommation ou la production a été validée.  
* Transférez les ordres où l’expédition a été validée.  
* Commandes achat dans lesquelles la réception a été validée.  

Outre le chargement des types d’offre et de demande, certains types sont chargés en fonction de règles et de dépendances spéciales. Les sections suivantes de cet article décrivent ces règles et dépendances.  

### <a name="item-dimensions-are-separated"></a>Les dimensions d’article sont distinctes

Le programme d’approvisionnement doit être calculé pour chaque combinaison des dimensions d’article, comme la variante et le magasin. Seules les combinaisons contenant une demande et/ou un approvisionnement doivent être calculées.  

Le système de planification recherche des combinaisons dans le profil d’inventaire. Lorsqu’il trouve une nouvelle combinaison, il crée un enregistrement de contrôle interne qui contient les informations sur la combinaison. Le système de planification insère alors le point de stock comme enregistrement de contrôle, ou boucle externe. Par conséquent, les paramètres de planification sont définis en fonction d’une combinaison de variante et de magasin, et le système peut passer à la boucle interne. 

> [!NOTE]  
> Vous n’avez pas besoin d’entrer un enregistrement de point de stock lorsque vous entrez une offre et/ou une demande pour une combinaison particulière de variante et d’emplacement. Par conséquent, si un point de stock n’existe pas pour une combinaison donnée, [!INCLUDE [prod_short](includes/prod_short.md)] crée un enregistrement provisoire de point de stock basé sur les données de l’article. Si le bouton à bascule **Emplacement obligatoire** est activé sur la **page Paramètres stock**, vous devez soit créer un point de stock, soit activer le bouton à bascule **Composants à l’emplacement**. Learn more at [Planification avec/sans magasin](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Les numéros de série et de lot sont chargés en fonction du niveau de détail

Les numéros de série et de lot sont chargés dans le profil de stock avec l’offre et la demande auxquels ils sont affectés.  

Les attributs d’offre et de demande sont réorganisés par priorité de commande et par niveau de spécification. Étant donné que les correspondances de numéros de série et de lot reflètent le niveau de spécification, une demande plus spécifique correspondra avant une demande moins spécifique. Par exemple, une demande spécifique peut être un numéro de lot spécifié pour une ligne de vente. Une demande moins spécifique peut être une vente provenant de n’importe quel numéro de lot.

> [!NOTE]  
> Les seules règles de priorité dédiées pour l’offre et la demande assorties de numéros de lot et de série sont le niveau de spécification défini par leurs combinaisons et la manière dont da traçabilité est configurée pour les articles.  

Lors de l’équilibrage, le système de planification considère l’offre assortie de numéros de série et de lot comme inflexible. Le système n’augmentera ni ne replanifiera ces commandes approvisionnement. La seule exception à cela est le cas où elles sont utilisées dans une relation ordre pour ordre Learn more at [Les Liens ordre pour ordre ne sont jamais rompus](#order-to-order-links-are-never-broken). Cette exception empêche l’approvisionnement de recevoir plusieurs messages d’action, éventuellement contradictoires, lorsque les attributs sont variables. Par exemple, des attributs variables peuvent survenir lorsque l’approvisionnement comporte un ensemble de numéros de série différents.  

Une autre raison pour laquelle l’approvisionnement à numéros de série et de lot n’est pas flexible est que les numéros de série et de lot sont souvent attribués tard dans le processus. Cela pourrait prêter à confusion si des changements sont suggérés à ce stade.  

L’équilibrage des numéros de série et de lot ne respecte pas la règle qui consiste à ne rien planifier avant la date de début de la planification. Si l’offre et la demande ne sont pas synchronisés, le système de planification proposera des modifications ou de nouvelles commandes, quelle que soit la date de début de la planification.  

### <a name="order-to-order-links-are-never-broken"></a>Les liens ordre pour ordre ne sont jamais rompus

Lors de la planification d’un article ordre pour ordre, l’approvisionnement lié ne doit être utilisé que pour ce à quoi il était prévu à l’origine. La demande liée ne doit être couverte par aucune autre offre, même si l’offre est disponible en temps et en quantité. Par exemple, vous ne pouvez pas utiliser un ordre d’assemblage lié à une commande vente dans un scénario Assembler pour commande pour couvrir une autre demande.  

L’offre et la demande ordre pour ordre doivent être équilibrées exactement. Le système de planification assure l’approvisionnement sans tenir compte des paramètres de taille de commande, des modificateurs, ni des quantités en stock (autres que les quantités liées aux commandes). Pour le même motif, le système suggère de diminuer les approvisionnements excédentaires si la demande liée est réduite.  

Cet équilibre affecte également le temps. L’horizon limité accordé par l’intervalle de planification n’est pas pris en compte ; l’approvisionnement sera replanifié si le délai de la demande a été modifié. Cependant, le seuil sera respecté et empêchera que des approvisionnements ordre pour ordre soient planifiés en sortie, sauf pour les approvisionnements internes d’un O.F. multi-niveau (O.F. projet).  

> [!NOTE]  
> Les numéros de série et de lot peuvent également être spécifiés sur la demande ordre pour ordre. Dans ce cas, l’offre n’est pas inflexible, ce qui est normalement le cas pour les numéros de série et de lot. Dans ce cas, le système augmentera ou diminuera en fonction des modifications de la demande. Si une demande comporte différents numéros de série et de lot, par exemple plusieurs numéros de lot, une commande approvisionnement est proposée pour chaque lot.  

> [!NOTE]  
> Les prévisions ne doivent pas entraîner la création de commandes approvisionnement liées par un lien ordre pour ordre. Si la prévision est utilisée, elle doit être utilisée comme générateur d’une demande dépendante dans un environnement de fabrication.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Le besoin composant est chargé en fonction des modifications d’ordre de fabrication

Lors de la gestion des ordres de fabrication, le système de planification doit contrôler les composants nécessaires avant de les charger dans le profil de demande. Les lignes composant qui résultent d’un ordre de fabrication modifié remplaceront les lignes de la commande originale. La modification garantit que le système de planification ne duplique pas les lignes planning pour un besoin de composant.  

### <a name="consume-safety-stock"></a>Consommer le stock de sécurité

Le stock de sécurité est une demande qui est chargée dans le profil de stock à la date de début de la planification.  

Le stock de sécurité est une quantité en stock mise de côté pour compenser les incertitudes de la demande pendant le réapprovisionnement. Cependant, il peut être consommé pour répondre à une demande. Dans ce cas, le système de planification veillera à ce que le stock de sécurité soit rapidement remplacé. Le système propose une commande approvisionnement pour réapprovisionner la quantité du stock de sécurité à la date à laquelle elle est consommée. La ligne planning affiche une icône d’avertissement Exception qui indique que le stock de sécurité est partiellement ou entièrement consommé via une commande d’exception de la quantité manquante.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>La prévision de demande est réduite par les commandes vente

les prévisions de demande expriment une future demande anticipée. Lorsqu’une demande réelle est saisie, généralement comme commandes vente pour les articles produits, elle consomme la prévision.

La prévision elle-même n’est pas réduite par les commandes vente. Cependant, les quantités prévues utilisées dans le calcul de planification sont réduites par les quantités de commande vente avant que la quantité restante, le cas échéant, ne soit saisie dans le profil de demande. Pour les ventes au cours d’une période, la planification inclut à la fois les commandes vente en cours et les écritures comptables article des ventes expédiées. L’exception à cette règle est lorsqu’elles proviennent d’une commande cadre.  

Vous devez définir une période de prévision valide. La date de la quantité prévue définit le début de la période, et la date de la prévision suivante définit la fin de la période.  

La prévision pour les périodes antérieures à la période de planification n’est pas utilisée, qu’elle soit consommée ou non. Le premier chiffre de prévision intéressant est la date de début de la planification, ou la date la plus proche.  

La prévision peut concerner différents types de demande :

* Demande indépendante, telle que les commandes vente
* Demande dépendante, telle que des composants d’ordre de fabrication.

Un article peut avoir deux types de prévision. Lors de la planification, la consommation a lieu séparément, d’abord pour une demande indépendante puis pour une demande dépendante.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>La demande de commande cadre est réduite par les commandes vente

Des prévisions sont renseignées par les commandes cadres vente comme moyen de spécifier une future demande pour un client spécifique. Comme pour la prévision (non spécifiée), les ventes réelles doivent consommer la demande prévue, et la quantité restante doit être entrée dans le profil du stock de demande. La consommation ne réduit pas la quantité de la commande cadre.

Le calcul de planification tient compte des commandes vente ouvertes liées à la ligne spécifique de la commande cadre, mais ne comprend aucune période valide. Elle ne prend pas non plus en compte les commandes validées, parce que la procédure de validation a déjà réduit la quantité restante de la commande cadre.

## <a name="prioritize-orders"></a>Hiérarchisation des commandes

Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée. La demande d’aujourd’hui devrait être traitée avant la demande de la semaine prochaine. Mais, en plus de cette priorité globale, le système de planification fera les suggestions suivantes en fonction des priorités d’ordre :

* Quel type de demande vous devez satisfaire en premier.
* Quelle source d’approvisionnement soit lettrée avant d’appliquer d’autres sources d’approvisionnement.  

L’offre et la demande chargées contribuent à un profil pour le stock prévisionnel en fonction des priorités.  

### <a name="priorities-on-the-demand-side"></a>Priorités du côté de la demande

1. Déjà expédié : écriture comptable article  
2. Retour commande achat  
3. Commande vente  
4. Commande service  
5. Besoins de composants de production  
6. Ligne ordre d’assemblage  
7. Commande désenlogement transfert  
8. Commande cadre (qui n’a pas déjà été consommée par les commandes vente associées)  
9. Prévision (qui n’a pas déjà été consommée par d’autres commandes vente)  

> [!NOTE]  
> Les retours achat ne sont généralement pas impliqués dans la planification d’approvisionnement ; ils doivent toujours être réservés à partir du lot qui va être retourné. S’il ne sont pas réservés, les retours achat jouent un rôle dans la disponibilité et sont classés en priorité élevée pour éviter que le système de planification ne suggère une commande approvisionnement uniquement pour servir un retour achat.  

### <a name="priorities-on-the-supply-side"></a>Priorités du côté de l’approvisionnement

1. Déjà dans le stock : écriture comptable article (Flexibilité planification = Aucune)  
2. Retour vente (flexibilité de planification = aucune)  
3. Enlogement transfert  
4. Ordre de fabrication  
5. Ordre d’assemblage  
6. Commande achat  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a>Priorité liée à l’état de l’offre et de la demande

En plus des priorités du type d’offre et de demande, il y a d’autres choses qui affectent la flexibilité de la planification. Par exemple, les activités de l’entrepôt et le statut des commandes suivantes :

* Vente
* Achats
* Transfert
* Assemblage
* Fabrication

Le statut de ces commandes a les effets suivants : 

1. En partie géré (flexibilité de planification = Aucune)  
2. Déjà en cours de traitement dans l’entrepôt (Flexibilité planification = Aucune)  
3. Lancé - tous types de commande (flexibilité de planification = illimitée)  
4. Ordre de fabrication planifié ferme (flexibilité de planification = illimitée)  
5. Planifié/ouvert - tous types de commande (flexibilité de planification = illimitée)

## <a name="balancing-supply-with-demand"></a>Équilibrage de l’offre et de la demande

Le système de planification équilibre l’offre et la demande en suggérant des actions pour réviser les commandes approvisionnement qui ne sont pas équilibrées. Cet équilibre se produit pour chaque combinaison de variante et d’emplacement.  

Imaginons que chaque profil de stock contienne deux chaînes :

* Une chaîne d’événements de demande, triés par date et priorité
* Une chaîne correspondante d’événements d’approvisionnement

Chaque événement fait référence à son type origine et à son identification. Les règles pour équilibrer l’article sont simples. L’adéquation de l’offre et de la demande peut se produire à n’importe quel moment du processus, comme suit :  

1. Aucune demande ou offre n’existe pour l’article => la planification est terminée (ou ne doit pas démarrer).  
2. La demande existe mais il n’y a pas d’offre => une offre doit être proposée.  
3. L’offre existe mais il n’y a pas de demande correspondante => l’offre doit être annulée.  
4. L’offre et la demande existent => des questions doivent être posées et recevoir une réponse avant que [!INCLUDE [prod_short](includes/prod_short.md)] ne puisse assurer que l’offre peut répondre à la demande.

    Si le délai de l’approvisionnement n’est pas approprié, l’approvisionnement peut être replanifié, comme suit :  

    1. Si l’approvisionnement est placé avant la demande, l’approvisionnement peut éventuellement être planifié de sorte que le stock soit le plus bas possible.  
    2. Si l’approvisionnement est placé après la demande, l’approvisionnement peut éventuellement être planifié en aval. Sinon, le système suggère un nouvel approvisionnement.  
    3. Si l’approvisionnement satisfait la demande à la date, le système de planification peut chercher si la quantité de l’approvisionnement peut couvrir la demande.  

    Une fois que le délai est en place, la quantité à approvisionner peut être calculée comme suit :  

    1. Si la quantité d’approvisionnement est inférieure à la demande, la quantité d’approvisionnement peut être augmentée (ou pas, si limitée par une stratégie de quantité maximum).  
    2. Si la quantité d’approvisionnement est supérieure à la demande, la quantité d’approvisionnement peut être diminuée (ou pas, si limitée par une stratégie de quantité minimum).  

    A ce stade, l’une de ces deux situations existe :  

    1. La demande actuelle peut être couverte, dans ce cas, elle peut être clôturée et la planification des demandes suivantes peut commencer.  
    2. L’approvisionnement a atteint son maximum, en laissant une partie de la quantité de demande non couverte. Dans ce cas, le système de planification peut clôturer l’approvisionnement actif et passer au suivant.  

 La procédure recommence à la demande suivante et à l’approvisionnement actif ou vice versa. L’approvisionnement actif peut peut-être couvrir cette demande suivante également, ou la demande actuelle n’a pas encore été entièrement couverte.  

### <a name="rules-for-actions-for-supply-events"></a>Règles concernant les actions pour les événements d’approvisionnement

Pour les calculs descendants dans lesquels l’offre doit répondre à la demande, la demande est considérée comme une donnée. Elle échappe au contrôle du système de planification. Cependant, le système de planification peut gérer le côté approvisionnement et fera les suggestions suivantes :

* Créer de nouvelles commandes approvisionnement
* Reprogrammer des commandes existantes ou modifier leurs quantités
* Annuler les commandes approvisionnement qui ne sont plus nécessaires  

Pour exclure une commande approvisionnement des propositions de la planification, vous pouvez déclarer qu’il n’y a pas de flexibilité de planification (flexibilité de planification = Aucune). Ensuite, l’approvisionnement excédentaire à partir de cette commande est utilisé pour répondre à la demande, mais aucune action n’est suggérée. 

En général, tous les approvisionnements ont une flexibilité de planification qui est limitée par les conditions de chacune des actions suggérées.  

* **Replanifier en dehors** : La date à partir d’une commande approvisionnement existante peut être planifiée en dehors pour satisfaire la date d’échéance de demande à moins que :

  * Il représente le stock (toujours au jour zéro).  
  * Elle a un ordre pour ordre lié à une autre demande.  
  * Il est en dehors de la fenêtre de reprogrammation dans l’intervalle de planification.
  * Il existe un approvisionnement plus proche qui peut être utilisé.  
  * Par ailleurs, l’utilisateur peut choisir de ne pas replanifier pour les raisons suivantes :
  * La commande approvisionnement est liée à une autre demande à une date précédente.  
  * La nouvelle planification nécessaire est si minime qu’elle est négligeable.  

* **Replanifier dans** : la date d’une commande approvisionnement existante peut être replanifiée dans, sauf dans les conditions suivantes :

  * Elle est directement liée à une autre demande.  
  * Elle est en dehors de la fenêtre de reprogrammation définie par l’intervalle de planification.

> [!NOTE]  
> Lors de la planification d’un article à l’aide d’un point de commande, vous pouvez replanifier la commande approvisionnement. Cela se produit souvent dans les commandes approvisionnement en aval déclenchées par un point de commande.

* **Augmenter la quantité** : il est possible d’augmenter la quantité d’une commande approvisionnement existante pour répondre à la demande sauf si la commande approvisionnement est directement liée à une demande par un lien ordre pour ordre.  

> [!NOTE]  
> Bien que vous puissiez augmenter la commande approvisionnement, l’augmentation peut être limitée en raison d’une quantité de commande maximale définie.  

* **Diminuer la quantité** : une commande approvisionnement existante avec un excédent par rapport à la demande existante peut être diminuée pour répondre à la demande.  

> [!NOTE]  
> Bien que la quantité puisse être diminuée, il peut y avoir des excédents par rapport à la demande en raison d’une quantité de commande ou d’un multiple de commande minimum défini. 

* **Annuler** : comme un incident spécial de l’action de diminuer la quantité, la commande approvisionnement peut être annulée si elle a été diminuée à zéro. 
* **Nouveau** : si aucune commande approvisionnement n’existe déjà, ou si une commande existante ne peut pas être modifiée pour satisfaire la quantité nécessaire à la date d’échéance de la demande, une nouvelle commande approvisionnement est suggérée.  

### <a name="determine-the-supply-quantity"></a>Déterminer la quantité d’approvisionnement

Vous définissez les paramètres de planification qui contrôlent la quantité suggérée de chaque commande approvisionnement.  

Lorsque le système de planification calcule la quantité d’une nouvelle commande approvisionnement ou la modification de quantité d’une commande existante, la quantité proposée peut différer de la demande réelle.  

Si un stock maximum ou une quantité de commande fixe sont sélectionnés, la quantité proposée peut être augmentée pour répondre à cette quantité fixe ou au stock maximum. Si une méthode de réapprovisionnement utilise un point de commande, la quantité peut être augmentée au moins pour répondre au point de commande. 

La quantité proposée peut être modifiée selon cette séquence :  

1. Diminuer jusqu’à la quantité de commande maximale.  
2. Augmenter jusqu’à la quantité de commande minimale.  
3. Augmenter jusqu’à répondre à la commande multiple la plus proche.

### <a name="order-tracking-links-during-planning"></a>Liens de chaînage dynamique lors de la planification

Pour le chaînage dynamique pendant la planification, le système de planification réorganise les liens de chaînage dynamique pour les combinaisons d’articles, de variantes et d’emplacements. Le système réorganise les liens de chaînage dynamique pour les raisons suivantes :

* Pour vérifier si ses suggestions couvrent toute la demande et s’assurer que toutes les commandes approvisionnement sont nécessaires.  
* Les liens de chaînage dynamique doivent être rééquilibrés régulièrement.  

Au fil du temps, les liens de chaînage dynamique deviennent déséquilibrés. Les liens sont déséquilibrés car le réseau de chaînage dynamique n’est pas réorganisé tant qu’un événement d’offre ou de demande n’est pas clôturé.

Avant d’équilibrer l’offre par la demande, le système de planification supprime les liens de chaînage existants. Au cours de la procédure d’équilibrage, lorsqu’un événement de demande ou d’offre est clôturé, il crée de nouveaux liens de chaînage dynamique entre l’offre et la demande.  

> [!NOTE]  
> Même si l’article n’est pas configuré pour le chaînage dynamique, le système de planification crée des liens de chaînage équilibrés.

## <a name="close-balanced-supply-and-demand"></a>Offre et demande proches de l’équilibre

L’équilibrage de l’offre a trois résultats possibles :

* La quantité et la date requises des événements de demande sont respectées et leur planification peut être clôturée. L’événement d’approvisionnement reste ouvert et pourrait être en mesure de couvrir la prochaine demande. Le maintien de l’événement d’approvisionnement ouvert permet à la procédure d’équilibrage de recommencer avec l’événement d’approvisionnement en cours et la demande suivante.  
* La commande approvisionnement ne peut pas être modifiée pour couvrir l’ensemble de la demande. L’événement de demande est encore ouvert, avec une quantité non couverte qui peut être couverte par l’événement suivant d’approvisionnement. Ainsi, l’événement d’approvisionnement actuel est fermé, et l’équilibrage peut recommencer avec la demande actuelle et l’événement d’approvisionnement suivant.  
* Toute la demande est couverte et il n’y a pas de demande suivante (ou il n’y a pas eu de demande du tout). L’offre excédentaire peut être réduite (ou annulée) puis fermée. Tout autre événement d’approvisionnement doit également être annulé.  

Enfin, le système de planification crée un lien de chaînage entre l’approvisionnement et la demande.  

### <a name="create-the-planning-line-suggested-action"></a>Création de la ligne planning (action suggérée)

Si une action quelconque **Nouveau**, **Changer qté**, **Replanifier**, **Replanifier et changer qté** ou **Annuler** est suggérée pour modifier la commande approvisionnement, le système de planification crée une ligne planning dans la feuille planning. Pour le chaînage dynamique, la ligne planning est créée non seulement lorsque l’événement d’approvisionnement est clôturé, mais également si l’événement de demande est clôturé. Cela est vrai même si l’événement d’approvisionnement est toujours ouvert et peut être modifié lors du traitement de l’événement de demande suivant. La ligne planning peut être à nouveau modifiée lors de sa création.

Pour réduire la charge sur la base de données lors du traitement des ordres de fabrication, la ligne planning peut être gérée sur trois niveaux :

* Créer uniquement la ligne planning avec la date d’échéance et la quantité actuelles mais sans gamme et composants.  
* Inclure la gamme : la gamme planifiée inclut le calcul des dates et heures de début et de fin. « Inclure la gamme » est exigeant en termes d’accès aux bases de données. Pour déterminer les dates de fin et d’échéance, il peut être nécessaire de calculer la gamme même si l’événement d’approvisionnement n’a pas été clôturé. Par exemple, si vous effectuez une planification en aval.  
* Inclure l’éclatement de la nomenclature : ceci se produit juste avant que l’événement approvisionnement ne soit clôturé.

## <a name="see-also"></a>Voir aussi

[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)  
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
