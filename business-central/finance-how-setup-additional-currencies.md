---
title: Configuration des devises supplémentaires
description: 'Votre comptabilité est configurée pour utiliser votre devise société (DS) et une autre devise est configurée comme devise supplémentaire, à laquelle est affecté un taux de change courant.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 07/23/2021
ms.author: edupont
---
# <a name="set-up-an-additional-reporting-currency" />Configurer une devise report supplémentaire

Les sociétés opérant dans un nombre croissant de pays/régions, il est de plus en plus important qu’elles puissent consulter et générer des états de données financiers dans plusieurs devises.

> [!NOTE]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], si vous recherchez des informations en temps réel sur les taux de devise étrangère (FX) ou les taux historiques, vous les trouverez sous la désignation de devise. En plus de cet article, consultez aussi [Mettre à jour les taux de change devise](finance-how-update-currencies.md).


Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change courant. Si vous désignez une deuxième devise comme « devise report supplémentaire », [!INCLUDE[prod_short](includes/prod_short.md)] enregistre automatiquement les montants d’état en DS et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d’autres écritures, telles que les écritures TVA.

> [!Warning]
> Il est déconseillé d’utiliser la fonctionnalité de devise report comme base pour une conversion d’état financier sauf si vous comprenez les limites. Cet outil ne permet pas d’effectuer une conversion d’états financiers de filiale étrangère dans le cadre d’une consolidation de société. La fonctionnalité de devise report peut uniquement être utilisée pour préparer des états dans une autre devise, comme s’il s’agissait de la devise société.
>
> Par exemple, vous avez un grand nombre de comptes clients en livres sterling (GBP) et vous avez configuré votre devise de déclaration supplémentaire (DR) en GBP. Dans ce scénario, les montants des comptes clients qui utilisent la livre sterling ne seront pas ajustés pour les gains/pertes de change dans la DR, mais uniquement les montants des comptes clients qui sont dans d’autres devises. Cela signifie que si vous utilisez la DR pour déclarer vos états financiers, cela peut entraîner des soldes impayés sous-estimés ou surestimés des comptes débiteurs.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency" />Affichage d’états et de montants dans la devise report
L’utilisation d’une devise report peut faciliter le processus de génération d’états d’une société dans les cas suivants :

- Sociétés situées dans des pays/régions extérieur(e)s à l’UE qui effectuent un grand nombre de transactions avec des sociétés situées dans des pays/régions de l’UE. Dans ce cas, la société extérieure à l’UE peut vouloir générer des états financiers en euros afin qu’ils soient plus lisibles pour les partenaires commerciaux de l’UE.
- Sociétés qui souhaitent pouvoir générer des états financiers dans une devise davantage utilisée au niveau international que leur devise société.

Plusieurs états financiers sont basés sur les écritures comptables. Pour afficher les données d’états en devise report supplémentaire, activez simplement le champ **Afficher montants en devise report** sur le raccourci **Options** pour l’état comptable approprié.

## <a name="adjusting-exchange-rates" />Ajustement des taux de change

Comme les taux de change ne cessent de fluctuer, il convient d’ajuster périodiquement les équivalents devise supplémentaires de votre système. À défaut d’effectuer ces ajustements, les montants convertis à partir de devises étrangères (ou supplémentaires) et publiés dans la comptabilité en DS risquent d’être erronés. En outre, les écritures quotidiennes validées avant la saisie d’un taux de change quotidien dans l’application doivent être mises à jour après la saisie des informations de taux de change quotidienne. Le traitement par lots **Ajuster taux de change** permet d’ajuster les taux de change d’écritures client, fournisseur et compte bancaire validées. Il peut également mettre à jour d’autres montants en devise report dans des écritures comptables. Pour plus d’informations, voir [Mettre à jour les taux de change devise](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency" />Configuration d’une devise report supplémentaire

Pour configurer une devise report supplémentaire, procédez comme suit :

- Spécifiez les comptes généraux pour la validation d’ajustements de taux de change.  
- Spécifiez la méthode d’ajustement de taux de change pour tous les comptes généraux.  
- Spécifiez la méthode d’ajustement de taux de change pour les écritures TVA.  
- Activez la devise report.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments" />Pour spécifier les comptes généraux pour la validation d’ajustements de taux de change

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devises**, puis choisissez le lien associé.  
2. Sur la page **Devises**, renseignez les champs suivants pour la devise report.  

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**Cpte gains constatés report**|Numéro du compte général sur lequel les gains de change sur ajustements de devise entre devise société et devise report sont validés.|  
|**Cpte pertes constatées report**|Numéro du compte général sur lequel les pertes de change sur ajustements de devise entre devise société et devise report sont validés.|  
|**Compte gains résiduels DR**|Compte général dans lequel les montants résiduels qui correspondent à des gains sont validés si vous validez dans le module de comptabilité en DS ainsi qu’en devise report.|  
|**Compte pertes résiduelles DR**|Compte général dans lequel les montants résiduels qui correspondent à des pertes sont validés si vous validez dans le module de comptabilité en DS ainsi qu’en devise report.|

> [!NOTE]  
>  Des montants résiduels peuvent apparaître lorsque [!INCLUDE[prod_short](includes/prod_short.md)] arrondit des montants débit et crédit convertis de DS en devise report.  

Pour chaque compte général, vous devez spécifier la manière dont les montants comptables du compte sont ajustés en fonction des fluctuations de taux de change entre DS et la devise report.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts" />Pour spécifier la méthode d’ajustement de taux de change pour tous les comptes généraux

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, sélectionnez le compte approprié, puis cliquez sur l’action **Modifier**.  
3. Sur la page **Fiche compte général**, sélectionnez la méthode adéquate dans le champ **Ajustement taux de change**.  

    Si vous validez dans une devise report, spécifiez, dans le champ **Ajustement taux de change**, la manière dont ce compte général est ajusté en fonction des fluctuations de taux de change entre DS et la devise report. Le tableau suivant répertorie les options au choix.  

    |Champ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Aucun ajustement**|Aucun ajustement de taux de change n’est effectué sur le compte général. C’est l’option par défaut.<br /><br /> **NOTE :** sélectionnez cette option si le taux de change entre DS et la devise report est toujours fixe.|  
    |**Ajuster montant**|La devise société est ajustée pour tous les gains ou toutes les pertes de change. Les gains ou pertes sur le taux de change sont validés dans le compte général, champ **Montant**, et dans les comptes que vous avez spécifiés pour les gains ou les pertes dans le champ **Cpte gains constatés report** et **Cpte pertes constatées report** de la page **Devises**.|  
    |**Ajuster montant devise report**|La devise report est ajustée pour les gains ou les pertes de change. Les gains ou pertes sur le taux de change sont validés dans le compte général, champ **Montant DR**, et dans les comptes que vous avez spécifiés pour les gains ou les pertes dans le champ **Cpte gains constatés report** et **Cpte pertes constatées report** de la page **Devises**.|  

    Les gains et les pertes en relation avec les taux de change sont validés lorsque vous exécutez le traitement par lots **Ajuster taux de change**. Dans le cadre de ce traitement par lots, le taux de change d’ajustement est identifié sur la page **Taux de change devise**, puis les montants des champs **Montant** et **Montant DR** de l’écriture comptable sont comparés afin de déterminer s’il y a gain ou perte sur le taux de change. Le traitement par lots utilise l’option que vous sélectionnez dans le champ **Ajustement taux de change** pour déterminer comment calculer et valider des gains ou des pertes sur le taux de change pour des comptes généraux.  

4.  Fermez la page **Fiche compte général**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries" />Pour spécifier la méthode d’ajustement de taux de change pour toutes les écritures TVA

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Paramètres comptabilité**, sélectionnez la méthode adéquate dans le champ **Ajustement tx de change TVA**.  
3. Si vous validez en devise report (DS), vous pouvez spécifier dans le champ **Ajustement taux de change TVA** la manière dont les comptes définis pour la validation de la TVA sur la page **Paramètres compta. TVA** sont ajustés pour les fluctuations de taux de change entre devise société et devise report.  

    Lorsque vous exécutez le traitement par lots **Ajuster taux de change**, le taux de change ajustement est identifié sur la page **Taux de change devise**, puis les montants des champs **Montant** et **Montant devise report** de l’écriture TVA sont comparés afin de déterminer s’il y a un gain ou une perte de change. Le traitement par lots utilise l’option sélectionnée dans ce champ pour déterminer la manière de valider les gains et pertes de change pour les comptes TVA.  

    Vous disposez des mêmes options qu’avec les écritures comptables mais, dans ce cas, les écritures ajustées sont les écritures TVA. Le tableau suivant répertorie les options au choix.

    |Champ|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Aucun ajustement**|Aucun ajustement de taux de change n’est effectué sur le compte général. C’est l’option par défaut.|  
    |**Ajuster montant**|La devise société est ajustée pour tous les gains ou toutes les pertes de change. Les gains ou pertes sur le taux de change sont validés dans le compte général, champ **Montant**, et dans les comptes que vous avez spécifiés pour les gains ou les pertes dans le champ **Cpte gains constatés report** et **Cpte pertes constatées report** de la page **Devises**.|  
    |**Ajuster montant devise report**|La devise report est ajustée pour les gains ou les pertes de change. Les gains ou pertes sur le taux de change sont validés dans le compte général, champ **Montant DR**, et dans les comptes que vous avez spécifiés pour les gains ou les pertes dans le champ **Cpte gains constatés report** et **Cpte pertes constatées report** de la page **Devises**.|  

### <a name="to-activate-the-additional-reporting-currency" />Pour activer la devise report
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Paramètres comptabilité**, choisissez le champ **Devise report (DR)** pour sélectionner la devise supplémentaire à utiliser pour vos états.  
3. Lorsque vous quittez le champ, [!INCLUDE[prod_short](includes/prod_short.md)] affiche un message de confirmation décrivant les effets de l’activation de la devise report.  
4. Cliquez sur **Oui** pour confirmer que vous souhaitez activer la devise.  
5. Le traitement par lots **Ajuster devise report** s’ouvre.

    Ce traitement par lots convertit les montants en devise société des écritures existantes en devise report. Le traitement par lots utilise un taux de change par défaut copié à partir du taux de change, qui est valide à la date de travail sur la page **Taux de change devise**. Les montants résiduels qui résultent d’une conversion de DS en devise report sont validés dans les comptes de gains et pertes résiduels spécifiés sur la page **Devises**. La date de comptabilisation et le numéro de document pour ces écritures sont les mêmes que pour l’écriture comptable originale. Une fois toutes ces écritures résiduelles validées, le traitement par lots valide une écriture arrondie à la date de clôture de chaque exercice clôturé dans le compte de bénéfices non répartis. Cela résulte de la nécessité de s’assurer que le solde de clôture des comptes produit pour chaque exercice clôturé est 0 tant en DS que dans la devise report.
6. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Pour lancer le traitement par lots, cliquez sur le bouton **OK**.  

Après exécution du traitement par lots, les montants des écritures existantes suivantes sont exprimés en DS et dans la devise report :  

- Écritures comptables  
- Écritures lettrage article  
- Écritures TVA  
- Écritures comptables projet  
- Écritures valeur  
- Lignes ordre de fabrication  
- Écritures comptables ordre de fabrication  

En outre, toutes les écritures futures du même type ont des montants enregistrés en DS et dans la devise report.  

> [!NOTE]  
> Le champ **Devise report** n’est activé qu’après que vous avez cliqué sur le bouton **OK** dans le traitement par lots **Ajuster devise report**.  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/paths/use-multiple-currencies-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Mettre à jour des taux de change devise](finance-how-update-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
