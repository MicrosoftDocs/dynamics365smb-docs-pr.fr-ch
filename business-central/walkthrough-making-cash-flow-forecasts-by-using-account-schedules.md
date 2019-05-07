---
title: "Procédure pas-à-pas : Créer des prévisions de trésorerie à l'aide des tableaux d'analyse | Microsoft Docs"
description: Cette procédure pas-à-pas décrit le mode d'utilisation des tableaux d'analyse pour élaborer des prévisions de trésorerie. Les tableaux d'analyse procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie. Dans les tableaux d'analyse, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie. Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c09eedbb812df909a43e514dc462dcf8c1cf182a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "932638"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Procédure pas-à-pas : créer des prévisions de trésorerie à l'aide de tableaux d'analyse
Cette procédure pas-à-pas décrit le mode d'utilisation des tableaux d'analyse pour élaborer des prévisions de trésorerie. Les tableaux d'analyse procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie. Dans les tableaux d'analyse, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie. Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Cette procédure pas à pas décrit les tâches suivantes :  

- Configuration d'un nouveau nom du tableau d'analyse de trésorerie.  
- Configuration de lignes du tableau d'analyse  
- Configuration d'une nouvelle présentation de colonne  
- Affectation d'une présentation de colonne à un tableau d'analyse.  
- Affichage et impression des prévisions de trésorerie.  

### <a name="prerequisites"></a>Conditions préalables  
Pour exécuter ce processus pas à pas, vous devez :  

- Installer [!INCLUDE[d365fin](includes/d365fin_md.md)].  
- Les lignes de la feuille d'activité de trésorerie sont enregistrées.  

## <a name="roles"></a>Rôles  
Cette procédure pas à pas présente les tâches effectuées par le rôle utilisateur suivant :  

- Contrôleur  

## <a name="story"></a>Scénario  
Ken est un contrôleur chez CRONUS, chargé d'élaborer des prévisions mensuelles de trésorerie. Il inclut les finances, les ventes, les achats et les immobilisations dans les prévisions, puis les présente à CFO Sara dans un souci de visibilité commerciale.  

## <a name="setting-up-a-new-account-schedule-name"></a>Configuration d'un nouveau nom du tableau d'analyse  
Un tableau d'analyse est composé d'un nom de tableau d'analyse de trésorerie avec une série de lignes et une présentation de colonne.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Pour configurer un nouveau nom de tableau d'analyse  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tableaux d'analyse**, puis sélectionnez le lien associé.  
2.  Sur la page **Noms tableaux d'analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d'analyse de trésorerie.  
3.  Dans le champ **Nom**, entrez **Prévision**.  
4.  Dans le champ **Description**, entrez **Prévision de trésorerie**.  
5.  Laissez vierges les champs **Présentation colonne par déf.** et **Nom vue d'analyse** .  

## <a name="setting-up-account-schedule-lines"></a>Configuration de lignes du tableau d'analyse  
Après la configuration d'un nom de tableau d'analyse, Ken définit chaque ligne qui s'y affiche. Ken définit les lignes qui peuvent être affichées dans les états en plus des lignes destinées uniquement au calcul.  

### <a name="to-set-up-account-schedule-lines"></a>Pour configurer les lignes du tableau d'analyse  

1.  Sur la page **Noms tableaux d'analyse**, sélectionnez le nouveau nom du tableau d’analyse **Prévision** que vous venez de créer. Sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Modifier tableau d'analyse**.  
2.  Sur la page **Tableau d'analyse**, entrez chaque ligne, comme indiqué dans le tableau suivant.  

    > [!NOTE]  
    >  À l’aide de la fonction **Insérer des comptes CF**,vous pouvez sélectionner rapidement les comptes de trésorerie à partir du plan comptable de trésorerie et les copier vers les lignes du tableau d’analyse.  

    |N° ligne|Description|Type totalisation|Totalisation|Type ligne|Type montant|Afficher|  
    |-------|-----------|-------------|--------|--------|---  ------|----| |C10|Montant|Solde période|Écritures|Montant net|Toujours|  
    |C20|Montant jusque date|Solde au|Ecritures|Montant net|Toujours|  
    |C30|Exercice complet|Exercice complet|Ecritures|Montant net|Toujours|  

4.  Cliquez sur le bouton **OK**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Affectation de la présentation de colonne au nom de tableau d'analyse  
Ken est désormais prêt à affecter la présentation de colonne au nom de tableau d'analyse.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Pour affecter la présentation de colonne au nom de tableau d'analyse  

1.  Sur la page **Noms tableaux d'analyse**, sélectionnez **Prévision** dans le champ **Nom**.  
2.  Dans le champ **Présentation colonne par déf.**, sélectionnez la présentation de colonne **Trésorerie** pour la définir par défaut.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Pour afficher et imprimer les prévisions de trésorerie  
1.  Sur la page **Noms tableaux d'analyse**, choisissez l'action **Aperçu** pour afficher les prévisions de trésorerie.  
2.  Sur la page **Aperçu tableau d'analyse**, vous pouvez sélectionner un montant, puis afficher les écritures de prévisions de trésorerie qui constituent ce montant. En outre, vous pouvez afficher la formule qui est utilisée pour calculer le montant. Vous pouvez également filtrer les montants par date et par axe analytique.  
3.  Choisissez l'action **Imprimer** pour imprimer les prévisions de trésorerie.  

## <a name="see-also"></a>Voir aussi  
 [Utilisation des tableaux d'analyse](bi-how-work-account-schedule.md)   
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
