---
title: Modifier les fonctionnalités affichées
description: 'En savoir plus sur ce que signifie le niveau d’expérience Essentiel et Premium pour l’interface utilisateur, les domaines d’application, et votre société.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: 1
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="change-which-features-are-displayed"></a>Modifier les fonctionnalités affichées
[!INCLUDE[prod_short](includes/prod_short.md)] est conçu pour vous aider à gérer votre entreprise indépendamment de sa taille et de sa complexité. Au cœur du produit, vous trouverez des fonctionnalités essentielles, telles que la génération d’états financiers, les ventes, les achats et la gestion des stocks. À mesure que la complexité de l’entreprise augmente, vous pouvez activer des fonctionnalités pour la fabrication et la gestion des services, par exemple.

Vous pouvez définir le niveau de complexité du produit, et donc les fonctionnalités auxquelles les utilisateurs de la société ont accès, en modifiant le paramètre **Expérience** sur la page **Informations société**. Notez que le paramètre d’expérience peut également être modifié par l’ajout de certaines extensions provenant d’AppSource. Pour plus d’informations, voir [Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md).

Le tableau suivant répertorie les expériences actuellement disponibles.

| Expérience | Impact sur l’interface utilisateur |
| --- | --- |
| **Essential** |Affiche tous les champs et actions pour toutes les fonctionnalités d’entreprise communes.|
| **Premium** |Affiche tous les champs et actions pour toutes les fonctionnalités d’entreprise, y compris la fabrication et la gestion des services.|

Les expériences qui peuvent être sélectionnées dans [!INCLUDE[prod_short](includes/prod_short.md)] reflètent les licences de la solution, appelées plans, définies pour le produit. Pour plus d’informations sur les abonnements Essentiel et Premium, voir [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) sur le site Microsoft Dynamics 365 Marketing. Consultez également le [Guide des licences [!INCLUDE[prod_short](includes/prod_short.md)]](https://go.microsoft.com/fwlink/?linkid=2068931).

> [!IMPORTANT]  
> Tous les utilisateurs réguliers d’une solution doivent avoir le même plan, Essential ou Premium, pour pouvoir sélectionner l’expérience pour la société. En conséquence, un utilisateur ne peut pas accéder aux fonctionnalités Premium si un ou plusieurs autres utilisateurs peuvent uniquement accéder aux fonctionnalités Essential. Ce n’est pas le cas pour les utilisateurs non réguliers du type Membre de l’équipe, Administrateur interne, Comptable externe et Administrateur délégué, qui peuvent avoir un plan différent de celui des autres utilisateurs de la solution.<br /><br /> Seuls les utilisateurs de type Evaluation ou Premium peuvent modifier la valeur du champ **Expérience** d’Essential en Premium.

Avant de définir les paramètres d’expérience d’une société, vous devez définir l’accès des utilisateurs à des fonctions et à des pages spécifiques en affectant des ensembles d’autorisations. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

Le paramètre **Expérience** s’applique à tous les utilisateurs d’une société, mais chaque utilisateur peut personnaliser davantage sa propre expérience en modifiant la mise en page et le contenu. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Activation des fonctionnalités Premium après mise à niveau d’un plan
Les utilisateurs sont affectés à des plans dans le centre d’administration Microsoft 365 dans le cadre de la tâche générale de création des utilisateurs Business Central. Pour plus d’informations, consultez [Ajouter des utilisateurs et attribuer des licences en simultané](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Pour mettre à jour les modifications de plan des groupes d’utilisateurs

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Si vous avez modifié les plans des utilisateurs dans le centre d’administration Microsoft 365, par exemple en affectant plus d’utilisateurs au plan Premium, vous devez mettre à jour [!INCLUDE[prod_short](includes/prod_short.md)] pour refléter les modifications.

1. Connectez-vous en tant qu’administrateur.
2. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis choisissez le lien associé.
3. Sur la page **Utilisateurs**, choisissez l’action **Mettre à jour les utilisateurs depuis Microsoft 365**.

### <a name="to-select-the-premium-experience"></a>Pour sélectionner l’expérience Premium
Vous pouvez maintenant sélectionner la nouvelle expérience.
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Informations société**, puis choisissez le lien associé.
2. Sur la page **Informations société**, dans le raccourci **Expérience utilisateur**, sélectionnez Premium dans le champ **Expérience**.

## <a name="help-assumes-premium-experience"></a>L’aide implique l’expérience Premium
Tous les descriptions de fonctions de la documentation utilisateur de [!INCLUDE[prod_short](includes/prod_short.md)] assument l’expérience **Premium**, ce qui signifie que les descriptions couvrent la portée complète des éléments de l’interface utilisateur.

## <a name="see-also"></a>Voir aussi
[Personnaliser votre espace de travail](ui-personalization-user.md)  
[Personnalisation de Business Central](ui-customizing-overview.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Création de sociétés](about-new-company.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Guide des licences [!INCLUDE[prod_short](includes/prod_short.md)]](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
