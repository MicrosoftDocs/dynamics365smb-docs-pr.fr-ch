---
title: Consommer en aval des composants en fonction de la production réalisée
description: Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l’ordre de fabrication lancé le statut Terminé.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779268"
---
# <a name="flush-components-according-to-operation-output"></a>Consommer en aval des composants en fonction de la production réalisée
Vous pouvez définir différentes stratégies de rinçage, pour automatiser l'enregistrement de la consommation des composants. 

Par exemple, si un ordre de fabrication de 800 mètres nécessite pour son exécution 8 kilogrammes d’un composant, lorsque vous validez 200 mètres de production, 2 kilogrammes sont automatiquement validés comme étant consommés. 

Cette fonctionnalité est utile pour les motifs suivants :  

- **Évaluation du stock**

    Les écritures de valeur de production et de consommation sont créées parallèlement à l’état d’exécution de l’ordre de fabrication. Sans les codes lien gamme, la valeur du stock augmente lorsque la production est validée, puis réduit ultérieurement lorsque la valeur de la consommation des composants est validée en même temps que l’ordre de fabrication terminé.  
- **Disponibilité stock**

    Avec une validation progressive de la consommation, la disponibilité des composants est mieux actualisée, ce qui est important pour conserver l’équilibre interne entre l’offre et la demande. Sans les codes lien gamme, les autres demandeurs du composant peuvent croire qu’il est disponible tant que la validation de sa consommation reste en attente.  
- **À flux tendu**

    Si vous pouvez personnaliser les produits en fonction des demandes client, vous pouvez réduire les rebuts en vous organisant pour que les procédures de travail et les systèmes ne soient modifiés que lorsque c’est nécessaire.  

Pour y parvenir, combinez la méthode de consommation en amont et les codes lien gamme pour que la quantité consommée par chaque opération soit proportionnelle à la production réelle de cette opération terminée. Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l’ordre de fabrication lancé le statut **Terminé**. Si vous définissez également les codes lien gamme, le calcul et la validation ont lieu lorsque chaque opération est terminée et la quantité effectivement consommée au cours de l’opération est validée. Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Pour consommer en aval des composants en fonction de la production réalisée

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.  
2.  Choisissez l’action **Modifier**.  
3.  Sur le raccourci **Réapprovisionnement**, dans le champ **Méthode consommation**, sélectionnez **En amont**.  

    > [!NOTE]  
    >  Sélectionnez **Prélèvement + Amont** si le composant est utilisé dans un magasin configuré pour un prélèvement et un rangement suggérés.  

4.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Gammes**, puis sélectionnez le lien associé.  
5.  Définir les codes lien gamme pour chaque opération qui consomme le composant. Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > N'utilisez pas le même lien de gamme pour différentes opérations dans la gamme, car cela entraînera l'enregistrement de la consommation de composant pour chaque opération liée.  
6.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Nomenclature production**, puis sélectionnez le lien associé.  
7.  Associe aux codes lien gamme de chaque instance du composant l’opération dans laquelle il est consommé.

La consommation sera affichée automatiquement lorsque vous enregistrez la sortie. Pour plus d’informations, voir [Valider par lots la production et les temps d’exécution](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Méthodes consommation

Le tableau suivant décrit les options de méthode consommation disponibles que vous pouvez spécifier sur les cartes **Article** et **Unité de gestion des stocks**.

|Option|Description|
|------------|-------------|  
|Manuel|Requiert d'entrer et de valider manuellement la consommation dans la feuille consommation.|
|Aval|Valide automatiquement la consommation en fonction des lignes composant O.F. <br><br>Par défaut, la validation de la consommation de composants se produit lorsque vous basculez le statut de l'ordre de fabrication sur **Lancé**. Toutefois, si vous utilisez le champ Code **lien gamme** sur lignes composant O.F., la validation est effectuée par opération lorsque l'opération commence. Pour plus d'informations, reportez-vous à [Comment créer des liens gamme](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Remarque**<br>Pour la consommation en aval, la validation propre à chaque opération que vous obtenez avec des codes lien gamme est basée sur la quantité prévue définie sur la ligne composant. Pour plus d'informations sur la consommation en aval propre à l'opération sur la production réelle, reportez-vous à la description de **Amont** dans cette rubrique.<br><br>Si le magasin ou les ressources utilisant ce composant sont créées avec une structure d'emplacement par défaut, l'article est consommé à partir du **Code emplacement atelier ouvert**. Pour plus d'informations, voir [Procédure : configurer des entrepôts de base avec les zones d'opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Important** <br>La consommation en aval se produit aussi lorsque vous choisissez **Actualiser** sur un ordre de fabrication lancé créé à partir de zéro. Sur ces écritures arrondies des O.F. lancés directement créés, vous ne pouvez pas modifier les informations sur les emplacements car les lignes composant O.F. sont générées lors de l'actualisation de la commande avec consommation en aval simultanée des composants. Toutefois, si vous souhaitez modifier les informations d'emplacement sur les lignes composant O.F. avant que la consommation en aval se produise, cette commande doit être créée avec le statut *Planifié* ou *Planifié ferme*.|
|Amont|Calcule et valide automatiquement la consommation en fonction des lignes composant O.F.<br><br> Par défaut, le calcul et la validation de la consommation de composants se produit lorsque vous basculez le statut de l'ordre de fabrication sur **Terminé**. Toutefois, si vous utilisez le champ **Code lien gamme** sur lignes composant O.F., le calcul et la validation sont effectués à la fin de chaque opération.<br><br> **Remarque** <br>Les codes de consommation en amont et de lien gamme peuvent être combinés afin que la quantité consommée par opération soit proportionnelle à la production réelle de cette opération. Pour plus d'informations, voir [Procédure : consommer en aval des composants en fonction de la production réalisée](#to-flush-components-according-to-operation-output).<br><br> Si le magasin ou le poste de charge utilisant ce composant sont créées avec une structure d'emplacement par défaut, l'article est consommé à partir du **Code emplacement atelier ouvert**.|
|Prélèvement + Aval|Identique à la méthode de consommation en aval, mais ne fonctionne que pour les magasins qui utilisent le prélèvement et le rangement suggérés.<br><br> La consommation est calculée et validée à partir de l'emplacement défini dans le champ **Code empl. des consommations** sur le magasin ou le poste de charge après le prélèvement du composant de l'entrepôt.<br><br> **Remarque** <br>Si un composant est configuré avec le prélèvement et la méthode de consommation en aval, vous ne pouvez pas avoir un code lien gamme pour une opération configurée avec la méthode de consommation en aval. Le composant est ensuite automatiquement consommé lorsque l'opération commence, rendant impossible toute demande d'activité de prélèvement.|
|Prélèvement + Amont|Identique à la méthode de consommation en amont, mais ne fonctionne que pour les magasins qui utilisent le prélèvement et le rangement suggérés.<br><br> La consommation est calculée et validée à partir de l'emplacement défini dans le champ **Code empl. des consommations** sur le magasin ou le poste de charge après le prélèvement du composant de l'entrepôt.|

## <a name="see-also"></a>Voir aussi

[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
