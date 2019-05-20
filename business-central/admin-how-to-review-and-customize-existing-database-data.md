---
title: Procédure de vérification et de personnalisation des données existantes de base de données | Microsoft Docs
description: Lors de la création d’un package configuration pour une solution, vous pouvez consulter et personnaliser les données de base de données disponibles pour les adapter aux besoins de votre client. La table de base de données doit être associée à une page.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244576"
---
# <a name="review-and-customize-existing-database-data"></a>Vérifier et personnaliser les données existantes de base de données
Lors de la création d’un package configuration pour une solution, vous pouvez consulter et personnaliser les données de base de données disponibles pour les adapter aux besoins de votre client. La table de base de données doit être associée à une page.  

### <a name="to-customize-data-in-the-database"></a>Pour personnaliser des données dans la base de données  

1.  Dans la feuille configuration, identifiez les tables dont vous souhaitez afficher ou personnaliser les données.  

    > [!NOTE]  
    >  Assurez-vous que chaque table dispose d’un ID page qui lui est affecté. Pour les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] standard, cette valeur est automatiquement insérée. Pour les tables personnalisées, vous devez fournir l'ID.  

2.  Sous l’onglet **Actions**, dans le groupe **Afficher**, choisissez **Données de base de données**.  

     La page [!INCLUDE[d365fin](includes/d365fin_md.md)] pour la page s’ouvre.  

3.  Révisez les informations disponibles. Modifiez-les selon vos besoins en supprimant les enregistrements qui ne sont pas appropriés ou en ajoutant de nouveaux enregistrements.  

## <a name="see-also"></a>Voir aussi  
 [Gérer la configuration de la société dans une feuille](admin-how-to-manage-company-configuration-in-a-worksheet.md)
