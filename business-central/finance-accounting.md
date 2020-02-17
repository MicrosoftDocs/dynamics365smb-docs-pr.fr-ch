---
title: Expérience comptable dans Business Central | Microsoft Docs
description: En savoir plus sur le portail Comptable pour Business Central et le tableau de bord Comptable qui prend en charge les comptables internes et externes de la société du client.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/06/2020
ms.author: edupont
ms.openlocfilehash: 50cc4aba9f3a01b9518d974cf011de3b9b20a4da
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991871"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Expériences de comptable dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Chaque entreprise doit tenir ses comptes et valider sa comptabilité. Certaines sociétés utilisent un comptable externe, et d'autres ont un comptable dans le personnel. Peu importe le type de comptable que vous êtes, vous pouvez utiliser le tableau de bord **Comptable** comme pages d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)]. De là, vous pouvez accéder à toutes les pages nécessaires pour votre travail.  

## <a name="accountant-role-center"></a>Tableau de bord Comptable
Le tableau de bord est un tableau de bord avec des vignettes d'activité qui affichent des chiffres essentiels en temps réel et vous permettent d'accéder rapidement aux données. Dans le ruban en haut de la page, vous avez accès à plusieurs actions, par exemple ouvrir les états et les états financiers les plus couramment utilisés dans Excel. Dans la barre de navigation supérieure, vous pouvez rapidement basculer entre les listes que vous utilisez le plus fréquemment. Ici, vous pouvez visualiser d'autres éléments, tels que **Documents validés** avec divers types de documents que la société a validés.  

Si vous débutez avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez lancer une liste de vidéos depuis votre Tableau de bord. Vous pouvez également lancer une visite de **Mise en route** qui précise des domaines clé.  

## <a name="inviteaccountant"></a>Inviter votre comptable externe dans votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, votre administrateur peut l'inviter à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] afin qu'il puisse travailler avec vous sur vos données fiscales. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprend trois licences de type Comptable externe. Pour plus d'informations sur la gestion des licences, voir le [Guide des licences Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Une fois que votre comptable a accédé à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux pages les plus appropriées pour son travail.  

Nous avons simplifié pour vous la façon d'inviter votre comptable externe. Ouvrez simplement la page **Utilisateurs**, puis choisissez l'action **Inviter un comptable externe** dans le ruban. Un e-mail est préparé pour vous afin de vous permettre d'ajouter l'e-mail professionnel de votre comptable et d'envoyer l'invitation.  

> [!Note]  
> Pour cela, il faudrait que vous ayez configuré la messagerie SMTP. Pour plus d'informations, voir [Configurer la messagerie](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> L'adresse électronique du comptable doit être une adresse professionnelle basée sur Azure Active Directory. Si le comptable utilise un autre type d'adresse électronique, l'invitation ne peut pas être envoyée. 
> 
> Comme cette tâche nécessite un accès à la gestion des utilisateurs et des licences dans Azure Active Directory, l'utilisateur qui envoie cette invitation doit se voir attribuer le rôle **Administrateur global** ou le rôle **Administrateur utilisateur** dans le centre d'administration Office 365. Pour plus d'informations, voir [À propos des rôles d'administrateur](/office365/admin/add-users/about-admin-roles) dans le centre d'administration Office 365.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Ajout de votre comptable à votre Office 365 via le Portail Azure

Si votre administrateur ou partenaire revendeur ne souhaite pas utiliser le guide **Inviter un comptable externe**, il peut ajouter un utilisateur externe dans le Portail Azure et attribuer à cet utilisateur la licence Comptable externe. Pour plus d'informations, voir [Démarrage rapide : Ajouter des utilisateurs invités à votre annuaire dans le portail Azure](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Pour ajouter votre comptable en tant qu'utilisateur invité

1. Ouvrez le [Portail Azure](https://portal.azure.com/).
2. Dans le volet gauche, sélectionnez **Azure Active Directory**.
3. Sous **Gérer**, sélectionnez **Utilisateurs**.
4. Sélectionnez **Nouvel utilisateur invité**.
5. Sur la page **Nouvel utilisateur**, sélectionnez **Inviter un utilisateur**, puis ajoutez des informations sur votre comptable externe.  

   Vous pouvez éventuellement inclure un message de bienvenue personnel à l'attention du comptable pour l'informer que vous l'ajoutez à votre [!INCLUDE [prodshort](includes/prodshort.md)].

6. Sélectionner **Inviter** pour envoyer automatiquement l'invitation. Une notification apparaît en haut à droite avec le message **Utilisateur invité avec succès**. 
7. Après avoir envoyé l'invitation, le compte utilisateur est automatiquement ajouté au répertoire en tant qu'invité.

Ensuite, vous devez attribuer au nouvel utilisateur invité une licence pour [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-include-prodshortincludesprodshortmd"></a>Pour donner à votre comptable accès à votre [!INCLUDE [prodshort](includes/prodshort.md)]

1. Dans le Portail Azure, pour le nouvel utilisateur ajouté, choisissez **Profil**, puis **Modifier**
2. Mettez à jour le champ **Lieu d'utilisation** et indiquez le pays concerné, puis choisissez **Enregistrer**.
3. Choisissez **Licences**, puis ouvrez **Affectations**.
4. Choisissez la licence **Comptable externe Dynamics 365 Business Central**.  

    Si cette licence n'est pas disponible, vous devez utiliser une licence **Dynamics 365 Business Central pour IWs** à la place.
5. Enregistrez l'affectation.

En cas de réussite, la licence est attribuée à l'utilisateur invité et le compte invité est créé.

### <a name="importing-the-new-user-into-include-prodshortincludesprodshortmd"></a>Importation du nouvel utilisateur dans [!INCLUDE [prodshort](includes/prodshort.md)]

Le comptable recevra un e-mail l'informant qu'on lui a accordé l'accès à votre Active Directory. Ensuite, vous devez lui donner accès à la bonne société dans [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Pour ajouter le comptable à la bonne société

1. Ouvrez la société [!INCLUDE [prodshort](includes/prodshort.md)] à laquelle vous souhaitez donner accès au comptable sur [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Utilisateurs**, puis sélectionnez le lien associé.  
3. Choisissez l'action **Obtenir de nouveaux utilisateurs à partir de Office 365**.

Cela a pour effet d'importer dans la société le compte utilisateur que vous avez créé dans le portail Azure. Pour plus d'informations, voir [Pour ajouter un utilisateur dans Business Central](ui-how-users-permissions.md#to-add-a-user-in-business-central).  

Si vous souhaitez donner accès à plusieurs sociétés, vous devez vous connecter à chaque société et répéter ce processus. Vous pouvez également mettre à jour les groupes d'autorisations pour le profil utilisateur du comptable dans [!INCLUDE [prodshort](includes/prodshort.md)], par exemple en lui attribuant le groupe d'utilisateurs *D365 Bus Premium*. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

## <a name="accountant-hub"></a>Accountant Hub

Si vous êtes un comptable avec plusieurs clients, vous pouvez utiliser [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] pour un meilleur aperçu de vos clients. Depuis cette fenêtre, vous pouvez accéder à l'abonné de chaque client dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et utiliser le tableau de bord Comptable comme décrit ci-dessus. Pour en savoir plus, voir [Bienvenue dans [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] est actuellement en version préliminaire publique sur un nombre limité de marchés.

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Analyse des états financiers dans Excel](finance-analyze-excel.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Configuration d'une analyse de trésorerie](finance-setup-cash-flow-analyses.md)  
[Bienvenue dans [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub sur Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
