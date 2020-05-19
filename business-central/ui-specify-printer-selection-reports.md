---
title: Paramétrage d'états à imprimer sur des imprimantes spécifiques | Microsoft Docs
description: En savoir plus sur la configuration d'une imprimante pour un état et l'utilisation de la page Sélections d'imprimantes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/17/2020
ms.author: sgroespe
ms.openlocfilehash: dbfdb22447f20b4e4b811dc40cf892d9b971dc77
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/21/2020
ms.locfileid: "3272101"
---
# <a name="set-up-printers"></a>Paramétrage imprimantes
Comme [!INCLUDE[prodshort](includes/prodshort.md)] est un service cloud, il ne peut pas atteindre les imprimantes locales connectées aux machines des utilisateurs. Cependant, il peut se connecter aux imprimantes cloud. Dans la version générique de [!INCLUDE[prodshort](includes/prodshort.md)], une imprimante cloud nommée **Imprimante par e-mail** est installée en tant qu'extension et prête à l'emploi après la configuration initiale.

Si aucune imprimante cloud n'est installée et configurée ou si une imprimante installée échoue, l'impression reprend par défaut les options d'impression du navigateur. Ceci est indiqué par cette valeur dans le champ **Imprimante** sur la page de demande d'état : *(aucune, gestion par le navigateur)*.

Sur la page **Gestion des imprimantes**, vous pouvez voir les imprimantes configurées. Après avoir configuré une ou plusieurs imprimantes, vous pouvez ouvrir la page **Sélections d'imprimantes** pour configurer les états spécifiques à imprimer avec l'imprimante de votre choix pour votre compte utilisateur.

Lorsqu'une imprimante est configurée et affectée à des états spécifiques, vous imprimez un état en cliquant sur le bouton **Imprimer** sur la page de demande d'état. Pour en savoir plus, consultez [Impression d'un état](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Dimensionnement des travaux d'impression
L'impression cloud est conçue pour des documents de taille raisonnable. La plupart des services cloud, y compris PrintNode et HP ePrint, ont une limite de 10 Mo par tâche. Si vous devez imprimer des rapports plus volumineux, vous devrez peut-être les diviser en plusieurs impressions.

## <a name="to-set-up-a-printer"></a>Pour configurer une imprimante
Sur la page **Gestion des imprimantes**, vous pouvez voir les imprimantes configurées et accéder à la page **Paramètres** pour chaque imprimante, afin de modifier une configuration existante ou de configurer une nouvelle imprimante.

La procédure suivante décrit comment configurer l'imprimante existante **Imprimante par e-mail**, qui est une extension préinstallée.

> [!NOTE]
> Pour utiliser l'impression par e-mail, la fonctionnalité de messagerie doit être configurée. Pour plus d'informations, voir [Configurer la messagerie](admin-how-setup-email.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne pour l'imprimante **Imprimante par e-mail**, puis l'action **Modifier les paramètres de l'imprimante**.
3. Sur la page **Paramètres**, renseignez les champs nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Vous devez sélectionner manuellement le format de papier approprié pour une imprimante, car aucune imprimante locale ni aucun paramètre utilisateur ne peuvent être stockés.
    >
    > Sachez que l'extension Imprimante par e-mail est définie par défaut sur le format de papier **A4**, qui n'est pas adapté en Amérique du Nord, par exemple.
4. Pour faire d'une imprimante votre imprimante par défaut, choisissez l'action **Définir comme imprimante par défaut** sur la page **Gestion des imprimantes**.

### <a name="privacy-notice"></a>Déclaration de confidentialité
Si vous utilisez l'extension Imprimante par e-mail, tout ou partie des travaux d'impression sont envoyés à l'adresse e-mail que vous avez fournie lors de la configuration de l'imprimante. Nous vous recommandons vivement d'associer un ID e-mail unique à un périphérique d'impression en utilisant uniquement les services officiels fournis par le fabricant du matériel, tels que HP ePrint, KonicaMinolta EveryonePrint ou Epson Email Print.

Vous devez prendre toutes les précautions de confidentialité nécessaires, notamment en veillant à configurer correctement les autorisations, les paramètres de confidentialité et les stratégies de conservation de la solution d'impression d'e-mails. Il est de votre responsabilité de fournir une adresse e-mail correcte, vérifiée et opérationnelle. Pour en savoir plus, consultez [Déclaration de confidentialité Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Pour sélectionner les imprimantes imprimant des états spécifiques
Sur la page **Sélections d'imprimantes**, vous pouvez configurer les états à imprimer sur des imprimantes spécifiques. Ceci est utile si vous utilisez différents états nécessitant différentes imprimantes en raison de leur placement dans la société ou de leurs capacités d'impression.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sélections d'imprimantes**, puis sélectionnez le lien associé. Sinon, sur la page **Gestion des imprimantes**, sélectionnez une imprimante, puis l'action **Sélections d'imprimantes**.
2. Choisissez l'action **Nouveau** pour ajouter une sélection d'imprimante pour un état spécifique.
3. Renseignez les champs selon vos besoins.

L'état spécifié est désormais configuré pour être imprimé sur l'imprimante sélectionnée par défaut.

> [!NOTE]
> Lorsque vous imprimez l'état en question, vous pouvez remplacer cette configuration en sélectionnant une autre imprimante sur la page de demande **Paramètres d'impression**.

> [!NOTE]
> Si vous ne configurez pas un état pour une imprimante spécifique sur la page **Sélections d'imprimantes**, il est imprimé sur l'imprimante par défaut de la société, comme défini sur la page **Gestion des imprimantes**.

Vous pouvez ou l'administrateur peut également utiliser la page **Sélections d'imprimantes** pour définir d'autres variantes d'impression pour les utilisateurs et les états. Le tableau suivant décrit les combinaisons de valeurs nécessaires pour spécifier une autre configuration d'impression pour un état.

|Pour                                                 |Définir les valeurs suivantes                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Imprimer un état sur une imprimante spécifique pour tous les utilisateurs |Spécifiez une valeur dans les champs **ID état** et **Nom de l'imprimante** et ne renseignez pas le champ **ID utilisateur**.|
|Imprimer tous les états sur une imprimante spécifique pour un utilisateur spécifique|Spécifiez une valeur dans les champs **ID utilisateur** et **Nom de l'imprimante** et ne renseignez pas le champ **ID état**.|
|Définir l'imprimante par défaut pour tous les états|Spécifiez une valeur dans le champ **Nom de l'imprimante** et ne renseignez pas les champs **ID utilisateur** et **ID état**.|
|Imprimer un état spécifique sur l'imprimante par défaut de l'utilisateur|Spécifiez une valeur dans le champ **ID état** et ne renseignez pas les champs **Nom de l'imprimante** et **ID utilisateur**.|
|Imprimer un état spécifique sur une imprimante spécifique pour un utilisateur spécifique|Spécifiez une valeur dans les trois champs.|

> [!NOTE]
> Des sélections d'imprimantes plus spécifiques prévalent sur des sélections d'imprimantes plus générales. Par exemple, une sélection d'imprimante ayant des valeurs dans les champs **ID utilisateur**, **ID état** et **Nom de l'imprimante** prévaut sur une sélection d’imprimante ayant des entrées vides dans le champ **ID utilisateur** ou **ID état**.

## <a name="see-also"></a>Voir aussi
[Impression d'un état](ui-work-report.md#PrintReport)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Exécuter des traitements par lots](ui-how-run-batch-jobs.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
