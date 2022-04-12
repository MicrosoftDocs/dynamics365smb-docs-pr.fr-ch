---
title: Configurer une société
description: En tant que partenaire, configurez correctement Business Central pour votre client avec les configurations par défaut ou spécifiques au client que vous regroupez en packages de configuration.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e142f8aef14ea82d67de0c51a996e4f6a6b43dbf
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513189"
---
# <a name="set-up-company-configuration-with-rapidstart-services"></a>Configurer une société avec RapidStart Services

Le processus d’implémentation commence avec le partenaire Microsoft. En tant que partenaire, vous êtes chargé d’analyser les détails de configuration et de créer un package qu’un client peut facilement appliquer. Avant de créer une nouvelle société dans [!INCLUDE [prod_short](includes/prod_short.md)] en ligne ou sur site, vous devez planifier la façon dont elle sera configurée. Vous devez prendre en compte les données de configuration de base et les types de données requis par la solution [!INCLUDE[prod_short](includes/prod_short.md)]. Vous regroupez toutes ces informations dans des packages configuration.

RapidStart Services fournit également les outils que vous utiliserez pour migrer les données héritées, telles que les clients et les fournisseurs.  

Il est recommandé de créer des packages configuration dont la plupart des tables de configuration sont déjà renseignées pour permettre aux clients de ne modifier que quelques paramètres après l’application du package. Par exemple, lorsque vous créez une société, les tables **Souches de n°** et **Ligne souche de n°** sont renseignées à l’aide d’un ensemble de souches de numéros et les numéros de début. Les champs **Souches de n°** correspondants des tables de configuration sont également renseignés automatiquement. Il n’est pas nécessaire d’entrer les souches de numéros et autres informations de configuration de base. Vous pouvez également modifier manuellement toutes les données par défaut utilisées avec RapidStart Services à l’aide de la feuille de configuration.  

Les packages configuration sont constitués sur la base d’une société préconfigurée. Après avoir configuré une société qui répond à vos besoins, vous pouvez créer un package configuration qui contient les données pertinentes de cette société. Vous pouvez ensuite les utiliser lorsque vous créez une société que vous voulez configurer de la même manière.  

Pour faciliter l’importation des données principales, par exemple les informations sur le fournisseur et le client, vous pouvez utiliser des modèles de configuration. Les modèles de configuration contiennent un ensemble de paramètres par défaut, qui sont automatiquement affectés aux enregistrements importés dans [!INCLUDE[prod_short](includes/prod_short.md)].

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Planifier une configuration de la société en renseignant la feuille de configuration.|[Gérer la configuration de la société dans une feuille](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Créer un package configuration, personnaliser un package, affecter des tables à un package, vérifier ou modifier les données client existantes, créer la société et déplacer les données de test vers l’environnement de production.|[Préparer un package configuration](admin-how-to-prepare-a-configuration-package.md)|

Vous pouvez également créer des packages de configuration avec des configurations standard que vous pouvez réutiliser. Pour plus d’informations, voir [Configurer les packages de configuration standard de la société](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) dans le contenu pour développeurs et administrateurs.  

## <a name="see-also"></a>Voir aussi

[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]