---
title: "Rappeler ou pénaliser les clients pour les impayés| Microsoft Docs"
description: "Décrit comment envoyer une relance à un client sur un paiement dû et ajouter des frais, ou des commissions au paiement en raison de retard."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 310cad43853f347ac7ab74e186edd82e7c54727e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="collect-outstanding-balances"></a>Collecte des soldes restants
La gestion des clients comprend le contrôle du règlement des montants à temps. Si des clients ont des paiements dus, vous pouvez commencer par envoyer l'état du Relevé client comme relance. Sinon, vous pouvez émettre de relances.

Vous pouvez utiliser des relances pour rappeler aux clients les soldes échus. Vous pouvez également utiliser les relances pour calculer les intérêts de retard tels que les intérêts ou les frais et les inclure dans la relance. Utilisez les factures d'intérêts pour débiter des clients d'intérêts ou de frais sans leur rappeler les montants échus.  

## <a name="reminders"></a>Relances
Avant de pouvoir créer des relances, vous devez configurer des conditions relance et les affecter à vos clients. Chaque code condition relance prédéfinit des niveaux de relance. Chaque niveau de relance inclut des règles relatives à l'émission de la relance, par exemple, le nombre de jours après l'échéance de la facture ou la date de la relance précédente après lequel elle doit être émise. Le contenu de la fenêtre **Conditions intérêts de retard** détermine si les intérêts sont calculés dans la relance.  

Vous pouvez exécuter périodiquement le traitement par lots **Création de relances** afin de créer des relances pour tous les clients ayant des soldes échus. Vous pouvez également créer manuellement une relance pour un client spécifique et demander à ce que les lignes soient calculées et renseignées automatiquement.  

Une fois que vous avez créé les relances, vous pouvez les modifier. Le texte apparaissant au début et à la fin de chaque relance est déterminé par les conditions niveau de relance de la colonne **Désignation**. Si un montant calculé a été inséré automatiquement dans le texte de début ou de fin, ce texte ne sera pas ajusté si vous supprimez des lignes. Vous devez alors utiliser la fonction **Mettre à jour texte relance**.  

Une écriture comptable client pour laquelle le champ **En attente** est renseigné ne génèrera pas la création d'une relance. Néanmoins, si une relance est créée à partir d'une autre écriture, une écriture échue en attente d'approbation est incluse dans la relance. Les intérêts ne sont pas calculés sur les lignes avec ces écritures.

Après avoir créé les relances et effectué toutes les modifications souhaitées, vous pouvez lancer les impressions test ou émettre les relances, en général par e-mail.

## <a name="finance-charges"></a>Frais financiers
Lorsqu'un client n'effectue pas son paiement à la date d'échéance, des intérêts de retard peuvent être calculés automatiquement et ajoutés aux montants échus sur le compte du client. Vous pouvez informer le client des frais ajoutés en lui envoyant une facture d'intérêts.  

> [!NOTE]  
> Les factures d'intérêts permettent de calculer les intérêts et les intérêts de retard et d'en informer vos clients sans leur rappeler les paiements échus. Vous pouvez également calculer les intérêts sur les paiements échus lorsque vous créez des relances.  

Vous pouvez créer manuellement une facture d'intérêts pour un client particulier et renseigner les lignes automatiquement. Vous pouvez également utiliser la tâche de fonction **Créer factures d'intérêts** pour créer des factures d'intérêts pour tous les clients ayant des soldes échus ou pour une sélection de clients ayant des soldes échus.  

Une fois que vous avez créé les factures d'intérêts, vous pouvez les modifier. Le texte apparaissant au début et à la fin de chaque facture d'intérêts est déterminé par les conditions intérêts de retard de la colonne **Désignation** de chaque ligne. Si un montant calculé a été inséré automatiquement dans le texte de début ou de fin, ce texte ne sera pas ajusté si vous supprimez des lignes. Vous devez alors utiliser la fonction **Mise à jour du texte des intérêts de retard**.  

Une fois que vous avez créé des factures d'intérêts et effectué toutes les modifications requises, vous pouvez effectuer des impressions test ou émettre des factures d'intérêts; en général par e-mail.  

## <a name="to-send-the-customer-statement-report"></a>Pour envoyer l’état du relevé client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relevé client**, puis sélectionnez le lien connexe.
2. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans **Options sortie**, sélectionnez la manière dont l'état est envoyé au client.

> [!NOTE]  
>   Si vous utilisez plusieurs devises, l'état Relevé client est toujours imprimé dans la devise du client. La dernière date dans une période de déclaration est également utilisée comme date de relevé et cumul date, si le cumul est inclus.

## <a name="to-set-up-reminder-terms"></a>Pour configurer des conditions de relance
Si des clients ont des impayés, vous devez décider quand et comment leur envoyer une relance. En outre, vous pouvez être amené à débiter leurs comptes d'intérêts ou de frais. Vous pouvez configurer autant de conditions relance que vous le souhaitez. Vous pouvez définir un nombre illimité de niveaux de relance pour chaque code de condition de relance.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Conditions de relance**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins.  
3. Pour utiliser plusieurs combinaisons de conditions de relance, créez un code pour chacun d'eux.

## <a name="to-set-up-reminder-levels"></a>Pour configurer des niveaux de relance
La première fois qu'une relance est créée pour un client, le paramétrage utilisé est celui du niveau 1. Lorsque la relance est émise, le numéro du niveau est enregistré dans les écritures relance qui sont créées et associées à l'écriture comptable client spécifique. S'il est nécessaire de relancer le client, toutes les écritures comptables relance associées aux écritures comptables client ouvertes sont vérifiées afin de localiser le numéro de niveau le plus élevé. Les conditions du niveau suivant seront alors utilisées pour la nouvelle relance.

Si vous créez plus de relances qu'il n'y a de niveaux relance, les conditions utilisées seront celles du niveau le plus élevé. Vous pouvez utiliser autant de relances que le champ **Nombre max. de relances** des conditions relance le permet.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Conditions de relance**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Conditions de relance**, cliquez sur la ligne comportant les conditions pour lesquelles configurer des niveaux, puis cliquez sur l'action **Niveaux**.  
3. Renseignez les champs selon vos besoins.  

    Pour chaque niveau de relance, vous pouvez spécifier des conditions particulières, qui peuvent inclure des frais supplémentaires en devise société (DS) et en devise étrangère. Vous pouvez définir plusieurs frais supplémentaires en devise étrangère pour chaque code de la fenêtre **Niveaux relance**.
4. Sélectionnez l'action **Devises**.
5. Dans la fenêtre **Devises niveau relance**, définissez un code de niveau pour chaque relance et le numéro du niveau de rappel correspondant, une devise et des frais supplémentaires.

    > [!NOTE]  
    > Lorsque vous créez une relance en devise, les conditions devise définies ici permettront de créer des relances. Si aucune condition devise n'a été définie, les conditions devise société définies dans la fenêtre **Niveaux relance** seront utilisées et converties dans la devise appropriée.

    Pour chaque niveau relance, vous pouvez indiquer le texte à imprimer avant (**Texte début**) ou après (**Texte fin**) les écritures de la relance.

6. Choisissez les actions **Texte de début** ou **Texte de fin** respectivement, puis renseignez la fenêtre **Texte relance**.
7. Pour insérer automatiquement des valeurs correspondantes dans le texte de relance résultant, entrez les espaces réservés suivants dans le champ **Texte**.  

|Paramètre substituable|Valeur|  
|-----------------|-----------|  
|%1|Contenu du champ **Date du document** de l'en\-tête de relance|  
|%2|Contenu du champ **Date d'échéance** de l'en\-tête de relance|  
|%3|Contenu du champ **Taux d'intérêt** dans les conditions d'intérêts de retard associées|  
|%4|Contenu du champ **Montant ouvert** de l'en\-tête de relance|  
|%5|Contenu du champ **Montant intérêts** de l'en\-tête de relance|  
|%6|Contenu du champ **Frais supplémentaires** de l'en\-tête de relance|  
|%7|Montant total de la relance|  
|%8|Contenu du champ **Niveau relance** de l'en\-tête de relance|  
|%9|Contenu du champ **Code devise** de l'en\-tête de relance|  
|%10|Contenu du champ **Date de validation** de l'en\-tête de relance|  
|%11|Nom de la société|  
|%12|Contenu du champ **Frais supplémentaires par ligne** de l'en\-tête de relance|  

Par exemple, si vous saisissez **Vous devez %9 %7 dus au %2.**, la relance résultante contiendra le texte suivant : **Vous devez 1 200,50 DS dus au 02022014**.

Si vous avez configuré les conditions relance (avec des niveaux et du texte supplémentaires), saisissez l'un des codes sur chaque fiche client. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Pour créer automatiquement une relance
Une relance est identique à une facture. Lorsque vous créez une relance, un en-tête relance, ainsi qu'une ou plusieurs lignes relance, doivent être renseignés. Vous pouvez utiliser une fonction pour créer des relances pour tous les clients automatiquement.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relances**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Relance**, cliquez sur l'action **Créer relance**.
3. Dans la fenêtre **Créer relances**, renseignez les champs pour définir comment et pour qui les relances sont créées.
4. Cliquez sur le bouton **OK**.

## <a name="to-create-a-reminder-manually"></a>Pour créer une relance manuellement
Dans la fenêtre **Relance**, vous pouvez renseigner le raccourci **Général** manuellement et ensuite renseigner les lignes automatiquement.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relances**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire.
4. Choisissez l'action **Proposer lignes relance**.
5. Dans le traitement par lots **Proposer lignes relance**, renseignez les champs pour définir comment et pour qui les relances sont créées.
6. Activez la case à cocher **Inclure les écritures en attente** si vous souhaitez que les relances contiennent des écritures ouvertes impayées qui sont en attente.

    > [!Important]
    > Les écritures ouvertes en attente sont insérées, indépendamment du paramètre de la case à cocher Seulement écritures dont l'échéance est dépassée.

7. Cliquez sur le bouton **OK**.

## <a name="to-replace-reminder-texts"></a>Pour remplacer les textes relance  
Vous pouvez déterminer de plusieurs manières le texte devant figurer sur la relance imprimée. Dans certains cas, vous pouvez remplacer les textes début et fin définis pour le niveau actuel par ceux d'un autre niveau.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relances**, puis sélectionnez le lien connexe.
2. Ouvrez la relance appropriée, puis cliquez sur l'action **Mettre à jour texte relance**.
3. Dans la fenêtre **Mettre à jour texte relance**, entrez le niveau requis dans le champ **Niveau relance**.
3. Cliquez sur le bouton **OK** pour que le programme mette à jour les textes début et fin.

## <a name="to-issue-a-reminder"></a>Pour émettre une relance
Après avoir créé les relances et effectué toutes les modifications souhaitées, vous pouvez lancer les impressions test ou émettre les relances.

Lorsque vous émettez une relance, les données sont transférées dans une fenêtre séparée pour les relances émises. Les écritures relance sont simultanément validées. Si des intérêts ou des frais supplémentaires ont été calculés, les écritures sont validées dans les écritures client et dans la comptabilité.

Lorsqu'une relance est émise, les écritures sont validées selon les spécifications de la fenêtre **Conditions de relance**. Cette spécification détermine si les intérêts et les frais supplémentaires sont validés sur le compte client et dans la comptabilité. La configuration dans la fenêtre **Groupes compta. client** détermine les comptes qui seront utilisés.

Pour chaque écriture comptable client de la facture d'intérêts, une écriture est créée dans la fenêtre **Ecr. relance/fact. intérêts**.

Si les cases à cocher **Comptabiliser intérêts** ou le champ **Compta. frais supplémentaires** de la table **Conditions de relance** sont activées, les écritures suivantes sont aussi créées :

- Une écriture dans la fenêtre **Écritures comptables client**,
- Une écriture client sur le compte général approprié,
- Une écriture intérêts et/ou une écriture frais supplémentaires sur le compte général approprié.

De plus, émettre une facture d'intérêts peut créer des écritures de TVA.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relances**, puis sélectionnez le lien connexe.
2. Sélectionnez la relance concernée, puis cliquez sur l'action **Émission**.
3. Dans la fenêtre **Emettre relances**, renseignez les champs selon vos besoins.
4. Cliquez sur le bouton **OK**.

La relance est imprimée pour être envoyé à un e-mail spécifié en tant que document joint PDF.

## <a name="to-set-up-finance-charge-terms"></a>Pour configurer des conditions intérêts de retard
Vous devez créer un code qui représente un calcul d'intérêts de retard. Vous pouvez ensuite entrer ce code dans le champ **Code condition intérêts** des fiches client ou fournisseur.

Les intérêts de retard peuvent être calculés en utilisant la méthode du solde journalier moyen ou celle du solde échu.

Avec la méthode du solde échu, les intérêts représentent simplement un pourcentage du montant échu :  

    Balance Due method - Finance Charge = Overdue Amount x (Interest Rate / 100)

Avec la méthode du solde journalier moyen, le nombre de jours de retard de paiement est pris en compte :  

    Average Daily Balance method - Finance Charge = Overdue Amount x (Days Overdue / Interest Period) x (Interest Rate/100)

En outre, chaque code de la table Conditions intérêts de retard est lié à une autre table, la table Texte intérêts de retard. Pour chaque ensemble de conditions, vous pouvez définir un texte début et un texte fin à inclure dans la facture d'intérêts.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Conditions intérêts de retard**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins.  
3. Pour utiliser plusieurs combinaisons de conditions intérêts de retard, créez un code pour chacun d'eux.

    Pour chaque condition intérêts de retard, vous pouvez spécifier des conditions particulières, qui peuvent inclure des frais supplémentaires en devise société (DS) et en devise étrangère. Vous pouvez définir des frais supplémentaires en devise pour chaque code de la fenêtre **Conditions intérêts de retard**.
4. Sélectionnez l'action **Devises**.
5. Dans la fenêtre **Devises condition intérêts**, définissez pour chaque condition un code devise et des frais supplémentaires.

    > [!NOTE]  
    > Lorsque vous créez des intérêts de retard en devise, les conditions intérêts devise définies ici serviront à créer des factures d'intérêts. Si aucune condition intérêts de retard en devise n'est définie, les conditions intérêts de retard en devise société définies dans la table **Conditions intérêts de retard** seront utilisées, puis converties dans la devise souhaitée.

    Pour chaque condition intérêts, vous pouvez spécifier le texte à imprimer avant (**Texte début**) ou après (**Texte fin**) les écritures de la facture d'intérêts.  
6. Choisissez les actions **Texte de début** ou **Texte de fin** respectivement, puis renseignez la fenêtre **Texte intérêts de retard**.
7. Pour insérer automatiquement des valeurs correspondantes dans le texte facture d'intérêts résultant, entrez les espaces réservés suivants dans le champ **Texte**.

|Paramètre substituable|Valeur|  
|-----------------|-----------|  
|%1|Contenu du champ **Date du document** de l'en-tête de facture d'intérêts|  
|%2|Contenu du champ **Date d'échéance** de l'en-tête de facture d'intérêts|  
|%3|Contenu du champ **Taux d'intérêt** dans les conditions d'intérêts de retard associées|  
|%4|Contenu du champ **Montant ouvert** de l'en-tête de facture d'intérêts|  
|%5|Contenu du champ **Montant intérêts** de l'en-tête de facture d'intérêts|  
|%6|Contenu du champ **Frais supplémentaires** de l'en-tête de facture d'intérêts|  
|%7|Montant total de la relance|  
|%8|Contenu du champ **Code devise** de l'en-tête de facture d'intérêts|  
|%9|Contenu du champ **Date comptabilisation** de l'en-tête de facture d'intérêts|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Pour créer manuellement des factures d'intérêts  
Une facture d'intérêts ressemble à une facture. Vous pouvez renseigner un en-tête manuellement et faire renseigner les lignes, ou créer des factures d'intérêts automatiquement pour tous les clients.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures d'intérêts**, puis sélectionnez le lien connexe.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins.  
3. Sélectionnez **Proposer lignes fact. intérêts**.
4. Dans la fenêtre **Proposer lignes facture intérêts**, définissez un filtre sur le raccourci **Écriture comptable client** si vous souhaitez créer des factures d'intérêts uniquement pour des écritures spécifiques.  
5.  Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.  

## <a name="to-update-finance-charge-memo-texts"></a>Pour mettre à jour des textes de factures d'intérêts  
Dans certains cas, vous pouvez modifier les textes début et fin définis pour les conditions intérêts de retard. Si vous le faites au moment où vous avez créé, mais pas encore émis, les factures d'intérêts, vous pouvez mettre à jour ces factures avec le texte modifié.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Facture d'intérêts**, puis sélectionnez le lien connexe.  
2. ouvrez la facture d'intérêts dont vous souhaitez modifier le texte, puis sélectionnez **MAJ texte fact. d'intérêts**.
3. Dans la fenêtre **MAJ texte fact. d'intérêts**, vous pouvez définir un filtre pour mettre à jour plusieurs factures d'intérêts.
4. Cliquez sur le bouton **OK** pour que le programme mette à jour les textes début et fin.  

## <a name="to-issue-finance-charge-memos"></a>Pour émettre des factures d'intérêts
Une fois que vous avez créé des factures d'intérêts et effectué toutes les modifications requises, vous pouvez effectuer des impressions test ou émettre des factures d'intérêts.

Lorsqu'une relance est émise, les écritures sont validées selon les spécifications de la fenêtre **Conditions intérêts de retard**. Cette spécification détermine si les intérêts et les frais supplémentaires sont validés sur le compte client et dans la comptabilité. La configuration dans la fenêtre **Groupes compta. client** détermine les comptes qui seront utilisés.

Pour chaque écriture comptable client de la facture d'intérêts, une écriture est créée dans la fenêtre **Ecr. relance/fact. intérêts**.

Si les cases à cocher **Comptabiliser intérêts** ou le champ **Compta. frais supplémentaires** de la table **Conditions intérêts de retard** sont activées, les écritures suivantes sont aussi créées :

- Une écriture dans la fenêtre **Écritures comptables client**,
- Une écriture client sur le compte général approprié,
- Une écriture intérêts et/ou une écriture frais supplémentaires sur le compte général approprié.

De plus, émettre une facture d'intérêts peut créer des écritures de TVA.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures d'intérêts**, puis sélectionnez le lien connexe.
2. Sélectionnez la facture concernée, puis cliquez sur l'action **Emettre**.
3. Dans la fenêtre **Emettre factures d'intérêts**, renseignez les champs selon vos besoins.
4. Cliquez sur le bouton **OK**.

La factures d'intérêts est imprimée pour être envoyé à un e-mail spécifié en tant que document joint PDF.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Pour afficher les écritures relance et facture d'intérêts  
Lorsque vous émettez une relance, une écriture relance est créée dans la fenêtre **Écr. relance/fact. intérêts** pour chaque ligne relance contenant une écriture comptable client. Vous pouvez ensuite obtenir un aperçu des écritures relance créées pour un client spécifique.    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.  
2. Ouvrez la fiche client appropriée, puis sélectionnez l'action **Écritures comptables**.
3. Dans la fenêtre **Écritures comptables client**, cliquez sur la ligne de l'écriture comptable pour laquelle vous souhaitez visualiser les écritures relance, puis sélectionnez l'action **Écr. relance/fact. intérêts**.

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

