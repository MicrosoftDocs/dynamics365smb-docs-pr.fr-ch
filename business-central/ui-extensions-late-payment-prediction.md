---
title: Prévoir un retard de paiement pour les documents vente
description: Cet article explique comment utiliser notre modèle prédictif pour prévoir si une facture sera payée à temps.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/06/2023
ms.custom: bap-template
---
# Extension Prévisions de retard de paiement

Une gestion efficace des créances est importante pour la santé financière générale d’une société. Pour minimiser les créances ouvertes et ajuster votre stratégie de collectes, l’extension prédit si des retard de paiements sont à attendre. Par exemple, si un retard de paiement est prévu, vous pouvez décider d’ajuster les conditions de paiement ou le mode de règlement du client.

## Démarrer

Lorsque vous ouvrez un document vente validé, une notification s’affiche en haut de la page. Pour utiliser l’extension Prévision de retard de paiement, sélectionnez **Activer** dans la notification. Sinon, vous pouvez configurer l’extension manuellement. Par exemple, si vous regrettez d’ignorer la notification.

Pour activer manuellement l’extension, procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de prévision de paiement en retard**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

> [!NOTE]
> Si vous décidez d’activer l’extension manuellement, sachez que [!INCLUDE[prod_short](includes/prod_short.md)] ne vous permet pas de le faire si la qualité du modèle est faible. La qualité du modèle indique la probabilité de précision des prévisions du modèle. Plusieurs facteurs peuvent affecter la qualité d’un modèle. Par exemple, il n’y avait peut-être pas suffisamment de données ou les données n’avaient pas de variation suffisante. Vous pouvez afficher la qualité du modèle que vous utilisez actuellement sur la page **Configuration des prévisions de retard de paiement**. Vous pouvez également spécifier un seuil minimum pour la qualité du modèle.

## Afficher toutes les prévisions de paiement

Si vous activez l’extension, une vignette **Retards de paiements prévus** est disponible dans le tableau de bord **Gestionnaire d’activité**. La vignette affiche le nombre de retards de paiements prévus, et vous permet d’ouvrir la page **Écritures comptables client** où vous pouvez examiner plus en détail dans les factures validées. Il existe trois colonnes à examiner attentivement :  

* **Retard de paiement** - Indique si le paiement de la facture sera en retard.
* **Niveau de fiabilité de la prévision** - Indique la fiabilité de la prévision. **Elevée** signifie que la prévision est fiable à au moins 90 %, **Moyenne** est compris entre 80 % et 90 %, et **Faible** est inférieur à 80 %.
* **% du niveau de fiabilité de la prévision** - Affiche le pourcentage réel de du niveau de fiabilité. Par défaut, cette colonne est masquée, mais vous pouvez l’ajouter si vous le souhaitez. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

> [!TIP]
> La page Écritures comptables client affiche un Récapitulatif à droite. Lorsque vous vérifiez les prévisions, les informations de la section **Détails client** peuvent être utile. Lorsque vous sélectionnez la facture dans la liste, la section affiche des informations sur le client. Elle vous permet également de prendre une mesure immédiate. Par exemple, si un client égare fréquemment son portefeuille, vous pouvez ouvrir la fiche client dans le récapitulatif et bloquer le client pour des ventes futures.  

## Détails de conception

Microsoft déploie et exploite des services web prédictifs dans toutes les régions où [!INCLUDE[prod_short](includes/prod_short.md)] est disponible. L’accès à ces services web est inclus dans votre abonnement [!INCLUDE[prod_short](includes/prod_short.md)]. Pour en savoir plus, consultez le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Les services web fonctionnent en trois modes :

* Former le modèle. Le service web forme le modèle sur la base de l’ensemble de données fourni.
* Évaluer le modèle. Le service web vérifie si le modèle renvoie des données fiables pour l’ensemble de données fourni.
* Prévoir. Le service web applique le modèle à l’ensemble de données fourni pour établir une prévision.

Ces services web sont sans état. Autrement dit, ils utilisent des données uniquement pour calculer des prévisions à la demande. Ils ne stockent pas de données.

> [!NOTE]  
> Vous pouvez utiliser votre propre service web prévisionnel au lieu du nôtre. Pour en savoir plus, consultez [Créer et utiliser votre propre service web prévisionnel pour des prévisions de retard de paiement](#AnchorText).

### Données nécessaires pour former et évaluer le modèle

Pour chaque **Écriture comptable client** ayant une **Facture vente enregistrée** associée :

* Montant (DS) TTC
* Les conditions de paiement en jours sont calculées comme suit : **Date d’échéance** moins **Date comptabilisation**
* S’il existe un avoir lettré

En outre, l’enregistrement a agrégées les données provenant d’autres factures associées au même client.

- Nombre total et montants total des factures payées
- Nombre total et montants total des factures payées en retard
- Nombre total et montants total des factures en souffrance
- Nombre total et montants total des factures en souffrance déjà en retard
- Moyenne des retards en jours
- Ratio : nombre de factures payées en retard/payées
- Ratio : montant des factures payées en retard/payées
- Ratio : nombre de factures en retard en attente/en souffrance
- Ratio : montants des factures en souffrance en retard/en souffrance

> [!NOTE]
> Les informations sur le client ne sont pas incluses dans le jeu de données.

### Modèle standard et Mon modèle

Le modèle prédictif de l’extension Prévision de retard de paiement est formé à l’aide de données représentant un éventail de PME. Lorsque vous commencez à valider des factures et à recevoir des paiements, [!INCLUDE[prod_short](includes/prod_short.md)] évalue si le modèle standard correspond à votre flux d’activité.

Si vos processus ne correspondent pas au modèle standard, vous pouvez toujours utiliser l’extension, mais vous devrez obtenir plus de données. Continuez simplement à utiliser [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Nous utilisons une partie de votre temps de calcul chaque semaine lorsque nous évaluons et reformons le modèle.

[!INCLUDE[prod_short](includes/prod_short.md)] exécute automatiquement la formation et l’évaluation lorsqu’un nombre suffisant de factures payées et en retard sont disponibles. Cependant, vous pouvez l’exécuter manuellement quand vous le souhaitez.

#### Pour former et utiliser votre modèle

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de prévision de paiement en retard**, puis sélectionnez le lien associé.  
2. Dans le champ **Modèle sélectionné**, choisissez **Mon modèle**.
3. Choisissez l’action **Créer mon modèle** pour former le modèle sur vos données.  

## <a name="AnchorText"> </a>Créer et utiliser votre propre service web prévisionnel pour des prévisions de retard de paiement

Vous pouvez également utiliser votre propre service web prévisionnel basé sur un modèle public nommé **Expérience prévisionnelle pour Dynamics 365 Business Central**. Ce modèle prévisionnel est disponible en ligne dans la galerie Azure AI. Pour utiliser le modèle, procédez comme suit :  

1. Ouvrez un navigateur et accédez à la [Galerie Azure AI](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Recherchez **Expérience prévisionnelle pour Dynamics 365 Business Central**, puis ouvre le modèle dans Azure Machine Learning Studio.  
3. Utilisez votre compte Microsoft pour enregistrer un espace de travail, puis copiez le modèle.  
4. Exécutez le modèle, et publiez-le comme service Web.  
5. Notez l’URL d’API et la clé d’API. Vous allez utiliser ces informations d’identification pour une configuration de trésorerie.  
6. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de prévision de paiement en retard**, puis sélectionnez le lien associé.  
7. Activez la case à cocher **Utiliser mon abonnement Azure**.
8. Sur l’organisateur **Mes informations d’identification du modèle**, saisissez l’URL d’API et la clé API de votre modèle.  

## Voir aussi

[Documentation Azure Machine Learning Studio](/azure/machine-learning/classic/)  
[Personnalisation de Business Central à l’aide d’extensions](ui-extensions.md)  
[Bienvenue dans [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Utiliser l’intelligence artificielle dans Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
