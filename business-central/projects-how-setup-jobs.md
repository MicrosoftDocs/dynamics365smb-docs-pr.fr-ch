---
title: 'Configurer des projets, des prix et des groupes comptabilisation projet'
description: 'Décrit comment configurer des informations générales de projets, et des prix d’articles de projet, des ressources, ainsi que des comptes généraux et des groupes de comptabilisation projets.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.date: 04/01/2021
ms.author: edupont
---
# Configurer des projets, des prix et des groupes comptabilisation projet

En tant que chef de projet, vous pouvez définir des projets qui définissent chacun des projets que vous gérez dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Paramètres projets**, vous devez spécifier comment utiliser certaines fonctions de projet.

Pour chaque projet, vous précisez ensuite les fiches projet individuelles avec des informations concernant les prix pour les articles, les ressources et les comptes généraux du projet, puis vous devez configurer des groupes comptabilisation du projet.

## Pour configurer des informations générales pour les projets

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres projets**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Le champ **Appliquer le lien d′utilisation par défaut** indique si les écritures comptables projet sont liées aux lignes planning projet par défaut. Sélectionnez le champ si vous souhaitez appliquer ce paramètre à tous les nouveaux projets que vous créez. Vous pouvez activer ou désactiver le suivi de l′utilisation des projets pour un projet donné en modifiant la valeur du champ **Appliquer le lien d′utilisation** sur la fiche projet individuelle. Les conséquences sont expliquées dans la section suivante.

### Pour configurer un suivi d’utilisation de projet

Lors de l’utilisation d’un projet, vous avez peut-être besoin de savoir si votre utilisation est conforme au plan. Pour entreprendre facilement cette action, vous pouvez créer un lien entre vos lignes planning du projet et l’utilisation réelle. Cela vous permet de suivre vos coûts et de voir aisément le travail qui reste à effectuer. Par défaut, le type ligne planning projet est *Budget*, mais l’utilisation du type ligne **Budget et Facturable** a des effets similaires.

Après avoir configuré le suivi de l′utilisation en sélectionnant le champ **Appliquer le lien d’utilisation**, vous pouvez consulter les informations sur la ligne planning projet. Vous pouvez définir la quantité de ressources, d’articles ou le compte général, puis indiquer la quantité à transférer sur la feuille projet. Le champ **Quantité restante** dans la ligne planning projet vous aide à déterminer ce qui reste à transférer et à valider dans la feuille projet.

>[!NOTE]
> Si le champ **Appliquer le lien d′utilisation** est sélectionné sur le projet individuel et que le champ **Type ligne** sur la ligne feuille projet ou la ligne achat est *Facturable*, de nouvelles lignes planning projet de type ligne *Budget* sont créées lorsque vous validez une ligne feuille ou un document achat.  
> Pour plus d′informations, voir [Enregistrer l′utilisation pour les projets](projects-how-record-job-usage.md) et [Gérer les fournitures de projet](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Si le champ **Type ligne** sur la ligne feuille projet ou la ligne achat est vide, aucune ligne planning projet n′est créée lorsque vous validez la feuille projet ou le document achat.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## Pour paramétrer les prix pour des ressources, des articles et des comptes généraux pour des projets

> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé de nouveaux processus pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Vous pouvez paramétrer les prix pour des articles, des ressources et des comptes généraux associés à un projet. 

#### [Expérience actuelle](#tab/current-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet, puis cliquez sur l’action **Ressource**, **Article** ou **Compte général**.
3. Sur la page **Prix ressource projet**, **Prix article projet** ou **Prix compte général projet**, remplissez les champs selon vos besoins.

Le tableau suivant montre comment les informations des champs facultatifs seront utilisées sur les lignes planning projet et les journaux lorsque la ressource, l’article ou le compte général sont choisis pour le projet.

|Colonne1  |Colonne2  |
|---------|---------|
|**Ressources du projet**|Champs **N° tâche projet**, **Type travail**, **Code devise**, **% Remise ligne** et **Facteur coût unitaire**. La valeur du champ **Prix unitaire** de la ressource sera utilisée sur les lignes planning du projet et les feuilles projet lorsque cette ressource, une ressource affectée au groupe de ressources ou une ressource quelconque est entrée. Notez que ce prix remplace toujours les prix paramétrés sur la page **Prix ressource/Prix groupe ressources** existante.|
|**Articles du projet**|Champs **N° tâche projet**, **Code devise** et **% Remise ligne**. La valeur du champ **Prix unitaire** pour l’article sera utilisée sur les lignes planning du projet et les feuilles projet lorsque cet article sera entré. Notez que ce prix remplace toujours le prix client habituel (mécanisme du « meilleur prix ») des articles. Pour utiliser les mécanismes des prix client habituels, ne créez pas de prix article projet pour le projet.|
|**Comptes généraux**|Les informations contenues dans les champs **N° tâche projet**, **Code devise**, **% remise ligne**, **Facteur coût unitaire** et **Coût unitaire** serviront sur les lignes planning projet et les feuilles projet lorsque ce compte général sera entré et ajouté à un projet. La valeur du champ **Prix unitaire** pour les dépenses du compte général sera utilisée sur les lignes planning du projet et les feuilles projet lorsque le compte général sera entré.|

#### [Nouvelle expérience](#tab/new-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis cliquez sur l’action **Listes prix vente**.

---

## Pour configurer les groupes compta. projet

L’un des aspects des projets de planification est de décider quels comptes de validation utiliser pour l’évaluation du stock projet. Pour valider des projets, vous configurez des comptes afin de valider chaque groupe compta. projet. Un groupe comptabilisation représente un lien entre le projet et la manière dont il doit être traité dans la comptabilité. Lorsque vous créez un projet, vous pouvez spécifier un groupe comptabilisation et, par défaut, chaque tâche que vous créez pour le projet est associée avec ce groupe comptabilisation. Toutefois, lorsque vous créez des tâches, vous pouvez remplacer la valeur par défaut et sélectionner un groupe comptabilisation plus approprié.  

> [!NOTE]  
>   Les comptes nécessaires dans la table Plan comptable doivent être configurés avant de créer les groupes comptabilisation. Pour plus d’informations, reportez-vous à [Configuration ou modification du plan comptable](finance-setup-chart-accounts.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. projet**, puis choisissez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs du compte comme indiqué dans le tableau suivant.  

| Champ de compte | Désignation |
| --- | --- |
| **Code** |Un code pour le groupe comptabilisation. Vous pouvez entrer un maximum de 10 caractères, espaces compris. |
| **Compte dépenses TEC** |Compte TEC pour les dépenses calculées des TEC du projet, qui est un compte d’actif capital de bilan. |
| **Compte coûts à payer TEC** |Compte pour la méthode Valeur coût ou Coût des ventes du calcul TEC, qui est un compte de passif bilan de charge à payer. Validé lorsque l’ajustement TEC exige l’augmentation des coûts d′utilisation validés dans les comptes de gestion. |
| **Compte coûts lettrés projet** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés article** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés ressource** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte ajustement coûts projet** |Compte de contrepartie du compte coûts à payer TEC, qui est un compte frais. |
| **Compte frais Général (budget)** |Le compte ventes qui sera utilisé pour les dépenses générales dans les tâches projet avec ce groupe comptabilisation. S’il n’est pas renseigné, le compte général entré sur la ligne planning projet est utilisé. |
| **Compte ventes à payer TEC** |Compte TEC pour la valeur des ventes calculée des TEC, qui est un compte de passif bilan. Validé lorsque l’ajustement TEC exige l’augmentation du revenu réceptionné. |
| **Compte ventes facturées TEC** |Compte pour la valeur des ventes facturées des TEC qui ne peuvent pas être réceptionnés. Il s’agit d’un compte bilan produit comptabilisé d’avance. |
| **Compte ventes lettrées projet** |Compte de contrepartie du Compte ventes facturées TEC, qui est un compte de contrepartie de revenu. |
| **Compte ajustement vente projet** |Compte de contrepartie du Compte ventes projet TEC, qui est un compte de revenu. |
| **Compte coûts récep.** |Compte frais contenant les coûts réceptionnés du projet. Il s’agit ordinairement d’un compte frais pour débit. |
| **Compte ventes récep.** |Compte de revenu contenant les revenus réceptionnés du projet. Il s’agit ordinairement d’un compte de revenu pour crédit. |

## Voir la [formation Microsoft](/training/paths/set-up-jobs-resources/) associée

## Voir aussi

[Configurer la gestion de projet](projects-setup-projects.md)  
[Vidéo : Créer un projet dans Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestion des projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
