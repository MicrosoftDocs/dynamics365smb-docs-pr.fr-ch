---
title: "Fonctionnalité multilingue et localisation | Microsoft Docs"
description: "Découvrez comment la langue et les paramètres régionaux influencent votre expérience dans Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b46f4d9882297b147ecee1c86faf3eb19f4e9fa7
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="language-and-locale"></a>Langue et paramètres régionaux
[!INCLUDE[d365fin](includes/d365fin_md.md)]  est pris en charge dans plusieurs marchés et est disponible dans les langues requises par ces marchés. Cela résulte de la prise en charge de plusieurs langues au moment de l'exécution, en plus de la prise en charge des exigences légales dans les marchés pris en charge. Cela signifie que [!INCLUDE[d365fin](includes/d365fin_md.md)] peut être affiché en plusieurs langues. Vous pouvez modifier la langue utilisée pour l'affichage des textes et ce changement est immédiat une fois que le système vous a déconnecté et reconnecté automatiquement. Le paramètre ne s'applique qu'à vous et non aux autres utilisateurs de votre société.  

Par exemple, si vous êtes canadien, vous pouvez afficher l'interface utilisateur en anglais et en français, mais pour tous les autres aspects de l'application, il s'agit toujours de la version canadienne de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Elle diffère, par exemple, de la version de [!INCLUDE[d365fin](includes/d365fin_md.md)] destinée au Royaume-Uni.  

> [!NOTE]  
>  La modification de la langue n'est pas actuellement prise en charge dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

La modification des textes stockés sous forme de données d'application n'appartient pas à la fonctionnalité multilingue. C'est une question de conception de l'application. Il s'agit par exemple de textes tels que le nom des articles du stock ou les commentaires concernant un client. En d'autres termes, ces types de texte ne sont pas traduits.  

> [!NOTE]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]  ne prend en charge qu'un jeu de caractères unique pour les données. Aussi, il se peut que certains caractères ne soient pas pris en charge dans votre abonné et vous pouvez rencontrer des problèmes de récupération des données saisies à l'aide d'un autre jeu de caractères. Par exemple, votre abonné peut ne prendre en charge que les caractères anglais et russes, et si vous entrez des données dans une autre langue, elles peuvent ne pas être stockées correctement. Vous devez contacter votre administrateur système pour connaître les langues prises en charge pour votre client [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="changing-the-locale"></a>Modification des paramètres régionaux
Les paramètres régionaux diffèrent des exigences linguistiques et légales des marchés locaux. Les paramètres régionaux déterminent la manière dont vos données s'affichent en termes de séparateur de virgule, aligné à gauche ou à droite, et certains autres paramètres. Les paramètres régionaux déterminent également certains éléments du système dans le navigateur, par exemple l'action permettant de créer un élément dans une liste.  

Vous pouvez modifier les paramètres régionaux dans l'onglet du navigateur que vous utilisez pour travailler dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Les modifications ne s'appliquent qu'à vous et non aux autres utilisateurs de votre société.  

> [!IMPORTANT]  
>  Lorsque vous modifiez les paramètres régionaux, une longue liste de langues et de paramètres régionaux s'affiche. Toutefois, seuls les paramètres régionaux sont utilisés dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Pour modifier les paramètres régionaux, accédez à la fenêtre **Mes paramètres**. Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).  

## <a name="see-also"></a>Voir aussi  
[Langues de Docs](about-languages.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

