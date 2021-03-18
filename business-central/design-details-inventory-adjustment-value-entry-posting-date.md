---
title: Date comptabilisation des écritures valeur
description: Découvrez comment le traitement par lots Ajuster coûts - Écr. article identifie et affecte une date comptabilisation aux écritures valeur que le traitement par lots est sur le point de créer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fd8ac52ae5a35114adc2e06ad8653799f7557123
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389964"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Détails de conception : date comptabilisation de l’écriture valeur d’ajustement
Cet article fournit des instructions aux utilisateurs de la fonctionnalité Évaluation stock dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’article spécifique donne des informations sur la façon dont le traitement par lots **Ajuster coûts - Écr. article** identifie et affecte une date comptabilisation aux écritures valeur que le traitement par lots est sur le point de créer.  

Tout d’abord, le concept du processus est passé en revue, c’est-à-dire la manière dont le traitement par lots identifie et affecte la date comptabilisation à l’écriture valeur à créer. Ensuite, des scénarios communs que l’équipe de support rencontre parfois sont décrits. Enfin, les concepts utilisés à partir de la version 3.0 sont résumés.  

## <a name="the-concept"></a>Le concept  
À partir de la version 5.0, le traitement par lots **Ajuster coûts - Écr. article** affecte une date comptabilisation à l’écriture valeur qu’il est sur le point de créer dans les étapes suivantes :  

1.  Initialement, la date comptabilisation de l’écriture à créer est la même que celle de l’écriture qu’elle ajuste.  

2.  La date comptabilisation est validée par rapport aux périodes inventaire et/ou aux paramètres comptabilité.  

3.  Affectation d’une date comptabilisation : si la date comptabilisation initiale n’est pas compris dans la plage de dates comptabilisation autorisées, le traitement par lots affecte une date comptabilisation autorisée à partir des paramètres comptabilité ou de la période inventaire. Si les périodes inventaire et les dates comptabilisation autorisées dans les paramètres comptabilité sont définies, la date la plus récente des deux est affectée à l’écriture valeur d’ajustement.  

 Examinons ce processus plus en détail. Supposons que nous avons une écriture comptable article de type Vente. L’article a été livré le 5 septembre 2013 et il a été facturé le jour suivant.  

![État des écritures comptables article dans le scénario](media/helene/TechArticleAdjustcost1.png "État des écritures comptables article dans le scénario")  

La première écriture valeur (379) représente l’expédition et utilise la même date comptabilisation que l’écriture comptable article parent.  

La deuxième écriture valeur (381) représente la facture.  

 La troisième écriture valeur (391) est un ajustement de l’écriture valeur de facturation (381)  

 ![État des écritures valeur dans le scénario](media/helene/TechArticleAdjustcost2.png "État des écritures valeur dans le scénario")  

 Étape 1 : l’écriture valeur d’ajustement à créer a la même date comptabilisation que l’écriture qu’elle ajuste, comme illustré ci-dessus par l’écriture valeur 391.  

 Étape 2 : validation de la date comptabilisation affectée initiale.  

Le traitement par lots **Ajuster coûts - Écr. article** détermine si la date comptabilisation initiale de l’écriture valeur d’ajustement est comprise dans la plage de dates comptabilisation autorisées en fonction des périodes inventaire et/ou des paramètres comptabilité.  

 Examinons la vente mentionnée ci-dessus en ajoutant le paramétrage des plages de dates comptabilisation autorisées.  

 Périodes inventaire :  

![Périodes inventaire dans le scénario](media/helene/TechArticleAdjustcost3.png "Périodes inventaire dans le scénario")

 La première date comptabilisation autorisée est le premier jour de la première période ouverte. 1er septembre 2013.  

 Paramètres comptabilité :  

![Configuration comptabilité dans le scénario](media/helene/TechArticleAdjustcost4.png "Configuration comptabilité dans le scénario")

 La première date comptabilisation autorisée est la date indiquée dans le champ Début période validation : 10 septembre 2013.  

 Si les périodes inventaire et les dates comptabilisation autorisées dans les paramètres comptabilité sont définies, la date la plus récente des deux définit la plage de dates comptabilisation autorisées.  

 Étape 3 : affectation d’une date comptabilisation autorisée.  

 La date comptabilisation initiale était le 6 septembre, comme illustré à l’étape 1. Toutefois, dans la 2ème étape, le traitement par lots Ajuster coûts - Écr. article identifie que la date comptabilisation autorisée la plus proche est le 10 septembre et affecte donc le 10 septembre à l’écriture valeur d’ajustement ci-dessous.  

 ![État des écritures valeur dans le scénario 2](media/helene/TechArticleAdjustcost5.png "État des écritures valeur dans le scénario 2")

 Nous avons passé en revue le concept d’affectation de dates comptabilisation aux écritures valeur créées par le traitement par lots Ajuster coûts - Écr. article.  

 Examinons maintenant certains scénarios que l’équipe de support rencontre parfois pour les dates comptabilisation affectées dans le traitement par lots Ajuster coûts – Écr article et les paramètres associés.  

## <a name="scenarios"></a>Cas de figure  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scénario I : « La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées... »  
 Dans ce scénario, l’utilisateur reçoit le message d’erreur indiqué lorsque le traitement par lots Ajuster coûts – Écr article est exécuté.  

 Dans la section précédente qui décrit le concept d’affectation de dates comptabilisation, l’intention du traitement par lots Ajuster coûts – Écr article est de créer une écriture valeur avec la date comptabilisation du 10 septembre.  

![Message d’erreur sur la date comptabilisation](media/helene/TechArticleAdjustcost6.png "Message d’erreur sur la date comptabilisation")

 Nous passons aux paramètres utilisateur :  

![Configuration des dates comptabilisation autorisées de l’utilisateur](media/helene/TechArticleAdjustcost7.png "Configuration des dates comptabilisation autorisées de l’utilisateur")

 L’utilisateur dans ce cas a une plage de dates comptabilisation autorisées allant du 11 au 30 septembre et n’est donc pas autorisé à valider l’écriture valeur d’ajustement avec la date comptabilisation du 10 septembre.  

![Aperçu de la configuration de la date comptabilisation impliquée](media/helene/TechArticleAdjustcost8.png "Aperçu de la configuration de la date comptabilisation impliquée")

 L’article de la Base de connaissances [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) décrit des scénarios supplémentaires associés au message d’erreur indiqué.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scénario II : comparaison entre la date comptabilisation de l’écriture valeur d’ajustement et la date comptabilisation de l’écriture à l’origine de l’ajustement, comme une réévaluation ou des frais annexes.  

### <a name="revaluation-scenario"></a>Scénario de réévaluation :  
 Conditions préalables :  

 Paramètres stock :  

-   Compta. coûts automatique = Oui  

-   Ajustement automatique des coûts = Toujours  

-   Type calcul coût moyen = Article  

-   Période coût moyen = Jour  

 Paramètres comptabilité :  

-   Début période validation = 1er janvier 2014  

-   Fin période validation = Vide  

 Paramètres utilisateur :  

-   Début période validation = 1er décembre 2013.  

-   Fin période validation = Vide  

##### <a name="to-test-the-scenario"></a>Pour tester le scénario  

1.  Créez un article TEST :  

     Unité de base = PCS  

     Mode évaluation stock = Moyen  

     Sélectionnez des groupes comptabilisation facultatifs.  

2.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date comptabilisation = 15 décembre 2013  

     Article = TEST  

     Type écriture = Achat  

     Quantité = 100  

     Montant unitaire = 10  

3.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date = 20 décembre 2013  

     Article = TEST  

     Type écriture = Ajustement négatif  

     Quantité = 2  

4.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date = 15 janvier 2014  

     Article = TEST  

     Type écriture = Ajustement négatif  

     Quantité = 3  

5.  Ouvrez la feuille réévaluation, puis créez et validez une ligne comme suit :  

     Article = TEST  

     Écriture lettrage = Sélectionnez l’écriture achat validée à l’étape 2. La date comptabilisation de la réévaluation est identique à l’écriture qu’elle ajuste.  

     Coût unitaire réévalué = 40  

 Les écritures comptables article et les écritures valeur suivantes ont été validées :  

![Aperçu des écritures comptables article et valeur article résultantes 1](media/helene/TechArticleAdjustcost9.png "Aperçu des écritures comptables article et valeur article résultantes 1")

 ![Aperçu des écritures comptables article et valeur article résultantes 2](media/helene/TechArticleAdjustcost10.png "Aperçu des écritures comptables article et valeur article résultantes 2")

 Le traitement par lots Ajuster coûts – Écr article a identifié une modification des coûts et ajusté les ajustements négatifs.  

 **Révision des dates comptabilisation des écritures valeur d’ajustement créées :** la date comptabilisation autorisée la plus proche à laquelle le traitement par lots Ajuster coûts – Écr article doit faire référence est le 1er janvier 2014, comme indiqué dans les paramètres comptabilité.  

 **Ajustement négatif à l’étape 3 :** la date comptabilisation affectée est le 1er janvier, qui est fournie par les paramètres comptabilité. La date comptabilisation de l’écriture valeur concernée par l’ajustement est le 20 décembre 2013. Selon les paramètres comptabilité, la date n’est pas comprise dans la plage de dates comptabilisation autorisées. Par conséquent, la date comptabilisation indiquée dans le champ Début période validation des paramètres comptabilité est affectée à l’écriture valeur d’ajustement.  

 **Ajustement négatif à l’étape 4 :** la date comptabilisation affectée est le 15 janvier. L’écriture valeur concernée par l’ajustement a une date comptabilisation fixée au 15 janvier, qui est comprise dans la plage de dates comptabilisation autorisées selon les paramètres comptabilité.  

 L’ajustement effectué pour l’ajustement négatif à l’étape 3 fait l’objet d’une discussion. La date comptabilisation favorable pour l’écriture valeur d’ajustement aurait été le 20 décembre ou au moins une date en décembre, car la réévaluation à l’origine du changement de COGS a été validée en décembre.  

 Pour procéder à l’ajustement en décembre de l’ajustement négatif à l’étape 3, le champ Début période validation dans les paramètres comptabilité doit indiquer une date en décembre.  

 **Conclusion :**  

 Avec les expériences tirées de ce scénario et en tenant compte du paramétrage le plus approprié de la plage de dates comptabilisation autorisées pour une société, la recommandation suivante peut être utile : tant que les modifications de la valeur de stock peuvent être validées dans une période, décembre en l’occurrence, le paramétrage utilisé par la société pour les plages de dates comptabilisation autorisées doit être aligné sur cette décision. Lorsque l’option Début période validation dans les paramètres comptabilité est définie sur le 1er décembre, la réévaluation effectuée en décembre peut être transférée vers les écritures sortantes affectées dans la même période.  

 Les groupes d’utilisateurs qui ne sont pas autorisés à effectuer des validations en décembre mais en janvier, ce qui était probablement censé être limité par les paramètres comptabilité dans ce scénario, devront plutôt être gérés via les paramètres utilisateur.  

### <a name="item-charge-scenario"></a>Scénario de frais annexes :  
 Conditions préalables :  

 Paramètres stock :  

-   Compta. coûts automatique = Oui  

-   Ajustement automatique des coûts = Toujours  

-   Type calcul coût moyen = Article  

-   Période coût moyen = Jour  

 Paramètres comptabilité :  

-   Début période validation = 1er décembre 2013.  

-   Fin période validation = Vide  

 Paramètres utilisateur :  

-   Début période validation = 1er décembre 2013.  

-   Fin période validation = Vide  

##### <a name="to-test-the-scenario"></a>Pour tester le scénario  

1.  Créez des frais annexes :  

     Unité de base = PCS  

     Mode évaluation stock = Moyen  

     Sélectionnez des groupes comptabilisation facultatifs.  

2.  Créer une commande achat  

     Numéro du fournisseur : 10000  

     Date comptabilisation = 15 décembre 2013  

     N° facture fournisseur : 1234  

     Sur la ligne commande achat :  

     Article = FRAIS  

     Quantité = 1  

     Coût unitaire direct = 100  

     Validez la réception et la facture.  

3.  Créez une commande vente :  

     N° donneur d’ordre : 10000  

     Date comptabilisation = 16 décembre 2013  

     Sur la ligne de commande vente :  

     Article = FRAIS  

     Quantité = 1  

     Prix unitaire = 135  

     Validez la livraison et la facture.  

4.  Paramètres comptabilité :  

     Début période validation = 1er janvier 2014  

     Fin période validation = Vide  

5.  Créez une commande achat :  

     Numéro du fournisseur : 10000  

     Date de comptabilisation = 2 janvier 2014  

     N° facture fournisseur : 2345  

     Sur la ligne commande achat :  

     Frais annexes = JB-FREIGHT  

     Quantité = 1  

     Coût unitaire direct = 3  

     Affectez les frais annexes à la réception achat à l’étape 2.  

     Validez la réception et la facture.  

     ![Aperçu des écritures comptables article et valeur article résultantes 3](media/helene/TechArticleAdjustcost11.png "Aperçu des écritures comptables article et valeur article résultantes 3")

6.  À la date du 3 janvier arrive une facture achat, contenant des frais annexes supplémentaires pour l’achat effectué à l’étape 2. La date de document de cette facture est le 30 décembre, elle est donc validée avec la date comptabilisation du 30 décembre 2013.  

     Créez une commande achat :  

     Numéro du fournisseur : 10000  

     Date comptabilisation = 30 décembre 2013  

     N° facture fournisseur : 3456  

     Sur la ligne commande achat :  

     Frais annexes = JB-FREIGHT  

     Quantité = 1  

     Coût unitaire direct = 2  

     Affectez les frais annexes à la réception achat à l’étape 2  

     Validez la réception et la facture.  

   ![Aperçu des écritures comptables article et valeur article résultantes 4](media/helene/TechArticleAdjustcost12.png "Aperçu des écritures comptables article et valeur article résultantes 4")

 L’état Évaluation du stock est imprimé à la date du 31 décembre 2013  

![Contenu du rapport d’évaluation du stock](media/helene/TechArticleAdjustcost13.png "Contenu du rapport d’évaluation du stock")

 **Résumé du scénario :**  

 Le scénario décrit se termine avec un état Évaluation du stock indiquant Quantité = 0 alors que la valeur = 2. Les frais annexes validés à l’étape 11 font partie de la valeur d’entrée de stock de décembre alors que la valeur Sortie de stock pour la même période n’est pas affectée.  

 Définir l’option Début période validation au 1er janvier dans les paramètres comptabilité était recommandé pour les premiers frais annexes. Les coûts de l’entrée et de la sortie de stock ont été enregistrés dans la même période. Cependant, pour les deuxièmes frais annexes, le changement de COGS est reconnu dans la période suivante.  

 **Conclusion :**  

 Il est difficile d’avoir un état Évaluation du stock indiquant Quantité = 0 alors que la valeur <> 0. Dans ce cas, il est également plus difficile d’exprimer des paramètres optimaux, étant donné que les factures achat arrivent le même jour mais couvrent différentes périodes ou même différents exercices comptables. Le passage à un nouvel exercice comptable nécessite généralement une planification et à cet effet, le processus Ajuster coûts – Écr article qui reconnaît COGS, doit être pris en compte.  

 Dans ce scénario, une solution aurait pu être que le champ Début période validation dans les paramètres comptabilité indique une date en décembre pour quelques jours de plus et que la validation des premiers frais annexes soit reportée pour que tous les coûts de la période ou de l’exercice précédent soient reconnus pour la période à laquelle ils appartiennent. Ainsi, le traitement par lots Ajuster coûts – Écr. article serait exécuté et la date comptabilisation autorisée serait déplacée vers la nouvelle période ou le nouvel exercice. Les premiers frais annexes avec la date comptabilisation du 2 janvier peuvent ensuite être validés.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historique du traitement par lots Ajuster coûts – Écr. article  
 Voici un résumé du concept d’affectation de dates comptabilisation aux écritures valeur d’ajustement par le traitement par lots Ajuster coûts – Écr article depuis la version 3.0.  

### <a name="from-version-30370a"></a>À partir de la version 3.0..3.70.A  
 Dans le formulaire de demande du traitement par lots Ajuster coûts - Écr. article, la date comptabilisation doit être saisie par l’utilisateur. Le traitement par lots exécute toutes les modifications nécessaires et crée des écritures valeur avec la date comptabilisation saisie dans le formulaire de demande. La date comptabilisation suggérée à utiliser est la date du jour.  

### <a name="version-370b40"></a>Version 3.70.B..4.0  
 Dans le formulaire de demande du traitement par lots Ajuster coûts - Écr. article, la date comptabilisation écriture période clôturée doit être saisie par l’utilisateur. Le traitement par lots exécute toutes les modifications nécessaires et crée des écritures valeur avec la date comptabilisation de l’écriture comptable article parent (date d’expédition de la vente concernée par l’ajustement). Si la date comptabilisation de l’écriture comptable article parent n’est pas comprise dans la plage de dates comptabilisation autorisées, la date comptabilisation indiquée comme date comptabilisation écriture période clôturée sera affectée à l’écriture valeur d’ajustement. Une date est considérée comme incluse dans une période clôturée lorsqu’elle est antérieure à la date indiquée dans le champ Début période validation dans les paramètres comptabilité.  

### <a name="from-version-50"></a>À partir de la version 5.0 :  
 Il n’est plus nécessaire d’indiquer une date comptabilisation dans le formulaire de demande du traitement par lots Ajuster coûts - Écr. article. Le traitement par lots exécute toutes les modifications nécessaires et crée des écritures valeur avec la date comptabilisation de l’écriture valeur qu’il ajuste. Si la date comptabilisation n’est pas comprise dans la plage de dates comptabilisation autorisées dans le champ Début période validation des paramètres comptabilité ou si les périodes inventaire sont utilisées, la date la plus récente des deux sera utilisée. Reportez-vous au concept décrit ci-dessus.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historique du traitement par lots Valider coûts ajustés  
 Le traitement par lots Valider coût ajustés est étroitement lié au traitement par lots Ajuster coûts – Écr article. C’est pourquoi l’historique de ce traitement par lots est résumé et partagé ici également.  

### <a name="from-version-30370a"></a>À partir de la version 3.0..3.70.A  
 Dans le formulaire de demande du traitement par lots Valider coûts ajustés, une date comptabilisation doit être saisie par l’utilisateur. Le traitement par lots exécute toutes les écritures valeur correspondant au filtre, le cas échéant, et crée des écritures comptables avec la date comptabilisation saisie dans le formulaire de demande.  

### <a name="version-370b40"></a>Version 3.70.B..4.0  
 Dans le formulaire de demande du traitement par lots Valider coûts ajustés, le champ Date comptabilisation écriture période clôturée est disponible. L’application utilise la date que vous saisissez dans ce champ comme date comptabilisation pour les écritures comptables qu’il crée pour les écritures valeur dont les dates comptabilisation se trouvent dans des périodes comptables clôturées. Sinon, les écritures comptables auront la même date comptabilisation que les écritures valeur d’origine. Une date est considérée comme incluse dans une période clôturée lorsqu’elle est antérieure à la date indiquée dans le champ Début période validation dans les paramètres comptabilité. En cas de validation en comptabilité par groupe comptabilisation, les écritures comptables auront la date comptabilisation spécifiée dans le champ Date comptabilisation du formulaire de demande.  

 Dans la version 3 et 4, le traitement par lot analyse toutes les écritures valeur pour détecter s’il existe des écritures valeur dont le coût total (réel) diffère du coût validé en comptabilité. Si une différence est détectée, le montant différent sera validé dans une écriture comptable. Si la comptabilisation des coûts prévus est utilisée, les champs correspondants sont traités de la même manière.  

![Coût réel comparé au coût prévu](media/helene/TechArticleAdjustcost14.png "Coût réel comparé au coût prévu")

### <a name="from-version-50"></a>À partir de la version 5.0 :  
 Il n’est plus nécessaire d’indiquer une date comptabilisation dans le formulaire de demande du traitement par lots Valider coûts ajustés. L’écriture comptable est créée avec la même date comptabilisation que l’écriture valeur associée. Pour exécuter le traitement par lots, la plage de dates comptabilisation autorisées doit autoriser la date comptabilisation de l’écriture comptable créée. Sinon, la plage de dates comptabilisation autorisées doit être temporairement rouverte en modifiant ou en supprimant les dates des champs Début période validation et Fin période validation dans les paramètres comptabilité. Pour éviter les problèmes de rapprochement, la date comptabilisation de l’écriture comptable doit correspondre à la date comptabilisation de l’écriture valeur.  

 Le traitement par lots analyse la table 5811 - Valider écriture valeur en comptabilité pour identifier les écritures valeur concernées par la validation en comptabilité. Une fois l’exécution réussie, la table est vidée.

## <a name="see-also"></a>Voir aussi  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]