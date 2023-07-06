---
title: Prélever pour des opérations internes dans les configurations de stockage avancées
description: 'Si vos sites utilisent le prélèvement et l’expédition, choisissez des composants pour les activités de production, d’assemblage et les tâches dans la page Sélection d’entrepôt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a><a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a><a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Prélever pour la fabrication, l’assemblage ou les tâches dans les configurations de stockage avancées

Le mode de prélèvement de vos composants pour les ordres de fabrication, d’assemblage ou les tâches dépend de la configuration de l’entrepôt en tant qu’emplacement. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans une configuration d’entrepôt avancée pour le flux sortant (prélèvement), activez les boutons à bascule **Prélèvement requis** et **Expédition requise** sur la page **Fiche magasin** pour l’emplacement.

Lorsque le magasin est configuré pour appeler un traitement de prélèvement entrepôt et un traitement d’expédition entrepôt, vous pouvez utiliser les documents prélèvement entrepôt pour créer et traiter les informations de prélèvement avant de valider l’utilisation ou la consommation des composants.  

Vous ne pouvez pas créer un document de prélèvement en entrepôt à partir de rien. Les prélèvements font partie d’un flux de travail où une personne qui traite une commande les crée de manière « push », ou l’employé de l’entrepôt les crée de manière « pull » :

- De la manière « push », où vous utilisez l’action **Créer un prélèvement** dans la page **Ordre de fabrication**, **Ordre d’assemblage**, **Fiche projet**. Sélectionnez les lignes à prélever et préparez les prélèvements en spécifiant, par exemple, à partir de quels emplacements les prendre, à quels emplacements les placer, et le nombre d’unités à traiter. Les emplacements peuvent être prédéfinis pour l’entrepôt ou la ressource.
- En mode « pull », vous lancez un **Ordre de fabrication**, un **Ordre d’assemblage** ou une **Fiche projet** vers l’entrepôt pour rendre les articles disponibles pour le prélèvement. Ensuite, sur la page **Feuille prélèvement**, les employés de l’entrepôt peuvent utiliser l’action **Extraire documents entrepôt** pour retirer les prélèvements qui leur sont assignés.

Pour prélever ou déplacer des composants pour des documents origine en mode « pull », vous devez émettre le document origine pour qu’il soit prêt pour le prélèvement. Lancez les documents origine des opérations internes en procédant comme suit.  

|Document origine|Méthode de lancement|  
|---------------------|--------------------|  
|Ordre de fabrication|Changez le statut de la commande sur Lancé ou créez immédiatement un ordre de fabrication lancé.|  
|Ordre d’assemblage|Remplacez le statut actuel par le statut Lancé.|
|Projets | Changez le statut en Ouvert ou créez une tâche avec le statut Ouvert immédiatement.|  

## <a name="production"></a><a name="production"></a><a name="production"></a>Fabrication

Utilisez les documents **Prélèvement entrepôt** pour prélever des composants de production dans le flux vers la production.

Pour un site qui utilise des emplacements pour déplacer des articles vers des emplacements d’atelier ouverts, vous pouvez utiliser les méthodes suivantes :

* Pour un site qui utilise le rangement et le prélèvement dirigés, suivez les étapes de l’article [Déplacer des articles dans les configurations de stockage avancée](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Pour les autres sites, suivez les étapes de l’article [Déplacer des articles dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a><a name="assembly"></a><a name="assembly"></a>Assemblage

Utilisez les documents **Prélèvement entrepôt** pour déplacer les composants d’assemblage vers la zone d’assemblage.

[!INCLUDE [prod_short](includes/prod_short.md)] prend en charge les types de flux d’assemblage Assembler pour stock et Assembler pour commande. Pour en savoir plus sur l’assemblage pour commande dans le flux d’entrepôt sortant, accédez à [Traitement des articles à assembler pour commande dans les expéditions entrepôt](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a><a name="project-management"></a><a name="project-management"></a>Gestion de projets

Utilisez les documents **Prélèvement entrepôt** pour sélectionner les composants de la tâche dans le flux vers la gestion de projet.

> [!NOTE]
> La possibilité de sélectionner des composants pour les lignes de planning des tâches a été ajoutée à [!INCLUDE[d365fin](includes/d365fin_md.md)] dans la 2è vague de lancement 2022. Pour commencer à utiliser la capacité, un administrateur doit activer **Mise à jour des fonctionnalités : activer prélèvement stock et entrepôt à partir des projets** sur la page **Gestion des fonctionnalités**.
>
> Les tâches ne prennent pas en charge les configurations avancées dans lesquelles le bouton à bascule **Prélèvement et rangement dirigés** est activé.

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Pour créer des documents de prélèvement en bloc avec la feuille prélèvement

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille prélèvement**, puis choisissez le lien associé.  

2. Choisissez l’action **Extraire documents entrepôt**.  

    La liste affiche la production lancée, les tâches, les ordres d’assemblage qui ont été transmis à la fonction de prélèvement. Les commandes incluent celles pour lesquelles des instructions de prélèvement ont déjà été créées. Les documents dont les lignes prélèvement ont été entièrement prélevées et enregistrées n’apparaissent pas dans cette liste.  
3. Sélectionnez les commandes pour lesquelles vous souhaitez préparer un prélèvement.

    > [!NOTE]  
    > Si vous sélectionnez un document qui contient déjà des instructions pour toutes ses lignes, [!INCLUDE [prod_short](includes/prod_short.md)] vous informe qu’il n’y a rien à gérer. Pour combiner les instructions de prélèvement entrepôt déjà créées en une instruction de prélèvement, supprimez d’abord les prélèvements entrepôt individuels.

4. Renseignez le champ **Méthode de tri** pour trier les lignes à votre convenance.  

    > [!NOTE]  
    > La façon dont les lignes sont triées dans la feuille ne se répercute pas automatiquement sur l’instruction de prélèvement. Cependant, les mêmes outils de tri sont disponibles, ainsi que le classement des emplacements. Vous pouvez facilement recréer l’ordre des lignes planifié dans la feuille lorsque vous créez ou triez les instructions de prélèvement.

5. Renseignez le champ **Quantité à traiter**. Choisissez l’action **Remplir qté à traiter**, ou renseignez les champs manuellement.  

    La page affiche les quantités disponibles dans les bacs de transbordement, ce qui est utile pour planifier les affectations de travail dans les situations de transbordement. [!INCLUDE[prod_short](includes/prod_short.md)] proposera toujours en premier un prélèvement dans un bac de transbordement.

6. Si nécessaire, vous pouvez modifier les lignes manuellement. Vous pouvez aussi supprimer certaines lignes pour rendre le prélèvement plus efficace. Par exemple, si plusieurs lignes comportent des articles situés dans des bacs de transbordement, vous pouvez créer un prélèvement pour toutes les lignes. Les articles transbordés seront prélevés avec les autres articles du document origine, et les emplacements de transbordement pourront à nouveau recevoir d’autres articles entrants.

    > [!NOTE]  
    >  Les lignes ne sont supprimées de cette feuille, et non de la liste de sélection des prélèvements.  

7. Choisissez l’action **Créer prélèvement**. La page **Créer un prélèvement** s’ouvre, où vous pouvez ajouter plus d’informations au prélèvement.  

    Spécifiez la façon de combiner les lignes prélèvement dans les documents prélèvement en sélectionnant l’une des options suivantes.  

    |Option|Description|
    |-|-|
    |Par entrepôt Document|Crée des documents prélèvement distincts pour les lignes feuille avec le même document d’origine entrepôt.|
    |Par client/fourn./mag.|Crée des documents de prélèvement séparés pour chaque client (tâches)|
    |Par article|Crée des documents prélèvement distincts pour chaque article dans la feuille prélèvement.|
    |Par zone origine|Crée des documents prélèvement distincts pour chaque zone où vous prendrez les articles.|
    |Par emplacement|Crée des documents prélèvement distincts pour chaque emplacement où vous prendrez les articles.|
    |Par délai|Crée des documents prélèvement distincts pour les documents d’origine qui ont la même date d’échéance.|

    Spécifiez la façon de créer les documents prélèvement en sélectionnant l’une des options suivantes.  

    |Option|Description|
    |-|-|
    |Montant Nombre de lignes prélèvement|Crée des documents prélèvement qui n’ont pas plus que le nombre de lignes spécifié dans chaque document.|
    |Montant Non. de docs origine prélèvement|Crée des documents prélèvement qui couvrent pas plus que le nombre spécifié de documents d’origine.|
    |Code utilisateur affecté|Crée des documents prélèvement uniquement pour les lignes qui sont affectées au magasinier sélectionné.|
    |Méthode de tri|Choisissez parmi les options disponibles pour trier les lignes du document prélèvement créé.|
    |Filtrer déconditionnement|Masque les lignes prélèvement déconditionnement intermédiaires lorsqu’une plus grande unité est convertie en une unité de mesure inférieure et est prélevée dans son intégralité.|
    |Ne pas remplir qté à traiter|Laisse le champ **Qté. à gérer** vide sur les lignes prélèvement créées.|
    |Imprimer prélèvement|Imprime les documents prélèvement lors de leur création. Vous pouvez également imprimer à partir des documents prélèvement créés.|

8. Cliquez sur le bouton **OK**.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a><a name="to-pick-items-for-a-productions-order-assembly-order-job"></a><a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Pour prélever des articles pour un ordre de fabrication, un ordre d’assemblage, une tâche

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements**, puis choisissez le lien associé.  

    Si vous souhaitez travailler à un prélèvement particulier, sélectionnez-le dans la liste ou filtrez cette dernière afin de trouver les prélèvements qui vous ont été affectés. Ouvrez la fiche prélèvement.  
2. Si le champ **ID utilisateur affecté** est vide, entrez votre ID pour vous identifier, si nécessaire.  
3. Prélevez les articles.  

    Si le magasin est configuré pour utiliser des emplacements, les emplacements par défaut des articles sont utilisés pour suggérer où prendre les articles. Les instructions contiennent au moins deux lignes distinctes pour les actions Prendre et Placer.  

    Les zones d’exploitation telles que les ateliers de production peuvent avoir un emplacement par défaut pour les composants dont ils ont besoin. Si c’est le cas, le code emplacement par défaut est ajouté au document prélèvement entrepôt pour indiquer où placer les articles. Pour plus d’informations, reportez-vous aux info-bulles pour les champs **Code empl. des consommations**, **Code empl. vers assemblage**, **Code emplacement vers projet**.

    Si l’entrepôt est configuré pour utiliser le rangement et le prélèvement dirigés, les classements des emplacements sont utilisés pour calculer les meilleurs emplacements pour le prélèvement. Ces emplacements sont suggérés sur les lignes prélèvement. Les instructions contiennent au moins deux lignes distinctes pour les actions Prendre et Placer.  

    * La première ligne, avec **Prendre** dans le champ **Type d’action**, indique l’endroit où se trouvent les articles dans la zone de prélèvement. Si vous expédiez un grand nombre d’articles sur une seule ligne d’expédition, vous devrez peut-être prélever les articles dans plusieurs emplacements ; il y a donc une ligne Prendre pour chaque emplacement.
    * La ligne suivante, avec **Placer** dans le champ **Type d’action**, indique l’endroit où vous devez placer les articles dans l’entrepôt. Vous ne pouvez pas modifier la zone et l’emplacement de cette ligne.

    > [!NOTE]
    > Si vous devez prélever ou placer les articles d’une ligne dans plusieurs emplacements, notamment parce que l’emplacement indiqué est plein, utilisez l’action **Eclater ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.

4. Après avoir prélevé et placé les articles dans la zone de production, d’assemblage ou de travail, choisissez l’action **Enregistrer le prélèvement**.  

    Vous pouvez maintenant amener les articles dans la zone respective et publier l’utilisation ou la consommation des composants prélevés en validant la feuille consommation, l’ordre d’assemblage ou la feuille projet. Pour en savoir plus, consultez les articles suivants :

    * [Enregistrer la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md)
    * [Assembler des articles](assembly-how-to-assemble-items.md)
    * [Enregistrer la consommation ou l′utilisation pour les projets](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a><a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a><a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a>Consommer les composants pour la fabrication dans une configuration entrepôt avancée

Les modes de consommation affectent le flux des composants en production. Learn more at [Consommer des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md). En fonction de la méthode de consommation sélectionnée, vous pouvez prélever des composants pour la production des manières suivantes :

* Utilisez un document **Prélèvement entrepôt** pour enregistrer le prélèvement des articles qui utilisent la méthode de consommation **manuelle**. Vous devrez enregistrer la consommation séparément. Learn more at [Valider par lots la consommation de la production](production-how-to-post-consumption.md).
* Utilisez un document **Prélèvement entrepôt** pour enregistrer le prélèvement des articles qui utilisent la méthode de consommation **Prélèvement + Aval**, **Prélèvement + Amont**. La consommation des composants se produira automatiquement, soit lorsque vous modifiez le statut de l’ordre de fabrication, soit en démarrant ou en terminant une opération. Tous les composants requis doivent être disponibles. Autrement, la validation de la consommation du composant est arrêtée.
* Utilisez un document **Mouvement entrepôt** sans référence à un document origine ou d’autres moyens d’enregistrer le mouvement des composants qui utilisent la méthode de consommation **Aval** ou **Amont**. Les composants sont automatiquement consommés, soit lorsque vous changez le statut de l’ordre de fabrication, soit lorsque vous démarrez ou terminez une opération. Tous les composants requis doivent être disponibles. Autrement, la validation de la consommation s’arrête pour ce composant. Learn more at [Déplacement d’articles](warehouse-move-items.md).

### <a name="example"></a><a name="example"></a><a name="example"></a>Exemple :

Vous avez un ordre de fabrication pour 15 pièces de l’article SP-SCM1004. Certains des articles de la liste des composants doivent être consommés manuellement dans une feuille consommation. D’autres articles peuvent être prélevés et consommés automatiquement à l’aide de la méthode de consommation **Prélèvement + Amont**.  

Les étapes suivantes décrivent les actions prises par divers utilisateurs et la réponse associée :  

1. Le chef atelier lance l’ordre de fabrication. Les articles utilisant la méthode de consommation **Aval** et aucun lien gamme sont déduits de l’emplacement atelier ouvert.  
2. Le chef atelier choisit l’action **Créer prélèvement entrepôt** sur l’ordre de fabrication. Un document prélèvement entrepôt est créé pour les articles avec les méthodes de consommation **Manuelle**, **Prélèvement + Amont** et **Prélèvement + Aval**. Ces articles sont placés dans l’emplacement des consommations.  
3. Le gestionnaire d’entrepôt affecte les prélèvements à un magasinier.  
4. Le magasinier prélève les articles dans les emplacements appropriés et les place dans l’emplacement des consommations ou dans l’emplacement spécifié sur le prélèvement entrepôt. L’emplacement peut être un emplacement de poste de travail ou de poste de charge.
5. Le magasinier enregistre le prélèvement. La quantité est transférée entre l’emplacement de prélèvement et l’emplacement de consommation. Le champ **Qté prélevée** sur la liste des composants de tous les articles prélevés est mis à jour.

    > [!NOTE]  
    >  Seule la quantité prélevée peut être consommée.  
6. L’opérateur indique au gestionnaire de production que les articles finis sont terminés.
7. Le chef d’atelier utilise la feuille consommation ou la feuille production pour valider la consommation des composants qui utilisent la méthode de consommation **manuelle**.
8. Le chef d’atelier utilise la feuille production pour valider la sortie. La quantité des composants qui utilisent les méthodes de consommation **Prélèvement + Aval** ou **Prélèvement + Amont** avec des liens gammes est déduite de l’emplacement des consommations.
9. Le gestionnaire de production modifie le statut de l’ordre de fabrication en **Terminé**. La quantité de composants qui utilisent la méthode de consommation **Amont** est déduite de l’emplacement atelier ouvert, et la quantité de composants qui utilisent la méthode de consommation **Prélèvement + Amont** et pas de lien gamme est déduite de l’emplacement des consommations.  

La figure ci-après indique la date à laquelle le champ **Code emplacement** de la liste des composants est renseigné en fonction du paramétrage de votre magasin ou poste/centre de charge.  

:::image type="content" source="media/binflow.png" alt-text="Aperçu de quand et comment le champ Code emplacement est renseigné.":::

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
