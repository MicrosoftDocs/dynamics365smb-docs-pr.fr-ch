---
title: Configurer le flux de la Yodlee Bank| Microsoft Docs
description: "Vous pouvez convertir les informations paiement dans n'importe quel format de données que votre banque nécessite et activer l'exportation ou l'importation des fichiers bancaires."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa5c0c39dbbce40b59d639f810522c66da1a09ab
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Configurer le service de flux de la Envestnet Yodlee Bank
Vous pouvez importer des relevés bancaires électroniques auprès de votre banque pour renseigner rapidement la fenêtre **Feuille rapprochement bancaire** de sorte à pouvoir lettrer les paiements et rapprocher le compte bancaire. Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Le service de flux de la banque Envestnet Yodlee est installé comme une extension de [!INCLUDE[d365fin](includes/d365fin_md.md)] et est prêt à être activé. Pour plus d'informations, voir [Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md).

> [!NOTE]
> Le service Envestnet Yodlee Bank Feeds n'est pris en charge qu'aux États-Unis, au Canada et au Royaume-Uni.

Une fois que vous avez activé le service de flux bancaire, vous devez lier le compte bancaire au compte bancaire en ligne à partir duquel proviendra le flux. Vous liez des comptes bancaires à des comptes bancaires en ligne dans chacun des scénarios suivants :

* Il n'existe aucun compte bancaire dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour votre compte bancaire en ligne. Par conséquent, vous créez le compte bancaire en le liant à partir du compte bancaire en ligne.
* Il existe un compte bancaire dans [!INCLUDE[d365fin](includes/d365fin_md.md)] que vous souhaitez lier à un compte bancaire en ligne.
* Un compte bancaire lié doit être dissocié car vous souhaitez arrêter d'utiliser le service de flux bancaire pour le compte.
* Les comptes bancaires en ligne ont changé et vous souhaitez mettre à jour les informations relatives aux comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Lorsque le service de flux bancaire est activé, vous pouvez configurer un compte bancaire de sorte à importer automatiquement de nouveaux relevés bancaires dans la fenêtre **Feuille rapprochement bancaire** toutes les deux heures. Les transactions pour les paiements qui ont déjà été validés comme lettrés et/ou rapprochés dans la fenêtre **Feuille rapprochement bancaire** ne sont pas importées. Pour en savoir plus, voir la section « Pour activer l'importation automatique des relevés bancaires ».

> [!NOTE]  
>   Si vous utilisez la configuration assistée Configurer la société, certaines étapes des procédures suivantes s'effectuent automatiquement lorsque vous parvenez à la configuration de compte bancaire de la société. Pour en savoir plus, voir [Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Pour activer le service de flux bancaire
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez le compte bancaire que vous allez utiliser pour le service de flux bancaire.
3. Dans la fenêtre **Compte bancaire**, dans le champ **Format importation relevé bancaire**, sélectionnez YODLEEBANKFEED.  

Le service de flux bancaire est activé lorsque vous liez un compte bancaire à son compte bancaire en ligne connexe. Consultez la procédure suivante.  

## <a name="to-create-a-new-linked-bank-account"></a>Pour créer un compte bancaire lié
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez le compte bancaire approprié, puis sélectionnez **Créer un compte bancaire lié**. La fenêtre **Comptes bancaires liés** s'ouvre au bout de quelques instants.

    > [!NOTE]  
>   Cette fenêtre affiche la page Web réelle du service de flux de la Envestnet Yodlee Bank. La terminologie et la fonctionnalité de la fenêtre peuvent ne pas correspondre aux instructions fournies dans cette rubrique.  
3. Dans la fenêtre **Comptes bancaires en ligne liés**, dans le volet **Lier un compte**, utilisez la fonction de recherche pour trouver la banque qui abrite un ou plusieurs de vos comptes bancaires en ligne.
4. Choisissez le nom de la banque. Le volet **Connexion** s'ouvre.
5. Saisissez le nom de l'utilisateur et le mot de passe que vous utilisez pour la connexion à la banque en ligne, puis cliquez sur le bouton **Suivant**.  
6. Le service de flux bancaire se prépare à lier le premier compte bancaire en ligne de la banque spécifiée à un nouveau compte bancaire dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Si vous disposez de plusieurs comptes bancaires en ligne dans cette banque, vous devez créer des comptes bancaires supplémentaires pour ceux-ci dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Voir les étapes 8 à 10.  

    À la fin du processus, le nom de la banque s'affiche dans le volet **Mes comptes** sur l'onglet **Lié**. Le numéro entre parenthèses indique le nombre de comptes bancaires en ligne ayant été liés.  
7. Cliquez sur le bouton **OK**.

    Si vous liez un seul compte bancaire en ligne, la fenêtre **Fiche compte bancaire archivé** s'ouvre et affiche le nom du compte bancaire en ligne. Dans ce cas, la tâche de liaison de compte bancaire est terminée. Il ne vous reste plus qu'à configurer le compte bancaire. Pour plus d'informations, reportez vous à [Configuration de comptes bancaires](bank-how-setup-bank-accounts.md).

    Si plusieurs comptes bancaires en ligne sont liés, la fenêtre **Comptes bancaires liés** s'ouvre et répertorie les comptes bancaires en ligne supplémentaires qui n'ont pas encore été liés à des comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans ce cas, suivez l'étape suivante.  
8. Dans la fenêtre **Comptes bancaires liés**, sélectionnez la ligne correspondant à un compte bancaire en ligne, puis sélectionnez l'action **Lier à un nouveau compte bancaire**.  

    La fenêtre **Fiche compte bancaire** pour un nouveau compte bancaire s'ouvre et affiche le nom du compte bancaire en ligne.

    Si un compte bancaire existe déjà dans [!INCLUDE[d365fin](includes/d365fin_md.md)] auquel vous souhaitez lier le compte bancaire en ligne supplémentaire, appliquez l'étape suivante.  
9. Dans la fenêtre **Comptes bancaires liés**, sélectionnez la ligne correspondant à un compte bancaire en ligne, puis sélectionnez l'action **Lier à un compte bancaire existant**.
10. Dans la fenêtre **Liste des comptes bancaires**, sélectionnez le compte bancaire que vous voulez lier, puis cliquez sur le bouton **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Pour lier un compte bancaire à un compte bancaire en ligne
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez la ligne correspondant à un compte bancaire qui n'est pas lié à un compte bancaire en ligne, puis sélectionnez l'action **Lier au compte bancaire en ligne**. La fenêtre **Comptes bancaires en ligne liés** s'ouvre, préremplie avec le nom de la banque dans le volet **Lier un compte**.
3. Choisissez le nom de la banque. Le volet **Connexion** s'ouvre.
4. Saisissez le nom de l'utilisateur et le mot de passe que vous utilisez pour la connexion à la banque en ligne, puis cliquez sur le bouton **Suivant**.  

    Le service de flux bancaire se prépare à lier votre compte bancaire dans [!INCLUDE[d365fin](includes/d365fin_md.md)] au compte bancaire en ligne connexe.  

    Une fois le processus terminé avec succès, le nom de la banque s'affiche dans le volet **Mes comptes** sous l'onglet **Lié** . Si la banque a plusieurs comptes bancaires, seul le compte bancaire que vous avez sélectionné à l'étape 2 est lié.  
5. Cliquez sur le bouton **OK**.

Dans la fenêtre **Liste des comptes bancaires**, la case **Lié** est cochée.

## <a name="to-unlink-a-bank-account"></a>Pour détacher un compte bancaire en ligne
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.  
2. Sélectionnez la ligne correspondant à un compte bancaire lié que vous souhaitez détacher du compte bancaire en ligne connexe, puis sélectionnez l'action **Détacher le compte bancaire en ligne**.

> [!NOTE]  
>   Si vous choisissez **Oui** dans la boîte de dialogue de confirmation, le lien vers le compte bancaire en ligne est supprimé, et les informations de connexion sont effacées. Pour lier à nouveau le compte bancaire au compte bancaire en ligne, vous devez vous connecter de nouveau à la banque. Pour en savoir plus, voir la section « Pour lier un compte bancaire à un compte bancaire en ligne ».

## <a name="to-update-bank-account-linking"></a>Pour mettre à jour la liaison des comptes bancaires
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez le compte bancaire approprié, puis sélectionnez l'action **Mettre à jour la liaison des comptes bancaires**.

Si des problèmes existent pour les comptes bancaires liés dans la fenêtre **Liste des comptes bancaires**, la fenêtre **Comptes bancaires liés** s'ouvre et indique les comptes bancaires affectés par des problèmes. Le meilleur moyen de résoudre ces problèmes est de détacher le compte bancaire en ligne, puis de recréer le lien. Pour en savoir plus, voir la section « Pour lier un compte bancaire à un compte bancaire en ligne ».

## <a name="to-enable-automatic-import-of-bank-statements"></a>Pour activer l'importation automatique des relevés bancaires
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez la ligne correspondant à un compte bancaire lié, puis sélectionnez l'action **Configuration de l'importation de relevés bancaires automatique**.
3. Dans la fenêtre **Configuration de l'importation de relevés bancaires automatique**, dans le champ **Nombre de jours inclus**, indiquez jusqu'à quelle date il faut remonter dans le temps pour obtenir les nouvelles transactions bancaires.

    > [!NOTE]  
>   Il est recommandé de définir cette valeur à 7 jours ou plus.  
4. Cochez la case **Activé**.  

Toutes les heures, la fenêtre **Feuille rapprochement bancaire** affichera les nouveaux paiements effectués sur le compte bancaire en ligne.

> [!NOTE]  
>   Les transactions pour les paiements qui ont déjà été validés comme lettrés et/ou rapprochés dans la fenêtre **Feuille rapprochement bancaire** ne sont pas importées.

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

