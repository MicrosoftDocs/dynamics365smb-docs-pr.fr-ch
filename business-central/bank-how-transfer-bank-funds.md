---
title: Transfert de fonds à la banque
description: 'Vous pouvez transférer des montants d’un compte bancaire à un autre, y compris dans différentes devises, en validant la transaction dans la feuille comptabilité.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: edupont
---
# <a name="transfer-bank-funds"></a>Transfert de fonds à la banque

Il peut vous arriver de devoir transférer un montant d’un compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] vers un autre. Pour ce faire, vous devez valider la transaction sur la page **Feuille comptabilité**. La tâche varie selon que les comptes bancaires utilisent la même devise ou des devises différentes.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Pour valider un transfert entre comptes bancaires avec le même code devise

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille comptabilité**, puis choisissez le lien associé.
2. Dans une ligne feuille, renseignez les champs **Date comptabilisation** et **N° document** .
3. Cliquez sur le champ **Type compte**, sélectionnez le **Compte bancaire**.
4. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
5. Dans le champ **Montant**, entrez le total à transférer.

    Ensuite, vous devez spécifier le compte contrepartie. Si vous ne visualisez pas les champs appropriés, choisissez l′action **Afficher plus de colonnes** pour afficher tous les champs disponibles.
6. Dans le champ **Type compte contrepartie**, sélectionnez **Compte bancaire**.
7. Dans le champ **N° compte contrepartie**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
8. Validez la feuille.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Pour valider des transferts entre comptes bancaires dotés de codes devise différents

Pour transférer des fonds entre des comptes bancaires qui utilisent des devises différentes, vous devez valider deux lignes feuille comptabilité.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille comptabilité**, puis choisissez le lien associé.
2. Créez deux lignes feuille, et renseignez les champs **Date comptabilisation** et **N° document**.
3. Sur la première ligne feuille, dans le champ **Type**, sélectionnez **Compte bancaire**.
4. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
5. Dans le champ **Montant**, saisissez le montant dans la devise du compte bancaire avec ou sans signe moins.

    > [!TIP]
    > Un montant sans signe est un débit et un montant avec un signe moins est un crédit.

    > [!NOTE]
    > Certaines entreprises préfèrent effectuer des transferts entre comptes sur des lignes feuille distinctes. D′autres entreprises préfèrent tout valider sur une seule ligne feuille en utilisant un compte contrepartie. Consultez votre expert local si vous ne savez pas quoi faire.
    >
    > Si votre entreprise préfère utiliser un compte contrepartie, définissez le champ **Type compte contrepartie** sur **Compte bancaire** et définissez le champ **N° compte contrepartie** sur le compte bancaire sur lequel vous souhaitez transférer les fonds. Passez ensuite à l′étape 9 ou 10.
    >
    > Si votre entreprise préfère utiliser une ligne feuille distincte, passez à l′étape suivante.
6. Sur la seconde ligne feuille, dans le champ **Type**, sélectionnez **Compte bancaire**.
7. Dans le champ **N° compte**, sélectionnez le compte bancaire à partir duquel vous souhaitez transférer les fonds.
8. Dans le champ **Montant**, saisissez le montant dans la devise du compte bancaire avec ou sans signe moins.

    > [!TIP]
    > Un montant sans signe est un débit et un montant avec un signe moins est un crédit.
9. Si les taux de change utilisés dans la feuille sont différents des taux de change de la page **Taux de change devise**, saisissez une nouvelle ligne feuille pour les pertes ou les gains de change.  

    1. Entrez **Compte général** dans le champ **Type compte**.  

    2. Entrez le numéro de compte général pour les gains ou les pertes liés au taux de change dans le champ **N° compte**.  

    3. Saisissez le gain ou la perte de change dans le champ **Montant** avec ou sans signe moins.

    > [!TIP]
    > Un montant sans signe est un débit et un montant avec un signe moins est un crédit.
10. Validez la feuille.

## <a name="see-also"></a>Voir aussi

[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
