---
title: Détails de conception - Concepts centraux du système de planification | Microsoft Docs
description: Les fonctions de planification se trouvent dans un traitement par lots qui sélectionne d'abord les articles appropriés et la période à planifier. Il suggère ensuite les actions que l'utilisateur peut effectuer en fonction de la situation demande/approvisionnement et des paramètres de planification des articles.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6cfe028d21086269f1492aefde31fe6b659d06b4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788136"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Détails de conception : concepts centraux du système de planification
Les fonctions de planification se trouvent dans un traitement par lots qui sélectionne d'abord les articles appropriés et la période à planifier. Puis, en fonction du code de bas niveau de chaque article (ligne nomenclature), le traitement par lots appelle une unité de code, qui calcule un programme d'approvisionnement en équilibrant les séries approvisionnement-demande et en suggérant des actions possibles à mener pour l'utilisation. Les mesures suggérées apparaissent sous forme de lignes dans la feuille planning ou dans la demande achat.  

![Contenu de la page Feuille planning](media/NAV_APP_supply_planning_1_planning_worksheet.png "Contenu de la page Feuille planning")  

Le gestionnaire d'une société, par exemple un acheteur ou un gestionnaire de production, est censé être l'utilisateur du système de planification. Le système de planification aide l'utilisateur en effectuant les calculs étendus mais relativement simples d'une planification. L'utilisateur peut alors se consacrer à résoudre les problèmes plus difficiles, par exemple lorsque les choses diffèrent de la normale.  

Le système de planification est guidé par la demande prévue et réelle des clients, par exemple, les commandes de prévisions et de vente. L'exécution du calcul de planification a pour effet que l'application suggère à l'utilisateur de prendre des mesures spécifiques concernant l'approvisionnement possible auprès des fournisseurs, des départements Production ou Assemblage, ou les transferts à partir d'autres entrepôts. Ces mesures suggérées peuvent être de créer de nouvelles commandes approvisionnement, comme des ordres d'achat ou de fabrication. S'il y a déjà des commandes approvisionnement, les mesures suggérées peuvent être d'augmenter ou d'accélérer les commandes pour répondre à l'évolution de la demande.  

Un autre objectif du système de planification est de garantir que le stock ne croisse pas inutilement. En cas de baisse de la demande, le système de planification suggère à l'utilisateur de reporter, de réduire ou d'annuler des commandes approvisionnement existantes.  

MRP et PDP, Calculer planning par écart et Calculer planning régénératif sont toutes des fonctions en une seule unité de code qui contient la logique de planification. Cependant, le calcul du programme d'approvisionnement implique différents sous-systèmes.  

Notez que le système de planification ne comprend aucune logique dédiée pour le nivellement de la capacité ou la planification précise. Par conséquent, un tel travail de planification s'effectue en tant que discipline séparée. Le manque d'intégration directe entre les deux domaines signifie également que des changements substantiels de capacité ou de planification obligeront à exécuter de nouveau la planification.  

## <a name="planning-parameters"></a>Paramètres de planification  
Les paramètres de planification que l'utilisateur définit pour un article ou un groupe d'articles contrôlent les actions que le système de planification va proposer dans les différentes situations. Les paramètres de planification sont définis sur chaque fiche article pour contrôler quand, combien et comment réapprovisionner.  

Les paramètres de planification peuvent également être définis pour toute combinaison d'article, de variante et de magasin en définissant un point de stock pour chaque combinaison nécessaire, puis en spécifiant différents paramètres.  

Pour plus d'informations, voir [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) et [Détails de conception : paramètres de planification](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Date début de la planification  
Pour éviter un plan d'approvisionnement incorporant des commandes ouvertes dans le passé et proposant des actions potentiellement impossibles, le système de planification traite toutes les dates antérieures à la date de début de la planification comme zone gelée dans laquelle les règles spécifiques suivantes s'appliquent :  

L'ensemble de l'offre et de la demande antérieur à la date de début de la période de planification sera considéré comme faisant partie du stock ou comme étant expédié.  

En d'autres termes, il est supposé que la planification pour le passé est exécutée conformément au planning donné.  

Pour plus d'informations, voir [Traiter les commandes avant la date début de la planification](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Chaînage dynamique (Origine des besoins)  
Le chaînage dynamique, avec sa création simultanée des messages d'action dans la feuille planning, ne fait pas partie du système de planification des approvisionnements dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette fonction lie, en temps réel, la demande et des montants qui pourraient les couvrir, chaque fois qu'une nouvelle demande ou un approvisionnement est créé ou modifié.  

Par exemple, si l'utilisateur entre ou modifie une commande vente, le système chaînage dynamique recherche immédiatement un approvisionnement approprié pour couvrir la demande. Cela peut être à partir du stock ou d'une commande approvisionnement prévue (telle qu'une commande achat ou un ordre de fabrication). Lorsqu'une source d'approvisionnement est trouvée, le système crée un lien entre la demande et l'approvisionnement, et l'affiche sur des pages en lecture seule qui sont consultées depuis les lignes document associées. Lorsque l'approvisionnement approprié est introuvable, le système de suivi de commande dynamique crée des messages d'action dans la feuille de planification avec des suggestions de plan d'approvisionnement reflétant l'équilibre dynamique. Par conséquent, le système chaînage dynamique offre un système de planification de base qui peut être utile au gestionnaire et à d'autres rôles dans la chaîne d'approvisionnement interne.  

Par conséquent, le chaînage dynamique peut être considéré comme un outil qui aide l'utilisateur à déterminer s'il faut accepter les suggestions de commande approvisionnement. Du côté de l'approvisionnement, un utilisateur peut visualiser quelle demande a créé l'approvisionnement, et du côté de la demande, quel approvisionnement doit couvrir la demande.  

![Exemple de chaînage dynamique](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Exemple de chaînage dynamique")  

Pour plus d'informations, voir [Détails de conception : réservation, chaînage et message d'action](design-details-reservation-order-tracking-and-action-messaging.md).  

Dans les sociétés avec un faible flux d'articles et des structures de produits moins avancées, il peut être adéquat d'utiliser le chaînage dynamique comme moyen principal de planification de l'approvisionnement. Toutefois, dans des environnements où l'activité est plus intense, le système de planification doit être utilisé pour assurer un planning d'approvisionnement à tout moment correctement équilibré.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Comparaison entre le chaînage dynamique et le système de planification  
À première vue, il peut être difficile de différencier le système de planification du chaînage dynamique. Les deux fonctions affichent une sortie dans la feuille planning en suggérant les actions que le gestionnaire doit entreprendre. Toutefois, la manière dont cette production est produite diffère.  

Le système de planification traite l'ensemble de la configuration de demande et d'approvisionnement d'un article au travers de tous les niveaux de la hiérarchie de nomenclature, alors que le chaînage dynamique gère uniquement la situation de la commande qui l'a activée. Lors de l'équilibre de la demande et de l'approvisionnement, le système de planification crée des liens dans un mode de lots activé par l'utilisateur, alors que Dynamic Order Tracking crée les liens automatiquement et à la volée, chaque fois que l'utilisateur saisit une demande ou un approvisionnement dans l'application, comme une commande vente ou une commande achat.  

Le chaînage dynamique crée des liens entre la demande et l'approvisionnement lorsque les données sont saisies, sur la base du principe premier arrivé, premier servi. Cela peut conduire du désordre dans les priorités. Par exemple, une commande vente saisie en premier, avec une date d'échéance du mois suivant, peut être liée à l'approvisionnement en stock, alors que la commande vente suivante à échéance le lendemain peut entraîner la création d'une commande achat par un message d'action afin de la couvrir, comme illustré ci-dessous.  

![Exemple de chaînage dans la planification de l'approvisionnement 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Exemple de chaînage dans la planification de l'approvisionnement 1")  

Par contre, le système de planification traite l'ensemble des demandes et approvisionnements pour un article spécifique, par ordre de priorité en fonction des dates d'échéance et des types de commande., c.-à-d., sur la base du principe de priorité selon les besoins. Il supprime les liens traçabilité commande qui ont été créés de façon dynamique et les rétablit en fonction de la priorité date d'échéance. Lorsque le système de planification a été exécuté, il a résolu tous les déséquilibres entre la demande et l'approvisionnement, comme illustré ci-dessous pour les mêmes données.  

![Exemple de chaînage dans la planification de l'approvisionnement 2](media/NAV_APP_supply_planning_1_planning_graph.png "Exemple de chaînage dans la planification de l'approvisionnement 2")  

Après l'exécution de la planification, il ne reste aucun message d'action dans la table Écriture message d'action, parce qu'ils ont été remplacés par les actions suggérées dans la feuille planning  

Pour plus d'informations, voir Liens de chaînage lors de la planification dans [Équilibrage de l'approvisionnement avec la demande](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand).  

## <a name="sequence-and-priority-in-planning"></a>Séquence et priorité de la planification  
Lors de l'établissement d'un plan, la séquence des calculs est importante que le travail soit réalisé dans un délai raisonnable. En outre, la gestion des priorités des besoins et ressources joue un rôle important pour obtenir les meilleurs résultats.  

Le système de planification dans [!INCLUDE[d365fin](includes/d365fin_md.md)] est axé sur les demandes. Les articles de niveau supérieur doivent être planifiés avant les articles de bas niveau, car la planification des articles de niveau supérieur peut générer une demande supplémentaire d'articles de niveau inférieur. Ceci signifie, par exemple, que des sites de détail doivent être planifiés avant que les centres de distribution ne soient planifiés, car le programme pour un site de détail peut inclure une demande supplémentaire du centre de distribution. Sur un niveau d'équilibre détaillé, cela signifie également qu'une commande vente ne doit pas déclencher une commande approvisionnement si une commande approvisionnement déjà lancée peut couvrir la commande vente. De même, un approvisionnement portant un numéro de lot spécifique ne doit pas être affecté pour couvrir une demande générique si une autre demande requiert ce lot spécifique.  

### <a name="item-priority--low-level-code"></a>Priorité d'article / Code plus bas niveau  
Dans un environnement de fabrication, la demande d'un article fini et pouvant être vendu a pour résultat une demande dérivée pour les composants qui constituent l'article fini. La structure de nomenclature contrôle la structure des composants et peut couvrir plusieurs niveaux d'articles semi-finis. La planification d'un article va créer une demande dérivée pour des composants au niveau suivant, etc. Cela peut entraîner une demande dérivée pour les articles achetés. Par conséquent, le système de planification planifie les articles par ordre de leur classement dans la hiérarchie de nomenclature totale, en commençant par les articles terminés vendables au niveau supérieur et en continuant dans la structure produit jusqu'aux articles du plus bas niveau (en fonction du code plus bas niveau.)  

![Planification des nomenclatures](media/NAV_APP_supply_planning_1_BOM_planning.png "Planification des nomenclatures")  

Les chiffres indiquent dans quelle séquence le système fait des propositions pour les commandes approvisionnement au niveau supérieur, et en supposant que l'utilisateur acceptent ces propositions, pour tous les articles au niveau inférieur également.  

Pour plus d'informations sur la fabrication, voir [Chargement des profils de stock](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

### <a name="locations--transfer-level-priority"></a>Magasins/priorité de niveau transfert  
Les sociétés actives dans plus d'un magasin peuvent être amenées à planifier chaque magasin individuellement. Par exemple, le niveau de stock de sécurité d'un article et sa méthode de réapprovisionnement peuvent différer d'un magasin à un autre. Dans ce cas, les paramètres de planification doivent être spécifiés par article et également par magasin.  

Ceci est pris en charge avec l'utilisation des points de stock, où des paramètres de planification individuels peuvent être spécifiés au niveau des points de stock. Un point de stock peut être considéré comme un article dans un magasin spécifique. Si l'utilisateur n'a pas défini un point de stock pour ce magasin, l'application utilisera par défaut les paramètres définis sur la fiche article. L'application calcule une planification pour les magasins actifs uniquement, c'est-à-dire les magasins où il existe une demande ou un approvisionnement pour l'article donné.  

En principe, tout article peut être traité dans n'importe quel magasin, mais l'application du programme du concept de magasin est assez stricte. Par exemple, une commande vente dans un magasin ne peut pas être satisfaite par une certaine quantité en stock dans un autre magasin. La quantité en stock doit d'abord être transférée au magasin spécifié sur la commande vente.  

![Planification pour points de stock](media/NAV_APP_supply_planning_1_SKU_planning.png "Planification pour points de stock")  

Pour plus d'informations, voir [Détails de conception : transferts de planification](design-details-transfers-in-planning.md)  

### <a name="order-priority"></a>Priorité de commande  
Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée ; la demande du jour doit être traitée avant la demande des jours suivants. Mais en plus de ce certain type de priorité, les différents types de demande et d'approvisionnement doivent être triés en fonction de l'importance commerciale pour choisir quelle demande doit être satisfaite avant de répondre à une autre demande. Du côté de l'approvisionnement, la priorité de la commande indique la source d'approvisionnement qui doit être lettrée avant d'appliquer d'autres source d'approvisionnement.  

Pour en savoir plus, voir [Affecter une priorité aux commandes](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Prévisions de demande et commandes ouvertes  
Les prévisions et les commandes ouvertes représentent la demande anticipée. La commande ouverte, qui regroupe les achats prévus d'un client sur une certaine période, se charge d'amortir l'incertitude de la prévision globale. La commande ouverte est une prévision spécifique au client qui s'ajoute à la prévision non spécifiée comme illustré ci-dessous.  

![Planification avec prévisions](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planification avec prévisions")  

Pour plus d'informations, reportez-vous à la section « La demande de prévision est réduite par les commandes vente » dans [Chargement des profils de stock](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Affectation planning  
Tous les articles doivent être planifiés. Cependant, il n'existe aucune raison de calculer une planification pour un article à moins qu'il n'y ait eu une modification de la configuration de l'offre ou de la demande depuis la dernière fois qu'un plan a été calculé.  

Si l'utilisateur a saisi une commande vente ou en a modifié une existante, il existe un motif de recalculer la planification. Les autres motifs sont notamment une modification de prévision ou la quantité de stock de sécurité souhaitée. La modification de nomenclatures lorsque vous ajoutez ou supprimez un composant indique très probablement une modification, mais pour le composant uniquement.  

Le système de planification contrôle ces événements et affecte les articles appropriés pour la planification.  

Pour plusieurs magasins, l'affectation se fait au niveau de l'article par combinaison de magasins. Si, par exemple, une commande vente a été créée à un seul magasin, l'application affecte l'article à ce magasin spécifique pour la planification.  

La raison de la sélection d'articles pour la planification est une question de performances système. Si aucune modification du motif demande-approvisionnement d'un article n'a été apportée, le système de planification ne propose aucune action à effectuer. Sans l'affectation de planification, le système devrait effectuer les calculs pour tous les articles afin de déterminer quoi planifier, et cela purgerait des ressources du système.  

La liste complète des motifs pour affecter un article à la planification est disponible dans [Détails de conception : tableau d'affectation de planification](design-details-planning-assignment-table.md).  

Les options de planification dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sont les suivantes :  

-   Calculer planning régénératif – calcule tous les articles sélectionnés, que ce soit nécessaire ou non.  
-   Calculer planning par écart – calcule uniquement les articles sélectionnés dont la configuration demande-approvisionnement a été modifiée et, par conséquent, qui ont été affectés au planning.  

Certains utilisateurs croient que la planification par écart doit être exécutée à la volée, par exemple, quand les commandes vente sont saisies. Toutefois, ceci peut être source de confusion car le chaînage dynamique et les messages d'action sont également calculés à la volée. En outre, [!INCLUDE[d365fin](includes/d365fin_md.md)] offre un contrôle en temps réel de la disponibilité à la vente, qui fournit des alertes contextuelles lors de la saisie de commande de vente si la demande ne peut pas être traitée dans le programme d'approvisionnement actif.  

En plus de ces considérations, le système de planification planifie uniquement les articles que l'utilisateur a préparés avec les paramètres de planification appropriés. Sinon, nous considérons que l'utilisateur organisera les articles manuellement ou semi-automatiquement à l'aide de la fonction Planification commande.  

Pour plus d'informations sur les procédures de planification automatiques, voir [Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Dimensions d'article  
La demande et l'approvisionnement peuvent contenir des codes variante et des codes magasin qui doivent être respectés lorsque le système de planification équilibre la demande et l'approvisionnement.  

Le système traite les codes variante et magasin du système en tant que dimensions d'article sur une ligne de commande vente, une écriture comptable de stock, etc. Par conséquent, il calcule une planification pour chaque combinaison de variante et de magasin, comme si la combinaison était un numéro d'article distinct.  

Au lieu de calculer une combinaison théorique de variante et magasin, l'application ne calcule que les combinaisons réellement existantes dans la base de données.  

Pour plus d'informations sur la manière dont le système de planification traite les codes magasin sur demande, voir [Détails de conception : demande à un magasin vide](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Attributs article  
Outre les axes analytiques généraux, par exemple le numéro d'article, le code variante, le code magasin et le type de commande, chaque événement d'offre et de demande peut comporter des spécifications supplémentaires sous forme de numéros de série/lot. Le système de planification planifie ces attributs de certaines manières en fonction de leur niveau de spécification.  

Un lien ordre pour ordre entre l'offre et la demande est un autre type d'attribut qui affecte le système de planification.  

### <a name="specific-attributes"></a>Attributs spécifiques  
Certains attributs de la demande sont spécifiques et doivent correspondre exactement à un approvisionnement correspondant. Les deux attributs spécifiques suivants existent :  

-   Numéros de série/lot demandés qui nécessitent une application spécifique (si la case à cocher **NS - Traçabilité spéc.** ou **N° lot - Traçabilité spéc.** est sélectionnée sur la page **Fiche code traçabilité** pour le code de traçabilité utilisé par l'article.)  
-   Les liens avec les commandes approvisionnement créées manuellement ou automatiquement pour une demande spécifique (liens ordre pour ordre).  

Pour les attributs, le système de planification applique les règles suivantes :  

-   Une demande avec des attributs spécifiques peut être satisfaite uniquement par un approvisionnement aux attributs correspondants.  
-   L'approvisionnement avec des attributs spécifiques peut également répondre à la demande qui ne demande pas spécifiquement ces attributs.  

Par conséquent, si une demande d'attributs spécifiques ne peut pas être satisfaite par le stock ou les approvisionnements prévisionnels, le système de planification suggère une commande approvisionnement pour couvrir la demande spécifique, quels que soient les paramètres de planification.  

### <a name="non-specific-attributes"></a>Attributs non spécifiques  
Les articles numérotés par série/lot sans configuration de traçabilité spécifique peuvent conserver les numéros de série/lot qui n'ont pas besoin d'être appliqués exactement au même numéro de série/lot, mais peuvent être appliqués à n'importe quel numéro de série/lot. Cela offre au système de planification plus de liberté pour répondre, par exemple, à une demande de série fabriquée avec un approvisionnement de série, généralement dans le stock.  

Des demandes-approvisionnements avec des numéros de série et/ou de lot, spécifiques ou non spécifiques, sont considérés comme de haute priorité et sont donc exempts de la zone gelée, c'est-à-dire qu'ils font partie de la planification même s'ils sont dus avant la date début de la planification.  

Pour plus d'informations, reportez-vous à la section « Les numéros de série/lot sont chargés en fonction du niveau de spécification » dans [Chargement des profils de stock](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Pour plus d'informations sur la manière dont le système de planification équilibre les attributs, voir [Les numéros de série et/ou de lot et les liens Ordre pour ordre sont exempts de la zone gelée](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Liens ordre pour ordre  
Un approvisionnement ordre pour ordre signifie qu'un article est acheté, assemblé ou produit pour couvrir exclusivement une demande spécifique. Généralement, il se rapporte aux A-items et la motivation pour choisir cette méthode peut être que la demande n'est pas fréquente, le délai de production est insignifiant ou les attributs requis varient.  

Il existe un autre cas particulier d'utilisation des liens ordre pour ordre : la liaison d'un ordre d'assemblage à une commande vente dans un scénario assembler pour commande.  

les liens ordre pour ordre sont appliqués entre la demande et l'approvisionnement de quatre manières :  

-   Lorsque l'article planifié utilise l'ordre de méthode de réapprovisionnement.  
-   Lors de l'utilisation de la méthode de fabrication Make-to-Order pour créer des ordres de fabrication de type multi-niveau ou projet (la production avait besoin de composants sur le même ordre de fabrication).  
-   Lors de la création des ordres de fabrication pour les commandes vente avec la fonction Sales Order Planning.  
-   En assemblant un article à une commande vente. (La stratégie d'assemblage est définie sur Assembler pour commande.  

Dans ces instances, le système de planification suggère uniquement de commander la quantité nécessaire. Une fois que créé, l'achat, la production ou l'ordre d'assemblage continueront à correspondre à la demande correspondante. Par exemple, en cas de modification du délai ou de la quantité d'une commande vente, le système de planification suggère que la commande approvisionnement correspondante soit modifiée en conséquence.  

Lorsque les liens commande-à-commande existent, le système de planification n'implique pas d'approvisionnement ou de stock lié dans la procédure d'équilibre. C'est à l'utilisateur d'évaluer si l'approvisionnement lié doit être utilisé pour couvrir une autre ou une nouvelle demande et, dans ce cas, de supprimer la commande approvisionnement ou de réserver l'approvisionnement lié manuellement.  

Les réservations et les liens traçabilité commande s'arrêteront si une situation devient impossible, tels que déplacer la demande à une date antérieure à l'approvisionnement. Toutefois, le lien ordre pour ordre s'adapte à tout changement dans la demande ou l'approvisionnement correspondant et le lien n'est de ce fait jamais rompu.  

## <a name="reservations"></a>Réservations  
Le système de planification n'inclut aucune quantité réservée dans le calcul. Par exemple, si une commande vente a été totalement ou partiellement réservée par rapport à la quantité du stock, la quantité réservée dans le stock ne peut pas être utilisée pour couvrir l'autre demande. Le système de planification n'inclut pas cet ensemble demande-approvisionnement dans ses calculs.  

Cependant, le système de planification inclut toujours les quantités réservées dans le profil de stock prévisionnel parce que toutes les quantités doivent être considérées pour déterminer quand le point de commande a été passé et la quantité de réapprovisionnement nécessaire pour atteindre et ne pas dépasser le niveau de stock maximum. Par conséquent, les réservations inutiles augmenteront les risques d'épuisement des niveaux de stock parce que la logique de planification ne détecte pas les quantités réservées.  

La figure suivante permet de visualiser la manière dont les réservations peuvent gêner le programme le plus faisable.  

![Planification avec réservations](media/NAV_APP_supply_planning_1_reservations.png "Planification avec réservations")  

Pour plus d'informations, voir [Détails de conception : réservation, chaînage et message d'action](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Alertes  
La première colonne dans la feuille planning concerne les champs d'avertissement. Les lignes planning créées pour une situation inhabituelle affichent une icône d'avertissement dans ce champ. L'utilisateur peut cliquer dessus pour consulter des informations supplémentaires.  

L'approvisionnement pour les lignes planning avec les alertes n'est normalement pas modifié en fonction des paramètres de planification. Au lieu de cela, le système de planification propose uniquement un approvisionnement pour couvrir la quantité de demande exacte. Cependant, le système peut être configuré pour respecter certains paramètres de planification pour les lignes planning avec certaines alertes. Pour plus d'informations, reportez-vous à la description de ces options pour le traitement par lots **Calc. planning - F. planning** et le traitement par lots **Calculer planning - F. demande** respectivement.  

Les informations d'avertissement sont affichées sur la page **Éléments planning non chaînés**, qui est également utilisée pour afficher les liens de suivi de commande vers des entités réseau hors commande. Les types d'alerte suivants existent :  

-   Urgence  
-   Exception  
-   Attention  

![Avertissements dans la feuille planning](media/NAV_APP_supply_planning_1_warnings.png "Avertissements dans la feuille planning")  

### <a name="emergency"></a>Urgence  
L'avertissement Urgence est affiché dans deux situations :  

-   Lorsque le stock est négatif à la date de début de la planification.  
-   Lorsqu'il existe des événements d'offre ou de demande rétroactifs.  

Si le stock d'un article est négatif à la date de début de la planification, le système de planification suggère un approvisionnement d'urgence afin que la quantité négative arrive à la date de début de la planification. Le texte d'avertissement indique la date de début et la quantité de la commande d'urgence. Pour plus d'informations, voir [Traitement du stock prévisionnel négatif](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Les lignes document avec une date d'échéance antérieure à la date de début de la planification sont consolidées dans une commande approvisionnement d'urgence pour que l'article arrive à la date de début de la planification.  

### <a name="exception"></a>Exception  
L'avertissement Exception s'affiche si le stock disponible prévu descend en dessous du stock de sécurité. Le système de planification suggère une commande approvisionnement pour répondre aux besoins à la date d'échéance. Le texte d'avertissement indique la quantité du stock de sécurité et la date à laquelle elle est entamée.  

Entamer le stock de sécurité est considéré comme une exception car cela ne doit pas se produire si le point de commande a été correctement défini. Pour plus d'informations, voir [Le rôle du point de commande](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

En règle générale, les propositions de commande exceptionnelles permettent de s'assurer que le stock disponible prévu n'est jamais inférieur au niveau de stock de sécurité. Cela signifie que la quantité proposée est suffisante pour couvrir le stock de sécurité, sans prendre en compte les paramètres de planification. Toutefois, dans certains cas, des modificateurs de commande sont pris en compte.  

> [!NOTE]  
>  Le système de planification peut consommer le stock de sécurité intentionnellement, puis le réapprovisionne immédiatement. Pour plus d'informations, reportez-vous à [Le stock de sécurité peut être consommé](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Attention  
L'avertissement Attention est affiché dans trois situations :  

-   La date de début de la planification est antérieure à la date de travail.  
-   La ligne planning suggère de changer une commande achat ou un ordre de fabrication lancé.  
-   Le stock prévisionnel dépasse le niveau de dépassement de capacité à la date d'échéance. Pour plus d'informations, voir [Rester sous le niveau de dépassement de capacité](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  Dans les lignes planning comportant des avertissements, le champ **Accepter message d'action** n'est pas sélectionné, car le gestionnaire doit poursuivre l'étude de ces lignes avant de mettre en application ce plan.  

## <a name="error-logs"></a>Journaux des erreurs  
Dans la page de demande Calculer planning, l'utilisateur peut sélectionner le champ **Arrêter et afficher la première erreur** pour arrêter l'exécution de la planification quand il rencontre la première erreur. Au même moment, un message affiche des informations sur l'erreur. S'il y a une erreur, seules les lignes planning traitées avant la détection de l'erreur apparaissent dans la feuille planning.  

Si le champ n'est pas activé, le traitement par lots Calculer planning se poursuit jusqu'à ce qu'il soit terminé. Les erreurs éventuelles n'interrompent pas le traitement par lots. S'il y a une ou plusieurs erreurs, une fois l'exécution de l'application terminée, celui-ci affiche un message indiquant le nombre d'articles concernés par les erreurs. La page **Journal des erreurs de planning** s'ouvre ensuite pour afficher des informations supplémentaires sur l'erreur et pour fournir des liens vers les documents ou les fiches paramètres concernés.  

![Messages d'erreur dans la feuille planning](media/NAV_APP_supply_planning_1_error_log.png "Messages d'erreur dans la feuille planning")  

## <a name="planning-flexibility"></a>Flexibilité planification  
Il n'est pas toujours pratique de planifier une commande approvisionnement existante, par exemple si la fabrication a commencé ou si du personnel supplémentaire est engagé un jour spécifique pour faire le travail. Pour indiquer si une commande existante peut être modifiée par le système de planification, toutes les lignes de commande approvisionnement ont un champ Planning Flexibility avec deux options : Unlimited ou None. Si le champ est défini sur Aucune, le système de planification ne tente pas de modifier la ligne commande approvisionnement.  

Le champ peut être manuellement défini par l'utilisateur, cependant, dans certains cas il est automatiquement paramétré par le système. Le fait que la flexibilité de planification peut être définie manuellement par l'utilisateur est important, parce que cela permet d'adapter facilement l'utilisation de la fonction dans différents flux de travail et cas commerciaux.  

Pour plus d'informations sur l'utilisation de ce champ, voir [Détails de conception : transferts de planification](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Planification commande  
L'outil de base de planification de l'approvisionnement représenté par la page **Planification commande** est conçu pour la prise de décision manuelle. Il ne tient compte d'aucun paramètre de planification et n'est donc pas traité ultérieurement dans ce document. Pour plus d'informations sur la fonction Planification commande, reportez-vous à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Il n'est pas recommandé d'utiliser la Planification commande si la société utilise déjà les feuilles planning ou demande. Les commandes approvisionnement créées via la page **Planning commande** peuvent être modifiées ou supprimées pendant les planifications automatisées. En effet, la planification automatisée utilise les paramètres de planification qui n'ont peut-être pas été pris en compte par l'utilisateur ayant créé la planification manuelle sur la page Planning commande.  

##  <a name="finite-loading"></a>Chargement limité  
[!INCLUDE[d365fin](includes/d365fin_md.md)] est un système ERP standard, et non un système d'affectation ou de gestion d'atelier. Il prévoit une utilisation des ressources faisable via une planification approximative, mais il ne crée ni ne met à jour automatiquement des plannings détaillés sur la base des priorités ou des règles d'optimisation.  

L'utilisation prévue de la fonction Capacité critique est 1) : pour éviter la surcharge de ressources spécifiques et 2) : pour s'assurer qu'aucune capacité n'est laissée non affectée si elle peut augmenter le délai d'exécution d'un ordre de fabrication. La fonction n'inclut pas d'équipements ni d'options pour gérer les priorités ou optimiser des opérations, comme on s'attendrait à en trouver dans un système d'affectation. Toutefois, elle permet de fournir des informations de capacité approximative utiles pour identifier des goulots d'étranglement et éviter de surcharger des ressources.  

Lors de la planification avec des ressources avec contraintes de capacité, le système veille à ce qu'aucune ressource ne soit chargée au-dessus de sa capacité définie (charge critique). Ceci est effectué en affectant chaque opération à l'emplacement du temps disponible le plus proche. Si le créneau n'est pas assez long pour effectuer toute l'opération, l'opération est répartie en au moins deux parties placées dans les créneaux disponibles les plus proches.  

> [!NOTE]  
>  En cas de répartition des opérations, le temps de préparation n'est affecté qu'une fois car on suppose qu'un certain ajustement manuel est effectué pour optimiser le planning.  

Le seuil peut être ajouté aux ressources pour réduire la répartition des opérations. Cela permet au système de planifier la charge sur le dernier jour possible en dépassant légèrement le pourcentage de charge critique si ceci peut réduire le nombre d'opérations qui sont divisées.  

Cela complète la planification des concepts centraux en relation avec la planification des approvisionnements dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Les sections suivantes examinent les concepts plus profonds et les placent dans le cadre des procédures de planification de base, de l'équilibrage de l'approvisionnement et de la demande, ainsi que de l'utilisation des méthodes de réapprovisionnement.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : transferts de planification](design-details-transfers-in-planning.md)   
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : tableau d'affectation de planification](design-details-planning-assignment-table.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)
