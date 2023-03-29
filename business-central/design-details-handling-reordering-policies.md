---
title: "Détails de conception\_: gestion des méthodes de réapprovisionnement"
description: Cet article donne un aperçu des stratégies de réapprovisionnement que vous pouvez utiliser dans la planification de l’approvisionnement.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# Détails de conception : gestion des méthodes de réapprovisionnement

Pour inclure un article dans la planification de l’approvisionnement, vous devez spécifier une politique de réapprovisionnement pour celui-ci sur la page **Fiche article**. Les méthodes de réapprovisionnement suivantes sont disponibles :  

* Qté fixe de commande.  
* Qté maximum  
* Ordre  
* Lot pour lot  

Les méthodes **Qté fixe de commande** et **Qté maximum** sont liées à la planification du stock. Ces méthodes coexistent avec l’équilibrage pas à pas de l’approvisionnement et le chaînage dynamique.  

## Le rôle du point de commande

Un point de commande représente la demande lors d’un délai. Lorsque le stock prévisionnel passe en dessous du niveau de stock défini par le point de commande, il est temps de commander. Le stock diminuera progressivement jusqu’à ce que le réapprovisionnement arrive. Il peut atteindre zéro ou le niveau du stock de sécurité. Le système de planification suggère une commande approvisionnement planifiée en aval au moment où le stock passe sous le point de commande.  

Les niveaux de stock peuvent varier considérablement au cours de l’intervalle de planification. Par conséquent, le système de planification surveille en permanence le stock disponible.

## Surveillance du niveau de stock prévisionnel et du point de commande

Le stock est un type d’approvisionnement, mais pour la planification de stock, le système de planification différencie deux niveaux de stock :  

* Stock projeté  
* Stock disponible projeté  

### Stock projeté  

Au début du processus de planification, l’le stock prévisionnel est la quantité brute en stock. La quantité brute comprend l’offre et la demande comptabilisées et non comptabilisées dans le passé. Cette quantité devient un niveau de stock projeté, maintenu par les quantités brutes de l’offre et de la demande futures. L’offre et la demande futures sont introduites dans la chronologie, qu’elles soient réservées ou allouées d’une autre manière.  

Le système de planification utilise le stock prévisionnel pour surveiller le point de commande et pour déterminer la quantité de réapprovisionnement lorsque la méthode de réapprovisionnement **Qté maximum** est utilisée.  

### Stock disponible projeté  

Le stock disponible projeté est le stock prévisionnel qui est disponible à un moment donné pour répondre à la demande. Le système de planification utilise le stock disponible projeté lors du contrôle du niveau de stock de sécurité. Le stock de sécurité doit toujours être disponible pour une demande inattendue.  

### Intervalles de planification  

Le stock prévisionnel est crucial pour détecter le moment où le point de commande est atteint et pour calculer la quantité de commande correcte en utilisant la méthode de réapprovisionnement **Qté maximum**.  

Le niveau de stock projeté est calculé au début de la période de planification. Il s’agit d’un niveau brut qui ne tient pas compte des réservations et des autres allocations. Pour contrôler ce niveau de stock durant la séquence de planification, le système de planification gère les changements cumulés sur une période de temps. Cette période est appelée un *intervalle de planification*. Pour en savoir plus sur les intervalles de planification, consultez [Intervalles de planification](#time-buckets). Le système de planification garantit que l’intervalle de planification est d’au moins un jour. Un jour est l’unité de temps minimale pour les événements d’offre ou de demande.  

### Déterminer le niveau de stock prévisionnel  

La prochaine séquence décrit la manière dont le système de planification détermine le niveau de stock prévisionnel :  

* Lorsqu’un événement d’approvisionnement est entièrement planifié, tel qu’une commande achat, il augmente le stock prévisionnel à la date d’échéance de l’événement.  
* Lorsqu’un événement de demande est entièrement satisfait, il ne diminue pas le stock prévisionnel immédiatement. Au lieu de cela, il valide un rappel de diminution, qui est un enregistrement interne qui contient la date et la quantité de l’ajout au stock prévisionnel.  
* Lorsqu’un événement d’approvisionnement ultérieur est planifié et ajouté à la chronologie, le système examine les rappels de baisse postés un par un jusqu’à la date planifiée de l’approvisionnement. Lors de ce processus, le niveau du point de commande du rappel interne d’augmentation peut être atteint ou dépassé.  
* Si une nouvelle commande approvisionnement est créée, le système vérifie si elle est saisie avant l’approvisionnement en cours. Si c’est le cas, le nouvel approvisionnement devient l’approvisionnement actif et la procédure d’équilibrage redémarre.  

L’image suivante illustre ce principe.  

![Déterminer le niveau de stock prévisionnel.](media/nav_app_supply_planning_2_projected_inventory.png "Déterminer le niveau de stock prévisionnel")  

1. L’approvisionnement **Sa** de 4 (fixe) clôture la demande **Da** de 3.  
2. CloseDemand : créez une relance de baisse de -3 (pas affiché).  
3. L’approvisionnement **Sa** est clôturé avec un excédent de 1 (plus aucune demande n’existe).  

     Le niveau de stock prévisionnel augmente à +4, alors que le stock **disponible** devient -1.  

4. L’approvisionnement suivant **Sb** de 2 (une autre commande) a déjà été placé dans la chronologie.  
5. Le système de planification recherche un rappel de diminution avant **Sb** (dans cet exemple, il n’y en a pas, donc aucune action n’est entreprise).  
6. Le système de planification ferme l’approvisionnement **Sb** (plus aucune demande n’existe), soit de A, en le réduisant à 0 (annuler), soit de B, en le laissant tel quel.  

     Le niveau de stock prévisionnel augmente (A: +0 => +4 or B: +2 = +6).  

7. Le système de planification effectue une dernière vérification. Y a-t-il un rappel de diminution ? Oui, il y en a un en date du **Da**.  
8. Le système de planification ajoute le rappel de diminution -3 au niveau de stock projeté, soit A : +4 -3 = 1 or B : +6 -3 = +3.  
9. Pour A, le système de planification crée une commande planifiée en aval qui commence à la date **Da**. Pour B, le point de commande est atteint et aucune commande n’est créée.

## Le rôle de l’intervalle de planification

L’objectif de l’intervalle de planification est de collecter les événements de demande sur la page de temps de manière à effectuer une commande approvisionnement commune.  

Pour les méthodes de réapprovisionnement qui utilisent un point de commande, vous pouvez définir un intervalle de planification. Les intervalles de planification permettent de s’assurer que les demandes appartenant à la même période sont accumulées. Le système vérifie ensuite l’effet sur le stock prévisionnel et si le point de commande a été dépassé.

Si vous dépassez le point de commande, le système planifie une nouvelle commande approvisionnement à partir de la fin de l’intervalle de planification. Les intervalles de planification débutent à la date de début de la planification.  

Le concept d’intervalle de planification reflète le processus manuel de vérifier le niveau de stock de manière fréquente plutôt que pour chaque transaction. Vous définissez la fréquence (l’intervalle de planification). Par exemple, vus pouvez rassembler tous les articles d’un fournisseur pour passer une commande hebdomadaire.  

![Exemple d’intervalle de planification dans la planification.](media/nav_app_supply_planning_2_reorder_cycle.png "Exemple d’intervalle de planification dans la planification")  

Les intervalles de planification sont souvent utilisés pour éviter un effet de cascade. Par exemple, une ligne équilibrée de demande et d’approvisionnement dans laquelle une demande antérieure est annulée ou une nouvelle demande est créée. Le résultat est que chaque commande approvisionnement (sauf la dernière) est replanifiée.

## Rester sous le niveau de dépassement de capacité

Lors de l’utilisation des méthodes **Qté maximum** et **Qté fixe de commande**, le système de planification se concentre sur le stock prévisionnel dans l’intervalle de planification donné uniquement. Il peut suggérer un approvisionnement supplémentaire lorsque des modifications de demande négative ou d’offre positive se produisent en dehors de l’intervalle de planification. Pour un approvisionnement supplémentaire, le système de planification calcule la quantité de laquelle vous devez diminuer l’approvisionnement. Cette quantité est appelée « niveau de dépassement de capacité ». Le dépassement de capacité est disponible sous la forme d’une ligne planning avec une action **Changer qté (diminuer)** ou **Annuler** et le message d’avertissement suivant :  

* Attention : le stock prévisionnel [xx] est supérieur au niveau de dépassement de capacité [xx] à la date d’échéance [xx].*  

![Niveau de dépassement de capacité.](media/supplyplanning_2_overflow1_new.png "Niveau de dépassement de capacité")  

### Calcul du niveau de dépassement de capacité  

Le niveau de dépassement de capacité est calculé de différentes manières en fonction de la méthode de réapprovisionnement.  

#### Qté maximum

Niveau de dépassement de capacité = stock maximum  

> [!NOTE]  
> Si vous utilisez une quantité minimale de commande, celle-ci est ajoutée comme suit :
>
> Niveau de dépassement de capacité = inventaire maximum + quantité minimum de commande.  

#### Qté fixe de commande.  

Niveau de dépassement de capacité = Quantité de réappro. + Point de commande  

> [!NOTE]  
> Si la quantité minimale de commande est supérieure au point de commande, elle est remplacée comme suit :
>
> Niveau de dépassement de capacité = quantité de réapprovisionnement + quantité minimale de commande  

#### Commandé par ;  

Si un multiple de commande existe, il ajuste le niveau de dépassement de capacité pour les deux méthodes de réapprovisionnement Qté maximum et Qté fixe de commande.  

### Création de la ligne planning avec un avertissement de dépassement capacité  

Une ligne planning est calculée lorsqu’un approvisionnement rend le stock prévisionnel supérieur au niveau de dépassement de capacité à la fin d’un intervalle de planification. Pour avertir sur l’approvisionnement supplémentaire, la ligne planning a un message d’avertissement, le champ **Accepter message d’action** n’est pas sélectionné et le message d’action est **Annuler** ou **Changer qté**  

#### Calcul de la quantité pour la ligne planning  

La quantité sur une ligne planning est calculée comme suit :

Quantité pour la ligne planning = Quantité d’approvisionnement actif – (Stock prévisionnel – Niveau de dépassement de capacité)  

> [!NOTE]  
> Pour toutes les lignes d’avertissement, les quantités maximales et minimales de commande et les multiples de commande sont ignorés.  

#### Définir le type de message d’action  

* Si la quantité de la ligne planning est supérieure à 0, le message d’action est **Changer qté**  
* Si la quantité de la ligne planning est égale ou inférieure à 0, le message d’action est **Annuler**  

#### Composition du message d’avertissement  

Dans le cas d’un dépassement de capacité, la page **Éléments planning non chaînés** affiche un message d’avertissement avec les informations suivantes :  

* Le niveau de stock prévisionnel qui a déclenché l’alerte  
* Niveau de dépassement de capacité calculé  
* Date d’échéance d’un événement d’approvisionnement  

Exemple : « Le stock projeté 120 est supérieur au niveau de dépassement de capacité 60 au 01/28/23 »  

### Exemple de scénario  

Dans ce scénario, un client modifie une commande vente de 70 à 40 pièces entre deux exécutions de planification. La fonction de dépassement de capacité réduit l’achat qui a été proposé pour la quantité de ventes initiale.  

#### Paramétrage de l’article  

|Méthode de réapprovisionnement|Qté maximum|  
|-----------------------|------------------|  
|Qté maximum commande|100|  
|Point de commande|50|  
|Stocks|80|  

#### Situation avant la sortie de vente  

|Événement|Changer qté|Stocks projetés|  
|-----------|-----------------|-------------------------|  
|Un jour|Aucune|80|  
|Vente|-70|10|  
|Fin de l’intervalle de planification|Aucune|10|  
|Suggérer une nouvelle commande achat|+90|100|  

#### Situation après la sortie de vente  

|Activer|Changer qté|Stocks projetés|  
|------------|-----------------|-------------------------|  
|Un jour|Aucune|80|  
|Vente|-40|40|  
|Achats|+90|130|  
|Fin de l’intervalle de planification|Aucune|130|  
|Proposer de réduire l’achat<br><br> achat de 90 à 60|-30|100|  

#### Lignes planning résultantes  

Le système crée une ligne planning d’avertissement pour réduire l’achat de 30, passant de 90 à 60, pour conserver le stock prévisionnel à 100 conformément au niveau de dépassement de capacité.  

![Planifier en fonction du niveau de dépassement de capacité.](media/nav_app_supply_planning_2_overflow2.png "Planifier en fonction du niveau de dépassement de capacité")  

> [!NOTE]  
> Sans la fonction de dépassement de capacité, aucun avertissement n’est créé si le niveau de stock prévisionnel est supérieur au maximum, ce qui pourrait entraîner un approvisionnement supplémentaire de 30.

## Traitement du stock prévisionnel négatif

Le point de commande exprime la demande anticipée lors du délai de l’article. Le stock prévisionnel doit être suffisamment élevé pour couvrir la demande jusqu’à ce que la nouvelle commande soit reçue. Par ailleurs, le stock de sécurité doit se charger des fluctuations de la demande jusqu’à un niveau de service ciblé.  

Le système de planification considère qu’il s’agit d’une urgence si une demande future ne peut pas être satisfaite à partir du stock prévisionnel. Ou, exprimé d’une autre manière, que le stock prévisionnel devient négatif. Le système vous suggère de créer une nouvelle commande approvisionnement pour couvrir la partie non satisfaite de la demande. La taille de la nouvelle commande approvisionnement ne tiendra pas compte du stock maximal ou de la quantité de réapprovisionnement, ni des modificateurs de commande suivants :

* Qté maximum commande ;
* Qté minimum commande ;
* Commandé par ; 

Au lieu de cela, elle reflète l’insuffisance exacte.  

La ligne planning pour ce type de commande approvisionnement affiche une icône d’avertissement **Urgence** et fournit des informations supplémentaires sur la situation.  

Dans l’illustration suivante, l’approvisionnement D représente une commande d’urgence pour ajuster le stock négatif.  

![Suggestion de planification d’urgence pour éviter un stock négatif.](media/nav_app_supply_planning_2_negative_inventory.png "Suggestion de planification d’urgence pour éviter un stock négatif")  

1. L’approvisionnement **A**, stock prévisionnel initial, est inférieur au point de commande.  
2. Un approvisionnement planifié en aval est créé (**C**).  

     (Quantité = Stock maximum – Niveau de stock projeté)  
3. L’approvisionnement **A** est clôturé par la demande **B** qui n’est pas totalement couverte.  

     (La demande **B** pourrait essayer de programmer l’offre C, mais l’intervalle de planification l’en empêche.)  
4. Un nouvel approvisionnement (**D**) est créé pour couvrir la quantité restante sur demande **B**.  
5. La demande **B** est clôturée (création d’une relance dans le stock prévisionnel).  
6. Le nouvel approvisionnement **D** est clôturé.  
7. Le stock prévisionnel est vérifié. Le point de commande n’a pas été franchi.  
8. L’offre **C** est clôturée (plus aucune demande n’existe).  
9. Vérification finale. Il n’y a pas de rappels de niveau de stock en attente.  

La section suivante décrit les caractéristiques des quatre méthodes de réapprovisionnement prises en charge.

## Méthodes de réapprovisionnement

Les méthodes de réapprovisionnement définissent la quantité à commander lorsque l’article doit être réapprovisionné. Quatre différentes méthodes de réapprovisionnement existent.  

### Qté fixe de commande

La méthode Qté fixe de commande est généralement utilisée pour la planification des stocks pour les articles présentant les caractéristiques suivantes :

* Faible coût de stock
* Faible risque d’obsolescence
* Faible nombre d’articles

En règle générale, utilisez cette méthode avec un point de commande qui reflète la demande anticipée pendant le délai de livraison de l’article.  

#### Calculé par intervalle de planification  

Si vous atteignez ou franchissez le point de commande dans un intervalle de planification (cycle de réapprovisionnement), le système suggère deux actions :

* Créer une nouvelle commande approvisionnement pour la quantité de réapprovisionnement
* Planifier une commande en aval à partir de la première date suivant la fin de l’intervalle de planification  

Le point de commande délimité par un intervalle de planification réduit le nombre de suggestions d’approvisionnement. Il reflète un processus de vérification manuelle du contenu réel des emplacements dans votre entrepôt.  

#### Crée uniquement l’approvisionnement nécessaire  

Avant de suggérer une nouvelle commande approvisionnement en réponse à un point de commande, le système de planification vérifie l’approvisionnement suivant :

* Si l’approvisionnement est déjà commandé
* Si vous vous attendez à recevoir l’approvisionnement dans le délai de livraison de l’article

Le système ne proposera pas de nouvelle commande approvisionnement si un approvisionnement doit amener le stock prévisionnel au point de commande dans le délai imparti.  

Les commandes approvisionnement créées spécifiquement pour répondre à un point de commande sont exclues de l’équilibrage de l’approvisionnement et ne seront pas modifiées. Si vous souhaitez supprimer progressivement un article qui a un point de commande, vérifiez manuellement vos commandes approvisionnement en attente ou modifiez la méthode de réapprovisionnement en **Lot pour lot**. Le système réduira ou annulera l’approvisionnement supplémentaire.  

#### Associe avec les modificateurs de commande  

Les modificateurs de commande, Qté minimum commande, Qté maximum commande et Multiple de commande, ne doivent pas jouer de rôle significatif lorsque vous utilisez la méthode Quantité fixe de commande. Cependant, le système de planification les prend en compte :

* Diminuez la quantité jusqu’à la quantité de commande maximale spécifiée (et créez deux nouveaux approvisionnements ou plus afin d’atteindre la quantité totale de commande)
* Augmentez la commande jusqu’à la quantité minimale de commande spécifiée
* Arrondissez la quantité de commande pour atteindre un multiple de commande spécifié  

#### Associe avec des calendriers  

Avant de suggérer une nouvelle commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé. Il utilise les calendriers que vous spécifiez dans le champ **Code calendrier principal** sur les pages **Informations société** et **Fiche magasin**.  

Si la date prévue est un jour chômé, le système de planification déplace la commande en aval au jour ouvré le plus proche. Le déplacement de la date peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une demande spécifique. Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.  

#### Ne doit pas être utilisé avec les prévisions  

Étant donné que la demande prévue est déjà exprimée au niveau du point de commande, il n’est pas nécessaire d’inclure une prévision dans la planification. S’il est important de baser le programme sur une prévision, utilisez la méthode **Lot pour lot**.  

#### Ne doit pas être utilisé avec les réservations  

Si vous avez réservé une quantité, par exemple une quantité dans le stock, pour une demande éloignée, vous pouvez perturber la base de la planification. Même si le niveau de stock projeté est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles. Le système peut essayer de compenser en créant des commandes exceptionnelles. Cependant, nous vous recommandons de définir le champ **Réserver** sur **Jamais** sur les articles planifiés à l’aide d’un point de commande.

### Quantité maximale

La stratégie Quantité maximum est une manière de mettre à jour le stock à l’aide d’un point de commande.  

Tout ce qui concerne la stratégie Qté fixe de commande s’applique également à cette méthode. La seule différence est la quantité de l’approvisionnement proposé. Lorsque vous utilisez la méthode de quantité maximale, la quantité de réapprovisionnement sera définie dynamiquement en fonction du niveau de stock prévisionnel. Par conséquent, cela diffère généralement de la méthode Ordre pour ordre.  

#### Calculer par intervalle de planification

Lorsque vous atteignez ou franchissez le point de commande, le système détermine la quantité de réapprovisionnement à la fin d’un intervalle de planification. Il mesure l’écart entre le niveau de stock prévisionnel actuel et le stock maximum spécifié pour déterminer la quantité à commander. Le système vérifie alors :

* Si l’approvisionnement est déjà commandé
* Si vous vous attendez à recevoir l’approvisionnement dans le délai de livraison de l’article

Si tel est le cas, le système réduit la quantité de la nouvelle commande approvisionnement des quantités déjà commandées.  

Si vous ne spécifiez pas de quantité de stock maximale, le système de planification garantit que le stock prévisionnel atteint la quantité de réapprovisionnement.

#### Associe avec les modificateurs de commande

En fonction de votre configuration, il peut être préférable de combiner la méthode Quantité maximale avec des modificateurs de commande : 

* Pour assurer une quantité minimum de commande
* Arrondissez la quantité à un nombre entier d’unités de mesure d’achat
* Fractionnez la quantité en lots, définis par la quantité maximale de commande  

### Combinaison avec des calendriers

Avant de suggérer une nouvelle commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé. Il utilise les calendriers que vous spécifiez dans le champ **Code calendrier principal** sur les pages **Informations société** et **Fiche magasin**.  

Si la date prévue est un jour chômé, le système de planification déplace la commande en aval au jour ouvré le plus proche. Le déplacement de la date peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une demande spécifique. Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.

### Ordre

Dans un environnement de fabrication à la commande, un article est acheté ou produit pour couvrir une demande spécifique. En règle générale, la méthode de réapprovisionnement de commande est utilisée pour les articles présentant les caractéristiques suivantes :

* La demande est peu fréquente
* Le délai est insignifiant
* Les attributs requis varient  

[!INCLUDE [prod_short](includes/prod_short.md)] crée un lien ordre pour ordre, qui agit en tant que connexion préliminaire entre l’approvisionnement (une commande approvisionnement ou un stock) et la demande. Vous pouvez appliquer le lien de ordre pour ordre lors de la planification des manières suivantes :  

* Lorsque vous utilisez la méthode de fabrication Fabrication à la commande pour créer des ordres de fabrication de type multi-niveau ou projet (la production avait besoin de composants sur le même ordre de fabrication)  
* Lorsque vous utilisez la fonction Planification commande vente pour créer un ordre de fabrication à partir d’une commande vente  

> [!TIP]
> Si les attributs des articles ne varient pas, il peut être préférable d’utiliser une méthode de réapprovisionnement Lot pour Lot. Par conséquent, le système utilise le stock non planifié et additionne uniquement les commandes vente ayant la même date d’expédition ou faisant partie d’un intervalle de planification défini.  

#### Liens ordre pour ordre et dates arriérées

Contrairement à la plupart des ensemble approvisionnement-demande, les commandes liées avec des dates d’échéance antérieures à la date de début de la planification sont entièrement planifiées par le système. La raison de cette exception est que les ensembles spécifiques offre-demande doivent être synchronisés. Pour plus d’informations sur la zone gelée qui s’applique à la plupart des types d’offre-demande, consultez [Traiter les commandes avant la date début de la planification](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### Lot pour lot

La méthode Lot pour Lot est la plus flexible car le système ne réagit qu’à la demande réelle. Il agit sur la demande anticipée à partir des prévisions et des commandes cadres, puis règle la quantité de la commande en fonction de la demande. La méthode cible les articles pour lesquels le stock peut être accepté, mais il convient de l’éviter.  

À certains égards, la méthode Lot pour lot est similaire à la méthode Ordre, mais elle a une approche générique des articles. Elle peut accepter des quantités en stock et regroupe l’offre et la demande dans les intervalles de planification que vous définissez.  

Vous spécifiez l’intervalle de planification dans le champ **Intervalle de planification** sur la page **Fiche article**. La taille minimale d’un intervalle de planification est d’un jour, car il s’agit de la plus petite unité de mesure de temps applicable aux événements d’offre et de demande dans [!INCLUDE [prod_short](includes/prod_short.md)].  

L’intervalle de planification fixe également des limites lorsque vous devez replanifier une commande approvisionnement pour répondre à une demande donnée. L’approvisionnement dans l’intervalle de planification est replanifié en entrée ou en sortie pour répondre à la demande. Un approvisionnement anticipé entraînera un excédent de stock et vous devez l’annuler. Pour un approvisionnement ultérieur, créez une nouvelle commande approvisionnement.  

Avec cette stratégie, vous pouvez spécifier un stock de sécurité pour compenser les variations de l’offre ou pour répondre à une demande soudaine.  

Étant donné que la quantité de la commande approvisionnement est basée sur la demande réelle, il peut être judicieux d’utiliser les modificateurs de commande :

* Arrondissez la quantité commandée pour atteindre un multiple de commande (ou une unité de mesure d’achat)
* Augmentez la commande jusqu’à la quantité minimale de commande spécifiée
* Diminuez la quantité jusqu’à la quantité de commande maximale spécifiée (et créez deux nouveaux approvisionnements ou plus afin d’atteindre la quantité totale nécessaire)

## Voir aussi  

[Détails de conception : paramètres de planification](design-details-planning-parameters.md)  
[Détails de conception : tableau d’affectation de planification](design-details-planning-assignment-table.md)  
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)  
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]