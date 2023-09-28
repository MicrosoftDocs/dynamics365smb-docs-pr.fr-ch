---
title: Collecte des soldes restants
description: 'Découvrez comment rappeler à vos clients les impayés. Envoyez un relevé client, émettez un rappel ou envoyez une note de frais financiers.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 02/09/2022
ms.author: bholtorf
---
# Collecte des soldes restants

La gestion des clients comprend le contrôle du règlement des montants à temps. Si des clients ont des paiements dus, vous pouvez commencer par envoyer l’état du **Relevé client** comme relance. Sinon, vous pouvez émettre de relances.

Vous pouvez utiliser des relances pour rappeler aux clients les soldes échus. Vous pouvez également utiliser les relances pour calculer les intérêts de retard tels que les intérêts ou les frais et les inclure dans la relance. Utilisez les factures d’intérêts pour débiter des clients d’intérêts ou de frais sans leur rappeler les montants échus.

## Relevés

À partir de la fiche client, vous pouvez créer un relevé avec les transactions de ce client avec vous. Ensuite, vous envoyez au client le fichier PDF généré. Sinon, utilisez l’état **Relevé client** pour envoyer à vos clients un aperçu de leur activité avec vous. Le relevé client peut être envoyé à Excel pour un traitement ultérieur.  

### Pour envoyer l’état du relevé client

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 10.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Relevé client**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans **Options sortie**, sélectionnez la manière dont l’état est envoyé au client.

> [!NOTE]
> Si vous utilisez plusieurs devises, l’état Relevé client est toujours imprimé dans la devise du client. La dernière date dans une période de déclaration est également utilisée comme date de relevé et cumul date, si le cumul est inclus.

## Relances

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## Frais financiers

Lorsqu’un client n’effectue pas son paiement à la date d’échéance, des intérêts de retard peuvent être calculés automatiquement et ajoutés aux montants échus sur le compte du client. Vous pouvez informer le client des frais ajoutés en lui envoyant une facture d'intérêts.  

> [!NOTE]  
> Les factures d'intérêts permettent de calculer les intérêts et les intérêts de retard et d'en informer vos clients sans leur rappeler les paiements échus. Vous pouvez également calculer les intérêts sur les paiements échus lorsque vous créez des relances.  

Pour pouvoir créer des factures d’intérêts, vous devez configurer des conditions. Pour plus d’informations, voir [Configurer les conditions intérêts de retard](finance-setup-finance-charges.md).  

Vous pouvez créer manuellement une facture d’intérêts pour un client particulier et renseigner les lignes automatiquement. Vous pouvez également utiliser la tâche de fonction **Créer factures d’intérêts** pour créer des factures d’intérêts pour tous les clients ayant des soldes échus ou pour une sélection de clients ayant des soldes échus.  

Une fois que vous avez créé les factures d'intérêts, vous pouvez les modifier. Le texte apparaissant au début et à la fin de chaque facture d'intérêts est déterminé par les conditions intérêts de retard de la colonne **Désignation** de chaque ligne. Si un montant calculé a été inséré automatiquement dans le texte de début ou de fin, ce texte ne sera pas ajusté si vous supprimez des lignes. Vous devez alors utiliser la fonction **Mise à jour du texte des intérêts de retard**.  

Une fois que vous avez créé des factures d’intérêts et effectué toutes les modifications requises, vous pouvez effectuer des impressions test ou émettre des factures d’intérêts; en général par e-mail.

### Pour créer manuellement des factures d’intérêts

Une facture d’intérêts ressemble à une facture. Vous pouvez renseigner un en-tête manuellement et faire renseigner les lignes, ou créer des factures d’intérêts automatiquement pour tous les clients.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures d’intérêts**, puis sélectionnez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins.  
3. Sélectionnez **Proposer lignes fact. intérêts**.
4. Sur la page **Proposer lignes facture intérêts**, définissez un filtre sur le raccourci **Écriture comptable client** si vous souhaitez créer des factures d’intérêts uniquement pour des écritures spécifiques.

    > [!NOTE]
    > Même s’ils sont répertoriés, la sélection des champs **Paiement** et **Avoir** comme filtres de **Type de document** n’a aucun effet, car la fonction **Proposer lignes facture intérêts** ne gère que les montants positifs.
5.  Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.  

### Pour mettre à jour des textes de factures d’intérêts  
Dans certains cas, vous pouvez modifier les textes début et fin définis pour les conditions intérêts de retard. Si vous le faites au moment où vous avez créé, mais pas encore émis, les factures d’intérêts, vous pouvez mettre à jour ces factures avec le texte modifié.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Facture d’intérêts**, puis sélectionnez le lien associé.  
2. ouvrez la facture d’intérêts dont vous souhaitez modifier le texte, puis sélectionnez **MAJ texte fact. d’intérêts**.
3. Sur la page **MAJ texte fact. d’intérêts**, vous pouvez définir un filtre pour mettre à jour plusieurs factures d’intérêts.
4. Cliquez sur le bouton **OK** pour que le programme mette à jour les textes début et fin.  

### Pour émettre des factures d’intérêts
Une fois que vous avez créé des factures d’intérêts et effectué toutes les modifications requises, vous pouvez effectuer des impressions test ou émettre des factures d’intérêts.

Lorsqu’une relance est émise, les écritures sont validées selon les spécifications sur la page **Conditions intérêts de retard**. Cette spécification détermine si les intérêts et les frais supplémentaires sont validés sur le compte client et dans la comptabilité. La configuration sur la page **Groupes compta. client** détermine les comptes qui seront utilisés.

Pour chaque écriture comptable client de la facture d’intérêts, une écriture est créée sur la page **Ecr. relance/fact. intérêts**.

Si les cases à cocher **Comptabiliser intérêts** ou le champ **Compta. frais supplémentaires** de la page **Conditions intérêts de retard** sont activées, les écritures suivantes sont aussi créées :

- Une écriture sur la page **Écritures comptables client**,
- Une écriture client sur le compte général approprié,
- Une écriture intérêts et/ou une écriture frais supplémentaires sur le compte général approprié.

De plus, émettre une facture d’intérêts peut créer des écritures de TVA.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 4.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures d’intérêts**, puis sélectionnez le lien associé.
2. Sélectionnez la facture concernée, puis cliquez sur l’action **Emettre**.
3. Sur la page **Emettre factures d’intérêts**, renseignez les champs selon vos besoins.
4. Cliquez sur le bouton **OK**.

La factures d’intérêts est imprimée pour être envoyé à un e-mail spécifié en tant que document joint PDF.

### Pour annuler une facture d’intérêts émise
Si des factures d’intérêts ont été émises par erreur, vous pouvez les annuler avant leur envoi. Vous pouvez les annuler une par une ou par lots.
1. Sur la page **Factures d’intérêts émises**, sélectionnez une ou plusieurs lignes pour les factures d’intérêts émises que vous souhaitez annuler, puis choisissez l’action **Annuler**.
2. Sur la page **Annuler les factures d’intérêts émises**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.

### Pour afficher les écritures relance et facture d’intérêts  
Lorsque vous émettez une relance, une écriture relance est créée sur la page **Écr. relance/fact. intérêts** pour chaque ligne relance contenant une écriture comptable client. Vous pouvez ensuite obtenir un aperçu des écritures relance créées pour un client spécifique.    
1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 5.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis choisissez le lien associé.  
2. Ouvrez la fiche client appropriée, puis sélectionnez l’action **Écritures comptables**.
3. Sur la page **Écritures comptables client**, cliquez sur la ligne de l’écriture comptable pour laquelle vous souhaitez visualiser les écritures relance, puis sélectionnez l’action **Écr. relance/fact. intérêts**.

## Taux d’intérêt multiples

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Pour plus d’informations, reportez vous à [Paramétrer plusieurs taux d’intérêt](finance-how-to-set-up-multiple-interest-rates.md).  

## Voir aussi

[Configuration des conditions et niveaux](finance-setup-reminders.md)  
[Configuration des conditions des frais financiers](finance-setup-finance-charges.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
