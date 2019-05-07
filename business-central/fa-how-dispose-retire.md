---
title: Cession ou annulation d'immobilisations| Microsoft Docs
description: Vous devez valider une valeur de cession lorsque vous ferraillez, vendez, ou annulez une immobilisation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8afc427ab4bce255c69d797f659b4578723cc023
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "941554"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Céder ou annuler des immobilisations
Lorsque vous commercialisez ou cédez une immobilisation, la valeur de cession doit être validée pour calculer et enregistrer le gain ou la perte. Une écriture cession doit être la dernière écriture validée pour une immobilisation. Pour les immobilisations partiellement cédées, vous pouvez valider plusieurs écritures cession. Le total de tous les montants de cession validés doit être un montant crédit.  

> [!NOTE]  
>   Si vous négociez une immobilisation en échange d'une autre, vous devez enregistrer à la fois la vente de l'ancienne immobilisation (cession) et l'achat de la nouvelle (acquisition). Pour en savoir plus, voir [Acquérir des immobilisations](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Valider une cession à partir d'une feuille comptabilisation immobilisation
1. Choisissez l'icône de ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilisation immobilisation**, puis sélectionnez le lien associé.  
2. Créez une feuille comptable initiale et complétez les champs, le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Dans le champ **Type compta. immo**, sélectionnez **Cession**.  
4. Sélectionnez l'action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de la cession.  

    > [!NOTE]  
    >   L'étape 4 ne fonctionne que si vous avez configuré ce qui suit : la page **Fiche groupe compta. immo.** pour le groupe de validation de l'immobilisation, le champ **Cession immobilisation** contient le compte débit général et le champ **Compte contrepartie cession** contient le compte général auquel vous souhaitez valider les écritures contrepartie pour appréciation. Pour plus d'informations, reportez vous à [Pour configurer des groupes de validation immobilisation](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Sélectionnez l'action **Valider**.  

Si vous vendez une immobilisation ou en cédez une partie, vous devez d'abord diviser l'immobilisation avant de pouvoir enregistrer la transaction cession. Pour en savoir plus, voir [Transférer, fractionner ou regrouper les immobilisations](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Pour visualiser des écritures comptables cession
Lorsque vous vendez ou cédez une immobilisation, la valeur de cession est validée en comptabilité où vous pouvez afficher le résultat.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.  
2. Sélectionnez l'immobilisation pour laquelle vous souhaitez afficher les écritures, puis sélectionnez l'action **Lois d'amortissement**.  
3. Sélectionnez la loi d'amortissement pour laquelle vous souhaitez afficher les écritures, puis sélectionnez l'action **Écritures comptables**.  
4. Sélectionnez une ligne avec **Cession** dans le champ **Catégorie compta. immo.**, puis sélectionnez l'action **Naviguer**.  
5. Sur la page **Naviguer**, sélectionnez la ligne d'écriture comptable, puis l'action **Afficher**.  

La page **Écritures comptables** s'ouvre. Vous pouvez y voir les écritures résultant de la validation de la cession.  

## <a name="see-also"></a>Voir aussi
[COMPTES D'IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d'immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
