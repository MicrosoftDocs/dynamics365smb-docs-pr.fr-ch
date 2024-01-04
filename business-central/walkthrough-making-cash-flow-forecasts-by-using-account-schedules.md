---
title: Faire des prévisions de trésorerie à l’aide d’états financiers
description: "Cette procédure pas-à-pas décrit le mode d’utilisation d’états financiers pour élaborer des prévisions de trésorerie dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: bholtorf
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Procédure pas-à-pas : créer des prévisions de trésorerie à l’aide d’états financiers

Cette procédure pas-à-pas décrit le mode d’utilisation d’états financiers pour élaborer des prévisions de trésorerie. Les états financiers procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie. Dans les états financiers, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie. Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas

Cette procédure pas à pas décrit les tâches suivantes :  

- Configuration d’un nouveau nom de l’état financier de trésorerie.  
- Mise en place des lignes d’état financier.  
- Configuration d’une nouvelle définition de colonne.  
- Affectation d’une définition de colonne à un état financier.  
- Affichage et impression des prévisions de trésorerie.  

### <a name="prerequisites"></a>Conditions préalables

Pour exécuter ce processus pas à pas, vous devez :  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Une feuille d’activité de trésorerie avec lignes enregistrées  

## <a name="roles"></a>Rôles

Cette procédure pas à pas présente les tâches effectuées par le rôle utilisateur suivant :  

- Contrôleur  

## <a name="story"></a>Scénario

Ken est un contrôleur chez CRONUS, chargé d’élaborer des prévisions mensuelles de trésorerie. Ken inclut les finances, les ventes, les achats et les immobilisations dans les prévisions, et les présente à CFO Sara dans un souci de visibilité commerciale.  

## <a name="setting-up-a-new-financial-report-name"></a>Configuration d’un nouveau nom de l’état financier

Le nom de l’état financier est le nom que vous donnez à la prévision de flux de trésorerie qui comprend une série de lignes définies et une définition de colonne.  

### <a name="set-up-a-new-financial-report-name"></a>Configurer un nouveau nom de l’état financier

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **États financiers**, puis choisissez le lien associé.  
2. Sur la page **États financiers**, choisissez **Nouveau** pour créer un nom d’état financier de flux de trésorerie.  
3. Dans le champ **Nom**, entrez **Prévision**.  
4. Dans le champ **Description**, entrez **Prévision de trésorerie**.  
5. Laissez les champs **Définition de ligne** et **Définition de colonne** vides.

## <a name="setting-up-row-definition-lines"></a>Configuration des lignes de définition de ligne

Une fois le nom de l’état financier défini, Ken définit chaque ligne de l’état financier sur les flux de trésorerie. Ken définit les lignes qui peuvent être affichées dans les états en plus des lignes destinées uniquement au calcul.  

### <a name="set-up-row-definition-lines"></a>Configuration des lignes de définition de ligne

1. Sur la page **États financiers**, sélectionnez le nouvel état financier **Prévision** que vous avez créé, puis choisissez l’action **Modifier la définition de ligne**.  
2. Sur la page **Définition de ligne**, entrez chaque ligne comme indiqué dans le tableau suivant.  

    > [!TIP]  
    > Utilisez la fonction **Insérer des comptes CF**,vous pouvez sélectionner rapidement les comptes de trésorerie à partir du plan comptable de trésorerie et les copier vers les lignes de définition de ligne.  

    | N° ligne | Désignation              | Type totalisation            | Totalisation | Type ligne   | Type de montant | Afficher |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Clients              | Comptes d’écritures de trésorerie | 10       |Solde période | Montant net  | Oui  |
    | R10     | Commandes vente en cours        | Comptes d’écritures de trésorerie | 20       |Solde période | Montant net  | Oui  |
    | R10     | Location                  | Comptes d’écritures de trésorerie | 30       |Solde période | Montant net  | Oui  |
    | R10     | Actifs financiers         | Comptes d’écritures de trésorerie | 40       |Solde période | Montant net  | Oui  |
    | R10     | Cession d’immobilisations    | Comptes d’écritures de trésorerie | 50       |Solde période | Montant net  | Oui  |
    | R10     | Investissements privés      | Comptes d’écritures de trésorerie | 60       |Solde période | Montant net  | Oui  |
    | R10     | Réceptions diverses   | Comptes d’écritures de trésorerie | 70       |Solde période | Montant net  | Oui  |
    | R10     | Commandes service en cours      | Comptes d’écritures de trésorerie | 80       |Solde période | Montant net  | Oui  |
    | R20     | Total règlements      | Formule                  | R10      |Solde période | Montant net  | Oui  |
    | R30     | Fournisseurs                 | Comptes d’écritures de trésorerie | 1010     |Solde période | Montant net  | Oui  |
    | R30     | Commandes achat en cours     | Comptes d’écritures de trésorerie | 1020     |Solde période | Montant net  | Oui  |
    | R30     | Charges de personnel          | Comptes d’écritures de trésorerie | 1030     |Solde période | Montant net  | Oui  |
    | R30     | Charges d’exploitation            | Comptes d’écritures de trésorerie | 1040     |Solde période | Montant net  | Oui  |
    | R30     | Coûts financiers            | Comptes d’écritures de trésorerie | 1050     |Solde période | Montant net  | Oui  |
    | R30     | Investissements              | Comptes d’écritures de trésorerie | 1070     |Solde période | Montant net  | Oui  |
    | R30     | Consommations privées     | Comptes d’écritures de trésorerie | 1090     |Solde période | Montant net  | Oui  |
    | R30     | TVA due                  | Comptes d’écritures de trésorerie | 1100     |Solde période | Montant net  | Oui  |
    | R30     | Autres dépenses           | Comptes d’écritures de trésorerie | 1110     |Solde période | Montant net  | Oui  |
    | R40     | Total décaissements | Formule                  | R30      |Solde période | Montant net  | Oui  |
    | R50     | Excédent                  | Formule                  | R20+R40  |Solde période | Montant net  | Oui  |
    | R60     | Fonds de trésorerie          | Comptes d’écritures de trésorerie | 2100     |Solde période | Montant net  | Oui  |
    | R70     | Total trésorerie          | Formule                  | R50+R60  |Solde période | Montant net  | Oui  |

    > [!NOTE]
    > Le numéro de ligne R10 est utilisé pour capturer les totaux du compte client. Le numéro de ligne R20 est utilisé pour calculer la somme de tous les règlements. Le numéro de ligne R30 est utilisé pour capturer les totaux du compte fournisseur. Le numéro de ligne R40 est utilisé pour calculer la somme de tous les décaissements. Le numéro de ligne R50 est utilisé pour calculer la somme des excédents. Le numéro de ligne R60 est utilisé pour capturer les fonds liquides. Le numéro de ligne R70 est utilisé pour calculer la trésorerie prévue.

## <a name="setting-up-a-new-column-definition"></a>Configuration d’une nouvelle définition de colonne

Avant de pouvoir imprimer les prévisions de trésorerie, Ken doit créer la définition de colonne pour les informations numériques. Dans les colonnes, Ken définit les informations qu’il souhaite utiliser dans les lignes.

- La première colonne porte le numéro *C10* avec l’intitulé **Montant** et indique le solde de la période.  
- La deuxième colonne porte le numéro *C20* avec l’intitulé **Solde au** et indique les transactions de la période.  
- La troisième colonne porte le numéro *C30* avec l’intitulé **Exercice comptable** et indique le solde de la période dans les soldes pour l’exercice comptable.  
- Pour finir, Ken définit la définition de colonne par défaut pour l’état financier **Prévision**.  

### <a name="set-up-a-new-column-definition"></a>Configurer une nouvelle définition de colonne

1. Sur la page **États financiers**, sélectionnez le nom du nouvel état financier **Prévision** que vous venez de créer. Sous l’onglet **Accueil**, dans le groupe **Processus**, choisissez **Modifier la définition de colonne**.

2. Créez une définition de colonne que vous nommez **Trésorerie**.

3. Cliquez sur le bouton **OK**.

4. Saisissez chaque ligne comme indiqué dans le tableau suivant.

    |N° colonne|En-tête colonne|Type colonne|Type écriture comptable|Type montant|Afficher|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Montant|Solde période|Écritures|Montant net|Toujours|  
    |C20|Montant jusque date|Solde au|Écritures|Montant net|Toujours|  
    |C30|Exercice comptable complet|Exercice comptable complet|Écritures|Montant net|Toujours|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a>Affectation d’une définition de colonne à un nom d’état financier

Ken est désormais prêt à affecter la définition de colonne au nom d’état financier.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a>Affecter une définition de colonne à un nom d’état financier

1. Sur la page **États financiers**, sélectionnez le nouvel état financier **Prévision** que vous avez créé, puis choisissez l’action **Modifier la définition de colonne**.  
2. Dans le champ **Nom présentation colonne**, sélectionnez la définition de colonne **Trésorerie** pour la définir par défaut.  

## <a name="view-and-print-the-cash-flow-forecast"></a>Afficher et imprimer les prévisions de trésorerie

1. Sur la page **États financiers**, choisissez l’état financier **Prévision** pour visualiser la prévision de trésorerie.  
2. Sur la page **État financier**, vous pouvez sélectionner un montant, puis afficher les écritures de prévisions de trésorerie qui constituent ce montant. En outre, vous pouvez afficher la formule qui est utilisée pour calculer le montant. Vous pouvez également filtrer les montants par date et par axe analytique.  
3. Choisissez l’action **Imprimer** pour imprimer les prévisions de trésorerie.  

## <a name="see-also"></a>Voir aussi

[Utilisation des états financiers](bi-how-work-account-schedule.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
