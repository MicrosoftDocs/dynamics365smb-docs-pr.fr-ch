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
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440755"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Détails de conception : date comptabilisation de l’écriture valeur d’ajustement  

Cet article fournit des instructions aux utilisateurs de la fonctionnalité Évaluation stock dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’article spécifique donne des informations sur la façon dont le traitement par lots **Ajuster coûts - Écr. article** identifie et affecte une date comptabilisation aux écritures valeur que le traitement par lots est sur le point de créer.  

Tout d’abord, le concept du processus est passé en revue, c’est-à-dire la manière dont le traitement par lots identifie et affecte la date comptabilisation à l’écriture valeur à créer. Ensuite, des scénarios communs que l’équipe de support rencontre parfois sont décrits. Enfin, les concepts utilisés sont résumés.  

## <a name="the-concept"></a>Le concept  

Le traitement par lots **Ajuster coûts - Écr. article** affecte une date comptabilisation à l’écriture valeur qu’il est sur le point de créer dans les étapes suivantes :  

1.  Initialement, la date comptabilisation de l’écriture à créer est la même que celle de l’écriture qu’elle ajuste.  

2.  La date comptabilisation est validée par rapport aux périodes inventaire et/ou aux paramètres comptabilité.  

3.  Affectation d’une date comptabilisation : si la date comptabilisation initiale n’est pas compris dans la plage de dates comptabilisation autorisées, le traitement par lots affecte une date comptabilisation autorisée à partir des paramètres comptabilité ou de la période inventaire. Si les périodes inventaire et les dates comptabilisation autorisées dans les paramètres comptabilité sont définies, la date la plus récente des deux est affectée à l’écriture valeur d’ajustement.  

 Examinons ce processus plus en détail. Supposons que nous avons une écriture comptable article de type Vente. L’article a été livré le 5 septembre 2020 et il a été facturé le jour suivant.  


**Écriture comptable article**  
Format de date YYYY-MM-DD

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture  | N° document |Code magasin  |Quantité  |Coût total (réel)  |Quantité facturée  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020/09/05     |  Vente       |102033     |  Bleu       | -1    |    -11     |-1     |    0     |

La première écriture valeur (379) représente l’expédition et utilise la même date comptabilisation que l’écriture comptable article parent.  
  
La deuxième écriture valeur (381) représente la facture.  

La troisième écriture valeur (391) est un ajustement de l’écriture valeur de facturation (381).  
  

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture comptable article  |Type écriture  |N° document  |N° écriture comptable article  |Code magasin  |Quantité écriture comptable article  |Quantité facturée  |Coût total (réel)  |Coût total (prévu)  |Ajustement  |Ecriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020/09/05     |    Vente     | Coût direct   | 102033        |319     | Bleu        | -1       |0         |  0       |     -10   |Non   |0    |Ventes          |
|381     |  A       |    2020/09/06     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |-1        |-10       |    10     | Non  |0      |       Ventes   |
|391     |  A       |    2020/09/10     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |0         |-1        |    0     |Oui   |    181   | AJSTK   |

La date comptabilisation de l’écriture d’ajustement est initialement définie sur la même date comptabilisation que celle de l’écriture qu’elle ajuste.

 Étape 1 : l’écriture valeur d’ajustement à créer a la même date comptabilisation que l’écriture qu’elle ajuste, comme illustré ci-dessus par l’écriture valeur 391.  
  
 Étape 2 : validation de la date comptabilisation affectée initiale.  

Le traitement par lots **Ajuster coûts - Écr. article** détermine si la date comptabilisation initiale de l’écriture valeur d’ajustement est comprise dans la plage de dates comptabilisation autorisées en fonction des périodes inventaire et/ou des paramètres comptabilité.  

Examinons la vente mentionnée ci-dessus en ajoutant le paramétrage des plages de dates comptabilisation autorisées.  
  
**Périodes inventaire**

|Date de fin  |Name  |Fermé  |
|---------|---------|---------|
|2020/01/31     |2020 janvier      |  Oui    |
|2020/02/28     |Février 2020     |  Oui    |
|2020/03/31     |Mars 2020        |  Oui    |
|2020/04/30     |Avril 2020        |  Oui    |
|2020/05/31     |Mai 2020        |  Oui    |
|2020/06/30     |Juin 2020       |  Oui    |
|2020/07/31     |Juillet 2020        |   Oui   |
|2020/08/31     |Août 2020     |   Oui   |
|2020/09/30     |Septembre 2020  |         |
|2020/10/31     |Octobre 2020    |         |
|2020/11/30     |Novembre 2020   |         |
|2020/12/31     |Décembre 2020   |         |

La première date comptabilisation autorisée est le premier jour de la première période ouverte. 1 septembre 2020.  

**Paramètres comptabilité**

|Champ|Valeur  |
|---------|---------|
|Début période validation :  |  2020/09/10      |
|Fin période validation :    |  2020/09/30      |
|Registre temps :       |         |
|Format adresse local :|   Code postal      |  

 La première date comptabilisation autorisée est la date indiquée dans le champ Début période validation : 10 septembre 2020.  
 Si les périodes inventaire et les dates comptabilisation autorisées dans les paramètres comptabilité sont définies, la date la plus récente des deux définit la plage de dates comptabilisation autorisées.  

 Étape 3 : affectation d’une date comptabilisation autorisée.  

 La date comptabilisation initiale était le 6 septembre, comme illustré à l’étape 1. Toutefois, dans la deuxième étape, le traitement par lots Ajuster coûts - Écr. article identifie que la date comptabilisation autorisée la plus proche est le 10 septembre et affecte donc le 10 septembre à l’écriture valeur d’ajustement ci-dessous.  

   
|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture comptable article  |Type écriture  |N° document  |N° écriture comptable article  |Code magasin  |Quantité écriture comptable article  |Quantité facturée  |Coût total (réel)  |Coût total (prévu)  |Ajustement  |Ecriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020/09/05     |    Vente     | Coût direct   | 102033        |319     | Bleu        | -1       |0         |  0       |     -10   |Non   |0    |Ventes          |
|381     |  A       |    2020/09/06     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |-1        |-10       |    10     | Non  |0      |       Ventes   |
|391     |  A       |    **2020-09-10**     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |0         |-1        |    0     |Oui   |    181   | AJSTK   |

 Nous avons passé en revue le concept d’affectation de dates comptabilisation aux écritures valeur créées par le traitement par lots Ajuster coûts - Écr. article.  

 Examinons maintenant certains scénarios que l’équipe de support rencontre parfois pour les dates comptabilisation affectées dans le traitement par lots Ajuster coûts – Écr article et les paramètres associés.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scénario I : « La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées... »  

 Dans ce scénario, l’utilisateur reçoit le message d’erreur indiqué lorsque le traitement par lots Ajuster coûts – Écr article est exécuté.  

 Dans la section précédente qui décrit le concept d’affectation de dates comptabilisation, l’intention du traitement par lots Ajuster coûts – Écr article est de créer une écriture valeur avec la date comptabilisation du 10 septembre.  

![Message d’erreur sur la date comptabilisation.](media/helene/TechArticleAdjustcost6.png "Message d’erreur sur la date comptabilisation")

 Nous passons aux paramètres utilisateur :  

**Paramètres utilisateur**  

Tri : ID utilisateur  

|ID utilisateur  |Début période validation  | Fin période validation  |
|---------|---------|--------|
|EUROPE  |  2020/09/11      |2020/09/30      |

 L’utilisateur dans ce cas a une plage de dates comptabilisation autorisées allant du 11 au 30 septembre et n’est donc pas autorisé à valider l’écriture valeur d’ajustement avec la date comptabilisation du 10 septembre.  

### <a name="overview-of-involved-posting-date-setup"></a>Aperçu de la configuration de la date comptabilisation impliquée :

**Périodes inventaire**  

|Date de fin  |Name  |Fermé  |
|---------|---------|---------|
|2020/01/31     |2020 janvier      |  Oui    |
|2020/02/28     |Février 2020     |  Oui    |
|2020/03/31     |Mars 2020        |  Oui    |
|2020/04/30     |Avril 2020        |  Oui    |
|2020/05/31     |Mai 2020        |  Oui    |
|2020/06/30     |Juin 2020       |  Oui    |
|2020/07/31     |Juillet 2020        |   Oui   |
|2020/08/31     |Août 2020     |   Oui   |
|2020/09/30     |Septembre 2020  |         |
|2020/10/31     |Octobre 2020    |         |
|2020/11/30     |Novembre 2020   |         |
|2020/12/31     |Décembre 2020   |         |  

**Paramètres comptabilité**  

|Champ|Valeur|
|---------|---------|
|Début période validation :  |  2020/09/10      |
|Fin période validation :    |  2020/09/30      |
|Registre temps :       |         |
|Format adresse local :|   Code postal      |  

**Paramètres utilisateur**    

|ID utilisateur  |Début période validation  | Fin période validation  |
|---------|---------|--------|
|USERNAME |  2020/09/10      |2020/09/30      |

 En attribuant à l’utilisateur une plage de dates comptabilisation autorisée plus large (ou identique) que dans la période inventaire ou les paramètres comptabilité, le conflit mentionné sera évité. L’écriture valeur d’ajustement avec la date comptabilisation du 10 septembre sera publiée avec succès avec cette configuration.

Un ancien article de la Base de connaissances [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) décrit d’autres scénarios associés au message d’erreur indiqué.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scénario II : comparaison entre la date comptabilisation de l’écriture valeur d’ajustement et la date comptabilisation de l’écriture à l’origine de l’ajustement, comme une réévaluation ou des frais annexes.  

### <a name="revaluation-scenario"></a>Scénario de réévaluation :  

 Conditions préalables :  

 Paramètres stock :  
me
-   Compta. coûts automatique = Oui  

-   Ajustement automatique des coûts = Toujours  

-   Type calcul coût moyen = Article  

-   Période coût moyen = Jour  

 Paramètres comptabilité :  

-   Début période validation = 1er janvier 2021  

-   Fin période validation = Vide  

 Paramètres utilisateur :  

-   Début période validation = 1er décembre 2020  

-   Fin période validation = Vide  

### <a name="to-test-the-scenario"></a>Pour tester le scénario  

1.  Créez un article TEST :  

     Unité de base = PCS  

     Mode évaluation stock = Moyen  

     Sélectionnez des groupes comptabilisation facultatifs.  

2.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date comptabilisation = 15 décembre 2020  

     Article = TEST  

     Type écriture = Achat  

     Quantité = 100  

     Montant unitaire = 10  

3.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date = 20 décembre 2020  

     Article = TEST  

     Type écriture = Ajustement négatif  

     Quantité = 2  

4.  Ouvrez la feuille article, puis créez et validez une ligne comme suit :  

     Date = 15 janvier 2021  

     Article = TEST  

     Type écriture = Ajustement négatif  

     Quantité = 3  

5.  Ouvrez la feuille réévaluation, puis créez et validez une ligne comme suit :  

     Article = TEST  

     Écriture lettrage = Sélectionnez l’écriture achat validée à l’étape 2. La date comptabilisation de la réévaluation est identique à l’écriture qu’elle ajuste.  

     Coût unitaire réévalué = 40  

Les **écritures comptables article** et les **écritures valeur** suivantes ont été validées :  

**Écriture comptable article - achat** :  
Format de date YYYY-MM-DD  

|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020/12/15         |Achats         |T00001         |100         |4000         |95        |

**Écritures valeur**  

|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  |Quantité écriture numéro article  |Coût total (réel)  |Coût validé en comptabilité  |Ajustement  |Écriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020/12/15    |317         |Achats         |Coût direct         |T00001         |100         |1 000,00          |1 000,00    |Non         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Achats         |Réévaluation         |T04002         |0         |3 000,00         |3 000,00         |Non         |0         |REVALINL         |

**Écriture comptable article - ajustement négatif, étape 3**  

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020/12/20   |Ajustement négatif  |T00002         |-2         |-80         | 0        |

**Écritures valeur**  

|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  |Quantité écriture numéro article  |Coût total (réel)  |Coût validé en comptabilité  |Ajustement  |Écriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020/12/20    |318         |Ajustement négatif         |Coût direct         |T00002         |-2         |-20          |-20    |Non         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Ajustement négatif         |Coût direct         |T04002         |0         |-60         |-60         |Oui         |377         |INVTADAMT         |

**Écriture comptable article - ajustement négatif, étape 4**  

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021/01/15   |Ajustement négatif  |T00003         |-3         |-120         | 0        |

**Écritures valeur**  

|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  |Quantité écriture numéro article  |Coût total (réel)  |Coût validé en comptabilité  |Ajustement  |Écriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021/01/15    |319         |Ajustement négatif         |Coût direct         |T00003         |-3         |-30          |-30    |Non         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Ajustement négatif         |Coût direct         |T04003         |0         |-90         |-90         |Oui         |378         |INVTADAMT         |

Le traitement par lots Ajuster coûts – Écr article a identifié une modification des coûts et ajusté les ajustements négatifs.  

**Révision des dates comptabilisation des écritures valeur d’ajustement créées :** la date comptabilisation autorisée la plus proche à laquelle le traitement par lots Ajuster coûts – Écr article doit faire référence est le 1er janvier 2021, comme indiqué dans les paramètres comptabilité.  

**Ajustement négatif à l’étape 3 :** la date comptabilisation affectée est le 1er janvier, qui est fournie par les paramètres comptabilité. La date comptabilisation de l’écriture valeur concernée par l’ajustement est le 20 décembre 2020. Selon les paramètres comptabilité, la date n’est pas comprise dans la plage de dates comptabilisation autorisées. Par conséquent, la date comptabilisation indiquée dans le champ Début période validation des paramètres comptabilité est affectée à l’écriture valeur d’ajustement.  

**Ajustement négatif à l’étape 4 :** la date comptabilisation affectée est le 15 janvier. L’écriture valeur concernée par l’ajustement a une date comptabilisation fixée au 15 janvier, qui est comprise dans la plage de dates comptabilisation autorisées selon les paramètres comptabilité.  

L’ajustement effectué pour l’ajustement négatif à l’étape 3 fait l’objet d’une discussion. La date comptabilisation favorable pour l’écriture valeur d’ajustement aurait été le 20 décembre ou au moins une date en décembre, car la réévaluation à l’origine du changement de COGS a été validée en décembre.  

Pour procéder à l’ajustement en décembre de l’ajustement négatif à l’étape 3, le champ Début période validation dans les paramètres comptabilité doit indiquer une date en décembre.  

**Conclusion :**  

Avec les expériences tirées de ce scénario et en tenant compte du paramétrage le plus approprié de la plage de dates comptabilisation autorisées pour une société, l’information suivante peut s’avérer utile : tant que vous autorisez la vaidation des modifications de la valeur de stock dans une période, décembre en l’occurrence, le paramétrage utilisé par la société pour les plages de dates comptabilisation autorisées doit être aligné sur cette décision. Lorsque l’option Début période validation dans les paramètres comptabilité est définie sur le 1er décembre, la réévaluation effectuée en décembre peut être transférée vers les écritures sortantes affectées dans la même période.  

Les groupes d’utilisateurs qui ne sont pas autorisés à effectuer des validations en décembre mais en janvier, ce qui était probablement censé être limité par les paramètres comptabilité dans ce scénario, devront plutôt être gérés via les paramètres utilisateur.  

### <a name="item-charge-scenario"></a>Scénario de frais annexes :  

 Conditions préalables :  

 Paramètres stock :  

-   Compta. coûts automatique = Oui  

-   Ajustement automatique des coûts = Toujours  

-   Type calcul coût moyen = Article  

-   Période coût moyen = Jour  

 Paramètres comptabilité :  

-   Début période validation = 1er décembre 2020.  

-   Fin période validation = Vide  

 Paramètres utilisateur :  

-   Début période validation = 1er décembre 2020.  

-   Fin période validation = Vide  


### <a name="to-test-the-scenario"></a>Pour tester le scénario  

1.  Créez des frais annexes :  

     Unité de base = PCS  

     Mode évaluation stock = Moyen  

     Sélectionnez des groupes comptabilisation facultatifs.  

2.  Créer une commande achat  

     Numéro du fournisseur : 10000  

     Date comptabilisation = 15 décembre 2020

     N° facture fournisseur : 1234  

     Sur la ligne commande achat :  

     Article = FRAIS  

     Quantité = 1  

     Coût unitaire direct = 100  

     Validez la réception et la facture.  

3.  Créez une commande vente :  

     N° donneur d’ordre : 10000  

     Date comptabilisation = 16 décembre 2020  

     Sur la ligne de commande vente :  

     Article = FRAIS  

     Quantité = 1  

     Prix unitaire = 135  

     Validez la livraison et la facture.  

4.  Paramètres comptabilité :  

     Début période validation = 1er janvier 2021  

     Fin période validation = Vide  

5.  Créez une commande achat :  

     Numéro du fournisseur : 10000  

     Date de comptabilisation = 2 janvier 2021  

     N° facture fournisseur : 2345  

     Sur la ligne commande achat :  

     Frais annexes = JB-FREIGHT  

     Quantité = 1  

     Coût unitaire direct = 3  

     Affectez les frais annexes à la réception achat à l’étape 2.  

     Validez la réception et la facture.  


**Statut écriture comptable article achat, étape 2** :  
  
|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |FRAIS         |2020/12/15         |Achats         |107030         |1         |105         |0        |

**Écritures valeur**  

|Numéro d’écriture |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  | N° frais annexes    |  Quantité écriture comptable article   |Coût total (réel)     |Coût validé en comptabilité |Ajustement |Ecriture lettrage |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |FRAIS|   2020/12/15    |324         |Achats         |Coût direct         |108029         |         |1          |100    |100         |Nº         |0         |
|399      |FRAIS   |2021/01/02    |324         |Achats         |Coût direct         |108009         |JBFREIGHT         |0         |3         |3         |Nº         |0         |


**Statut écriture comptable article vente** :  
  
|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |FRAIS         |2020/12/16         |Vente         |102035         |-1         |-105         |0        |

**Écritures valeur**  

|Numéro d’écriture |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  | N° frais annexes    |  Quantité écriture comptable article   |Coût total (réel)     |Coût validé en comptabilité |Ajustement |Ecriture lettrage |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |FRAIS|   2020/12/16    |325         |Vente         |Coût direct         |109024         |         |-1          |-100    |-100         |Nº         |0         |
|400      |FRAIS   |2021/01/01    |325         |Vente         |Coût direct         |109024         |         |0         |-3         |-3         |Oui         |398         |


6.  À la date du 3 janvier arrive une facture achat, contenant des frais annexes supplémentaires pour l’achat effectué à l’étape 2. La date de document de cette facture est le 30 décembre, elle est donc validée avec la date comptabilisation du 30 décembre 2020.  

     Créez une commande achat :  

     Numéro du fournisseur : 10000  

     Date comptabilisation = 30 décembre 2020  

     N° facture fournisseur : 3456  

     Sur la ligne commande achat :  

     Frais annexes = JB-FREIGHT  

     Quantité = 1  

     Coût unitaire direct = 2  

     Affectez les frais annexes à la réception achat à l’étape 2  

     Validez la réception et la facture.  


**Statut écriture comptable article achat** :  

|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |FRAIS         |2020/12/15         |Achats         |107030         |1         |105         |0        |

**Écritures valeur**  

|Numéro de la séquence |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  | N° frais annexes    |  Quantité écriture comptable article   |Coût total (réel)     |Coût validé en comptabilité |Ajustement |Ecriture lettrage |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |FRAIS   |2020/12/15    |324         |Achats         |Coût direct         |108029         |            |1         |100    |100         |Non         |0         |
|399      |FRAIS   |2021/01/02    |324         |Achats         |Coût direct         |108030         |JBFREIGHT   |0         |3         |3         |Non         |0         |
|401      |FRAIS   |**2020-12-30**    |324         |Achats         |Coût direct         |108031         |JBFREIGHT   |0         |2         |2         |Non         |0         |

**Statut écriture comptable article vente** :  
  
|Numéro d’écriture  |Nombre d’articles  |Date comptabilisation  |Type écriture  |N° document  |Quantité  |Coût total (réel)  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |FRAIS         |2020/12/16         |Vente         |102035         |-1         |-105         |0        |

**Écritures valeur**  

|Numéro de la séquence |Nombre d’articles  |Date comptabilisation  |N° écriture comptable article  |Type écriture comptable article  |Type écriture  |N° document  | N° frais annexes    |  Quantité écriture comptable article   |Coût total (réel)     |Coût validé en comptabilité |Ajustement |Ecriture lettrage |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |FRAIS   |2020/12/16        |325         |Vente         |Coût direct         |103024         |            |-1         |-100       |-100         |Non         |0         |
|400      |FRAIS   |2021/01/01        |325         |Vente         |Coût direct         |103024         |            |0          |-3         |-3         |Oui         |398         |
|402      |FRAIS   |**2021-01-01**    |325         |Vente         |Coût direct         |103024         |            |0          |-2         |-2         |Oui         |398         |

L’état Évaluation du stock est imprimé à la date du 31 décembre 2020

![Contenu du rapport d’évaluation du stock.](media/helene/TechArticleAdjustcost13.png "Contenu du rapport d’évaluation du stock")

 **Résumé du scénario :**  

 Le scénario décrit se termine avec un état Évaluation du stock indiquant Quantité = 0 alors que la valeur = 2. Les frais annexes validés à l’étape 11 font partie de la valeur d’entrée de stock de décembre alors que la valeur Sortie de stock pour la même période n’est pas affectée.  

 Définir l’option Début période validation au 1er janvier dans les paramètres comptabilité était recommandé pour les premiers frais annexes. Les coûts de l’entrée et de la sortie de stock ont été enregistrés dans la même période. Cependant, pour les deuxièmes frais annexes, le changement de COGS est reconnu dans la période suivante.  

 **Conclusion :**  

 Il est difficile d’avoir un état Évaluation du stock indiquant Quantité = 0 alors que la valeur <> 0. Dans ce cas, il est également plus difficile d’exprimer des paramètres optimaux, étant donné que les factures achat arrivent le même jour mais couvrent différentes périodes ou même différents exercices comptables. Le passage à un nouvel exercice comptable nécessite généralement une planification et à cet effet, le processus Ajuster coûts – Écr article qui reconnaît COGS, doit être pris en compte.  

 Dans ce scénario, une solution aurait pu être que le champ Début période validation dans les paramètres comptabilité indique une date en décembre pour quelques jours de plus et que la validation des premiers frais annexes soit reportée pour que tous les coûts de la période ou de l’exercice précédent soient reconnus pour la période à laquelle ils appartiennent. Ainsi, le traitement par lots Ajuster coûts – Écr. article serait exécuté et la date comptabilisation autorisée serait déplacée vers la nouvelle période\/le nouvel exercice. Les premiers frais annexes avec la date comptabilisation du 2 janvier peuvent ensuite être validés.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historique du traitement par lots Ajuster coûts – Écr. article  

 Voici un résumé du concept d’affectation de dates comptabilisation aux écritures valeur d’ajustement par le traitement par lots Ajuster coûts – Écr article.  

### <a name="about-the-request-form-posting-date"></a>À propos de la date comptabilisation du formulaire de sélection :  

 Il n’est plus nécessaire d’indiquer une date comptabilisation dans le formulaire de demande du traitement par lots Ajuster coûts - Écr. article. Le traitement par lots exécute toutes les modifications nécessaires et crée des écritures valeur avec la date comptabilisation de l’écriture valeur qu’il ajuste. Si la date comptabilisation n’est pas comprise dans la plage de dates comptabilisation autorisées dans le champ Début période validation des paramètres comptabilité ou si les périodes inventaire sont utilisées, la date la plus récente des deux sera utilisée. Reportez-vous au concept décrit ci-dessus.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historique du traitement par lots Valider coûts ajustés  

 Le traitement par lots Valider coût ajustés est étroitement lié au traitement par lots Ajuster coûts – Écr article. C’est pourquoi l’historique de ce traitement par lots est résumé et partagé ici également.  
 
![Coût réel comparé au coût prévu.](media/helene/TechArticleAdjustcost14.png "Coût réel comparé au coût prévu")

### <a name="about-the-posting-date"></a>À propos de la date comptabilisation  

 Il n’est plus nécessaire d’indiquer une date comptabilisation dans le formulaire de demande du traitement par lots Valider coûts ajustés. L’écriture comptable est créée avec la même date comptabilisation que l’écriture valeur associée. Pour exécuter le traitement par lots, la plage de dates comptabilisation autorisées doit autoriser la date comptabilisation de l’écriture comptable créée. Sinon, la plage de dates comptabilisation autorisées doit être temporairement rouverte en modifiant ou en supprimant les dates des champs Début période validation et Fin période validation dans les paramètres comptabilité. Pour éviter les problèmes de rapprochement, la date comptabilisation de l’écriture comptable doit correspondre à la date comptabilisation de l’écriture valeur.  

 Le traitement par lots analyse la table 5811 - Valider écriture valeur en comptabilité pour identifier les écritures valeur concernées par la validation en comptabilité. Une fois l’exécution réussie, la table est vidée.

## <a name="see-also"></a>Voir aussi  

[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
