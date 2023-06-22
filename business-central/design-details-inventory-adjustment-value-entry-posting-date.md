---
title: Date comptabilisation des écritures valeur
description: Découvrez comment le traitement par lots Ajuster coûts - Écr. article identifie et affecte une date comptabilisation aux écritures valeur que le traitement par lots est sur le point de créer.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---
# <a name="design-details-posting-date-on-adjustment-value-entry" />Détails de conception : date comptabilisation de l’écriture valeur d’ajustement

Cet article fournit des conseils aux utilisateurs de la fonctionnalité Évaluation stock dans [!INCLUDE[prod_short](includes/prod_short.md)], et en particulier pour la façon dont le traitement par lots **Ajuster coûts : Écr. article** identifie et attribue une date comptabilisation aux écritures de valeur que le traitement par lots est sur le point de créer.

## <a name="how-posting-dates-are-assigned" />Modalités d’attribution des dates comptabilisation

Le traitement par lots **Ajuster coûts - Écr. article** affecte une date comptabilisation à l’écriture valeur qu’il est sur le point de créer dans les étapes suivantes :  

1. Initialement, la date comptabilisation de l’écriture à créer est la même que celle de l’écriture qu’elle ajuste.  

2. La date comptabilisation est validée par rapport aux périodes inventaire et/ou aux paramètres comptabilité.  

3. Affectation d’une date comptabilisation : si la date comptabilisation initiale n’est pas compris dans la plage de dates comptabilisation autorisées, le traitement par lots affecte une date comptabilisation autorisée à partir des paramètres comptabilité ou de la période inventaire. Si les périodes inventaire et les dates comptabilisation autorisées dans les paramètres comptabilité sont définies, la date la plus récente des deux est affectée à l’écriture valeur d’ajustement.  

Examinons ce processus plus en détail. Supposons que nous avons une écriture comptable article de type Vente. L’article a été livré le 5 septembre 2020 et il a été facturé le jour suivant.  

#### <a name="item-ledger-entry" />Écriture comptable article

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture  | N° document |Code magasin  |Quantité  |Coût total (réel)  |Quantité facturée  |Quantité restante  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020/09/05     |  Vente       |102033     |  Bleu       | -1    |    -11     |-1     |    0     |

Vous trouverez ci-dessous les écritures de valeur associées :

- **Écriture n°379** représente l’expédition et utilise la même date comptabilisation que l’écriture comptable article parent.  
- **Écriture n°381** représente la facture.  
- **Écriture n°391** est un ajustement de l’écriture valeur de facturation (Écriture n°381 ci-dessus).  

|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture comptable article  |Type écriture  |N° document  |N° écriture comptable article  |Code magasin  |Quantité écriture comptable article  |Quantité facturée  |Coût total (réel)  |Coût total (prévu)  |Ajustement  |Ecriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020/09/05     |    Vente     | Coût direct   | 102033        |319     | Bleu        | -1       |0         |  0       |     -10   |Non   |0    |Ventes          |
|381     |  A       |    2020/09/06     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |-1        |-10       |    10     | Non  |0      |       Ventes   |
|391     |  A       |    2020/09/10     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |0         |-1        |    0     |Oui   |    181   | AJSTK   |

Pour affecter la date comptabilisation à **Écriture n°391**, les étapes suivantes ont été appliquées :

1. **L’écriture valeur d’ajustement** à créer (**Écriture n°391**) se voit attribuer la même **Date comptabilisation** que l’écriture qu’elle ajuste.

2. Le traitement par lots **Ajuster coûts - Écr. article** détermine si la date comptabilisation initiale de l’écriture valeur d’ajustement est comprise dans la plage de dates comptabilisation autorisées en fonction des périodes inventaire et/ou des paramètres comptabilité.  

Examinons la vente mentionnée ci-dessus en ajoutant le paramétrage des plages de dates comptabilisation autorisées.  
  
#### <a name="inventory-periods" />Périodes inventaire

|Date de fin  |Name  |Fermé  |
|---------|---------|---------|
|2020/01/31     |2020 janvier      |  Oui    |
|2020/02/28     |Février 2020     |  Oui    |
|2020/03/31     |Mars 2020        |  Oui    |
|2020/04/30     |Avril 2020        |  Oui    |
|2020/05/31     |Mai 2020        |  Oui    |
|2020/06/30     |Juin 2020       |  Oui    |
|2020/07/31     |Juillet 2020        |  Oui    |
|2020/08/31     |Août 2020     |  Oui    |
|2020/09/30     |Septembre 2020  |         |
|2020/10/31     |Octobre 2020    |         |
|2020/11/30     |Novembre 2020   |         |
|2020/12/31     |Décembre 2020   |         |

La première date comptabilisation autorisée est le premier jour de la première période ouverte, qui est le 1e septembre 2020.  

#### <a name="general-ledger-setup" />Paramètres comptabilité

|Champ|Valeur  |
|---------|---------|
|Début période validation :  |  2020/09/10      |
|Fin période validation :    |  2020/09/30      |
|Registre temps :       |         |
|Format adresse local :|   Code postal      |  

La première date comptabilisation autorisée est la date indiquée dans le champ **Début période validation** : 10 septembre 2020. Si les périodes inventaire et les dates comptabilisation autorisées dans les **paramètres comptabilité** sont définies, la date la plus récente des deux définit la plage de dates comptabilisation autorisées.  

**Affectation d’une date comptabilisation autorisée**  

La date comptabilisation initiale était le 6 septembre, comme illustré à l’étape 1. Toutefois, dans la deuxième étape, le traitement par lots Ajuster coûts - Écr. article identifie que la date comptabilisation autorisée la plus proche est le 10 septembre et affecte donc le 10 septembre à l’écriture valeur d’ajustement (**Écriture n°391**), ci-dessous.  


|Numéro de la séquence  |Nombre d’articles  |Date comptabilisation  |Type écriture comptable article  |Type écriture  |N° document  |N° écriture comptable article  |Code magasin  |Quantité écriture comptable article  |Quantité facturée  |Coût total (réel)  |Coût total (prévu)  |Ajustement  |Ecriture lettrage  |Code journal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020/09/05     |    Vente     | Coût direct   | 102033        |319     | Bleu        | -1       |0         |  0       |     -10   |Non   |0    |Ventes          |
|381     |  A       |    2020/09/06     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |-1        |-10       |    10     | Non  |0      |       Ventes   |
|391     |  A       |    **2020-09-10**     |    Vente     | Coût direct   | 103022        |319     | Bleu        |  0       |0         |-1        |    0     |Oui   |    181   | AJSTK   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job" />Problèmes courants avec le traitement par lots « Ajuster coûts - Écr. article »

Il existe deux scénarios que l’équipe d’assistance rencontre suffisamment fréquemment pour justifier la rédaction d’articles de résolution de problèmes dédiés.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates" />Message d’erreur : « La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées... »

Si vous rencontrez cette erreur, vous devez ajuster les dates pour lesquelles l’utilisateur est autorisé à valider des écritures. Pour en savoir plus, voir [Message d’erreur : « La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées »](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge" />Comparaison entre la date comptabilisation de l’écriture valeur d’ajustement et la date comptabilisation de l’écriture à l’origine de l’ajustement, comme une réévaluation ou des frais annexes

Pour en savoir plus, voir [Date comptabilisation sur l’écriture valeur d’ajustement par rapport à l’écriture source](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also" />Voir aussi

[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
