---
title: "Écart de règlement et écart d'escompte | Microsoft Docs"
description: "Vous pouvez configurer l'écart de règlement de manière à fermer une facture lorsque le paiement ne couvre pas entièrement le montant de la facture."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: feae398e064a03d01903fcc65c6f4d99be8374a2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Utilisation des écarts de règlement et des écarts d'escompte
Vous pouvez configurer un écart de règlement de manière à fermer une facture lorsque le paiement ne couvre pas entièrement le montant de la facture. Vous pouvez configurer un écart de règlement pour accorder un escompte après expiration de la date d'escompte.  

Vous pouvez utiliser les écarts de règlement pour qu'un écart de règlement maximum autorisé soit défini pour chaque montant en commande. Si l'écart de règlement est rempli, le montant règlement est analysé. Si le montant règlement est un moins-perçu, alors le montant en commande est totalement clôturé par le moins-perçu. Une écriture comptable détaillée est validée dans l'écriture règlement de sorte qu'il ne subsiste aucun montant ouvert dans l'écriture facture lettrée. Si le montant règlement est un trop-perçu, alors une nouvelle écriture comptable détaillée est validée dans l'écriture règlement de sorte qu'il ne subsiste aucun montant ouvert dans l'écriture règlement.

Vous pouvez utiliser des écarts d'escompte au cas où vous accepteriez un escompte après la date d'escompte, alors il sera toujours validé dans le compte escompte ou dans un compte écart de règlement.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Application de l'écart de règlement à plusieurs documents  
Un document unique comporte le même écart de règlement, qu'il soit lettré seul ou avec d'autres documents. L'acceptation d'un escompte tardif, lorsque vous appliquez l'écart de règlement à plusieurs documents, se produit automatiquement pour chaque document où la règle suivante est vraie :  

*date d'escompte < date de règlement dans l'écriture sélectionnée <= date d'écart de règlement*  

Cette règle détermine également la nécessité d'afficher des alertes lorsque vous appliquez l'écart de règlement à plusieurs documents. L'alerte liée à l'écart d'escompte s'affiche pour chaque écriture répondant aux critères de date. Pour plus d'informations, reportez-vous à la section « Exemple 2 - Calculs de l'écart pour plusieurs documents ».

Vous pouvez afficher une alerte en fonction des situations relatives à l'écart.  

- La première alerte concerne l'écart d'escompte. Vous êtes informé que vous pouvez accepter un escompte tardif. Vous pouvez ensuite décider s'il faut accepter l'écart sur la date d'escompte.  
- La seconde alerte concerne l'écart de règlement. Vous êtes informé que toutes les écritures peuvent être clôturées car la différence est inférieure à l'écart de règlement maximum pour les écritures lettrées. Vous pouvez ensuite décider s'il faut accepter l'écart sur la date de règlement.

Pour plus d'informations, voir la section « Comment activer ou désactiver les alertes d'écart de règlement ».     

## <a name="to-set-up-tolerances"></a>Pour configurer les écarts  
Le fait de configurer des écarts pour la date ou le montant permet de fermer une facture alors que le règlement ne couvre pas le montant indiqué sur la facture, que ce soit parce que l'échéance de l'escompte est dépassée ou que des marchandises ont été déduites, ou suite à une erreur anodine. Ceci est également vrai pour les remboursements et les avoirs.  

Pour configurer l'écart, vous devez configurer plusieurs comptes écart, spécifier des méthodes de comptabilisation d'écart escompte et d'écart règlement, puis exécuter le traitement par lots **Modifier écart de règlement**.  
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilisation**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Paramètres comptabilisation**, configurez un compte écart règlement crédit et débit pour les ventes et un autre pour les achats.  
3. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Groupes compta. client**, puis choisissez le lien associé.    
4. Dans la fenêtre **Groupes compta. client**, configurez un compte écart règlement débit et un compte écart règlement crédit. Pour plus d'informations, voir [Configuration de groupes comptabilisation](finance-posting-groups.md).  
5. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilisation fournisseur**, puis choisissez le lien associé.  
6. Dans la fenêtre **Groupes compta. fournisseur**, configurez un compte écart règlement débit et un compte écart règlement crédit.  
7. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilité**, puis sélectionnez le lien connexe.  
8. Ouvrez la fenêtre **Paramètres comptabilité**.  
9. Sur le raccourci **Application**, renseignez les champs **Validation écart d'escompte**, **Période carence escompte** et **Validation écart de règlement**.   
10. Choisissez l'action **Modifier écart de règlement**.
11. Dans la fenêtre **Modifier écart de règlement**, renseignez les champs **% écart de règlement** et **Montant écart règlement max.**, puis cliquez sur le bouton **OK**.

> [!IMPORTANT]  
>  Vous n'avez configuré l'écart que pour la devise société. Si vous souhaitez que [!INCLUDE[d365fin](includes/d365fin_md.md)] gère l'écart pour les paiements, les avoirs et les remboursements en devise étrangère, vous devez exécuter le traitement par lots **Modifier écart de règlement** avec une valeur dans le champ **Code devise**.  

> [!NOTE]  
>  Si vous souhaitez recevoir une alerte écart règlement chaque fois que vous validez un lettrage dans l'écart, vous devez activer l'alerte écart règlement. Pour plus d'informations, voir la section « Comment activer ou désactiver les alertes d'écart de règlement ».  
>   
>  Pour désactiver l'écart pour un client ou un fournisseur, vous devez bloquer les écarts sur la fiche client ou fournisseur correspondante. Pour plus d'informations, voir la section « Pour bloquer l'écart règlement pour des clients ».  
>   
>  Lorsque vous configurez un écart, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie s'il existe des écritures ouvertes et calcule l'écart pour ces écritures.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Pour activer ou désactiver les alertes d'écart de règlement
L'alerte écart règlement apparaît lorsque vous validez un lettrage dont le solde se situe dans l'écart autorisé. Vous pouvez alors choisir comment valider et journaliser le solde.    
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilité**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Paramètres comptabilité**, sur le raccourci **Application**, cochez la case **Alerte écart de règlement** pour activer l'alerte. Pour désactiver l'alerte, désactivez la case à cocher.  

> [!NOTE]  
>  L'option par défaut de la fenêtre **Alerte écart de règlement** est **Laisser le solde ouvert**. L'option par défaut de la fenêtre **Alerte écart d'escompte** est **Ne pas accepter d'escompte tardif**.

## <a name="to-block-payment-tolerance-for-customers"></a>Pour bloquer l'écart règlement pour des clients  
Par défaut, un écart règlement est accordé. Pour ne pas accorder un écart règlement à un certain client ou fournisseur, vous devez bloquer l'écart sur la fiche fournisseur ou client appropriée. Ce qui suit décrit comment l'exécuter pour un client. La procédure est identique pour un fournisseur.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Client** ou **Fournisseur**, puis sélectionnez le lien connexe.  
2. Sur le raccourci **Paiements**, cochez la case **Bloquer écart de règlement**.  

> [!NOTE]  
>  Si le client ou le fournisseur possède des écritures ouvertes, vous devez d'abord supprimer l'écart règlement des écritures actuellement ouvertes.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Exemple 1 - Calculs de l'écart pour un seul document
Voici quelques exemples de scénarios illustrant les calculs et comptabilisations d'écart qui sont effectués dans différentes situations.  

La fenêtre **Configuration comptabilité** contient le paramétrage suivant :
- Période carence escompte : 5D  
- Ecart de règlement max : 5  

Scénarios comportant deux alternatives, A et B. En voici la signification :  

- **A** L'alerte écart d'escompte a été désactivée OU l'alerte est activée, mais l'utilisateur a accepté l'escompte tardif (Valider le solde en tant qu'écart de règlement).  
- **B** L'alerte est activée et l'utilisateur a choisi de ne pas accepter l'escompte tardif (Laisser le solde ouvert).  

[!div class="mx-tdBreakAll"]  
|—|Fact.|Si le champ Ajust.|Ecart règl. max.|Date d'escompte|Ecart d'escompte Date|Date de règlement|Règl.|Type d'écart|Toutes les écritures clôturées|Ecart d'escompte Cpta/CL|Ecart de règlement Comptabilité|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1 000|20|5|15/01/03|20/01/03|<=15/01/03|985|Ecart règl.|Oui|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Aucun**|**Oui**|**0**|**0**|  
|3|1 000|20|5|15/01/03|c|<=15/01/03|975|Ecart règl.|Oui|0|5|  
|4A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Ecart d'escompte|Non, 25 sur Règl.|20/-20|0|  
|5A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1000|Ecart d'escompte|Non, 20 sur Règl.|20/-20|0|  
|6A|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Ecart d'escompte|Non, 15 sur Règl.|20/-20|0|  
|4B|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Ecart règl.|Oui|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 20/01/03**|**1000**|**Aucun**|**Oui**|**0**|**0**|  
|6B|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Ecart règl.|Oui|0|5|  
|7|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|985|Ecart d'escompte & Écart règlement|Oui|20/-20|-5|  
|8|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|980|Ecart d'escompte|Oui|20/-20|0|  
|9|1 000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|975|Ecart d'escompte & Écart règlement|Oui|20/-20|5|  
|10|1 000|20|5|15/01/03|20/01/03|>20/01/03|1005|Ecart règl.|Oui|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Aucun**|**Oui**|**0**|**0**|  
|12|1 000|20|5|15/01/03|20/01/03|>20/01/03|995|Ecart règl.|Oui|0|5|  
|13|1 000|20|5|15/01/03|20/01/03|>20/01/03|985|Aucune|Non, 15 sur la facture|0|0|  
|14|1 000|20|5|15/01/03|20/01/03|>20/01/03|980|Aucune|Non, 20 sur la facture|0|0|  
|15|1 000|20|5|15/01/03|20/01/03|>20/01/03|975|Aucune|Non, 25 sur la facture|0|0|  

### <a name="payment-range-diagrams"></a>Schémas de chaîne de paiement  
Sur la base du scénario ci-avant, les diagrammes des plages de dates de règlement se présentent sous la forme suivante :  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Date de règlement <=15/01/03 (scénarios 1-3)  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement uniques &#40;before 03&#47;15&#41;](media/singlePmtTolRules(Pre1503).gif "singlePmtTolRules(Pre1503)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) La date de règlement est comprise entre le 16/01/03 et le 20/01/03 (scénarios 4-9).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement uniques &#40;grace period&#41;](media/singlePmtTolRules(GracePeriod).gif "singlePmtTolRules(GracePeriod)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) La date de règlement est située après le 20/01/03 (scénarios 10-15).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement uniques &#40;before 01&#47;20&#41;](media/singlePmtTolRules(Post0120).gif "singlePmtTolRules(Post0120)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Exemple 2 - Calculs de l'écart pour plusieurs documents
Voici quelques exemples de scénarios illustrant les calculs et comptabilisations d'écart qui sont effectués dans différentes situations. Ces exemples se limitent aux scénarios permettant à toutes les écritures du module d'être clôturées.  

La fenêtre **Configuration comptabilité** contient le paramétrage suivant :
- Période carence escompte 5D  
- Ecart de règlement max 5  

Scénarios comportant deux alternatives, A, B, C ou D. En voici la signification :  

- **A** L'alerte écart d'escompte a été désactivée OU l'alerte est activée, mais l'utilisateur a accepté l'escompte tardif (Valider en tant qu'écart) pour toutes les factures.  
- **B** L'alerte est activée et l'utilisateur a choisi de n'accepter l'escompte tardif pour aucune des factures.  
- **C** : L'alerte est activée et l'utilisateur a choisi d'accepter l'escompte tardif pour la première facture, mais non pour la deuxième.  
- **D** : L'alerte est activée et l'utilisateur a choisi de ne pas accepter l'escompte tardif pour la première facture, mais de l'accepter pour la seconde.  

[!div class="mx-tdBreakAll"]  

|—|Fact.|Escompte|Ecart règl. max.|Date d'escompte|Ecart d'escompte Date|Date règl.|Règl.|Type d'écart|Toutes les écritures clôturées|Ecart d'escompte Cpta/CL|Ecart de règlement Comptabilité|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|Ecart règl.|Oui|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Aucun**|**Oui**|**0**<br /><br /> **0**|0 <br />0|  
|3|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|Ecart règl.|Oui|0<br /><br /> 0|5 <br />5|  
|4B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|Ecart règl.|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 17/01/03**|**1970**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|Ecart règl.|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|Ecart d'escompte & Écart règlement|Oui|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|Ecart escompte|Oui|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|Ecart d'escompte & Écart règlement|Oui|60/60|5 <br />5|  
|10B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|Ecart règl.|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 20/01/03**|**2000**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|Ecart règl.|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|Ecart d'escompte & Écart règlement|Oui|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|Ecart escompte|Oui|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|Ecart d'escompte & Écart règlement|Oui|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|Ecart d'escompte & Écart règlement|Oui|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|Ecart escompte|Oui|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|Ecart d'escompte & Écart règlement|Oui|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|Ecart d'escompte & Écart règlement|Oui|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|Ecart escompte|Oui|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|Ecart d'escompte & Écart règlement|Oui|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|Ecart règl.|Oui|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 22/01/03**|**2000**|**Aucun**|**Oui**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|Ecart règl.|Oui|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|Ecart d'escompte & Écart règlement|Oui|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|Ecart escompte|Oui|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|Ecart d'escompte & Écart règlement|Oui|0/0<br /><br /> 30/30|5 <br />5|  
|28|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|Ecart règl.|Oui|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Aucun**|**Oui**|**0**|**0**|  
|30|1 000 <br />1 000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|Ecart règl.|Oui|0|5|  

### <a name="payment-range-diagrams"></a>Schémas de chaîne de paiement  
Sur la base du scénario ci-avant, les diagrammes des plages de dates de règlement se présentent sous la forme suivante :  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Date de règlement <=15/01/03 (scénarios 1-3)  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement multiples &#40;before 03&#47;15&#41;](media/multiplePmtTolRules(Pre1503).gif "multiplePmtTolRules(Pre1503)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) La date de règlement est comprise entre le 16/01/03 et le 17/01/03 (scénarios 4-9).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement multiples &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv1).gif "multiplePmtTolRules(GracePeriodInv1)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) La date de règlement est comprise entre le 18/01/03 et le 20/01/03 (scénarios 10-21).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement multiples &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv1-2).gif "multiplePmtTolRules(GracePeriodInv1-2)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) La date de règlement est comprise entre le 21/01/03 et le 22/01/03 (scénarios 22-27).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement multiples &#40;grace period&#41;](media/multiplePmtTolRules(GracePeriodInv2).gif "multiplePmtTolRules(GracePeriodInv2)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) La date de règlement est située après le 22/01/03 (scénarios 28-30).  
Montant ouvert par  

Règles d'application normales  

![Règles sur les écarts de règlement multiples &#40;after 01&#47;22&#41;](media/multiplePmtTolRules(Post0122).gif "multiplePmtTolRules(Post0122)")  

(1) Si le règlement intervient dans l'une de ces plages de dates, toutes les écritures lettrage peuvent être clôturées avec ou sans écart.  

(2) Si le règlement intervient dans l'une de ces plages, toutes les écritures lettrage ne peuvent pas être clôturées, même avec un écart.

## <a name="see-also"></a>Voir aussi  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

