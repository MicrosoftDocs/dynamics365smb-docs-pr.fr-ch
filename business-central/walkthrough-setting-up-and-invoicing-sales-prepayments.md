---
title: Procédure pas à pas Configuration et facturation d’acomptes
description: Les acomptes sont des paiements qui sont facturés et validés dans une commande acompte vente ou achat avant la facturation finale. Vous pouvez demander un acompte avant de fabriquer les produits commandés ou le paiement avant d’envoyer les articles à un client. Vous utilisez la fonctionnalité d’acomptes dans Business Central pour facturer et collecter les acomptes requis des clients ou régler des acomptes aux fournisseurs. Vous pouvez ainsi vous assurer que tous les paiements sont validés sur une facture.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: dacf9e5492f583513e69f2316a0440fce2597269
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216195"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Procédure pas à pas : configuration et facturation d’acomptes

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Les acomptes sont des paiements qui sont facturés et validés dans une commande acompte vente ou achat avant la facturation finale. Vous pouvez demander un acompte avant de fabriquer les produits commandés ou le paiement avant d’envoyer les articles à un client. Vous utilisez la fonctionnalité d’acomptes dans [!INCLUDE[prod_short](includes/prod_short.md)] pour facturer et collecter les acomptes requis des clients ou régler des acomptes aux fournisseurs. Vous pouvez ainsi vous assurer que tous les paiements sont validés sur une facture.  

Les conditions d’acompte peuvent être définies pour un client ou un fournisseur pour tous les articles ou pour une sélection d’articles. Lorsque vous avez effectué la configuration requise, vous pouvez générer des factures acompte à partir des commandes vente et achat pour le montant acompte calculé. Au besoin, vous pouvez modifier les montants par défaut dans la facture. Par exemple, vous pouvez également envoyer des factures acompte supplémentaires si des articles supplémentaires sont ajoutés à la commande.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  

Cette procédure pas à pas présente les scénarios suivants :  

-  configuration d’acomptes ;  
-  création d’une commande nécessitant un acompte ;  
-  création d’une facture acompte ;  
-  correction des conditions d’acompte sur une commande ;  
-  lettrage d’acomptes avec une commande ;  
-  facturation du montant final sur une commande avec acompte.  

### <a name="roles"></a>Rôles

Cette procédure pas à pas inclut les tâches correspondant aux rôles suivants :  

-  responsable de la comptabilité (Phyllis) ;  
-  préparatrice de commandes (Susan) ;  
-  administrateur Ventes (Arnie).  

## <a name="story"></a>Scénario

 Phyllis est responsable de la comptabilité. Elle décide des clients qui doivent payer un acompte avant que les articles soient fabriqués ou expédiés. Phyllis configure [!INCLUDE[prod_short](includes/prod_short.md)] de façon à calculer automatiquement les acomptes.  

 Susan est préparatrice de commandes vente. Lorsque le client appelle pour passer une commande, elle entre la commande dans le système pendant que le client est au téléphone. Elle peut ainsi vérifier immédiatement les prix et les conditions de paiement avec le client et ajuster la commande pendant qu’elle négocie avec le client.  

 Arnie travaille dans le département Comptabilité client où sa fonction consiste à valider les factures et les paiements.  

 Dans ce scénario, Phyllis configure les conditions d’acompte pour le client Selangorian, en se basant sur leurs antécédents en matière de crédit. Elle donne à Susan des instructions sur le traitement de leurs commandes.  

 Lorsque le client appelle, Susan négocie avec lui jusqu’à ce qu’ils arrivent à un accord. Elle peut alors choisir de calculer l’acompte de différentes manières.  

 Après que Susan a envoyé la facture, le client commande un article supplémentaire. Susan met à jour la commande et crée une seconde facture acompte.  

 Arnie enregistre le paiement du client et le lettre avec la facture, puis envoie la facture finale.  

## <a name="setting-up-prepayments"></a>Configuration d’acomptes

Phyllis configure le système afin qu’il gère les acomptes des clients.  

-  Elle décide d’utiliser la même souche de numéros pour les acomptes et la facturation vente.  
-  Elle configure l’application pour qu’elle vérifie si des acomptes sont requis avant la facturation finale d’une commande.  
-  Elle configure les valeurs par défaut pour un pourcentage d’acompte requis pour certains articles et clients.  

Les procédures suivantes décrivent le mode d’exécution des tâches de Phyllis :  

#### <a name="to-set-up-number-series-for-prepayments"></a>Pour configurer des souches de numéros pour les acomptes

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres ventes**, puis sélectionnez le lien associé.  
2.  Sur la page **Paramètres ventes**, affichez le raccourci **Souches de numéros**.  
3.  Vérifiez que la souche de numéros des factures acompte validées dans le champ **N° fact. acompte enreg.** est identique à celles des factures vente validées (**N° facture enregistrée**) et que la souche de numéros des avoirs acompte validés (**N° avoir acompte enreg.**) est identique à celle des avoirs enregistrés (**N° avoir enregistré**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Pour bloquer les expéditions pour un acompte impayé

1.  Sur la page **Paramètres ventes**, sur le raccourci **Général**, cochez la case **Vérifier les acomptes lors de la validation**.

Vous ne pouvez pas expédier ou facturer une commande dont le montant d’acompte n’est pas réglé.  

Par défaut, Phyllis requiert que le client 20000 soit facturé avec un acompte de 30 % sur toutes les commandes. Pour cela, elle entre un pourcentage d’acompte par défaut dans la fiche client.  

Phyllis requiert que tous les clients soient facturés avec un acompte de 20 % pour l’article 1896-S. Le client 20000 a un mauvais historique de paiements. Par conséquent, elle demande un acompte de 40 % au client 20000 pour l’article 1896-S. La procédure suivante présente le mode de configuration des pourcentages d’acompte par défaut.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Pour affecter des pourcentages d’acompte par défaut aux clients et aux articles

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.  
2.  Ouvrez la fiche pour le client 20000 (Trey Research).
3.  Dans le champ **% acompte**, entrez **30**.  
4.  Sélectionnez **En rapport**, puis sélectionnez **Ventes** et enfin **Pourcentages d’acompte**
5.  Renseignez deux lignes de la page **Pourcentages acompte vente**, comme suit.  

    |**Type vente**|**Code vente**|**N° article**|**% acompte**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Client**|**20000**|**1896-S**|**40**|  
    |**Tous les clients**| |**1896-S**|**20**|  

    > [!IMPORTANT]  
    >  En fonction de votre pays/région, vous devez également spécifier un code groupe taxes sur le raccourci **Facturation** pour l’article 1896-S.  

6.  Fermez toutes les pages.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Pour spécifier un compte acomptes vente dans les paramètres comptabilisation

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres comptabilisation**, puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne où le champ **Groupe compta. marché** est défini sur **NATIONAL**, et où le champ **Groupe compta. produit** est défini sur **DÉTAIL**.  
3.  Dans le champ **Compte acomptes vente**, indiquez le compte approprié. Votre sélection est automatiquement enregistrée.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Création d’une commande nécessitant un acompte

 Dans le scénario suivant, Susan, la préparatrice des commandes, crée une commande en discutant avec le client. Les articles que le client commande nécessitent un acompte et le client a connu des retards de paiement par le passé. Susan a donc reçu l’ordre de demander un montant fixe de **800** comme acompte sur la commande.  

Le client demande à pouvoir payer 35 %, ce que Susan peut accepter. Elle modifie donc la commande.  

Susan crée la facture acompte et l’envoie au client.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Pour créer une commande vente avec acompte

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Pour le champ **N° client** , sélectionnez **20000**.  
4.  Fermez l’avertissement de solde échu qui s’affiche.  
5.  Renseignez deux lignes vente avec les informations suivantes.  

    |**Type**|**N°**|**Quantité**|  
    |--------------|-------------|------------------|  
    |**Article**|**1896-S**|**1**|  
    |**Article**|**1900-S**|**1**|

    Par défaut, les champs de l’acompte étant masqués, vous devez les afficher. Pour cela, vous devez personnaliser la page. Pour plus d’informations, consultez [Commencer à personnaliser une page au moyen de la bannière Personnalisation](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6.  Vérifiez que le champ **% acompte** de la ligne correspondant à l’article **1900-S** a pour valeur **30**. La valeur par défaut a été prise dans l’en-tête vente, qui a été renseigné à partir de la fiche client.  

    Le champ **% acompte** de la ligne correspondant à l’article **1896-S** a pour valeur **40**. Il s’agit du pourcentage que vous avez entré sur la page **Pourcentages acompte vente** pour l’article **1896-S** et le client **20000**.  

    Pour plus d’informations, reportez\-vous à [Configuration des acomptes](finance-set-up-prepayments.md).  
7.  Dans l’action **Ordre**, choisissez **Statistiques**.  
8.  Sur le raccourci **Acompte**, le champ **Montant acompte HT** indique **458,16**. Si vous créez une facture acompte pour la commande dès maintenant, c’est le montant qui s’affiche sur la facture.  

    Dans ce scénario, Susan a reçu des instructions lui demandant de proposer un acompte total de **800** pour la commande.  

    > [!IMPORTANT]  
    >  En fonction de votre pays/région, l’étape suivante peut ne pas s’appliquer.  
9.  Remplacez le montant du champ **Montant acompte HT** par **800**, puis fermez la page.  
10.  Consultez le champ **% acompte** des lignes vente : le montant a été recalculé, il est désormais de **67,02438** et **67,02282**.  

     Le nouveau calcul inclut toutes les lignes dont le pourcentage d’acompte est supérieur à 0.  

     À présent, le client demande si le pourcentage de l’acompte peut être fixé à 35 %. Le chef de Susan accepte la modification.
11.  Sur la page **Commande vente**, sur le raccourci **Acompte**, dans le champ **% acompte**, entrez **35**.  
12.  Dans l’avertissement qui s’affiche, cliquez sur le bouton **Oui** . Un taux de 35 % sera appliqué comme pourcentage du paiement de l’ensemble de la commande.  
13.  Vérifiez que les lignes ont été mises à jour en conséquence.  

## <a name="creating-a-prepayment-invoice"></a>Création d’une facture acompte  
Après avoir entré la valeur d’acompte correcte sur la commande, Susan crée la facture acompte et l’envoie au client.  

#### <a name="to-create-a-prepayment-invoice"></a>Pour créer une facture acompte

1.  Sur la page **Commande**, choisissez **Actions**, puis **Validation**, puis **Acompte**, puis **Valider et imprimer facture acompte**.
2.  Choisissez le bouton **Oui** pour valider la facture.  

> [!NOTE]  
>  Susan pourrait sélectionner **Valider et imprimer facture acompte** et envoyer par courrier la facture au client.  

## <a name="creating-an-additional-prepayment-invoice"></a>Création d’une facture acompte supplémentaire

Le jour suivant, le client appelle Susan et modifie sa commande. Il souhaite deux exemplaires de l’article 1100. Susan rouvre et met à jour la commande, puis crée une seconde facture acompte sur la commande et l’envoie au client.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Pour créer une facture acompte supplémentaire

1.  Sur la page **Commande vente**, choisissez l’action **Lancer**, puis **Rouvrir**  
2.  Sur la ligne de l’article **1896-S**, dans le champ **Quantité**, entrez **2**.  

    Dans l’action **Ordre**, choisissez **Statistiques**. Le champ **Montant acompte HT** affiche à présent **768.04** et le champ **Montant fact. acompte HT** indique **417.76**. Ceci indique qu’il existe un montant d’acompte supplémentaire qui n’a pas encore été facturé.  
3.  Pour valider une facture pour le montant d’acompte supplémentaire, choisissez **Actions**, puis **Validation**, puis **Acompte**, puis **Valider et imprimer facture acompte**.
4.  Choisissez le bouton **Oui** pour valider la facture.  

## <a name="applying-the-prepayments"></a>Lettrage des acomptes  
Le client paie le montant des acomptes. Arnie, qui travaille au département Comptabilité, enregistre le paiement et le lettre avec les factures acompte.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Pour lettrer un paiement avec les factures acompte

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles règlement**, puis sélectionnez le lien associé.  
2.  Renseignez une ligne feuille avec les informations suivantes.  

    |Nom du champ|Saisissez|  
    |----------------|-----------|  
    |**Type document**|**Paiement**|  
    |**Type compte**|**Client**|  
    |**N° compte**|**20000**|  
3.  Choisissez l’action **Traitement**, puis **Appliquer les entrées**.  
4.  Sur la page **Lettrer écritures client**, sélectionnez la première facture acompte, puis, sélectionnez l’action **Traitement** et enfin **Définir ID lettrage**.  
5.  Répétez l’étape précédente pour le deuxième acompte.  
6.  Cliquez sur le bouton **OK**.  

    Le champ montant est maintenant renseigné avec la somme des deux factures acompte.  

7.  Pour valider la feuille, choisissez l’action **Valider/Imprimer**, puis sélectionnez **Valider**.
8.  Cliquez sur le bouton **Oui**.

## <a name="invoicing-the-remaining-amount"></a>Facturation du montant ouvert

Arnie a été informé que les articles de la commande ont été expédiés et que la commande est prête pour facturation. Il crée donc la facture correspondante.  

#### <a name="to-invoice-the-remaining-amount"></a>Pour facturer le montant ouvert

1.  Ouvrez la commande vente.
2.  Choisissez l’action **Validation**, puis **Valider**.
3.  Sélectionnez **Expédition et facturation**, puis cliquez sur le bouton **OK**.
4.  Si vous souhaitez afficher un aperçu de la facture, cliquez sur le bouton **Oui**.

> [!NOTE]  
>  Normalement, le département Expédition devrait déjà avoir validé l’expédition.  

Arnie peut afficher l’historique pour vérifier que la facture vente a été créée comme prévue.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente enregistrées**, puis sélectionnez le lien associé.  

## <a name="next-steps"></a>Étapes suivantes

Cette procédure pas-à-pas vous a présenté les étapes de configuration de [!INCLUDE[prod_short](includes/prod_short.md)] pour la gestion des acomptes. Vous avez configuré des pourcentages d’acompte par défaut pour des clients et des articles et vous avez également utilisé différentes méthodes pour calculer les acomptes d’une commande. Vous avez essayé d’affecter un montant d’acompte total à la commande et vous avez enregistré le montant acompte calculé en tant que pourcentage de l’ensemble de la commande.  

Vous avez également validé une facture acompte, créé une deuxième lorsque la commande est modifiée, et validé la facture finale pour le montant ouvert.  

La fonctionnalité d’acompte de [!INCLUDE[prod_short](includes/prod_short.md)] facilite la configuration et la mise en place de règles d’acompte pour les clients et les articles. Elle vous permet également de valider tous les paiements d’une facture.  

## <a name="see-also"></a>Voir aussi  
[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
