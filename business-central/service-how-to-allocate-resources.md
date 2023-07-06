---
title: Comment affecter des ressources | Microsoft Docs
description: Vous pouvez modifier le montant annuel du contrat service ou du devis contrat afin de rectifier le montant qui sera facturé annuellement.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="allocate-resources"></a><a name="allocate-resources"></a><a name="allocate-resources"></a>Affecter des ressources
Les personnes qui fournissent le service représentent l’élément clé de la gestion des services. Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour affecter les personnes aux tâches de manière appropriée. Vous pouvez baser les affectations sur les zones de service dans lesquelles les personnes sont situées ou dans lesquelles le service se produit. En outre, vous pouvez regrouper les ressources lors de la réponse aux demandes de service. Pour plus d’informations, voir [Configurer l’affectation des ressources](service-how-setup-resource-allocation.md).

Vous pouvez affecter des ressources, par exemple, des techniciens, à l’aide du **Tableau d’affectation** ou d’une commande service. Vous pouvez utiliser la disponibilité des ressources pour affecter des ressources à l’exécution des tâches service dans les commandes ou les devis.

Vous pouvez ventiler la même ressource, par exemple, un technicien, ou le même groupe ressources sur tous les articles de service d’une commande service. Des écritures affectation sont crées pour les autres articles de service de la commande avec le même numéro ressource et la même date affectation que la ligne affectée. Les heures affectées sont obtenues en divisant les heures que vous avez affectées par le nombre d’articles de service de la commande. Le champ **Statut** est automatiquement paramétré sur **Actif** pour toutes les écritures créées.

## <a name="to-see-an-overview-of-service-orders-and-service-quotes"></a><a name="to-see-an-overview-of-service-orders-and-service-quotes"></a><a name="to-see-an-overview-of-service-orders-and-service-quotes"></a>Pour afficher un aperçu des commandes/devis service :
Vous aurez souvent besoin de consulter la liste des commandes service ou des devis service répondant à certaines exigences pour être en mesure d’exécuter des actions spécifiques sur chacun de ces documents. Vous devrez, par exemple, affecter des ressources à des commandes service appartenant à un client spécifique.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableau d’affectation**, puis sélectionnez le lien associé.  
2. Dans le champ **Filtre document**, choisissez le type des documents que vous souhaitez afficher.
3. Pour obtenir la liste des documents contenant des tâches service auxquelles une ressource ou un groupe ressources est affecté, renseignez les champs **Filtre ressource** et **Resource Group Filter**, puis sélectionnez <kbd>Entrée</kbd>.  
4. Pour obtenir la liste des documents contenant une certaine date de réponse ou des dates de réponse comprises dans une période, renseignez le champ **Filtre date réponse** puis sélectionnez <kbd>Entrée</kbd>.  
5. Pour obtenir la liste des documents avec un état d’affectation ou statut document spécifié, renseignez le champ **Filtre affectation/Filtre statut** puis sélectionnez <kbd>Entrée</kbd>.  
6. Pour obtenir la liste des documents appartenant à un certain contrat, client ou zone, renseignez le champ **Filtre contrat/Filtre client/Filtre zone** puis sélectionnez <kbd>Entrée</kbd>.  
7. Cliquez sur une ligne qui correspond à une commande service ou le devis service, puis sélectionnez l’action **Afficher document**.  

    La page **Commande service** ou **Devis service** s’ouvre et vous pouvez utiliser le document. Pour revenir à la page **Tableau d’affectation**, choisissez **OK**.

## <a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a><a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a><a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a>Pour affecter une ressource à l’aide de la disponibilité ressource ou groupe ressources
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableau d’affectation**, puis sélectionnez le lien associé.  
2. Choisissez la commande service, puis sélectionnez l’action **Affectations ressources**.  
3. Choisissez l’écriture comportant la tâche service à laquelle vous souhaitez affecter une ressource.  
4. Choisissez **Disponibilité ressource** ou l’action **Disponibilité groupe ressources**.  
5. Sur la page **Disponibilité ressource serv.**, choisissez **Afficher matrice**.  
6. Choisissez une ressource à affecter. Votre sélection peut varier en fonction de la qualification de la ressource pour la tâche, si elle se trouve dans la zone client et/ou si elle a été choisie par le client.  
7. Spécifiez une date à laquelle la ressource dispose de suffisamment d’heures disponibles pour la tâche, cette date doit être proche de la date de réponse de la commande service.  
8. Dans le champ **Qté à affecter**, saisissez le nombre d’heures pendant lesquelles vous souhaitez affecter la ressource à la tâche service.  
9. Sélectionnez l’action **Affecter** pour affecter la ressource sélectionnée à la date sélectionnée.  

     Le champ **Statut** est automatiquement paramétré sur **Actif**.  

 Répétez ces étapes pour chaque date à laquelle vous souhaitez affecter la ressource à la tâche service.  

> [!NOTE]  
>  Pour un article de service d’une commande service, il ne peut y avoir que des écritures affectation **actives** avec une seule ressource ou un seul groupe ressources à la fois.  

## <a name="to-allocate-a-resource-using-a-service-order"></a><a name="to-allocate-a-resource-using-a-service-order"></a><a name="to-allocate-a-resource-using-a-service-order"></a>Pour affecter une ressource à l’aide d’une commande service
Après avoir créé et renseigné une commande service ou un devis service, vous pouvez affecter des ressources, par exemple, des techniciens, pour exécuter des tâches service enregistrées sous forme de lignes article de service dans le document.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Cliquez sur la commande service, puis choisissez **Modifier**.  
3. Choisissez la ligne article de service correspondant à la tâche service à laquelle vous souhaitez affecter une ressource.  
4. Choisissez **Affectations ressources**.
5. Sur la page **Affectations ressources**, choisissez une écriture affectation non active avec la tâche service à laquelle vous souhaitez affecter la ressource. Si l’écriture affectation non active n’existe pas, vous pouvez en créer une en choisissant **Nouveau**.  
7. Spécifiez la tâche service en renseignant le champ **N° article de service** de la ligne.  
8. Dans le champ **N° de ressource**, choisissez la ressource. Si la ressource appartient à un groupe ressources, le numéro du groupe ressources est inséré automatiquement dans le champ **N° groupe ressources**. .  
9. Renseignez les champs **Date affectation** et **Heures affectées**. La **statut** du champ est **Actif**. Cela signifie que la ressource est affectée à la tâche service.  
10. Éventuellement, pour affecter la ressource à tous les articles, choisissez **Affecter à tous les articles de service**.

> [!NOTE]  
>  Pour un article de service d’une commande service, il ne peut y avoir que des écritures affectation actives avec une seule ressource ou un seul groupe ressources à la fois.

## <a name="to-reallocate-resources-on-a-service-order"></a><a name="to-reallocate-resources-on-a-service-order"></a><a name="to-reallocate-resources-on-a-service-order"></a>Pour réaffecter des ressources à une commande service
Vous pouvez réaffecter des ressources directement à partir d’une commande service ou devis service en cours d’utilisation. L’écriture d’origine existe toujours mais son statut est mis à jour comme suit :  

* Si la maintenance a débuté pendant que l’affectation était **Active** (c’est-à-dire, si l’état réparation de l’article de service de l’écriture est passé à **En cours**), l’état affectation passe de **réallocation nécessaire** à **Terminée**.  
* Si la maintenance n’a pas débuté pendant que l’affectation était **Active**,l’état affectation passe de **Réallocation nécessaire** à **Annulée**.  
* Si vous réaffectez une commande service issue d’un devis, le statut des écritures affectation enregistrées pour le devis passe toujours à **Terminé** lorsque vous réaffectez les articles de service de la commande service.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Ouvrez la commande service.  
3. Sélectionnez la ligne article de service correspondant à la tâche service à laquelle vous souhaitez affecter une ressource, puis sélectionnez l’action **Affectations ressources**.  
4. Sur la page **Affectations ressources**, sélectionnez une écriture affectation avec la tâche service à laquelle vous souhaitez réaffecter la ressource. Sélectionnez la ressource concernée dans le champ **N° de ressource**. Ce numéro remplace le numéro ressource qui figurait dans le champ.  
5. Sélectionnez <kbd>Entrée</kbd>. La boîte de dialogue qui s’ouvre vous demande de confirmer la réaffectation de cette écriture. Renseignez le champ **Code motif** si nécessaire et cliquez sur le bouton **Oui** pour confirmer la réaffectation.  
6. Renseignez les champs **Date affectation** et **Heures affectées**. L’écriture contient maintenant la nouvelle ressource et son statut est **Actif**.

## <a name="to-reallocate-a-resource-using-the-dispatch-board"></a><a name="to-reallocate-a-resource-using-the-dispatch-board"></a><a name="to-reallocate-a-resource-using-the-dispatch-board"></a>Pour réaffecter une ressource à l’aide du tableau d’affectation
Si la ressource affectée à une tâche service ne peut pas accomplir le travail, vous devez la réaffecter. Généralement, vous réaffectez des ressources aux tâches service à l’aide du **tableau d’affectation**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableau d’affectation**, puis sélectionnez le lien associé.  
2. Dans le champ **Filtre affectation**, sélectionnez **Réaffectation nécessaire**. La page **Tableau d’affectation** affiche maintenant uniquement les commandes service comprenant des tâches service qui doivent être réaffectées.  
3. Sélectionnez la commande service appropriée, puis sélectionnez l’action **Affectations ressources**. La page **Affectations ressources** s’ouvre.  
4. Sélectionnez l’écriture affectation comprenant la tâche service à laquelle vous souhaitez réaffecter une ressource.  
5. Sélectionnez la ressource concernée dans le champ **N° de ressource**. Ce numéro remplace le numéro ressource qui figurait dans le champ.  
6. Sélectionnez <kbd>Entrée</kbd>. La boîte de dialogue **Motifs des écritures de réaffection** s’ouvre, et vous êtes invité à réaffecter ou non cette écriture. Renseignez le champ **Code motif** si nécessaire et cliquez sur le bouton **Oui** pour confirmer la réaffectation.  
7.  Renseignez les champs **Date affectation** et **Heures affectées**. L’écriture contient maintenant la nouvelle ressource et son statut est **Actif**.  

    > [!NOTE]  
    >  L’ancienne écriture existe toujours mais son statut à jour est mis à jour comme suit :  
    >   
    >  * Si la maintenance a débuté pendant que l’affectation était **Active** (c’est-à-dire, si l’état réparation de l’article de service de l’écriture est passé à **En cours**), l’état affectation passe de **réallocation nécessaire** à **Terminée**.  
    > * Si la maintenance n’a pas débuté pendant que l’affectation était **Active**,l’état affectation passe de **Réallocation nécessaire** à **Annulée**.  
    > * Si vous réaffectez une commande service issue d’un devis, le statut des écritures affectation enregistrées pour le devis passe toujours à **Terminé** lorsque vous réaffectez les articles de service de la commande service.  

## <a name="to-register-resource-hours"></a><a name="to-register-resource-hours"></a><a name="to-register-resource-hours"></a>Pour enregistrer les heures ressource
Lorsque vous utilisez des articles de service de commandes service, vous devez enregistrer les heures ressource utilisées pour le service. La procédure suivante vous explique comment enregistrer les heures ressource sur la page **Feuille activité article de service**.  

Vous pouvez utiliser la même procédure pour enregistrer les heures sur la page **Lignes service** que vous pouvez ouvrir sur la page Commande de service. Ouvrez la fiche service appropriée, puis cliquez sur l’action **Lignes service**.  

Si la même ressource travaille sur tous les articles de service de la commande service, vous pouvez enregistrer le nombre total d’heures ressource pour un seul article de service, puis vous pouvez répartir les lignes ressource pour affecter les heures ressource aux autres articles de service.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tâches service**, puis choisissez le lien associé.
2. Sélectionnez la ligne comprenant l’article de service approprié, puis choisissez l’action **Feuille activité article**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-resource-to-all-service-items-in-an-order"></a><a name="to-assign-a-resource-to-all-service-items-in-an-order"></a><a name="to-assign-a-resource-to-all-service-items-in-an-order"></a>Pour affecter une ressource à tous les articles de service d’une commande
Si la même ressource, par exemple, un technicien, travaille sur tous les articles de service de la commande service, vous pouvez enregistrer le nombre total d’heures ressource pour un seul article de service et répartir la ligne ressource pour diviser les heures ressource sur les lignes ressource des autres articles de service.  

La procédure suivante explique comment répartir des lignes ressource sur la page **Lignes facture service**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Ouvrez la commande service.  
3. Dans le raccourci **Lignes**, sélectionnez l’action **Lignes de service**. La page **Lignes de service** s’ouvre.  
4. sélectionnez la ligne ressource à répartir. La valeur du champ **Quantité** est répartie entre tous les articles de service de la commande.  
5. Sélectionnez l’action **Répartir ligne ressource**. Choisissez **Oui** pour confirmer.  

    Des lignes ressource pour les autres articles de service de la commande sont créées avec le même numéro ressource que la ligne répartie. La quantité représente la quantité de la ligne répartie divisée par le nombre d’articles de service de la commande.  

## <a name="to-cancel-an-allocation"></a><a name="to-cancel-an-allocation"></a><a name="to-cancel-an-allocation"></a>Pour annuler des affectations :
Vous pouvez annuler des affectations de ressources pour des tâches service sans réaffecter les tâches.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableau d’affectation**, puis sélectionnez le lien associé.  
2. Choisissez la commande service, puis sélectionnez l’action **Affectations ressources**.  
3. Choisissez l’écriture affectation contenant la tâche service pour laquelle vous souhaitez annuler l’affectation.  
4. Sélectionnez l’action **Annuler affectation**.  
5. Dans le champ **Code motif**, sélectionner le code motif adéquat.  
6. Cliquez sur **Oui** pour confirmer l’annulation.  

    > [!NOTE]  
    > L’option **Réaffectation nécessaire** dans le champ **Statut** est automatiquement sélectionnée. Si le statut réparation de l’article de service de l’écriture est **Initial**, le programme le transforme en **Expertisé** (aucun service n’a été commencé). Si l’état réparation est **En cours**, il est modifié en **Service en partie réalisé**càd que la maintenance a été partiellement effectuée.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Configurer l’affectation des ressources](service-how-setup-resource-allocation.md)  
[Statut affectation et statut réparation](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
