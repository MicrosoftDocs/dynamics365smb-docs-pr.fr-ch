---
title: Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client
description: Décrit comment lettrer des règlements ou des remboursements client dans une ou plusieurs écritures comptables client ouvertes. Cela fait partie du rapprochement des paiements des clients.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client

Lorsque vous recevez un règlement en espèces d’un client ou que vous effectuez un remboursement, vous pouvez lettrer le paiement ou le remboursement pour clôturer une ou plusieurs écritures débit ou crédit. Vous pouvez indiquer le montant à appliquer. Par exemple, vous pouvez appliquer des paiements partiels aux écritures comptables client. La clôture des écritures comptables client garantit que les statistiques clients, les relevés bancaires et les intérêts de retard, etc. sont à jour.

> [!TIP]  
>   Sur la page **Écritures comptables client**, le rouge signifie que le paiement associé a dépassé sa date d’échéance. Si les paiements échus deviennent un problème, nous pouvons vous aider à minimiser leur fréquence. Vous pouvez activer l’extension **Prévisions des retards de paiement**, qui utilise un modèle prédictif que nous avons généré dans Azure Machine Learning pour prévoir les délais de paiement. Ces prévisions vous permettent de réduire les créances ouvertes et d’ajuster votre stratégie de collectes. Par exemple, si un retard de paiement est prévu, vous pouvez ajuster les conditions de paiement ou le mode de règlement du client. Pour plus d’informations, consultez [Prévisions de retard de paiement](ui-extensions-late-payment-prediction.md).  

Vous pouvez lettrer les écritures comptables client de plusieurs manières :

* En entrant des informations sur les pages dédiées :
    * La page **Feuille rapprochement bancaire**. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * La page **Enregistrement de paiement**. Pour plus d’informations, voir [Rapprocher les paiements client dans une liste des documents vente échus](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
    * La **Feuille règlement**. Cette option est décrite ci-dessous.
* En renseignant le champ **N° doc. lettrage** sur les documents Avoir vente. Cette option est décrite ci-dessous.
* Grâce à l’action **Définir ID lettrage** d’une écriture comptable client. Cette option est décrite ci-dessous.
* En utilisant l’action **Lettrer écritures** sur la page **Dépôt bancaire**, puis en saisissant le numéro de facture dans le champ **Définir ID lettrage**. Pour plus d’informations, voir [Créer des dépôts bancaires](bank-create-bank-deposits.md).

> [!NOTE]  
>   Si le champ **Mode de lettrage** de la fiche client contient **Au plus ancien**, les paiements sont automatiquement lettrés avec l’écriture de crédit ouverte la plus ancienne sauf si vous spécifiez une écriture manuellement. Si le mode de lettrage pour un fournisseur est **Manuel**, vous devez toujours lettrer les écritures manuellement.

## Pour renseigner et valider une feuille règlement
Une feuille règlement est un type de journal général. Vous pouvez l’utiliser pour valider les transactions sur les comptes généraux, bancaires, client, fournisseur et immobilisation. Vous pouvez lettrer le règlement sur une ou plusieurs écritures débit lorsque vous validez le règlement. Vous pouvez également lettrer à partir des écritures validées ultérieurement.
1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille règlement**, puis choisissez le lien associé.
2. Sélectionnez **Modifier journal**.
3. Sélectionnez le nom de traitement par lots souhaité dans le champ **Nom de la feuille**.
4. Renseignez le champ **Date comptabilisation**.  
5. Dans le champ **Type document**, sélectionnez **Paiement**.

    Le champ **N° document** contient les souches de numéros affectées au lot.  
6. Utilisez le champ **N° doc. externe** pour stocker un identifiant, tel que le numéro de chèque du client.
7. Dans le champ **Type compte**, sélectionnez **Client**.
8. Dans le champ **N° compte**, sélectionnez le compte général approprié.
9. Si vous souhaitez valider l’application en même temps que la feuille, suivez l’un des exemples ci-dessous.
10. Dans le champ **Type compte contrepartie**, sélectionnez **Compte général** pour les règlements et **Compte bancaire** pour les autres paiements.
11. Dans le champ **N° compte contrepartie**, sélectionnez le compte pour les règlements ou le compte bancaire approprié pour d’autres paiements.
12. Validez la feuille.

## Pour lettrer un paiement avec une seule écriture comptable client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille règlement**, puis choisissez le lien associé.
2. Sélectionnez **Modifier journal**.
3. Dans la première ligne feuille, saisissez les informations appropriées sur l’écriture à lettrer.
4. Dans le champ **Type document**, entrez **Paiement**.
5. Dans le champ **Type compte**, entrez **Client**.
6. Dans le champ **Type compte contrepartie**, entrez **Compte bancaire.**
7. Dans le champ **N° doc. lettrage**, sélectionnez le champ permettant d’ouvrir la page **Lettrer écritures client**.
8. Sur la page **Lettrer écritures client**, sélectionnez l’écriture à laquelle lettrer le paiement.
9. Dans le champ **Montant à lettrer**, entrez le montant à lettrer à l’écriture. Si vous n’entrez aucun montant, le montant maximal est lettré.

    Au bas de la page **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
10. Cliquez sur le bouton **OK**. La page **Feuille règlement** affiche désormais l’écriture des champs **Type doc. lettrage** et **N° doc. lettrage**.
11. Validez la feuille règlement.

## Pour lettrer un paiement avec plusieurs écritures client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille règlement**, puis choisissez le lien associé.
2. Sélectionnez **Modifier journal**.
3. Dans la première ligne feuille, saisissez les informations appropriées sur l’écriture à lettrer.
4. Dans le champ **Type document**, entrez **Paiement**.
5. Dans le champ **Type compte**, entrez **Client**.
6. Dans le champ **Type compte contrepartie**, entrez **Compte bancaire.**
7. Dans le champ **Montant**, entrez le paiement complet sous forme de montant négatif.
8. Pour lettrer le paiement avec plusieurs écritures comptables client lors de la validation, sélectionnez l’action **Lettrer écritures**.  
9. Sélectionnez les lignes correspondant aux écritures avec lesquelles l’écriture lettrage doit être lettrée, puis sélectionnez l’action **Définir ID lettrage**.  
10. Sur chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l’écriture. Si vous n’entrez aucun montant, le montant maximal est lettré.

    Au bas de la page **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
11. Cliquez sur le bouton **OK**.
12. Validez la feuille règlement.

## Pour lettrer un avoir avec une seule écriture comptable client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs vente**, puis sélectionnez le lien associé.
2. Ouvrez l’avoir vente souhaité.
3. Pour lettrer l’avoir avec une seule écriture comptable client lors de la validation, dans le champ **N° doc. lettrage**, sélectionnez l’écriture avec laquelle lettrer le paiement.
4. Sur la ligne du champ **Montant à lettrer**, entrez le montant à lettrer avec l’écriture.  

    Si vous n’entrez aucun montant, l’application lettre automatiquement le montant maximal. Au bas de la page **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.    
5. Choisissez le bouton **OK**. La page **Avoir vente** affiche désormais l’écriture que vous avez saisie dans les champs **Type doc. lettrage** et **N° doc. lettrage**. Et le montant de l’avoir à valider, escomptes éventuels déduits.
6. Valider l’avoir.

## Pour lettrer un avoir avec plusieurs écritures comptables client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs vente**, puis sélectionnez le lien associé.
2. Ouvrez l’avoir vente souhaité.
3. Pour lettrer l’avoir avec plusieurs écritures comptables client lors de la validation, sélectionnez l’action **Lettrer écritures**.
4. Sélectionnez les lignes correspondant aux écritures avec lesquelles l’écriture lettrage doit être lettrée, puis sélectionnez l’action **Définir ID lettrage**.
5. Sur chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l’écriture. Si vous n’entrez aucun montant, le montant maximal est lettré.  

    Au bas de la page **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré** et constatez si le lettrage est équilibré.  
6. Choisissez le bouton **OK**. La page **Avoir vente** affiche désormais le montant de l’avoir à valider, escomptes éventuels déduits.
7. Valider l’avoir.

## Pour lettrer des écritures comptables client validées
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la fiche du client possédant les écritures que vous souhaitez lettrer.
3. Sélectionnez l’action **Écritures comptables**, puis sélectionnez la ligne où figure l’écriture qui sera l’écriture lettrage.
4. Sélectionnez l’action **Lettrer écritures**. La page **Lettrer écritures client** s’ouvre et affiche les écritures ouvertes de ce client.
5. Sélectionnez les lignes correspondant aux écritures avec lesquelles l’écriture lettrage doit être lettrée, puis sélectionnez l’action **Définir ID lettrage** .
6. Pour chaque ligne du champ **Montant à lettrer**, entrez le montant que vous souhaitez lettrer à l’écriture. Si vous n’entrez aucun montant, le montant maximal est lettré.  

    Au bas de la page **Lettrer écritures client**, vous voyez le montant spécifique dans le champ **Montant lettré**.  
7. Sélectionnez l’action **Valider le lettrage**. La page **Valider le lettrage** s’ouvre et affiche le numéro de document de l’écriture lettrage et la date comptabilisation de l’écriture ayant la date comptabilisation la plus récente.  
8. Cliquez sur **OK** pour valider le lettrage.

    Si le lettrage validé génère des écritures comptables client lettrées, ces écritures comptables ne sont plus activées dans le champ **Ouvert**.    
9. Pour voir les écritures comptables, sélectionnez l’icône ![Ampoule qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé. Accédez à la fiche du client approprié pour afficher les écritures comptables.  

Dans la liste écritures comptables, sur la ligne contenant l’écriture comptable totalement lettrée vous constatez que la case **Ouvert** n’est pas cochée.  

> [!NOTE]  
>   Une fois que vous avez sélectionné une écriture de la page **Lettrer écritures client** ou plusieurs écritures avec l’**ID lettrage**, le champ **Montant lettré** de la ligne feuille contient la somme des montants restants des écritures validées que vous avez sélectionnées, cela à moins que le champ ne soit déjà renseigné. Si vous sélectionnez **Au plus ancien** dans le champ **Mode de lettrage** sur la fiche client, le lettrage intervient automatiquement.

## Pour lettrer des écritures comptables client avec d’autres écritures dans différentes devises
Si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez toujours lettrer la facture avec le paiement.  

Prenons un exemple. Vous lettrez une écriture (Écriture 1) dans une devise avec une autre écriture (Écriture 2) dans une autre devise. La date de comptabilisation de l’Écriture 1 est utilisée pour trouver le taux de change adéquat et convertir les montants de l’Écriture 2. Le taux de change se trouve sur la page **Taux de change devise**.  

Le lettrage d’écritures comptables client en devises différentes doit être activé. Pour plus d’informations, voir [Activer le lettrage d’écritures comptables client en devises différentes](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille règlements**, puis choisissez le lien associé.
2. Ouvrez la feuille que vous souhaitez, puis renseignez la première ligne vide de la feuille à l’aide d’un code devise.
3. Sélectionnez l’action **Lettrer écritures**.
4. Sélectionnez la ligne comportant l’écriture à lettrer avec l’écriture de la feuille règlement. Sélectionnez ensuite l’action **Définir ID lettrage**, puis sélectionnez l’écriture sur laquelle le lettrage doit être effectué.
5. Cliquez sur le bouton **OK** pour revenir à la feuille règlement.
6. Validez la feuille ventes.  

> [!IMPORTANT]  
>   Lorsque vous lettrez des écritures en devises différentes, les écritures sont converties en USD. Bien que le taux de change des deux devises concernées soit fixe, comme entre l’USD et l’EUR, leur conversion en USD peut donner un petit montant résiduel. Le programme valide ces petits montants résiduels en tant que gains et pertes dans le compte défini dans les champs **Cpte gains constatés report** ou **Cpte pertes constatées report** de la page **Devises**. La valeur du champ **Montant (USD)** est également ajustée sur les écritures comptables fournisseur.  

## Pour créer un lettrage des écritures client
Lorsque vous corrigez une application, des écritures de correction sont créées et validées pour toutes les écritures. Les écritures de correction sont les mêmes que les originales mais elles ont un signe opposé dans le champ **Montant**. Les écritures de correction incluent toutes les écritures du grand livre issues de l’application. Par exemple, l’escompte et les pertes et gains en devise. Les écritures fermées par l’application sont rouvertes.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la fiche client appropriée.
3. Sélectionnez l’action **Écritures comptables**.
4. Sélectionnez l’écriture comptable appropriée, puis sélectionnez l’action **Délettrer les écritures**.
5. Sinon, sélectionnez l’action **Écritures comptables détaillées**.
6. Sélectionnez l’écriture lettrage appropriée, puis sélectionnez l’action **Délettrer les écritures**.
7. Renseignez les champs de l’en-tête, puis sélectionnez l’action **Délettrer**.  

> [!IMPORTANT]  
>   Si une écriture a été lettrée par plusieurs écritures lettrage, vous devez commencer par délettrer la dernière écriture lettrage.  

## Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]