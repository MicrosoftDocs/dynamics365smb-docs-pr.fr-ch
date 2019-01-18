---
title: "Procédure de configuration des coûts associés | Microsoft Docs"
description: "Découvrez comment configurer les coûts associés, qui sont similaires aux axes analytiques pour la comptabilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 616fcbe937e556c17e8beb79f68bc961ea8bbe18
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-cost-objects"></a>Configurer les coûts associés
Les coûts associés sont les projets, les biens ou les services d'une société. Le plan des coûts associés est semblable aux informations sur l'axe analytique pour la comptabilité. Vous pouvez configurer le plan des coûts associés comme suit :  

* Transférez des sections analytiques de la comptabilité vers le plan comptable des coûts associés. Vous pouvez effectuer tous les ajustements nécessaires après le transfert.  
* Créez un nouveau plan des coûts associés, qui est indépendant de la comptabilité ou ajoutez un nouveau coût associé à un plan existant des coûts associés. Vous devez créer chaque coût associé individuellement.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Pour transférer des sections analytiques depuis la comptabilité vers le plan comptable des coûts associés  
1.  Définissez un axe analytique pour être celui des coûts associés sur la page **Actualiser axes analytiques CA**. Seules les valeurs de cet axe analytique sont transférées.  
2.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable des coûts associés**, puis sélectionnez le lien associé.  
3.  Choisissez l'action **Extraire les coûts associés de l'axe analytique** pour transférer des sections analytiques du plan comptable de coûts associés. La fonction transfère les axes analytiques que vous avez définis dans l'étape 1.  

    > [!NOTE]  
    >  Vous pouvez configurer le champ **Aligner axe coûts associés** pour définir la synchronisation unidirectionnelle des sections analytiques à partir de la comptabilité vers le plan des coûts associés. Vous ne pouvez pas définir une synchronisation du plan de coûts associés avec les sections analytiques issues de la comptabilité.  

Le plan comptable de coûts associés comprend désormais toutes les sections analytiques spécifiées provenant de la comptabilité. Il inclut les titres et les sous-totaux.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Pour créer de nouveaux coûts associés sur la page Plan comptable des coûts associés  
Vous pouvez configurer et gérer les coûts associés, soit sur la page **Fiche coûts associés**, soit sur la page **Plan comptable des coûts associés**. Dans cette procédure, vous configurez de nouveaux coûts associés sur la page **Plan comptable des coûts associés**.  

1.  Ouvrez la page **Plan comptable des coûts associés** en mode édition.  
2.  Dans le champ **Code**, entrez le code coût associé. Tous les coûts associés doivent avoir un code.  
3.  Dans le champ **Nom**, saisissez le nom du coût associé.  
4.  Sélectionnez la flèche déroulante dans le champ **Type ligne** pour spécifier l'objectif du coût associé.  

    * Pour les coûts associés de type de ligne **Total**, renseignez le champ **Total De/À**. Utilisez l'opérateur **or**, qui est une ligne verticale (**&#124;**), pour définir les plages des coûts associés.  
    * Pour les coûts associés de type de ligne **Fin total**, ce champ est renseigné automatiquement lorsque vous utilisez la fonction d'indentation.  
5.  Renseignez le champ **Ordre de tri**.  
6.  Choisissez la ligne vide suivante pour créer un coût associé, puis répétez les étapes 2 à 5.  
7.  Après avoir défini tous les coûts associés, choisissez l'action **Indenter les coûts associés**. Cliquez sur le bouton **Oui**.  

> [!IMPORTANT]  
>  Si vous avez saisi des définitions dans les champs **Total De/À** pour les coûts associés **Fin total** avant d'exécuter la fonction d'indentation, vous devez les saisir à nouveau. La fonction remplace les valeurs dans tous les champs **Fin total**.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Définition des centres de coûts et des coûts associés pour le plan comptable](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Soldes entre le type de coût, un centre de coûts et les coûts associés](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)   
[Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)   
[À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

