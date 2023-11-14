---
title: "Détails de conception\_: concepts centraux du système de planification"
description: La planification suggère des actions possibles pour l’utilisateur en fonction de la situation de l’offre/de la demande et des paramètres de planification des articles.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Détails de conception : concepts centraux du système de planification

Les fonctions de planification se trouvent dans un traitement par lots qui sélectionne d’abord les articles appropriés et la période à planifier. Ensuite, selon le code plus bas niveau de chaque article (sa position dans la nomenclature), le traitement par lots appelle une unité de code qui calcule un plan d’approvisionnement. L’unité de code équilibre les ensembles offre-demande et suggère des actions à l’utilisateur. Les mesures suggérées apparaissent sous forme de lignes dans la feuille planning ou dans la demande achat.  

![Contenu de la page Feuilles planning.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Contenu de la page Feuilles planning")  

Le gestionnaire d’une société, par exemple un acheteur ou un gestionnaire de production, est censé être l’utilisateur du système de planification. Le système de planification aide l’utilisateur en effectuant les calculs étendus mais relativement simples d’une planification. L’utilisateur peut alors se consacrer à résoudre les problèmes plus difficiles, par exemple lorsque les choses diffèrent de la normale.  

Le système de planification est guidé par la demande prévue et réelle des clients, par exemple, les commandes de prévisions et de vente. Les calculs de planification suggèrent des actions que vous pouvez entreprendre concernant l’approvisionnement auprès des fournisseurs, l’assemblage ou la production, ou les transferts depuis d’autres entrepôts. Une action suggérée peut être, par exemple, de créer de nouvelles commandes approvisionnement, comme des ordres d’achat ou de fabrication. S’il y a déjà des commandes approvisionnement, les mesures suggérées peuvent être d’augmenter ou d’accélérer les commandes pour répondre à l’évolution de la demande.  

Un autre objectif du système de planification est de garantir que le stock ne croisse pas inutilement. En cas de baisse de la demande, le système de planification suggère à l’utilisateur de reporter, de réduire ou d’annuler des commandes approvisionnement existantes.  

Une unité de code contient la logique de planification et les fonctions suivantes :

* MRP et PDP
* Calculer planning par écart
* Calculer planning régénératif

Cependant, le calcul du programme d’approvisionnement implique différents sous-systèmes.  

Le système de planification ne comprend aucune logique dédiée pour le nivellement de la capacité ou la planification précise. Ces types de travail de planification sont effectués séparément. Le manque d’intégration directe entre les deux domaines signifie également que des changements substantiels de capacité ou de planification obligeront à exécuter de nouveau la planification.  

## Paramètres de planification

Les paramètres de planification que vous définissez pour un article ou un groupe d’articles contrôlent les actions que le système de planification va proposer dans différentes situations. Définissez des paramètres de planification pour chaque article pour contrôler quand, combien et comment réapprovisionner.  

Vous pouvez également définir des paramètres de planification pour toute combinaison d’article, de variante et de magasin en définissant un point de stock pour chaque combinaison nécessaire, puis en spécifiant différents paramètres. Découvrez plus d’informations dans les sections [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) et [Détails de conception : paramètres de planification](design-details-planning-parameters.md).  

## Date début de la planification

Le système de planification vous aide à éviter d’avoir des commandes ouvertes dans le passé et des actions suggérées qui ne sont pas possibles. La planification traite toutes les dates précédant la date de début comme une zone gelée. La règle suivante s’applique à la zone gelée :  

* L’ensemble de l’offre et de la demande antérieur à la date de début de la période de planification est considéré comme faisant partie du stock ou comme étant expédié. En d’autres termes, il est supposé que la planification pour le passé s’exécute conformément au planning donné. Pour en savoir plus, consultez [Traiter les commandes avant la date de début de la planification](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Chaînage dynamique (Origine des besoins)

Le chaînage dynamique et sa création simultanée de messages d’action dans la feuille planning ne font pas partie du système de planification des approvisionnements. Lorsqu’une demande ou une offre est créée ou modifiée, le chaînage dynamique des commandes relie la demande et les quantités à couvrir en temps réel.  

Par exemple, si vous saisissez ou modifiez une commande client, le chaînage dynamique des commandes recherche instantanément l’offre pour couvrir la demande. L’approvisionnement peut provenir du stock ou d’une commande approvisionnement prévue (telle qu’une commande achat ou un ordre de fabrication). Lorsqu’il trouve une source d’approvisionnement, [!INCLUDE [prod_short](includes/prod_short.md)] fait le lien entre la demande et l’offre. Vous accédez au lien sur des pages en lecture seule à partir des lignes de document. Lorsque l’approvisionnement est introuvable, le système de chaînage dynamique des commandes crée des messages d’action dans la feuille de planification avec des suggestions de plan d’approvisionnement.  

Le chaînage dynamique des commandes vous aide à évaluer si vous acceptez les suggestions de commande approvisionnement. Du côté de l’offre, il montre la demande qui a créé l’offre. Du côté de la demande, il identifie l’offre qui devrait couvrir la demande.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Exemple de chaînage dynamique.":::

Pour plus d’informations, consultez [Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md).  

Dans les sociétés avec un faible flux d’articles et des structures de produits moins avancées, il peut être suffisant d’utiliser le chaînage dynamique pour la planification de l’approvisionnement. Toutefois, dans des environnements où l’activité est plus intense, le système de planification doit être utilisé pour assurer un planning d’approvisionnement correctement équilibré.  

### Comparaison entre le chaînage dynamique et le système de planification

Il peut être difficile de faire la différence entre le système de planification et le chaînage dynamique. Les deux fonctions affichent une sortie dans la feuille planning en suggérant les actions que le gestionnaire doit entreprendre. Toutefois, la manière dont cette production est produite diffère.  

Le système de planification traite l’ensemble du schéma d’offre et de demande d’un article. Il prend en compte tous les niveaux de la hiérarchie de la nomenclature en même temps que la chronologie. Le chaînage dynamique ne traite que la situation de la commande qui l’a activé. Lors de l’équilibrage de la demande et de l’offre, le système de planification crée des liens dans un mode de traitement par lots activé par l’utilisateur. Le chaînage dynamique crée les liens automatiquement lorsque vous saisissez une demande ou une offre. Par exemple, lorsque vous créez une commande client ou une commande fournisseur.  

Le chaînage dynamique crée des liens entre la demande et l’offre sur la base du principe premier arrivé, premier servi au moment de la saisie des données. Cette base peut conduire à du désordre dans les priorités. Par exemple, une commande client saisie en premier avec une date d’échéance le mois prochain peut être liée à de l’offre en stock. La commande client suivante, due demain, peut entraîner qu’un message d’action crée une nouvelle commande fournisseur pour la couvrir. L’image suivante illustre ce scénario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Exemple de chaînage dans la planification de l’approvisionnement 1.":::

Le système de planification traite la demande et l’offre des articles selon un ordre de priorité. La commande est priorisée en fonction des dates d’échéance et des types de commande. C’est-à-dire selon le principe du premier nécessaire, premier servi. Il supprime les liens de chaînage dynamique qui ont été créés de façon dynamique et les rétablit en fonction de la priorité de la date d’échéance. Lorsque le système de planification a été exécuté, il a résolu tous les déséquilibres entre la demande et l’approvisionnement, comme illustré ci-dessous pour les mêmes données.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Exemple de chaînage dans la planification de l’approvisionnement 2.":::  

Après avoir exécuté la planification, la table Écriture message d’action ne contient aucun message d’action. Ces messages sont remplacés par les actions suggérées dans la feuille planning. Pour en savoir plus, consultez [Liens de chaînage lors de la planification](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## Séquence et priorité de la planification

La séquence des calculs dans votre planification est importante pour que le travail soit fait dans un délai raisonnable. La gestion des priorités des besoins et ressources joue également un rôle important pour obtenir les meilleurs résultats.  

Le système de planification est axé sur les demandes. Les articles de haut niveau doivent être planifiés avant les articles de bas niveau, car ils peuvent générer une demande pour des articles de niveau inférieur. Par exemple, planifiez les sites de vente au détail avant les centres de distribution, car un site de vente au détail peut inclure une demande du centre de distribution. À un niveau d’équilibrage détaillé, si une commande d’approvisionnement lancée peut couvrir une commande client, le système ne doit pas créer de nouvelle commande d’approvisionnement. Un approvisionnement portant un numéro de lot spécifique ne doit pas être affecté pour couvrir une demande générique si une autre demande requiert ce lot spécifique.  

### Priorité d’article / Code plus bas niveau

Dans un environnement de fabrication, la demande d’un article fini et pouvant être vendu a pour résultat une demande dérivée pour les composants qui constituent l’article fini. La structure de nomenclature contrôle la structure des composants et peut couvrir plusieurs niveaux d’articles semi-finis. La planification d’un article va créer une demande dérivée pour des composants au niveau suivant. Cette hiérarchie peut finalement entraîner une demande dérivée pour les articles achetés. Le système de planification planifie les articles dans l’ordre de leur classement dans la hiérarchie de nomenclature totale. Le système commence par les articles vendables finis au niveau supérieur et descend la structure du produit jusqu’aux articles de niveau inférieur (selon le code de niveau inférieur).  

L’image suivante montre la séquence dans laquelle [!INCLUDE [prod_short](includes/prod_short.md)] suggère des commandes approvisionnement au niveau supérieur. Il suppose que les suggestions ont été acceptées et affiche également les articles de niveau inférieur.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planification des nomenclatures.":::

Pour en savoir plus sur les considérations de fabrication, accédez à [Charger les profils d’inventaire](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Optimisation des performances pour les calculs de plus bas niveau

Les calculs de code plus bas niveau peuvent affecter les performances du système. Pour atténuer cet effet, vous pouvez désactiver le bouton à bascule **Calcul de code plus bas niveau dynamique** sur la page **Configuration de la fabrication**. Quand vous le faites, [!INCLUDE[prod_short](includes/prod_short.md)] vous suggère de créer une entrée de file d’attente de tâches récurrente pour mettre à jour quotidiennement les codes plus bas niveau. Vous pouvez vous assurer que la tâche s’exécutera en dehors des heures de travail en spécifiant une heure de début dans le champ **Date/heure de début au plus tôt**.

Vous pouvez également accélérer les calculs de code plus bas niveau en activant le bouton à bascule **Optimiser le calcul du code plus bas niveau** sur la page **Configuration de la fabrication**.

> [!IMPORTANT]
> Si vous choisissez d’optimiser les performances, [!INCLUDE[prod_short](includes/prod_short.md)] utilise de nouvelles méthodes de calcul pour déterminer les codes plus bas niveau. Si vous disposez d’une extension qui repose sur les événements utilisés par les anciens calculs, l’extension peut cesser de fonctionner.

### Magasins/priorité de niveau transfert

Les sociétés possédant plus d’un site peuvent être amenées à planifier chaque magasin individuellement. Par exemple, le niveau de stock de sécurité d’un article et sa méthode de réapprovisionnement peuvent différer d’un magasin à un autre. Vous devez spécifier les paramètres de planification par article et par site.  

Vous pouvez utiliser des points de stock pour spécifier des paramètres de planification individuels. Un point de stock peut être considéré comme un article dans un magasin spécifique. Si vous n’avez pas défini de point de stock pour cet emplacement, [!INCLUDE [prod_short](includes/prod_short.md)] utilisera les paramètres définis sur la fiche article. [!INCLUDE [prod_short](includes/prod_short.md)] calcule un plan pour les emplacements actifs uniquement, là où il existe une demande ou une offre pour un article donné.  

N’importe quel article peut être manipulé à n’importe quel emplacement, mais [!INCLUDE [prod_short](includes/prod_short.md)] a une approche stricte du concept d’emplacements. Par exemple, une commande vente d’un article dans un magasin ne peut pas être satisfaite par le stock d’un un autre magasin. La quantité en stock doit d’abord être transférée au magasin spécifié sur la commande vente.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planification pour points de stock.":::

Pour plus d’informations, voir [Détails de conception : transferts de planification](design-details-transfers-in-planning.md).  

### Priorité de commande

Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée ; la demande du jour doit être traitée avant la demande des jours suivants. Mais en plus de ce type de priorité, les différents types de demande et d’offre doivent être triés en fonction de l’importance commerciale pour choisir quelle demande doit être satisfaite en premier. Du côté de l’offre, la priorité de commande détermine la source d’approvisionnement à appliquer en premier. Pour plus d’informations, voir [Hiérarchisation des commandes](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Prévisions de demande et commandes cadres

Les prévisions et les commandes cadres représentent la demande anticipée. La commande cadre, qui regroupe les achats prévus d’un client sur une certaine période, se charge d’amortir l’incertitude de la prévision globale. La commande cadre est une prévision spécifique au client qui s’ajoute à la prévision non spécifiée comme illustré ci-dessous.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planification avec prévisions.":::

Learn more at [La demande de prévision est réduite par les commandes vente](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Affectation de planification

Tous les articles doivent être replanifiés lorsque le modèle de demande ou d’offre a changé depuis le dernier calcul d’un plan. Par exemple, si vous saisissez une nouvelle commande client ou en modifiez une existante, recalculez le plan. Les autres motifs de nouvelle planification sont notamment une modification de prévision ou la quantité de stock de sécurité souhaitée. La modification d’une nomenclature par l’ajout ou la suppression d’un composant indique très probablement une modification, mais pour le composant uniquement.  

Le système de planification contrôle ces événements et affecte les articles appropriés pour la planification.  

Pour plusieurs magasins, l’affectation se produit au niveau de l’article par combinaison de magasins. Si une commande vente a été créée à un seul magasin, [!INCLUDE [prod_short](includes/prod_short.md)] affecte l’article à ce magasin spécifique pour la planification.  

La raison de la sélection d’articles pour la planification est une question de performances système. Si le motif demande-approvisionnement d’un article n’a pas été modifié, le système de planification ne propose aucune action à effectuer. Sans l’affectation de planification, le système devrait effectuer les calculs pour tous les articles afin de déterminer quoi planifier. Pour en savoir plus sur les raisons d’affecter des articles à la planification, accédez à [Détails de conception : tableau d’affectation de planification](design-details-planning-assignment-table.md).  

Voici les options de planification disponibles :  

* **Calculer planning régénératif** calcule tous les articles sélectionnés, que ce soit nécessaire ou non.  
* **Calculer planning par écart** calcule uniquement les articles dont le motif demande-approvisionnement a été modifié et, par conséquent, qui ont été affectés au planning.  

Certaines personnes croient que la planification par écart doit être exécutée à la volée, par exemple, quand les commandes vente sont saisies. Toutefois, la planification à la volée peut être source de confusion car le chaînage dynamique et les messages d’action sont également calculés à la volée. [!INCLUDE[prod_short](includes/prod_short.md)] offre un contrôle en temps réel de disponibilité à la vente. Il fournit des avertissements contextuels lorsque vous saisissez des commandes client et que le plan d’approvisionnement actuel ne peut pas répondre à la demande.  

Le système de planification planifie uniquement les articles que vous avez préparés avec les paramètres de planification appropriés. Sinon, il suppose que vous allez planifier les articles manuellement ou semi-automatiquement à l’aide de la fonction Planification commande. Pour plus d’informations sur les procédures de planification automatiques, consultez [Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md).  

## Dimensions d’article

La demande et l’approvisionnement peuvent contenir des codes variante et des codes magasin qui doivent être respectés lorsque le système de planification équilibre la demande et l’approvisionnement.  

[!INCLUDE [prod_short](includes/prod_short.md)] traite les codes variante et magasin du système en tant que dimensions d’article sur une ligne de commande vente, une écriture comptable de stock, etc. Par conséquent, il calcule une planification pour chaque combinaison de variante et de magasin, comme si la combinaison était un numéro d’article distinct.  

Au lieu de calculer des combinaisons théoriques de variante et magasin, [!INCLUDE [prod_short](includes/prod_short.md)] ne calcule que les combinaisons réellement existantes dans la base de données. Pour plus d’informations sur la manière dont le système de planification traite les codes magasin sur demande, consultez [Détails de conception : demande à un magasin vide](design-details-balancing-demand-and-supply.md).  

## Attributs article

Les articles ont souvent des attributs généraux, tels qu’un numéro d’article, un code de variante, un code d’emplacement et un type de commande. Cependant, chaque événement d’offre et de demande peut comporter d’autres spécifications, telles que des numéros de série ou de lot. Le système de planification planifie ces attributs de certaines manières en fonction de leur niveau de spécification.  

Un lien ordre pour ordre entre l’offre et la demande est un autre type d’attribut qui affecte le système de planification. Learn more at [Liens ordre pour ordre](#order-to-order-links).

### Attributs spécifiques

Certains attributs de demande sont spécifiques et un approvisionnement doit leur correspondre exactement.

* Numéros de série ou de lot qui nécessitent une application spécifique (ces attributs sont requis si vous activez le bouton à bascule **NS - Traçabilité spéc.** ou **N° lot - Traçabilité spéc.** sur la page **Fiche code traçabilité** pour le code de traçabilité utilisé par l’article.)  
* Les liens avec les commandes approvisionnement créées manuellement ou automatiquement pour une demande spécifique (liens ordre pour ordre).  

Le système de planification applique les règles suivantes à ces attributs :  

* Une demande avec des attributs spécifiques peut être satisfaite uniquement par un approvisionnement aux attributs correspondants.  
* L’approvisionnement avec des attributs spécifiques peut également répondre à la demande qui ne requiert pas spécifiquement ces attributs.  

Si le stock ou les approvisionnements prévus ne peuvent pas répondre à une demande d’attributs spécifiques, le système de planification suggère une nouvelle commande approvisionnement sans tenir compte des paramètres de planification.  

### Attributs non spécifiques

Les articles avec numéro de série ou de lot sans configuration de traçabilité d’article spécifique peuvent avoir des numéros de série ou de lot non spécifiques. Ces types de numéros peuvent être appliqués à n’importe quel numéro de série ou de lot. Le système de planification a plus de liberté pour répondre, par exemple, à une demande de série fabriquée avec un approvisionnement de série, généralement dans le stock.  

Les demandes-approvisionnements avec des numéros de série ou de lot, spécifiques ou non spécifiques, sont de haute priorité et sont donc exempts de la zone gelée Ils feront partie de la planification, même s’ils sont dus avant la date de début de la planification. Learn more at [Les numéros de série et de lot sont chargés en fonction du niveau de détail](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Pour plus d’informations sur la manière dont le système de planification équilibre les attributs, consultez [Les numéros de série et de lot et les liens Ordre pour ordre sont exempts de la période précédente](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Liens ordre pour ordre

Ordre pour ordre signifie que vous achetez, assemblez ou produisez un article pour une demande spécifique. Il y a plusieurs raisons de choisir cette stratégie :

* La demande est peu fréquente.
* Le délai est insignifiant.
* Les attributs requis varient.  

Il existe un autre cas d’utilisation des liens ordre pour ordre : la liaison d’un ordre d’assemblage à une commande vente dans un scénario Assembler pour commande.  

les liens ordre pour ordre sont appliqués entre la demande et l’approvisionnement de quatre manières :  

* Lorsque l’article planifié utilise la méthode de réapprovisionnement **Commande**  
* Lorsque vous utilisez la méthode de fabrication Fabrication à la commande pour créer des ordres de fabrication de type multi-niveau ou projet (la production de composants sur le même ordre de fabrication)  
* Lorsque vous créez des ordres de fabrication pour les commandes vente avec la fonction Planification commande vente  
* Lorsque vous assemblez un article pour une commande client (**Stratégie d’assemblage** est définie sur **Assembler pour commande**)  

Le système de planification suggère que vous ne commandiez que la quantité requise. L’ordre d’achat, de production ou d’assemblage continue de répondre à la demande. Par exemple, en cas de modification du délai ou de la quantité d’une commande vente, le système de planification suggère que vous modifiiez la commande approvisionnement en conséquence.  

Lorsque les liens commande-à-commande existent, le système de planification n’implique pas d’approvisionnement ou de stock lié dans la procédure d’équilibre. Les planificateurs peuvent décider d’utiliser l’approvisionnement lié ou une nouvelle demande. Dans ce dernier cas, ils peuvent supprimer la commande approvisionnement ou réserver manuellement l’approvisionnement lié.  

Les réservations et les liens de chaînage dynamique se rompent si une situation devient impossible. Par exemple, lors du déplacement de la demande à une date antérieure à celle de l’offre. Les liens de commande à commande s’adaptent aux changements de la demande ou de l’offre et ne se rompent jamais.  

## Réservations

Le système de planification n’inclut pas de quantité réservée dans les calculs. Par exemple, si une quantité pour une commande client est entièrement ou partiellement réservée, vous ne pouvez pas utiliser la quantité pour couvrir une autre demande.

Le système de planification inclut les quantités réservées dans le profil de stock prévisionnel. Il doit prendre en compte toutes les quantités pour déterminer quand le point de commande est passé et de combien il faut réapprovisionner pour atteindre le niveau de stock maximum. Les réservations inutiles augmentent donc les risques d’épuisement des niveaux de stock parce que la logique de planification ne détecte pas les quantités réservées.  

L’image suivante montre comment les réservations peuvent entraver la planification.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planification avec réservations.":::

Pour plus d’informations, consultez [Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md).  

## Alertes

La première colonne dans la feuille planning concerne les champs d’avertissement. Une icône d’avertissement s’affiche lorsque vous créez une ligne planning pour une situation inhabituelle.  

L’approvisionnement pour les lignes planning avec des avertissements n’est pas modifié en fonction des paramètres de planification. Au lieu de cela, le système de planification propose un approvisionnement pour couvrir la quantité de demande exacte. Cependant, le système peut être configuré pour respecter les paramètres de planification pour les lignes planning avec certains avertissements. Les informations d’avertissement sont affichées sur la page **Éléments planning non chaînés**, qui est affiche également les liens de suivi de commande vers des entités réseau hors commande. Trois types d’avertissements sont disponibles :  

* Urgence  
* Exception  
* Attention  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Avertissements dans la feuille planning.":::

### Urgence

L’avertissement Urgence est affiché dans deux situations :  

* Lorsque le stock est négatif à la date de début de la planification  
* Lorsqu’il existe des événements d’offre ou de demande rétroactifs  

Si le stock d’un article est négatif à la date de début de la planification, le système de planification suggère un approvisionnement d’urgence afin que la quantité négative arrive à la date de début de la planification. Le texte d’avertissement indique la date de début et la quantité de la commande d’urgence. Learn more at [Traitement du stock prévisionnel négatif](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Les lignes de document dont les dates d’échéance sont antérieures à la date de début de la planification sont regroupées en une commande approvisionnement d’urgence. La commande est planifiée pour arriver à la date de début de la planification.  

### Exception

L’avertissement Exception s’affiche si le stock disponible prévu descend en dessous du stock de sécurité. Le système de planification suggère une commande approvisionnement pour répondre aux besoins à la date d’échéance. Le texte d’avertissement indique la quantité du stock de sécurité et la date à laquelle elle est entamée.  

La violation du niveau de stock de sécurité est une exception. Cela ne devrait pas arriver si le point de commande est correctement défini. Learn more at [Le rôle du point de commande](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Les propositions de commande exceptionnelles permettent de s’assurer que le stock disponible prévu n’est jamais inférieur au niveau de stock de sécurité. La quantité proposée couvre le stock de sécurité, sans tenir compte des paramètres de planification. Toutefois, dans certains cas, des modificateurs de commande sont pris en compte.  

> [!NOTE]  
> Le système de planification peut consommer le stock de sécurité intentionnellement, puis le réapprovisionne immédiatement. Learn more at [Consommer le stock de sécurité](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Attention

L’avertissement Attention est affiché dans trois situations :  

* La date de début de la planification est antérieure à la date de travail.  
* La ligne planning suggère de changer une commande achat ou un ordre de fabrication lancé.  
* Le stock prévisionnel dépasse le niveau de dépassement de capacité à la date d’échéance. Learn more at [Rester sous le niveau de dépassement de capacité](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Dans les lignes planning comportant des avertissements, le champ **Accepter message d’action** n’est pas sélectionné, car le gestionnaire doit étudier les lignes avant de mettre en application ce plan.  

## Journaux des erreurs

Dans la page de demande **Calculer planning**, vous pouvez sélectionner le champ **Arrêter et afficher la première erreur** pour arrêter l’exécution de la planification quand il rencontre la première erreur. Un message affiche des informations sur l’erreur. S’il y a une erreur, la feuille planning affiche uniquement les lignes planning traitées avec succès avant que l’erreur ne se produise.  

Si le champ n’est pas activé, le traitement par lots **Calculer planning** se poursuit jusqu’à ce qu’il soit terminé. Les erreurs éventuelles n’interrompent pas le traitement par lots. S’il y a des erreurs, un message indique le nombre d’articles concernés. La page **Journal des erreurs de planning** fournit des informations supplémentaires sur l’erreur et des liens vers les documents ou les configurations concernés.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Messages d’erreur dans la feuille planning.":::

## Flexibilité planification

Il n’est pas toujours pratique de planifier une commande approvisionnement existante. Par exemple, lorsque la production a commencé ou que vous embauchez des personnes supplémentaires un jour précis pour faire le travail. Pour indiquer si le système de planification peut modifier une commande existante, toutes les lignes de commande approvisionnement ont un champ **Flexibilité planification** avec deux options :  **Illimitée** ou **Aucune**. Si le champ est défini sur **Aucune**, le système de planification ne tente pas de modifier la ligne commande approvisionnement.  

Vous pouvez choisir manuellement une option dans le champ ; cependant, dans certains cas, elle sera définie automatiquement par [!INCLUDE [prod_short](includes/prod_short.md)]. Le fait que vous puissiez manuellement définir la flexibilité de planification est important, parce que cela permet d’adapter facilement l’utilisation de la fonction dans différents flux de travail et scénarios métier. Pour plus d’informations sur l’utilisation de ce champ, consultez [Détails de conception : transferts de planification](design-details-transfers-in-planning.md).  

## Planning commande

L’outil de base de planification de l’approvisionnement représenté par la page **Planification commande** est conçu pour la prise de décision manuelle. Il ne tient compte d’aucun paramètre de planification et n’est donc pas traité ultérieurement dans cet article. Learn more at [Planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Nous vous recommandons de ne pas utiliser la planification des commandes si votre entreprise utilise déjà des feuilles planning ou des demandes achat. Les commandes approvisionnement créées via la page **Planning commande** peuvent être modifiées ou supprimées pendant les planifications automatisées. Ces modifications se produisent parce que l’exécution de la planification automatisée utilise des paramètres de planification que vous n’avez peut-être pas pris en compte lorsque vous avez créé manuellement le plan dans la page Planning commande.  

## Chargement limité

[!INCLUDE[prod_short](includes/prod_short.md)] fournit un calendrier approximatif pour planifier une utilisation raisonnable des ressources. Il ne crée ni ne gère automatiquement des plannings détaillés basés sur des priorités ou des règles d’optimisation.  

L’utilisation prévue de la fonction de capacité critique est la suivante :

* Pour éviter de surcharger les ressources
* Pour s’assurer que la capacité n’est pas laissée non allouée, si cela pourrait réduire le délai d’exécution d’un ordre de fabrication

Lors de la planification avec des ressources avec capacité critique, [!INCLUDE [prod_short](includes/prod_short.md)] veille à ce que les ressources ne soient pas chargées au-dessus de leur capacité (charge critique). Il affecte chaque opération à l’emplacement du temps disponible le plus proche. Si le créneau n’est pas assez long pour effectuer toute l’opération, il divise l’opération en au moins deux parties placées dans les créneaux disponibles les plus proches.  

> [!NOTE]  
> En cas de répartition des opérations, le temps de préparation n’est affecté qu’une fois, car on suppose qu’un certain ajustement manuel est effectué pour optimiser le planning.  

Vous pouvez ajouter un délai tampon aux ressources pour réduire la répartition des opérations. Ce délai permet à [!INCLUDE [prod_short](includes/prod_short.md)] de programmer la charge le dernier jour possible en dépassant légèrement le pourcentage de charge critique.  

## Voir aussi

[Détails de conception : transferts de planification](design-details-transfers-in-planning.md)  
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)  
[Détails de conception : tableau d’affectation de planification](design-details-planning-assignment-table.md)  
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)  
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
