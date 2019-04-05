---
title: Procédure de consommation en aval des composants en fonction de la production réalisée | Microsoft Docs
description: Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l'ordre de fabrication lancé le statut **Terminé**. Pour plus d'informations, voir Méthode consommation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 53f2dac9a2ea3b2ec44827e8404abfd10d03e32a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820600"
---
# <a name="flush-components-according-to-operation-output"></a>Consommer en aval des composants en fonction de la production réalisée
Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l'ordre de fabrication lancé le statut **Terminé**.  

Si vous définissez également les codes lien gamme, le calcul et la validation ont lieu lorsque chaque opération est terminée et la quantité effectivement consommée au cours de l'opération est validée. Pour plus d'informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  

Par exemple, si un ordre de fabrication de 800 mètres nécessite pour son exécution 8 kilogrammes d'un composant, lorsque vous validez 200 mètres de production, 2 kilogrammes sont automatiquement validés comme étant consommés.  

Cette fonctionnalité est utile pour les motifs suivants :  

-   **Évaluation du stock** - Les écritures de valeur de production et de consommation sont créées parallèlement à l'état d'exécution de l'ordre de fabrication. Sans les codes lien gamme, la valeur du stock augmente lorsque la production est validée, puis réduit ultérieurement lorsque la valeur de la consommation des composants est validée en même temps que l'ordre de fabrication terminé.  
-   **Disponibilité du stock** - Avec une validation progressive de la consommation, la disponibilité des composants est mieux actualisée, ce qui est important pour conserver l'équilibre interne entre l'offre et la demande. Sans les codes lien gamme, les autres demandeurs du composant peuvent croire qu'il est disponible tant que la validation de sa consommation reste en attente.  
-   **Just-in-Time** - Si vous pouvez personnaliser les produits en fonction des demandes client, vous pouvez réduire les rebuts en vous organisant pour que les procédures de travail et les systèmes ne soient modifiés que lorsque c'est nécessaire.  

La procédure suivante montre comment combiner la consommation en amont et les codes lien gamme pour que la quantité consommée par chaque opération soit proportionnelle à la production réelle de cette opération terminée.  

## <a name="to-flush-components-according-to-operation-output"></a>Pour consommer en aval des composants en fonction de la production réalisée  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.  
2.  Choisissez l'action **Modifier**.  
3.  Sur le raccourci **Réapprovisionnement**, dans le champ **Méthode consommation**, sélectionnez **En aval**.  

    > [!NOTE]  
    >  Sélectionnez **Prélèvement + Aval** si le composant est utilisé dans un magasin configuré pour un prélèvement et un rangement suggérés.  

4.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Gammes**, puis sélectionnez le lien associé.  
5.  Définir les codes lien gamme pour chaque opération qui consomme le composant. Pour plus d'informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  
6.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Nomenclature de production**, puis sélectionnez le lien associé.  
7.  Associe aux codes lien gamme de chaque instance du composant l'opération dans laquelle il est consommé.

    > [!IMPORTANT]  
    >  Le composant doit avoir un lien gamme l'associant à la dernière opération de la gamme.  

## <a name="see-also"></a>Voir aussi  
[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[Planifié](production-planning.md)   
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
