---
title: "Ajouter votre comptable externe à votre Financials | Microsoft Docs"
description: "Découvrez comment vous pouvez inviter votre comptable externe à votre Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fde920f4626079d66f285f366114d10807e7821b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitation de votre comptable externe à votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] afin qu'ils puissent travailler vous et utiliser vos données fiscales.

Une fois que votre comptable a accédé à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux fenêtres les plus appropriées pour son travail.  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Inviter votre comptable à votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Dans la dernière version de [!INCLUDE[d365fin](includes/d365fin_md.md)], nous avons simplifié pour vous la façon d'inviter votre comptable externe. Ouvrez simplement la fenêtre **Utilisateurs**, puis choisissez l'action **Inviter un comptable externe** dans le ruban. Un e-mail est préparé pour vous afin de vous permettre d'ajouter l'e-mail professionnel de votre comptable et d'envoyer l'invitation.  

![Inviter votre comptable](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Pour cela, il faudrait que vous ayez configuré la messagerie SMTP. Vous pouvez le faire manuellement ou demander à votre partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)]. En outre, vous devez être connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'administrateur utilisateur, pas en tant que chef d'entreprise ou autres utilisateurs. Enfin, vous devez avoir quitté la société test de sorte que vous ayez un administrateur Azure Active Directory.  

> [!IMPORTANT]  
>  L'adresse électronique du comptable doit être une adresse professionnelle basée sur Active Directory. Si le comptable utilise un autre type d'adresse électronique, l'invitation ne peut pas être envoyée.  

### <a name="separate-license"></a>Séparer la licence
En arrière-plan, le comptable est ajouté à votre abonné Active Directory. Votre administrateur peut vérifier que le comptable accepte l'invitation et que la licence correcte lui est attribuée. Pour cela la procédure dépend du type de compte que vous avez utilisé pour lorsque vous vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette rubrique est basée sur l'utilisation d'un compte Office 365, qui utilise Microsoft Azure Active Directory.  

Si vous avez activé votre abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)] et que vous n'utilisez plus la société d'évaluation, vous avez un abonné Azure Active Directory. Votre administrateur ou partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)] gère cet abonné dans le [Portail Azure](https://portal.azure.com). C'est là que de nouveaux utilisateurs sont ajoutés et que des licences sont appliquées et supprimées. Pour plus d'informations, voir [.Présentation du portail Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview)  

L'un des types de licence de [!INCLUDE[d365fin](includes/d365fin_md.md)] est la licence *Comptable externe*. Ce type de licence est prévu pour les utilisateurs comme les comptables externes. Cela signifie que vous ne devez pas acheter un poste supplémentaire dans votre Active Directory actuel ou utiliser l'un de vos comptes [!INCLUDE[d365fin](includes/d365fin_md.md)] utilisateur existants pour votre comptable externe. Par exemple, si votre abonnement actuel à Office 365 inclut 10 utilisateurs pour [!INCLUDE[d365fin](includes/d365fin_md.md)], et que vous utilisez actuellement 10 licences *Utilisateur complet*, votre administrateur peut simplement ajouter votre comptable externe en tant qu'utilisateur invité dans le portail Azure et affecter à cet utilisateur la licence *Comptable externe* sans coût supplémentaire. Cependant, vous ne pouvez avoir qu'un utilisateur avec la licence *Aide-comptable externe*. Si vous souhaitez ajouter des utilisateurs supplémentaires, vous devez mettre à jour votre abonnement à Office 365 en conséquence.  

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Paramétrer la messagerie manuellement ou à l'aide de la configuration assistée](madeira-how-setup-email.md)  
[Expériences de comptable dans Finance and Operations, Business edition ](finance-accounting.md)  
[Finance and Operations, Business edition pour comptables sur Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

