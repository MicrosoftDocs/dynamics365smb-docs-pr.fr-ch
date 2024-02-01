---
title: 'Configurer des projets, des prix et des groupes comptabilisation projet'
description: Décrit comment configurer des informations générales sur les projets.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# Configurer des projets, des prix et des groupes comptabilisation projet

En tant que chef de projet, vous pouvez définir des projets qui définissent chacun des projets que vous gérez dans [!INCLUDE[prod_short](includes/prod_short.md)]. Utilisez la page **Paramètres projets** pour définir la façon dont vous utilisez les fonctions du projet.

Pour chaque projet, précisez diverses informations :

* Prix des articles du projet
* Ressources du projet
* Comptes généraux du projet
* Groupes comptabilisation du projet (requis)

## Pour configurer des informations générales pour les projets

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Paramètres projets**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Le bouton bascule **Appliquer le lien d′utilisation par défaut** sur la page **Paramètres projets** indique si les écritures comptables projet sont liées aux lignes planning projet par défaut. Activez le bouton bascule pour appliquer ce paramètre à tous les nouveaux projets. Vous pouvez activer ou désactiver le suivi de l′utilisation des projets pour un projet donné en activant ou désactivant le bouton bascule **Appliquer le lien d′utilisation** sur la page **Fiche projet**.

### Pour configurer un suivi d’utilisation de projet

Lors de l’utilisation d’un projet, vous avez peut-être besoin de savoir si votre utilisation est conforme au plan. Pour explorer l’utilisation, vous pouvez créer un lien entre vos lignes planning projet et l’utilisation réelle. Le lien vous permet de suivre vos coûts et de comprendre la quantité de travail restante. Par défaut, le type de ligne planning projet est **Budget**, mais l’utilisation du type de ligne **Budget et Facturable** a des effets similaires.

Après avoir configuré le suivi de l′utilisation en activant le bouton bascule **Appliquer le lien d’utilisation par défaut**, vous pouvez consulter les informations sur la ligne planning projet. Par exemple, vous pouvez définir la quantité de la ressource, de l’article ou du compte général. Vous pouvez également définir la quantité à transférer vers la feuille projet. Le champ **Quantité restante** sur la ligne planning projet indique ce qui reste à transférer et à valider dans la feuille projet.

>[!NOTE]
> Si le champ **Appliquer le lien d′utilisation** est sélectionné dans le projet et que le champ **Type ligne** sur la ligne feuille projet ou la ligne achat est **Facturable**, de nouvelles lignes planning projet du type de ligne **Budget et Facturable** sont créées lorsque vous validez la ligne feuille ou le document achat.  
>
> Pour plus d′informations, voir [Enregistrer l′utilisation pour les projets](projects-how-record-job-usage.md) et [Gérer les fournitures de projet](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Si vous ne spécifiez pas de valeur dans le champ **Type ligne** de la ligne feuille projet ou la ligne achat, les lignes planning projet ne sont pas créées lorsque vous validez la feuille projet ou le document achat.

## Pour paramétrer les prix pour des ressources, des articles et des comptes généraux pour des projets

> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé de nouveaux processus pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Vous pouvez paramétrer les prix pour des articles, des ressources et des comptes généraux associés à un projet. 

#### [Expérience actuelle](#tab/current-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet, puis cliquez sur l’action **Ressource**, **Article** ou **Compte général**.
3. Sur la page **Prix ressource projet**, **Prix article projet** ou **Prix compte général projet**, remplissez les champs selon vos besoins.

Lorsque vous choisissez une ressource, un article ou un compte général pour un projet, [!INCLUDE [prod_short](includes/prod_short.md)] utilise des informations dans les champs facultatifs des lignes planning projet et des feuilles projet. Le tableau suivant explique comment.

|Colonne1  |Colonne2  |
|---------|---------|
|**Ressources du projet**|Champs **N° tâche projet**, **Type travail**, **Code devise**, **% Remise ligne** et **Facteur coût unitaire**. La valeur du champ **Prix unitaire** de la ressource est utilisée sur les lignes planning projet et les feuilles projet lorsque vous saisissez une ressource ou une ressource affectée au groupe de ressources. Ce prix remplace les prix spécifiés sur la page **Prix de la ressource/Prix du groupe de ressources**.|
|**Articles du projet**|Champs **N° tâche projet**, **Code devise** et **% Remise ligne**. La valeur du champ **Prix unitaire** pour l’article sera utilisée sur les lignes planning du projet et les feuilles projet lorsque cet article sera entré. Ce prix remplace le prix client habituel (mécanisme du « meilleur prix ») des articles. Pour utiliser le prix client habituel, ne spécifiez pas de prix article projet pour le projet.|
|**Comptes généraux**|Les informations contenues dans les champs **N° tâche projet**, **Code devise**, **% remise ligne**, **Facteur coût unitaire** et **Coût unitaire** serviront sur les lignes planning projet et les feuilles projet lorsque ce compte général sera entré et ajouté à un projet. Lorsque vous choisissez un compte général, des lignes planning projet et des feuilles projet, utilisez la valeur du champ **Prix unitaire** pour les dépenses du projet.|

#### [Nouvelle expérience](#tab/new-experience)

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis cliquez sur l’action **Listes prix vente**.

---

## Pour configurer les groupes compta. projet

L’un des aspects des projets de planification est de décider quels comptes de validation utiliser pour l’évaluation du stock projet. Pour valider des projets, vous configurez des comptes afin de valider chaque groupe compta. projet. Un groupe comptabilisation représente un lien entre le projet et la manière dont il doit être traité dans la comptabilité. Lorsque vous créez un projet, vous pouvez spécifier un groupe comptabilisation et, par défaut, chaque tâche que vous créez pour le projet est associée avec ce groupe comptabilisation. Toutefois, lorsque vous créez des tâches, vous pouvez remplacer la valeur par défaut et sélectionner un groupe comptabilisation plus approprié.  

> [!NOTE]  
> Vous devez configurer les comptes dans le plan comptable avant de configurer les groupes comptabilisation. Pour plus d’informations, reportez-vous à [Configuration ou modification du plan comptable](finance-setup-chart-accounts.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. projet**, puis choisissez le lien associé.  
2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

| Champ de compte | Désignation | Utilisé dans le type TEC |
| --- | --- |  --- |
| **Code** |Identificateur pour le groupe comptabilisation. Vous pouvez entrer un maximum de 10 caractères, espaces compris. | |
| **Compte dépenses TEC** |Compte TEC pour les dépenses calculées des TEC du projet, qui est un compte d’actif capital de bilan. | Coût appliqué, coûts reconnus|
| **Compte coûts à payer TEC** |Compte pour la méthode Valeur coût ou Coût des ventes du calcul TEC. Ce compte concerne le passif de charge à payer sur votre bilan. Lorsqu’un ajustement TEC vous oblige à augmenter les coûts activité que vous validez dans votre compte de gestion, vous les validez dans ce compte. | Coûts à payer|
| **Compte coûts lettrés projet** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. Utilisé lorsque **Méthode de comptabilisation TEC utilisée** est définie sur *Projet*. | Coûts appliqués, coûts reconnus|
| **Compte coûts lettrés article** |Identique au **Compte coûts lettrés projet**, mais utilisé lorsque **Méthode de comptabilisation TEC utilisée** est définie sur *Écriture comptable projet*.| |
| **Compte coûts lettrés ressource** |Identique au **Compte coûts lettrés projet**, mais utilisé lorsque **Méthode de comptabilisation TEC utilisée** est définie sur *Écriture comptable projet*.| |
| **Compte coûts lettrés général** |Identique au **Compte coûts lettrés projet**, mais utilisé lorsque **Méthode de comptabilisation TEC utilisée** est définie sur *Écriture comptable projet*.| |
| **Compte ajustement coûts projet** |Compte de contrepartie du compte coûts à payer TEC, qui est un compte frais. | Coûts à payer|
| **Compte frais Général (budget)** |Le compte ventes qui sera utilisé pour les dépenses générales dans les tâches projet avec ce groupe comptabilisation. S’il n’est pas renseigné, le compte général entré sur la ligne planning projet est utilisé. | |
| **Compte ventes à payer TEC** |Compte TEC pour la valeur des ventes calculée des TEC, qui est un compte de revenus à payer pour votre bilan. Lorsqu’un ajustement TEC vous oblige à augmenter le revenu réceptionné, vous le validez dans ce compte. | Ventes accumulées, ventes reconnues|
| **Compte ventes facturées TEC** |Compte pour la valeur des ventes facturées des TEC qui ne peuvent pas être réceptionnés. Il s’agit d’un compte bilan produit comptabilisé d’avance. | Ventes Lettrées, ventes reconnues|
| **Compte ventes lettrées projet** |Compte de contrepartie du Compte ventes facturées TEC, qui est un compte de contrepartie de revenu. | Ventes Lettrées, ventes reconnues|
| **Compte ajustement vente projet** |Compte de contrepartie du Compte ventes projet TEC, qui est un compte de revenu. | Ventes à payer|
| **Compte coûts récep.** |Compte frais contenant les coûts réceptionnés du projet. Il s’agit ordinairement d’un compte frais pour débit. | Coûts réceptionnés|
| **Compte ventes récep.** |Compte de revenu contenant les revenus réceptionnés du projet. Il s’agit ordinairement d’un compte de revenu pour crédit. | Ventes réceptionnées|

## Voir aussi

[Configuration de la gestion des stocks](projects-setup-projects.md)  
[Vidéo : Créer un projet dans Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestion des projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
