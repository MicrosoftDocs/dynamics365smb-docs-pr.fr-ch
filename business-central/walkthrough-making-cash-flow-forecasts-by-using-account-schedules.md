---
title: Procédure pas-à-pas – Créer des prévisions de trésorerie à l’aide de tableaux d’analyse
description: Découvrez comment utiliser des tableaux d’analyse pour élaborer des prévisions de trésorerie.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48a176c4c363c4a33ae336d754be71c9f7dd0aeb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772119"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Procédure pas-à-pas : créer des prévisions de trésorerie à l’aide de tableaux d’analyse

Cette procédure pas-à-pas décrit le mode d’utilisation des tableaux d’analyse pour élaborer des prévisions de trésorerie. Les tableaux d’analyse procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie. Dans les tableaux d’analyse, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie. Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas

Cette procédure pas à pas décrit les tâches suivantes :  

- Configuration d’un nouveau nom du tableau d’analyse de trésorerie.  
- Configuration de lignes du tableau d’analyse  
- Configuration d’une nouvelle présentation de colonne  
- Affectation d’une présentation de colonne à un tableau d’analyse.  
- Affichage et impression des prévisions de trésorerie.  

### <a name="prerequisites"></a>Conditions préalables

Pour exécuter ce processus pas à pas, vous devez :  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Les lignes de la feuille d’activité de trésorerie sont enregistrées  

## <a name="roles"></a>Rôles

Cette procédure pas à pas présente les tâches effectuées par le rôle utilisateur suivant :  

- Contrôleur  

## <a name="story"></a>Scénario

Ken est un contrôleur chez CRONUS, chargé d’élaborer des prévisions mensuelles de trésorerie. Il inclut les finances, les ventes, les achats et les immobilisations dans les prévisions, puis les présente à CFO Sara dans un souci de visibilité commerciale.  

## <a name="setting-up-a-new-account-schedule-name"></a>Configuration d’un nouveau nom du tableau d’analyse

Un tableau d’analyse est composé d’un nom de tableau d’analyse de trésorerie avec une série de lignes et une présentation de colonne.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Pour configurer un nouveau nom de tableau d’analyse  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Tableaux d’analyse**, puis sélectionnez le lien associé.  
2. Sur la page **Noms tableaux d’analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d’analyse de trésorerie.  
3. Dans le champ **Nom**, entrez **Prévision**.  
4. Dans le champ **Description**, entrez **Prévision de trésorerie**.  
5. Laissez vierges les champs **Présentation colonne par déf.** et **Nom vue d’analyse** .  

## <a name="setting-up-account-schedule-lines"></a>Configuration de lignes du tableau d’analyse

Après la configuration d’un nom de tableau d’analyse, Ken définit chaque ligne qui s’y affiche. Ken définit les lignes qui peuvent être affichées dans les états en plus des lignes destinées uniquement au calcul.  

### <a name="to-set-up-account-schedule-lines"></a>Pour configurer les lignes du tableau d’analyse  

1. Sur la page **Noms tableaux d’analyse**, sélectionnez le nouveau nom de tableau d’analyse **Prévoir** que vous avez créé, puis choisissez l’action **Modifier tableau d’analyse**.  
2. Sur la page **Tableau d’analyse**, entrez chaque ligne comme indiqué dans le tableau suivant.  

    > [!TIP]  
    >  À l’aide de la fonction **Insérer des comptes CF**,vous pouvez sélectionner rapidement les comptes de trésorerie à partir du plan comptable de trésorerie et les copier vers les lignes du tableau d’analyse.  

    | N° ligne totalisation | Description              | Type totalisation            | Totalisation | Type ligne   | Type montant | Afficher |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Commandes vente en cours        | Comptes d’écritures de trésorerie | 20       |Solde période | Montant net  | Oui  |
    | R10     | Location                  | Comptes d’écritures de trésorerie | 30       |Solde période | Montant net  | Oui  |
    | R10     | Actifs financiers         | Comptes d’écritures de trésorerie | 40       |Solde période | Montant net  | Oui  |
    | R10     | Cession d’immobilisations    | Comptes d’écritures de trésorerie | 50       |Solde période | Montant net  | Oui  |
    | R10     | Investissements privés      | Comptes d’écritures de trésorerie | 60       |Solde période | Montant net  | Oui  |
    | R10     | Réceptions diverses   | Comptes d’écritures de trésorerie | 70       |Solde période | Montant net  | Oui  |
    | R10     | Commandes service en cours      | Comptes d’écritures de trésorerie | 80       |Solde période | Montant net  | Oui  |
    | R20     | Total règlements      | Formule                  | R10      |Solde période | Montant net  | Oui  |
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
    | R50     | Surplus                  | Formule                  | R20+R40  |Solde période | Montant net  | Oui  |
    | R60     | Fonds de trésorerie          | Comptes d’écritures de trésorerie | 2100     |Solde période | Montant net  | Oui  |
    | R70     | Total trésorerie          | Formule                  | R50+R60  |Solde période | Montant net  | Oui  |

    > [!NOTE]
    > Le numéro de ligne R10 est utilisé pour capturer les totaux du compte client. Le numéro de ligne R20 est utilisé pour calculer la somme de tous les règlements. Le numéro de ligne R30 est utilisé pour capturer les totaux du compte fournisseur. Le numéro de ligne R40 est utilisé pour calculer la somme de tous les décaissements. Le numéro de ligne R50 est utilisé pour calculer la somme des excédents. Le numéro de ligne R60 est utilisé pour capturer les fonds liquides. Le numéro de ligne R70 est utilisé pour calculer la trésorerie prévue.

## <a name="setting-up-a-new-column-layout"></a>Configuration d’une nouvelle présentation de colonne

Avant de pouvoir imprimer les prévisions de trésorerie, Ken doit créer la présentation de colonne pour les informations numériques. Dans les colonnes, il définit les informations qu’il souhaite utiliser dans les lignes.

- La première colonne porte le numéro *C10* avec l’intitulé **Montant** et indique le solde de la période.  
- La deuxième colonne porte le numéro *C20* avec l’intitulé **Solde au** et indique les transactions de la période.  
- La troisième colonne porte le numéro *C30* avec l’intitulé **Exercice comptable** et indique le solde de la période dans les soldes pour l’exercice comptable.  
- Pour finir, il définit la présentation de colonne par défaut pour le tableau d’analyse **Prévision**.  

## <a name="to-set-up-a-new-column-layout"></a>Pour configurer une nouvelle présentation de colonne

1. Dans la fenêtre **Noms tableaux d’analyse**, sélectionnez le nouveau nom du tableau d’analyse **Prévision** que vous venez de créer. Sous l’onglet **Accueil**, dans le groupe **Processus**, choisissez **Modifier paramètres présentation colonne**.

    > [!TIP]
    > Vous pouvez trouver la même action sur la page **Tableau d’analyse** si vous êtes toujours en train de modifier le tableau d’analyse **Prévision**.

2. Créez une présentation de colonne que vous nommez **Trésorerie**.

3. Cliquez sur le bouton OK.

4. Saisissez chaque ligne comme indiqué dans le tableau suivant.

    |N° colonne|En-tête colonne|Type colonne|Type écriture comptable|Type montant|Afficher|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Montant|Solde période|Écritures|Montant net|Toujours|  
    |C20|Montant jusque date|Solde au|Écritures|Montant net|Toujours|  
    |C30|Exercice comptable|Exercice comptable|Écritures|Montant net|Toujours|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Affectation de la présentation de colonne au nom de tableau d’analyse

Ken est désormais prêt à affecter la présentation de colonne au nom de tableau d’analyse.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Pour affecter la présentation de colonne au nom de tableau d’analyse  

1. Sur la page **Tableau d’analyse** dans laquelle vous utilisez le tableau d’analyse **Prévision**, choisissez l’action **Modifier paramètres présentation colonne**.  
2. Dans le champ **Nom présentation colonne**, sélectionnez la présentation de colonne **Trésorerie** pour la définir par défaut.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Pour afficher et imprimer les prévisions de trésorerie

1. Sur la page **Noms tableaux d’analyse**, choisissez l’action **Aperçu** pour afficher les prévisions de trésorerie.  
2. Sur la page **Aperçu tableau d’analyse**, vous pouvez sélectionner un montant, puis afficher les écritures de prévisions de trésorerie qui constituent ce montant. En outre, vous pouvez afficher la formule qui est utilisée pour calculer le montant. Vous pouvez également filtrer les montants par date et par axe analytique.  
3. Choisissez l’action **Imprimer** pour imprimer les prévisions de trésorerie.  

## <a name="see-also"></a>Voir aussi

[Utilisation des tableaux d’analyse](bi-how-work-account-schedule.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]