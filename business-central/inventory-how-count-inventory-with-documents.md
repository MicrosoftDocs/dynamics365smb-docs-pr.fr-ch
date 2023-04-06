---
title: Inventaire et ajustement du stock
description: Décrit comment compter l’inventaire et utiliser les documents d’inventaire pour ajuster le stock disponible.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/01/2021
ms.author: edupont
---
# Faire l’inventaire et l’ajuster à l’aide de documents

Vous pouvez effectuer l’inventaire d’un stock physique de vos articles à l’aide des documents Commande de stock physique et Enregistrement de stock physique. La page **Commande de stock physique** est utilisée pour organiser le projet d’inventaire complet, par exemple un par magasin. La page **Enregistrement de stock physique** est utilisée pour communiquer et capturer le nombre réel d’articles. Vous pouvez créer plusieurs enregistrements pour une commande, par exemple, pour répartir les groupes d’articles vers différents employés.

L’état **Enregistrement de stock physique** peut être imprimé depuis chaque enregistrement et contient des champs de quantité vides pour saisir l’inventaire. Quand un utilisateur a terminé l’inventaire et quand les quantités sont saisies sur la page **Enregistrement de stock physique**, sélectionnez l’action **Terminer**. Cela transfère les quantités vers les lignes concernées sur la page **Enregistrement de stock physique**. La fonctionnalité s’assure qu’aucun inventaire d’articles ne peut être enregistré à deux reprises.  

> [!NOTE]
> L’utilisation de documents pour effectuer un inventaire offre un plus grand contrôle et prend en charge la répartition de l’inventaire vers plusieurs employés. Vous pouvez également effectuer la tâche à l’aide de feuilles, les pages **Feuilles inventaire** et **Feuilles inventaire entrepôt**. Pour plus d’informations, voir [Inventaire, ajustement et reclassement du stock avec les journaux](inventory-how-count-adjust-reclassify.md). Cet article décrit comment effectuer un inventaire physique à l’aide de documents.
>
> Si vous utilisez des zones, vous ne pouvez pas utiliser de commandes d’inventaire. À la place, utilisez la page **Feuille inventaire entrepôt** pour faire l’inventaire de vos écritures d’entrepôt avant de les synchroniser avec les écritures comptables d’article.

Réaliser l’inventaire à l’aide de documents se produit comme suit :

1. Créez une commande de stock physique avec les quantités d’articles prévus pré-remplies.
2. Générez un ou plusieurs enregistrements de stock physique depuis la commande.
3. Saisissez les quantités d’articles répertoriés sur les enregistrements, comme saisis sur les bordereaux, par exemple, puis sélectionnez le statut **Terminé**.
4. Exécutez et validez la commande de stock physique.

## Pour créer une commande de stock physique

Une commande de stock physique est un document complet composé d’une en-tête de commande de stock physique et de quelques lignes de commande de stock physique. Les informations relatives à une en-tête de stock physique décrivent comment effectuer l’inventaire. Les lignes de commande de stock physique contiennent les informations relatives aux articles et à leurs magasins.

Pour créer les lignes de commande de stock physique, vous utilisez généralement la fonction **Calculer les lignes** pour refléter le stock actuel comme lignes de la commande. Sinon, vous pouvez utiliser la fonction **Copier à partir du document** pour compléter les lignes avec le contenu de toute autre commande de stock physique ouverte ou validée. La procédure suivante décrit uniquement comment utiliser la fonction **Calculer les lignes**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Commandes de stock**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Renseignez les champs requis du raccourci **Général**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Choisissez l’action **Calculer les lignes**.
5. Sélectionnez des options, le cas échéant.
6. Définissez les filtres, par exemple, pour inclure uniquement un sous-ensemble d’articles à comptabiliser avec le premier enregistrement.

    > [!TIP]
    > Pour planifier l’exécution de l’inventaire par plusieurs employés, il est recommandé de définir différents filtres à chaque utilisation de l’action **Calculer les lignes** pour ne remplir que la commande avec le sous-ensemble d’articles de l’inventaire qu’un utilisateur enregistrera. Ainsi, en générant plusieurs enregistrements de stock physique par plusieurs employés, vous réduisez le risque de comptabilisation de doublons d’articles. Pour plus d’informations, voir la section [Pour créer un enregistrement de stock physique](#to-create-a-physical-inventory-recording).

7. Cliquez sur le bouton **OK**.

Une ligne pour chaque article qui existe sur l’emplacement sélectionné et conformément aux filtres et options définis est insérée sur la commande. Pour les articles configurés pour le suivi des articles, la case à cocher **Utiliser le suivi des articles** est sélectionnée et les informations relatives à la quantité prévue des numéros de lot et de série est disponible en sélectionnant l’action **Lignes**, puis **Lignes de suivi des articles**. Pour plus d’informations, reportez-vous à la section [Gérer le suivi des articles lors de la réalisation de l’inventaire](#handling-item-tracking-when-counting-inventory).

Vous pouvez désormais commencer en créant un ou plusieurs enregistrements, qui correspondent aux instructions données aux employés en charge du décompte réel.  

## Pour créer un enregistrement de stock physique

Pour chaque commande de stock physique, vous pouvez créer un ou plusieurs documents d’enregistrement de stock physique sur lesquels les employés saisissent les quantités comptabilisées, manuellement ou via un appareil de lecture intégré.

Par défaut, un enregistrement est créé pour toutes les lignes sur la commande de stock physique. Pour éviter que deux employés comptabilisent les mêmes articles en cas d’inventaire distribué, il est recommandé de compléter au fur et à mesure la commande de stock physique en définissant des filtres sur le traitement par lots **Calculer les lignes** (voir la rubrique « Créer une commande de stock physique »), puis de créer l’enregistrement de stock physique tout en cochant la case **Uniquement les lignes qui ne figurent pas dans les enregistrements**. Ces paramètres veillent à ce que chaque nouvel enregistrement créé ne contienne que des articles différents de ceux des autres enregistrements.

En cas de décompte manuel, vous pouvez imprimer une liste, l’état **Enregistrement de stock physique**, sur lequel figure une colonne vide où vous renseignerez les quantités comptabilisées. Une fois le décompte effectué, vous saisissez les quantités enregistrées sur les lignes concernées de la page **Enregistrement de stock physique**. Enfin, transférez les quantités enregistrées dans la commande de stock physique concernée en définissant le statut sur **Terminé**.

1. Sur une page **Commande de stock physique** qui contient des lignes pour les articles à comptabiliser dans un enregistrement, sélectionnez l’action **Créer un enregistrement**.
2. Sélectionnez les options et définissez les filtres, le cas échéant.
3. Cliquez sur le bouton **OK**.

    Un document d’enregistrement de stock physique est créé.

4. Pour chaque ensemble d’article à comptabiliser, importez-les sur la commande de stock physique concernée et répétez les étapes 1 à 3 en veillant à bien cocher la case **Uniquement les lignes qui ne figurent pas dans les enregistrements**.

5. Sélectionnez l’action **Enregistrements** pour ouvrir la page **Liste des enregistrements de stock physique**.
6. Ouvrez l’enregistrement approprié.
7. Sur le raccourci **Général**, complétez les champs, comme nécessaire.
8. Pour les articles qui utilisent le suivi des articles, créez une ligne supplémentaire pour chaque numéro de lot ou code de numéro de série en sélectionnant l’action **Fonctions**, puis l’action **Copier la ligne**. Pour plus d’informations, reportez-vous à la section [Gérer le suivi des articles lors de la réalisation de l’inventaire](#handling-item-tracking-when-counting-inventory).  
9. Choisissez l’action **Imprimer** pour préparer le document physique que les employés utiliseront pour écrire les quantités comptabilisées.

## Pour finaliser un enregistrement de stock physique

Lorsque les employés ont comptabilisé les quantités en stock, vous devez préparer leur enregistrement dans le système.

1. Sur la page **Liste des enregistrements de stock physique**, sélectionnez l’enregistrement de stock physique que vous souhaitez terminer, puis sélectionnez l’action **Modifier**.
2. Sur le raccourci **Lignes**, renseignez la quantité comptabilisée réellement dans le champ **Quantité** pour chaque ligne.
3. Pour les articles avec des numéros de série ou de lot (la case **Utiliser le suivi des articles** est cochée), saisissez les quantités comptabilisées sur les lignes dédiées pour la question respective aux numéros de lot et de série de l’article. Pour plus d’informations, reportez-vous à la section [Gérer le suivi des articles lors de la réalisation de l’inventaire](#handling-item-tracking-when-counting-inventory).
4. Sélectionnez la case à cocher **Enregistrée** sur chaque ligne.
5. Une fois que vous avez saisi toutes les données pour un enregistrement de stock physique, sélectionnez l’action **Terminer**. Vous observerez que toutes les lignes doivent avoir la case **Enregistrée** sélectionnée.

> [!NOTE]
> Lorsque vous avez terminé un enregistrement de stock physique, chaque ligne est transférée vers la ligne sur la commande de stock physique associée qui correspond exactement. Pour correspondre, les valeurs des champs **N° article**, **Code variante**, **Code magasin** et **Code emplacement** doivent être identiques sur l’enregistrement et les lignes de commande.<br /><br />
> Si aucune ligne de commande de stock physique correspondante n’existe, et si la case **Autoriser l’enregistrement sans commande** est cochée, une nouvelle ligne est insérée automatiquement et la case **Enregistré sans commande** sur la ligne de commande de stock physique concernée est sélectionnée. Sinon, un message d’erreur s’affiche et le processus est annulé.<br /><br />
> Si plusieurs lignes d’enregistrement de stock physique correspondent à une ligne de commande de stock physique, un message s’affiche et le processus est annulé. Si, pour une raison ou une autre, deux lignes de stock physique identiques arrivent sur la commande de stock physique, vous pouvez utiliser une fonction pour résoudre le problème. Pour plus d’informations, reportez-vous à la rubrique [Rechercher des lignes de commande de stock physique](#to-find-duplicate-physical-inventory-order-lines).

## Pour finaliser une commande de stock physique

Lorsque vous avez terminé un enregistrement de stock physique, le champ **Quantité enregistrée (base)** sur la commande de stock physique associée est mis à jour avec les valeurs comptabilisées (enregistrées) et la case à cocher **Lors de l’enregistrement** est sélectionnée. Si une valeur comptabilisée diffère de la valeur prévue, cette différence s’affiche respectivement dans les champs **Qté positive (de base)** et **Qté négative (de base)**.

Pour voir les quantités prévues et toute différence enregistrée pour les articles avec le suivi des articles, sélectionnez l’action **Lignes**, puis choisissez l’action **Lignes de suivi des articles** pour sélectionner différentes vues pour les numéros de lot et de série impliqués dans l’inventaire.

Vous pouvez aussi choisir l’action **Diff. commande de stock physique** pour visualiser les différences entre la quantité prévue et la quantité comptabilisé.

### Pour rechercher les doublons de lignes de commande de stock physique

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Commandes de stock**, puis choisissez le lien associé.
2. Ouvrez la commande de stock physique pour laquelle vous souhaitez afficher les doublons de lignes.
3. Choisissez l’action **Afficher les doublons de lignes**.

Tout doublon de ligne de commande de stock physique est affiché de telle sorte que vous puissiez les supprimer et ne conserver qu’une ligne avec un ensemble de valeurs unique dans les champs **N° article**, **Code variante**, **Code magasin** et **Code emplacement**.

### Pour valider une commande de stock physique

Après avoir effectué une commande de stock physique et modifié son statut sur **Terminé**, vous pouvez la valider. Vous pouvez définir uniquement le statut d’une commande de stock physique sur **Terminé** si les éléments suivants sont vrais :

- Tous les enregistrements du stock physique concerné ont un statut défini sur **Terminé**.
- Chaque ligne de commande de stock physique a été comptabilisée par au moins une ligne d’enregistrement de stock.
- Les cases à cocher **Dans les lignes enregistrement** et **Qté prévue (calculée)** ont été sélectionnées pour toutes les lignes de commande de stock physique.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Commandes de stock**, puis choisissez le lien associé.
2. Sélectionnez la commande de stock physique que vous souhaitez compléter, puis sélectionnez l’action **Modifier**.

    Sur la page **Commande de stock physique**, vous visualisez la quantité enregistrée dans le champ **Qté enregistrée (de base)**.
3. Sélectionnez l’action **Terminer**.

    La valeur dans le champ **Statut** est passée sur **Terminé**, et la commande peut être modifiée maintenant uniquement en sélectionnant tout d’abord l’action **Rouvrir**.
4. Pour valider la commande, sélectionnez l’action **Valider**, puis le bouton **OK**.

Les écritures comptables des articles concernés sont mises à jour ainsi que les écritures de suivi des articles concernées.

### Pour afficher les commandes de stock physique validées

Après validation, la commande de stock physique est supprimée et vous pouvez afficher et évaluer le document en tant que commande de stock physique validée, y compris ses enregistrements de stock physique et tout commentaire effectué.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Commandes de stock physique validées**, puis choisissez le lien associé.
2. Sur la page **Commandes de stock physique validées**, sélectionnez la commande de stock validée que vous souhaitez afficher, puis sélectionnez l’action **Afficher**.
3. Pour afficher une liste des enregistrements de stock physique concernés, sélectionnez l’action **Enregistrements**.

## Gestion du suivi des articles lors de l’exécution de l’inventaire

Le suivi des articles concerne les numéros de lot ou de série attribués aux articles. Lors de la comptabilisation d’un article enregistré dans le stock, par exemple, 10 différents numéros de lot, l’employé doit être en mesure d’enregistrer quelles unités, et leur nombre, de chaque numéro de lot figurent en stock. Pour plus d’informations sur la fonctionnalité de suivi des articles, reportez-vous à la rubrique [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).

La case à cocher **Utiliser le suivi des articles** sur les lignes de commande de stock physique est automatiquement sélectionnée si un code de suivi des articles est configuré pour l’article, mais vous pouvez également la cocher ou la décocher manuellement.

### Exemple - Préparer un enregistrement de stock physique pour un article - Article suivi

Imaginons un stock physique pour l’article A, enregistré en stock sous la forme de dix différents numéros de série.
1. Sur la ligne d’enregistrement pour l’article, sélectionnez la case **Utiliser le suivi des articles**.
2.  Sélectionnez le champ **N° de série**, sélectionnez le premier numéro de série existant dans le stock pour l’article, puis cliquez sur le bouton **OK**.

    Commencez par copier la ligne pour le premier article suivi pour insérer des lignes supplémentaires correspondant au nombre de numéros de série enregistrés en stock.

3. Choisissez l’action **Fonctions**, puis l’action **Copier ligne**.
4. Sur la page **Copier la ligne enregistrement de stock physique**, saisissez 9 dans le champ **Nombre de copies**, puis sélectionnez le bouton **OK**.
5. Sur la première des lignes de copie, sélectionnez le champ **N° de série** et sélectionnez le numéro de série suivant pour l’article.
6. Répétez l’étape 5 pour les huit numéros de série restants, en veillant à ne pas sélectionner le même deux fois.
7. Choisissez l’action **Imprimer** pour préparer le bordereau que les employés utiliseront pour écrire les numéros de lot/de série et les articles comptabilisés.

Vous observerez que l’état **Enregistrement de stock physique** contient dix lignes pour l’article A, un pour chaque numéro de série.

### Exemple - Enregistrer et valider les différences de numéro de lot comptabilisé

Un article suivi est enregistré en stock avec la souche de numéros « LOT ».

**Stock prévu** :

|N° lot|Quantité|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Total|120|

**Quantités enregistrées** :

|N° lot|Quantité|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Total|112|

**Quantités à valider** :

|N° lot|Quantité prévue|Quantité enregistrée|Quantité à valider|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Total|120|112|-8|

Sur la page **Commande de stock physique**, le champ **Qté négative (de base)** contiendra *8*. Pour la ligne de commande en question, la page **Liste traçabilité stock physique** contiendra les quantités positives ou négatives pour les numéros de lot individuels.

## Documents d’inventaire

Les types de documents suivants sont utiles pour gérer votre entrepôt :

- Utilisez **Réception d’inventaire** pour enregistrer les ajustements positifs des articles en fonction de la qualité, de la quantité et du coût.
- Utilisez **Expéditions d’inventaire** pour radier les marchandises manquantes ou endommagées.

Vous pouvez imprimer ces documents à tout moment, les libérer et les rouvrir, et attribuer des valeurs communes, y compris des dimensions, dans l’en-tête. Si vous souhaitez réimprimer les documents après leur publication, vous pouvez le faire sur les pages **Réception d’inventaire validée** et **Expédition du stock validé**.

> [!NOTE]
> Avant de pouvoir utiliser ces documents, vous devez spécifier une souche de numéros pour créer leurs identificateurs. Pour plus d’informations, voir la section suivante.

### Pour paramétrer la numérotation des documents de stock

La procédure suivante indique comment définir la numérotation des documents stock.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres stock**, puis choisissez le lien associé.
2. Sur le Raccourci **Numérotation**, spécifiez dans les champs suivants la souche de numéros pour les documents :
   - **N° réception stock**  
   - **N° réceptions stock validées**  
   - **N° expédition stock**  
   - **N° expédition stock validée**  

### Pour créer et publier un document d’inventaire

La procédure suivante montre comment créer, imprimer et valider un reçu d’inventaire. La procédure est identique pour des expéditions de stock.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réceptions de stock**, puis choisissez le lien associé.  
2. Dans l’en-tête de la page **Réception de stock**, choisissez l’emplacement dans le champ **Code magasin**, puis remplissez les champs restants si nécessaire.
3. Sur le Raccourci **Lignes**, dans le champ **Article**, choisissez l’article en stock. Dans le champ **Quantité**, saisissez le nombre d’articles à ajouter. 
4. Pour imprimer un état **Réception stock** de la page **Réception stock**, choisissez l’action **Imprimer**.

Les fonctions suivantes sont disponibles sur la page **Réception stock** :

- Choisissez les actions **Libérer** ou **Rouvrir** pour définir le statut de la prochaine étape de traitement  
- Choisissez l’action **Valider** pour enregistrer la réception stock, ou choisissez **Publier et imprimer** pour valider la réception et imprimer le rapport de test  

## Impression des documents stock

Vous pouvez spécifier les états à imprimer à différentes étapes en choisissant l’une des options suivantes dans le champ **Utilisation** de la page **Sélection d’états – Stock** :

- Réception stock
- Expédition stock
- Réception en stock validée
- Expédition stock validée

> [!NOTE]
> Les rapports disponibles peuvent varier en fonction de la localisation de votre pays. L’application de base n’inclut aucune présentation.

## Voir la [formation Microsoft](/training/modules/adjust-inventory/) associée

## Voir aussi

[Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md)  
[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)  
[Ventes](sales-manage-sales.md)  
[Procédure d’achat](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
