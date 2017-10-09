---
title: Configurer des tarifs de projets et des groupes de comptabilisation de projet| Microsoft Docs
description: "Décrit comment configurer des informations générales de projets, et des prix d'articles de projet, des ressources, ainsi que des comptes généraux et des groupes de comptabilisation projets."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b0e8a73af6f979cb426db1bffc34d154fc439dce
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-jobs"></a>Procédure : configurer des projets
Dans la fenêtre **Paramètres projets**, vous devez spécifier comment utiliser certaines fonctions de projet.

Sur les fiches projet individuelles, vous devez configurer les prix pour les articles, les ressources et les comptes généraux du projet, puis vous devez configurer des groupes comptabilisation du projet.

## <a name="to-set-general-information-for-jobs"></a>Pour configurer des informations générales pour les projets
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres projets**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   La case à cocher **Appliquer le lien d'utilisation** est assez complexe et est donc expliquée dans la section suivante.

## <a name="to-set-up-job-usage-tracking"></a>Pour configurer un suivi d'activité de projet
Lors de l'exécution d'un projet, vous aurez peut-être besoin de savoir si votre activité est conforme au plan. Pour entreprendre facilement cette action, vous pouvez créer un lien entre vos lignes planning du projet et l'utilisation réelle. Cela vous permet de suivre vos coûts et de voir aisément le travail qui reste à effectuer. Par défaut, le type de ligne planning projet est **Budget**, mais l'utilisation du type de ligne **Budget et Facturable** a des effets similaires.

Si vous sélectionnez la case à cocher **Appliquer le lien d'utilisation**, vous pouvez alors consulter les informations sur la ligne planning projet. Vous pouvez définir la quantité de ressources, d'articles ou le compte général, puis indiquer la quantité que vous souhaitez transférer vers la feuille projet. Le champ **Quantité restante** dans la ligne planning projet vous aide à déterminer ce qui reste à transférer et à valider dans la feuille projet.

Lorsque la case à cocher **Appliquer le lien d'utilisation** est activée et que le type de ligne planning projet est **Facturable**, Financials crée une ligne planning projet de type **Budget** une fois la ligne feuille validée.

> [!NOTE]  
>   Si la case à cocher **Appliquer le lien d'utilisation de la fiche projet** est activée et que le champ **Type ligne** sur la ligne feuille projet est vide, alors des lignes planning projet de type ligne **Budget** sont créées lorsque vous validez des lignes feuille. Si la case à cocher **Appliquer le lien d'utilisation** de la fiche projet n'est pas activée et que le champ **Type ligne** sur la ligne feuille projet est vide, dans ce cas aucune ligne planning projet n'est créée lorsque vous validez des lignes feuille. Pour plus d'informations, reportez-vous à [Procédure : Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres projets**, puis choisissez le lien associé.
2. Sélectionnez ou désélectionnez la case à cocher **Appliquer le lien d'utilisation**.

> [!NOTE]  
>   Vous pouvez modifier le paramètre de la case à cocher **Appliquer le lien d'utilisation** sur les différentes fiches projet. Dans ce cas, le paramètre pour ce projet remplace la valeur par défaut globale décrite précédemment.

## <a name="to-set-up-prices-for-job-resources"></a>Pour paramétrer des prix pour les ressources de projet
Vous pouvez paramétrer des prix spécifiques pour les ressources d'un projet. Réalisez cette opération dans la fenêtre **Prix ressource projet**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis l'action **Ressource**.
3. Dans la fenêtre **Prix ressource projet**, renseignez les champs selon vos besoins.

Les informations complémentaires contenues dans les champs **N° tâche projet**, **Type travail**, **Code devise**, **% remise ligne** et **Facteur coût unitaire** serviront sur les lignes planning projet et les feuilles activité lorsque cette ressource sera entrée et ajoutée au projet.  

La valeur du champ **Prix unitaire** de la ressource sera utilisée sur les lignes planning du projet et les feuilles projet lorsque cette ressource, une ressource affectée au groupe de ressources ou une ressource quelconque est entrée.  

> [!NOTE]  
>   Ce prix remplace toujours les prix paramétrés dans les tables **Prix ressource/Prix groupe ressources** existantes.

## <a name="to-set-up-prices-for-job-items"></a>Pour paramétrer les prix pour les articles
Vous pouvez paramétrer des prix spécifiques pour les articles d'un projet. Réalisez cette opération dans la fenêtre **Prix article projet**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis cliquez sur **Article**.
3. Dans la fenêtre **Prix article projet**, renseignez les champs selon vos besoins.

Les informations facultatives des champs **N° tâche projet**, **Code devise** et **% remise ligne** serviront sur les lignes planning du projet et les feuilles projet lorsque cet article sera entré ou ajouté au projet.  

La valeur du champ **Prix unitaire** pour l'article sera utilisée sur les lignes planning du projet et les feuilles projet lorsque cet article sera entré.  

> [!NOTE]  
>   Ce prix remplace toujours le prix client habituel (mécanisme du « meilleur prix ») des articles. Pour utiliser les mécanismes des prix client habituels, ne créez pas de prix article projet pour le projet.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Pour configurer les prix des comptes généraux projet
Vous pouvez configurer les prix spécifiques des frais d'un projet. Réalisez cette opération dans la fenêtre **Prix compte général projet**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.  
2. Sélectionnez le projet concerné, puis cliquez sur **Compte général**.  
3. Dans la fenêtre **Prix compte général projet**, renseignez les champs selon vos besoins.

Les informations complémentaires contenues dans les champs **N° tâche projet**, **Code devise**, **% remise ligne**, **Facteur coût unitaire** et **Coût unitaire** serviront sur les lignes planning projet et les feuilles projet lorsque ce compte général sera entré et ajouté à un projet.  

La valeur du champ **Prix unitaire** pour les dépenses du compte général sera utilisée sur les lignes planning du projet et les feuilles projet lorsque le compte général sera entré.

## <a name="to-set-up-job-posting-groups"></a>Pour configurer les groupes compta. projet
L'un des aspects des projets de planification est de décider quels comptes de validation utiliser pour l'évaluation du stock projet. Pour valider des projets, vous configurez des comptes afin de valider chaque groupe compta. projet. Un groupe comptabilisation représente un lien entre le projet et la manière dont il doit être traité dans la comptabilité. Lorsque vous créez un projet, vous pouvez spécifier un groupe comptabilisation et, par défaut, chaque tâche que vous créez pour le projet est associée avec ce groupe comptabilisation. Toutefois, lorsque vous créez des tâches, vous pouvez remplacer la valeur par défaut et sélectionner un groupe comptabilisation plus approprié.  

> [!NOTE]  
>   Les comptes nécessaires dans la table Plan comptable doivent être configurés avant de créer les groupes comptabilisation. Pour plus d'informations, reportez-vous à [Configuration ou modification du plan comptable](finance-setup-chart-accounts.md).  

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Groupes compta. projet**, puis choisissez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs du compte comme indiqué dans le tableau suivant.  

| Champ de compte | Désignation |
| --- | --- |
| **Code** |Un code pour le groupe comptabilisation. Vous pouvez entrer un maximum de 10 caractères, espaces compris. |
| **Compte dépenses TEC** |Compte TEC pour les dépenses calculées des TEC du projet, qui est un compte d'actif capital de bilan. |
| **Compte coûts à payer TEC** |Compte pour la méthode Valeur coût ou Coût des ventes du calcul TEC, qui est un compte de passif bilan de charge à payer. Validé lorsque l'ajustement TEC exige l'augmentation des coûts activité validés dans les comptes de gestion. |
| **Compte coûts lettrés projet** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés article** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés ressource** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte coûts lettrés** |Un compte de contrepartie du Compte dépenses TEC, qui est un compte de contrepartie de frais négatif. |
| **Compte ajustement coûts projet** |Compte de contrepartie du compte coûts à payer TEC, qui est un compte frais. |
| **Compte frais Général (budget)** |Le compte ventes qui sera utilisé pour les dépenses générales dans les tâches projet avec ce groupe comptabilisation. S'il n'est pas renseigné, le compte général entré sur la ligne planning projet est utilisé. |
| **Compte ventes à payer TEC** |Compte TEC pour la valeur des ventes calculée des TEC, qui est un compte de passif bilan. Validé lorsque l'ajustement TEC exige l'augmentation du revenu réceptionné. |
| **Compte ventes facturées TEC** |Compte pour la valeur des ventes facturées des TEC qui ne peuvent pas être réceptionnés. Il s'agit d'un compte bilan produit comptabilisé d'avance. |
| **Compte ventes lettrées projet** |Compte de contrepartie du Compte ventes facturées TEC, qui est un compte de contrepartie de revenu. |
| **Compte ajustement vente projet** |Compte de contrepartie du Compte ventes projet TEC, qui est un compte de revenu. |
| **Compte coûts récep.** |Compte frais contenant les coûts réceptionnés du projet. Il s'agit ordinairement d'un compte frais pour débit. |
| **Compte ventes récep.** |Compte de revenu contenant les revenus réceptionnés du projet. Il s'agit ordinairement d'un compte de revenu pour crédit. |

## <a name="see-also"></a>Voir aussi
[Configurer la gestion de projet](projects-setup-projects.md)  
[Gestion des projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

