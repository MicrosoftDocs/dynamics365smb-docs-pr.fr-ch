---
title: "Enregistrer l'utilisation facturable et budgétée des ressources de projet| Microsoft Docs"
description: "Décrit comment enregistrer la consommation ou l'utilisation des articles ou des ressources sur des projets pour faciliter la gestion de projets."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b0bd4f9a4c0963520631e1571fd182adce85fdd9
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="record-usage-for-jobs"></a>Enregistrer l'utilisation pour les projets
Dans la fenêtre **Lignes planning projet**, vous pouvez consulter et enregistrer l'activité sur les différentes parties de votre projet, qui est automatiquement mis à jour lorsque vous modifiez et transférez des informations entre les projets et les feuilles projet ou les factures projet. Cela suppose d'avoir paramétré un projet afin que **Appliquer le lien d'utilisation** soit activé. Pour plus d'informations, voir [Configuration de projets](projects-how-setup-jobs.md).  

Par exemple, pour les lignes planning de type **Budget**, vous pouvez saisir la quantité d'une ressource et indiquer la quantité à transférer vers la feuille projet. Si le type de la ligne planning est **Facturable**, vous pouvez saisir la quantité de la ressource et indiquer la quantité à transférer vers une facture. En comparant la quantité qui a été transférée vers la feuille ou la facture avec la quantité restante, vous pouvez rapidement vérifier les informations sur l'activité.

Les procédures suivantes décrivent comment enregistrer les prix et les coûts réels (facturables) ou budgétés du projet. Pour plus d'informations sur l'estimation des valeurs budgétées lors de la planification, voir [Gérer les budgets de projets](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Pour enregistrer l'activité d'une ligne planning projet de type Budget
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis cliquez sur **Lignes planning projet**.
3. Sélectionnez une ligne planning projet de type **Budget** ou **Budget et Facturable** pour laquelle vous voulez enregistrer une activité.
4. Dans le champ **Qté à transférer sur la feuille**, entrez le nombre que vous souhaitez transférer vers la facture. La quantité par défaut est la même valeur que celle du champ **Quantité**.

    Le champ **Quantité restante** indique la quantité qui reste pour terminer le projet et à transférer à la feuille.  
5. Choisissez l'action **Créer des lignes feuille projet**.
6. Dans la fenêtre **Projet Transférer la ligne planning projet**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Cliquez sur **Ouvrir la feuille projet**.  
8. Dans la fenêtre **Feuille projet**, sélectionnez la ligne appropriée, puis cliquez sur **Valider**.
9. Dans la fenêtre **Lignes planning projet**, examinez l'activité enregistrée en observant les champs **Quantité**, **Quantité restante** et **Qté à transférer sur la feuille**.  
10. Répétez les étapes 3 à 8 pour enregistrer l'activité supplémentaire.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Pour enregistrer l'activité d'une ligne planning projet de type Facturable
Dans la tâche suivante, vous devez aussi enregistrer l'activité, mais pour une ligne planning projet de type **Facturable**. En général, dans ce cas, vous facturez votre activité, mais vous pouvez également la transférer vers une feuille. Néanmoins, lorsque vous faites cela, une ligne planning projet de type **Budget** est créée pour correspondre à la ligne facturable. Pour en savoir plus, voir [Gérer les budgets de projets](projects-how-manage-budgets.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.
2. Sélectionnez le projet concerné, puis cliquez sur **Lignes planning projet**.  
3. Sélectionnez une ligne planning projet de type **Facturable** pour laquelle vous voulez enregistrer une activité.
4. Dans le champ **Qté à transférer à facturer**, entrez le nombre que vous souhaitez transférer vers la facture. La quantité par défaut est la même valeur que celle du champ **Quantité**.

    Le champ **Quantité à facturer** indique la quantité restante pour terminer le projet et qui doit être facturée.  
5. Cliquez sur **Créer facture vente**.
6. Dans la fenêtre **Projet Transférer vers facture vente**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.
7. Dans la fenêtre **Lignes planning projet**, sélectionnez la ligne appropriée, puis cliquez sur **Valider**.
8. Examinez l'activité enregistrée en observant les champs **Quantité**, **Quantité à facturer**, **Qté à transférer à facturer** et vérifiez si la facture vente est validée, ainsi que les champs **Qté facturée**.
9. Répétez les étapes 3 à 8 pour enregistrer l'activité supplémentaire.  
10. Pour passer en revue une facture vente validée associée, cliquez sur **Avoirs/Factures vente**.  
11. Dans la fenêtre **Factures projet**, sélectionnez la facture appropriée et cliquez sur **Ouvrir la facture vente/l'avoir**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Pour créer des lignes feuille projet à partir de lignes planning projet
Lorsque vous êtes prêt à valider les données financières pour les projets, vous devez créer des lignes feuilles projets que vous pouvez valider.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez un projet concerné, puis cliquez sur **Lignes planning projet**.  
3. Dans la fenêtre **Lignes planning projet**, sur la ligne planning projet souhaitée, dans le champ **Qté à transférer sur la feuille**, entrez la quantité que vous souhaitez transférer vers une feuille projet.  
4. Choisissez l'action **Créer des lignes feuille projet**.
5. Dans la fenêtre **Projet Transférer la ligne planning projet**, renseignez les champs selon vos besoins.  
6. Cliquez sur le bouton **OK**. Des lignes feuille projet sont créées.
7. Pour vérifier le transfert, ouvrez la feuille projet appropriée et vérifiez les écritures.  
8. Lorsque les lignes feuilles projets sont renseignées, cliquez sur **Valider**.  

## <a name="to-create-job-journal-lines-manually"></a>Pour créer des lignes feuille projet manuellement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles projet**, puis sélectionnez le lien connexe.  
2. Dans le champ **Nom de la feuille**, choisissez un nom de feuille projet approprié.  
3. Dans une nouvelle ligne, entrez le numéro de document, le numéro de projet, le numéro tâche projet, le type et la quantité du type consommé.  
4. Lorsque les lignes feuilles projets sont renseignées, cliquez sur **Valider**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Pour consulter les lignes planning pour une écriture comptable projet
Après avoir validé les lignes feuilles projets, vous pouvez voir les lignes planning associées à des écritures de la feuille projet qui ont été validées.

> [!NOTE]  
>   Cela nécessite que le champ **Appliquer le lien d'utilisation** ait été sélectionné pour le projet, ou qu'il s'agisse de la configuration par défaut pour tous les projets de votre organisation. Pour plus d'informations, voir [Configuration de projets](projects-how-setup-jobs.md).  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles projet**, puis sélectionnez le lien connexe.  
2. Sélectionnez une feuille projet appropriée, puis cliquez sur **Écritures comptables**.  
3. Dans la fenêtre **Écritures comptables projet**, cliquez sur **Afficher les lignes planning projet liées**.

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

