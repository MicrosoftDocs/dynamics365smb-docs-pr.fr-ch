---
title: Configuration des comptes d'utilisateur pour l'intégration à Dynamics 365 for Sales | Microsoft Docs
description: Découvrez comment configurer les comptes d'utilisateur que les applications utilisent pour échanger les données, et que les utilisateurs emploient pour accéder aux données et les synchroniser dans les applications.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3163389cb0818133fba9ab8c55b8d0cf662130f1
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620968"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Configuration des comptes d'utilisateur pour intégration à Dynamics 365 for Sales
Cet article fournit un aperçu de la manière dont la configuration des comptes d'utilisateur requis pour intégrer [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Configuration du compte d'utilisateur de l'administrateur dans Sales
Vous devez ajouter votre compte d'utilisateur d'administrateur pour [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)], puis promouvoir l'utilisateur en tant qu'administrateur dans [!INCLUDE[crm_md](includes/crm_md.md)]. Le compte d'utilisateur d'administrateur doit également avoir le rôle Personnalisateur du système et au moins un autre rôle d'utilisateur non-administratif, tel que Directeur des ventes dans [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Configuration du compte d'utilisateur pour l'intégration
Vous devez créer un compte d'utilisateur dédié dans votre abonnement Office 365 que [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] peuvent utiliser pour synchroniser les données. Ce compte utilisateur doit pouvoir se connecter à [!INCLUDE[crm_md](includes/crm_md.md)], ce qui signifie que cet utilisateur doit avoir une licence pour [!INCLUDE[crm_md](includes/crm_md.md)] et au moins un rôle de sécurité doit lui être affecté dans [!INCLUDE[crm_md](includes/crm_md.md)], comme décrit [ici](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Pour en savoir plus sur la manière de créer des utilisateurs dans [!INCLUDE[crm_md](includes/crm_md.md)], reportez-vous à la rubrique [Gérer la sécurité, les utilisateurs et les équipes](http://go.microsoft.com/fwlink/?LinkID=616518). Une fois la connexion configurée, [!INCLUDE[d365fin](includes/d365fin_md.md)] affectera au compte utilisateur les rôles de sécurité nécessaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et ce compte peut être défini sur le [mode d'accès non interactif](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) dans [!INCLUDE[crm_md](includes/crm_md.md)]

![Guide de configuration assistée présentant l'espace pour saisir les identifiants d'utilisateur de synchronisation](media/sync-user-setup.png "Page de l'assistant de configuration assistée de visualisation présentant l'espace pour saisir les identifiants d'utilisateur de synchronisation")

> [!IMPORTANT]  
> N'utilisez pas le compte administrateur pour la synchronisation [!INCLUDE[crm_md](includes/crm_md.md)]. Cela interromprait la synchronisation.
> En outre, pour éviter une synchronisation constante, les modifications apportées aux données par le compte d'utilisateur d'intégration ne sont pas synchronisées. <!--What changes would this account make?--> Une fois la connexion établie, nous recommandons de définir le mode d'accès pour le compte d'utilisateur pour l'intégration au mode non interactif dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, reportez-vous à la rubrique [Créer un compte d'utilisateur non interactif](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Configuration des comptes pour les vendeurs
Vous devez créer des comptes d'utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] pour les vendeurs depuis [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour simplifier les choses, le Centre d'administration Microsoft 365 propose un modèle Excel à utiliser. Sur la page **Utilisateurs actifs**, sélectionnez **Plus**, puis **Importer plusieurs utilisateurs**. Sélectionnez **Télécharger un fichier CSV avec des en-têtes uniquement**, puis saisissez les informations pour les vendeurs. En guise d'exemple, sélectionnez **Télécharger un fichier CSV avec des en-têtes et des exemples d'informations d'utilisateur**. Après la saisie des informations concernant les utilisateurs, la prochaine étape du processus d'importation consiste à attribuer les licences d'utilisateur au plan Dynamics 365 Customer Engagement.  

Après l'importation des utilisateurs et l'attribution de licences pour Dynamics 365 Customer Engagement, vous devez affecter les utilisateurs au rôle **Vendeur** dans [!INCLUDE[crm_md](includes/crm_md.md)].

![Couplage de vendeurs aux utilisateurs dans Dynamics 365 for Sales](media/couple-salespeople.png "Visualisation du couplage des vendeurs aux utilisateurs dans Dynamics 365 for Sales")

## <a name="see-also"></a>Voir aussi  
[Intégration à Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
