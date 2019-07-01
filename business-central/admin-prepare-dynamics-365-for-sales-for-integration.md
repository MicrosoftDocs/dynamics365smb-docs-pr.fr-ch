---
title: Intégration de Dynamics 365 for Sales| Microsoft Docs
description: Découvrez comment préparer Dynamics 365 Business Central pour l'intégrer à Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: bbe5041f853af9d58149d446627b0b21fa0e0f12
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540261"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Intégration à Dynamics 365 for Sales
Le rôle de vendeur est souvent considéré comme tourné vers l'extérieur dans une entreprise. Toutefois, il peut être utile pour les vendeurs d'être en mesure de regarder à l'intérieur de l'entreprise et d'observer ce qu'il s'y passe en arrière-plan. En intégrant [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)], vous pouvez donner à vos vendeurs cet aperçu en leur permettant de visualiser les informations dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant qu'ils travaillent dans [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, dans le cadre de la préparation d'un devis, il peut s'avérer utile de savoir si vous avez suffisamment de stock pour répondre à la commande. Pour plus d'informations, reportez-vous à la rubrique [Utilisation de Dynamics 365 for Sales depuis Business Central](marketing-integrate-dynamicscrm.md)

> [!Note]
> Ces étapes décrivent le processus d'intégration des versions en ligne de [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Aperçu du processus d'intégration
Les étapes suivantes offrent un aperçu des étapes pour intégrer [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Ces tâches exigent le rôle de sécurité **Administrateur système** dans [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Dans le centre d'administration Office 365, configurez un compte d'utilisateur auquel se connecter et synchroniser les données avec [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, voir également [Configuration de l'intégration à Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Affectez les licences pour [!INCLUDE[crm_md](includes/crm_md.md)] aux utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui utiliseront les applications intégrées.

3. Configurez une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, voir [Configurer une connexion à Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. En option : couplez les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synchronisez les données entre les applications. Pour plus d'informations, voir la rubrique [Synchronisation de Business Central et de Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>À propos de la solution d'intégration Business Central
La solution permet aux individus de voir les informations dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant qu'ils travaillent dans [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, elle peut fournir des aperçus des statistiques client, elle permet aux utilisateurs de coupler et de visualiser des enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis [!INCLUDE[crm_md](includes/crm_md.md)], et permet aux personnes de voir quels produits sont disponibles dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Par défaut, le guide de configuration assistée Configurer la connexion Dynamics 365 for Sales importera la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour ce faire, le guide de configuration utilise un compte d'utilisateur d'administrateur. Ce compte doit être également un utilisateur valide dans [!INCLUDE[crm_md](includes/crm_md.md)] avec les rôles de sécurité suivants :

* Administrateur système  
* Personnalisateur de solution  

Pour en savoir plus, reportez-vous aux rubriques [Configuration des comptes d'utilisateur pour l'intégration à Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer les rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md), et [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).  

Ce compte est utilisé une seule fois lors de la configuration. Une fois la solution importée dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le compte n'est plus nécessaire. L'intégration continue à utiliser le compte d'utilisateur qui a été créé spécialement pour l'intégration.

Outre la personnalisation de [!INCLUDE[crm_md](includes/crm_md.md)], la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] crée également les rôles suivants dans [!INCLUDE[crm_md](includes/crm_md.md)] pour l'intégration :

* **Administrateur d'intégration** : permet aux utilisateurs de gérer la connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)]. Attribué généralement uniquement au compte d'utilisateur pour la synchronisation.  
* **Utilisateur d'intégration** : permet aux utilisateurs d'accéder aux données synchronisées. Généralement affecté au compte d'utilisateur pour synchronisation et tout autre utilisateur devant visualiser les données synchronisées ou y accéder.
* **Utilisateur de la disponibilité des produits** : permet aux utilisateurs de demander la disponibilité des produits dans [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis [!INCLUDE[crm_md](includes/crm_md.md)].

À la fin du guide d'installation, [!INCLUDE[d365fin](includes/d365fin_md.md)] vous invite à coupler les vendeurs aux utilisateurs dans [!INCLUDE[crm_md](includes/crm_md.md)]. Les enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)] ont généralement un propriétaire (utilisateur) assigné, et si le couplage entre l'utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] et le vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)] n'existe pas, la synchronisation connaîtra un échec. Vous pouvez également effectuer cette opération ultérieurement à l'aide de l'action **Coupler les vendeurs** sur la page **Configuration de la connexion Microsoft Dynamics 365**.

## <a name="see-also"></a>Voir aussi  
[Configuration des comptes d'utilisateur pour intégration à Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Synchronisation de Business Central et Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)