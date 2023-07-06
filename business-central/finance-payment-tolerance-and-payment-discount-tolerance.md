---
title: Écart de règlement et écart d’escompte
description: Cet article explique comment configurer l’écart de règlement de manière à fermer une facture lorsque le paiement ne couvre pas entièrement le montant de la facture.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '118, 314, 395'
ms.date: 04/03/2023
ms.author: edupont
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a><a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a><a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Utilisation des écarts de règlement et des écarts d’escompte

Vous pouvez configurer l’écart de règlement de manière à fermer une facture lorsque le paiement ne couvre pas entièrement le montant de la facture. Par exemple, les écarts de règlement concernent généralement de petits montants qui coûteraient plus cher à corriger qu’à accepter. Vous pouvez configurer un écart de règlement pour accorder un escompte après expiration de la date d’escompte.  

Vous pouvez utiliser les écarts de règlement pour qu’un écart de règlement maximum autorisé soit défini pour chaque montant en commande. Si l’écart de règlement est rempli, le montant règlement est analysé. Si le montant règlement est un moins-perçu, alors le montant en commande est totalement clôturé par le moins-perçu. Une écriture comptable détaillée est validée dans l’écriture règlement de sorte qu’il ne subsiste aucun montant ouvert dans l’écriture facture lettrée. Si le montant règlement est un trop-perçu, alors une nouvelle écriture comptable détaillée est validée dans l’écriture règlement de sorte qu’il ne subsiste aucun montant ouvert dans l’écriture règlement.

Vous pouvez utiliser des écarts d’escompte au cas où vous accepteriez un escompte après la date d’escompte, alors il sera toujours validé dans le compte escompte ou dans un compte écart de règlement.

## <a name="applying-payment-tolerance-to-multiple-documents"></a><a name="applying-payment-tolerance-to-multiple-documents"></a><a name="applying-payment-tolerance-to-multiple-documents"></a>Lettrage de l’écart de règlement sur plusieurs documents

Un document unique comporte le même écart de règlement, qu’il soit lettré seul ou avec d’autres documents. L’acceptation d’un escompte tardif, lorsque vous appliquez l’écart de règlement à plusieurs documents, se produit automatiquement pour chaque document où la règle suivante est vraie :  

*date d’escompte < date de règlement dans l’écriture sélectionnée <= date d’écart de règlement*  

Cette règle détermine également la nécessité d’afficher des alertes lorsque vous appliquez l’écart de règlement à plusieurs documents. L’alerte liée à l’écart d’escompte s’affiche pour chaque écriture répondant aux critères de date. Pour plus d’informations, reportez-vous à [Exemple 2 - Calculs de l’écart pour plusieurs documents](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Vous pouvez afficher une alerte en fonction des situations relatives à l’écart.  

- La première alerte concerne l’écart d’escompte. Vous êtes informé que vous pouvez accepter un escompte tardif. Vous pouvez ensuite décider s’il faut accepter l’écart sur la date d’escompte.  
- La seconde alerte concerne l’écart de règlement. Vous êtes informé que toutes les écritures peuvent être clôturées car la différence est inférieure à l’écart de règlement maximum pour les écritures lettrées. Vous pouvez ensuite décider s’il faut accepter l’écart sur la date de règlement.

> [!NOTE]
> L’activation du message d’avertissement vous permettra de choisir comment traiter les paiements dans les limites de la tolérance. Si vous n’activez pas le message et qu’un niveau de tolérance est spécifié, les factures dont les montants se situent dans la tolérance seront automatiquement fermées et vous ne pourrez pas choisir de laisser le montant restant. 

Pour plus d’informations, voir [Pour activer ou désactiver l’alerte d’écart de règlement](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a><a name="to-set-up-tolerances"></a><a name="to-set-up-tolerances"></a>Pour configurer les écarts

L’écart au niveau des jours et des montants vous permet de fermer une facture même si le paiement ne couvre pas entièrement le montant de la facture. Par exemple, parce que la date d’échéance de l’escompte de paiement a été dépassée, des marchandises ont été déduites ou à cause d’une erreur mineure. Ceci est également vrai pour les remboursements et les avoirs.  

Pour configurer l’écart, vous devez configurer plusieurs comptes écart, spécifier des méthodes de comptabilisation d’écart escompte et d’écart règlement, puis exécuter le traitement par lots **Modifier écart de règlement**.  
1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilisation**, puis choisissez le lien associé.  
2. Sur la page **Paramètres comptabilisation**, configurez un compte écart règlement crédit et débit pour les ventes et un autre pour les achats.  
3. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. client**, puis choisissez le lien associé.    
4. Sur la page **Groupes compta. client**, configurez un compte écart règlement débit et un compte écart règlement crédit. Pour plus d’informations, voir [Configuration de groupes comptabilisation](finance-posting-groups.md).  
5. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration compta. fournisseur**, puis choisissez le lien associé.  
6. Sur la page **Groupes compta. fournisseur**, configurez un compte écart règlement débit et un compte écart règlement crédit.  
7. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.  
8. Ouvrez la page **Paramètres comptabilité**.  
9. Sur le raccourci **Lettrage**, renseignez les champs **Validation écart d’escompte**, **Période carence escompte** et **Validation écart de règlement**.   
10. Choisissez l’action **Modifier écart de règlement**.

    > [!NOTE]
    > Lorsque vous sélectionnez **Au plus ancien** dans le champ **Mode de lettrage** sur une page **Fiche client**, [!INCLUDE[prod_short](includes/prod_short.md)] n’affichera pas automatiquement les tolérances de paiement, même lorsqu’elles sont dans les seuils définis sur la page **Paramètres comptabilité**. [!INCLUDE[prod_short](includes/prod_short.md)] suppose que le paramètre Au plus ancien indique que le client (ou vous en tant que client de votre fournisseur) a un compte chez vous où il paie régulièrement le solde. Par conséquent, les montants restants ne doivent pas être supprimés en enregistrant une écriture d’écart de paiement.

11. Sur la page **Modifier écart de règlement**, renseignez les champs **% écart de règlement** et **Montant écart règlement max.**, puis cliquez sur le bouton **OK**.

> [!IMPORTANT]  
> Vous n’avez configuré l’écart que pour la devise société. Si vous souhaitez que [!INCLUDE[prod_short](includes/prod_short.md)] gère l’écart pour les paiements, les avoirs et les remboursements en devise étrangère, vous devez exécuter le traitement par lots **Modifier écart de règlement** avec une valeur dans le champ **Code devise**.  

> [!NOTE]  
> Si vous souhaitez recevoir une alerte écart règlement chaque fois que vous validez un lettrage dans l’écart, vous devez activer l’alerte écart règlement. Pour plus d’informations, voir [Pour activer ou désactiver l’alerte d’écart de règlement](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
> Pour désactiver l’écart pour un client ou un fournisseur, vous devez bloquer les écarts sur la fiche client ou fournisseur correspondante. Pour plus d’informations, voir [Pour bloquer l’écart règlement pour des clients](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
> Lorsque vous configurez un écart, [!INCLUDE[prod_short](includes/prod_short.md)] vérifie s’il existe des écritures ouvertes et calcule l’écart pour ces écritures.

> [!IMPORTANT]  
> Lorsque vous activez le champ **Ajuster pour escompte** sur la page **Paramètres comptabilisation TVA**, le montant de la TVA est pris en compte puisqu’il est associé aux montants **Écarts de paiement** et **Escomptes**, et la TVA sera déduite pour les deux montants de transaction, s’ils existent. Le système ne peut pas être configuré pour utiliser la réduction de TVA uniquement pour un type de transaction.  

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a><a name="to-enable-or-disable-payment-tolerance-warnings"></a><a name="to-enable-or-disable-payment-tolerance-warnings"></a>Pour activer ou désactiver les alertes d’écart de règlement

L’alerte écart règlement apparaît lorsque vous validez un lettrage dont le solde se situe dans l’écart autorisé. Vous pouvez alors choisir comment valider et journaliser le solde.    
1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Paramètres comptabilité**, sur le raccourci **Application**, activez le bouton bascule **Alerte écart de règlement** pour activer l’alerte. Pour désactiver l’avertissement, désactivez le bouton bascule.  

> [!NOTE]  
> L’option par défaut de la page **Alerte écart de règlement** est **Laisser le solde ouvert**. L’option par défaut de la page **Alerte écart d’escompte** est **Ne pas accepter d’escompte tardif**.

## <a name="to-block-payment-tolerance-for-customers"></a><a name="to-block-payment-tolerance-for-customers"></a><a name="to-block-payment-tolerance-for-customers"></a>Pour bloquer l’écart règlement pour des clients

Par défaut, un écart règlement est accordé. Pour ne pas accorder un écart règlement à un certain client ou fournisseur, vous devez bloquer l’écart sur la fiche fournisseur ou client appropriée. Ce qui suit décrit comment l’exécuter pour un client. La procédure est identique pour un fournisseur.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Client** ou **Fournisseur**, puis choisissez le lien associé.  
2. Sur le raccourci **Paiements**, cochez la case **Bloquer écart de règlement**.  

> [!NOTE]  
> Si le client ou le fournisseur possède des écritures ouvertes, vous devez d’abord supprimer l’écart règlement des écritures actuellement ouvertes.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a><a name="example-1---tolerance-calculations-for-a-single-document"></a><a name="example-1---tolerance-calculations-for-a-single-document"></a>Exemple 1 - Calculs de l’écart pour un seul document

Voici quelques exemples de scénarios illustrant les calculs et comptabilisations d’écart qui sont effectués dans différentes situations.  

La page **Configuration comptabilité** contient le paramétrage suivant :
- Période carence escompte : 5D  
- Ecart de règlement max : 5  

Scénarios comportant deux alternatives, A et B. En voici la signification :  

- **A** L’alerte écart d’escompte a été désactivée OU l’alerte est activée, mais l’utilisateur a accepté l’escompte tardif (Valider le solde en tant qu’écart de règlement).  
- **B** L’alerte est activée et l’utilisateur a choisi de ne pas accepter l’escompte tardif (Laisser le solde ouvert).  

|—|Fact.|Escompte|Écart de règlement maximal|Date d’escompte|Date d’écart d’escompte|Date règl.|Règlement|Type d’écart|Toutes les écritures clôturées|Écart d’escompte Cpta/CL|Écart de règlement comptable|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1 000|20|5|15/01/03|20/01/03|<=15/01/03|985|PaymentTolerance|Oui|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Aucun**|**Oui**|**0**|**0**|  
|3|1 000|20|5|15/01/03|c|<=15/01/03|975|PaymentTolerance|Oui|0|5|  
|4A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|PaymentDiscountTolerance|Non, 25 sur le règlement|20/-20|0|  
|5A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1000|PaymentDiscountTolerance|Non, 20 sur le règlement|20/-20|0|  
|6A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|PaymentDiscountTolerance|Non, 15 sur le règlement|20/-20|0|  
|4B|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|PaymentTolerance|Oui|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 20/01/03**|**1000**|**Aucun**|**Oui**|**0**|**0**|  
|6B|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|PaymentTolerance|Oui|0|5|  
|7|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|985|PaymentDiscountTolerance et PaymentTolerance|Oui|20/-20|-5|  
|8|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|980|PaymentDiscountTolerance|Oui|20/-20|0|  
|9|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|975|PaymentDiscountTolerance et PaymentTolerance|Oui|20/-20|5|  
|10|1 000|20|5|15/01/03|20/01/03|>20/01/03|1005|PaymentTolerance|Oui|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Aucun**|**Oui**|**0**|**0**|  
|12|1 000|20|5|15/01/03|20/01/03|>20/01/03|995|PaymentTolerance|Oui|0|5|  
|13|1 000|20|5|15/01/03|20/01/03|>20/01/03|985|Aucun|Non, 15 sur la facture|0|0|  
|14|1 000|20|5|15/01/03|20/01/03|>20/01/03|980|Aucune|Non, 20 sur la facture|0|0|  
|15|1 000|20|5|15/01/03|20/01/03|>20/01/03|975|Aucune|Non, 25 sur la facture|0|0|  

### <a name="payment-range-diagrams"></a><a name="payment-range-diagrams"></a><a name="payment-range-diagrams"></a>Schémas de chaîne de paiement

Sur la base du scénario ci-avant, les diagrammes des plages de dates de règlement se présentent sous la forme suivante :  

#### <a name="1-payment-date-011503-scenarios-1-3"></a><a name="1-payment-date-011503-scenarios-1-3"></a><a name="1-payment-date-011503-scenarios-1-3"></a>(1) Date de règlement <=15/01/03 (scénarios 1-3)

Montant ouvert par  

Règles de lettrage normales  

![Règles sur les écarts de règlement uniques 1.](media/singlePmtTolRules_Pre1503.gif "Règles sur les écarts de règlement uniques 1")  

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a><a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a><a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) La date de règlement est comprise entre le 16/01/03 et le 20/01/03 (scénarios 4-9).

Montant ouvert par  

Règles de lettrage normales  

![Règles sur les écarts de règlement uniques 2.](media/singlePmtTolRules_GracePeriod.gif "Règles sur les écarts de règlement uniques 2")  

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a><a name="3-payment-date-is-after-012003-scenarios-10-15"></a><a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) La date de règlement est située après le 20/01/03 (scénarios 10-15).

Montant ouvert par  

Règles de lettrage normales  

![Règles sur les écarts de règlement uniques 3.](media/singlePmtTolRules_Post0120.gif "Règles sur les écarts de règlement uniques 3")  

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a><a name="example-2---tolerance-calculations-for-multiple-documents"></a><a name="example-2---tolerance-calculations-for-multiple-documents"></a>Exemple 2 - Calculs de l’écart pour plusieurs documents

Voici quelques exemples de scénarios illustrant les calculs et comptabilisations d’écart qui sont effectués dans différentes situations. Ces exemples se limitent aux scénarios permettant à toutes les écritures du lettrage d’être clôturées.  

La page **Configuration comptabilité** contient le paramétrage suivant :
- Période carence escompte 5D  
- Ecart de règlement max 5  

Scénarios comportant deux alternatives, A, B, C ou D. En voici la signification :  

- **A** L’alerte écart d’escompte a été désactivée OU l’alerte est activée, mais l’utilisateur a accepté l’escompte tardif (Valider en tant qu’écart) pour toutes les factures.  
- **B** L’alerte est activée et l’utilisateur a choisi de n’accepter l’escompte tardif pour aucune des factures.  
- **C** : L’alerte est activée et l’utilisateur a choisi d’accepter l’escompte tardif pour la première facture, mais non pour la deuxième.  
- **D** : L’alerte est activée et l’utilisateur a choisi de ne pas accepter l’escompte tardif pour la première facture, mais de l’accepter pour la seconde.  

|—|Fact.|Escompte|Écart de règlement maximal|Date d’escompte|Date d’écart d’escompte|Date règl.|Règlement|Type d’écart|Toutes les écritures clôturées|Écart d’escompte Cpta/CL|Écart de règlement comptable|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|PaymentTolerance|Oui|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Aucun**|**Oui**|**0**<br /><br /> **0**|0 <br />0|  
|3|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|PaymentTolerance|Oui|0<br /><br /> 0|5 <br />5|  
|4B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|PaymentTolerance|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 17/01/03**|**1970**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|PaymentTolerance|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|PaymentDiscountTolerance et PaymentTolerance|Oui|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|PaymentDiscountTolerance|Oui|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|PaymentDiscountTolerance et PaymentTolerance|Oui|60/60|5 <br />5|  
|10B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|PaymentTolerance|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 20/01/03**|**2000**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|PaymentTolerance|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|PaymentDiscountTolerance et PaymentTolerance|Oui|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|PaymentDiscountTolerance|Oui|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|PaymentDiscountTolerance et PaymentTolerance|Oui|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|PaymentDiscountTolerance et PaymentTolerance|Oui|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|PaymentDiscountTolerance|Oui|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|PaymentDiscountTolerance et PaymentTolerance|Oui|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|PaymentDiscountTolerance et PaymentTolerance|Oui|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|PaymentDiscountTolerance|Oui|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|PaymentDiscountTolerance et PaymentTolerance|Oui|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|PaymentTolerance|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 22/01/03**|**2000**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|PaymentTolerance|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|PaymentDiscountTolerance et PaymentTolerance|Oui|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|PaymentDiscountTolerance|Oui|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|PaymentDiscountTolerance et PaymentTolerance|Oui|0/0<br /><br /> 30/30|5 <br />5|  
|28|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|PaymentTolerance|Oui|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Aucun**|**Oui**|**0**|**0**|  
|30|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|PaymentTolerance|Oui|0|5|  

### <a name="payment-range-diagrams-1"></a><a name="payment-range-diagrams-1"></a><a name="payment-range-diagrams-1"></a>Schémas de chaîne de paiement

Sur la base du scénario ci-avant, les diagrammes des plages de dates de règlement se présentent sous la forme suivante :  

#### <a name="1-payment-date-011503-scenarios-1-3-1"></a><a name="1-payment-date-011503-scenarios-1-3-1"></a><a name="1-payment-date-011503-scenarios-1-3-1"></a>(1) Date de règlement <=15/01/03 (scénarios 1-3)

Montant ouvert par  

Règles de lettrage normales  

:::image type="content" source="media/multiplePmtTolRules_Pre1503.gif" alt-text="Règles sur les écarts de règlement multiples 1a":::

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a><a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a><a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) La date de règlement est comprise entre le 16/01/03 et le 17/01/03 (scénarios 4-9).

Montant ouvert par  

Règles de lettrage normales  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1-2.gif" alt-text="Règles sur les écarts de règlement multiples 2":::

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a><a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a><a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) La date de règlement est comprise entre le 18/01/03 et le 20/01/03 (scénarios 10-21).

Montant ouvert par  

Règles de lettrage normales  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1.gif" alt-text="Règles sur les écarts de règlement multiples 3":::

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a><a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a><a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) La date de règlement est comprise entre le 21/01/03 et le 22/01/03 (scénarios 22-27).

Montant ouvert par  

Règles de lettrage normales  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv2.gif" alt-text="Règles sur les écarts de règlement multiples 4":::

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a><a name="5-payment-date-is-after-012203-scenarios-28-30"></a><a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) La date de règlement est située après le 22/01/03 (scénarios 28-30).

Montant ouvert par  

Règles de lettrage normales  

:::image type="content" source="media/multiplePmtTolRules_Post0122.gif" alt-text="Règles sur les écarts de règlement multiples 5":::

(1) Si le règlement intervient dans l’une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l’une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/enter-payments-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
