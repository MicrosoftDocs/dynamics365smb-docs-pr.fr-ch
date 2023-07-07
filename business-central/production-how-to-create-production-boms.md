---
title: Créer des nomenclatures de production
description: 'Découvrez comment créer une nomenclature de production, de nouvelles versions d’une nomenclature de production et utiliser la formule de calcul de quantité.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="create-production-boms"></a>Créer des nomenclatures de production

Une nomenclature de production contient les données de base qui décrivent les composants et les produits semi-finis utilisés lors de la fabrication d’un article parent. Après la création d’un ordre de fabrication pour cet article parent, sa nomenclature de production gouvernera le calcul de besoins matériels tels que représentés sur la page **Composants ordre prod.**.

[!INCLUDE[prod_short](includes/prod_short.md)] prend également en charge les nomenclatures d’assemblage. Vous utilisez des ordres d’assemblage pour fabriquer des produits finis à partir de composants dans le cadre d’un processus simple qui peut être exécuté par une ou plusieurs ressources de base, qui ne sont pas des postes ou centres de charge, ou sans ressource. Par exemple, un processus d’assemblage peut consister à prélever deux bouteilles de vin et un sachet de café puis à les emballer comme article de cadeau. Pour plus d’informations, voir [Nomenclatures d’assemblage ou nomenclatures de production](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> L’application **Données de démonstration Contoso Coffee** comprend des produits de démonstration pour une variété de scénarios de nomenclature de production qui peuvent être utilisés dans un environnement de test, y compris lors d’un essai. Découvrez comment configurer les données Contoso Coffee et trouvez des procédures pas à pas pour différents scénarios dans la section [Présentation des données de démonstration Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).

Pour pouvoir configurer une gamme, les éléments suivants doivent être en place :  

- Des fiches article sont créées pour les articles parents qui participent à la production. Pour plus d’informations, reportez-vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).
- Les ressources de production sont configurées. Pour plus d’informations, voir [Configurer les centres de charge et les postes de charge](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Pour créer une nomenclature de production

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Nomenclatures de production**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Pour modifier la nomenclature, définissez le champ **Statut** sur **Création en cours** ou sur **Modification en cours**. Pour l’activer, définissez le champ **Statut** sur **Validée**.  

    Renseignez les lignes nomenclature de production.
5. Dans le champ **Type**, indiquez si l’article sur la ligne nomenclature est un article ordinaire ou s’il s’agit d’une nomenclature de production. Dans le dernier cas, l’article doit déjà exister en tant que nomenclature de production certifiée.  
6. Dans le champ **N°**, consultez et sélectionnez l’article ou la nomenclature de production concernée \(ou entrez l’un ou l’autre\).  
7. Dans le champ **Quantité par**, spécifiez le nombre d’unités de l’article intégrant l’article parent, par exemple, les 4 roues d’une voiture.  
8. Dans le champ **% rebut**, vous pouvez indiquer le taux fixe de perte de composants lors de la production. Une fois qu’ils sont prêts à être consommés dans un ordre de fabrication lancé, ce taux est ajouté à la quantité prévue dans le champ **Quantité consommée** dans une feuille production. Pour plus d’informations, voir [Comment enregistrer la consommation et la production](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  ce taux de rebut correspond aux composants perdus au cours de la production durant le prélèvement stock, alors que, sur les lignes gamme, il représente la production perdue avant stockage.  

9. Dans le champ **Code lien gamme**, vous pouvez entrer un code permettant de lier le composant à une opération spécifique. Pour plus d’informations, reportez-vous à [Pour créer des liens gamme](production-how-to-create-routings.md#to-create-routing-links).
10. Pour copier des lignes à partir d’une nomenclature de production existante, choisissez l’action **Copier nomenclature** pour sélectionner des lignes existantes.  
11. Certifiez la nomenclature de production.  
12. Vous pouvez désormais joindre la nouvelle nomenclature de production à la fiche de l’article parent en question. Pour plus d’informations, reportez-vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Pour recalculer le coût standard de l’article figurant sur la fiche article, choisissez l’action **Production**, puis l’action **Calculer coût standard**.  

## <a name="to-create-a-new-version-of-a-production-bom"></a>Pour créer une nouvelle version d’une nomenclature de production

Les nouvelles versions des nomenclatures de production sont utilisées lorsque, par exemple, un article est remplacé par un autre article, ou lorsqu’un client demande une version spéciale d’un produit. Le principe de la version permet de gérer différentes versions d’une nomenclature de production. La structure des versions de nomenclature de production correspond à celle des nomenclatures de production. La principale différence réside dans la validité des versions. La validité est définie par la date début.  

La date début indique le début de la période de validité de la version. La date début peut également être considérée comme un filtre pour les calculs et les évaluations. La version de la nomenclature est valide jusqu’à l’entrée en vigueur de la version suivante, qui est indiquée par sa date début.  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Nomenclatures de production**, puis choisissez le lien associé.  
2. Sélectionnez la nomenclature de production à copier, puis choisissez l’action **Versions**.  
3. Sélectionnez l’action **Nouveau**.  
4. Renseignez les champs selon vos besoins.
5. Dans le champ **Code version**, saisissez le numéro d’identification unique de la version. Ce champ admet n’importe quelle combinaison de chiffres et de lettres.  

    Le statut **Nouveau** est automatiquement affecté à la version que vous venez de créer.
6. Lorsque la version de nomenclature est terminée, définissez le champ **Statut** sur **Validé**.  

La validité de la version est définie par le champ **Date début**.  

> [!NOTE]  
> Sélectionnez l’option **Article** du champ **Type** pour utiliser un article des données de base article dans la nomenclature de production. Si cet article possède aussi une nomenclature de production, le champ **N° nomenclature production** est alors renseigné dans la fiche article, cette nomenclature de production est aussi prise en considération.  
>
> Sélectionnez l’option **Nomenclature de production** si vous souhaitez utiliser une nomenclature fantôme dans la ligne.  
>
> Les nomenclatures fantômes servent à structurer les produits. Ce type de nomenclature de production n’aboutit jamais à un produit fini, mais est exclusivement destiné à déterminer la demande dépendante. Les nomenclatures fantômes ne possèdent pas de données de base article propres.

## <a name="quantity-calculation-formula-on-production-boms"></a>Formule de calcul de la quantité sur les nomenclatures de production

Le calcul de la quantité tient compte des différents axes analytiques également insérés dans les lignes nomenclature de production. Ces axes se rapportent à une unité de commande de l’article concerné. Les axes ainsi entrés peuvent être une longueur, une largeur, une profondeur ou un poids.  

Les colonnes Formule de calcul, Longueur, Largeur, Profondeur et Poids ne s’affichent pas car seuls quelques utilisateurs les emploient. Si vous souhaitez utiliser le calcul de la quantité, vous devez d’abord afficher ces colonnes.  

La relation entre chacun des composants est définie par la formule de calcul. Vous pouvez utiliser les formules de calcul comme suit :  

- **Vide** - Pas de prise en compte des axes. (Quantité = Quantité par)  
- **Longueur** - Quantité = Quantité par * Longueur  
- **Longueur x Largeur** - Quantité = Quantité par * Longueur x Largeur  
- **Longueur x Largeur x Profondeur** - Quantité = Quantité par x Longueur x Largeur x Profondeur  
- **Poids** - Quantité = Quantité par x Poids  
- **Quantité fixe** - Quantité = Quantité par

> [!NOTE]
> La formule de calcul **Quantité fixe** permet de s’assurer que la consommation d’un composant reste la même, quelles que soient les quantités de rebuts ou de sorties. Pour les composants d’ordre de fabrication, lorsque le champ **Formule de calcul** est défini sur **Quantité fixe**, la valeur du champ **Quantité prévue** est toujours égale à celle du champ **Quantité par**. Le pourcentage de rebut défini sur la même ligne est ignoré. La quantité fixée est respectée par l’état **Disponibilité par nomenclature**. L’état affichera l’article comme goulot d’étranglement si la quantité disponible est inférieure à la quantité dans le champ **Quantité par parent**. Les champs **Capable de fabriquer le parent** et **Capable de fabriquer le meilleur article** sont toujours vides, quelle que soit la quantité disponible. La quantité fixe est également incluse dans les calculs des coûts standard. La taille du lot de l’article produit a un impact sur le coût alloué à un article.

### <a name="example"></a>Exemple :

Une nomenclature de production répertorie 70 feuilles de métal dotées des axes suivants : longueur = 0,20 m et largeur = 0,15 m. Les valeurs suivantes sont saisies : Formule de calcul = Longueur x Largeur, Longueur = 20, Largeur = 15, Quantité par = 70. La quantité est donnée par la valeur Quantité par x Longueur * Largeur, c’est-à-dire Quantité = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Voir aussi

[Créer des gammes](production-how-to-create-routings.md)  
[Gérer les variantes de produits](inventory-item-variants.md)  
[Procédure pas à pas : variantes](contoso-coffee/manufacturing/variants.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
