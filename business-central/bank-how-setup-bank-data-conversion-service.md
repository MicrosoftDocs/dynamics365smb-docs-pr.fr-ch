---
title: Configurer le service de conversion de données bancaires
description: 'Vous pouvez configurer des comptes bancaires pour suivre les transactions et importer ou exporter des flux bancaires, tels que Yodlee.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Configurer l’extension AMC Banking 365 Fundamentals
Un fournisseur global de services permettant de convertir les informations de paiement dans n’importe quel format de données que votre banque requiert est connecté et prêt à être activé dans [!INCLUDE[prod_short](includes/prod_short.md)]. Dans cette rubrique [!INCLUDE[prod_short](includes/prod_short.md)], il s’agit de l’extension AMC Banking 365 Fundamentals.

Vous pouvez exporter des lignes de paiement à partir de la page **Feuille paiement** vers un fichier ou un flux de données que vous téléchargez ensuite vers votre banque pour un traitement automatique. Ainsi, vous n’avez pas à effectuer de paiements électroniques individuels. Pour plus d’informations, reportez-vous à [Exportation de paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Vous pouvez importer des fichiers de relevé bancaire sur la page **Feuille rapprochement bancaire** à l’aide de l’extension AMC Banking 365 Fundamentals pour convertir un fichier que vous recevez de votre banque en flux de données que [!INCLUDE[prod_short](includes/prod_short.md)] peut importer. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Vous pouvez utiliser le service Envestnet Yodlee Bank Feeds au lieu d’importer des relevés bancaires avec l’extension AMC Banking 365 Fundamentals. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Pour importer ou exporter des fichiers bancaires, vous devez configurer votre propre compte bancaire et les comptes bancaires de vos fournisseurs. Pour plus d’informations, reportez vous à [Configuration de comptes bancaires](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> L’extension AMC Banking 365 Fundamentals peut fixer une limite imposée du nombre de lignes qui peuvent être exportées dans un fichier. Si cette limite est dépassée, vous recevrez un message d’erreur. Il est conseillé que les fichiers de relevé bancaire ne dépassent pas 1 000 lignes, sans quoi le temps de traitement dans l’extension AMC Banking 365 Fundamentals peut augmenter de façon significative.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Pour inscrire votre société à l’extension AMC Banking 365 Fundamentals
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres service conv. données banque**, puis choisissez le lien associé.  
2. La page **Paramètres service conv. données banque** s’ouvre avec trois champs préremplis avec les URL appropriées du fournisseur de l’extension AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   Dans la base de données de démonstration CRONUS International Ltd., les champs Nom d’utilisateur et Mot de passe sont préremplis avec les informations de connexion à la démonstration, que vous remplacerez par les informations réelles de votre société en vous inscrivant à l’extension AMC Banking 365 Fundamentals.
3. Dans le champ **URL d’inscription**, cliquez sur le bouton de navigateur pour ouvrir la page d’inscription du fournisseur de service.  
4. Dans la page d’inscription du fournisseur de services de données bancaires, entrez le nom de l’utilisateur et le mot de passe de l’abonnement de votre société au service, puis suivez le processus d’inscription comme indiqué par le fournisseur de service.

    Votre société est désormais inscrite à l’extension AMC Banking 365 Fundamentals. Entrez maintenant le nom de l’utilisateur et le mot de passe que vous avez spécifiés pour le service dans les champs de configuration associés dans [!INCLUDE[prod_short](includes/prod_short.md)].

5. Sur la page **Paramètres service conv. données banque**, dans le champ **Nom d’utilisateur**, entrez la même valeur que vous avez validée comme nom de connexion dans la page du fournisseur de service au cours de l’étape 4.
6. Dans le champ **Mot de passe**, entrez la même valeur que vous avez saisie dans le champ **Mot de passe** de la page du fournisseur de service au cours de l’étape 4.

> [!NOTE]  
> Vos données de connexion sont automatiquement chiffrées.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Pour afficher ou mettre à jour la liste des formats de données bancaires actuellement pris en charge
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres service conv. données banque**, puis choisissez le lien associé.
2. Sur la page **Paramètres service conv. données banque**, sélectionnez l’action **Nom banque - Liste conversions données** pour ouvrir la liste des noms de banques représentant les formats de données bancaires pris en charge par le service de conversion.
3. Sur la page **Nom banque - Liste conversions données**, sélectionnez l’action **Mettre à jour liste noms banque**.

La liste des formats de données bancaires qui sont pris en charge par l’extension AMC Banking 365 Fundamentals est désormais mise à jour. Il s’agit de la liste de noms de banques, filtrés par pays/région, que vous pouvez sélectionner dans le champ **Nom banque - Conversion données** de la page **Fiche compte bancaire**.

> [!NOTE]  
>   Les formats de données bancaires pris en charge sont aussi mis à jour lorsque vous sélectionnez ou entrez une valeur dans le champ **Nom banque - Conversion données** du compte bancaire.

Vous êtes désormais inscrit à l’extension AMC Banking 365 Fundamentals. Continuez pour refléter les informations de connexion sur chaque compte bancaire qui utilise le service.

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
