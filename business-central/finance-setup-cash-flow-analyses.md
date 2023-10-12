---
title: Configuration d’une analyse de trésorerie (contient une vidéo)
description: 'Utilisez les graphiques du tableau de bord Comptes pour aider à analyser le flux de trésorerie dans vos activités, y compris les dépenses et les recettes, liquidités, et les règlements entrants moins les règlements sortants.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
---
# Configuration d’une analyse de trésorerie

Si vous souhaitez de l’aide pour décider quelles opérations effectuer avec votre trésorerie, consultez les graphiques dans le tableau de bord Comptable :

* **Cycle trésorerie**  
* **Revenus et dépenses**  
* **Trésorerie**  
* **Prévisions de la trésorerie**  

Cet article décrit d’où proviennent les données dans les graphiques et, si nécessaire, quoi faire pour commencer à utiliser les graphiques.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## Les graphiques Cycle trésorerie et Revenus et dépenses

Les graphiques **Cycle trésorerie** et **Revenus et dépenses** sont prêts à être utilisés, en fonction du plan comptable et des états financiers. Les données sont issues de ces comptes, et les états financiers calculent les relations entre les ventes et les créances. Certains comptes et états financiers sont fournis. Vous pouvez les utiliser tels quels, les modifier, puis en ajouter de nouveaux. Si vous ajoutez des comptes généraux à votre plan comptable, par exemple, en les important de QuickBooks, vous devez les associer aux comptes sur la page **États financiers** pour les états suivants :

| Nom état financier | Emplacement d’utilisation |
| --- | --- |
| **I_CACYCLE** |Cycle trésorerie |
| **I_CASHFLOW** |Trésorerie |
| **I_INCEXP** |Revenus et dépenses |
| **I_MINTRIAL** |Comme compte de gestion si vous n’utilisez pas le plan comptable |

> [!NOTE]
> Il est conseillé de conserver les calculs qui sont fournis pour l’état financier.

Saisissez les comptes dans le champ **Totalisation** pour **Total produits**, **Total clients**, **Total fournisseurs** et **Stock total**. Pour mapper sur une plage de comptes, entrez les numéros de compte séparés par « .. » comme dans **1111..4444**. Sinon, pour mapper sur des comptes spécifiques, entrez les numéros de compte séparés par une barre verticale dans **2222|3333|5555**.  

> [!TIP] 
> Vérifiez votre mappage en choisissant l’option **Aperçu**.  

## Configurer le plan comptable de trésorerie

Le plan comptable de trésorerie est basé sur ce qui suit :  

* Un plan comptable de trésorerie.
* Un ou plusieurs paramétrages de trésorerie. Ils spécifient les comptes à utiliser pour les écritures comptables, les achats, les ventes, les services et les immobilisations.  

Pour vous aider à poursuivre, certains comptes et paramétrages de trésorerie sont fournis. Vous pouvez en ajouter, en modifier ou en supprimer.  

Pour les configurer, recherchez **Comptes de trésorerie**, choisissez le lien, puis renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Répétez ces étapes pour **Paramètres trésorerie**.

## Configurer les prévisions de trésorerie

Le graphique **Prévision de trésorerie** utilise les comptes de trésorerie, les paramétrages de trésorerie et les prévisions de trésorerie. Certains comptes sont fournis, cependant, vous pouvez définir les vôtres à l’aide d’un guide de configuration assistée. Le guide vous aide à spécifier des éléments, tels que la fréquence de mise à jour des prévisions, les comptes sur lesquels les baser, les informations concernant l’échéance de paiement des taxes et s’il convient d’utiliser [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Les prévisions de trésorerie peuvent utiliser Azure AI pour créer une prévision plus complète. La connexion à Azure AI est déjà configurée pour vous. Vous devez juste l’activer. Lorsque vous vous connectez à [!INCLUDE[prod_short](includes/prod_short.md)], une notification s’affiche dans une barre bleue et inclut un lien vers le paramétrage par défaut de trésorerie. La notification s’affiche une seule fois. Si vous la fermez, mais décidez d’activer Azure AI, vous pouvez utiliser le guide de configuration assistée ou un processus manuel.  

> [!NOTE]
>
> Sinon, vous pouvez utiliser votre propre service Web prévisionnel. Pour plus d’informations, voir [Créer et utiliser votre propre service Web prévisionnel pour des prévisions de trésorerie](#AnchorText).  

Pour utiliser le guide de configuration assistée :  

1. Dans le tableau de bord Comptable, sous le graphique **Prévisions de trésorerie**, sélectionnez l’action **Ouvrir la configuration assistée**.
2. Complétez les champs de chaque étape du guide. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans le tableau de bord Comptable, sous le graphique **Prévision de trésorerie**, sélectionnez l’action **Recalculer la prévision**.

Pour utiliser une procédure manuelle :  

1. Dans le tableau de bord Comptable, sélectionnez l’![icône en forme d’ampoule qui ouvre la fonctionnalité Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de trésorerie**, puis sélectionnez le lien associé.
2. Affichez l’organisateur **Azure AI**, puis sélectionnez le champ **Azure AI activé**.
3. Dans le tableau de bord Comptable, sous le graphique **Prévision de trésorerie**, sélectionnez l’action **Recalculer la prévision**.

> [!TIP]  
> Tenez compte de la durée des périodes utilisée par le service lors de ses calculs. Plus vous fournissez de données, plus les prévisions seront précises. En outre, soyez prudent en ce qui concerne les grands écarts entre les périodes. Cela aura également un impact sur les prévisions. Si Azure AI ne trouve pas suffisamment de données ou si les données varient considérablement, le service ne fera pas de prévisions.  

## Détails de conception

Les abonnements à [!INCLUDE[prod_short](includes/prod_short.md)] fournissent un accès à plusieurs services web prévisionnels dans toutes les régions où [!INCLUDE[prod_short](includes/prod_short.md)] est disponible. En savoir plus sur le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Ces services web sont sans état. Autrement dit, ils utilisent des données uniquement pour calculer des prévisions à la demande. Ils ne stockent pas de données.

> [!NOTE]
>
> Vous pouvez utiliser votre propre service web prévisionnel au lieu du nôtre. Pour plus d’informations, voir [Créer et utiliser votre propre service Web prévisionnel pour des prévisions de trésorerie](#AnchorText).

### Données requises pour les prévisions

Pour faire des prévisions sur les revenus et dépenses futurs, les services web nécessitent des données historiques sur les créances, les dettes et les taxes.

#### Clients

Champs **Date d’échéance** et **Montant DS** sur la page **Écritures comptables client**, où :

* Le type de document est *Facture* ou *Avoir*.
* La date d’échéance se situe entre la date calculée sur la base des valeurs dans les champs **Périodes historiques** et **Type de période** sur la page **Paramètres trésorerie** et la date de travail.

Avant d’utiliser le service web prédictif, [!INCLUDE[prod_short](includes/prod_short.md)] comprime les transactions par **Date d’échéance** sur la base de la valeur dans le champ **Type de période** sur la page **Paramètres trésorerie**.

#### Fournisseurs

Champs **Date d’échéance** et **Montant DS** sur la page **Écritures comptables fournisseur**, où :

* Le type de document est *Facture* ou *Avoir*.
* La date d’échéance se situe entre la date calculée sur la base des valeurs dans les champs **Périodes historiques** et **Type de période** sur la page **Paramètres trésorerie** et la date de travail.

Avant d’utiliser le service web prédictif, [!INCLUDE[prod_short](includes/prod_short.md)] comprime les transactions par **Date d’échéance** sur la base de la valeur dans le champ **Type de période** sur la page **Paramètres trésorerie**.

#### Taxe

Champs **Date document** et **Montant** sur la page **Écritures comptables TVA (taxe)**, où :

* Le type de document est *vente*.
* La date document se situe entre la date calculée sur la base des valeurs dans les champs **Périodes historiques** et **Type de période** sur la page **Paramètres trésorerie** et la date de travail.

Avant d’utiliser le service web prédictif, [!INCLUDE[prod_short](includes/prod_short.md)] comprime les transactions par **Date document** sur la base de la valeur dans le champ **Type de période** sur la page **Paramètres trésorerie**.

## <a name="AnchorText"></a>Créer et utiliser votre propre service Web prévisionnel pour des prévisions de trésorerie

Vous pouvez aussi utiliser votre propre service Web prévisionnel basé sur un modèle public intitulé **Modèle de prévision pour Microsoft Business Central**. Ce modèle prévisionnel est disponible en ligne dans la galerie Azure AI. Pour utiliser le modèle, procédez comme suit :  

1. Ouvrez un navigateur et accédez à la [Galerie Azure AI](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Recherchez **Modèle prévisionnel pour Microsoft Business Central**, puis ouvrez-le dans Microsoft Azure Machine Learning Studio.  
3. Utilisez votre compte Microsoft pour enregistrer un espace de travail, puis copiez le modèle.  
4. Exécutez le modèle, et publiez-le comme service Web.  
5. Notez l’URL d’API et la clé d’API. Vous allez utiliser ces informations d’identification pour une configuration de trésorerie.  
6. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de trésorerie**, puis sélectionnez le lien associé.  
7. Développez le raccourci **Azure AI**, puis renseignez les champs, y compris l’URL de l’API et la clé d’API fournie depuis Azure Machine Learning studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Dans le tableau de bord Comptable, sous le graphique **Prévision de trésorerie**, sélectionnez l’action **Recalculer la prévision**.

## Voir aussi

[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
