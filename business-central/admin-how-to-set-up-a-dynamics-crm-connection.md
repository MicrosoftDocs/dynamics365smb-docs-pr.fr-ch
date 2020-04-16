---
title: Se connecter à Dynamics 365 Sales | Microsoft Docs
description: Vous pouvez intégrer d'autres applications à Business Central au moyen de Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196654"
---
# <a name="connect-to-common-data-service"></a>Se connecter à Common Data Service
Cette rubrique décrit comment configurer une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)]. En règle générale, les entreprises créent la connexion pour intégrer et synchroniser des données avec une autre application métier Dynamics 365 telle que [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Avant de commencer
Avant de créer la connexion, quelques informations doivent être préparées :  

* L'URL pour l’environnement [!INCLUDE[d365fin](includes/cds_long_md.md)] auquel vous souhaitez vous connecter. Si vous utilisez le guide de configuration assistée **Paramétrage de la connexion CDS** pour créer la connexion, nous découvrirons vos environnements, mais vous pouvez également saisir l'URL d'un autre environnement dans votre abonné.  
* Un nom d'utilisateur et un mot de passe d'un compte utilisateur utilisés uniquement pour l'intégration. Ce compte est appelé le compte « d'utilisateur d'intégration ». 
* Le nom d'utilisateur et le mot de passe d'un compte ayant les autorisations administrateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Ces étapes décrivent la procédure pour la version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Configurer une connexion vers [!INCLUDE[d365fin](includes/cds_long_md.md)]  
Pour tous les types d'authentification autres que l'authentification Office 365, configurez votre connexion à [!INCLUDE[d365fin](includes/cds_long_md.md)] sur la page **Paramétrage de la connexion CDS**. Pour l'authentication Office 365, il est recommandé d'utiliser le guide de configuration assistée **Paramétrage de la connexion CDS**. Le guide facilite la configuration de la connexion et spécifie les fonctions avancées telles que le couplage entre les enregistrements.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Pour utiliser le guide de configuration assistée Paramétrage de la connexion CDS 
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration assistée**, puis sélectionnez le lien associé.
2. Sélectionnez **Configurer la connexion à l'intégration de base CDS** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.

> [!Note]
> Le guide de configuration assistée **Paramétrage de la connexion CDS** affecte automatiquement les rôles de sécurité **Administrateur d'intégration** et **Utilisateur d'intégration** au compte d'utilisateur utilisé pour l'intégration et définit le mode d'accès du compte sur **non interactif**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Pour créer ou conserver manuellement la connexion
La procédure suivante décrit comment configurer manuellement la connexion sur la page **Paramétrage de la connexion CDS**. Il s'agit également de la page sur laquelle vous gérez les paramètres pour l'intégration.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage de la connexion CDS**, puis sélectionnez le lien associé.
2. Saisissez les informations suivantes pour la connexion de [!INCLUDE[d365fin](includes/cds_long_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Champ|Description|
|-----|-----|
|**URL Environnement**|Si vous possédez des environnements dans [!INCLUDE[d365fin](includes/cds_long_md.md)], nous les trouverons lorsque vous exécuterez le guide de configuration. Si vous souhaitez vous connecter à un autre environnement dans un autre abonné, vous pouvez saisir les informations d'identification administrateur pour l'environnement et nous les découvrirons. |
|**Nom d'utilisateur** et **Mot de passe**|Il s'agit des informations d'identification du compte d'utilisateur dédié à l'intégration. Pour en savoir plus, reportez-vous à la rubrique [Configuration des comptes d'utilisateur pour l'intégration à [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Activé**|Commencez avec l'intégration. Si vous n'activez pas la connexion tout de suite, les paramètres de connexion seront sauvegardés, mais les utilisateurs ne seront pas en mesure d'accéder aux données [!INCLUDE[d365fin](includes/cds_long_md.md)] à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous pouvez revenir sur cette page et activer la connexion ultérieurement.  |

3. Dans le champ **Modèle de propriété**, choisissez si vous souhaitez une entité Équipe dans [!INCLUDE[d365fin](includes/cds_long_md.md)] pour posséder de nouveaux enregistrements, ou un ou plusieurs utilisateurs spécifiques. Si vous choisissez **Personne**, vous devez indiquer chaque utilisateur. Si vous choisissez **Équipe**, le centre de profit par défaut BCI_Company s'affiche dans le champ **Centre de profit couplé**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Pour tester les paramètres de connexion, choisissez **Connexion**, puis **Tester la connexion**.  

    > [!NOTE]  
    >  Si le chiffrement des données n'est pas activé dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous recevrez un message vous demandant si vous souhaitez l'activer. Pour activer le chiffrement des données, cliquez sur **Oui** et fournissez les informations requises. Sinon, sélectionnez **Non**. Vous pouvez activer le chiffrement des données ultérieurement. Pour plus d'informations, voir [Chiffrement des données dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) de l'aide sur Developer and IT Pro.  

5. Si la synchronisation de [!INCLUDE[d365fin](includes/cds_long_md.md)] n'est pas déjà configurée, vous recevrez un message vous demandant si vous souhaitez utiliser les paramètres de synchronisation par défaut. Selon que vous souhaitez conserver ou non les enregistrements alignés dans [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez **Oui** ou **Non**.

> [!Note]
> La connexion à [!INCLUDE[d365fin](includes/cds_long_md.md)] à l'aide de la page **Paramétrage de la connexion CDS** peut nécessiter que vous affectiez les rôles de sécurité Administrateur d'intégration et Utilisateur d'intégration au compte utilisé pour l'intégration dans Dynamics 365 Sales. Pour plus d'informations, voir [Attribuer un rôle de sécurité à un utilisateur](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Pour se déconnecter de [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage de la connexion CDS**, puis sélectionnez le lien associé.
2. Sur la page **Paramétrage de la connexion CDS**, désactivez le bouton bascule **Activé**.  

## <a name="see-also"></a>Voir aussi  
[Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md)  
