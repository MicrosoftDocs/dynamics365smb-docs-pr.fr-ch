---
title: Configurer les conditions intérêts de retard
description: "Découvrez comment configurer Business\_Central afin de pouvoir informer les clients des frais supplémentaires en envoyant des factures d’intérêts."
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: edupont
---
# Configurer les conditions intérêts de retard

Lorsqu’un client n’effectue pas son paiement à la date d’échéance, des intérêts de retard peuvent être calculés automatiquement et ajoutés aux montants échus sur le compte du client. Vous pouvez informer le client des frais ajoutés en lui envoyant une facture d’intérêts. Mais tout d’abord, vous devez créer un code qui représente un calcul d’intérêts de retard. Vous pouvez ensuite entrer ce code dans le champ Code condition intérêts des fiches client.  

## Conditions intérêts de retard

Vous devez configurer des conditions intérêts de retard pour chaque calcul de frais financiers, puis affecter les conditions au client dans le champ **Code condition intérêts** sur la page **Client**.

Les intérêts de retard peuvent être calculés en utilisant les méthodes du solde journalier moyen ou celles du solde échu.

* Solde journalier moyen  
  
  Le nombre de jours pendant lequel le paiement est en retard est pris en compte :  
  *Méthode Solde journalier moyen* - *Frais financiers* = *Montant échu* x *(Jours échus/ Période d’intérêts)* x *(Taux d’intérêt/100)*

* Solde dû  
  
  La facture d’intérêts représente un pourcentage du montant échu :  
  *Méthode du solde échu* - *Frais financiers* = *Montant échu* x *(Taux d’intérêt / 100)*

En outre, chaque condition de la table Conditions intérêts de retard est lié à une autre table, la table Texte intérêts de retard. Pour chaque ensemble de conditions, vous pouvez définir un texte début et un texte fin à inclure dans la facture d’intérêts.

### Pour configurer des conditions intérêts de retard

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Conditions intérêts de retard**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.
3. Pour utiliser plusieurs combinaisons de conditions intérêts de retard, créez un code pour chacun d’eux.

    Pour chaque condition intérêts de retard, vous pouvez spécifier des conditions particulières, qui peuvent inclure des frais supplémentaires en devise société (DS) et en devise étrangère. Vous pouvez définir des frais supplémentaires en devise pour chaque condition sur la page **Conditions intérêts de retard**.
4. Sélectionnez l’action **Devises**.
5. Sur la page **Devises condition intérêts**, définissez pour chaque condition un code devise et des frais supplémentaires.

    > [!NOTE]  
    > Lorsque vous créez des intérêts de retard en devise, les conditions intérêts devise définies ici serviront à créer des factures d’intérêts. Si aucune condition intérêts de retard en devise n’est définie, les conditions intérêts de retard en devise société définies sur la page **Conditions intérêts de retard** seront utilisées, puis converties dans la devise souhaitée.

    Pour chaque condition intérêts, vous pouvez spécifier le texte à imprimer avant (**Texte début**) ou après (**Texte fin**) les écritures de la facture d’intérêts.  
6. Choisissez les actions **Texte de début** ou **Texte de fin** respectivement, puis renseignez la page **Texte intérêts de retard**.
7. Pour insérer automatiquement des valeurs correspondantes dans le texte facture d’intérêts résultant, entrez les espaces réservés suivants dans le champ **Texte**.

|Paramètre substituable|Valeur|  
|-----------------|-----------|  
|%1|Contenu du champ **Date du document** de l’en-tête de facture d’intérêts|  
|%2|Contenu du champ **Date d’échéance** de l’en-tête de facture d’intérêts|  
|%3|Contenu du champ **Taux d’intérêt** dans les conditions d’intérêts de retard associées|  
|%4|Contenu du champ **Montant ouvert** de l’en-tête de facture d’intérêts|  
|%5|Contenu du champ **Montant intérêts** de l’en-tête de facture d’intérêts|  
|%6|Contenu du champ **Frais supplémentaires** de l’en-tête de facture d’intérêts|  
|%7|Montant total de la relance|  
|%8|Contenu du champ **Code devise** de l’en-tête de facture d’intérêts|  
|%9|Contenu du champ **Date comptabilisation** de l’en-tête de facture d’intérêts|  

## Voir la [formation Microsoft](/training/modules/send-memos-dynamics-365-business-central/) associée

## Voir aussi

[Collecte des soldes restants](receivables-collect-outstanding-balances.md)  
[Configurer les conditions et niveaux de relance](finance-setup-reminders.md)  
[Configuration de Finance](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
