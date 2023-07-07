---
title: Enregistrer la consommation ou l′utilisation des articles et des ressources du projet
description: Cet article décrit comment enregistrer la consommation ou l’utilisation des articles ou des ressources pour des projets dans la gestion de projets.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-jobs"></a>Enregistrer la consommation ou l′utilisation pour les projets

À partir de la page **Fiche projet**, vous pouvez ouvrir la page **Lignes planning projet** pour examiner et enregistrer l’utilisation sur diverses composantes de votre projet. Ces informations sont automatiquement mises à jour lorsque vous modifiez et transférez des informations entre projets et entre feuilles projet et factures projet. Cela nécessite que vous activiez le bouton à bascule **Appliquer le lien d’utilisation par défaut** sur la page **Configuration projet**. Learn more at [Configuration de projets](projects-how-setup-jobs.md).  

Par exemple, pour les lignes planning de type **Budget**, vous pouvez saisir la quantité d’une ressource, puis indiquer la quantité à transférer vers la feuille projet. Si le type de la ligne planning est **Facturable**, vous pouvez saisir la quantité de la ressource, puis indiquer la quantité à transférer vers une facture. Pour en savoir plus sur la facturation du client, consultez [Facturation des projets](projects-how-invoice-jobs.md). En comparant la quantité d′origine, la quantité restante ou la quantité validée, vous pouvez rapidement examiner les informations d′utilisation. Pour en savoir plus sur l’estimation des valeurs budgétées lors de la planification, consultez [Gérer les budgets de projets](projects-how-manage-budgets.md).  

Les procédures suivantes décrivent comment enregistrer les quantités (budgétées) et les coûts réels avec une feuille projet. Sinon, vous pouvez utiliser les documents achat pour enregistrer les achats pour un projet. Learn more at [Gérer les fournitures pour un projet](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Pour enregistrer l’utilisation d’une ligne planning projet de type Budget

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet, puis sélectionnez l’action **Lignes planning projet**. 
3. Sélectionnez une ligne planning projet de type **Budget** ou **Budget et Facturable** pour laquelle vous voulez enregistrer une utilisation.   

    > [!NOTE]
    > Vous pouvez également enregistrer l’utilisation d′une ligne planning projet de type **Facturable**. En général, vous utilisez ces lignes pour créer des factures, mais vous pouvez également transférer les informations vers une feuille. Learn more at [Facturation des projets](projects-how-invoice-jobs.md) 

4. Dans le champ **Qté à transférer sur la feuille**, entrez la quantité à transférer. La quantité par défaut est la même valeur que celle du champ **Quantité**.

    Le champ **Quantité restante** indique la quantité qui reste pour terminer le projet et à transférer à la feuille.
5. Choisissez l’action **Créer des lignes feuille projet**.

    > [!TIP]
    > Si vous allez ajouter d’autres lignes planning projet pour ce projet, attendez avec cette étape jusqu’à ce que vous ayez ajouté toutes les lignes planning projet.
6. Sur la page **Projet Transférer la ligne planning projet**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Cliquez sur **Ouvrir la feuille projet**.  
8. Sur la page **Feuille projet**, sélectionnez la ligne appropriée, puis cliquez sur **Valider**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Sur la page **Lignes planning projet**, examinez l’utilisation enregistrée en observant les champs **Quantité**, **Quantité restante** et **Qté à transférer sur la feuille**.  
10. Répétez les étapes 3 à 8 pour enregistrer l’utilisation supplémentaire.  

## <a name="to-create-job-journal-lines-manually"></a>Pour créer des lignes feuille projet manuellement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles projet**, puis choisissez le lien associé.  
2. Dans le champ **Nom de la feuille**, choisissez un nom de feuille projet approprié.  
3. Dans une nouvelle ligne, entrez le numéro de document, le numéro de projet, le numéro tâche projet, le type et la quantité du type consommé.  
4. Lorsque les lignes feuilles projets sont renseignées, cliquez sur **Valider**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Pour visualiser les estimations projet et valider les mises à jour

Vous pouvez visualiser l′utilisation projet jusqu’à son achèvement en une étape. Pour ce faire, utilisez le traitement par lots **Projet Calc. utilisation restante** pour toutes les tâches jusqu’à la fin du projet.  

Cela vous permet de suivre vos estimations initiales, de les comparer aux résultats réels, ainsi que d’apporter des modifications et d’ajouter de nouvelles écritures, selon les besoins. Par exemple, alors que vous aviez estimé qu’un projet nécessitait 10 heures de travail, vous en avez effectué 15. Vous pouvez ajouter les cinq heures supplémentaires à la ligne feuille existante ou créer une ligne feuille pour les déclarer en tant qu’heures supplémentaires, ce qui constitue un autre type de tâche. Le coût et le prix appropriés sont calculés. Vous pouvez les valider dans la feuille.  

> [!NOTE]  
> Les écritures article créent des écritures comptables article et diminuent les articles en stock. Le traitement par lots **Valider coûts ajustés** permet de transférer le coût du stock à la comptabilité. Les écritures ressource créent des écritures comptables ressource.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles projet**, puis choisissez le lien associé.  
2. Sélectionnez une feuille projet appropriée, puis cliquez sur l’action **Calc. utilisation restante**.  
3. Sur la page **Projet Calc. utilisation restante**, entrez le numéro et la date de comptabilisation du document devant être insérés dans la feuille, puis sélectionnez le bouton **OK**.  
4. Mettez à jour la feuille avec toutes les modifications qui peuvent être nécessaires.  
5. Sélectionnez l’action **Valider**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Créez des documents prélèvement entrepôt et stock pour un projet

Pour créer des documents de prélèvement entrepôt et stock pour les projets, votre administrateur doit activer **Mise à jour des fonctionnalités : activer prélèvement stock et entrepôt à partir des projets** sur la page **Gestion des fonctionnalités**.

La fonctionnalité ajoute les actions **Créer un prélèvement stock** et **Créer un prélèvement entrepôt** à la **Fiche projet**. Pour créer ou enregistrer un document de prélèvement, utilisez les actions **Rangement/Lignes prélèvement/Lignes Mouvements** ou **Lignes prélèvement enregistrées**. Learn more at [Flux pour la production, l’assemblage et les projets](design-details-internal-warehouse-flows.md).

Vous pouvez utiliser les actions dans les conditions suivantes :

* Le **Statut** du projet est **Ouvert**.
* Le **Type de ligne** de la ligne de planning du projet est **Budget** ou **Budget et Facturable**.
* Le **Type** de la ligne de planning du projet est **Article**.
* **Prélèvement requis** est activé pour l’emplacement associé.
* **Prélèv. et rangement dirigés** est désactivé.

> [!NOTE] 
> Bien que le paramètre s’appelle **Prélèvement requis**, vous pouvez toujours valider la consommation directement à partir de la ligne du journal des tâches pour l’emplacement. Si votre magasin est configuré pour exiger un traitement des prélèvements mais pas des expéditions, utilisez la page **Prélèvement stock** pour organiser et imprimer les informations de prélèvement. Vous utilisez également la page pour saisir et afficher le résultat du prélèvement, qui à son tour affiche la consommation des articles. 
> 
> Lorsque le magasin est configuré pour appeler un traitement de prélèvement et d’expédition, ce qui implique que vous avez activé les champs **Prélèvement requis** et **Expédition requise** sur la page **Fiche magasin**, utilisez le document **Prélèvement entrepôt** pour gérer le retrait. Les prélèvements entrepôt sont similaires aux prélèvements stock. La différence est qu’au lieu d’afficher les informations de prélèvement, vous enregistrez le prélèvement. Ce processus d’enregistrement ne valide pas la consommation, il rend simplement les articles disponibles pour la validation. En tant que responsable d’entrepôt, vous pouvez utiliser une feuille de calcul pour organiser les informations de prélèvement avant de créer les instructions de prélèvement d’entrepôt individuelles

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Pour consulter les lignes planning pour une écriture comptable projet

Après avoir validé les lignes feuilles projets, vous pouvez voir les lignes planning associées à des écritures de la feuille projet qui ont été validées.

> [!NOTE]  
> Cela nécessite que la case **Appliquer le lien d′utilisation** soit cochée pour le projet. Pour plus d’informations, voir [Configuration de projets](projects-how-setup-jobs.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles projet**, puis choisissez le lien associé.  
2. Sélectionnez une feuille projet appropriée, puis cliquez sur **Écritures comptables**.  
3. Sur la page **Écritures comptables projet**, cliquez sur **Afficher les lignes planning projet liées**.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/post-job-usage-sales/) associée

## <a name="see-also"></a>Voir aussi

[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Procédure d’achat](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
