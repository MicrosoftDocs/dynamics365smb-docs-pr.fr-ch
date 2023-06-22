---
title: "Prélèvement SEPA dans Business\_Central"
description: 'Avec le consentement de votre client, vous pouvez collecter les paiements directement à partir du compte bancaire du client en fonction du format SEPA.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="collect-payments-with-sepa-direct-debit" />Recouvrement de paiements par prélèvement automatique SEPA

Avec le consentement de votre client, vous pouvez collecter les paiements directement à partir du compte bancaire du client en fonction du format SEPA.  

Tout d’abord, définissez le format d’exportation du fichier bancaire qui indique à votre banque comment effectuer un prélèvement automatique. Ensuite, paramétrez le mode de paiement du client. Enfin, configurez le mandat de prélèvement qui reflète votre accord avec le client pour collecter leurs paiements pendant une certaine durée.  

Pour demander à la banque de transférer le montant du paiement du compte bancaire du client vers le compte de votre société, vous créez une écriture de collection prélèvement automatique, qui conserve des informations sur les comptes bancaires, les factures de vente concernées et le mandat de prélèvement. Vous exportez ensuite un fichier XML basé sur l’écriture de collection, que vous envoyez à votre banque pour traitement. La banque vous communiquera tous les paiements impossibles à traiter, et vous devez rejeter manuellement les écritures de collection prélèvement automatique en question.  

Vous pouvez définir des codes vente client standard avec les informations de mode et de mandat de prélèvement. Vous pouvez ensuite utiliser le traitement par lots **Créer factures client standard** pour générer plusieurs factures vente avec les informations de prélèvement automatique préremplies. Ceci peut être effectué manuellement ou automatiquement, en fonction de la date d’échéance du paiement.  

Lorsque les paiements sont traités avec succès, tel que communiqué par votre banque, vous pouvez valider les réceptions de paiement directement à partir de la page **Écritures recouvrement prélèvement**, ou en déplaçant les lignes paiement vers la feuille où vous validez des réceptions de paiement, tels que la page **Feuille règlement**. Sinon, en fonction de votre processus de gestion de trésorerie, vous pouvez attendre et lettrer les paiements lors du rapprochement bancaire.  

> [!NOTE]  
> Pour réunir les paiements à l’aide du prélèvement SEPA, la devise sur la facture vente doit être l’EURO.  

## <a name="setting-up-sepa-direct-debit" />Configuration d’un prélèvement SEPA

Sur la page **Recouvrements prélèvement**, vous pouvez exporter des instructions vers votre banque électronique pour exécuter un recouvrement par prélèvement automatique depuis le compte bancaire du client vers votre compte bancaire selon le format de prélèvement SEPA.

> [!NOTE]
> La version globale de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge le format de prélèvement SEPA uniquement. La version de votre pays/région peut prendre en charge d’autres formats pour le paiement électronique. Reportez-vous à la section **Fonctionnalités locales** dans la table des matières.  

Pour activer l’exportation de formats de fichiers bancaires qui ne sont pas pris en charge en natif dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez configurer une définition d’échange de données à l’aide de l’infrastructure d’échange de données. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

Avant de pouvoir traiter les paiements client par voie électronique en exportant des instructions de prélèvement automatique dans le format de prélèvement automatique SEPA, vous devez exécuter les étapes de configuration suivantes :  

* Configurez le format d’exportation du fichier bancaire qui donne l’ordre à votre banque d’exécuter une collection prélèvement automatique du compte bancaire du client vers votre compte bancaire.  
* Configurez le mode de paiement du client.  
* Configurez le mandat de prélèvement automatique qui reflète votre accord avec le client pour collecter ses paiements pendant une certaine durée établie.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit" />Pour configurer votre compte bancaire par prélèvement automatique SEPA

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.  
2. Ouvrez le compte bancaire que vous souhaitez utiliser pour les prélèvements automatiques.  
3. Sur le raccourci **Transfert**, dans le champ **Format exp. prélèvement SEPA** choisissez l’option pour le prélèvement SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit" />Pour configurer le mode de paiement client pour le prélèvement automatique SEPA

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modes de paiement**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Configurez un mode de règlement. Remplissez les champs relatifs au prélèvement automatique comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Prélèvement**|Spécifie si le mode de paiement est utilisé pour une collection prélèvement automatique SEPA.|  
    |**Code conditions paiem. prélèvement**|Spécifiez les conditions de paiement, par exemple NE PAS PAYER, qui sont affichées sur les factures vente payées par prélèvement automatique SEPA pour indiquer au client que le paiement sera collecté automatiquement. Vous pouvez également laisser le champ vide.|  

    > [!NOTE]  
    >  N’entrez pas de valeur dans le champ **N° compte contrepartie**.  

4. Cliquez sur le bouton **OK** pour fermer la page **Modes de règlement**.  
5. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  
6. Ouvrez la fiche du client que vous voulez paramétrer pour la collection prélèvement automatique SEPA.  
7. Sélectionnez le champ **Code mode de règlement**, puis le code mode de règlement que vous avez spécifié à l’étape 3.  
8. Répétez les étapes 6 et 7 pour tous les clients que vous voulez paramétrer pour les collections prélèvements automatiques SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement" />Pour configurer le mandat de prélèvement qui représente l’accord client

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  
2. Ouvrez la fiche du client que vous voulez paramétrer pour les prélèvements automatiques SEPA.  
3. Choisissez l’option **Comptes bancaires**.  
4. Sur la page **Liste des comptes bancaires client**, sélectionnez le compte bancaire client utilisé pour les prélèvements automatique, puis sélectionnez l’action **Mandats prélèvement automatique**.  
5. Sur la page **Mandats de prélèvement SEPA**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code compte bancaire client**|Spécifie le compte bancaire à partir duquel les prélèvements automatiques sont collectés. Ce champ est complété automatiquement.|  
    |**Valide à partir de**|Spécifie la date à laquelle le mandat de prélèvement commence.|  
    |**Valide jusque**|Spécifie la date à laquelle le mandat de prélèvement se termine.|  
    |**Date de signature**|Spécifie la date à laquelle le client a signé le mandat de prélèvement.|  
    |**Type de paiement**|Spécifie si l’accord couvre plusieurs (**Récurrent**) ou une seule (**Unique**) collection de prélèvement.|  
    |**Nombre attendu de prélèvements**|Spécifie le nombre de collections prélèvement automatique à effectuer. Ce champ n’est utile que si vous avez sélectionné **Récurrent** dans le champ **Type de paiement**.|  
    |**Compteur prélèvements**|Spécifie le nombre de collections de prélèvement réalisées à l’aide de ce mandat de prélèvement. Le champ est mis à jour automatiquement.|  
    |**Bloqué**|Spécifie que des collections de prélèvement ne peuvent pas être réalisées à l’aide de ce mandat de prélèvement.|  

6. Répétez les étapes 1 à 5 pour tous les clients que vous voulez paramétrer pour les prélèvements automatiques SEPA.  

 Le mandat de prélèvement est automatiquement inséré dans le champ **ID mandat de prélèvement** lorsque vous créez une facture vente pour le client que vous avez sélectionné à l’étape 2. Pour plus d’informations, voir [Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file" />Création d’écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire

Pour demander à la banque de transférer le montant du paiement du compte bancaire du client vers le compte de votre société, vous créez une écriture de collection prélèvement automatique, qui conserve des informations sur le compte bancaire du client, les factures de vente concernées et le mandat de prélèvement. À partir de l’écriture de collection prélèvement automatique qui en résulte, vous exportez ensuite un fichier XML que vous envoyez ou transférez à votre banque électronique pour traitement. La banque vous communiquera tous les paiements qu’elle n’a pas pu traiter, et vous devez rejeter manuellement les écritures de collection prélèvement automatique en question.  

 > [!NOTE]  
 > Pour réunir les paiements à l’aide du prélèvement SEPA, la devise sur la facture vente doit être l’EURO.  

### <a name="to-create-a-direct-debit-collection" />Pour créer une collection prélèvement automatique

 1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Recouvrements prélèvement**, puis sélectionnez le lien associé.  
 2. Sur la page **Recouvrements prélèvement**, sélectionnez l’action **Créer collection prélèvement automatique**.  
 3. Sur la page **Créer recouvrement prélèvement**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Date d’échéance début**|Spécifie la date d’échéance de paiement la plus proche sur les factures vente pour lesquelles vous souhaitez créer une collection prélèvement automatique.|  
    |**Date d’échéance fin**|Spécifie la date d’échéance de paiement la plus ancienne sur les factures vente pour lesquelles vous souhaitez créer une collection prélèvement automatique.|  
    |**Type partenaire**|Spécifie si la collection prélèvement automatique est réalisée pour des clients de type **Société** ou **Personne**.|  
    |**Uniquement les clients avec mandat valide**|Spécifie si une collection de prélèvement est créée pour les clients disposant d’un mandat de prélèvement valable. **Remarque :** une collection prélèvement automatique est créée même si le champ **ID mandat de prélèvement** n’est pas rempli sur la facture vente.|  
    |**Uniquement les factures avec mandat valide**|Spécifiez si une collection prélèvement est créée uniquement pour les factures vente si un mandat de prélèvement valide est sélectionné dans le champ **ID mandat de prélèvement** de la facture vente.|  
    |**N° compte bancaire**|Spécifie les comptes bancaires de votre société sur lesquels le paiement collecté sera transféré à partir du compte bancaire du client.|  
    |**Nom compte bancaire**|Spécifie le nom du compte bancaire que vous sélectionnez dans le champ **N° compte bancaire**. Ce champ est complété automatiquement.|  

 4. Cliquez sur le bouton **OK**.  

Une collection prélèvement automatique est ajoutée à la page **Recouvrements prélèvement** et une ou plusieurs écritures de collection prélèvement automatique sont créées.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file" />Pour exporter une collection prélèvement automatique vers un fichier bancaire

 1. Sur la page **Recouvrements prélèvement**, sélectionnez l’action **Écritures recouvrement prélèvement**.  
 2. Sur la page **Écritures recouvrement prélèvement**, sélectionnez l’écriture que vous voulez exporter, puis sélectionnez l’action **Créer fichier prélèvement automatique**.  
 3. Enregistrez le fichier d’exportation à l’emplacement où vous l’envoyez ou transférez\-le à votre banque électronique.  

      Sur la page **Écritures recouvrement prélèvement**, le champ **Statut recouvrement prélèvement** est modifié sur Fichier créé. Sur la page **Mandats de prélèvement SEPA**, le champ **Compteur prélèvements** est mis à jour avec un nombre.  

 Si le fichier exporté ne peut pas être traité, par exemple parce que le client est insolvable, vous pouvez rejeter l’écriture de collection prélèvement automatique. Si le fichier exporté est correctement traité par la banque, les paiements dus des factures vente impliquées sont collectés automatiquement auprès des clients concernés. Dans ce cas, vous pouvez fermer la collection.  

### <a name="to-reject-a-direct-debit-collection-entry" />Pour rejeter une écriture collection prélèvement automatique

* Sur la page **Écritures recouvrement prélèvement**, sélectionnez l’écriture qui n’a pas été traitée, puis sélectionnez l’action **Rejeter écriture**.  

    La valeur du champ **Statut** de la page **Écritures recouvrement prélèvement** est modifiée sur **Rejetée**.  

### <a name="to-close-a-direct-debit-collection" />Pour fermer une collection prélèvement automatique

* Sur la page **Écritures recouvrement prélèvement**, sélectionnez l’écriture qui n’a pas été traitée, puis sélectionnez l’action **Fermer collection**.  

    La collection prélèvement automatique associée est fermée.  

 Vous pouvez maintenant passer à la validation des réceptions de paiement pour les factures vente impliquées. Vous pouvez généralement le faire pendant que vous validez des réceptions de paiement, tel que sur la page **Enregistrement de paiement**, ou vous pouvez valider les réceptions de paiement directement à partir de la page **Écritures recouvrement prélèvement**. Pour plus d’informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts" />Validation des réceptions règlement de prélèvement SEPA

Lorsqu’une collection prélèvement automatique est correctement traitée par votre banque, vous pouvez procéder à la validation de la réception du paiement pour les factures vente impliquées. Pour plus d’informations, voir [Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Vous pouvez valider la réception paiement directement à partir de la page **Recouvrements prélèvement** ou de la page **Écritures recouvrement prélèvement**. Vous pouvez également relayer le travail à un autre utilisateur en préparant les lignes feuille associées.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page" />Pour valider une réception de paiement de prélèvement automatique à partir de la page Collections prélèvement automatique

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Recouvrements prélèvement**, puis sélectionnez le lien associé.  
2. Sélectionnez une ligne pour une collection prélèvement automatique qui a été exportée vers un fichier bancaire et traitée avec succès par la banque.
3. Sélectionnez l’action **Valider reçus paiement**.  
4. Sur la page **Valider recouvrement prélèvement**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N° recouvrement prélèvement**|Spécifie la collection prélèvement automatique pour laquelle vous souhaitez valider la réception paiement.|  
    |**Modèle feuille comptabilité**|Spécifie le modèle de feuille comptabilité à utiliser pour la validation de la réception du paiement, comme le modèle pour les encaissements.|  
    |**Nom feuille comptabilité**|Spécifie la feuille comptabilité à utiliser pour la validation de la réception du paiement.|  
    |**Créer feuille uniquement**|Activez cette case à cocher si vous ne souhaitez pas valider la réception règlement lorsque vous cliquez sur le bouton **OK**. La réception de paiements est préparée dans la feuille spécifiée et n’est pas validée jusqu’à ce qu’une personne valide les lignes feuille en question.|  

5. Cliquez sur le bouton **OK**.

## <a name="see-also" />Voir aussi

[Gestion des comptes client](receivables-manage-receivables.md)  
[Gestion des services](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
