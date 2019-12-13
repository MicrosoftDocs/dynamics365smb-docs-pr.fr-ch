---
title: Documents vente et Documents achat, Suisse
description: Les améliorations suisses comprennent des fonctions spéciales propres aux documents d'achat et de vente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8b0d1e4f0ae66105f6bb6c019307bddac5fb1259
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878799"
---
# <a name="swiss-purchase-documents-and-sales-documents"></a>Documents vente et Documents achat, Suisse
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] comprend des améliorations suisses propres aux documents d'achat et de vente. Notamment :  

- Libellés écriture améliorés pour les écritures comptables, écritures comptables client et fournisseur. Pour plus d'informations, voir la table Écriture comptable, la table Écriture comptable client et la table Écriture comptable fournisseur.  
- Possibilité d'avoir des sous-titres, des sous-totaux et des totaux de début et de fin dans les devis et les commandes vente.  
- Possibilité d'arrondir les totaux de facture dans les lignes de feuille paiement en cas d'escompte.  
- Possibilité de désactiver l'impression de documents d'expédition supplémentaires pour les factures d'achat et les factures de vente.  

## <a name="purchase-documents-and-sales-documents"></a>Documents vente et Documents achat  
Les libellés écriture affichés dans les écritures comptables pour les commandes achat et les commandes vente affichent le nom des fournisseurs ou des clients, ainsi que les factures ou les numéros d'avoir. Par exemple, le **Fact. 103020/ The Cannon Group PLC** est un libellé écriture. Ce libellé écriture affiche un numéro qui est utile pour les transactions financières, qui permet d'analyser les transactions plus aisément.  

### <a name="sales-quotes-and-sales-orders"></a>Devis et commandes vente  
Lors de la création d'un devis ou d'une commande vente, si le type de la ligne devis ou ligne commande vente est **Début total** ou **Fin total**, les articles figurant sur les lignes sont marquées comme étant des articles physiques ou en tant qu'articles de service. Les articles ont alors des sous-positions pour chaque groupe d'articles, et un sous-total est créé pour chaque groupe d'articles.  

Les articles sont divisés en fonction des valeurs générées par le système affichées dans le champ **Niveau**.  

Vous pouvez spécifier un article comme variante de la ligne devis. Cela vous permet de répertorier les articles secondaires sans inclure le prix du devis. Vous pouvez également faire référence aux éléments spécifiques de devis ou de commande vente en fonction de la valeur affichée dans le champ **Position** de la ligne devis ou de la ligne commande vente. Pour plus d'informations, voir la table Ligne vente.  

## <a name="purchase-invoices-and-sales-invoices-with-payment-discounts"></a>Factures achat et Factures vente avec escomptes  
Pour les factures achat et les factures vente, le montant facture est retranché du montant remise, puis arrondi. Le facture totale est également arrondie s'il existe une remise. Pour plus d'informations, voir la table Paramètres comptabilité.  

## <a name="shipment-documents"></a>Documents d'expédition  
Dans la page **Paramètres ventes**, le champ **Expédition sur Livrer et facturer** est utilisé pour désactiver l'impression de documents d'expédition supplémentaires pour les factures d'achat et les factures de vente. Lorsque vous validez une commande, une expédition validée et une facture enregistrée sont automatiquement créées. Si la facture imprimée est également utilisée comme document expédition, la documentation supplémentaire d'expédition n'a pas besoin d'être imprimée. Vous pouvez désactiver l'impression de documents d'expédition supplémentaires pour les factures d'achat et les factures de vente en désactivant le champ **Expédition sur Livrer et facturer** dans la page **Paramètres vente**. Pour plus d'informations, voir la table Paramètres ventes.  

## <a name="see-also"></a>Voir aussi  
 [Importer les codes postaux suisses](how-to-import-swiss-post-codes.md)   
 [Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [Fonctionnalité locale, Suisse](switzerland-local-functionality.md)
