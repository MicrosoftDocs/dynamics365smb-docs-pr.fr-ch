---
title: "Message d’erreur\_: «\_La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées\_»"
description: "Résolvez l’erreur sou-jacente au message «\_La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées\_» lorsque vous exécutez le traitement par lots Ajuster coûts\_: Écr. article."
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Message d’erreur : « La date comptabilisation n’est pas incluse dans la plage de dates comptabilisation autorisées... »

Lors de l’utilisation du traitement par lots **Ajuster coûts : Écr. article**, vous pouvez rencontrer le message d’erreur suivant :

**La date de comptabilisation n’est pas dans votre plage de dates de comptabilisation autorisées**

Ce message d’erreur indique que l’utilisateur n’est pas autorisé à valider des écritures pour la date en question, et cela peut être résolu en modifiant les paramètres utilisateur.

## <a name="change-the-user-setup"></a><a name="change-the-user-setup"></a><a name="change-the-user-setup"></a>Modifier les paramètres utilisateur

|ID utilisateur  |Début période validation  | Fin période validation  |
|---------|---------|--------|
|EUROPE  |  2020/09/11      |2020/09/30      |

L’utilisateur dans ce cas a une plage de dates comptabilisation autorisées allant du 11 au 30 septembre et n’est donc pas autorisé à valider l’écriture valeur d’ajustement avec la date comptabilisation du 10 septembre.  

### <a name="overview-of-involved-posting-date-setup"></a><a name="overview-of-involved-posting-date-setup"></a><a name="overview-of-involved-posting-date-setup"></a>Aperçu de la configuration de la date comptabilisation impliquée

#### <a name="inventory-periods"></a><a name="inventory-periods"></a><a name="inventory-periods"></a>Périodes inventaire

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

#### <a name="general-ledger-setup"></a><a name="general-ledger-setup"></a><a name="general-ledger-setup"></a>Paramètres comptabilité

|Champ|Valeur|
|---------|---------|
|Début période validation :  |  2020/09/10      |
|Fin période validation :    |  2020/09/30      |
|Registre temps :       |         |
|Format adresse local :|   Code postal      |  

#### <a name="user-setup"></a><a name="user-setup"></a><a name="user-setup"></a>Paramètres utilisateur

|ID utilisateur  |Début période validation  | Fin période validation  |
|---------|---------|--------|
|USERNAME |  2020/09/10      |2020/09/30      |

En attribuant à l’utilisateur une plage de dates comptabilisation autorisée plus large que dans la période inventaire ou les paramètres comptabilité, il devient possible d’éviter le conflit à l’origine du message d’erreur. L’écriture valeur d’ajustement avec la date comptabilisation du 10 septembre sera publiée avec succès avec cette configuration.
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Détails de conception : date comptabilisation de l’écriture valeur d’ajustement](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
