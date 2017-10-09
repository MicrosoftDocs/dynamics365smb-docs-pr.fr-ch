---
title: "Définition de la relation entre les types de coûts et les comptes généraux | Microsoft Docs"
description: "Découvrez comment définir la relation entre le type de coût et le compte général."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Définition de la relation entre les types de coûts et les comptes généraux
Une relation entre le type de coût et le compte général est créée dans le type de coût et le compte général.  

* Le champ **Plage compte général** de la table **Type coût** définit les comptes généraux appartenant à un type de coût.  
* Le champ **N° type coût de solde** du plan comptable définit l'appartenance du compte général à un type de coût.  

Ces deux champs sont renseignés automatiquement lorsque vous utilisez la fonction **Obtenir les types de coûts à partir du plan comptable**.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relations entre les comptes généraux et les types de coûts  
Une relation n:1 existe entre les comptes généraux et les types de coûts. Plusieurs comptes généraux peuvent appartenir à un type de coût, mais chaque compte général appartient à un seul type de coût. Le tableau suivant décrit la relation en détails.  

|Relation|**Plage compte général**|**N° type coût**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Un compte général pour chaque type de coût|Un compte général|Un type de coût|  
|Plusieurs comptes généraux pour chaque type de coût|Plage de comptes généraux, par exemple, 7110..7193 pour chaque compte général|Pour chaque compte général de la plage, il n'existe qu'un seul type de coût|  
|Types de coûts sans comptes généraux correspondants|<Empty>||  
|Comptes généraux dont les écritures ne seront pas transférées||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Types de coûts sans relation avec la comptabilité générale  
Un type de coût risque de ne pas afficher une relation avec les comptes généraux si une des conditions suivantes est vraie :  

* Les comptes pour la comptabilité opérationnelle, notamment les intérêts et l'amortissement, prennent uniquement les coûts provenant de la comptabilité opérationnelle.  
* Les types de coûts, notamment 9901, 9902 et 9903, dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] servent de comptes de crédit et de débit pour les affectations.  
* Le compte 9920 dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] indique les régularisations réelles qui font état de la différence entre les coûts et les frais provenant de la comptabilité.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)   
[À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

