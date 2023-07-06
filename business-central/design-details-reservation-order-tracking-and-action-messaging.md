---
title: "Détails de conception\_: réservation, chaînage et message d’action | Microsoft Docs"
description: Le système de réservation est complet et inclut les fonctionnalités étroitement liées et parallèles du Chaînage et des Messages d’action.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-reservation-order-tracking-and-action-messaging"></a><a name="design-details-reservation-order-tracking-and-action-messaging"></a><a name="design-details-reservation-order-tracking-and-action-messaging"></a>Détails de conception : réservation, chaînage et message d’action
Le système de réservation est complet et inclut les fonctionnalités étroitement liées et parallèles du Chaînage et des Messages d’action.  

 Au cœur du système de réservation se trouve la liaison entre une écriture de demande et une écriture d’offre correspondante, que ce soit via une réservation ou un chaînage. Une réservation est un lien généré par l’utilisateur, alors qu’un enregistrement de chaînage est un lien généré par le système. Une quantité d’articles entrée dans le système de réservation est réservée ou chaînée, mais pas les deux à la fois. La manière dont les systèmes traitent un article dépend de la manière dont l’article est configuré.  

 Le système de réservation interagit avec le système de planification en créant des messages d’action sur les lignes planning pendant les exécutions de planification. Un message d’action peut être considéré comme un ajout à un enregistrement de chaînage. Les messages d’action, s’ils sont créés dynamiquement dans le chaînage ou lors de l’exécution de la planification, offrent un outil de choix pour une planification efficace de l’approvisionnement.  

> [!NOTE]  
>  Les quantités réservées sont ignorées par le système de planification., c.-à-d., le lien fixe qui est effectué entre la demande et l’approvisionnement ne peut pas être modifié par le biais de la planification.  

 Le système de réservation forme également la base structurelle du système de traçabilité. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="reservation"></a><a name="reservation"></a><a name="reservation"></a>Réservation
 Une réservation est un lien ferme qui connecte une demande spécifique à un approvisionnement spécifique. Ce lien affecte directement la transaction d’inventaire ultérieure et garantit la bonne application des écritures article à des fins de coûts. Une réservation remplace le mode d’évaluation du stock par défaut d’un article. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-tracking.md).  

 La page **Réservation** est accessible à partir de toutes les lignes d’ordre à la fois des types demande et approvisionnement. Sur la page, l’utilisateur peut spécifier avec quelle écriture demande ou approvisionnement créer un lien réservation. La réservation comporte deux enregistrements qui partagent le même numéro de séquence. Un enregistrement contient un signe négatif et pointe vers la demande. L’autre enregistrement a un signe positif et pointe vers l’approvisionnement. Ces enregistrements sont stockés dans la table **Écriture réservation** avec la valeur d’état **Réservation**. L’utilisateur peut afficher toutes les réservations sur la page **Écritures réservation**.  

### <a name="offsetting-in-reservations"></a><a name="offsetting-in-reservations"></a><a name="offsetting-in-reservations"></a>Compensation dans les réservations
 Les réservations sont effectuées par rapport aux quantités disponibles article. La disponibilité article est calculée en termes de base comme suit :  

 quantité disponible = stock + réceptions planifiées - besoins bruts  

 Le tableau suivant montre les détails des entités réseau d’ordres qui font partie du calcul de disponibilité.  

||Champ dans T27|Table source|Filtre table|Champ origine|  
|-|------------------|------------------|------------------|------------------|  
|**Stocks**|Stocks|Écriture comptable article|N/A|Quantité|  
|**Réceptions planifiées**|Récep. ordre plan. ferme (qté)|Ligne O.F.|=Planifié ferme|Quantité restante (base)|  
|**Réceptions planifiées**|Réception ordre lancé (qté)|Ligne O.F.|=Lancé|Quantité restante (base)|  
|**Réceptions planifiées**|Qté sur ordre d’assemblage|En-tête d’assemblage|=Ordre|Quantité restante (base)|  
|**Réceptions planifiées**|Qté sur commande achat|Ligne achat|=Ordre|Quantité ouverte (base)|  
|**Réceptions planifiées**|Réception transfert (qté)|Ligne transfert|N/A|Quantité restante|  
|**Besoins brut**|Qté sur commande vente|Ligne vente|=Ordre|Quantité ouverte (base)|  
|**Besoins brut**|Besoin planifié (qté)|Composant O.F.|<>Simulé|Quantité restante (base)|  
|**Besoins brut**|Qté sur composant d’assemblage|Ligne assemblage|=Ordre|Quantité restante (base)|  
|**Besoins brut**|Expédition transfert (qté)|Ligne transfert|N/A|Quantité restante|  

 Pour plus d’informations, voir [Détails de conception : disponibilité dans l’entrepôt](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a><a name="manual-reservation"></a><a name="manual-reservation"></a>Réservation manuelle
 Lorsqu’un utilisateur crée une réservation intentionnellement, l’utilisateur gagne la propriété complète et la responsabilité et de ces articles. Cela signifie que l’utilisateur doit également modifier manuellement ou annuler une réservation. Ces modifications manuelles peuvent entraîner la modification automatique des réservations impliquées.  

 Le tableau suivant montre quand apparaissent les modifications et lesquelles :  

|Action de l’utilisateur|Réaction du système|  
|-----------------|---------------------|  
|Diminution de la quantité réservée|Les champs de quantité associés sont mis à jour.|  
|Modification des champs date|Les champs de date associés sont mis à jour.<br /><br /> **Remarque :** si la date d’échéance sur une demande est modifiée pour précéder la date d’expédition ou la date d’échéance de l’approvisionnement, la réservation est annulée.|  
|Suppression de la commande.|La réservation est annulée.|  
|Modification du magasin, de l’emplacement, de la variante, du numéro de série ou numéro de lot|La réservation est annulée.|  

> [!NOTE]  
>  La fonctionnalité Lien tardif peut également modifier des réservations sans informer l’utilisateur, en remaniant des réservations non spécifiques de numéros de série ou de lot. Pour plus d’informations, reportez-vous à « Détails de conception : traçabilité et réservations ».  

### <a name="automatic-reservations"></a><a name="automatic-reservations"></a><a name="automatic-reservations"></a>Réservations automatiques
 La fiche article peut être configurée pour être toujours réservée automatiquement à partir de la demande, par exemple, des commandes vente. Dans ce cas, la réservation est effectuée par rapport au stock, aux commandes achat, aux ordres d’assemblage et aux ordres de fabrication. Un avertissement est émis si l’approvisionnement est insuffisant.  

 De plus, les articles sont réservés automatiquement par diverses fonctions de planification afin de suivre une demande liée à un approvisionnement spécifique. Les écritures chaînage de ces liens de planification contiennent **Réservation** dans le champ **État de la réservation** dans la table **Écriture réservation**. Les réservations automatiques sont créées dans les cas suivants :  

-   Ordre de fabrication multi-niveaux où le champ **Mode de lancement** des articles enfants et parents associés est défini sur **Fabrication à la commande**. Le système de planification crée des réservations entre l’ordre de fabrication parent et les ordres de fabrication sous-jacents pour s’assurer qu’ils sont traités ensemble. Un tel lien de réservation remplace la méthode par défaut d’évaluation du stock et de lettrage de l’article.  

-   Un ordre de fabrication, un assemblage ou une commande achat dont le champ **Méthode réapprovisionnement** de l’article concerné est défini sur **Commande**. Le système de planification crée des réservations entre la demande et l’approvisionnement planifié pour s’assurer que l’approvisionnement spécifique est créé. Pour plus d’informations, reportez-vous à [Commande](design-details-handling-reordering-policies.md#order).  

-   Un ordre de fabrication créé à partir d’une commande vente avec la fonction **Planification commande vente** est lié à la commande vente avec une réservation automatique.  

-   Un ordre d’assemblage créé automatiquement pour une ligne commande vente afin de correspondre à la quantité dans le champ **($ T_37_900 Qty. to Assemble to Order $)**. Cette réservation automatique lie la demande de vente et l’approvisionnement d’assemblage afin que les préparateurs de commande puissent personnaliser et assurer l’élément d’assemblage directement au client. En outre, la réservation lie le résultat d’assemblage à la ligne commande vente via l’activité d’expédition qui répond à la commande client.  

 Dans le cas d’un approvisionnement ou d’une demande sans affectation, le système de planification affecte automatiquement l’état de réservation de type **Excédent**. Cela peut être le résultat de la demande qui est due aux quantités prévues ou des paramètres de planification saisis par l’utilisateur. Il s’agit du surplus légitime, que le système reconnaît, et cela ne provoque pas les messages d’action. Un excédent peut également être véritable, un excédent d’approvisionnement ou une demande qui reste non chaînée. Il s’agit d’une mention d’un déséquilibre dans le réseau d’ordres, qui conduit le système à émettre des messages d’action. Notez qu’un message d’action qui propose une modification de quantité fait toujours référence au type **Excédent**. Pour plus d’informations, reportez-vous à la section « Exemple : chaînage dans les ventes, production et transferts » de cette rubrique.  

 Les réservations automatiques qui sont créées lors de l’exécution de la planification sont traitées comme suit :  

-   Elles sont appliquées par rapport aux quantités d’article qui font partie du calcul de disponibilité, comme les réservations manuelles. Pour plus d’informations, voir la section « Compensation dans les réservations » de cette rubrique.  

-   Elles sont incluses et potentiellement modifiées dans les séries de planification ultérieures, contrairement aux articles réservés manuellement.  

## <a name="order-tracking"></a><a name="order-tracking"></a><a name="order-tracking"></a>Chaînage
 Le chaînage aide le gestionnaire à conserver un programme d’approvisionnement valide en fournissant un aperçu du décalage entre la demande et l’approvisionnement dans le réseau d’ordres. L’enregistrement de chaînage sert de base pour créer les messages d’action dynamiques et les propositions ligne planning lors de l’exécution de la planification.  

> [!NOTE]  
>  Le système de chaînage compense le stock disponible à mesure que les commandes sont saisies dans le réseau d’ordres. Cela implique que le système ne priorise pas les commandes qui peuvent être plus urgentes en termes de date d’échéance. C’est à la logique du système de planification ou à la sagesse du gestionnaire de réorganiser les priorités d’une manière explicite.  

> [!NOTE]  
>  La stratégie de suivi des commandes et la fonction Obtenir les messages d’action ne sont pas intégrées aux projets. Cela signifie qu’une demande liée à un projet n’est pas automatiquement suivie. Étant donné qu’il n’est pas suivi, il peut entraîner l’utilisation d’un réapprovisionnement existant avec suivi des informations de projet sur une autre demande, par exemple, une commande vente. Par conséquent, vous pouvez rencontrer la situation dans laquelle les informations sur le stock disponible ne sont pas synchronisées.  

### <a name="the-order-network"></a><a name="the-order-network"></a><a name="the-order-network"></a>Le Réseau d’ordres
 Le système de chaînage est basé sur le principe que le réseau d’ordres doit toujours être dans un état d’équilibre, dans lequel chaque demande qui entre dans le système est compensée par un approvisionnement correspondant et vice versa. Le système fournit ceci en identifiant les liens logiques entre toutes les écritures de de mande et d’approvisionnement dans le réseau de commandes.  

 Ce principe implique qu’un changement dans une demande entraîne un déséquilibre correspondant du côté de l’approvisionnement du réseau d’ordres. Inversement, une modification d’approvisionnement entraîne un déséquilibre correspondant du côté de la demande du réseau d’ordres. En réalité, le réseau d’ordres se trouve dans un état de flux constant tant que les utilisateurs saisissent, modifient et suppriment des commandes. Le chaînage traite les commandes dynamiquement, en réagissant à chaque modification au moment où elle entre dans le système et devient une partie du réseau d’ordres. Dès que de nouveaux enregistrements de chaînage sont créés, le réseau d’ordres est équilibré, mais uniquement jusqu’à la prochaine modification.  

 Pour augmenter la transparence des calculs dans le système de planification, la page **Éléments planning non chaînés** affiche les quantités non suivies, qui représentent la différence de quantité entre la demande connue et l’approvisionnement proposé. Chaque ligne de la page fait référence à la cause de l’excédent, par exemple, **Commande ouverte**, **Stock de sécurité**, **Qté fixe de commande**, **Qté minimum commande**, **Arrondi** ou **Seuil**.  

### <a name="offsetting-in-order-tracking"></a><a name="offsetting-in-order-tracking"></a><a name="offsetting-in-order-tracking"></a>Compensation dans le chaînage
 Contrairement aux réservations, qui ne peuvent être exécutées que pour des quantités d’article disponibles, le chaînage est possible sur toutes les entités réseau de commande qui sont incluses dans le calcul des besoins nets du système de planification. Les besoins nets sont calculés comme suit :  

 besoins nets = besoins bruts + point de commande - réceptions planifiées - réceptions prévues - stock prévisionnel  

> [!NOTE]  
>  Une demande liée aux paramètres de prévisions ou de planification n’est pas chaînée.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a><a name="example-order-tracking-in-sales-production-and-transfers"></a><a name="example-order-tracking-in-sales-production-and-transfers"></a>Exemple : chaînage dans les ventes, production et transferts
 Le scénario suivant montre les écritures chaînage qui sont créées dans la table **Écriture réservation** suite à diverses modifications du réseau d’ordres.  

 Prenez l’exemple des données suivantes pour deux articles configurés pour le chaînage.  

|Article 1|Name|« Composant »|
|-|-|-|
||Disponibilité|100 unités dans le magasin WEST<br /><br />- 30 unités de LOTA<br />- 70 unités de LOTB|  
|Article 2|Name|« Article produit »|
||Nomenclature de production|1 quantité par « Composant »|  
||demande|Vente de 100 unités au magasin EAST|  
||Approvisionnement|Ordre de fabrication lancé (généré à l’aide de la fonction **Planification commande vente** pour la vente de 100 unités)|  

Sur la page **Paramètres production**, le champ **Mag. composant par déf.** est défini sur **ROUGE**.

 Les écritures de chaînage suivantes existent dans la table **Écriture réservation**, en fonction des données de la table.  

 ![Premier exemple d’écritures chaînage dans la table Écriture réservation.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### <a name="entry-numbers-8-and-9"></a><a name="entry-numbers-8-and-9"></a><a name="entry-numbers-8-and-9"></a>Numéros d’écriture 8 et 9
 Pour le besoin composant de LOTA et de LOTB respectivement, des liens traçabilité commande sont créés entre la demande dans la table 5407, **Composant O.F.**, et l’approvisionnement dans la table 32, **Écriture comptable article**. Le champ **État de la réservation** contient **Traçabilité** pour indiquer que ces écritures sont des liens traçabilité commande dynamiques entre l’approvisionnement et la demande.  

> [!NOTE]  
>  Le champ **N° lot** est vide sur les lignes demande, parce que les numéros de lot ne sont pas spécifiés sur les lignes composant de l’ordre de fabrication lancé.  

### <a name="entry-numbers-10"></a><a name="entry-numbers-10"></a><a name="entry-numbers-10"></a>Numéros d’écriture 10
 Depuis la demande vente dans la table 37, **Ligne vente**, un lien de chaînage est créé avec l’approvisionnement dans la table 5406, **Ligne O.F.**. Le champ **État de la réservation** contient **Réservation**, et le champ **Lien** indique **Ordre pour ordre**. Ceci est dû au fait que l’ordre de fabrication émis a été généré spécifiquement pour la commande vente et doit rester lié contrairement aux liens de suivi de commande avec le statut de réservation **Traçabilité**, qui sont créés et modifiés de façon dynamique. Pour plus d’informations, voir la section « Réservations automatiques » de cette rubrique.  

 A ce stade dans ce scénario, les 100 unités de LOTA et LOTB sont transférées au magasin EAST par un ordre de transfert.  

> [!NOTE]  
>  Seule l’expédition de l’ordre de transfert est validée à ce stade, mais pas la réception.  

 À présent, les écritures de chaînage suivantes existent dans la table **Écriture réservation**.  

 ![Deuxième exemple d’écritures chaînage dans la table Écriture réservation.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### <a name="entry-numbers-8-and-9-1"></a><a name="entry-numbers-8-and-9-1"></a><a name="entry-numbers-8-and-9-1"></a>Numéros d’écriture 8 et 9
 Les écritures chaînage pour les deux lots du composant correspondant à la demande dans la table 5407 sont modifiées d’un statut de réservation **Traçabilité** à **Excédent**. La raison est que les approvisionnements qui ont été liés précédemment, dans la table 32, ont été utilisés par l’expédition de l’ordre de transfert.  

 Un excédent véritable, comme dans ce cas, reflète un excédent d’approvisionnement ou de demande qui reste non chaîné. Il s’agit d’une indication de déséquilibre dans le réseau d’ordres, qui génère un message d’action par le système de planification, sauf s’il est résolu de façon dynamique.  

### <a name="entry-numbers-12-to-16"></a><a name="entry-numbers-12-to-16"></a><a name="entry-numbers-12-to-16"></a>Numéros d’écriture 12 à 16
 Dans la mesure où les deux lots du composant sont validés sur l’ordre de transfert comme réceptionnés mais non acceptés, toutes les écritures chaînage positives associées sont du type de réservation **Excédent**, indiquant qu’elles ne sont affectées à aucune demande. Pour chaque numéro de lot, une écriture est liée au tableau 5741, **Ligne transfert**, et une écriture est liée à l’écriture comptable article au magasin transit où les articles sont disponibles à présent.  

 A ce stade dans ce scénario, l’ordre de transfert des composants du magasin EAST vers le magasin WEST est validé comme étant reçu.  

 À présent, les écritures de chaînage suivantes existent dans la table **Écriture réservation**.  

 ![Troisième exemple d’écritures chaînage dans la table Écriture réservation.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 Les écritures chaînage sont similaires à présent au premier point dans ce scénario, avant la validation de l’ordre de transfert comme expédié uniquement, sauf que les écritures du composant ont à présent le statut de réservation **Excédent**. Ceci est dû au fait que le besoin de composant est toujours au magasin WEST, reflétant ainsi que le champ **Code magasin** de la ligne composant de l’ordre de fabrication. **WEST** tel que configuré dans le champ de configuration **Mag. composant par déf.**. L’approvisionnement qui a été affecté à cette demande auparavant a été transféré au magasin EAST et ne peut pas être entièrement suivi à moins que le besoin de composant de la ligne O.F. ne soit modifié sur magasin EAST.  

 À ce stade dans ce scénario, le **Code magasin** de la ligne O.F. est défini sur **EAST**. En outre, sur la page **Lignes traçabilité**, les 30 unités de LOTA et les 70 unités de LOTB sont affectées à la ligne O.F.  

 À présent, les écritures de chaînage suivantes existent dans la table **Écriture réservation**.  

 ![Quatrième exemple d’écritures chaînage dans la table Écriture réservation.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### <a name="entry-numbers-21-and-22"></a><a name="entry-numbers-21-and-22"></a><a name="entry-numbers-21-and-22"></a>Numéros d’écriture 21 et 22
 Comme le besoin composant a été modifié au magasin EAST, et que l’approvisionnement est disponible comme écritures comptables article au magasin EAST, toutes les écritures chaînage pour les deux numéros de lot sont à présent entièrement suivis, comme indiqué par le statut **Traçabilité**de la réservation.  

 Le champ **N° lot** est désormais renseigné dans l’écriture chaînage de la table 5407, car les numéros de lot ont été affectés aux lignes composant O.F.  

 Pour plus d’exemples des écritures traçabilité dans la table **Écriture réservation**, reportez-vous au livre blanc « table Écriture réservation » sur [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (nécessite un login).

## <a name="action-messaging"></a><a name="action-messaging"></a><a name="action-messaging"></a>Messages d’action
 Lorsque le système de suivi d’ordre détecte un déséquilibre dans le réseau d’ordres, il crée automatiquement un message d’action pour en informer l’utilisateur. Les messages d’action sont des appels générés par le système en vue d’une action de l’utilisateur. Ils indiquent les détails du déséquilibre et suggèrent des propositions sur la façon de restaurer l’équilibre dans le réseau d’ordres. Elles sont affichées comme lignes de planification sur la page **Feuille planning** lorsque vous choisissez **Extraire messages d’action**. En outre, des messages d’action s’affichent sur les lignes planning qui sont générés par l’exécution de la planification pour tenir compte des propositions du système de planification sur la façon de rétablir l’équilibre du réseau d’ordres. Dans les deux cas, les propositions sont effectuées sur le réseau d’ordres, lorsque vous choisissez **Traiter messages d’action**.  

 Un message d’action traite un seul niveau de nomenclature à la fois. Si l’utilisateur accepte le message d’action, cela peut produire des messages d’action supplémentaire au niveau de nomenclature suivant.  

 Le tableau suivant montre les messages d’action existants.  

|Message d’action|Désignation|  
|--------------------|---------------------------------------|  
|**Changer qté**|Modifie la quantité d’une commande approvisionnement existante pour couvrir une demande modifiée ou nouvelle.|  
|**Replanifier**|Replanifie la date d’échéance sur un ordre de fabrication existant.|  
|**Replanifier & Changer qté**|Replanifie la date d’échéance et modifie la quantité de l’ordre de fabrication existant.|  
|**Nouveau**|Crée une commande si la demande ne peut pas être satisfaite par l’un des messages d’action précédents.|  
|**Annuler**|Annule un ordre de fabrication existant.|  

 Le système de chaînage essaie toujours de résoudre un déséquilibre dans le réseau d’ordres existant. Si ce n’est pas possible, il émet un message d’action pour créer une nouvelle commande. Voici la liste par ordre de priorité que le système de chaînage utilise lorsqu’il détermine la manière de restaurer le solde. Si une demande supplémentaire est entrée dans le réseau d’ordres, le système cherche à faire un chaînage par les vérifications suivantes :  

1.  Vérifier un approvisionnement excédentaire dans l’enregistrement existant de chaînage de cette demande.  
2.  Vérifier les réceptions prévues et planifiées par ordre de date de réception. La dernière date possible est sélectionnée.  
3.  Vérifier le stock disponible.  
4.  Vérifier si une commande approvisionnement apparaît dans l’enregistrement actuel de chaînage. Si c’est le cas, le système émet un message d’action de type **Modifier** pour augmenter la commande.  
5.  Vérifier qu’aucune commande approvisionnement n’apparaît dans l’enregistrement actuel de chaînage. Si c’est le cas, le système émet un message d’action de type **Nouveau** pour créer une nouvelle commande.  

 Une demande ouverte traverse la liste et compense l’approvisionnement disponible à chaque point. La demande restante est toujours couverte par la vérification 4 ou la vérification 5.  

 Si une sortie dans la quantité demandée se produit, le système de chaînage tente de résoudre le déséquilibre en effectuant les vérifications précédentes dans l’ordre inverse. Cela signifie que les messages d’action existants peuvent être modifiés ou même supprimés, si nécessaire. Le système de chaînage présente toujours le résultat net de ses calculs à l’utilisateur.  

## <a name="order-tracking-and-planning"></a><a name="order-tracking-and-planning"></a><a name="order-tracking-and-planning"></a>Chaînage et planification
 Lorsque le système de planification est exécuté, il supprime tous les enregistrements de suivi de commande et écritures de message d’action existants et les recrée en tant que suggestions de ligne de planification en fonction des paires approvisionnement/demande et priorités. Lorsque l’exécution de la planification a terminé, le réseau d’ordres est en équilibre.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a><a name="planning-system-versus-order-tracking-and-action-messaging"></a><a name="planning-system-versus-order-tracking-and-action-messaging"></a>comparaison entre système de planification et chaînage et message d’action
 La comparaison suivante montre les différences entre les méthodes utilisées par le système de planification pour créer des propositions de ligne planning et les méthodes utilisées par le système de chaînage pour créer les enregistrements de chaînage et les messages d’action.  

-   Le système de planification traite l’ensemble de la configuration de demande et d’approvisionnement d’un article particulier, alors que le chaînage traite la commande qui l’a activé.  

-   Le système de planification traite tous les niveaux de hiérarchie de la nomenclature, alors que le chaînage traite un niveau de nomenclature à la fois.  

-   Le système de planification crée des liens entre la demande et l’approvisionnement en fonction de la date d’échéance prioritaire. Le chaînage crée des liens entre la demande et l’approvisionnement en fonction de la séquence de saisie des commandes.  

-   Le système de planification prend en compte les paramètres de planification, alors que le chaînage non.  

-   Le système de planification crée des liens dans un mode de lots activé par l’utilisateur lorsqu’il équilibre la demande et l’approvisionnement, alors que le chaînage crée des liens automatiquement et de façon dynamique lorsque l’utilisateur saisit les commandes.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
