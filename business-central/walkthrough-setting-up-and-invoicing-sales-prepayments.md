---
title: Configuration et facturation d’acomptes
description: Les acomptes sont des paiements qui sont facturés et validés dans une commande acompte vente ou achat avant la facturation finale.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: bholtorf
---
# Procédure pas à pas : configuration et facturation d’acomptes

Cette procédure pas à pas vous guide tout au long du processus de configuration et d’utilisation des acomptes dans [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Par exemple, vous pouvez également envoyer plus de factures acompte si davantage d’articles supplémentaires sont ajoutés à la commande.  

## À propos de cette procédure pas à pas  

Cette procédure pas à pas présente les scénarios suivants :  

- configuration d’acomptes ;  
- création d’une commande nécessitant un acompte ;  
- création d’une facture acompte ;  
- correction des conditions d’acompte sur une commande ;  
- lettrage d’acomptes avec une commande ;  
- facturation du montant final sur une commande avec acompte.  

### Rôles

Cette procédure pas à pas inclut les tâches correspondant aux rôles suivants :  

- responsable de la comptabilité (Phyllis) ;  
- préparatrice de commandes (Susan) ;  
- administrateur Ventes (Arnie).  

## Scénario

 Phyllis est un comptable qui décide des clients qui doivent payer un acompte avant que les articles soient fabriqués ou expédiés. Phyllis configure [!INCLUDE[prod_short](includes/prod_short.md)] de façon à calculer automatiquement les acomptes.  

 Susan est préparatrice de commandes vente. Lorsque le client appelle pour passer une commande, Susan entre la commande dans le système pendant que le client est au téléphone. Susan peut ainsi vérifier immédiatement les prix et les conditions de paiement avec le client et ajuster la commande pendant qu’elle négocie avec le client.  

 Arnie travaille dans le département Comptabilité client où sa fonction consiste à valider les factures et les paiements.  

 Dans ce scénario, Phyllis configure les conditions d’acompte pour le client Selangorian, en se basant sur leurs antécédents en matière de crédit. Elle donne à Susan des instructions sur le traitement de leurs commandes.  

 Lorsque le client appelle, Susan négocie jusqu’à ce qu’ils arrivent à un accord : le système lui permet de calculer les acomptes de différentes manières.  

 Après que Susan a envoyé la facture, le client commande un article supplémentaire. Susan met à jour la commande et crée une seconde facture acompte.  

 Arnie enregistre le paiement du client et le lettre avec la facture, puis envoie la facture finale.  

## Configuration des acomptes

Phyllis configure le système afin qu’il gère les acomptes des clients.  

- Elle décide d’utiliser la même souche de numéros pour les acomptes et la facturation vente.  
- Elle configure l’application pour qu’elle vérifie si des acomptes sont requis avant la facturation finale d’une commande.  
- Elle configure les valeurs par défaut pour un pourcentage d’acompte requis pour certains articles et clients.  

Les procédures suivantes décrivent le mode d’exécution des tâches de Phyllis :  

### Pour configurer des souches de numéros pour les acomptes

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.  
2. Sur la page **Paramètres ventes**, affichez le raccourci **Souches de numéros**.  
3. Vérifiez que la souche de numéros des factures acompte validées dans le champ **N° fact. acompte enreg.** est identique à celles des factures vente validées (**N° facture enregistrée**) et que la souche de numéros des avoirs acompte validés (**N° avoir acompte enreg.**) est identique à celle des avoirs enregistrés (**N° avoir enregistré**).  

### Pour bloquer les expéditions pour un acompte impayé

1. Sur la page **Paramètres ventes**, sur le raccourci **Général**, cochez la case **Vérifier les acomptes lors de la validation**.

Vous ne pouvez pas expédier ou facturer une commande dont le montant d’acompte n’est pas réglé.  

Par défaut, Phyllis requiert que le client 20000 soit facturé avec un acompte de 30 % sur toutes les commandes. Pour cela, Phyllis entre un pourcentage d’acompte par défaut dans la fiche client.  

Phyllis requiert que tous les clients soient facturés avec un acompte de 20 % pour l’article 1896-S. Le client 20000 a un mauvais historique des paiements, c’est pourquoi Phyllis requiert un acompte de 40 % pour ce client pour l’article 1896-S. La procédure suivante présente le mode de configuration des pourcentages d’acompte par défaut.  

### Pour affecter des pourcentages d’acompte par défaut aux clients et aux articles

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  
2. Ouvrez la fiche pour le client 20000 (Trey Research).
3. Sur le raccourci **Paiements**, dans le champ **% acompte**, entrez **30**.  
4. Choisissez l’action **Associé**, sélectionnez l’élément de menu **Ventes**, puis choisissez l’élément de menu **Pourcentages acompte**.  
5. Renseignez deux lignes de la page **Pourcentages acompte vente**, comme suit.  

    |**Type vente**|**Code vente**|**N° article**|**% acompte**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Client**|**20000**|**1896-S**|**40**|
    |**Client**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > En fonction de votre pays/région, vous devez également spécifier un code groupe taxes sur le raccourci **Coûts et validation** pour l’article 1896-S. Lorsque vous utilisez la société de démonstration, ce champ est déjà défini.

6. Fermez toutes les pages.  

### Pour spécifier un compte acomptes vente dans les paramètres comptabilisation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilisation**, puis choisissez le lien associé.  
2. Sélectionnez la ligne où le champ **Groupe compta. marché** est défini sur **NATIONAL**, et où le champ **Groupe compta. produit** est défini sur **DÉTAIL**.  
3. Dans le champ **Compte acomptes vente**, indiquez le compte approprié. Votre sélection est automatiquement enregistrée.  

> [!TIP]
> Si vous ne pouvez pas voir le champ de la page **Paramètres comptabilisation**, utilisez la barre de défilement horizontale au bas de la page pour faire défiler l’affichage vers la droite.  

## Création d’une commande nécessitant un acompte

 Dans le scénario suivant, Susan, la préparatrice des commandes, crée une commande en discutant avec le client. Les articles commandés par le client nécessitent un prépaiement. De plus, le client a effectué des paiements en retard dans le passé. Susan a reçu l’ordre de demander un montant fixe de **800** comme acompte sur la commande.  

Le client demande à payer 35 %. Susan accepte et modifie la commande en conséquence.  

Susan crée la facture acompte et l’envoie au client.  

### Pour créer une commande vente avec acompte

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Nom du client**, choisissez **Trey Research**.  
4. Fermez l’avertissement de solde échu qui s’affiche.  
5. Renseignez deux lignes vente avec les informations suivantes.  

    |**Type**|**N°**|**Quantité**|  
    |--------------|-------------|------------------|  
    |**Article**|**1896-S**|**1**|  
    |**Article**|**1900-S**|**1**|

    Par défaut, les champs de l’acompte sont masqués. Pour afficher les champs vous devez personnaliser la page. Pour plus d’informations, consultez [Commencer à personnaliser une page au moyen de la bannière Personnalisation](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Vérifiez que le champ **% acompte** de la ligne correspondant à l’article **1900-S** a pour valeur **30**. La valeur par défaut a été prise dans l’en-tête vente, qui a été renseigné à partir de la fiche client.  

    Le champ **% acompte** de la ligne correspondant à l’article **1896-S** a pour valeur **40**. 40 désigne le pourcentage que vous avez entré sur la page **Pourcentages acompte vente** pour l’article **1896-S** et le client **20000**.  

    Pour plus d’informations, reportez\-vous à [Configuration des acomptes](finance-set-up-prepayments.md).  
7. Dans l’action **Ordre**, choisissez **Statistiques**.  
8. Sur le raccourci **Acompte**, le champ **Montant acompte HT** indique **458,16**. Si vous créez une facture acompte pour la commande dès maintenant, 458,16 est le montant qui s’affiche sur la facture.  

    Dans ce scénario, Susan a reçu des instructions lui demandant de proposer un acompte total de **800** pour la commande.  

    > [!IMPORTANT]  
    >  En fonction de votre pays/région, l’étape suivante peut ne pas s’appliquer.  
9. Remplacez le montant du champ **Montant acompte HT** par **800**, puis fermez la page.  
10. Consultez le champ **% acompte** des lignes vente : le montant a été recalculé, il est désormais de **67,02438** et **67,02282**.  

     Le nouveau calcul inclut toutes les lignes dont le pourcentage d’acompte est supérieur à 0.  

     À présent, le client demande si le pourcentage de l’acompte peut être fixé à 35 %. Le chef de Susan accepte la modification.
11. Sur la page **Commande vente**, sur le raccourci **Acompte**, dans le champ **% acompte**, entrez **35**.  
12. Dans l’avertissement qui s’affiche, cliquez sur le bouton **Oui** . Un taux de 35 % sera appliqué comme pourcentage du paiement de l’ensemble de la commande.  
13. Vérifiez que les lignes ont été mises à jour en conséquence.  

## Créer une facture acompte

Après avoir entré la valeur d’acompte correcte sur la commande, Susan crée la facture acompte et l’envoie au client.  

### Pour créer une facture acompte

1. Sur la page **Commande**, choisissez **Actions**, puis **Validation**, puis **Acompte**, puis **Valider et imprimer facture acompte**.
2. Choisissez le bouton **Oui** pour valider la facture.  

> [!NOTE]  
> Susan doit maintenant envoyer la facture au client.  

## Créer une facture acompte supplémentaire

Le jour suivant, le client appelle Susan et modifie sa commande. Il souhaite deux exemplaires de l’article 1896-S. Susan rouvre et met à jour la commande, puis crée une seconde facture acompte sur la commande et l’envoie au client.  

### Pour créer une facture acompte supplémentaire

1. Sur la page **Commande vente**, choisissez l’action **Lancer**, puis **Rouvrir**  
2. Sur la ligne de l’article **1896-S**, dans le champ **Quantité**, entrez **2**.  

    Dans l’action **Ordre**, choisissez **Statistiques**. Le champ **Montant acompte HT** indique à présent **768,04** et le champ **Montant fact. acompte HT** indique **417,76**. Ces valeurs indiquent qu’il existe un montant d’acompte supplémentaire qui n’a pas encore été facturé.  
3. Pour valider une facture pour le montant d’acompte supplémentaire, choisissez **Actions**, puis **Validation**, puis **Acompte**, puis **Valider et imprimer facture acompte**
4. Choisissez le bouton **Oui** pour valider la facture.  

## Lettrer les acomptes

Le client paie le montant de l’acompte. Arnie, du service comptabilité, enregistre le paiement et le lettre aux factures d’acompte.  

### Pour lettrer un paiement avec les factures acompte

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles règlement**, puis choisissez le lien associé.  
2. Renseignez une ligne feuille avec les informations suivantes.  

    |Nom du champ|Saisissez|  
    |----------------|-----------|  
    |**Type document**|**Paiement**|  
    |**Type compte**|**Client**|  
    |**N° compte**|**20000**|  
3. Choisissez l’action **Traitement**, puis **Appliquer les entrées**.  
4. Sur la page **Lettrer écritures client**, sélectionnez la première facture acompte, puis, sélectionnez l’action **Traitement** et enfin l’action **Définir ID lettrage**.  
5. Répétez l’étape précédente pour le deuxième acompte.  
6. Cliquez sur le bouton **OK**.  

    Les champs **Montant** sont maintenant renseignés avec la somme des deux factures acompte.  

7. Pour valider la feuille, choisissez l’action **Valider/Imprimer**, puis sélectionnez **Valider**.
8. Cliquez sur le bouton **Oui**.

## Facturer le montant ouvert

Arnie a été informé que les articles de la commande ont été expédiés et que la commande est prête pour facturation. Il crée donc la facture correspondante.  

### Pour facturer le montant ouvert

1. Ouvrez la commande vente.
2. Choisissez l’action **Validation**, puis **Valider**.
3. Sélectionnez **Expédition et facturation**, puis cliquez sur le bouton **OK**.
4. Si vous souhaitez afficher un aperçu de la facture, cliquez sur le bouton **Oui**.

    > [!NOTE]  
    > Normalement, le département Expédition devrait déjà avoir validé l’expédition.  

    Arnie peut afficher l’historique pour vérifier que la facture vente a été créée comme prévue.

5. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  

## Mettre à jour automatiquement le statut des commandes prépayées et des factures

Vous pouvez accélérer le traitement des commandes et des factures en configurant des entrées de file d’attente qui mettent automatiquement à jour le statut de ces documents. Lorsqu’une facture d’acompte est payée, les entrées de la file d’attente des travaux peuvent changer automatiquement le statut du document de **Acompte en attente** sur **Validé**. Lorsque vous configurez les entrées de la file d’attente des travaux, les unités de code que vous devrez utiliser sont **383 Mise à jour En attente Acompte Ventes** et **383 Mise à jour En attente Acompte Achats**. Nous vous recommandons de programmer les entrées pour qu’elles s’exécutent fréquemment, par exemple, toutes les minutes. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## Étapes suivantes

Cette procédure pas-à-pas vous a présenté les étapes de configuration de [!INCLUDE[prod_short](includes/prod_short.md)] pour la gestion des acomptes. 

- Configurez les pourcentages d’acompte par défaut sur les clients et les articles.
- Utilisez différentes méthodes pour calculer les acomptes sur une commande.  
- Calculez le montant de l’acompte en pourcentage du total de la commande.
- Attribuez un montant total d’acompte à la commande.  

Vous avez également validé une facture acompte, créé une deuxième lorsque la commande est modifiée, et validé la facture finale pour le montant ouvert.  

Les fonctionnalités d’acompte facilitent la configuration et l’application des règles d’acompte pour les clients et les articles. Ils vous permettent également de reporter chaque paiement sur une facture.  

## Voir aussi

[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
