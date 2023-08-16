---
title: Utiliser la facturation dans Business Central
description: Solution de contournement pour accéder à Microsoft Invoicing lorsque vous vous êtes inscrit à Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Utiliser le même compte Microsoft 365 dans [!INCLUDE[prod_short](includes/prod_long.md)] et Microsoft Invoicing
Lorsque vous êtes inscrit à une version d’évaluation avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez passer à une phase d’évaluation de 30 jours, démarrer un abonnement ou encore l’arrêter à l’aide de [!INCLUDE[prod_short](includes/prod_short.md)]. Dans tous les cas, vous avez peut-être à un moment donné vu quelque chose appelé **Microsoft Invoicing** et cliqué dessus. Il s’agissait d’une application qui faisait partie de ce qui est maintenant Microsoft 365 Business Standard et était anciennement connue sous le nom d’abonnement Business Premium Microsoft 365, donc tout le monde n’aura pas vu cette mosaïque au cours de son expérience Microsoft 365.  

Microsoft Invoicing n’est plus disponible, mais si vous devez vous connecter à Invoicing pour récupérer vos données, un message vous indiquant que vous ne pouvez pas accéder à Microsoft Invoicing car votre compte est utilisé dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Un message similaire s’affiche si vous installez l’application mobile pour Invoicing.  

## Solution de contournement
Invoicing et [!INCLUDE[prod_short](includes/prod_short.md)] ont une plate-forme partagée. Cela signifie que vous êtes reconnu en tant qu’utilisateur existant de [!INCLUDE[prod_short](includes/prod_short.md)] lorsque vous cliquez sur Invoicing dans le centre d’administration Microsoft 365. Invoicing ne peut pas utiliser la même société que [!INCLUDE[prod_short](includes/prod_short.md)].  

Vous devez donc vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] et renommer votre société existante, puis créer une nouvelle société que vous pourrez alors utiliser dans Invoicing. Aucune donnée n’est déplacée ou remplacée au cours de cette opération.

### Pour renommer votre société
1. Connectez-vous à [!INCLUDE[prod_short](includes/prod_short.md)].
2. Dans le coin supérieur droit, sélectionnez l’icône **Paramètres** ![Paramètres.](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis choisissez **Mes paramètres**.
3. Dans le champ **Société**, sélectionnez une autre société.
4. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sociétés**, puis choisissez le lien associé.  
5. Sur la page **Sociétés**, sélectionnez le bouton **Modifier la liste**.  
6. Remplacez le nom de l’entrée *Ma société* par un autre nom.  

    Patientez quelques minutes. Nous apporterons plusieurs modifications à la base de données sous-jacente, et cette opération prendra un certain temps.
7.  Lorsque le système est à nouveau prêt, sélectionnez le bouton **Créer une nouvelle société**.  
8.  Dans la boîte de dialogue qui s’affiche, entrez *Ma société* comme nom et sélectionnez l’option **Production - Données de configuration uniquement**.  

Cette opération prend plusieurs minutes. Lorsque le processus est terminé, vous pouvez accéder à Invoicing dans le cadre de votre expérience Microsoft 365 Business Standard. Mais uniquement pour exporter des données, car l’application Facturation est obsolète.  

### Qu’en est-il de mes données ?
Lorsque vous renommez la société d’origine, les tables de la base de données qui stockent vos données [!INCLUDE[prod_short](includes/prod_short.md)] existantes sont renommées, mais les données proprement dites sont conservées.  

Si vous utilisez Invoicing et [!INCLUDE[prod_short](includes/prod_short.md)], les données sont stockées dans deux conteneurs différents (les deux sociétés). Aucun donnée n’est partagée, vous devrez donc gérer les clients et les articles dans les deux sociétés.  

## Voir aussi
[Forum Aux Questions](across-faq.yml)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]