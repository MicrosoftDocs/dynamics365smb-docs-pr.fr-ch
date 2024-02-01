---
title: Valider plusieurs documents en même temps
description: Découvrez comment sélectionner plusieurs documents non validés dans une liste pour une validation par lots immédiate ou planifiée dans Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: null
ms.reviewer: bholtorf
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="post-multiple-documents-at-the-same-time"></a>Valider plusieurs documents en même temps

Au lieu de valider des documents individuels un par un, vous pouvez sélectionner plusieurs documents non validés dans une liste pour une validation immédiate ou une validation par lot, conformément à une planification, à la fin de la journée, par exemple. Cela peut être utile si seul un superviseur peut valider des documents créés par d’autres utilisateurs ou pour éviter des problèmes de performance du système liés à la validation pendant les heures de travail.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Pour valider plusieurs commandes achat immédiatement

La procédure suivante explique comment valider immédiatement plusieurs commandes achat. Les étapes sont similaires pour tous les documents achat et vente.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.
2. Sur la page **Commandes achat**, sélectionnez toutes les commandes à valider :
3. Dans le champ **N°**, choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage**.
4. Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.
5. Choisissez l’action **Validation**, puis sélectionnez l’action **Valider**.
6. Cliquez sur le bouton **Oui** dans le message de confirmation.

## <a name="to-batch-post-multiple-purchase-orders"></a>Pour valider plusieurs commandes achat par lots

La procédure suivante explique comment valider plusieurs commandes achat par lots. Les étapes sont similaires pour tous les documents d’achat et de vente où l’action **Valider par lots** est disponible.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
2. Sur la page **Commandes achat**, sélectionnez toutes les commandes à valider :
3. Dans le champ **N°**, choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage**.
4. Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.
5. Choisissez l’action **Validation**, puis sélectionnez l’action **Valider par lot**.
6. Sur la page **TPL validation commandes achat**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Cliquez sur le bouton **OK**.
8. Pour afficher les problèmes potentiels survenus lors de l’enregistrement par lots de documents, ouvrez la page **Registre des messages d’erreur**.

> [!NOTE]
> La validation de plusieurs documents peut prendre un certain temps et bloquer d’autres utilisateurs. Envisagez d’activer la validation en arrière-plan. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Pour paramétrer la validation en arrière-plan avec les files d’attente des travaux
Les files d’attente des travaux sont un outil efficace pour planifier l’exécution des processus d’entreprises en arrière-plan, par exemple lorsque plusieurs utilisateurs essaient de valider des commandes vente, mais uniquement une commande à la fois.  

La procédure suivante explique comment configurer la validation en arrière-plan des commandes vente. La procédure est identique pour les achats.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.
2. Sur la page **Paramètres ventes**, activez la case à cocher **Valider avec la file d’attente des travaux**.
3. Choisissez le champ **Code catégorie de la file d’attente des travaux**, puis spécifiez le code **SALESPOST**.

    > [!NOTE]
    > Certains travaux modifient les données identiques et ne doivent pas s’exécuter en simultané, car cela peut provoquer des conflits. Par exemple, les travaux d’arrière-plan des documents de vente tentent de modifier les données identiques en simultané. Les catégories de files d’attente des travaux permettent d’éviter ces types de conflits en garantissant que lorsqu’un travail est en cours d’exécution, un autre travail appartenant à la même catégorie de file d’attente des travaux ne s’exécutera pas avant la fin. Par exemple, un travail relevant d’une catégorie de file d’attente des travaux de vente attendra que tous les autres travaux liés aux ventes soient terminés. Vous spécifiez une catégorie de file d’attente des travaux sur le raccourci **Validation en arrière-plan** sur la page **Paramètre ventes**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] fournit des catégories de file d’attente des travaux pour les ventes, les achats et la comptabilité générale. Nous recommandons que l’une d’entre elles, ou celle que vous créez, soit toujours spécifiée. Si vous rencontrez des échecs en raison de conflits, pensez à configurer une catégorie pour toutes les ventes, les achats et la validation comptable en arrière-plan.

    Si vous souhaitez également que des documents vente soient imprimés lorsqu’ils sont validés, sélectionnez la case à cocher **Valider et imprimer avec la file d’attente des travaux** sur la page **Paramètres ventes**.  
    Si vous sélectionnez **PDF** dans le champ **Type sortie état**, les bons de commande validés avec succès seront disponibles dans la partie **boîte de réception état** de votre tableau de bord.

    > [!IMPORTANT]  
    > Si vous paramétrez un projet qui valide et imprime des documents et que l’imprimante affiche une boîte de dialogue, par exemple une demande d’informations d’identification ou un alerte à propos de la quantité faible d’encre, votre document est validé mais non imprimé. L’écriture file d’attente de travaux correspondante expire et la valeur du champ **Statut** devient **Erreur**. Par conséquent, nous vous recommandons de ne pas utiliser une configuration de l’imprimante nécessitant une interaction avec les boîtes de dialogue de l’imprimante relatives à la validation en arrière-plan.

    La prochaine fois que vous publiez des documents de vente, [!INCLUDE [prod_short](includes/prod_short.md)] crée automatiquement une entrée de file d’attente des travaux pour chaque document et exécute les travaux en arrière-plan, un par un.

4. Pour vérifier que la file d’attente des travaux fonctionne comme prévu, validez une commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
    Les commandes vente seront désormais ajoutées à une entrée de file d’attente de travaux dédiée, qui définit le moment où les documents sont validés. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Pour afficher un statut dans un document vente ou achat
Si la file d’attente des travaux ne peut pas valider la commande vente, le statut passe à **Erreur**, et la commande vente est ajoutée à la liste des commandes vente que l’utilisateur doit traiter.
1. Dans le document que vous avez essayé de valider avec la validation en arrière-plan, choisissez le champ **Statut de la file d’attente des travaux**, qui contient **Erreur**.
2. Examinez le message d’erreur et résolvez le problème.

Sinon, vous pouvez vérifier sur la page **Écritures journal file d’attente des travaux** si la commande vente a été validée avec succès. Pour plus d’informations, consultez la section [Surveiller la file d’attente des travaux](#monitor-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Pour créer une écriture file d’attente des travaux pour la validation par lots des commandes vente

Sinon, vous pouvez reporter les publications à des heures pratiques pour votre organisation. Par exemple, il peut sembler raisonnable dans votre activité d’exécuter certaines routines lorsque la plupart de la saisie de données de la journée est achevée. Vous pouvez obtenir cette opération en configurant la file projets pour exécuter différents états de validation par lots, par exemple, **TPL valider commandes vente**, **TPL valider factures vente** et les états similaires. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge la validation en arrière-plan de toutes les ventes, achats, et documents service.

La procédure suivante décrit comment définir le rapport **TPL valider commandes vente** pour une validation automatique des commandes vente lancées à 16 h 00 les jours de semaine.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures file d’attente des travaux**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Type objet à exécuter**, sélectionnez **Rapport**.  
4. Dans le champ **ID objet à exécuter**, sélectionnez 296, **TPL valider commandes vente**.

   Vous pouvez également utiliser les états suivants :
  
   * 900 **TPL validation ordres d’assemblage**
   * 497 **TPL validation factures achat**
   * 496 **TPL validation commandes achat**
   * 498 **TPL validation avoirs achat**
   * 6665 **TPL valider retours achat**
   * 298 **TPL valider avoirs vente**
   * 297 **TPL valider factures vente**
   * 296 **TPL valider commandes vente**
   * 6655 **TPL valider retours vente**
   * 6005 **TPL valider avoirs service**
   * 6004 **TPL valider factures service**
   * 6001 **TPL Commandes service**

5. Activez la case à cocher **Page requête état**.
6. Dans la page de demande **TPL valider commandes vente**, définissez ce qui est inclus lors de la validation automatique des commandes vente, puis sélectionnez le bouton **OK**.

    > [!IMPORTANT]
    > N’oubliez pas de définir des filtres stricts ; sinon, [!INCLUDE [prod_short](includes/prod_short.md)] affichera tous les documents, même s’ils ne sont pas prêts. Pensez à définir un filtre sur le champ **Statut** pour la valeur *Lancé*, et un filtre sur le champ **Date comptabilisation** pour la valeur *..aujourd’hui*. Pour plus d’informations, voir [Tri, recherche et filtrage](ui-enter-criteria-filters.md).
7. Activez toutes les cases à cocher de **Exécuter le lundi** à **Exécuter le vendredi**.
8. Dans le champ **Heure début**, entrez 16 h 00.
9. Choisissez l’action **Attribuer le statut Prêt**.

Les commandes vente dans les filtres définis sont à présent validées chaque jour de la semaine à 16 h 00.

## <a name="monitor-the-job-queue"></a>Surveiller la file d’attente des travaux

Si vous configurez la validation en arrière-plan avec les files d’attente des travaux, convertissez-la en une tâche périodique pour surveiller la file d’attente des travaux et détecter les éventuels problèmes. Vous pouvez suivre le statut dans la page **Écritures file d’attente des travaux**. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

En tant qu’administrateur, vous pouvez utiliser [Application Insights](/azure/azure-monitor/app/app-insights-overview) pour recueillir et analyser la télémétrie que vous pouvez utiliser pour identifier les problèmes. Pour plus d’informations, consultez [Surveillance et analyse de la télémétrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) dans le contenu pour développeurs et administrateurs.  

## <a name="see-also"></a>Voir aussi

[Validation des documents et des feuilles](ui-post-documents-journals.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Valider les documents validés](across-edit-posted-document.md)  
[Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Recherche de pages et d’informations avec Tell Me](ui-search.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
