---
title: 'Détails de conception : comparaison entre écritures traçabilité actives et historiques | Microsoft Docs'
description: Lorsque des parties d’une quantité de ligne document sont validées, seule cette quantité particulière est transférée vers les écritures comptables article et ses numéros de suivi. Toutefois, vous voudrez accéder à toutes les informations de traçabilité pertinentes directement à partir de la ligne document actif. C’est-à-dire, non seulement vous voudrez visualiser les écritures relatives à la quantité restante, mais vous voudrez également des informations sur les unités validées. Lorsque vous consultez ou modifiez la page **Lignes traçabilité**, le contenu collectif du tableau **Spécification traçabilité** (T336) et du tableau **Écriture réservation** (T337) est présenté dans une version temporaire de T336. Ceci garantit que les données de suivi article historiques et actives sont accessibles en même temps.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 587c396bece9437e170912dc523bebb04a39e1e4
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216043"
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Détails de conception : comparaison entre écritures traçabilité actives et historiques
Lorsque des parties d’une quantité de ligne document sont validées, seule cette quantité particulière est transférée vers les écritures comptables article et ses numéros de suivi. Toutefois, vous voudrez accéder à toutes les informations de traçabilité pertinentes directement à partir de la ligne document actif. C’est-à-dire, non seulement vous voudrez visualiser les écritures relatives à la quantité restante, mais vous voudrez également des informations sur les unités validées. Lorsque vous consultez ou modifiez la page **Lignes traçabilité**, le contenu collectif du tableau **Spécification traçabilité** (T336) et du tableau **Écriture réservation** (T337) est présenté dans une version temporaire de T336. Ceci garantit que les données de suivi article historiques et actives sont accessibles en même temps.  

 Le tableau suivant montre la manière dont T336 et T337 sont utilisés dans un scénario achat. Les chiffres en gras représentent les valeurs entrées manuellement par l’utilisateur sur la page **Lignes traçabilité**.  

 Étape 1 : Créez une ligne commande achat de sept pièces avec les numéros traçabilité.  

||**Quantité (base)**|**Qté à traiter**|**Qté à facturer (base)**|**Quantité traitée (base)**|**Quantité facturée (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Étape 2 : Recevez quatre pièces.  

||**Quantité (base)**|**Qté à traiter**|**Qté à facturer (base)**|**Quantité traitée (base)**|**Quantité facturée (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Page **Lignes traçabilité**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Étape 3 : Recevez deux pièces et facturez deux pièces.  

||**Quantité (base)**|**Qté à traiter**|**Qté à facturer (base)**|**Quantité traitée (base)**|**Quantité facturée (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Page **Lignes traçabilité**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Étape 4 : Recevez une pièce.  

||**Quantité (de base)**|**Qté à traiter**|**Qté à facturer (base)**|**Quantité traitée (base)**|**Quantité facturée (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Page **Lignes traçabilité**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Facturez 5 pièces.  

||**Quantité (de base)**|**Qté à traiter**|**Qté à facturer (base)**|**Quantité traitée (base)**|**Quantité facturée (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Page **Lignes traçabilité**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : traçabilité](design-details-item-tracking.md)   
 [Détails de conception : page Lignes traçabilité](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]