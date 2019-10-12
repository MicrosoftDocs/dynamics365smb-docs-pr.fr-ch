---
title: Utiliser Invoicing et Business Central | Microsoft Docs
description: Solution de contournement pour accéder à Microsoft Invoicing lorsque vous vous êtes inscrit à Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 354babea367b80cdb0eae4078f6111d44583df9e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300776"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365fin_long_mdmd-and-microsoft-invoicing"></a>Utilisation du même compte Office 365 dans [!INCLUDE[d365fin](includes/d365fin_long_md.md)] et Microsoft Invoicing
Lorsque vous êtes inscrit à une version d'évaluation avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez passer à une phase d'évaluation de 30 jours, démarrer un abonnement ou encore l'arrêter à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans tous les cas, si vous vous connectez au portail Office, une vignette intitulée **Microsoft Invoicing** s'affiche : vous pouvez cliquez dessus. Cela fait partie de l'abonnement Office 365 Business Premium, tous les utilisateurs ne verront donc pas cette vignette dans le portail Office.  

Si vous accédez à Microsoft Invoicing, vous verrez un message indiquant que vous ne pouvez pas accéder à Microsoft Invoicing car votre compte est utilisé dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Un message similaire s'affiche si vous installez l'application mobile pour Invoicing.  

## <a name="workaround"></a>Solution de contournement
Invoicing et [!INCLUDE[d365fin](includes/d365fin_md.md)] ont une plate-forme partagée. Cela signifie que vous êtes reconnu en tant qu'utilisateur existant de [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsque vous cliquez sur Invoicing dans le portail Office. Invoicing ne peut pas utiliser la même société que [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Vous devez donc vous connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)] et renommer votre société existante, puis créer une nouvelle société que vous pourrez alors utiliser dans Invoicing. Aucune donnée n'est déplacée ou remplacée au cours de cette opération.

### <a name="to-rename-your-company"></a>Pour renommer votre société
1. Connectez-vous à [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Dans le coin supérieur droit, sélectionnez l'icône **Paramètres** ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Mes paramètres**.
3. Dans le champ **Société**, sélectionnez une autre société.
4. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sociétés**, puis sélectionnez le lien associé.  
5. Sur la page **Sociétés**, sélectionnez le bouton **Modifier la liste**.  
6. Remplacez le nom de l'entrée *Ma société* par un autre nom.  

    Patientez quelques minutes. Nous apporterons plusieurs modifications à la base de données sous-jacente, et cette opération prendra un certain temps.
7.  Lorsque le système est à nouveau prêt, sélectionnez le bouton **Créer une nouvelle société**.  
8.  Dans la boîte de dialogue qui s'affiche, entrez *Ma société* comme nom et sélectionnez l'option **Production - Données de configuration uniquement**.  

Cette opération prend plusieurs minutes. Lorsque le processus est terminé, vous pouvez accéder à Invoicing dans le cadre de votre expérience Office 365 Business Premium.  

### <a name="what-about-my-data"></a>Qu'en est-il de mes données ?
Lorsque vous renommez la société d'origine, les tables de la base de données qui stockent vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] existantes sont renommées, mais les données proprement dites sont conservées.  

Si vous utilisez Invoicing et [!INCLUDE[d365fin](includes/d365fin_md.md)], les données sont stockées dans deux conteneurs différents (les deux sociétés). Aucun donnée n'est partagée, vous devrez donc gérer les clients et les articles dans les deux sociétés.  

## <a name="see-also"></a>Voir aussi
[Forum Aux Questions](across-faq.md)  
[Administration](admin-setup-and-administration.md)  
