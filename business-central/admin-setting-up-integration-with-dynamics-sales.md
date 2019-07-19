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
ms.openlocfilehash: 0f59324e41695e35e09a2dd970492acb3a8dba58
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726897"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Configuration des comptes d'utilisateur pour intégration à Dynamics 365 for Sales
Cet article fournit un aperçu de la manière dont la configuration des comptes d'utilisateur requis pour intégrer [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Configuration du compte d'utilisateur de l'administrateur dans Sales
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

## <a name="minimum-permissions-for-user-accounts-in-includecrmmdincludescrmmdmd"></a>Autorisations minimales pour les comptes d'utilisateurs dans [!INCLUDE[crm_md](includes/crm_md.md)]
Lorsque vous installez la solution d'intégration, les autorisations pour le compte d'utilisateur de l'intégration sont configurées dans [!INCLUDE[crm_md](includes/crm_md.md)]. Si ces autorisations sont modifiées, vous devrez peut-être les réinitialiser. Vous pouvez le faire en réinstallant la solution d'intégration ou en la réinitialisant manuellement. Les tableaux suivants répertorient les autorisations minimales pour les comptes d’utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Administrateur d'intégration
Le tableau suivant affiche les autorisations minimales sur chaque onglet pour chaque rôle de sécurité requis pour l'utilisateur administrateur.

##### <a name="customization"></a>Personnalisation
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Application basée sur un modèle|Global|||Lire|
|Assemblage de plug-in|Global|Lire|Lire|Lire|
|Type de plug-in|Global|Lire|Lire|Lire|
|Relation|Global|||Lire|
|Message du SDK|Global|Lire|Lire|Lire|
|Étape de traitement des messages du SDK|Global|Lire|Lire|Lire|
|Image de l'étape de traitement des messages du SDK|Global|Lire|Lire|Lire|
|Système à partir de|Global|||Écrire|

##### <a name="custom-entities"></a>Entités personnalisées
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Statistiques du compte Business Central|Global|Lire|Lire|Lire|
|Connexion Business Central|Global|Créer, Lire, Écrire, Supprimer|Créer, Lire, Écrire, Supprimer|Créer, Lire, Écrire, Supprimer|
|Configuration de la comptabilisation|Global|||Écrire|

#### <a name="integration-user"></a>Utilisateur de l'intégration
Le tableau suivant affiche les autorisations minimales sur chaque onglet pour chaque rôle de sécurité requis pour l'utilisateur de l'intégration.

##### <a name="core-records"></a>Dossiers de base
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Compte|Global|Créer, Lire, Écrire, Ajouter, Ajouter à, Attribuer|Créer, Lire, Écrire, Ajouter, Ajouter à, Attribuer|Créer, Lire, Écrire, Ajouter, Ajouter à, Attribuer|
|Carte d'action|Global||Lire|Lire|
|Connexion|Global|Lire|Lire|Lire|
|Contact|Global|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|
|Noter|Global|||Créer, Lire, Écrire, Supprimer, Ajouter, Attribuer|
|Opportunité|Global||Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|
|Comptabilisation|Global|||Créer, Lire, Ajouter à|
|Interface utilisateur de l'entité utilisateur|Utilisateur|Créer, Lire, Écrire|Créer, Lire, Écrire|Créer, Lire, Écrire|

##### <a name="sales"></a>Ventes
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Facturer|Global|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|
|Commande|Global|Lire, Écrire, Ajouter à|Lire, Écrire, Ajouter à|Lire, Écrire, Ajouter, Ajouter à, Attribuer|
|Produit|Global|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|
|Propriété|Global|Lire|Lire|Lire|
|Association de la propriété|Global|Lire|Lire|Lire|
|Propriété Option - Définir l'élément|Global|Lire|Lire|Lire|
|Devis|Global|Lire|Lire|Lire|

##### <a name="service"></a>Service
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Incident|Global|Lire|Lire|Lire|

##### <a name="business-management"></a>Gestion d'activité
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Devise|Global|Créer, Lire, Écrire|Créer, Lire, Écrire|Créer, Lire, Écrire|
|Organisation|Global|Lire, Écrire|Lire, Écrire|Lire, Écrire|
|Rôle de sécurité|Global|||Lire|
|Utilisateur|Global|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|Créer, Lire, Écrire, Ajouter, Ajouter à|
|Paramètres utilisateur|Global|Créer, Lire, Écrire, Supprimer, Ajouter à|Créer, Lire, Écrire, Supprimer, Ajouter à|Créer, Lire, Écrire, Supprimer, Ajouter à|
|Agir au nom d'un autre utilisateur|Global|Oui|Oui|Oui|

##### <a name="customization"></a>Personnalisation
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Champ|Global||Lire|Lire|
|Assemblage de plug-in|Global|Lire|Lire|Lire|
|Type de plug-in|Global|Lire|Lire|Lire|
|Message du SDK|Global|Lire|Lire|Lire|
|Étape de traitement des messages du SDK|Global|Lire|Lire|Lire|
|Ressource Web|Global|Lire|Lire|Lire|

##### <a name="custom-entities"></a>Entités personnalisées
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Statistiques du compte Dynamics 365 Business Central|Global|Créer, Lire, Écrire, Ajouter à|Créer, Lire, Écrire, Ajouter à|Créer, Lire, Écrire, Ajouter à|
|Dynamics 365 Business Central Connexion|Global|Lire|Lire|Lire|

### <a name="product-availability-user"></a>Produit Disponibilité Utilisateur
Vous pouvez permettre aux commerciaux de visualiser les niveaux de stock des articles vendus en leur accordant les autorisations décrites dans le tableau suivant.

##### <a name="custom-entities"></a>Entités personnalisées
|Rôle de sécurité|Niveau d'accès|Dynamics NAV 2018 et versions antérieures|Business Central <br> Octobre 2018|Business Central <br> Avril 2019|
|----|----|-----|----|----|
|Statistiques du compte Dynamics 365 Business Central|Global|Créer, Lire, Écrire, Ajouter à|Créer, Lire, Écrire, Ajouter à|Créer, Lire, Écrire, Ajouter à|
|Dynamics 365 Business Central Connexion|Global|Lire|Lire|Lire|

## <a name="see-also"></a>Voir aussi  
[Intégration à Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
