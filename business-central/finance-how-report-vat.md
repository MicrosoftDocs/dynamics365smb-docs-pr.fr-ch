---
title: Envoyer les déclarations de TVA destinées à l'administration fiscale | Microsoft Docs
description: Apprendre à préparer les déclarations qui répertorient la TVA des ventes au cours d'une période, ou à partir des ventes et achats, et envoyer la déclaration à l'administration fiscale.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7365886f09e1e3d1b67dcbea82594f3d3599f25a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183899"
---
# <a name="report-vat-to-tax-authorities"></a>Déclarer la TVA aux autorités fiscales
Cette rubrique décrit les états dans [!INCLUDE[d365fin](includes/d365fin_md.md)] que vous pouvez utiliser pour envoyer des informations sur les montants de la taxe sur la valeur ajoutée (TVA) relatifs aux ventes et achats à l'administration fiscale de votre région.

Vous pouvez utiliser les états suivants :

* La déclaration de liste de vente de l'Union européenne (EU) **Liste des ventes UE** répertorie les montants de la taxe sur la valeur ajoutée (TVA) que vous avez collectés pour les ventes aux clients enregistrés dans les pays de l'Union européenne (UE).  
* L'état **Retour TVA** inclut la TVA pour les ventes et les achats aux clients dans tous les pays utilisant la TVA.

Si vous souhaitez afficher un historique complet des écritures TVA, chaque validation impliquant la TVA crée une écriture dans la page **Écritures TVA**. Ces écritures sont utilisées pour calculer le montant de votre déclaration TVA, tel que paiement et remboursement, pour une période donnée. Pour afficher des écritures TVA, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures TVA**, puis sélectionnez le lien associé.

## <a name="about-the-ec-sales-list-report"></a>À propos de l'état Liste des ventes UE
Au Royaume-Uni, toutes les sociétés qui vendent des biens et des services aux clients enregistrés pour la TVA, y compris les clients dans d'autres pays de l'Union européenne (UE), doivent envoyer une version électronique de l'état Liste des ventes de la Communauté européenne (CE) au format XML sur le site Web du service de la fiscalité et des douanes du Royaume-Uni. La liste des ventes de l'Union européenne ne fonctionne que pour les pays de l'UE.

La déclaration comprend une ligne pour chaque type de transaction avec le client, et affiche le montant total pour chaque type de transaction. La déclaration peut inclure trois types de transactions :  

* Marchandises B2B  
* Services B2B  
* Marchandises triangulées B2B  

Les biens et des services B2B indiquent si vous avez vendu un bien ou un service, et sont contrôlés par le paramètre **Service UE** des paramètres validation TVA. Les marchandises triangulées B2B indiquent si vous vous êtes engagé dans des transactions avec un tiers, et sont contrôlées par le paramètre **Trans. tripartite UE** sur les documents vente, comme des commandes vente, des factures, des avoirs, etc.  

Une fois que l'administration fiscale aura examiné votre état, elle devra envoyer un e-mail au contact de votre société. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le contact est spécifié sur la page **Informations société**. Avant de soumettre l'état, assurez-vous qu'un contact est sélectionné.

## <a name="about-the-vat-return-report"></a>À propos de l'état Retour TVA
Utilisez cet état pour envoyer les documents relatifs à la TVA sur les ventes et les achats, tels que les commandes d'achat et de vente, les factures et les avoirs. Les informations contenues dans l'état sont au même format que dans la déclaration de l'administration fiscale et douanière.  

La TVA est calculée sur la base des paramètres validation TVA et des groupes comptabilisation TVA que vous avez définis.

Pour le retour TVA, vous pouvez spécifier les écritures pour :

* Envoyer les transactions ouvertes uniquement, ou ouvertes et clôturées. Par exemple, cela est utile lorsque vous préparez votre retour TVA annuel final.
* Envoyer uniquement les écritures des périodes définies, ou inclure également les écritures des périodes précédentes. Cette fonction est utile pour mettre à jour un retour TVA déjà envoyé, par exemple, si un fournisseur vous envoie une facture échue.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Pour vous connecter au service Web de votre administration fiscale
[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des connexions de service à des sites Web d'administrations fiscales. Par exemple, si vous vous trouvez au Royaume-uni, vous pouvez activer la connexion de service **GovTalk** pour envoyer la liste des ventes UE et les états de retour TVA par voie électronique. Si vous souhaitez envoyer l'état manuellement, par exemple en saisissant vos données sur le site Web de l'administration fiscale, cela n'est pas nécessaire.   

Pour déclarer la TVA à une administration par voie électronique, vous devez connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] au service Web de l'administration fiscale. Cela suppose que vous configuriez un compte avec votre administration fiscale. Lorsque vous avez un compte, vous pouvez activer une connexion de service que nous fournissons dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Connexions au service**, puis sélectionnez le lien approprié.
2. Renseignez les champs requis. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Il est judicieux de tester votre connexion. Pour cela, choisissez la case à cocher **Mode test**, puis préparez et envoyez votre état TVA comme décrit dans la section _Préparer et envoyer un état TVA_. En mode Test, le service vérifie si l'administration fiscale peut recevoir votre état, et le statut de l'état indiquera si l'envoi du test a réussi. Il est important de retenir que ce n'est pas un envoi réel. Pour réellement envoyer l'état, vous devez désactiver la case à cocher **Mode test**, puis répéter le processus d'envoi.

## <a name="to-set-up-vat-reports-in-d365fin"></a>Pour configurer les états TVA dans [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage déclaration TVA**, puis sélectionnez le lien associé.  
2. Pour laisser des utilisateurs modifier et retourner cet état, sélectionnez la case à cocher **Modifier les états soumis**.  
3. Choisissez la souche de numéros à utiliser pour chaque état.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Pour préparer et soumettre un état TVA
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste des ventes UE** ou **Retour TVA**, puis sélectionnez le lien associé.  
2. Sélectionnez **Nouveau**, puis renseignez les champs requis. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour générer le contenu de l'état, sélectionnez l'action **Proposer lignes**.  

    > [!NOTE]  
    >   Pour l'état Liste des ventes UE, vous pouvez consulter les transactions incluses dans les lignes de l'état avant d'envoyer l'état. Pour cela, sélectionnez la ligne, puis cliquez sur l'action **Afficher écritures TVA**.  
4. Pour valider et préparer l'état pour l'envoi, choisissez l'action **Emettre**.  

    > [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] confirme que l'état est configuré correctement. Si la validation échoue, les erreurs sont affichées sous **Erreurs et avertissements**, de sorte que vous sachiez quoi corriger. Généralement, si le message concerne un paramètre manquant dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez cliquer sur le message pour ouvrir la page contenant les informations à corriger.  
5. Pour envoyer l'état, sélectionnez l'action **Soumettre**.  

Une fois que vous envoyez la déclaration, [!INCLUDE[d365fin](includes/d365fin_md.md)] surveille le service et conserve un enregistrement de vos communications. Le champ **Statut** indique l'état de la déclaration en cours. Par exemple, lorsque l'administration traite votre déclaration, le statut de celle-ci passe à **Réussie**. Si l'administration fiscale trouve des erreurs dans la déclaration que vous avez envoyée, le statut de celle-ci est **Échec**. Vous pouvez afficher les erreurs sous **Erreurs et avertissements**, corrigez-les, puis envoyez la déclaration. Pour visualiser une liste de toutes vos déclarations de liste des ventes UE, consultez la page **États de liste des ventes UE**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Affichage de l’historique des communications avec votre administration fiscale
Dans certains pays, vous échangez des messages avec l'administration fiscale lorsque vous envoyez des états. Vous pouvez afficher le premier et le dernier message que vous avez envoyés ou reçus en choisissant **Télécharger le message d’envoi** et les actions **Télécharger le message de réponse**.  

## <a name="submitting-vat-reports-manually"></a>Envoi manuel des états TVA
Si vous utilisez une autre méthode pour envoyer l'état, par exemple en exportant le XML et en le téléchargeant sur le site Web d'une administration fiscale, vous pouvez ensuite choisir **Marquer comme Soumis** pour clôturer la période de référence. Lorsque vous signalez un état comme lancé, vous ne pouvez plus le modifier. Si vous devez modifier l'état après l'avoir signalé comme lancé, vous devez le rouvrir.

## <a name="vat-settlement"></a>Déclaration de TVA
Périodiquement, vous devez régler la TVA nette aux autorités fiscales. Si vous devez effectuer des déclarations de TVA fréquemment, vous pouvez exécuter le traitement par lots **Calculer et valider décl. TVA** pour clôturer les écritures TVA ouvertes et transférer les montants TVA achat et vente dans le compte de déclaration TVA.

Lors du transfert des montants TVA vers le compte de déclaration, le compte TVA achat est crédité et le compte TVA vente est débité sur la base des montants calculés pour la période spécifiée. Le montant net est crédité ou débité, si le montant achat TVA est supérieur, sur le compte de déclaration TVA. Vous pouvez valider la déclaration immédiatement ou imprimer d'abord une impression test.  

> [!Note]
> Lorsque vous utilisez le traitement par lots **Calculer et valider décl. TVA**, si vous ne spécifiez pas **Groupe compta. marché TVA** ni **Groupe compta. produit TVA**, les écritures contenant les codes des groupes comptabilisation marché et des groupes comptabilisation produit sont incluses.

## <a name="configuring-your-own-vat-reports"></a>Configuration de vos propres états de TVA
Vous pouvez utiliser l'état Liste des ventes UE prédéfini, cependant, vous pouvez également créer vos propres états. Cela nécessite de créer des codeunits. Si vous avez besoin de l'aide à cette fin, contactez un partenaire certifié Microsoft.  

Le tableau suivant décrit les codeunits que vous devez créer pour votre état.

| Codeunit | Ce qu'il doit effectuer |
|----|-----|
|Proposer lignes| Extraire les informations de la table Ecritures TVA, et les afficher sur les lignes de l'état TVA.|
|Contenu | Contrôler le format de l'état. Par exemple, si c'est un fichier XML ou JSON. Le format à utiliser dépend des besoins du service Web de votre administration fiscale. |
|Soumission | Contrôler comment et quand vous envoyez l'état selon les besoins de votre administration fiscale. |
|Gestionnaire de réponse | Gérer le retour de l'administration fiscale. Par exemple, elle peut envoyer un message e-mail au contact de votre société. |
|Annuler | Envoyer une annulation d'un état de TVA qui a été envoyé précédemment à votre administration fiscale. |  

> [!Note]
> Lorsque vous créez des codeunits pour l'état, faites attention à la valeur du champ **Version de la déclaration TVA**. Ce champ doit refléter la version de l'état qui est ou a été requis par l'administration fiscale. Par exemple, vous pouvez saisir **2017** dans le champ pour indiquer que l'état remplit les conditions qui étaient en place cette année. Pour trouver la version en cours, contactez votre administration fiscale.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi
[Configuration des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Définition des ventes](sales-setup-sales.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  
