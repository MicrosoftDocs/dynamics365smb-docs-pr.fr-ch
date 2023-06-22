---
title: Configurer plusieurs taux d’intérêt pour les paiements retardés
description: Cette rubrique vous explique comment calculer les intérêts avec plusieurs taux d’intérêts pour une période donnée.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '6, 431, 432, 572'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="set-up-multiple-interest-rates-for-delayed-payment" />Configurer plusieurs taux d’intérêt pour les paiements retardés

Vous pouvez utiliser différents taux d’intérêt pour différentes périodes pour les paiements retardés dans les transactions commerciales. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

Par exemple, un gouvernement définit l’intérêt maximum à prélever pour un consommateur. Ce taux d’intérêt peut être modifié deux fois par an le 1er janvier et le 1er juillet inclus. Le taux d’intérêt entre les sociétés (B2B) est accepté par les parties et il n’existe aucune limite à ce groupe de clients. Le taux annoncé est généralement quatre fois supérieur aux intérêts bancaires normaux.

Lorsque vous créez des conditions d’intérêts de retard et les conditions de relance, pour la pénalité de retard de paiement, vous pouvez spécifier plusieurs taux d’intérêt afin que les frais de pénalité soient calculés sur la base de plusieurs taux d’intérêt à différentes périodes.  

## <a name="to-set-up-multiple-interest-rates" />Pour paramétrer plusieurs taux d’intérêt

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Conditions intérêts de retard**, puis sélectionnez le lien associé.  
2. Sur la page **Conditions intérêts de retard**, sélectionnez les conditions d’intérêt, puis sélectionnez l’action **Taux d’intérêt**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Cliquez sur le bouton **OK**.  
5. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Conditions de relance**, puis sélectionnez le lien associé.  
6. Sur la page **Conditions de relance**, sélectionnez les conditions de relance, puis sélectionnez l’action **Niveaux**.  
7. Sur la page **Niveaux relance**, pour les niveaux de relance concernés, sélectionnez le champ **Calculer intérêts**.  

Lorsque vous émettez une facture d’intérêts, a facture affiche les frais financiers avec plusieurs taux d’intérêt pour une période donnée. La facture affiche également les informations contact du client, de la société émettant la facture, du montant supplémentaire, et du montant total. L’écriture ouverture sur la facture est affichée en gras. Les intérêts sont calculés avec plusieurs taux d’intérêt pour une période spécifique et sont imprimés après l’écriture ouverture de la facture.  

## <a name="see-also" />Voir aussi

[Collecte des soldes restants](receivables-collect-outstanding-balances.md)  
[Configuration de Finance](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
