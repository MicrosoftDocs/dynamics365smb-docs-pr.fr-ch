---
title: "Procédure de configuration des centres de coûts | Microsoft Docs"
description: "Les centres de coûts sont les départements responsables des coûts et des revenus. Le plan des centres de coûts est semblable aux informations sur l'axe analytique pour la comptabilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 38b6ce01e48f1b32c28b1883875a566d19f02ea3
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-cost-centers"></a>Configuration des centres de coûts
Les centres de coûts sont les départements responsables des coûts et des revenus. Le plan des centres de coûts est semblable aux informations sur l'axe analytique pour la comptabilité. Vous pouvez configurer le plan des centres de coûts comme suit :  

-   Transférez des sections analytiques de la comptabilité vers le plan des centres de coûts. Vous pouvez effectuer tous les ajustements nécessaires après le transfert.  
-   Créez un nouveau plan du centre de coûts, qui est indépendant de la comptabilité ou ajoutez un nouveau centre de coûts à un plan existant du centre de coûts. Vous devez créer chaque centre de coûts individuellement.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Pour transférer des sections analytiques de la comptabilité vers le plan des centres de coûts.  
1.  Définissez un axe analytique pour être celui de la dimension des centres de coûts dans la fenêtre **Mettre à jour les axes analytiques de comptabilité analytique**. Seules les valeurs de cet axe analytique sont transférées.  
2.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable des centres de coûts**, puis sélectionnez le lien connexe.  
3.  Sous l'onglet **Actions**, dans le groupe **Fonctions**, choisissez **Extraire les centres de coûts de l'axe analytique** pour transférer des sections du plan des centres de coûts. La fonction transfère les sections analytiques que vous avez définis dans l'étape 1.  

    > [!NOTE]  
    >  Vous pouvez configurer le champ **Aligner axe centre de coûts** pour définir la synchronisation unidirectionnelle des sections analytiques à partir de la comptabilité vers le plan des centres de coûts. Vous ne pouvez pas définir une synchronisation du plan des centres de coûts avec les sections analytiques issues de la comptabilité.  

Le plan des centres de coûts comprend désormais toutes les sections analytiques spécifiées provenant de la comptabilité. Il inclut les titres et les sous-totaux.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Pour créer de nouveaux centres de coût dans la fenêtre Plan comptable des centres de coûts  
Vous pouvez configurer et gérer les centres de coût, soit dans la fenêtre **Fiche centre de coût**, soit dans la fenêtre **Plan comptable des centres de coûts**. Dans cette procédure, vous configurez de nouveaux centres de coût dans la fenêtre **Plan comptable des centres de coûts**.  

1. Ouvrez la fenêtre **Plan comptable des centres de coûts** en mode édition.  
2. Dans le champ **Code**, entrez le code centre de coûts. Tous les centres de coûts doivent avoir un code.  
3. Dans le champ **Nom**, saisissez le nom du centre de coûts.  
4. Sélectionnez la flèche déroulante dans le champ **Type ligne** pour spécifier l'objectif du centre de coûts.  

    - Pour les centres de coûts de type **Total**, vous devez renseigner le champ **Totalisation**. Utilisez l'opérateur **or**, qui est une ligne verticale (**&#124;**) pour définir les plages des centres de coûts.  
    - Pour les centres de coûts de type de ligne **Fin total**, ce champ est renseigné automatiquement lorsque vous utilisez la fonction d'indentation.  
5.  Renseignez les champs **Ordre de tri** et **Sous-type coût**.  
6.  Choisissez la ligne vide suivante pour créer un centre de coûts, puis répétez les étapes 2 à 5.  
7.  Après avoir défini tous les centres de coûts, choisissez l'action **Indenter les centres de coûts**. Cliquez sur le bouton **Oui**.  

> [!IMPORTANT]  
>  Si vous avez saisi des définitions dans les champs **Totalisation** pour les centres de coûts **Fin total** avant d'exécuter la fonction d'indentation, vous devez les saisir à nouveau. La fonction remplace les valeurs dans tous les champs **Fin total**.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)   
[Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)   
[À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

