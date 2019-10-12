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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 79ed5e1b7200a668be2aa078531fd68e0131b6ff
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302611"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Expériences de comptable dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Chaque entreprise doit tenir ses comptes et valider sa comptabilité. Certaines sociétés utilisent un comptable externe, et d'autres ont un comptable dans le personnel. Peu importe le type de comptable que vous êtes, vous pouvez utiliser le tableau de bord **Comptable** comme pages d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)]. De là, vous pouvez accéder à toutes les pages nécessaires pour votre travail.  

## <a name="accountant-role-center"></a>Tableau de bord Comptable
Le tableau de bord est un tableau de bord avec des vignettes d'activité qui affichent des chiffres essentiels en temps réel et vous permettent d'accéder rapidement aux données. Dans le ruban en haut de la page, vous avez accès à plusieurs actions, par exemple ouvrir les états et les états financiers les plus couramment utilisés dans Excel. Dans la barre de navigation supérieure, vous pouvez rapidement basculer entre les listes que vous utilisez le plus fréquemment. Ici, vous pouvez visualiser d'autres éléments, tels que **Documents validés** avec divers types de documents que la société a validés.  

Si vous débutez avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez lancer une liste de vidéos depuis votre Tableau de bord. Vous pouvez également lancer une visite de **Mise en route** qui précise des domaines clé.  

## <a name="accountant-hub"></a>Accountant Hub
Si vous êtes un comptable avec plusieurs clients, vous pouvez utiliser [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] pour un meilleur aperçu de vos clients. Depuis cette fenêtre, vous pouvez accéder à l'abonné de chaque client dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et utiliser le tableau de bord Comptable comme décrit ci-dessus. Pour en savoir plus, voir [Bienvenue dans [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] est actuellement en version préliminaire publique sur un nombre limité de marchés.

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365fin_mdmd"></a>Invitation de votre comptable externe à votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] afin qu'ils puissent travailler vous et utiliser vos données fiscales.

Une fois que votre comptable a accédé à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux pages les plus appropriées pour son travail.  

Nous avons simplifié pour vous la façon d'inviter votre comptable externe. Ouvrez simplement la page **Utilisateurs**, puis choisissez l'action **Inviter un comptable externe** dans le ruban. Un e-mail est préparé pour vous afin de vous permettre d'ajouter l'e-mail professionnel de votre comptable et d'envoyer l'invitation.  

![Inviter votre comptable](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
> Pour cela, il faudrait que vous ayez configuré la messagerie SMTP. Vous pouvez le faire manuellement ou demander à votre partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)]. En outre, vous devez être connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'administrateur utilisateur, pas en tant que chef d'entreprise ou autres utilisateurs. Enfin, vous devez avoir quitté la société test de sorte que vous ayez un administrateur Azure Active Directory.  

> [!IMPORTANT]  
> L'adresse électronique du comptable doit être une adresse professionnelle basée sur Azure Active Directory. Si le comptable utilise un autre type d'adresse électronique, l'invitation ne peut pas être envoyée.  

### <a name="separate-license"></a>Séparer la licence
En arrière-plan, le comptable est ajouté à votre abonné Active Directory. Votre administrateur peut vérifier que le comptable accepte l'invitation et que la licence correcte lui est attribuée. Pour cela la procédure dépend du type de compte que vous avez utilisé pour lorsque vous vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette rubrique est basée sur l'utilisation d'un compte Office 365, qui utilise Microsoft Azure Active Directory.  

Si vous avez activé votre abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)] et que vous n'utilisez plus la société d'évaluation, vous avez un abonné Azure Active Directory. Votre administrateur ou partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)] gère cet abonné dans le [Portail Azure](https://portal.azure.com). C'est là que de nouveaux utilisateurs sont ajoutés et que des licences sont appliquées et supprimées. Pour plus d'informations, reportez-vous à la [présentation du portail Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

L'un des types de licence de [!INCLUDE[d365fin](includes/d365fin_md.md)] est la licence *Comptable externe*. Ce type de licence est prévu pour les utilisateurs comme les comptables externes. Cela signifie que vous ne devez pas acheter un poste supplémentaire dans votre Active Directory actuel ou utiliser l'un de vos comptes [!INCLUDE[d365fin](includes/d365fin_md.md)] utilisateur existants pour votre comptable externe. Par exemple, si votre abonnement actuel à Office 365 inclut 10 utilisateurs pour [!INCLUDE[d365fin](includes/d365fin_md.md)], et que vous utilisez actuellement 10 licences *Utilisateur complet*, votre administrateur peut simplement ajouter votre comptable externe en tant qu'utilisateur invité dans le portail Azure et affecter à cet utilisateur la licence *Comptable externe* sans coût supplémentaire. Cependant, vous ne pouvez avoir qu'un utilisateur avec la licence *Aide-comptable externe*. Si vous souhaitez ajouter des utilisateurs supplémentaires, vous devez mettre à jour votre abonnement à Office 365 en conséquence.

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
[Dynamics 365 - Accountant Hub sur Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
