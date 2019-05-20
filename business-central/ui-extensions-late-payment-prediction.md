---
title: Prévoir des retards de paiement pour les documents vente | Microsoft Docs
description: Utilisez notre modèle prédictif pour prévoir si une facture sera payée à temps.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 54a7ad407ef3322ec1e02de4b20a934163a21a8e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251346"
---
# <a name="the-late-payment-prediction-extension"></a>Extension Prévisions de retard de paiement  
Une gestion efficace des créances est importante pour la santé financière générale d'une société. L'extension de prévision de retard de paiement peut vous aider à minimiser les créances ouvertes et à ajuster votre stratégie de collectes en prévoyant si les factures vente seront payées à temps. Par exemple, si un retard de paiement est prévu, vous pouvez décider d'ajuster les conditions de paiement ou le mode de règlement du client.

## <a name="what-are-predictions-based-on"></a>Sur quoi sont basées les prévisions ?  
L'extension Prévision de retard de paiement utilise un modèle prédictif que nous avons développé dans Azure Machine Learning Studio et formé en utilisant des données représentant une plage de petites et moyennes sociétés. Bien que nous l'ayons déjà formé et évalué, notre modèle prédictif continue d'apprendre de vos données. Plus vous utilisez le modèle et plus vous lui fournissez de données, plus les prévisions deviendront précises. Par défaut, l'extension évalue le modèle et met à jour les prévisions sur une base hebdomadaire. Toutefois, vous pouvez mettre à jour les prévisions chaque fois que vous le souhaitez en choisissant l'action **Mettre à jour les prévisions** sur la page **Écritures comptables client**.  

> [!Note]
> Nous utilisons une partie de votre temps de calcul chaque semaine lorsque nous évaluons le modèle et mettons vos prévisions à jour. En plus de mettre manuellement les prévisions à jour, d'autres actions qui consomment du temps de calcul sont lorsque vous formez le modèle (ce que vous pouvez effectuer si vous avez récemment ajouté des données) et lorsque vous évaluez le modèle (qui examine la qualité du modèle).

## <a name="getting-started"></a>Mise en route
L'extension est gratuite dans [!INCLUDE[d365fin](includes/d365fin_md.md)], et nous fournissons un abonnement à Azure Machine Learning. L'abonnement offre 30 minutes de temps de calcul par mois. Si vous avez besoin de plus de temps vous pouvez créer votre propre modèle prédictif et l'utiliser à la place. Pour plus d'informations, voir la section intitulée _Création de votre propre modèle prédictif_ ultérieurement dans cette rubrique.  

Lorsque vous ouvrez un document vente validé, une notification s'affiche en haut de la page. Pour utiliser l'extension Prévision de retard de paiement vous pouvez choisir de sélectionner **Activer** dans la notification. Sinon, vous pouvez configurer l'extension manuellement. Par exemple, si vous regrettez d'ignorer la notification.  

Pour activer manuellement l'extension, procédez comme suit :

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Connexions au service**, puis sélectionnez le lien associé.  
2. Choisissez l'option **Configuration des prévisions de retard de paiement**, puis renseignez les champs selon vos besoins.

## <a name="viewing-all-payment-predictions"></a>Affichage de toutes les prévisions de paiement
Si vous activez l'extension, une vignette **Retards de paiements prévus** est disponible dans le tableau de bord **Gestionnaire d'activité**. La vignette affiche le nombre de retards de paiements prévus, et vous permet d'ouvrir la page **Écritures comptables client** où vous pouvez examiner plus en détail dans les factures validées. Il existe trois colonnes à examiner attentivement :  

* **Retard de paiement** - Indique si le paiement de la facture sera en retard.
* **Niveau de fiabilité de la prévision** - Indique la fiabilité de la prévision. **Elevée** signifie que la prévision est fiable à au moins 90 %, **Moyenne** est compris entre 80 et 90 %, et **Faible** est inférieur à 80 %.
* **% du niveau de fiabilité de la prévision** - Affiche le pourcentage réel de du niveau de fiabilité. Par défaut, cette colonne ne s'affiche pas, mais vous pouvez l'ajouter si vous le souhaitez. Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).

> [!Tip]
> La page Écritures comptables client affiche également un récapitulatif à droite. Lorsque vous vérifiez les prévisions, les informations de la section **Détails client** peuvent être utile. Lorsque vous sélectionnez la facture dans la liste, la section affiche des informations sur le client. Elle vous permet également de prendre une mesure immédiates. Par exemple, si un client égare fréquemment son portefeuille, vous pouvez ouvrir la fiche client dans le récapitulatif et bloquer le client pour des ventes futures.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Affichage d'une prévision de paiement pour un document vente spécifique
Vous pouvez également prévoir des retards de paiement par avance. Sur les pages **Devis**, **Commandes vente**, et **Factures vente**, vous pouvez utiliser l'action **Prévoir le paiement** pour générer des prévisions pour le document vente que vous visualisez.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Génération de votre propre modèle de prévision
Vous souhaitez générer votre propre modèle de prévision ? Vous pouvez utiliser Azure Machine Learning Studio pour générer votre propre modèle prédictif et l'utiliser dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour utiliser votre propre modèle, vous devez vous abonner Azure Machine Learning. Pour plus d'informations, voir [Documentation Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Cependant, nous offrons un moyen plus facile de créer et d'utiliser votre propre modèle de prévision. Vous pouvez partager les données de vos factures avec notre [expérience prévisionnelle pour Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?linkid=2086310) dans Azure Machine Learning, et laisser notre expérience créer et former un modèle prédictif selon vos données. Pour partager vos données, sur la page **Configuration des prévisions de retard de paiement**, choisissez l'action **Créer mon modèle**. Ensuite, les prévisions seront basées sur votre modèle et vos données, pas les nôtres.  

> [!Note]
>   La qualité du modèle est importante. Lorsque notre expérience prévisionnelle utilise vos données pour former un modèle, elles déterminent la valeur de la qualité du modèle en pourcentage. La qualité du modèle indique la probabilité de précision des prévisions du modèle. Plusieurs facteurs peuvent affecter la qualité d'un modèle. Par exemple, ces facteurs peuvent être qu'il n'y avait pas assez de données, ou que les données n'avaient pas de variation suffisante. Vous pouvez afficher la qualité du modèle que vous utilisez actuellement sur la page **Configuration des prévisions de retard de paiement**. Vous pouvez également spécifier un seuil minimum pour la qualité du modèle. Les modèles avec une valeur de qualité inférieure au seuil ne produiront pas de prévisions.  

### <a name="to-use-your-model-instead-of-ours"></a>Pour utiliser votre modèle au lieu du nôtre  
Si vous créez votre propre modèle dans Azure Machine Learning Studio, sans utiliser les outils de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez fournir vos informations d'identification afin que [!INCLUDE[d365fin](includes/d365fin_md.md)] puisse accéder au modèle. Plusieurs étapes sont nécessaires :

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration des prévisions de retard de paiement**, puis sélectionnez le lien associé.  
2. Activez la case à cocher **Utiliser mon abonnement Azure**.  
3. Dans le champ **Modèle sélectionné**, choisissez **Mon modèle**.  
4. Sur l'organisateur **Mes informations d'identification du modèle**, saisissez l'URL d'API et la clé API de votre modèle.  

## <a name="see-also"></a>Voir aussi  
[Documentation Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Personnalisation de Business Central à l'aide d'extensions](ui-extensions.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
