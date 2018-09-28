---
title: "Détails de conception - Compta. coûts prévus | Microsoft Docs"
description: "Les coûts prévus représentent l'estimation, par exemple, du coût d'un article acheté que vous enregistrez avant la réception de la facture de cet article."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 50ac9cbb946fedc687eb5ea1373c99d68f3d322b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-expected-cost-posting"></a>Détails de conception : validation du coût prévu
Les coûts prévus représentent l'estimation, par exemple, du coût d'un article acheté que vous enregistrez avant la réception de la facture de cet article.  

 Vous pouvez valider les coûts prévus dans le stock et dans la comptabilité. Lorsque vous validez une quantité qui est uniquement reçue ou expédiée mais pas facturée, une écriture valeur est créée avec le coût prévu. Ce coût prévu affecte la valeur du stock mais n'est pas porté au compte général, sauf si vous avez paramétré le programme à cette fin.  

> [!NOTE]  
>  Les coûts prévus sont gérés uniquement pour des transactions article. Les coûts prévus ne sont pas pour des types de transaction négligeables, tels que la capacité et les frais annexes.  

 Si seulement la partie de quantité d'une entrée de stock a été validée, la valeur du stock de la comptabilité ne change pas, sauf si vous avez sélectionné la case à cocher **Compta. coûts prévus** dans la fenêtre **Paramètres stock**. Dans ce cas, le coût prévu est validé dans les comptes d'attente au moment de la réception. Une fois que la réception a été entièrement facturée, les comptes d'attente sont ensuite équilibrés et le coût réel est validé dans le compte stock.  

 Pour prendre en charge le travail de rapprochement et de traçabilité, l'écriture valeur facturée montre que le montant du coût prévu validé pour équilibrer les comptes d'attente.  

## <a name="example"></a>Exemple :  
 L'exemple suivant indique le coût prévu si la case à cocher **Compta. coûts automatique** et la case à cocher **Compta. coûts prévus** sont sélectionnées dans la fenêtre **Paramètres stock**.  

 Vous validez une commande achat comme reçue. Le coût prévu est 95,00 DS.  

 **Ecritures valeur**  

|Date comptabilisation|Type écriture|Coût total (prévu)|Coût prévu validé en comptabilité|Coût prévu|N° écriture comptable article|Numéro de la séquence|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01/01/20|Coût direct|95,00|95,00|Oui|1|1|  

 **Liens des écritures dans la comptabilité – Table Écriture comptable article**  

|N° séquence compta.|N° écriture valeur|N° hist. transaction compta.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Écritures comptables**  

|Date comptabilisation|Compte général|N° compte (démonstration Fr-FR)|Montant|Numéro de la séquence|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01/01/20|Compte ajustement stock (attente)|5 530|-95,00|2|  
|01/01/20|Compte stocks (attente)|2 131|95,00|1|  

 Plus tard, vous pourrez valider la procédure achat comme étant facturée. Le coût facturé est 100,00 DS.  

 **Ecritures valeur**  

|Date comptabilisation|Coût total (réel)|Coût total (prévu)|Coût validé en comptabilité|Coût prévu|N° écriture comptable article|Numéro de la séquence|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|15/01/20|100,00|-95,00|100,00|Non|1|2|  

 **Liens des écritures dans la comptabilité – Table Écriture comptable article**  

|N° séquence compta.|N° écriture valeur|N° hist. transaction compta.|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Écritures comptables**  

|Date comptabilisation|Compte général|N° compte (démonstration Fr-FR)|Montant|Numéro de la séquence|  
|------------------|------------------|---------------------------------|------------|---------------|  
|15/01/20|Compte ajustement stock (attente)|5 530|95,00|4|  
|15/01/20|Compte stocks (attente)|2 131|-95,00|3|  
|15/01/20|Compte coût direct lettré|7291|-100|6|  
|15/01/20|Compte stocks|2130|100|5|  

## <a name="see-also"></a>Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)   
 [Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md)   
 [Détails de conception : comptabilisation stock](design-details-inventory-posting.md)   
 [Détails de conception : écart](design-details-variance.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

