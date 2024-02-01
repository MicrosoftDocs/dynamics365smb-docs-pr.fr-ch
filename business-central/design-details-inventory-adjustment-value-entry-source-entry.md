---
title: Date comptabilisation sur l’écriture valeur d’ajustement par rapport à l’écriture source
description: "Découvrez le scénario «\_Comparaison entre la date comptabilisation de l’écriture valeur d’ajustement et la date comptabilisation de l’écriture à l’origine de l’ajustement, comme une réévaluation ou des frais annexes\_» lors de l’exécution du traitement par lots Ajuster coûts\_: Écr. article."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Date comptabilisation sur l’écriture valeur d’ajustement par rapport à l’écriture source

Cet article compare la Date comptabilisation de l’écriture valeur d’ajustement et la date comptabilisation de l’écriture à l’origine de l’ajustement provoquant l’exécution du traitement par lots Ajuster coûts : Écr. article, en particulier un scénario de réévaluation et un scénario de frais annexes.

Le traitement par lots **Ajuster coûts : Écr. article** traitera vos données en fonction de votre scénario et de la configuration de [!INCLUDE[prod_short](includes/prod_short.md)]. Dans cette section, nous décrivons deux processus distincts et, pour chacun, nous montrons le type d’impact du traitement par lots Ajuster coûts : Écr. article sur les données.

## Scénario de réévaluation

### Conditions préalables  

Veuillez saisir les valeurs suivantes :

**Paramètres stock** :  

- Compta. coûts automatique = Oui  

- Ajustement automatique des coûts = Toujours  

- Type calcul coût moyen = Article  

- Période coût moyen = Jour  

**Paramètres comptabilité** :  

- Début période validation = 1er janvier 2021  

- Fin période validation = Vide  

**Paramètres utilisateur** :  

- Début période validation = 1er décembre 2020  

- Fin période validation = Vide  

### Pour tester le scénario

Testez ce scénario en effectuant les étapes suivantes.

1. Créez un **Article** appelé TEST avec les valeurs suivantes :  

     - Unité de base = PCS  

     - Mode évaluation stock = Moyen  

     - Sélectionnez des groupes comptabilisation facultatifs.  

2. Ouvrez une **feuille article**, puis créez une nouvelle et validez une ligne comme suit :  

     - Date comptabilisation = 15 décembre 2020  

     - Article = TEST  

     - Type écriture = Achat  

     - Quantité = 100  

     - Montant unitaire = 10  

3. Ouvrez une **feuille article**, puis créez une nouvelle et validez une ligne comme suit :  

     - Date = 20 décembre 2020  

     - Article = TEST  

     - Type écriture = Ajustement négatif  

     - Quantité = 2  

4. Ouvrez une **feuille article**, puis créez une nouvelle et validez une ligne comme suit :  

     - Date = 15 janvier 2021  

     - Article = TEST  

     - Type écriture = Ajustement négatif  

     - Quantité = 3  

5. Ouvrez une **feuille réévaluation article**, puis créez une nouvelle et validez une ligne comme suit :  

     - Article = TEST  

     - Écriture lettrage = Sélectionnez l’écriture achat validée à l’étape 2. La date comptabilisation de la réévaluation est identique à l’écriture qu’elle ajuste.  

     - Coût unitaire (réévalué) = 40  

Les **écritures comptables article** et les **écritures valeur** suivantes ont été validées :  

**Écriture comptable article - achat** :  

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

Le traitement par lots **Ajuster coûts – Écr. article** a identifié une modification des coûts et ajusté les ajustements négatifs.  

**Révision des dates comptabilisation des écritures valeur d’ajustement créées :** la date comptabilisation autorisée la plus proche à laquelle le traitement par lots Ajuster coûts – Écr article doit faire référence est le 1er janvier 2021, comme indiqué dans les paramètres comptabilité.  

**Ajustement négatif à l’étape 3 :** la date comptabilisation affectée est le 1er janvier, qui est fournie par les paramètres comptabilité. La date comptabilisation de l’écriture valeur concernée dans l’étendue de l’ajustement est le 20 décembre 2020. Selon les paramètres comptabilité, la date n’est pas comprise dans la plage de dates comptabilisation autorisées. Par conséquent, la date comptabilisation indiquée dans le champ Début période validation des paramètres comptabilité est affectée à l’écriture valeur d’ajustement.  

**Ajustement négatif à l’étape 4 :** la date comptabilisation affectée est le 15 janvier. L’écriture valeur concernée par l’ajustement a une date comptabilisation fixée au 15 janvier, qui est comprise dans la plage de dates comptabilisation autorisées selon les paramètres comptabilité.  

L’ajustement effectué pour l’ajustement négatif à l’étape 3 fait l’objet d’une discussion. La date comptabilisation favorable pour l’écriture valeur d’ajustement aurait été le 20 décembre ou au moins une date en décembre, car la réévaluation à l’origine du changement de COGS a été validée en décembre.  

Pour procéder à l’ajustement en décembre de l’ajustement négatif à l’étape 3, le champ Début période validation dans les paramètres comptabilité doit indiquer une date en décembre.  

### Conclusion

Avec l’expérience acquise dans ce scénario, lorsque vous envisagez la configuration la plus appropriée pour une plage de dates comptabilisation autorisées pour une entreprise, vous pouvez tenir compte des éléments suivants. Tant que vous autorisez la validation des modifications de la valeur stock au cours d’une période, telle que décembre dans ce cas, la configuration que la société utilise pour les plages de dates comptabilisation autorisées doit être alignée sur cette décision. Lorsque l’option Début période validation dans les paramètres comptabilité est définie sur le 1er décembre, la réévaluation effectuée en décembre peut être transférée vers les écritures sortantes affectées dans la même période.  

Les groupes d’utilisateurs qui ne sont pas autorisés à effectuer des validations en décembre mais en janvier, ce qui était probablement censé être limité par les paramètres comptabilité dans ce scénario, devront plutôt être gérés via les paramètres utilisateur.  

## Scénario de frais annexes  

### Conditions préalables  

Veuillez saisir les valeurs suivantes :

**Paramètres stock** :  

- Compta. coûts automatique = Oui  

- Ajustement automatique des coûts = Toujours  

- Type calcul coût moyen = Article  

- Période coût moyen = Jour  

**Paramètres comptabilité** :  

- Début période validation = 1er décembre 2020.  

- Fin période validation = Vide  

**Paramètres utilisateur** :  

- Début période validation = 1er décembre 2020.  

- Fin période validation = Vide  

### Pour tester le scénario  

Testez ce scénario en effectuant les étapes suivantes :

1.  Créez un frais **Article** avec les valeurs suivantes :  

     - Unité de base = PCS  

     - Mode évaluation stock = Moyen  

     - Sélectionnez des groupes comptabilisation facultatifs.  

2.  Créez une **Commande achat** avec les valeurs suivantes :  

     - Numéro du fournisseur : 10000  

     - Date comptabilisation = 15 décembre 2020

     - N° facture fournisseur : 1234  

     Sur la ligne de commande achat, sélectionnez les valeurs suivantes :  

     - Article = FRAIS  

     - Quantité = 1  

     - Coût unitaire direct = 100  

     Pour terminer l’étape, validez le document comme reçu et facturé.  

3.  Créez une **Commande vente** avec les valeurs suivantes :  

     - N° donneur d’ordre : 10000  

     - Date comptabilisation = 16 décembre 2020  

     Sur la ligne de commande vente :  

     - Article = FRAIS  

     - Quantité = 1  

     - Prix unitaire = 135  

     Pour terminer l’étape, validez le document comme reçu et facturé.  

4.  Entrez des valeurs pour la page **Paramètres comptabilité** :  

     - Début période validation = 1er janvier 2021  

    -  Fin période validation = Vide  

5.  Créez une **Commande achat** avec les valeurs suivantes :  

     - Numéro du fournisseur : 10000  

     - Date de comptabilisation = 2 janvier 2021  

     - N° facture fournisseur : 2345  

     Sur la ligne de commande achat :  

     - Frais annexes = JB-FREIGHT  

     - Quantité = 1  

     - Coût unitaire direct = 3  

     - Affectez les frais annexes à la réception achat à l’étape 2.  

     Pour terminer l’étape, validez le document comme reçu et facturé.  


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

6.  À la date du 3 janvier arrive une facture achat, contenant des frais annexes supplémentaires pour l’achat effectué à l’étape 2. La date de document de cette facture est le 30 décembre, elle est donc validée avec la date comptabilisation du 30 décembre 2020.  

     Créez une **Commande achat** avec les valeurs suivantes :  

     - Numéro du fournisseur : 10000  

     - Date comptabilisation = 30 décembre 2020  

     - N° facture fournisseur : 3456  

     Sur la ligne de commande achat, sélectionnez les valeurs suivantes :  

     - Frais annexes = JB-FREIGHT  

     - Quantité = 1  

     - Coût unitaire direct = 2  

     Affectez les frais annexes à la réception achat de l’étape 2.  

     Pour terminer l’étape, validez le document comme reçu et facturé.  


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

Le scénario décrit se termine avec un état Évaluation du stock indiquant Quantité = 0 alors que la valeur = 2. Les frais annexes validés à l’étape 6 font partie de la valeur d’entrée de stock de décembre alors que la valeur Sortie de stock pour la même période n’est pas affectée.  

Définir l’option Début période validation au 1er janvier dans les paramètres comptabilité était recommandé pour les premiers frais annexes. Les coûts de l’entrée et de la sortie de stock ont été enregistrés dans la même période. Cependant, pour les deuxièmes frais annexes, le changement de COGS est reconnu dans la période suivante.  

**Conclusion :**  

Il est difficile d’obtenir un état Évaluation du stock indiquant Quantité = 0 alors que la valeur <> 0. Dans ce cas, il est également plus difficile d’exprimer des paramètres optimaux, étant donné que les factures achat arrivent le même jour mais couvrent différentes périodes ou même différents exercices comptables. Le passage à un nouvel exercice comptable nécessite généralement une planification et, à cet effet, il est bon d’envisager le processus Ajuster coûts – Écr. article qui reconnaît COGS.  

Dans ce scénario, une solution aurait pu être que le champ Début période validation dans les paramètres comptabilité indique une date en décembre pour quelques jours de plus et que la validation des premiers frais annexes soit reportée pour que tous les coûts de la période ou de l’exercice précédent soient reconnus pour la période à laquelle ils appartiennent. Ainsi, le traitement par lots Ajuster coûts – Écr. article serait exécuté et la date comptabilisation autorisée serait déplacée vers la nouvelle période\/le nouvel exercice. Les premiers frais annexes avec la date comptabilisation du 2 janvier peuvent ensuite être validés.  

## Voir aussi  

[Détails de conception : date comptabilisation de l’écriture valeur d’ajustement](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
