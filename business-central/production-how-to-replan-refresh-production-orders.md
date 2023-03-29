---
title: Replanifier ou actualiser directement des ordres de fabrication
description: Cette rubrique décrit les procédures permettant de replanifier les ordres de fabrication et d’actualiser directement les ordres de fabrication.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000842, 99000843, 99000861, 99000862, 99000863'
ms.date: 06/25/2021
ms.author: edupont
---
# Replanifier ou actualiser directement des ordres de fabrication

La fonction **Replanifier** des ordres de fabrication est généralement utilisée après avoir ajouté ou modifié des composants constituant des ordres de fabrication sous-jacents. La fonction calcule les modifications apportées aux composants et aux lignes gamme. Elle inclut les articles situés à des niveaux de nomenclatures de production inférieurs, pour lesquels elle peut générer de nouveaux O.F.  

Sur la base des modifications apportées aux composants et aux lignes gamme, la fonction Replanifier calcule et planifie toutes les nouvelles demandes de l’ordre de fabrication.  

La fonction **Actualiser** des ordres de fabrication est généralement utilisée après avoir effectué une des opérations suivantes :

- Créé un en-tête d’ordre de fabrication manuellement pour calculer et créer des données de ligne pour la première fois.
- Apporté des modifications à un en-tête d’ordre de fabrication pour recalculer toutes les données de ligne.

La fonction Actualiser calcule les modifications apportées à un en-tête d’ordre de fabrication et ne prend pas en compte les niveaux nomenclature de production. La fonction a pour rôle de calculer et d’initier les valeurs des lignes composant et des lignes gamme en fonction des données de base définies dans la nomenclature de production et la gamme affectées, selon la quantité commande et la date d’échéance de l’en-tête de l’ordre de fabrication.

Vous pouvez soit insérer les lignes O.F. manuellement, soit utiliser la fonction de calcul de ces lignes à partir de l’en-tête.  

> [!NOTE]
> Si vous utilisez la fonction Actualiser pour recalculer des lignes O.F., les anciennes lignes O.F. sont supprimées et de nouvelles lignes sont calculées.  

## Pour replanifier un ordre de fabrication

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  
2. Ouvrez l’ordre de fabrication à replanifier.  
3. Sur le raccourci **Lignes**, choisissez l’action **Lignes**, puis choisissez l’action **Composants**.  
4. Ajoutez un composant qui soit un article produit ou un sous-ensemble.  
5. Dans l’ordre de fabrication, choisissez l’action **Replanifier**.  

    Sur la page **Replanifier O.F.**, définissez la procédure et les éléments à replanifier.  
6. Dans le champ **Direction**, sélectionnez l’une des options suivantes.  

    | Option | Désignation |
    |--|--|
    | **Amont** | Calcule la séquence d’opérations en amont, de la date fin la plus proche possible, définie par la date d’échéance et/ou d’autres commandes planifiées, à la date début la plus éloignée possible. **Note :** cette option par défaut convient à la majorité des cas. |
    | **Aval** | Calcule la séquence d’opérations en aval, de la date début la plus éloignée possible, définie par la date d’échéance et/ou d’autres commandes planifiées, à la date fin la plus proche possible. **Note :** cette option n’est utile que pour les commandes urgentes. |

7. Dans le champ **Planifier**, choisissez l’option correspondant au mode de calcul des exigences de production des articles produits sur la nomenclature, comme suit.  

    |Option|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Aucun niveau**|Ne prenez pas en compte la production de plus bas niveau. Cette option met uniquement à jour la planification de l’article, comme l’actualisation.|  
    |**Un niveau**|Planifie une demande fabrication pour le premier niveau. Des ordres de fabrication de premier niveau peuvent être créés.|  
    |**Tous niveaux**|Planifie une demande fabrication pour tous les niveaux. Des ordres de fabrication multi-niveaux peuvent être créés.|  

8. Sélectionnez **Un niveau**, puis choisissez le bouton **OK** pour replanifier l’ordre de fabrication, et calculer et créer un ordre de fabrication sous-jacent pour le nouveau sous-ensemble, s’il n’est pas totalement disponible.  

> [!NOTE]  
> Les modifications mises en œuvre via la fonction **Replanifier** risquent fortement de modifier la capacité nécessaire de l’ordre de fabrication et de vous obliger à effectuer par la suite une replanification des opérations.  

## Pour actualiser un ordre de fabrication

Si vous avez modifié des lignes O.F., des composants ou des lignes gamme, vous devez aussi actualiser les informations de l’ordre de fabrication. Dans la procédure qui suit, les composants d’un ordre de fabrication planifié ferme sont calculés. La procédure est identique pour les lignes gamme.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifié ferme**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Pour plus d’informations, voir [Créer des ordres de fabrication](production-how-to-create-production-orders.md).  
3. Sélectionnez l’action **Actualiser**.
4. Sur la page **Actualiser O.F.**, sélectionnez l’une des options suivantes :

    |Champ|Option|Description|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Direction**|**Aval**|La planification commence à la date début et se poursuit jusqu’à la date fin. Vous devez renseigner la date début pour pouvoir utiliser cette option.|  
    ||**Amont**|La planification commence à la date fin et remonte jusqu’à la date début.|  
    |**Calculer**|**Lignes**|Sélectionnez ce champ pour calculer les lignes O.F.|  
    ||**Gammes**|Ce champ n’affecte pas le calcul des lignes fabrication.|  
    ||**Besoin composant**|Ce champ n’affecte pas le calcul des lignes fabrication.|  
    |**Entrepôt**|**Créer demande d’enlogement**|Ce champ n’affecte pas le calcul des lignes fabrication.|  

5. Cliquez sur le bouton **OK** pour confirmer votre choix. Les lignes O.F. sont calculées.

> [!NOTE]  
> Le calcul des composants O.F. supprime les modifications précédentes des composants.

## Voir aussi

[Planifié](production-planning.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]