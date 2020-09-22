---
title: 'Procédure : configurer des clients effectuant un achat au comptoir | Microsoft Docs'
description: Cette rubrique décrit les étapes pour configurer un client qui paie en espèces.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b93999ec3e8520dedd1601efad7fc00d4d625317
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788640"
---
# <a name="set-up-cash-customers"></a>Configurer des clients effectuant un achat au comptoir
Vous ne pouvez pas créer une facture sans numéro de client. Ceci est valable même si vous effectuez une vente au comptoir et que vous n'avez rien à enregistrer dans un compte client.  

## <a name="to-set-up-a-cash-customer"></a>Pour configurer des clients effectuant un achat en espèces  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Client**, puis sélectionnez le lien associé.  
2.  Créez une fiche **Client**. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).
3.  Dans le champ **N°**, , saisissez par exemple **Espèces**.  
4.  Dans le champ **Nom**, saisissez par exemple **Vente au comptoir**.  
5.  Sur le raccourcie **Facturation**, renseignez les champs **Groupe compta. client** et **Groupe compta. marché**.  

 Vous avez alors configuré un client contenant suffisamment d'informations de facturation.  

> [!NOTE]  
>  Vous avez peut-être choisi un groupe comptabilisation également utilisé pour les ventes à crédit nationales. Si vous souhaitez mettre à jour des données séparées sur les ventes au comptoir, par exemple avec un compte client ou fournisseur spécial, vous pouvez configurer un groupe comptabilisation supplémentaire à cet effet.  
>   
>  Vous devez saisir le numéro d'un compte client pour le groupe comptabilisation, même si le solde de ce compte est toujours de 0 après la validation d'une facture.  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)    
[Finances](finance.md)  

