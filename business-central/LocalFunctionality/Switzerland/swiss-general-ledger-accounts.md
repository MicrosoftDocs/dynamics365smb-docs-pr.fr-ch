---
title: 'Comptes généraux, Suisse [CH]'
description: 'Cet article explique les améliorations apportées aux comptes généraux, Suisse et aux feuilles comptabilité.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 11500
ms.date: 06/21/2021
ms.author: bholtorf
---
# <a name="swiss-general-ledger-accounts"></a>Comptes généraux, Suisse
[!INCLUDE[prod_short](../../includes/prod_short.md)] inclut les améliorations suisses apportées aux fonctions spéciales liées aux comptes généraux.

- Conserver les soldes en devises d'un compte bancaire dans les comptes généraux.  
- Trier les numéros de comptes généraux dans la page **Plan comptable**.  
- Prévisualiser les effets que la validation des feuilles comptabilité auraient sur les soldes de certains comptes généraux avant leur validation réelle.  

## <a name="general-ledger-accounts-and-general-journals"></a>Comptes généraux et feuilles comptabilité
Les entreprises ont souvent des comptes bancaires différents pour les devises étrangères et disposent d'un compte général pour chaque compte bancaire. Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], vous pouvez définir un code devise et les informations de solde en devise étrangère dans la page **Plan comptable**. Cela vous permet de conserver le solde de départ en devises d'un compte bancaire. Pour plus d'informations, voir [Description des écritures comptables et du plan comptable](../../finance-general-ledger.md).  

Par exemple, une société a deux comptes bancaires : une pour la devise société (DS) et une pour les euros (EUR). Vous devez créer des écritures comptables pour chaque compte bancaire. Pour le compte en euros, définissez le code devise **EUR** et validez les feuilles en EUR ou DS.  

Lorsque le taux de change pour EUR et DS change, vous pouvez mettre à jour et ajuster le solde de la devise locale pour le grand livre EUR à l'aide du traitement par lots Ajuster taux de change. Ce traitement par lots crée et valide des écritures d'ajustement de devise dans le grand livre et met à jour le solde DS.  

## <a name="data-type-for-general-ledger-accounts"></a>Type de données pour les comptes du grand livre général
Le type de données est défini en texte pour le numéro de compte du grand livre général ou le code de compte afin de prendre en charge les exigences de tri pour le plan comptable standardisé Swiss Kontenrahmen Käfer (KMU). La liste des numéros de compte est triée selon le type de données de texte. Le plan comptable KMU indique les numéros de compte suivants :  

- 1176  
- 119.0  
- 1190  

## <a name="viewing-temporary-balances-in-general-journals"></a>Affichage des soldes temporaires dans les feuilles comptabilité
Avant de valider une feuille comptabilité, vous pouvez prévisualiser l'effet que cette validation aurait sur les soldes de certains comptes généraux. Vous pouvez ouvrir une page de statistiques qui affiche les soldes des comptes et les soldes des lignes actives qui incluaient les valeurs non intégrées pour le journal en cours. Pour plus d'informations, voir [Affichage des soldes temporaires dans les feuilles comptabilisation immobilisation](how-to-view-temporary-balances-in-general-ledger-journals.md).  

## <a name="see-also"></a>Voir aussi

[Afficher les soldes temporaires dans les feuilles comptabilisation immobilisation](how-to-view-temporary-balances-in-general-ledger-journals.md)  
[Fonctionnalité locale, Suisse](switzerland-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
