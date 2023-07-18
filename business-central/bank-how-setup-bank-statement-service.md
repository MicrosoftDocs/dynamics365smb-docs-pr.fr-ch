---
title: Configurer Yodlee Bank Feeds
description: Vous pouvez convertir les informations paiement dans n’importe quel format de données que votre banque nécessite et activer l’exportation ou l’importation des fichiers bancaires.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.search.form: '1280, 1290'
ms.date: 04/01/2021
ms.author: edupont
---
# Configurer le service Envestnet Yodlee Bank Feeds

Vous pouvez importer des relevés bancaires électroniques auprès de votre banque pour renseigner rapidement la page **Feuille rapprochement bancaire** de sorte à pouvoir lettrer les paiements et rapprocher le compte bancaire. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> En raison de la directive sur les services de paiement en Europe (PSD2), après le 14 septembre 2019, vous ne pourrez plus importer automatiquement des relevés bancaires de banques du Royaume-Uni vers [!INCLUDE[prod_short](includes/prod_short.md)]. Nous étudions la possibilité de proposer cette fonctionnalité à l’avenir.

> [!NOTE]
> Le service Envestnet Yodlee Bank Feeds est uniquement pris en charge dans la version en ligne de Business Central. Pour utiliser cette fonctionnalité sur site, vous devez obtenir un compte de cobrand d’Envestnet et vous devez ajouter du code pour l’intégrer à l’API Yodlee.
>
> Le service Envestnet Yodlee Bank Feeds n’est pris en charge qu’aux États-Unis et au Canada.
> Seules les banques résidant dans ces pays/régions sont prises en charge, même si des banques d’autres pays/régions peuvent apparaître dans la fenêtre de sélection des banques Envestnet Yodlee Bank Feeds dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Pour obtenir une assistance technique sur les fonctionnalités d’Envestnet Yodlee, contactez le support technique Microsoft. Ne contactez pas Envestnet Yodlee. Pour plus d’informations, voir [Configuration du support technique pour Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

Le service Envestnet Yodlee Bank Feeds est installé comme une extension de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne et est prêt à être activé dans les pays/régions pris en charge. Pour plus d’informations, voir [Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md).

Une fois que vous avez activé le service de flux bancaire, vous devez lier le compte bancaire au compte bancaire en ligne à partir duquel proviendra le flux. Vous liez des comptes bancaires à des comptes bancaires en ligne dans chacun des scénarios suivants :

* Il n’existe aucun compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] pour votre compte bancaire en ligne. Par conséquent, vous créez le compte bancaire en le liant à partir du compte bancaire en ligne.
* Il existe un compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] que vous souhaitez lier à un compte bancaire en ligne.
* Un compte bancaire lié doit être dissocié car vous souhaitez arrêter d’utiliser le service de flux bancaire pour le compte.
* Les comptes bancaires en ligne ont changé et vous souhaitez mettre à jour les informations relatives aux comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)].

Lorsque le service de flux bancaire est activé, vous pouvez configurer un compte bancaire de sorte à importer automatiquement de nouveaux relevés bancaires sur la page **Feuille rapprochement bancaire** toutes les deux heures. Les transactions pour les paiements qui ont déjà été validés comme lettrés et/ou rapprochés sur la page **Feuille rapprochement bancaire** ne sont pas importées. Pour en savoir plus, voir la section « Pour activer l’importation automatique des relevés bancaires ».

> [!NOTE]  
> Si vous utilisez le guide de configuration assistée Configurer la société, certaines étapes des procédures suivantes s’effectuent automatiquement lorsque vous parvenez à la configuration de compte bancaire de la société. Pour plus d’informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).

## Pour activer le service de flux bancaire
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez le compte bancaire que vous allez utiliser pour le service de flux bancaire.
3. Sur la page **Compte bancaire**, dans le champ **Format importation relevé bancaire**, sélectionnez YODLEEBANKFEED.  

Le service de flux bancaire est activé lorsque vous liez un compte bancaire à son compte bancaire en ligne connexe. Consultez la procédure suivante.  

> [!NOTE]
> Si vous utilisez le guide de configuration assistée **Configuration de la société**, vous activez le service en activant la case à cocher **Utilisez un service de flux bancaire**. Pour plus d’informations, voir [Création de sociétés dans Business Central](about-new-company.md).

## Pour créer un compte bancaire lié
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire approprié, puis sélectionnez **Créer un compte bancaire lié**. La page **Comptes bancaires liés** s’ouvre au bout de quelques instants.

    > [!NOTE]  
    > Cette page affiche la page Web réelle du service Envestnet Yodlee Bank Feeds. La terminologie et la fonctionnalité de la page peuvent ne pas correspondre aux instructions fournies dans cette rubrique.  
3. Sur la page **Comptes bancaires en ligne liés**, dans le volet **Lier un compte**, utilisez la fonction de recherche pour trouver la banque qui abrite un ou plusieurs de vos comptes bancaires en ligne.
4. Choisissez le nom de la banque. Le volet **Connexion** s’ouvre.
5. Saisissez le nom de l’utilisateur et le mot de passe que vous utilisez pour la connexion à la banque en ligne, puis cliquez sur le bouton **Suivant**.  
6. Le service de flux bancaire se prépare à lier le premier compte bancaire en ligne de la banque spécifiée à un nouveau compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Si vous disposez de plusieurs comptes bancaires en ligne dans cette banque, vous devez créer des comptes bancaires supplémentaires pour ceux-ci dans [!INCLUDE[prod_short](includes/prod_short.md)]. Voir les étapes 8 à 10.  

    À la fin du processus, le nom de la banque s’affiche dans le volet **Mes comptes** sur l’onglet **Lié**. Le numéro entre parenthèses indique le nombre de comptes bancaires en ligne ayant été liés.  
7. Choisissez le bouton **OK**.

    Si vous liez un seul compte bancaire en ligne, la page **Fiche compte bancaire archivé** s’ouvre et affiche le nom du compte bancaire en ligne. Dans ce cas, la tâche de liaison de compte bancaire est terminée. Il ne vous reste plus qu’à configurer le compte bancaire. Pour plus d’informations, reportez vous à [Configuration de comptes bancaires](bank-how-setup-bank-accounts.md).

    Si plusieurs comptes bancaires en ligne sont liés, la page **Comptes bancaires liés** s’ouvre et répertorie les comptes bancaires en ligne supplémentaires qui n’ont pas encore été liés à des comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)]. Dans ce cas, suivez l’étape suivante.  
8. Sur la page **Comptes bancaires liés**, sélectionnez la ligne correspondant à un compte bancaire en ligne, puis sélectionnez l’action **Lier à un nouveau compte bancaire**.  

    La page **Fiche compte bancaire** pour un nouveau compte bancaire s’ouvre et affiche le nom du compte bancaire en ligne.

    Si un compte bancaire existe déjà dans [!INCLUDE[prod_short](includes/prod_short.md)] auquel vous souhaitez lier le compte bancaire en ligne supplémentaire, appliquez l’étape suivante.  
9. Sur la page **Comptes bancaires liés**, sélectionnez la ligne correspondant à un compte bancaire en ligne, puis sélectionnez l’action **Lier à un compte bancaire existant**.
10. Sur la page **Liste des comptes bancaires**, sélectionnez le compte bancaire que vous voulez lier, puis cliquez sur le bouton **OK**.

## Pour lier un compte bancaire à un compte bancaire en ligne
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne correspondant à un compte bancaire qui n’est pas lié à un compte bancaire en ligne, puis sélectionnez l’action **Lier au compte bancaire en ligne**. La page **Comptes bancaires en ligne liés** s’ouvre, préremplie avec le nom de la banque dans le volet **Lier un compte**.
3. Choisissez le nom de la banque. Le volet **Connexion** s’ouvre.
4. Saisissez le nom de l’utilisateur et le mot de passe que vous utilisez pour la connexion à la banque en ligne, puis cliquez sur le bouton **Suivant**.  

    Le service de flux bancaire se prépare à lier votre compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] au compte bancaire en ligne connexe.  

    Une fois le processus terminé avec succès, le nom de la banque s’affiche dans le volet **Mes comptes** sous l’onglet **Lié** . Si la banque a plusieurs comptes bancaires, seul le compte bancaire que vous avez sélectionné à l’étape 2 est lié.  
5. Choisissez le bouton **OK**.

Sur la page **Liste des comptes bancaires**, la case **Lié** est cochée.

## Pour modifier les informations d’identification d’un compte bancaire en ligne
1. Choisissez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.  
2. Sélectionnez la ligne correspondant à un compte bancaire qui est liée à un compte bancaire en ligne, puis sélectionnez l’action **Modifier les informations sur le compte bancaire en ligne**.
3. Mettez à jour les informations de connexion.

## Pour détacher un compte bancaire en ligne
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.  
2. Sélectionnez la ligne correspondant à un compte bancaire lié que vous souhaitez détacher du compte bancaire en ligne connexe, puis sélectionnez l’action **Détacher le compte bancaire en ligne**.

> [!NOTE]  
> Si vous choisissez **Oui** dans la boîte de dialogue de confirmation, le lien vers le compte bancaire en ligne est supprimé, et les informations de connexion sont effacées. Pour lier à nouveau le compte bancaire au compte bancaire en ligne, vous devez vous connecter de nouveau à la banque. Pour en savoir plus, voir la section « Pour lier un compte bancaire à un compte bancaire en ligne ».

## Pour mettre à jour la liaison des comptes bancaires
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire approprié, puis sélectionnez l’action **Mettre à jour la liaison des comptes bancaires**.

Si des problèmes existent pour les comptes bancaires liés sur la page **Liste des comptes bancaires**, la page **Comptes bancaires liés** s’ouvre et indique les comptes bancaires affectés par des problèmes. Le meilleur moyen de résoudre ces problèmes est de détacher le compte bancaire en ligne, puis de recréer le lien. Pour en savoir plus, voir la section « Pour lier un compte bancaire à un compte bancaire en ligne ».

## Pour activer l’importation automatique des relevés bancaires
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne correspondant à un compte bancaire lié, puis sélectionnez l’action **Configuration de l’importation de relevés bancaires automatique**.
3. Sur la page **Configuration de l’importation de relevés bancaires automatique**, dans le champ **Nombre de jours inclus**, indiquez jusqu’à quelle date il faut remonter dans le temps pour obtenir les nouvelles transactions bancaires.

    > [!NOTE]  
    > Il est recommandé de définir cette valeur à 7 jours ou plus.  
4. Cochez la case **Activé**.  

Toutes les heures, la page **Feuille rapprochement bancaire** affichera les nouveaux paiements effectués sur le compte bancaire en ligne.

> [!NOTE]  
> Les transactions pour les paiements qui ont déjà été validés comme lettrés et/ou rapprochés sur la page **Feuille rapprochement bancaire** ne sont pas importées.

## Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions ](ui-extensions.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]