---
title: 'Procédure : Imprimer des factures ESR [CH]'
description: Cette rubrique décrit la procédure d'impression de factures et de coupons de bordereau paiement Einzahlungsschein mit Referenznummer (ESR).
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 3010531, 3010532
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: aff58fb7a81469e4ca59fc90e265559ac0bb8252
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129302"
---
# <a name="print-esr-invoices-in-the-swiss-version"></a>Imprimer des factures ESR dans la version suisse

Vous pouvez imprimer un bordereau paiement Einzahlungsschein mit Referenznummer (ESR) des façons suivantes :  

- En tant que facture vente ESR.  
- En tant que document séparé appelé coupon ESR.  

L'état ESR de la facture de vente correspond à la facture de vente accompagnée d'un coupon ESR supplémentaire. En utilisant l'état sur les coupons ESR des ventes, vous pouvez imprimer le bordereau de dépôt bleu.  

> [!NOTE]  
> Vous devez sélectionner une imprimante et sélectionner des paramètres lors de l'installation du module Paiement ESR pour imprimer le bordereau de versement correctement. Pour plus d'informations, voir la table Sélection de l'imprimante.  

La procédure suivante décrit comment imprimer des factures vente ESR, mais les mêmes étapes s'appliquent également pour imprimer des coupons ESR.  

## <a name="to-print-esr-invoices"></a>Pour imprimer des factures ESR  

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Facture ESR**, puis sélectionnez le lien associé.  
2. Dans le traitement par lots **Facture vente ESR**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Nombre de copies**|Saisissez le nombre requis de copies de rapport.|  
    |**Banque ESR**|Sélectionnez le code banque ESR qui doit être imprimé dans l'état.<br /><br /> Si la valeur de ce champ est \<Blank\> et si le code mode de règlement ESR n'est pas défini sur la page **Configuration ESR**, la banque principale ESR sélectionnée sur la page **Configuration ESR** sera imprimée.|  
    |**LogInteraction**|Spécifiez si les interactions avec vos contacts sont enregistrées.|  
    |**Système ESR**|Sélectionnez le système ESR via lequel vous pouvez envoyer des coupons ESR aux clients. Pour utiliser le système ESR utilisé par la banque que vous avez spécifié dans le champ **Banque ESR**, sélectionnez **En fonction de la banque ESR**.|  

3. Sélectionnez le bouton **Imprimer** pour imprimer l'état ou le bouton **Aperçu** pour l'afficher à l'écran.  

Vous pouvez également réimprimer l'état ESR de la facture vente ou l'état du coupon ESR vente.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de ESR, Suisse](swiss-electronic-payments-using-esr.md)   
 [Importer des paiements ESR](how-to-import-esr-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]