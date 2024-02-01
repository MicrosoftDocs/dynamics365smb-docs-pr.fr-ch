---
title: "Détails de conception\_-\_Validation du coût prévu"
description: 'Les coûts prévus représentent l’estimation, par exemple, du coût d’un article acheté que vous enregistrez avant la réception de la facture de cet article.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-expected-cost-posting"></a>Détails de conception : validation du coût prévu
Les coûts prévus représentent l’estimation, par exemple, du coût d’un article acheté que vous enregistrez avant la réception de la facture de cet article.  

 Vous pouvez valider les coûts prévus dans le stock et dans la comptabilité. Lorsque vous validez une quantité qui est uniquement reçue ou expédiée mais pas facturée, une écriture valeur est créée avec le coût prévu. Ce coût prévu affecte la valeur du stock mais n’est pas porté au compte général, sauf si vous avez paramétré le programme à cette fin.  

> [!NOTE]  
>  Les coûts prévus sont gérés uniquement pour des transactions article. Les coûts prévus ne sont pas pour des types de transaction négligeables, tels que la capacité et les frais annexes.  

 Si seulement la partie de quantité d’une entrée de stock a été validée, la valeur du stock de la comptabilité ne change pas, sauf si vous avez sélectionné la case à cocher **Compta. coûts prévus** sur la page **Paramètres stock**. Dans ce cas, le coût prévu est validé dans les comptes d’attente au moment de la réception. Une fois que la réception a été entièrement facturée, les comptes d’attente sont ensuite équilibrés et le coût réel est validé dans le compte stock.  

 Pour prendre en charge le travail de rapprochement et de traçabilité, l’écriture valeur facturée montre que le montant du coût prévu validé pour équilibrer les comptes d’attente.  

## <a name="prerequisites-for-posting-expected-costs"></a>Conditions préalables à la validation des coûts prévus

Pour rendre possible la validation des coûts prévus, vous devez procéder comme suit :
1. Dans la page **Paramètres stock**, cochez la case **Compta. coûts automatique** et la case **Compta. coûts prévus**.
2. Configurez les comptes d’attente à utiliser pendant le processus de validation des coûts prévus.  

  Dans la page **Paramètres compta. stock**, vérifiez les champs **Compte stocks** et **Compte stocks (attente)** pour le **Code magasin et Code groupe compta. stock** de l’article que vous allez acheter. Pour en savoir plus sur ces comptes, voir [Détails de conception - Comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).
3. Dans la page **Paramètres comptabilisation**, vérifiez le champ **Compte ajust. stock (attente)** pour le **Groupe compta. marché** et le **Groupe compta. produit** que vous utiliserez.
4. Lorsque vous créez une commande achat, la valeur par défaut est que le champ **N° facture fournisseur** est requis. Vous devez le désactiver dans la page **Paramètres achats**, en désélectionnant le champ **N° doc. ext. obligatoire**.

## <a name="example"></a>Exemple :

> [!NOTE]  
> Les numéros de compte utilisés dans cet exemple servent uniquement de référence et seront différents dans votre système. Configurez-les comme indiqué dans les conditions préalables ci-dessus.

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

|Date comptabilisation|Compte général|N° de compte (uniquement des exemples !)|Montant|Numéro de la séquence|  
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
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
