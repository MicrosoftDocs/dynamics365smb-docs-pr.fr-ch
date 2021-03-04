---
title: Procédure de configuration d’une société avec l’assistant RapidStart | Microsoft Docs
description: Vous pouvez rapidement configurer une nouvelle société que vous avez créée à l’aide de l’Assistant Configuration de RapidStart Services.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a8631e9ff23ac9972da82fca8f45876f4467031b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917941"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Configurer une société avec l’assistant RapidStart
Vous pouvez rapidement configurer une nouvelle société que vous avez créée à l’aide de l’Assistant Configuration de RapidStart Services.

Dans la procédure suivante, vous avez fourni au client un package configuration, qui est ensuite installé sur un ordinateur. Le client ouvre la nouvelle société, qui ne contient aucune donnée client. Vous ou le client suivez les étapes de l’Assistant RapidStart Services, décrites dans cette procédure, pour spécifier des informations de base sur la société. L’Assistant importe le package configuration, puis lettre le package à la société.  

## <a name="to-configure-a-new-company"></a>Pour configurer une nouvelle société  
1. Dans le tableau de bord Responsable de l’implémentation de RapidStart Services, choisissez l’action **Assistant RapidStart** .  
2. Affichez le raccourci **Étape 1** , qui contient des informations générales sur la nouvelle société. Entrez les informations appropriées sur la nouvelle société dans les champs. Il existe un champ que vous devez renseigner : **Nom** . Les autres champs sont facultatifs.  
3. Affichez le raccourci **Étape 2** , qui contient des informations de communication et de contact pour la nouvelle société. Entrez les informations appropriées sur la nouvelle société dans les champs.
4. Affichez le raccourci **Étape 3** , qui contient des informations sur le compte bancaire et sur le paiement pour la nouvelle société. Entrez les informations appropriées sur la nouvelle société dans les champs.  
5. Développez le raccourci **Étape 4** . Cliquez sur le bouton **AssistEdit** pour sélectionner le package configuration à lettrer. Le nom du package configuration est affiché. Vous pouvez ensuite effectuer les actions suivantes, dans l’ordre déterminé :  

    1. Appliquez la configuration en sélectionnant l’action **Appliquer package** . Il importe le package configuration et applique toutes les données de base de données de package simultanément.  

    2. Relisez la configuration après son application. Cette option vous permet d’étudier les détails de la configuration et les questionnaires fournis par le partenaire et d’importer des données de base requises pour votre société. Sélectionnez l’action **Feuille configuration** . Pour plus d’informations, voir [Pour remplir le questionnaire de configuration](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Développez le raccourci **Étape 5** . Spécifiez quel Tableau de bord sera la valeur par défaut pour la nouvelle société.  

    > [!IMPORTANT]  
    >  Modifiez votre Tableau de bord uniquement après avoir effectué la configuration de la société. Si vous avez d’autres informations de paramétrage à prendre en compte et à modifier, utilisez d’abord la feuille configuration pour effectuer votre travail. Enfin, revenez à l’Assistant pour mettre à jour votre profil Tableau de bord, ou sélectionnez l’action **Configuration terminée** .

7. Cliquez sur le bouton **OK** .  
8. Pour vérifier que les informations de configuration ont été appliquées à la nouvelle société, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Informations société** , puis sélectionnez le lien connexe.

La page **Informations société** contient les informations que vous avez spécifiées.   

Vous avez configuré la société, et des données ont été appliquées.  

## <a name="see-also"></a>Voir aussi  
[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]