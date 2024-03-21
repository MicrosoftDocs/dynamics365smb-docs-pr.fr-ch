---
title: Utilisation de l’extension AMC Banking 365 Fundamentals
description: Découvrez comment échanger facilement des données avec vos banques en les transformant au format souhaité.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bank, format, data'
ms.search.form: '20100, 20101, 20102, 20105, 20106, 20107, 20109,'
ms.date: 09/20/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="use-the-amc-banking-365-fundamentals-extension"></a>Utiliser l’extension AMC Banking 365 Fundamentals

L’extension AMC Banking 365 Fundamentals facilite et précise l’envoi des données à vos banques. L’extension connecte [!INCLUDE[prod_short](includes/prod_short.md)] au service AMC Banking 365 Fundamentals pour Microsoft Dynamics 365 Business Central, qui peut convertir les données bancaires de [!INCLUDE[prod_short](includes/prod_short.md)] dans des formats exigés par plus de 600 banques du monde entier. Par exemple, cela facilite le transfert des paiements et des crédits aux fournisseurs en entrant les paiements dans [!INCLUDE[prod_short](includes/prod_short.md)], puis en les téléchargeant dans votre banque. Les formats peuvent également faciliter les processus de rapprochement bancaire. Pour plus d’informations, voir [AMC Banking pour Microsoft Dynamics 365 Business Central](https://www.amcbanking.com/bc-fundamentals/).

> [!NOTE]
> AMC Banking a créé des extensions supplémentaires qui fonctionnent avec [!INCLUDE[prod_short](includes/prod_short.md)]. Cette rubrique décrit uniquement l’extension Fundamental.

> [!NOTE]
> Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], un fournisseur global de services pour convertir les données bancaires dans n’importe quel format de fichier que votre banque requiert est paramétré et connecté. Dans les versions nord-américaines, le même service peut être utilisé pour envoyer des fichiers de paiement sous forme de transfert de fonds électronique (EFT), par exemple le réseau ACH (Automated Clearing House), mais avec un processus légèrement différent.

## <a name="use-our-demonstration-account"></a>Utiliser notre compte de démonstration

[!INCLUDE[prod_short](includes/prod_short.md)] est fourni avec un compte de démonstration qui vous permet d’essayer l’extension AMC Banking 365 Fundamentals. Nous fournissons les paramètres par défaut pour la connexion à AMC Banking, en spécifiant les comptes bancaires à partir desquels obtenir des données dans [!INCLUDE[prod_short](includes/prod_short.md)], plus quelques définitions d’échange de données. Vous pouvez afficher les paramètres de connexion sur la page **Configuration AMC Banking**. Pour les comptes bancaires, l’extension applique des valeurs dans les champs **Nom banque**, **N° msg. virement**, **Format importation relevé bancaire** et **Format exportation paiement** dans les fiches de compte bancaire.

Nous fournissons les paramètres, mais, pour essayer l’extension, vous devez exécuter le guide de configuration assistée pour les appliquer. Pour exécuter le guide, sur la page **Configuration AMC Banking**, choisissez l’action **Configuration assistée**.

> [!NOTE]
> Il y a quelques limitations sur le compte de démonstration. Par exemple, lorsque vous convertissez des paiements, le montant du fichier converti ne correspond pas au montant réel. Au lieu de cela, le montant est toujours de cinq unités de la devise utilisée pour les paiements.  

## <a name="setting-up-the-extension"></a>Configuration de l’extension

Débuter avec l’extension ne nécessite que quelques étapes simples et un guide de configuration assistée établit la connexion et active l’extension. Le guide effectue des tâches, telles que l’installation des définitions d’échange de données pour les configurations d’importation/exportation de relevé bancaire et la création de souches de numéros pour les messages de virement.  

### <a name="to-set-up-the-required-permission-sets"></a>Pour configurer les ensembles d’autorisations requis

Avant que les utilisateurs puissent utiliser cette extension, votre administrateur doit copier les ensembles d’autorisations suivants, les modifier, puis attribuer les nouveaux ensembles d’autorisations aux utilisateurs au lieu de l’original :

* **D365 Basic**
* **Membre de l’équipe D365**
* **D365 Read**
* **IntelligentCloudBC**

Pour plus d’informations, voir [Pour copier un ensemble d’autorisations](ui-define-granular-permissions.md#to-copy-a-permission-set).

Pour chaque nouvel ensemble d’autorisations, accordez uniquement l’autorisation **Lecture** pour le **Tableau de configuration AMC Banking (20101)**. Pour plus d’informations, voir [Pour créer ou modifier des autorisations manuellement](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-connect-the-extension-to-amc-banking"></a>Pour connecter l’extension à AMC Banking

1. Obtenez un module et un plan de service pour AMC Banking. Pour ce faire, visitez la page [Licence AMC](https://license.amcbanking.com/register).
2. Dans [!INCLUDE[prod_short](includes/prod_short.md)], sélectionnez l’![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configurer AMC Banking**, puis choisissez le lien associé.  
3. Sur la page **Configuration AMC Banking**, choisissez l’action **Configuration assistée**.
4. Exécutez les étapes du guide de configuration assistée.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Pour connecter les comptes bancaires à l’extension

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez la fiche du compte bancaire que vous souhaitez connecter au service.
3. Dans le champ **Nom banque**, choisissez le format requis par votre banque.  

   Les formats sont filtrés pour afficher uniquement ceux qui sont pertinents pour le pays/la région spécifié pour le compte bancaire.
4. Dans le champ **N° msg. virement**, choisissez la souche de numéros à utiliser pour les messages accompagnant les paiements.
5. Dans les champs **Format importation relevé bancaire** et **Format exportation paiement**, choisissez les définitions d’échange de données requises par votre banque.

## <a name="use-the-extension"></a>Utiliser l’extension

L’utilisation de cette extension consiste simplement à exporter des données sur la page **Feuilles paiement**, puis à les téléchargeant vers le service web de votre banque. Pour plus d’informations, voir [Exécution de paiements avec le service de conversion de données bancaires ou un virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!NOTE]
> Vous devez remplir les champs **Code SWIFT** et **IBAN** pour chaque compte bancaire.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Pour exporter des données et les envoyer à votre banque

> [!CAUTION]  
> Lorsque vous exportez des données à l’aide de l’extension AMC Banking 365 Fundamentals, certaines de vos données métier sont exposées au fournisseur du service. Le fournisseur de service, AMC Consult A/S, est responsable de la confidentialité de ces données. Pour plus d’informations, reportez\-vous à [Politique de confidentialité AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles paiement**, puis choisissez le lien associé.
2. Créez les lignes feuille à exporter.  

   > [!NOTE]
   > Pour chaque ligne, pensez à choisir **Paiement électronique** dans le champ **Mode émission paiement**.
3. Sélectionnez l’option **Exporter**.

### <a name="to-import-and-apply-the-converted-file"></a>Pour importer et appliquer le fichier converti

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille rapprochement bancaire**, puis sélectionnez le lien associé.
2. Choisir l’action **Importer les transactions bancaires**, puis choisissez le fichier converti.  

   [!INCLUDE[prod_short](includes/prod_short.md)] va créer une nouvelle feuille rapprochement bancaire contenant les données du fichier. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Voir aussi

[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
