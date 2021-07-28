---
title: 'Procédure : Ajuster les taux de change devise [CH]'
description: Si vous avez des ventes imposables en devise étrangère, vous devez utiliser le taux officiel pour la conversion de devise TVA telle que définie par l'administration fiscale.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: b603a6b18f47f139d0dcd70d985065adac8702b3
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437516"
---
# <a name="adjust-exchange-rates-in-the-swiss-version"></a>Ajuster les taux de change devise dans la version suisse
Si vous avez des ventes imposables en devise étrangère, vous devez utiliser le taux officiel pour la conversion de devise TVA telle que définie par l'administration fiscale.  

Si ces taux ne correspondent pas aux taux de change utilisés dans les factures d'achat ou de vente, vous devrez ultérieurement ajuster les taux de TVA à l'aide d'un traitement par lots. Ces ajustements peuvent uniquement être exécutés en utilisant un taux de TVA autorisé.  

Vous pouvez exécuter ce traitement par lots aussi souvent que vous le souhaitez, cependant assurez-vous que vous l'exécutez toujours avant de créer une déclaration TVA.  

> [!NOTE]  
>  Lorsque vous utilisez une devise report, assurez-vous que le champ **Ajustement tx de change TVA** dans la page **Paramètres comptabilité** est défini sur **Aucun ajustement**.  

Pour plus d'informations sur la TVA et les devises étrangères, voir le site Web [ESTV](https://go.microsoft.com/fwlink/?LinkId=285999).  

## <a name="to-adjust-an-exchange-rate"></a>Pour ajuster un taux de change  

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Devises**, puis sélectionnez le lien associé.  
2.  Sélectionnez l'option **Taux de change**.  
3.  Dans la page **Taux de change devise**, saisissez le taux de TVA officiel par période pour chaque devise dans les champs **Montant taux change TVA** et **Montant taux change TVA lié**.  
4.  Cliquez sur le bouton **OK**.  
5.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Ajuster les taux de change devise**, puis sélectionnez le lien associé.  
6.  Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.   

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Date début**|Saisissez une date pour spécifier le début de la période pendant laquelle les écritures seront ajustées.|  
    |**Date fin**|Saisissez la dernière date à laquelle les écritures seront ajustées. Cette date est habituellement identique à la date du champ **Date comptabilisation**.|  
    |**Ajuster taux de change TVA**|Indiquez si vous souhaitez ajuster le taux de change TVA.|  

7.  Pour démarrer le traitement par lots, cliquez sur le bouton **Imprimer**. Ce traitement par lots contrôle si les entrées de TVA doivent être ajustées et prépare une écriture d'ajustement pour chacune de ces écritures pour les comptes Ajustement de taux de change non réalisés/réalisés. Les écritures TVA existantes sont également corrigées.  

## <a name="see-also"></a>Voir aussi  
 [Taxe sur la valeur ajoutée, Suisse](swiss-value-added-tax.md)   
 [Taux de TVA pour la Suisse](vat-rates-for-switzerland.md)   
[Mettre à jour des taux de change devise](../../finance-how-update-currencies.md)  
[Configurer une devise report supplémentaire](../../finance-how-setup-additional-currencies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]