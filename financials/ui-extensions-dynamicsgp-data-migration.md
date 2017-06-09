---
title: Microsoft Dynamics GP Data Migration | Microsoft Docs
description: Fournit des informations sur l&quot;extension Dynamics GP Data Migration
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a94afbd0ee689f6bd9157d0b441959f252230f08
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a>Extension Dynamics GP Data Migration pour Dynamics 365 for Financials
Cette extension facilite la migration des clients, des fournisseurs, des articles en stock et des comptes à partir de Dynamics GP vers [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si votre entreprise utilise Dynamics GP aujourd'hui, vous pouvez exporter les principaux enregistrements appropriés, puis ouvrir un guide de configuration assistée pour ajouter les données vers [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Migrer des données métier à partir d'autres systèmes financiers](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportation de données à partir de Dynamics GP
Vous devez avoir exporté certains ou tous vos clients, fournisseurs, articles de stock, et comptes dans un fichier à l'aide de la fonctionnalité Dynamics GP pour l'exportation de données. Pour les besoins de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter les types de données suivants :

* Compte  
* Client  
* Article  
* Fournisseur  

L'extension Dynamics GP Data Migration mappe automatiquement les données exportées afin qu'elles soient rapidement disponibles dans votre nouvelle société [!INCLUDE[d365fin](includes/d365fin_md.md)]. Au cours de ce processus, la prise en charge des informations de configuration est créée, comme des groupes comptabilisation. Les articles en stock sont transmis au système avec FIFO comme méthode d'évaluation du coût. Les comptes sont configurés comme segment principal à partir de Dynamics GP avec des axes, car [!INCLUDE[d365fin](includes/d365fin_long_md.md)] n'a pas de segments de compte.

## <a name="see-also"></a>Voir aussi
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  

