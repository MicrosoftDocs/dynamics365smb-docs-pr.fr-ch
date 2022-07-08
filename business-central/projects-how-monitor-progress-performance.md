---
title: Surveiller la progression et les performances
description: Décrit la manière dont vous pouvez créer une méthode de travaux en cours (TEC) et calculer les TEC pour estimer la valeur financière des projets lorsqu’ils sont en cours.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ee69503fa830d21ed433e88c3d8f55a42a4ec1bb
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074681"
---
# <a name="monitor-job-progress-and-performance"></a>Surveiller la progression et les performances

Au fur et à mesure de la progression du projet, les matières, ressources et autres frais sont consommés et doivent être validés dans le projet. La fonctionnalité Travaux en cours (TEC) permet d’estimer la valeur financière des projets dans la comptabilité au cours des projets. Dans de nombreux cas, vous pouvez valider les frais pour un projet avant de le facturer. Lorsque seuls les frais sont validés, l’état financier est incorrect. Pour en savoir plus, reportez-vous à [Comprendre les méthodes TEC](projects-understanding-wip.md).

Pour effectuer le suivi de la valeur dans la comptabilité, vous pouvez calculer les TEC et valider la valeur en comptabilité.

Vous pouvez calculer les TEC sur la base des éléments suivants :

* Valeur de coût
* Valeur des ventes
* Coût identifiable
* Pourcentage avancement
* Fin de contrat

Pour afficher le résultat avec une autre méthode, vous pouvez modifier la méthode et calculer les TEC de nouveau. Le calcul des TEC peut être exécuté un nombre illimité de fois. Le TEC est uniquement calculé, il n’est pas validé dans la comptabilité. Une fois les TEC calculés, vous pouvez effectuer une validation dans la comptabilité.

## <a name="to-create-a-job-wip-method"></a>Pour créer une méthode TEC projet

Vous pouvez créer une méthode TEC projet qui reflète les besoins de votre organisation. Après l’avoir créée, vous pouvez la configurer comme méthode par défaut de calcul TEC projet qui sera utilisée dans votre organisation.  

> [!NOTE]
> Après avoir utilisé la nouvelle méthode pour créer des écritures TEC, vous ne pouvez pas supprimer la méthode ou la modifier.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Méthodes TEC projet**, puis choisissez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Fermez la page.   
4. Pour faire de cette nouvelle méthode la méthode par défaut, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres projets**, puis choisissez le lien associé.  
5. Dans le champ **Méthode TEC par défaut**, choisissez la méthode de la liste.

## <a name="to-define-a-wip-method-for-a-job"></a>Pour définir une méthode TEC pour un projet

Lorsque vous créez un projet, vous devez spécifier la méthode TEC projet qui s’applique. Dans certains cas, quelle méthode TEC projet utilisable a été paramétrée pour vous par défaut.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**. Pour plus d’informations, voir [Créer des projets](projects-how-create-jobs.md).  
3. Sur la page **Fiche projet**, dans le champ **Méthode TEC**, sélectionnez une méthode TEC dans la liste. Si une méthode par défaut a été définie, vous pouvez sélectionner une autre option si nécessaire.  

## <a name="to-calculate-wip"></a>Pour calculer les TEC :

Vous pouvez déterminer le montant TEC devant être validé dans les comptes de bilan pour la génération d’états de clôture d’exercice. Pour ce faire, utilisez le traitement par lots **Projet Calculer TEC**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Projet calculer TEC**, puis choisissez le lien associé.  
2. Cliquez sur **Calculer TEC**.
3. Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.
4. Choisissez le bouton **OK**.  

> [!NOTE]  
>   Le traitement par lots calcule uniquement les TEC. Il n’est pas validé dans la comptabilité. Pour ce faire, exécutez le traitement par lots **Valider TEC en compta.** à l’issue du calcul. Pour plus d’informations, voir la procédure suivante.

## <a name="to-post-wip"></a>Pour valider les TEC

Quand vous avez calculé les TEC, vous pouvez les valider pour équilibrer les comptes bilan pour le reporting de fin de période. Pour ce faire, utilisez le traitement par lots **Projet Valider TEC en comptabilité**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Projet Valider TEC en comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.  
3. Cliquez sur le bouton **OK**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Pour calculer et valider les écritures d’achèvement du projet

À la fin des activités d’un projet (validation et facturation comprises), vous devez le mettre à jour pour définir le **Statut** du projet sur **Terminé**. Ensuite, vous devez contrepasser tous les travaux en cours validés antérieurement dans la comptabilité.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez un projet ouvert, puis cliquez sur **Modifier**.
3. Dans le champ **Statut**, sélectionnez **Terminé**.
4. Suivez les étapes d’aide pour calculer et valider les travaux en cours. Sinon, suivez les étapes 5 et 6 pour le faire manuellement.  
5. Cliquez sur **Calculer TEC**.
6. Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.  

     Les écritures TEC projet créées par le traitement par lots auront la case **Projet terminé** cochée pour indiquer qu’il s’agit d’écritures d’achèvement.  
7. Cliquez sur **Projet Valider TEC en comptabilité**.
8. Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.  

     Les écritures comptabilité TEC projet créées par le traitement par lots verront la case **Projet terminé** cochée pour indiquer qu’il s’agit d’écritures d’achèvement.

## <a name="to-view-job-ledger-entries"></a>Pour visualiser des écritures comptables projet

Toutes les écritures liées à des projets sont enregistrées dans des historiques des transactions projet et sont numérotées de manière séquentielle à partir de 1. L’historique des transactions projet permet d’obtenir un aperçu de toutes les écritures comptables projet.    

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Registres projet**, puis choisissez le lien associé.
2. Sélectionnez un historique approprié, puis cliquez sur **Écritures projet**

Sur la page **Écritures comptables projet** vous pouvez passer en revue les écritures associées à un projet.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/calculate-post-job-wip/)

## <a name="see-also"></a>Voir aussi

[Gestion des projets](projects-manage-projects.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
