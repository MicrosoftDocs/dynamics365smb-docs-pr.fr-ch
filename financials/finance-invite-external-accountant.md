---
title: "Ajouter votre comptable externe à votre Financials | Microsoft Docs"
description: "Découvrez comment vous pouvez inviter votre comptable externe à votre Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Inviter votre comptable externe à votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter à votre [!INCLUDE[d365fin](includes/d365fin_md.md)] afin qu'ils puissent travailler vous et utiliser vos données fiscales.

Une fois que votre comptable a accédé à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux fenêtres les plus appropriées pour son travail.  

> [!NOTE]  
>  Cette fonctionnalité nécessite que l'expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience Financials](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Inviter votre comptable à votre [!INCLUDE[d365fin](includes/d365fin_md.md)]
Dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)], pour inviter votre comptable externe vous avez besoin d'un administrateur pour l'ajouter à votre abonné Active Directory. Pour cela la procédure dépend du type de compte que vous avez utilisé pour lorsque vous vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette rubrique est basée sur l'utilisation d'un compte Office 365, qui utilise Microsoft Azure Active Directory.  

> [!TIP]  
>  Nous vous recommandons de contacter votre partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)] pour obtenir de l'aide.  

Si vous avez activé votre abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)] et que vous n'utilisez plus la société d'évaluation, vous avez un abonné Azure Active Directory. Votre administrateur ou partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)] gère cet abonné dans le [Portail Azure](https://portal.azure.com). C'est là que de nouveaux utilisateurs sont ajoutés et que des licences sont appliquées et supprimées. Pour plus d'informations, voir [.Présentation du portail Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview)  

### <a name="separate-license"></a>Séparer la licence
L'un des types de licence de [!INCLUDE[d365fin](includes/d365fin_md.md)] est la licence *Comptable externe*. Ce type de licence est prévu pour les utilisateurs comme les comptables externes. Cela signifie que vous ne devez pas acheter un poste supplémentaire dans votre Active Directory actuel ou utiliser l'un de vos comptes [!INCLUDE[d365fin](includes/d365fin_md.md)] utilisateur existants pour votre comptable externe. Par exemple, si votre abonnement actuel à Office 365 inclut 10 utilisateurs pour [!INCLUDE[d365fin](includes/d365fin_md.md)], et que vous utilisez actuellement 10 licences *Utilisateur complet*, votre administrateur peut simplement ajouter votre comptable externe en tant qu'utilisateur invité dans le portail Azure et affecter à cet utilisateur la licence *Comptable externe* sans coût supplémentaire. Cependant, vous ne pouvez avoir qu'un utilisateur avec la licence *Aide-comptable externe*. Si vous souhaitez ajouter des utilisateurs supplémentaires, vous devez mettre à jour votre abonnement à Office 365 en conséquence.  

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Expériences de comptables dans Dynamics 365 for Financials](finance-accounting.md)  
[Financials pour comptables sur Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

