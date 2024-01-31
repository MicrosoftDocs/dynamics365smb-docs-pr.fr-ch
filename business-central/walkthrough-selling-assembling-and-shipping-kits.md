---
title: 'Vente, assemblage et expédition de kits'
description: 'Pour prendre en charge un stock juste-à-temps (JIT), des ordres d’assemblage peuvent être créés automatiquement et associés dès que la ligne commande vente est créée.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procédure pas-à-pas : vente, assemblage et expédition de kits

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Pour prendre en charge un stock juste-à-temps (JIT) et permettre la personnalisation des produits conformément aux demandes client, il est possible de créer des ordres d’assemblage et de les lier automatiquement dès que la ligne commande vente est créée. Le lien entre la demande vente et l’approvisionnement d’assemblage permet aux préparateurs de commandes vente de personnaliser l’article d’assemblage et de proposer des dates de livraison en fonction de la disponibilité des composants. En outre, la consommation et le résultat d’assemblage sont validés automatiquement avec l’expédition de la commande vente liée.  

La fonctionnalité spéciale permet de gérer l’expédition des quantités « assembler pour commande », dans des configurations d’entrepôt de base et avancées. Lorsque les travailleurs chargés de l’assemblage finissent d’assembler les pièces ou l’ensemble de la quantité à assembler pour commande, ils l’enregistrent dans le champ **Qté à expédier** de la ligne expédition entrepôt dans les configurations avancées et sélectionnent ensuite **Valider expédition**. Par conséquent, le résultat d’assemblage correspondant est validé, y compris la consommation de composants liée, et une expédition vente de la quantité est validée pour la commande vente liée. Cette procédure pas à pas présente le processus entrepôt avancé.  

Dans les configurations entrepôt de base, lorsqu’une quantité à assembler pour commande est prête à être expédiée, le magasinier responsable valide un prélèvement stock pour les lignes de commande. Cela crée un mouvement stock pour les composants et valide la sortie d’assemblage et l’expédition de la commande. Pour plus d’informations, reportez-vous à [Traitement des articles à assembler pour commande dans les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).  

## À propos de cette procédure pas à pas

Cette procédure pas à pas présente les tâches suivantes :  

### Configuration des articles d’assemblage

Les articles d’assemblage sont caractérisés par leur système de réapprovisionnement et la nomenclature d’assemblage. La stratégie d’assemblage de l’article peut être « assembler pour commande » ou « assembler pour stock ». Cette section couvre les tâches suivantes :  

-   Définition du système de réapprovisionnement et de la stratégie d’assemblage appropriés sur une nouvelle fiche d’article d’assemblage.  
-   Création d’une nomenclature d’assemblage qui répertorie les composants d’assemblage et la ressource incluse dans l’article d’assemblage.  

### Vente d’articles d’assemblage personnalisés

[!INCLUDE[prod_short](includes/prod_short.md)] est flexible et permet d’entrer une quantité en stock et une quantité « assembler pour commande » sur la ligne commande vente. Cette section couvre les tâches suivantes :  

-   Création d’une ligne commande vente purement « assembler pour commande » lorsque la quantité totale n’est pas disponible et doit être réunie avant la livraison.  
-   Personnalisation des articles « assembler pour commande ».  
-   Nouveau calcul du prix unitaire d’un article d’assemblage personnalisé.  
-   Création d’une ligne commande vente mixte à laquelle une partie de la quantité de ventes provient du stock et la partie restante doit être assemblée avant la livraison.  
-   Compréhension des avertissements de disponibilité des articles « assembler pour commande ».  

### Planification pour les articles d’assemblage

L’offre et la demande d’assemblage sont traitées par le système de planification, tout comme pour les achats, les transferts et la production. Cette section couvre les tâches suivantes :  

-   Exécution d’un planning régénératif pour les articles utilisant une demande de vente pour l’approvisionnement assemblé.  
-   Génération d’un ordre d’assemblage en vue de répondre à la quantité de la ligne vente au plus tard à la date livraison demandée.  

### Assemblage des articles

Les ordres d’assemblage fonctionnent d’une manière similaire aux ordres de fabrication, prévoient que la consommation et la production sont enregistrées et validées directement à partir de la commande. Lorsque les articles sont assemblés pour stock, l’ouvrier d’assemblage a un accès total à tous les champs d’en-tête et de ligne. Lorsque les articles sont assemblés pour une commande lorsque la quantité et la date sont promises au client, certains champs de l’ordre d’assemblage ne sont pas modifiables. Dans ce cas, la validation d’assemblage est exécutée à partir de l’expédition entrepôt pour la commande vente liée. Cette section couvre les tâches suivantes.  

-   Enregistrement et validation de consommation d’assemblage et de production dans le stock.  
-   Accès à une ligne expédition entrepôt à partir d’un ordre d’assemblage pour commande pour enregistrer le travail d’assemblage.  
-   Accès à un ordre d’assemblage pour commande à partir d’une ligne expédition entrepôt pour afficher automatiquement les données entrées.  

### Expédition d’articles d’assemblage, à partir du stock et assemblés pour former une commande

Il existe une fonctionnalité spéciale qui permet de gérer l’expédition des quantités à assembler pour commande. Cette section couvre les tâches suivantes :  

-   Création d’un prélèvement entrepôt pour des articles d’assemblage de stock et pour des composants d’assemblage à assembler avant la livraison.  
-   Enregistrement des prélèvements entrepôt pour des composants d’assemblage, puis pour des articles d’assemblage.  
-   Accès à un ordre d’assemblage à partir d’une expédition entrepôt pour afficher des composants sélectionnés ou consommés.  
-   Expédition de quantités « assembler pour commande ».  
-   Expédition d’articles d’assemblage de stock.  

## Rôles

Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   préparateur de commandes vente ;  
-   Planificateur  
-   Ouvrier d’assemblage  
-   Employé en charge du prélèvement  
-   Responsable expédition  

## Conditions préalables

Avant d’exécuter cette procédure pas à pas, veuillez suivre les instructions ci-dessous :  

-   Installez [!INCLUDE[prod_short](includes/prod_short.md)].  
-   Devenez magasinier dans un magasin BLANC en procédant comme suit :  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2.  Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
3.  Dans le champ **Code magasin**, entrez BLANC.  
4.  Sélectionnez le champ **Par défaut**.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Préparez le magasin BLANC pour l’assemblage en procédant comme suit :  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2.  Ouvrez la fiche magasin du magasin BLANC.  
3.  Dans le raccourci **Emplacements**, entrez **W-10-0001** dans le champ **Code empl. vers assemblage**.  

    Lorsque vous entrez ce code emplacement qui n’est pas utilisé pour le prélèvement, toutes les lignes d’ordre d’assemblage sont prêtes à recevoir leurs composants dans l’emplacement.  

4.  Dans le champ **Code empl. depuis assemblage**, entrez **W-01-0001**.  

    Lorsque vous entrez ce code emplacement de prélèvement, des articles d’assemblage finis sont sortis à l’emplacement.  

Supprimez le délai par défaut pour les processus internes en procédant comme suit :  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres production**, puis choisissez le lien associé.  
2.  Sur la page **Paramètres production**, sous le raccourci **Planning**, supprimez la valeur dans le champ **Délai de sécurité par défaut**.  

<!-- Create inventory for assembly components by following [Prepare Sample Data](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).   -->

## Scénario

Le 23 janvier, Susan, préparatrice de commandes vente, accepte une commande de The Device Shop pour trois unités de kit B, c’est-à-dire un article « assembler pour commande ». Les trois unités sont personnalisées et doivent contenir la carte graphique élevée et un bloc de RAM supplémentaire. Les lecteurs de disque sont mis à niveau vers DWD car les lecteurs de CD ne sont pas disponibles. Susan sait que les unités peuvent être assemblées immédiatement, et laisse la date d’expédition suggérée du 23 janvier.  

En même temps, le client commande quinze unités du kit A avec une demande spéciale de cinq unités personnalisées contenant une carte graphique. Même si le kit A est généralement un article « assembler pour stock », le préparateur de commandes combine les quantités des lignes vente pour vendre dix unités du stock et assembler cinq unités personnalisées dans la commande. Les dix unités de kit A ne sont pas disponibles et doivent d’abord être fournies dans le stock par un ordre d’assemblage en fonction de la stratégie d’assemblage de l’article. Susan apprend du département d’assemblage que les unités du kit A ne peuvent pas être fournies pour la semaine en cours. Susan définit la date d’expédition de la deuxième ligne commande vente, pour la quantité « assembler pour commande » et la quantité en stock, sur le 27 janvier et informe le client que les 15 unités du kit A seront expédiées quatre jours après les trois unités du kit B. Pour signaler au département Expédition que cette commande vente requiert un processus d’assemblage, Susan crée le document expédition entrepôt depuis la commande vente.  

Eduardo, planificateur, exécute la feuille planning et génère un ordre d’assemblage pour dix unités standard du kit A avec une date d’échéance interne du 27 janvier.  

Sammy, responsable de l’expédition, obtient trois lignes expédition entrepôt de la commande vente : une ligne pour les trois unités « assembler pour commande » pures, une ligne pour les cinq unités « assembler pour commande » de la ligne commande vente mixte et une ligne pour les dix unités « assembler pour stock » de la ligne commande vente mixte. Sammy crée un document prélèvement entrepôt pour tous les composants d’assemblage qui sont nécessaires pour assembler le total de huit unités « assembler pour commande » dans le document expédition entrepôt.  

Jean, employé en charge du prélèvement, récupère les composants pour toutes les quantités « assembler pour commande » dans le document expédition entrepôt et les apporte à la zone d’assemblage. John indique la quantité d’articles à traiter et enregistre le prélèvement entrepôt.  

Linda assemble les trois unités « assembler pour commande » du kit B. Les composants ont été prélevés, et elle n’enregistre pas les quantités de production et de sortie ou valide la commande, car les deux actions sont effectuées automatiquement via les lignes expédition entrepôt liées.  

Sammy enregistre la quantité assemblée sur la ligne expédition entrepôt et valide l’expédition des trois unités de kit B. La première ligne de la commande vente est mise à jour comme étant expédiée. L’ordre d’assemblage lié reste ouvert jusqu’à ce que la commande vente soit entièrement facturée. Les deux lignes expédition entrepôt, une « assembler pour commande » et une « assembler pour stock », pour le kit A avec des dates d’échéance (27 janvier) toujours ouvertes.  

Le 27 janvier, Linda traite deux ordres d’assemblage pour le kit A. Le premier ordre est la commande ATO de cinq unités, qu’elle traite différemment de la commande ATO pour le kit B qu’elle a traitée le 23 janvier. Dans le cadre de cette commande, Linda est autorisée à accéder à la ligne expédition entrepôt elle-même pour enregistrer le travail d’assemblage accompli. Les composants nécessaires sont prêts dans le département Assemblage, au fur et à mesure qu’ils ont été prélevés avec des composants pour le kit B.  

Le second ordre d’assemblage est l’ordre « assembler pour stock » pour dix unités qui ont été créées par le système de planification. Dans cette commande « assembler pour stock », Linda exécute toutes les actions associées depuis l’ordre d’assemblage. Linda crée un document prélèvement entrepôt pour les composants d’assemblage nécessaires pour assembler les dix unités. Lorsque les ordinateurs sont assemblés, Linda valide l’ordre d’assemblage et signale par conséquent que les articles sont disponibles dans le stock et peuvent être prélevés pour l’expédition.  

Sammy crée un document prélèvement entrepôt pour toutes les quantités qui restent avant que l’expédition entrepôt ne puisse être validée. Un document prélèvement est créé pour les dix unités de kit A juste terminées. Les composants nécessaires pour assembler les cinq unités de kit A à commander ont été prélevés le 23 janvier.  

Jean apporte les dix unités de kit A de l’entrepôt à la zone expédition spécifiée, enregistre la quantité à traiter, puis enregistre le prélèvement.  

Sammy emballe les dix unités « assembler pour stock » avec les cinq unités « assembler pour commande » que Linda a assemblées plus tôt dans la journée. Sammy renseigne la quantité à livrer sur les deux lignes, puis valide la dernière expédition pour The Device Shop. L’ordre d’assemblage lié pour les cinq unités de kit A est automatiquement validé. La seconde ligne de la commande vente est mise à jour comme étant expédiée. Deux ordres d’assemblage liés restent ouverts jusqu’à ce que la commande vente soit facturée et clôturée.  

Lorsque la commande vente est validée ultérieurement comme étant entièrement facturée, la commande vente et les ordres d’assemblage liés sont supprimés.  

## Préparation d’exemples de données

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles article entrepôt**, puis choisissez le lien associé.  
2.  Choisissez le champ **Nom de la feuille**, puis sélectionnez la feuille par défaut.  
3.  Créez des ajustements positifs de stock à un magasin BLANC à la date de travail, le 23 janvier, en entrant les informations suivantes.  

    |**N° article**|**Code zone**|**Code emplacement**|**Quantité**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PRELEVEMT|W-01-0001|20|  
    |80005|PRELEVEMT|W-01-0001|20|  
    |80011|PRELEVEMT|W-01-0001|20|  
    |80014|PRELEV.|W-01-0001|20|  
    |80203|PRELEVEMT|W-01-0001|20|  
    |80209|PRELEVEMT|W-01-0001|20|  

4.  Choisissez l’action **Enregistrer**, puis cliquez sur le bouton **Oui**.  

    Ensuite, synchronisez les nouvelles écritures entrepôt avec le stock.  

5.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles article**, puis choisissez le lien associé. La page **Feuille article** s’ouvre.  
6.  Sélectionnez l’action **Calculer ajustement entrepôt**.  
7.  Sur la page **Calculer ajustement entrepôt**, cliquez sur le bouton **OK** .  
8.  Sur la page **Feuille article**, choisissez l’action **Valider**, puis cliquez sur le bouton **Oui**.  

### Création des articles d’assemblage  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Créez le premier article d’assemblage sur la base des informations suivantes.  

    |Champ|Valeur|  
    |---------------------------------|-----------|  
    |**Description**|Kit A - PC de base|  
    |**Unité de base**|PCS|  
    |**Code catégorie article**|Divers|  
    |**Système réappro.**|Assemblage|  
    |**Stratégie d’assemblage**|Assembler pour stock|  
    |**Méthode de réapprovisionnement**|Lot pour lot|  

    > [!NOTE]  
    >  Le kit A est généralement fourni par assemblage pour le stockage et a donc une méthode de réapprovisionnement pour le faire passer dans la planification générale de l’approvisionnement.  

4.  Choisissez l’action **Assemblage**, puis choisissez **Nomenclature d’élément d’assemblage**.  
5.  Définissez une nomenclature d’assemblage pour le kit A avec les informations suivantes.  

    |**Type**|**N°**|**Quantité par**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Article|80001|1|  
    |Article|80011|1|  
    |Article|80209|1|  
    |Ressource|Linda|1|  

6.  Créez le second article d’assemblage sur la base des informations suivantes.  

    |Champ|Valeur|  
    |---------------------------------|-----------|  
    |**Description**|Kit B - PC pro|  
    |**Unité de base**|PCS|  
    |**Code catégorie article**|Divers|  
    |**Système réappro.**|Assemblage|  
    |**Stratégie d’assemblage**|Assembler pour commande|  

    > [!NOTE]  
    >  Le kit B est généralement fourni par assemblage pour commande et donc n’a pas une méthode de réapprovisionnement, parce qu’il ne doit pas faire partie de la planification générale de l’approvisionnement.  

7.  Choisissez l’action **Assemblage**, puis choisissez **Nomenclature d’élément d’assemblage**.  
8.  Définissez une nomenclature d’assemblage pour le kit B avec les informations suivantes.  

    |**Type**|**N°**|**Quantité par**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Article|80005|1|  
    |Article|80014|1|  
    |Article|80210|1|  
    |Ressource|Linda|1|  

### Vente des articles d’assemblage  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Créez deux lignes commande vente pour le client 62000, The Device Shop, à la date de travail avec les informations suivantes.  

    |**Type**|**Description**|**Quantité**|Qté vers Assembler pour commande|Date de préparation|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Article ;|Kit B - PC pro|3|3|23 janvier|  
    |Article ;|Kit A - PC de base|15|5|27 janvier|  

    > [!NOTE]  
    >  Le problème de disponibilité suivant existe pour la ligne commande vente pour le kit B :  
    >   
    >  -   Le composant d’assemblage 80210 n’est pas disponible. Cela signifie que les trois unités spécifiées de kit B ne peuvent pas être assemblées, indiquées par **0** dans le champ **Capacité d’assembler** sur la page **Disponibilité assemblage**.  
    >   
    >  Le problème de disponibilité suivant existe pour la ligne commande vente pour le kit A :  
    >   
    >  -   Les dix unités de kit A ne sont pas disponibles. Ceci indique au système de planification que la quantité doit être assemblée pour le stock.  

    Ensuite, personnalisez la commande vente.  

4.  Sélectionnez la ligne commande vente pour trois unités de kit B.  
5.  Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande** et **Lignes d’assemblage pour commande**.  
6.  Sur la page **Lignes Assembler pour commande**, sur la ligne d’ordre d’assemblage pour l’article 80014, entrez **2** dans le champ **Quantité par**.  
7.  Sur la ligne d’ordre d’assemblage pour l’article 80210, choisissez le champ **N°** , puis sélectionnez l’article 80209 à la place.  
8.  Créez une ligne ordre d’assemblage à l’aide des informations suivantes.  

    |Type|N°|Quantité par|  
    |----------|---------|------------------|  
    |Article|80203|1|  

9. Fermez la page **Lignes d’assemblage pour commande**.  

    Ensuite, mettez à jour le prix unitaire du kit B en fonction de la personnalisation que vous venez d’exécuter. Prenez note de la valeur actuelle dans le champ **Prix unitaire HT**.  

10. Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande** et **Prix relation**.  
11. Cliquez sur le bouton **Oui**. Prenez note de la valeur augmentée dans le champ **Prix unitaire HT**.  
12. Sélectionnez la ligne commande vente pour 15 unités de kit A.  
13. Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande** et **Lignes d’assemblage pour commande**.  
14. Sur la page **Lignes Assembler pour commande**, créez une ligne ordre d’assemblage à l’aide des informations suivantes.  

    |Type|N°|Quantité par|  
    |----------|---------|------------------|  
    |Article ;|80203|1|  

     Ensuite, modifiez la date d’expédition de la deuxième ligne commande vente selon la planification d’assemblage.  

15. Sur la ligne commande vente de 15 unités du kit A, entrez **01-27-2014** **Date d’expédition**.  
16. Sélectionnez l’action **Lancer**.  
17. Choisissez l’action **Créer expédition entrepôt**.  
18. Fermez la commande vente.  

### Planification pour les articles « assembler pour stock » non disponibles  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille planning**, puis choisissez le lien associé.  
2.  Choisissez l’action **Calculer planning régénératif**.  
3.  Sur la page **Calculer planning**, définissez les filtres suivants.  

    |Date de début|Date de fin|N°|  
    |-------------------|-----------------|---------|  
    |23-01-2014|27-01-2014|Kit A - PC de base|  

4.  Cliquez sur le bouton **OK**.  

    Une nouvelle ligne planning est créée pour l’ordre d’assemblage nécessaire de dix unités, dû le 27 janvier. Elle n’a besoin d’aucune modification ; vous pouvez créer la commande.  

5.  Choisissez l’action **Traiter message d’action**.  
6.  Sur la page **Traiter messages d’action**, choisissez le champ **Ordre d’assemblage**, puis sélectionnez **Créer des ordres d’assemblage**.  
7.  Cliquez sur le bouton **OK**.  

### Assemblage et expédition de la première quantité « assembler pour commande »  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expédition entrepôt**, puis choisissez le lien associé.  

    > [!NOTE]  
    >  Dans cette section, la personne responsable de l’expédition est chargée d’enregistrer le travail d’assemblage « assembler pour commande » effectué sur la ligne expédition entrepôt. Ce flux de travail peut apparaître dans des environnements où le travail d’assemblage est effectué par la personne responsable de l’expédition ou par des ouvriers d’assemblage dans l’emplacement expédition.  
    >   
    >  Dans cette section, des actions de l’ordre d’assemblage sont exécutées indirectement à partir de la ligne expédition entrepôt. Pour plus d’informations sur la manière de traiter un ordre d’assemblage directement, reportez-vous à la section « Assemblage d’articles pour le stock » dans cette procédure pas à pas.  

2.  Ouvrez l’expédition entrepôt la plus récente créée à un magasin BLANC.  

    Remarquez les trois lignes expédition entrepôt : une ligne pour la quantité ATO du kit B, dû le 23 janvier. Une ligne pour la quantité ATO du kit A, dû le 27 janvier. Une ligne pour la quantité de stock du kit A, dû le 27 janvier.  

    Le champ **Assembler pour commande** spécifie la méthode d’assemblage.

    Ensuite, créez un document prélèvement pour tous les composants d’assemblage « assembler pour commande » nécessaires pour l’expédition entrepôt.  

3.  Choisissez l’action **Créer prélèvement**, puis cliquez sur le bouton **OK**.  

    Ensuite, effectuez la tâche de la personne en charge du prélèvement.  

4.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements**, puis choisissez le lien associé.  
5.  Ouvrez le document prélèvement entrepôt que vous avez créé à l’étape 3 de cette section.  

    Prenez note de la valeur du champ **Document origine** et que toutes les lignes prélèvement sont pour les composants d’assemblage.  

    Ensuite, enregistrez le prélèvement sans modifier les informations par défaut.  

6.  Choisissez l’action **Remplir qté à traiter**.  
7.  Choisissez l’action **Enregistrer prélèvement**.  

    Revenez à l’exécution des tâches d’expédition.  

8.  Rouvrez la page **Expédition entrepôt**.  

    Notez que le champ **Qté prélevée** est toujours blanc sur toutes les lignes. Ceci est dû au fait que vous n’avez toujours pas prélevé les articles à expédier, mais uniquement les composants nécessaires pour assembler les quantités « assembler pour commande ».  

    Révisez l’ordre d’assemblage lié.  

9. Sélectionnez la ligne expédition pour trois unités de kit B.  
10. Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande**. La page **Ordre d’assemblage** s’ouvre.  

    Notez que plusieurs champs de l’ordre d’assemblage ne sont pas disponibles parce que la commande est liée à une commande vente.  

    Notez sur les lignes ordre d’assemblage que le champ **Qté prélevée** est renseigné. Ceci est dû au prélèvement que vous avez enregistré à l’étape 7 de cette section.  

11. Dans le champ **Quantité à assembler**, essayez d’entrer une valeur inférieure à **3**.  

    Lire le message d’erreur expliquant pourquoi ce champ peut uniquement être renseigné par le champ **Qté à expédier** de l’expédition liée.  

    Le champ **Quantité à assembler** est modifiable et permet de prendre en charge des situations où vous voulez expédier partiellement une quantité en stock au lieu d’assembler plus d’unités à la commande. Pour plus d’informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Fermez la page **Ordre d’assemblage** pour revenir à la page **Expédition entrepôt**.  
13. Sur la ligne expédition pour trois unités du kit B, dans le champ **Qté à expédier**, entrez **3**.  
14. Choisissez l’action **Valider expédition**, puis sélectionnez le bouton **Expédier**.  

    Avec cette validation d’expédition entrepôt, l’ensemble de la consommation et des quantités produites de l’ordre d’assemblage lié est validé, et le champ **Quantité restante** est vide. La ligne commande vente pour le kit B est mise à jour pour indiquer que les trois unités sont expédiées.  

    Les activités entrepôt pour répondre à la première ligne commande vente sont effectuées avant le 23 janvier. Ensuite, traitez les lignes commande vente expédiées le 27 janvier  

### Assemblage et enregistrement de la seconde quantité « assembler pour commande »  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Ordres d’assemblage**, puis sélectionnez le lien associé.  

    Remarquez que la commande « assembler pour commande » pour les unités du kit B est toujours dans la liste, bien que le champ **Quantité restante** soit vide. En effet la commande vente liée n’est toujours pas entièrement facturée.  

    > [!NOTE]  
    >  Dans cette section, l’ouvrier d’assemblage est responsable de l’enregistrement du travail d’assemblage « assembler pour commande » effectué sur la ligne expédition entrepôt. Ce flux de travail peut apparaître dans des environnements dans lesquels le travail d’assemblage est effectué dans un département Assemblage séparé et les ouvriers d’assemblage sont autorisés à modifier la ligne expédition entrepôt.  

2.  Ouvrez l’ordre d’assemblage « assembler pour commande » pour cinq unités de kit A.  

    Remarquez que les champs **Quantité à assembler** et **Quantité à consommer** sont vides car aucun travail n’est encore enregistré.  

    Notez sur les lignes ordre d’assemblage que le champ **Qté prélevée** est renseigné. Ceci est dû au prélèvement enregistré le 23 janvier.  

    Ensuite, enregistrez que l’ordre d’assemblage est terminé.  

3.  Choisissez l’action **Ligne expédition entrepôt Assembler pour commande**.  
4.  Sur la page **Ligne expédition entrepôt Assembler pour commande**, dans le champ **Qté à expédier**, entrez **5**, puis fermez la page.  

    Remarquez dans la page **Ordre d’assemblage** que les champs **Quantité à assembler** et **Quantité à consommer** sont renseignés par les quantités de sortie et les quantités consommées qui seront validées avec l’expédition.  

5.  Fermez la page **Ordre d’assemblage**.  

### Assemblage de la quantité « assembler pour stock »  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Ordres d’assemblage**, puis sélectionnez le lien associé.  
2.  Ouvrez l’ordre d’assemblage pour dix unités de kit A.  

    Notez que le champ **Quantité à assembler** est renseigné avec la quantité prévue.  

    Ensuite, créez un document prélèvement pour récupérer les composants nécessaires.  

3.  Sélectionnez l’action **Lancer**.  
4.  Choisissez l’action **Créer prélèvement entrep.**, puis cliquez sur le bouton **OK**.  

    Ensuite, effectuez la tâche de la personne en charge du prélèvement.  

5.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements**, puis choisissez le lien associé.  
6.  Ouvrez le document prélèvement entrepôt que vous avez créé à l’étape 4 de cette section.  

     Enregistrez le prélèvement sans modifier les informations par défaut.  

7.  Choisissez l’action **Remplir qté à traiter**.  
8.  Choisissez l’action **Enregistrer prélèvement**.  

    Revenez à l’ordre d’assemblage pour effectuer la dernière tâche d’assemblage.  

9. Dans **Ordre d’assemblage**, choisissez l’action **Valider**, puis cliquez sur le bouton **Oui**.  

    Remarquez que l’ordre d’assemblage est supprimé de la liste des commandes ouvertes.  

### Expédition des autres articles, en partie du stock et en partie assemblés pour la commande  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expédition entrepôt**, puis choisissez le lien associé.  
2.  Ouvrez l’expédition entrepôt la plus récente créée à un magasin BLANC.  

    Notez que sur la ligne pour les dix unités de kit A les champs **Qté à expédier** et **Qté prélevée** sont vides.  

    Ensuite, prélevez les articles restants.  

3.  Choisissez l’action **Créer prélèvement**, puis cliquez sur le bouton **OK**.  

    Ensuite, effectuez la dernière tâche de la personne en charge du prélèvement pour cette expédition entrepôt.  

4.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements**, puis choisissez le lien associé.  
5.  Ouvrez le document prélèvement entrepôt que vous avez créé à l’étape 3 de cette section.  

    Remarquez que ce document prélèvement concerne l’article d’assemblage, pas les composants d’assemblage.  

    Ensuite, enregistrez le prélèvement sans modifier les informations par défaut.  

6.  Choisissez l’action **Remplir qté à traiter**.  
7.  Choisissez l’action **Enregistrer prélèvement**, puis cliquez sur le bouton **Oui**.  

    Revenez à l’expédition entrepôt pour effectuer la dernière tâche.  

8.  Rouvrez la page **Expédition entrepôt**.  

    Sur la page **Expédition entrepôt**, sur la ligne pour dix unités de kit A, notez que les champs **Qté à expédier** et **Qté prélevée** contiennent désormais la valeur **10**.  

9. Choisissez l’action **Valider expédition**, puis cliquez sur le bouton **Expédier**.  

    Le document expédition entrepôt est supprimé, ce qui indique que les activités entrepôt impliquées sont terminées. Ensuite, vérifiez que la commande vente a été traitée.  

10. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
11. Ouvrez la commande vente pour The Device Shop.  

    Notez que le champ **Quantité expédiée** affiche la quantité totale des deux lignes.  

    Lorsque The Device Shop paie pour la réception des 18 ordinateurs de CRONUS, la commande vente et ses ordres d’assemblage liés sont supprimés.  

## Voir aussi

 [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Assembler des articles](assembly-how-to-assemble-items.md)   
 [Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md)   
 [Assembler des articles](assembly-how-to-assemble-items.md)   
 [Détails de conception : validation d’ordre d’assemblage](design-details-assembly-order-posting.md)   
 [Détails de conception : flux d’entrepôt internes](design-details-internal-warehouse-flows.md)   
 [Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
