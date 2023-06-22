---
title: "Détails de conception\_: comptes de la comptabilité | Microsoft Docs"
description: 'Pour rapprocher le stock et les écritures comptables de capacité en comptabilité, les écritures valeur associées sont validées dans différents comptes en comptabilité.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-accounts-in-the-general-ledger" />Détails de conception : comptes de la comptabilité
Pour rapprocher le stock et les écritures comptables de capacité en comptabilité, les écritures valeur associées sont validées dans différents comptes en comptabilité. Pour plus d’informations, voir [Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger" />À partir de la comptabilité inventaire
Le tableau suivant montre les relations entre différents types d’écritures de valeur du stock et les comptes et les comptes contrepartie dans la comptabilité.  

|**Type écriture comptable article**|**Type écriture valeur**|**Type écart**|**Coût prévu**|**Compte**|**Compte contrepartie**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Achats|Coût direct||Oui|Stocks (attente)|Compte ajust. stock (attente)|  
|Achats|Coût direct||Non|STOCKS ET EN-COURS|Coût direct lettré|  
|Achats|Coût indirect||Non|STOCKS ET EN-COURS|Frais généraux lettrés|  
|Achats|Ecart|Achats|Non|STOCKS ET EN-COURS|Écart achat|  
|Achats|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Achats|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Vente|Coût direct||Oui|Stocks (attente)|Val. sortie stock (attente)|  
|Vente|Coût direct||Non|STOCKS ET EN-COURS|COGS|  
|Vente|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Vente|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Ajust. positif,Ajust. négatif, Transfert|Coût direct||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Ajust. positif,Ajust. négatif, Transfert|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Ajust. positif,Ajust. négatif, Transfert|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  
|(Production) Consommation|Coût direct||Non|STOCKS ET EN-COURS|TEC|  
|(Production) Consommation|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|(Production) Consommation|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Consommation d’assemblage|Coût direct||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Consommation d’assemblage|Coût direct||Non|Coût direct lettré|Ajustement stock|  
|Consommation d’assemblage|Coût indirect||Non|Frais généraux lettrés|Ajustement stock|  
|(Production) Production|Coût direct||Oui|Stocks (attente)|TEC|  
|(Production) Production|Coût direct||Non|STOCKS ET EN-COURS|TEC|  
|(Production) Production|Coût indirect||Non|STOCKS ET EN-COURS|Frais généraux lettrés|  
|(Production) Production|Ecart|Matière|Non|STOCKS ET EN-COURS|Ecarts matière|  
|(Production) Production|Ecart|Capacité|Non|STOCKS ET EN-COURS|Ecarts opératoires|  
|(Production) Production|Ecart|Sous-traitance|Non|STOCKS ET EN-COURS|Ecarts sous-traitance|  
|(Production) Production|Ecart|Frais généraux opératoires|Non|STOCKS ET EN-COURS|Ecarts frais généraux op.|  
|(Production) Production|Ecart|Frais généraux matière|Non|STOCKS ET EN-COURS|Ecarts frais généraux matière|  
|(Production) Production|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|(Production) Production|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Résultat d’assemblage|Coût direct||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Résultat d’assemblage|Réévaluation||Non|STOCKS ET EN-COURS|Ajustement stock|  
|Résultat d’assemblage|Coût indirect||Non|STOCKS ET EN-COURS|Frais généraux lettrés|  
|Résultat d’assemblage|Ecart|Matière|Non|STOCKS ET EN-COURS|Ecarts matière|  
|Résultat d’assemblage|Ecart|Capacité|Non|STOCKS ET EN-COURS|Ecarts opératoires|  
|Résultat d’assemblage|Ecart|Frais généraux opératoires|Non|STOCKS ET EN-COURS|Ecarts frais généraux op.|  
|Résultat d’assemblage|Ecart|Frais généraux matière|Non|STOCKS ET EN-COURS|Ecarts frais généraux matière|  
|Résultat d’assemblage|Arrondi||Non|STOCKS ET EN-COURS|Ajustement stock|  

## <a name="from-the-capacity-ledger" />À partir de la comptabilité capacité
 Le tableau suivant montre les relations entre les différents types d’écritures de valeur de capacité et les comptes et les comptes contrepartie dans la comptabilité. Les écritures comptables capacité représentent le temps de travail consommé dans l’assemblage ou la charge de production.  

|**Type travail**|**Type écriture comptable capacité**|**Type écriture valeur**|**Compte**|**Compte contrepartie**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Assemblage|Ressource|Coût direct|Coût direct lettré|Ajustement stock|  
|Assemblage|Ressource|Coût indirect|Frais généraux lettrés|Ajustement stock|  
|Production|Poste de charge/Centre de charge|Coût direct|Compte en-cours|Coût direct lettré|  
|Production|Poste de charge/Centre de charge|Coût indirect|Compte en-cours|Frais généraux lettrés|  

## <a name="assembly-costs-are-always-actual" />Les coûts d’assemblage sont toujours réels
 Comme indiqué dans le tableau ci-dessus, les validations d’assemblage ne sont pas représentées dans les comptes d’attente. Ceci est dû au fait que le concept de travail en cours (TEC) ne s’applique pas à la validation de résultats d’assemblage, contrairement à la validation des résultats de production. Les coûts d’assemblage sont uniquement validés en tant que coûts réels, jamais en tant que coûts prévus.  

 Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger" />Calcul du montant à valider dans la comptabilité
 Les champs suivants de la table **Ecritures valeur** permettent de calculer le coût total prévu qui est validé dans les écritures comptables :  

-   Coût total (réel)  
-   Coût validé en comptabilité  
-   Coût total (prévu)  
-   Coût prévu validé en comptabilité  

Le tableau suivant montre la manière dont les montants à valider en comptabilité sont calculés pour les deux types de coût différents.  

|Type coût|Calcul|  
|---------------|-----------------|  
|Coût réel|Coût total (réel) - Coût validé en comptabilité.|  
|Coût prévu|Coût total (prévu) - Coût prévu validé en comptabilité|  

## <a name="see-also" />Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : comptabilisation stock](design-details-inventory-posting.md)   
 [Détails de conception : validation du coût prévu](design-details-expected-cost-posting.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
