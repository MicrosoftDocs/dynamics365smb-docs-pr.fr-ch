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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896148"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Expériences de comptable dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Chaque entreprise doit tenir ses comptes et valider sa comptabilité. Certaines sociétés utilisent un comptable externe, et d'autres ont un comptable dans le personnel. Peu importe le type de comptable que vous êtes, vous pouvez utiliser le tableau de bord **Comptable** comme pages d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)]. De là, vous pouvez accéder à toutes les pages nécessaires pour votre travail.  

## <a name="accountant-role-center"></a>Tableau de bord Comptable
Le tableau de bord est un tableau de bord avec des vignettes d'activité qui affichent des chiffres essentiels en temps réel et vous permettent d'accéder rapidement aux données. Dans le ruban en haut de la page, vous avez accès à plusieurs actions, par exemple ouvrir les états et les états financiers les plus couramment utilisés dans Excel. Dans la barre de navigation supérieure, vous pouvez rapidement basculer entre les listes que vous utilisez le plus fréquemment. Ici, vous pouvez visualiser d'autres éléments, tels que **Documents validés** avec divers types de documents que la société a validés.  

Si vous débutez avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez lancer une liste de vidéos depuis votre Tableau de bord. Vous pouvez également lancer une visite de **Mise en route** qui précise des domaines clé.  

## <a name="inviteaccountant"></a>Inviter votre comptable externe dans votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] afin qu'ils puissent travailler vous et utiliser vos données fiscales.

Une fois que votre comptable a accédé à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux pages les plus appropriées pour son travail.  

Nous avons simplifié pour vous la façon d'inviter votre comptable externe. Ouvrez simplement la page **Utilisateurs**, puis choisissez l'action **Inviter un comptable externe** dans le ruban. Un e-mail est préparé pour vous afin de vous permettre d'ajouter l'e-mail professionnel de votre comptable et d'envoyer l'invitation.  
> [!Note]  
> Pour cela, il faudrait que vous ayez configuré la messagerie SMTP. Pour plus d'informations, voir [Configurer la messagerie](admin-how-setup-email.md).   

![Inviter votre comptable](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> L'adresse électronique du comptable doit être une adresse professionnelle basée sur Azure Active Directory. Si le comptable utilise un autre type d'adresse électronique, l'invitation ne peut pas être envoyée.  

### <a name="behind-the-scenes"></a>En arrière-plan
[!INCLUDE[d365fin](includes/d365fin_md.md)] comprend trois licences de type Comptable externe. Si votre société utilise un comptable externe, vous pouvez autoriser l'accès à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] en lui attribuant cette licence. Pour plus d'informations sur les licences, voir le [Guide des licences Microsoft Dynamics 365 Busincess Central](https://go.microsoft.com/fwlink/?LinkId=871590). 

Si une licence est toujours disponible dans votre abonnement, votre administrateur ou votre partenaire revendeur peut ajouter un utilisateur externe via le portail Azure et attribuer à cet utilisateur la licence Comptable externe. Pour plus d'informations, voir [Ajouter des utilisateurs de collaboration B2B Azure Active Directory dans le portail Azure](/azure/active-directory/b2b/add-users-administrator).

Vous pouvez ensuite inviter le comptable depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] en utilisant le guide de configuration assistée **Inviter un comptable externe**. Cependant, comme cette tâche nécessite un accès à la gestion des utilisateurs et des licences dans Azure Active Directory, le rôle **Administrateur global** ou le rôle **Administrateur utilisateur** doit être attribué à l'utilisateur qui envoie cette invitation dans le centre d'administration Office 365. Pour plus d'informations, voir [À propos des rôles d'administrateur](/office365/admin/add-users/about-admin-roles) dans le centre d'administration Office 365. 

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
