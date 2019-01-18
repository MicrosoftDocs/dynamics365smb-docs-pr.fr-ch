---
title: "Lettrer des paiements avec des documents vente échus | Microsoft Docs"
description: "Vous lettrez les montants payés par les clients avec des documents vente associés et validez le paiement pour mettre à jour le client, la comptabilité, et les écritures comptables bancaires."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 10/17/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: e00d7bb259ad8a8a494016746179b428b7975a8f
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Rapprocher les paiements client manuellement à partir de la liste des documents vente échus
Lorsque vos clients ont effectué des paiements sur votre compte bancaire électronique, vous devez lettrer chaque montant payé avec le document vente associé, puis valider le paiement pour mettre à jour les écritures client, comptables et banque. Selon les besoins de votre entreprise, vous pouvez être payé et enregistrer ce paiement de diverses manières : manuellement, automatiquement, et via des services de paiement.  

> [!NOTE]  
>   Vous pouvez effectuer les mêmes tâches, y compris les paiements fournisseur sur la page **Feuille rapprochement bancaire** à l'aide des fonctions dédiées à l'importation de relevés bancaires, au lettrage automatique et au rapprochement bancaire. Pour plus d'informations, voir [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

La page **Enregistrer les paiements client** est conçue pour vous aider à réaliser les tâches de contrepartie des comptes internes à l'aide des chiffres réels pour vous assurer que les paiements sont collectés de façon efficace auprès des clients. Cet outil de traitement des paiements vous permet de vérifier et valider rapidement les paiements individuels ou forfaitaires, de traiter les paiements escomptés, et de rechercher des documents impayés spécifiques pour lesquels un paiement est effectué.

Les paiements pour des clients différents qui ont des dates d'échéance différentes doivent être validés en tant que paiements individuels. Les paiements pour le même client qui ont la même date d'échéance peuvent être validés comme paiement forfaitaire. Cela est utile, par exemple, lorsqu'un client a effectué un paiement unique qui couvre plusieurs factures vente.

## <a name="to-set-up-the-payment-registration-journal"></a>Pour configurer la feuille enregistrement de paiement
Étant donné que vous pouvez valider différents types de règlement dans différents comptes de contrepartie, vous devez sélectionner un compte de contrepartie sur la page **Paramétrage de l'enregistrement de paiement** avant de commencer le traitement des paiements client. Si vous validez toujours sur le même compte contrepartie, vous pouvez définir ce compte par défaut et éviter cette étape chaque fois que vous ouvrez la page **Enregistrer les paiements client**.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage de l'enregistrement de paiement**, puis sélectionnez le lien associé.

    Sinon, sur la page **Enregistrer les paiements client**, sélectionnez l'action **Configuration**.    
2. Renseignez les champs de la page **Paramétrage de l'enregistrement de paiement**. Choisissez un champ pour lire une brève description du champ ou du lien des informations connexes.  

## <a name="to-register-customer-payments-individually"></a>Pour enregistrer les paiements client individuellement

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrer les paiements client**, puis sélectionnez le lien associé.  

    La page **Enregistrer les paiements client** affiche tous les documents validés pour lesquels un paiement peut être enregistré. La page peut également être ouverte à partir des pages **Clients** et **Fiche client** dans lesquelles elle sera automatiquement filtrée pour le client spécifié.  
2. Cochez la case **Paiement effectué** de la ligne représentant le document validé pour lequel un paiement a été effectué.

    Si la case **Renseigner automatiquement la date de réception** est cochée sur la page **Paramétrage de l'enregistrement de paiement**, la date de travail est entrée dans le champ **Date de réception**.  
3. Dans le champ **Date de réception**, entrez la date de réception du paiement. Cette date peut être différent de la date de travail.  
4. Dans le champ **Montant reçu**, saisissez le montant payé.

    Pour les paiements intégraux, le montant est le même que celui du champ **Montant ouvert** de la ligne. Pour les paiements partiels, le montant est inférieur à celui du champ **Montant ouvert** de la ligne.    
5. Répétez les étapes 2 à 4 pour les autres lignes représentant des documents validés pour lesquels des paiements sont effectués.  
6. Sélectionnez l'action **Valider les paiements**.  

Les informations de paiement saisies sont validées pour les documents représentés par les lignes dont la case **Paiement effectué** est cochée.  

Les écritures de paiement sont validées dans les comptes général, bancaire, et client. Chaque paiement est lettré au document vente validé lié.  

## <a name="to-reconcile-lump-payments"></a>Pour rapprocher des paiements forfaitaires
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.
2. Cochez la case **Paiement effectué** pour les lignes représentant les documents validés pour le même client pour lequel un paiement forfaitaire a été effectué.  

    > [!NOTE]  
    >   Le champ **Nom** du client doit être le même sur toutes les lignes validées comme paiement forfaitaire.  

    Si la case **Renseigner automatiquement la date de réception** est cochée sur la page **Paramétrage de l'enregistrement de paiement**, la date de travail est renseignée dans le champ **Date de réception**.  
3. Dans le champ **Date de réception**, entrez la date de réception du paiement. Cette date peut être différent de la date de travail.  

    > [!NOTE]  
    >   Cette date doit être identique sur toutes les lignes qui seront validées comme paiement forfaitaire.  
4. Dans le champ **Montant reçu**, entrez les montants sur plusieurs lignes pour obtenir le paiement forfaitaire.  

    > [!TIP]  
    >   Essayez de valider le plus de paiements intégraux possible avec le montant forfaitaire. Entrez des montants identiques au montant du champ **Montant ouvert** sur autant de lignes que possible.  
5. Répétez les étapes 2 à 4 pour les autres lignes représentant les documents validés pour le même client pour lequel un paiement forfaitaire a été effectué.  
6. Sélectionnez l'action **Valider comme paiement forfaitaire**. Les informations de paiement saisies sont validées pour les documents représentés par les lignes dont la case **Paiement effectué** est cochée.  

Les écritures de paiement sont validées dans les comptes général, bancaire, et client. Chaque paiement est lettré au document vente validé lié.  

Si un paiement avec la banque n'est pas représenté par une ligne sur la page **Enregistrement de paiement**, cela peut être parce que le document connexe n'a pas encore été validé. Dans ce cas, vous pouvez utiliser la fonction de recherche pour trouver rapidement le document et le valider pour traiter le paiement. Pour plus d'informations, voir la section « Pour rechercher un document vente spécifique qui n'est pas totalement facturé ».  

Si un paiement avec la banque n'est représenté par aucun document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez ouvrir une ligne feuille comptabilité préremplie depuis la page **Enregistrement de paiement** pour valider le paiement directement dans le compte contrepartie sans lettrer le paiement avec un document. Sinon, vous pouvez enregistrer le paiement dans la feuille jusqu'à ce que l'origine du paiement soit résolue. Pour plus d'informations, reportez-vous à la section « Pour enregistrer ou valider un paiement sans document connexe ».  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Pour traiter manuellement les paiements client avec remises
Si vous avez convenu d'un escompte avec le client, les montants règlement peuvent être inférieurs aux montants facture si le paiement est effectué avant la date d'escompte convenue.  

Les procédures suivantes expliquent quatre méthodes différentes permettant de valider des paiements escomptés sur la page **Enregistrement de paiement**.  

* Le montant règlement est égal au montant escompté ouvert, et la date d'échéance est antérieure à la date d'escompte. Vous validez le paiement tel quel.  
* Le montant règlement est égal au montant escompté ouvert, mais la date d'échéance est postérieure à la date d'escompte. Vous validez le paiement comme partiel. Le document reste ouvert pour collecter/payer le montant ouvert. Sinon, vous définirez la date d'escompte ultérieurement pour permettre la réalisation de la totalité du paiement.  
* Le montant règlement est inférieur au montant escompté ouvert. Vous validez le paiement comme partiel. Le document reste ouvert pour collecter/payer le montant ouvert.  
* Le montant règlement est supérieur au montant escompté ouvert. Vous validez les paiements tels quels. Seul le montant ouvert est validé. Le montant supplémentaire est crédité au client.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Pour traiter un montant règlement égal au montant escompté, et lorsque la date d'échéance est antérieure à la date d'escompte
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est égal au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.    
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique zéro (0).  
5. Sélectionnez l'action **Valider les paiements** pour valider l'intégralité du paiement sur les comptes général, bancaire et client.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Pour traiter un montant règlement égal au montant escompté, mais lorsque la date d'échéance est postérieure à la date d'escompte
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est égal au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.
3. Dans le champ **Date de réception**, saisissez une date d'échéance ultérieure à celle indiquée dans le champ **Date d'escompte**. La police des champs de date devient rouge et un message d'erreur s'affiche au bas de la page.

    > [!TIP]  
    >   Si vous voulez créer une exception et accorder la remise bien que le paiement soit échu, procédez comme suit :
4. Sélectionnez l'action **Détails**.  
5. Sur la page **Détails de l'enregistrement de paiement**, dans le champ **Date d'escompte** sur le raccourci **Escompte**, saisissez une date ultérieure à celle indiquée dans le champ **Date de réception** de la page **Enregistrement de paiement**.  

    Le message d'erreur et la police rouge disparaissent, vous pouvez traiter le paiement escompté.    
6. Vérifiez que le champ **Montant ouvert** indique le montant qui reste à régler pour le montant total de la facture.  
7. Sélectionnez l'action **Valider les paiements** pour valider le paiement partiel sur les comptes général, bancaire et client.  

Le document connexe reste ouvert.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Pour traiter un paiement inférieur au montant escompté ouvert
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est inférieur au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.  
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique le montant qui reste à régler pour le montant escompté.  
5. Sélectionnez l'action **Valider les paiements** pour valider le paiement partiel sur les comptes général, bancaire et client.  

Le document connexe reste ouvert.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Pour traiter un paiement supérieur au montant escompté ouvert
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est supérieur au montant du champ **Montant restant après remise**.  

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.    
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique zéro (0).  
5. Sélectionnez l'action **Valider les paiements** pour valider l'intégralité du paiement sur les comptes général, bancaire et client.  

Le document connexe est clôturé, et le client est crédité du montant règlement excédentaire.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Pour rechercher un document vente spécifique qui n'est pas totalement facturé
La page **Enregistrement de paiement** vous aide dans les tâches de contrepartie des comptes internes avec les chiffres réels de règlement pour assurer une collecte efficace auprès des clients et le paiement des sommes dues aux fournisseurs. Elle affiche les paiements entrants en attente sous la forme de lignes représentant les documents vente pour lesquels un montant doit être payé.  

Généralement, lorsqu'un paiement a été effectué, enregistré dans la banque ou autre, le document vente ou achat associé est représenté par une ligne sur la page **Enregistrement de paiement** parce que le document en question attend que le paiement soit validé par rapport au montant ouvert. Cependant, parfois un paiement qui a effectué n'est pas représenté par une ligne sur la page **Enregistrement de paiement**, généralement parce que la facture du document en question n'a pas encore été totalement validé.

Sur la page **Recherche de documents**, vous pouvez rechercher parmi les documents qui n'ont pas été entièrement facturés. Vous pouvez effectuer une recherche avec un ou plusieurs des critères suivants :  

* Numéro de document  
* Montant ou plage de montants  

La procédure suivante explique comment trouver un document spécifique à l'aide de deux critères de recherche.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.
2. Avec le pointeur sur n'importe quelle ligne, sélectionnez l'action **Rechercher des documents**.
3. Sur la page **Recherche de document**, entrez une valeur de recherche dans le champ **N° document**.  

    > [!NOTE]  
    >   La valeur que vous entrez dans ce champ est indiquée entre caractères génériques masqués. Cela signifie que la fonction recherche tous les numéros de document qui contiennent la valeur saisie.    
4. Dans le champ **Montant**, saisissez le montant spécifique qui figure sur le document que vous recherchez.  
5. Dans le champ **% écart de quantité**, saisissez la valeur du pourcentage pour définir la plage des montants dans laquelle rechercher le document ouvert.  

    Si vous saisissez 10, la fonction recherche les montants d'une plage comprise entre dix pour cent en moins et dix pour cent de plus que la valeur indiquée dans le champ **Montant**.    
6. Sélectionnez l'action **Rechercher**.  

La fonction de recherche effectue une recherche parmi les documents qui n'ont pas été entièrement facturés selon les critères spécifiés.  

Si un ou plusieurs documents correspondent aux critères de recherche, la page **Résultat de la recherche de documents** s'ouvre et affiche les lignes représentant ces documents. Chaque ligne contient un numéro de document, une description et un montant de manière à ce que vous puissiez facilement rechercher un document spécifique, par exemple à l'aide des informations de votre relevé bancaire.  

Si un paiement avec la banque n'est représenté par aucun document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez ouvrir une ligne feuille comptabilité préremplie depuis la page **Enregistrement de paiement** pour valider le paiement directement dans le compte contrepartie sans lettrer le paiement avec un document. Sinon, vous pouvez enregistrer le paiement dans la feuille jusqu'à ce que l'origine du paiement soit résolue.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Pour enregistrer ou valider un paiement sans document connexe
Si un paiement avec la banque n'est représenté par aucun document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez ouvrir une ligne feuille comptabilité préremplie depuis la page **Enregistrement de paiement** pour valider le paiement directement dans le compte contrepartie sans lettrer le paiement avec un document. Sinon, vous pouvez enregistrer le paiement dans la feuille jusqu'à ce que l'origine du paiement soit clarifiée.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Enregistrement de paiement**, puis sélectionnez le lien associé.  

    Enregistrez un paiement non documenté.  
2. Sélectionnez l'action **Feuille comptabilité**.  

    La page **Feuille comptabilité** s'affiche avec une ligne préremplie où figure le compte contrepartie du nom de feuille défini sur la page **Paramétrage de l'enregistrement de paiement**.  
3. Renseignez les autres champs de la ligne feuille comptabilité, tel que le montant et le numéro de client ou d'autres informations du relevé bancaire. Pour plus d'informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).  

Vous pouvez soit valider la ligne feuille mettre à jour le total sur le compte contrepartie. Sinon, vous pouvez laisser la ligne feuille non validée et ajouter par exemple une note indiquant que le paiement a besoin d'une autre analyse.  

Si vous laissez la ligne feuille non validée, elle s'ajoutera à la valeur du champ **Solde non validé** au bas de la page **Enregistrement de paiement**.  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

