---
title: Configurer un prélèvement SEPA | Microsoft Docs
description: Découvrez comment configurer des prélèvements SEPA dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 2ca52a5c1e6f009f0a430e5b35b725c832132c6f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242571"
---
# <a name="set-up-sepa-direct-debit"></a>Configurer un prélèvement SEPA
Sur la page **Recouvrements prélèvement**, vous pouvez exporter des instructions vers votre banque électronique pour exécuter un recouvrement par prélèvement automatique depuis le compte bancaire du client vers votre compte bancaire. [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge le format de prélèvement SEPA, mais dans votre pays/région, d'autres formats de paiements électroniques peuvent être disponibles.  

Pour activer l'exportation de formats de fichiers bancaires qui ne sont pas pris en charge en natif dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez configurer une définition d'échange de données à l'aide de l'infrastructure d'échange de données. Pour plus d'informations, voir [Configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md).  

Avant de pouvoir traiter les paiements client par voie électronique en exportant des instructions de prélèvement automatique dans le format de prélèvement automatique SEPA, vous devez exécuter les étapes de configuration suivantes :  

* Configurez le format d'exportation du fichier bancaire qui donne l'ordre à votre banque d'exécuter une collection prélèvement automatique du compte bancaire du client vers votre compte bancaire.  
* Configurez le mode de paiement du client.  
* Configurez le mandat de prélèvement automatique qui reflète votre accord avec le client pour collecter ses paiements pendant une certaine durée établie.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Pour configurer votre compte bancaire par prélèvement automatique SEPA  
1. Dans la zone **Rechercher**, saisissez **Comptes bancaires**, puis sélectionnez le lien associé.  
2. Ouvrez le compte bancaire que vous souhaitez utiliser pour les prélèvements automatiques.  
3. Sur le raccourci **Transfert**, dans le champ **Format exp. prélèvement SEPA** choisissez l'option pour le prélèvement SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Pour configurer le mode de paiement client pour le prélèvement automatique SEPA  
1. Dans la zone **Rechercher**, entrez **Modes de règlement**, puis choisissez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Configurez un mode de règlement. Remplissez les champs relatifs au prélèvement automatique comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Prélèvement**|Spécifie si le mode de paiement est utilisé pour une collection prélèvement automatique SEPA.|  
    |**Code conditions paiem. prélèvement**|Spécifiez les conditions de paiement, par exemple NE PAS PAYER, qui sont affichées sur les factures vente payées par prélèvement automatique SEPA pour indiquer au client que le paiement sera collecté automatiquement. Vous pouvez également laisser le champ vide.|  

    > [!NOTE]  
    >  N'entrez pas de valeur dans le champ **N° compte contrepartie**.  

4. Cliquez sur le bouton **OK** pour fermer la page **Modes de règlement**.  
5. Dans la zone **Rechercher**, saisissez **Clients**, puis sélectionnez le lien associé.  
6. Ouvrez la fiche du client que vous voulez paramétrer pour la collection prélèvement automatique SEPA.  
7. Sélectionnez le champ **Code mode de règlement**, puis le code mode de règlement que vous avez spécifié à l'étape 3.  
8. Répétez les étapes 6 et 7 pour tous les clients que vous voulez paramétrer pour les collections prélèvements automatiques SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Pour configurer le mandat de prélèvement qui représente l'accord client  
1. Dans la zone **Rechercher**, saisissez **Clients**, puis sélectionnez le lien associé.  
2. Ouvrez la fiche du client que vous voulez paramétrer pour les prélèvements automatiques SEPA.  
3. Choisissez l'option **Comptes bancaires**.  
4. Sur la page **Liste des comptes bancaires client**, sélectionnez le compte bancaire client utilisé pour les prélèvements automatique puis, sous l'onglet **Accueil**, dans le groupe **Processus**, cliquez sur **Mandats prélèvement automatique**.  
5. Sur la page **Mandats de prélèvement SEPA**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code compte bancaire client**|Spécifie le compte bancaire à partir duquel les prélèvements automatiques sont collectés. Ce champ est complété automatiquement.|  
    |**Valide à partir de**|Spécifie la date à laquelle le mandat de prélèvement commence.|  
    |**Valide jusque**|Spécifie la date à laquelle le mandat de prélèvement se termine.|  
    |**Date de signature**|Spécifie la date à laquelle le client a signé le mandat de prélèvement.|  
    |**Type de paiement**|Spécifie si l'accord couvre plusieurs (**Récurrent**) ou une seule (**Unique**) collection de prélèvement.|  
    |**Nombre attendu de prélèvements**|Spécifie le nombre de collections prélèvement automatique à effectuer. Ce champ n'est utile que si vous avez sélectionné **Récurrent** dans le champ **Type de paiement**.|  
    |**Compteur prélèvements**|Spécifie le nombre de collections de prélèvement réalisées à l'aide de ce mandat de prélèvement. Le champ est mis à jour automatiquement.|  
    |**Bloqué**|Spécifie que des collections de prélèvement ne peuvent pas être réalisées à l'aide de ce mandat de prélèvement.|  

6.  Répétez les étapes 1 à 5 pour tous les clients que vous voulez paramétrer pour les prélèvements automatiques SEPA.  

 Le mandat de prélèvement est automatiquement inséré dans le champ **ID mandat de prélèvement** lorsque vous créez une facture vente pour le client que vous avez sélectionné à l'étape 2. Pour plus d'informations, voir [Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Voir aussi  
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md)
[Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md)
[Échanger des données par voir électronique](across-data-exchange.md)
