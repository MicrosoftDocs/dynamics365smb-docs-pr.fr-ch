---
title: 'Prélever ou déplacer des articles pour la fabrication, l’assemblage ou les tâches dans les configurations de stockage de base'
description: 'Lorsque l’entrepôt appelle un traitement de prélèvement sans appeler de traitement d’expédition, vous pouvez utiliser la page Prélèvement stock pour organiser et enregistrer le prélèvement des composants.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# Prélever pour la fabrication, l’assemblage ou les tâches dans les configurations de stockage de base

Le mode de prélèvement de vos composants pour les ordres de fabrication, d’assemblage ou les tâches dépend de la configuration de l’entrepôt en tant qu’emplacement. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans une configuration d’entrepôt de base pour le flux sortant (prélèvement), sur la page **Fiche magasin** du site, activez le bouton à bascule **Prélèvement requis** mais désactivez le bouton à bascule **Expédition requise**.

Utilisez les documents suivants pour les opérations internes :

* Prélvmt invent
* Mouvement de stock

## Prélèvements stock

* Lorsque vous enregistrez un prélèvement stock pour une opération interne, telles que la production ou une tâche, la consommation des composants sélectionnés est validée en même temps.
* Le bouton à bascule **Emplacement obligatoire** sur la page **Fiche magasin** est facultatif.
* Lorsque vous utilisez les prélèvements stock, le champ **Code emplacement** sur une ligne de composant d’ordre de fabrication ou les lignes planning d’une tâche définit l’emplacement *prendre*. Les composants sont diminués dans le bac « prendre » lorsque vous validez la consommation.

## Mouvements de stock

* Les mouvements de stock nécessitent que vous activiez le bouton à bascule **Emplacement obligatoire** sur la page **Fiche magasin** pour l’emplacement.
* Les mouvements de stock ne fonctionnent qu’avec les lignes de composants d’ordre de fabrication et les lignes d’ordre d’assemblage.
* Lorsque vous enregistrez un mouvement stock pour une opération interne, vous enregistrez seulement le mouvement physique des composants dans un emplacement de la zone d’opération. Vous ne validez pas la consommation.
* Lorsque vous utilisez les mouvements stock, le champ **Code emplacement** sur une ligne de composant d’ordre de fabrication définit l’emplacement *placer* dans la zone d’opération. L’emplacement « placer » est l’endroit où les magasiniers doivent placer les composants.
* Enregistrez séparément la consommation des composants prélevés en publiant une feuille consommation ou un ordre d’assemblage.

>[!NOTE]
> Même si le bouton à bascule **Prélèvement requis** est désactivé, vous pouvez utiliser un document **Prélèvement entrepôt**. Les documents de prélèvement entrepôt sont similaires aux documents **Prélèvement stock**. Ceci est utile si vous souhaitez utiliser les prélèvements dans les opérations et expédier dans les flux sortants de l’entrepôt.

### Fabrication

Utilisez les documents **Prélèvement stock** pour prélever des composants de production dans le flux vers la production.

Pour un magasin qui utilise des emplacements, vous pouvez étendre le flux jusqu’à la production en utilisant les documents **Mouvement stock**. Les mouvements de stock sont particulièrement utiles pour la consommation des composants. Pour en savoir plus sur la façon dont la consommation de composants passe des emplacements de consommation aux emplacements atelier ouverts, consultez [Consommer les composants pour la production dans une configuration d’entrepôt de base](#flushing-production-components-in-a-basic-warehouse-configuration).

### Assemblage  

Utilisez les documents **Mouvement stock** pour déplacer les composants d’assemblage vers la zone d’assemblage.

> [!NOTE]
> Les documents **Mouvement stock** nécessitent des emplacements.

[!INCLUDE [prod_short](includes/prod_short.md)] prend en charge les types de flux d’assemblage Assembler pour stock et Assembler pour commande. Pour en savoir plus sur l’assemblage pour commande dans le flux d’entrepôt sortant, accédez à [Traitement des articles à assembler pour commande dans des prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Gestion de projets  

Utilisez les documents **Prélèvement stock** pour sélectionner les composants de la tâche dans le flux vers la gestion de projet.

Pour les magasins qui utilisent des emplacements, vous pouvez étendre le flux jusqu’aux projets en utilisant les documents **Mouvement stock**.

> [!NOTE]
> La possibilité de sélectionner des composants pour les lignes de planning des tâches a été ajoutée à [!INCLUDE[d365fin](includes/d365fin_md.md)] dans la 2è vague de lancement 2022. Pour commencer à utiliser la capacité, un administrateur doit activer **Mise à jour des fonctionnalités : activer prélèvement stock et entrepôt à partir des projets** sur la page **Gestion des fonctionnalités**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] utilise la valeur dans le champ **Quantité restante** sur la ligne de planning des tâches lorsqu’il crée des prélèvements stock. Pour utiliser les prélèvements d’inventaire pour les tâches, vous devez activer le bouton à bascule **Appliquer le lien d’utilisation** sur la page **Fiche projet** pour les tâches. Cela vous permet de suivre l’utilisation par rapport à votre forfait. Si vous n’activez pas le bouton à bascule, la quantité restante restera à **0** et le choix de stock ne sera pas créé. Learn more at [Pour configurer un suivi d’utilisation de projet](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## Prélever ou déplacer pour la production, l’assemblage ou les projets dans les configurations de stockage de base

Vous pouvez créer un prélèvement stock ou un mouvement stock de trois manières :  

* À partir du document origine lui-même.  
* Pour plusieurs documents origine en même temps en utilisant un traitement par lots.  
* En deux étapes. Publiez le document origine pour qu’il soit prêt pour le prélèvement. Créez le prélèvement ou le mouvement stock à partir des documents **Prélèvement stock** ou **Mouvement stock**. Le prélèvement ou le mouvement stock est basé sur le document origine.  

### Pour créer un prélèvement stock à partir du document origine

1. Sur le document origine, qui peut être un ordre de fabrication ou un projet, choisissez l’action **Créer prélèv./rangement stock**.  
2. Activez la case à cocher **Créer prélèvement stock**.
3. Cliquez sur le bouton **OK**.

### Pour créer un mouvement de stock à partir du document origine

1. Sur le document origine, qui peut être un ordre de fabrication, un ordre d’assemblage ou un projet, choisissez l’action **Créer prélèv./rangement stock**.  
2. Activez la case à cocher **Créer mouvement stock**.
3. Cliquez sur le bouton **OK**.

### Pour créer plusieurs prélèvements ou mouvements stock avec un traitement par lots

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Créer rangement/prélèvement/mouvement stock**, puis choisissez le lien associé.  
2. Sur le raccourci **Demande entrepôt**, utilisez les champs **Document origine** et **N° origine** pour opérer un filtrage sur les types de documents ou des plages de numéros de document. Par exemple, vous pouvez créer des prélèvements uniquement pour des ordres de fabrication.
3. Dans le raccourci **Options**, activez les boutons à bascule **Créer prélèvement stock** ou **Créer mouvement stock**.
4. Cliquez sur le bouton **OK**.

### Pour créer des prélèvements ou des mouvements stock en deux étapes

Pour prélever ou déplacer des composants pour des documents origine en deux étapes, vous devez émettre le document origine pour qu’il soit prêt pour le prélèvement. Lancez les documents origine des opérations internes en procédant comme suit.  

|Document origine|Méthode de lancement|  
|---------------------|--------------------|  
|Ordre de fabrication|Sur la page **Ordre de fabrication planifié**, changez le statut d’une commande en **Lancé** , ou utilisez la page **Ordre de fabrication lancé**pour créer un ordre de fabrication lancé.|  
|Ordre d’assemblage|Modifiez le statut d’un ordre d’assemblage en **Lancé**.|
|Projets | Changez le statut d’un projet en **Ouvert** ou créez un projet avec le statut Ouvert immédiatement.|  

Un magasinier affecté au prélèvement d’articles peut créer un document de rangement de stock pour le document origine.  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock** or **Inventory Movement**, and then choose the related link.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Document origine**, sélectionnez le type de document origine que concerne le rangement.

    > [!NOTE]
    > Vous ne pouvez pas utiliser les documents **Prélèvement stock** pour prélever des composants d’assemblage.
4. Dans le champ **N° origine**, sélectionnez le document origine.  
5. Sinon, choisissez l’action **Extraire document origine** pour sélectionner le document à partir de la liste des documents origine entrants prêts pour le prélèvement dans le magasin.  
6. Cliquez sur le bouton **OK** pour renseigner les lignes prélèvement ou mouvement en fonction du document origine sélectionné.  

## Pour enregistrer le prélèvement stock

1. Sur la page **Prélèvement stock**, ouvrez le document pour lequel enregistrer un prélèvement.  
2. Dans le champ **Code emplacement** sur les lignes prélèvement, l’emplacement à partir duquel les articles doivent être prélevés à partir de l’emplacement où l’article est disponible. Si nécessaire, vous pouvez modifier l’emplacement.
3. Exécutez le prélèvement, puis saisissez la quantité prélevée dans le champ **Quantité à traiter**.

    Si vous devez prélever les articles d’une ligne à partir de plusieurs emplacements, par exemple parce qu’un emplacement ne contient pas la quantité totale, utilisez l’action**Fractionner la ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.  
4. Sélectionnez l’action **Valider**.  

Voici ce qui se passe pendant le processus de validation :

* Validation de la consommation des lignes du document origine qui ont été prélevées.
* Si le magasin utilise des emplacements, la validation crée également des écritures entrepôt pour valider les modifications de la quantité de l’emplacement.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Pour enregistrer le mouvement stock

1. Sur la page **Mouvement stock**, ouvrez le document pour lequel enregistrer le mouvement.  
2. Dans le champ **Code emplacement** sur les lignes de mouvement, l’emplacement à prélever est suggéré en fonction de l’emplacement par défaut et de la disponibilité de l’article. Si nécessaire, vous pouvez modifier l’emplacement.  
3. Exécutez le mouvement, puis saisissez la quantité déplacée dans le champ **Quantité à traiter**. La valeur sur les lignes prélèvement et emplacement doit être la même. Sinon, vous ne pouvez pas enregistrer le mouvement.

    Si vous devez prendre les articles d’une ligne dans plusieurs emplacements, par exemple parce qu’un emplacement ne contient pas la quantité totale, utilisez l’action **Fractionner la ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.  
4. Sélectionnez l’action **Enregistrer mouvement de stock**.  

Voici ce qui se passe pendant le processus de validation :

* Les écritures entrepôt indiquent maintenant que les composants se trouvent dans les emplacements spécifiés sur les lignes d’ordre d’assemblage du document origine. Par exemple, la ligne d’ordre d’assemblage, de composant de production ou de planning projet.

>[!NOTE]
> Contrairement au déplacement de composants à l’aide de prélèvements stock, la consommation n’est pas validée lorsque vous enregistrez un mouvement de stock. Vous enregistrez la consommation dans une étape distincte en validant le document origine.

## Consommer les composants pour la production dans une configuration d’entrepôt de base

Les modes de consommation affectent le flux des composants en production. Learn more at [Consommer des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md). En fonction de la méthode de consommation sélectionnée, vous pouvez prélever des composants pour la production des manières suivantes :

* Utilisez un document **Prélèvement stock** pour enregistrer le prélèvement des articles qui utilisent la méthode de consommation **manuelle**. Lorsque vous enregistrez un prélèvement stock, la consommation des composants prélevés est enregistrée. 
* Utilisez un document **Mouvement stock** avec une référence à un document origine pour enregistrer les prélèvements pour les composants qui utilisent la méthode de consommation **Manuelle**. Vous devrez enregistrer la consommation séparément. Learn more at [Valider par lots la consommation de la production](production-how-to-post-consumption.md). 
* Utilisez un document **Mouvement stock** avec une référence à un document origine pour enregistrer les prélèvements pour les composants qui utilisent la méthode de consommation **Prélèvement + Aval**, **Prélèvement + Amont**. La consommation des composants se produira automatiquement, soit lorsque vous modifiez le statut de l’ordre de fabrication, soit en démarrant ou en terminant une opération. Tous les composants requis doivent être disponibles. Autrement, la validation de la consommation du composant est arrêtée.
* Utilisez un document **Mouvement stock** sans référence à un document origine ou d’autres moyens d’enregistrer le mouvement des composants qui utilisent la méthode de consommation **Aval** ou **Amont**. La consommation des composants se produira automatiquement, soit lorsque vous modifiez le statut de l’ordre de fabrication, soit lorsque vous démarrez ou terminez une opération. Tous les composants requis doivent être disponibles. Autrement, la validation de la consommation s’arrête pour ce composant. Learn more at [Déplacement des articles en interne dans les configurations entrepôt de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Exemple :

Vous avez un ordre de fabrication pour 15 pièces de l’article SP-SCM1004. Certains articles sur la liste des composants doivent être consommés manuellement dans une feuille consommation et d’autres articles peuvent être prélevés et consommés automatiquement à l’aide de la méthode de consommation **Prélèvement + Amont**.  

Les étapes suivantes illustrent les actions prises par divers utilisateurs et les réponses associées :  

1. Le chef atelier lance l’ordre de fabrication. Les articles utilisant la méthode de consommation **Aval** et aucun lien gamme sont déduits de l’emplacement atelier ouvert.  
2. Le chef d’atelier choisit l’action **Créer prélèv./rangement stock** sur l’ordre de fabrication et active les boutons à bascule **Créer prélèvement stock** et **Créer mouvement de stock**. Un document de prélèvement stock est créé pour les articles avec la méthode de consommation **manuelle**, et un mouvement de stock est créé pour les articles avec les méthodes de consommation **Prélèvement + Amont** et **Prélèvement + Aval**.
3. Le gestionnaire d’entrepôt affecte les prélèvements et les mouvements à un magasinier.
4. Le magasinier prélève les articles dans les emplacements appropriés et les place dans l’emplacement des consommations ou dans l’emplacement spécifié sur le mouvement stock. L’emplacement peut être un emplacement de poste de travail ou de poste de charge.  
5. Le magasinier valide le prélèvement. La quantité est déduite des emplacements.
6. Le magasinier valide le mouvement. La quantité est déduite des emplacements prélèvement et ajoutée à l’emplacement de consommation. Le champ **Qté prélevée** sur la liste des composants de tous les articles prélevés est mis à jour.  
7. L’opérateur indique au gestionnaire de production que les articles finis sont terminés.  
8. Le chef d’atelier utilise la feuille production pour valider la sortie. La quantité des composants qui utilisent les méthodes de consommation **Prélèvement + Aval** ou **Prélèvement + Amont** avec des liens gammes est déduite de l’emplacement des consommations.
9. Le gestionnaire de production modifie le statut de l’ordre de fabrication en **Terminé**. La quantité de composants qui utilisent la méthode de consommation **Amont** est déduite de l’emplacement atelier ouvert, et la quantité de composants qui utilisent la méthode de consommation **Prélèvement + Amont** et pas de lien gamme est déduite de l’emplacement des consommations.  

 La figure ci-après indique la date à laquelle le champ **Code emplacement** de la liste des composants est renseigné en fonction du paramétrage de votre magasin ou poste/centre de charge.  

:::image type="content" source="media/binflow.png" alt-text="Aperçu de quand et comment le champ Code emplacement est renseigné.":::

## Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
