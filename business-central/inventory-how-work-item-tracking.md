---
title: Affecter des numéros de série et des numéros de lot à des articles aux fins du suivi | Microsoft Docs
description: Vous pouvez ajouter des numéros de série et de lot à n’importe quel document sortant ou entrant, puis afficher les écritures traçabilité validées dans les écritures comptables articles correspondantes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 510958f185f748f1c8d122d2f199e164b7e45fba
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921882"
---
# <a name="work-with-serial-and-lot-numbers"></a>Utiliser les numéros de lot et de série
Vous pouvez affecter des numéros de série et de lot à n’importe quel document sortant ou entrant, puis afficher les écritures traçabilité validées dans les écritures comptables articles correspondantes. Vous effectuez le travail sur la page **Lignes traçabilité** , que vous pouvez ouvrir depuis un document entrant ou sortant.

La matrice des champs de quantité figurant en haut de la page **Lignes traçabilité** affiche les quantités et les sommes des numéros traçabilité qui sont définis dans les lignes. Les quantités doivent correspondre à celles de la ligne document dont les champs **Non défini** sont paramétrés sur 0.

En vue de mesurer les performances, l’application collecte les informations de disponibilité sur la page **Lignes traçabilité** une fois seulement lorsque vous ouvrez la page. Aussi, l’application ne met pas à jour les informations de disponibilité pendant que la page est ouverte, même si des modifications sont apportées dans le stock ou d’autres documents à ce moment.

Les articles portant des numéros de série ou de lot peuvent être suivis en amont et en aval de la chaîne d’approvisionnement. Cela est utile pour l’assurance qualité générale et pour les rappels de produit. Pour plus d’informations, voir [Tracer des articles suivis](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>À propos du prélèvement de numéros de série ou de lot dans l’entrepôt
Le traitement en sortie des numéros de série ou de lot est une tâche fréquente qui est réalisée au cours de différents processus entrepôt.  

Dans certains processus, les articles en stock ne portent aucun numéro de série ou de lot, et le magasinier doit en affecter un nouveau durant le traitement en sortie, généralement à partir d’une souche de numéros prédéfinie.

Dans les processus simples, les articles en stock comportent déjà des numéros de série ou de lot, par exemple affectés pendant le rangement, qui sont transférés automatiquement via toutes les activités entrepôt sortantes sans interaction de la part des magasiniers.

Dans les situations spéciales d’inventaire selon le numéro de lot ou de série, les numéros de série ou de lot spécifiques sont définis sur le document origine, tel qu’une commande vente, que le magasinier doit respecter lors du désenlogement. Cela peut être dû au fait que le client a demandé un lot spécifique au cours du processus de commande. Lorsque le document prélèvement stock ou entrepôt est créé à partir d’un document origine sortant sur lequel les numéros de série ou de lot sont déjà définis, tous les champs de la page **Lignes traçabilité** dans le prélèvement stock sont en lecture seule, à l’exception du champ **Quantité à traiter** . Dans ce cas, les lignes prélèvement stock indiquent les numéros traçabilité sur chaque ligne prélèvement et rangement. La quantité est déjà répartie dans des combinaisons de numéros de série ou lot uniques, car la commande vente spécifie les numéros traçabilité à expédier.  

## <a name="item-tracking-availability"></a>Disponibilité traçabilité
Lorsque vous travaillez avec des numéros de lot et de série, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule les informations de disponibilité pour les numéros de lot et de série et les affiche dans les diverses pages de suivi des articles. Cela vous permet de savoir l’utilisation d’un numéro de lot ou de série sur d’autres documents. Cela réduit les erreurs et incertitudes liées aux doubles affectations.

Sur la page **Lignes traçabilité** , une icône d’avertissement s’affiche dans le champ **Disponibilité n° lot** ou **Disponibilité n° de série** si une partie ou l’ensemble de la quantité sélectionnée est déjà utilisé dans d’autres documents ou si le numéro de lot ou de série est indisponible.

Sur les pages **Liste information n° de lot/n° de série** , **Disponibilité n° de lot/n° de série** et **Traçabilité - Sélectionner écritures** , des informations s’affichent sur la quantité utilisée d’un article. Il s’agit notamment des informations suivantes.

|Champ|Désignation|
|-----|-----------|  
|**Quantité totale**|Nombre total d’articles en stock actuellement|
|**Quantité totale demandée**|Nombre total d’articles demandés qui seront utilisés dans ce document et dans d’autres|
|**Quantité suspendue actuelle**|Nombre d’articles demandés qui seront utilisés dans le document actuel mais non encore consignés dans la base de données|
|**Quantité demandée actuelle**|Nombre d’articles demandés qui seront utilisés dans le document actuel|
|**Quantité totale disponible**|Nombre total d’articles en stock, moins la quantité d’articles demandés dans ce document et dans d’autres (quantité totale demandée), moins la quantité demandée mais non encore consignée dans ce document (quantité suspendue actuelle)|

Si vous travaillez sur la page **Lignes traçabilité** pendant une longue période ou s’il y beaucoup d’activité en lien avec l’article avec lequel vous travaillez, vous pouvez mettre à jour les informations de disponibilité en sélectionnant l’action **Actualiser disponibilité** . En outre, la disponibilité de l’article est automatiquement revérifiée lorsque vous fermez la page afin de confirmer qu’il n’y a pas de problème de disponibilité.

## <a name="to-set-up-item-tracking-codes"></a>Pour configurer les codes traçabilité
Les codes traçabilité reflètent les différents positionnements d’une société par rapport à l’utilisation des numéros de série et de lot pour les articles qu’elle traite.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes traçabilité** , puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau** .
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sur les raccourcis **N° de série** et **N° lot** , définissez des règles de traçabilité par numéros de série et numéros de lot respectivement.  

> [!NOTE]  
>  Si vous souhaitez suivre des articles spécifiques ou des lots spécifiques tout au long de leur durée de vie, vous devez sélectionner les champs **NS - Traçabilité spéc.** et **N° lot - Traçabilité spéc.** , respectivement. Par conséquent, lorsque vous gérez une unité sortante d’un article avec ce code traçabilité, vous devez toujours spécifier le numéro de série existant ou le numéro de lot existant à gérer. Ainsi, lorsque vous vendez une unité de cet article, elle doit être associée à un groupe précis de numéros de série ou à un numéro de lot spécifique dans le stock. Autrement dit, le numéro de série ou le numéro de lot affecté à l’article lors de son entrée en stock doit suivre ce type d’article lors de sa sortie.

Comme ce champ de configuration couvre toutes les transactions réalisables avec cet article, les différents champs Enlogement/Désenlogement sont également sélectionnés. Ces champs n’ont toutefois aucun rapport avec une quelconque application dans le stock ; ils définissent simplement le flux de travail de votre société en ce qui concerne le moment de l’affectation des numéros traçabilité.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Pour configurer des règles d’expiration pour les numéros de série ou de lot  
Pour certains articles, vous pouvez configurer des règles et des dates d’expiration spécifiques dans le code traçabilité. Cette fonctionnalité permet d’effectuer le suivi de la date d’expiration de numéros de série et de lot spécifiques.

1. Sélectionnez un code traçabilité existant, puis sélectionnez l’action **Modifier** .  
2.  Sur le raccourci **Divers** , activez les cases à cocher suivantes.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Date expiration stricte**|Spécifie qu’une date d’expiration affectée au numéro traçabilité lors de son entrée dans le stock doit être respectée lors de sa sortie du stock.|  
    |**Date expiration manuelle requise**|Spécifie que vous devez saisir une date d’expiration dans la ligne traçabilité.|  
    |**Ignorer les dates d’expiration**|Indique que vous ne souhaitez pas calculer les dates d’échéance. |  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Pour configurer des garanties pour les numéros de série ou de lot  
Pour certains articles, vous souhaitez peut-être configurer des garanties spécifiques dans le code traçabilité. Cette fonctionnalité vous permet d’effectuer le suivi de la date d’expiration des garanties concernant des numéros de série ou de lot spécifiques de votre stock.        
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes traçabilité** , puis sélectionnez le lien associé.  

1. Sélectionnez un code traçabilité existant, puis sélectionnez l’action **Modifier** .  
2.  Sur le raccourci **Divers** , renseignez le champ **Formule date garantie** , puis activez la case à cocher comme indiqué ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Formule date garantie**|Indique le dernier jour de garantie pour l’article.|  
    |**Date garantie requise**|Indique que vous devez saisir une date de garantie dans la ligne traçabilité.|  

## <a name="to-record-serial-or-lot-number-information"></a>Pour enregistrer des informations relatives au numéro de série ou de lot  
Vous pouvez lier des informations particulières à un numéro traçabilité, par exemple pour l’assurance qualité, sur une fiche informations de numéro de série/lot.

1. Ouvrez un document qui comporte des numéros de série ou de lot affectés.
2. Ouvrez la page **Lignes traçabilité** du document.
3. Sélectionnez, par exemple, l’action **Fiche information n° de série** .  

    Les champs **N° de série** et **N° lot** sont préremplis à partir de la ligne traçabilité.  
4. Entrez des informations courtes dans le champ **Description** , par exemple sur l’état de l’article.  
5. Sélectionnez l’action **Commentaire** pour créer un enregistrement de commentaire distinct.  
6. Sélectionnez le champ **Bloqué** pour exclure l’ancien numéro de lot ou de série de toutes les transactions.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Pour modifier des informations relatives au numéro de série ou de lot  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles** , puis sélectionnez le lien associé.  
2. Sélectionnez un article qui comporte un code traçabilité et des informations de numéro de série ou de lot.
3. Sur la page **Fiche article** , choisissez l’action **Écritures** , puis choisissez **Écritures comptables** .
4. Cliquez sur le champ **N° lot** ou **N° de série** . S’il existe des informations en relation avec ce numéro de traçabilité article, alors la page **Liste information n° lot** ou **Liste information n° de série** s’ouvre.  
5. Sélectionnez une fiche, puis choisissez l’action **Fiche information n° lot/série** .  
6. Modifiez le texte court de description, l’enregistrement de commentaire ou le champ **Bloqué** .  

Vous ne pouvez pas modifier les numéros de série ou de lot ni les quantités. Pour ce faire, vous devez reclasser l’écriture comptable article concerné. Pour plus d’informations, consultez [Pour reclasser des numéros de lot ou de série](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Pour affecter des numéros de série ou de lot lors d’une transaction entrante  
Les sociétés peuvent également effectuer le suivi des articles dès leur arrivée dans la société. Dans ce cas, la commande achat constitue souvent le document principal, mais la traçabilité peut être effectuée à partir de tout document entrant. Les écritures comptables qui lui sont associées s’affichent alors dans les écritures comptables article correspondantes.  

Pour définir les règles exactes de traitement des numéros traçabilité pour votre société, utilisez la page **Fiche Code traçabilité** .  

> [!NOTE]  
>  Pour utiliser les numéros de traçabilité dans les activités entrepôt, les champs de configuration **N° lot - Traçabilité entrepôt** et **NS - Traçabilité entrepôt** doivent être sélectionnés car ils définissent les principes de gestion des numéros de série et de lot dans les activités entrepôt.  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat** , puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne document appropriée et dans le raccourci **Lignes** , sélectionnez l’action **Ligne** , puis l’action **Lignes traçabilité** .  

    Vous pouvez affecter des numéros de série ou de lot. Pour cela, il existe plusieurs méthodes :  

    -   Automatiquement, en choisissant **Affecter n° de série** ou **Affecter n° lot** pour affecter des numéros de série/lot issus de souches de numéros prédéfinies.  
    -   Automatiquement, en choisissant **Créer n° de série personnalisé** pour affecter des numéros de série/lot en fonction des souches de numéros définies spécifiquement pour les articles livrés.  
    -   Manuellement, en entrant les numéros de série ou de lot (par exemple, les numéros fournisseur).  
    -   Manuellement, en affectant un numéro spécifique à chaque article.  

3. Pour affecter automatiquement, choisissez l’action **Créer n° de série personnalisé** .  
4. Dans le champ **N° de série perso.** , entrez le numéro de départ d’une souche de numéros de série descriptifs, par exemple **N° série-Fourn0001** .  
5. Dans le champ **Incrément** , entrez 1 afin que la valeur des numéros augmente de un en un.  

    Le champ **Quantité à créer** affiche la quantité de lignes par défaut ; vous pouvez la modifier.  

6. Cochez la case **Créer nouv. n° lot** pour organiser les nouveaux numéros de série dans un lot distinct.  
7. Cliquez sur le bouton **OK** .  

Un numéro de lot avec différents numéros de série est créé en fonction de la quantité d’articles de la ligne document, en commençant par **N° série-Fourn0001** .  

La matrice des champs de quantité figurant dans l’en-tête du formulaire affiche de façon dynamique les quantités et les sommes des numéros traçabilité que vous définissez sur la page. Les quantités doivent correspondre à celles de la ligne document dont les champs **Non défini** sont paramétrés sur 0.  

Lorsque le document est validé, les écritures traçabilité sont basculées vers les écritures comptables articles correspondantes.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Pour affecter un numéro de série ou de lot lors d’une transaction sortante  
Il existe deux méthodes pour ajouter des numéros de série et de lot aux transactions sortantes :  

-   Effectuer une sélection parmi les numéros de série ou de lot existants. Cela s’applique lorsque des numéros traçabilité ont été affectées au cours d’une transaction entrante. Pour plus d’informations, voir [Pour effectuer une sélection parmi les numéros de série et de lot existants](inventory-how-work-item-tracking.md#to-select-from-existing-serial-or-lot-numbers).
-   Affecter des numéros de série ou de lot lors de transactions sortantes Cela s’applique lorsque des numéros traçabilité ne sont pas affectés à des articles jusqu’à ce qu’ils soient vendus et prêts à être expédiés.  

Les différentes règles pour les numéros traçabilité sont définis sur la page **Fiche code traçabilité** .  

> [!NOTE]  
>  Pour affecter des numéros traçabilité dans les activités entrepôt, les champs **NS - Traçabilité entrepôt** et **N° lot - Traçabilité entrepôt** doivent être sélectionnés sur la fiche code de la traçabilité de l’article.    

1. Sélectionnez la ligne document appropriée et dans le raccourci **Lignes** , sélectionnez l’action **Commande** , puis l’action **Lignes traçabilité** .  

    Vous pouvez affecter des numéros traçabilité. Pour cela, il existe plusieurs procédures :  
    -   Automatiquement, de la souche de numéros prédéfinies : sélectionnez l’action **Affecter n° de série** ou **Affecter n° de lot** .  
    -   Automatiquement, en fonction des paramètres définis spécifiquement pour les articles sortants : sélectionnez l’action **Créer n° de série personnalisé** .  
    -   Manuellement, en entrant des numéros de série ou de lot sans utiliser de souches de numéros.  

2.  Pour cette procédure, affectez automatiquement un numéro de série en choisissant **Affecter n° de série**  

    Le champ **Quantité à créer** affiche la quantité de lignes par défaut ; vous pouvez la modifier.  
3.  Sélectionnez le champ **Créer nouv. n° lot** pour organiser les nouveaux numéros de série dans un lot distinct.  
4.  Cliquez sur le bouton **OK** pour créer un numéro de lot et de nouveaux numéros de série en fonction de la quantité d’articles à traiter sur la ligne document correspondante.  

La matrice des champs de quantité figurant en haut affiche de façon dynamique les quantités et les sommes des numéros traçabilité que vous définissez sur la page. Les quantités doivent correspondre à celles de la ligne document dont les champs **Non défini** sont paramétrés sur **0** .  

Lorsque le document est validé, les écritures traçabilité sont basculées vers les écritures comptables articles correspondantes.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Pour effectuer une sélection parmi les numéros de série ou de lot existants  
Lorsque vous travaillez sur des articles nécessitant une traçabilité et que vous créez des transactions sortantes, où les articles sortent du stock, vous devez généralement sélectionner les numéros de lot ou de série de ceux déjà présents dans le stock.  

 Pour définir les règles exactes de traitement des numéros traçabilité pour votre société, utilisez la table **Code traçabilité** .  

> [!NOTE]  
>  Pour pouvoir gérer les numéros traçabilité dans les activités entrepôt, vous devez configurer l’article en activant l’option Traçabilité entrepôt. Cette option détermine en effet les principes spéciaux qui régissent les numéros de série et de lot de l’entrepôt.

1.  Dans un document sortant, sélectionnez la ligne pour laquelle vous souhaitez sélectionner des numéros de série ou de lot.  
2.  Dans le raccourci **Lignes** , sélectionnez l’action **Actions** , sélectionnez l’action **Ligne** ou **Article** , puis sélectionnez l’action **Lignes traçabilité** .  
3.  Sur la page **Lignes traçabilité** , vous disposez de trois options pour spécifier un numéro de lot ou de série :  

    -   Sélectionnez le champ **N° lot** ou **N° de série** , puis sélectionnez un nombre sur la page **Disponibilité traçabilité** .  
    -   Sélectionnez l’action **Sélectionner écritures** . La page **Sélectionner écritures** affiche tous les numéros de lot ou de série en même temps que les informations de disponibilité.

4. Dans le champ **Quantité sélectionnée** , entrez la quantité de chaque numéro de lot ou de série que vous voulez utiliser.   
5. Cliquez sur le bouton **OK**  : les informations de traçabilité de l’article sélectionné sont transférées vers la page **Lignes traçabilité** .  
6. Tapez ou numérisez le numéro de traçabilité.

La matrice des champs de quantité figurant dans l’en-tête du formulaire affiche de façon dynamique les quantités et les sommes des numéros traçabilité que vous définissez sur la page. Les quantités doivent correspondre à celles de la ligne document dont les champs **Non défini** sont paramétrés sur **0** .  

 Lorsque vous validez la ligne document, les informations de traçabilité sont transférées vers les écritures comptables article associées.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Pour traiter les numéros de série et de lot dans les ordres de transfert  
Les procédures de traitement des numéros de série et de lot transférés entre les différents magasins sont similaires à celles qui sont appliquées lorsque les articles sont achetés et vendus.  

Toutefois, l’ordre de transfert est unique dans le sens où l’expédition et la réception sont effectuées à partir de la même ligne transfert et, par conséquent, utilisent la même instance de la page **Lignes traçabilité** . Cela signifie que les numéros traçabilité expédiés d’un magasin doivent être reçus intacts dans l’autre magasin.  

 Pour définir les règles exactes de traitement des numéros traçabilité pour votre société, utilisez la table  **Code traçabilité** .    
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ordres de transfert** , puis sélectionnez le lien associé.  
2.  Ouvrez l’ordre de transfert à traiter. Dans le raccourci **Lignes** , sélectionnez l’action **Ligne** , sélectionnez l’action **Lignes traçabilité** , puis sélectionnez l’action **Expédition** .  
3.  Sur la page **Lignes traçabilité** , affectez ou sélectionnez des numéros de série ou de lot, comme pour toute autre transaction article sortante.  

    En général, lorsque vous traitez les numéros de série et de lot d’articles transfert, les articles possèdent déjà des numéros affectés. La plupart du temps, vous devrez donc procéder à une sélection parmi les numéros de série ou de lot existants.  

4.  Validez l’ordre de transfert (expédition, puis réception) pour enregistrer les articles transférés avec les écritures traçabilité qui leur sont associées.  

Au cours du transfert, la page **Lignes traçabilité** est en lecture seule.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Pour traiter les numéros de série et de lot lors de l’obtention des lignes réception à partir d’une facture achat  
Lorsque vous utilisez la fonctionnalité pour obtenir une réception validée ou des lignes expédition des factures associées et des avoirs, toutes les lignes traçabilité sur les documents entrepôt sont transférées automatiquement, cependant, elles sont traitées d’une manière bien particulière.

La fonctionnalité prend en charge les processus entrants suivants :  
-   **Extraire lignes réception** , à partir d’une facture achat.  
-   **Extraire lignes expéd. retour** , à partir d’un avoir achat.  

La fonctionnalité prend en charge les processus sortants suivants :  
-   **Extraire lignes expédition** , à partir d’une facture vente ou de bons de livraison regroupés.  
-   **Extraire lignes récept. retour** , à partir d’un avoir vente.  

Dans tous ces cas, les lignes traçabilité préexistantes sont automatiquement copiées dans la facture ou l’avoir. La page **Lignes traçabilité** ne permet toutefois pas de changer les numéros de série ou de lot. Seules les quantités peuvent être modifiées.  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat** , puis sélectionnez le lien associé.  
2.  Ouvrez une facture achat pour les articles achetés avec des numéros de série ou de lot.  
3.  À partir d’une ligne facture achat, sur le raccourci **Lignes** , sélectionnez l’action **Extraire lignes réception** .  
4.  Sur la page **Extraire lignes réception** , sélectionnez les lignes réception qui ont des lignes traçabilité, puis cliquez sur le bouton **OK** .  

    Le document origine est copié dans la facture achat comme nouvelle ligne, et ses lignes traçabilité sont quant à elles copiées sur la page **Lignes traçabilité** sous-jacente.  

5.  Dans la facture achat, sélectionnez la ligne réception transférée.  
6.  Sur le raccourci **Lignes** , choisissez l’action **Ligne** , puis choisissez l’action **Lignes traçabilité** pour visualiser les lignes traçabilité.  

La valeur des champs **N° de série** et **N° lot** ne peut pas être modifié. Vous pouvez toutefois supprimer des lignes entières ou modifier les quantités pour refléter les modifications apportées à la ligne origine.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Pour reclasser les numéros de lot ou de série  
Le reclassement de la traçabilité pour un article consiste à remplacer un numéro de lot ou de série par un autre ou à remplacer la date de péremption par une autre. Si vous travaillez avec des lots, vous pouvez fusionner plusieurs lots en un seul. Vous traitez ces tâches à l’aide de la feuille reclassement.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille reclassement article** , puis sélectionnez le lien associé.  
2.  Renseignez la ligne à l’aide des informations appropriées. Pour plus d’informations, voir [Faire l’inventaire à l’aide de documents](inventory-how-count-inventory-with-documents.md) ou [Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md).
3.  Choisissez l’action **Lignes traçabilité** .  
4.  Dans le champ **N° de série** ou **N° lot** , sélectionnez le numéro de série/lot actuel.  
5.  Si vous voulez entrer un nouveau numéro de traçabilité, entrez-le dans le champ **Nouveau n° de série** ou le champ **Nouveau n° lot** . Vous pouvez également fusionner un ou plusieurs lots dans un nouveau lot ou un lot existant.  

    > [!NOTE]  
    >  Notez que lorsque vous reclassez les dates d’expiration, les articles avec les dates d’expiration les plus tôt pour les transactions sortantes sont suggérés en premier. Pour plus d’informations, voir [Prélèvement par FEFO](warehouse-picking-by-fefo.md).  

5.  Si vous voulez entrer une nouvelle date de péremption pour le numéro de lot ou de série, entrez-la dans le champ **Nouvelle date expiration** .  

    > [!IMPORTANT]  
    >  Si vous reclassez un lot sur le même numéro de lot mais une autre date d’expiration, vous devez reclasser le lot entier en utilisant une ligne de feuille reclassement article. Si vous reclassez plusieurs lots sur un nouveau numéro de lot, ce qui signifie que vous fusionnez plusieurs lots en un nouveau lot, vous devez entrer la même date d’expiration pour tous les lots. Si vous reclassez un lot existant sur un autre dont la date d’expiration diffère, vous devez utiliser la date d’expiration du second lot. Si vous laissez le champ **Nouvelle date expiration** vide, le numéro de lot ou de série est reclassé avec une date d’expiration vide.  

6.  Si des informations figurent sur l’ancien numéro de lot ou de série, vous pouvez les copier vers le nouveau numéro de lot ou de série.  

    1.  Sur la page **Lignes traçabilité** , sélectionnez l’action **Informations nouveau n° série** ou l’action **Informations nouveau n° lot** .  
    2.  Pour copier des informations de l’ancien numéro de lot ou de série, sélectionnez l’action sur **Info copie** .  
    3.  Sur la page Liste information, sélectionnez le numéro de lot ou de série à partir duquel vous souhaitez copier, puis choisissez le bouton **OK** .  

7.  Si vous voulez modifier les informations existantes du numéro de lot ou de série, vous pouvez enregistrer des informations de lot ou de série.  
8.  Validez la feuille pour lier les nouveaux numéros traçabilité ou dates d’expiration à l’écriture comptable article qui leur est associée.

## <a name="see-also"></a>Voir aussi
[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)   
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : traçabilité](design-details-item-tracking.md)
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
