---
title: "Gérer les déclarations de TVA destinées aux autorités fiscales| Microsoft Docs"
description: "Apprendre à préparer une déclaration qui répertorie la TVA des ventes au cours d'une période, et envoyer la déclaration à l'administration fiscale."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Comment : Déclarer la TVA aux autorités fiscales
La déclaration de liste de vente de l'Union européenne (EU) répertorie les montants de sur taxe sur la valeur ajoutée (VAT) que vous avez recueillis pour les ventes au sein de l'Union européenne, de sorte que vous puissiez envoyer les montants de TVA au service Web d'une administration fiscale.

> [!NOTE]  
>   Au Royaume-Uni, toutes les sociétés qui vendent plus qu'une certaine valeur chaque exercice à des clients dans des états membres de l'Union européenne doivent envoyer une version électronique de leur déclaration de liste de vente de l'Union européenne au format XML sur le site Web du service de la fiscalité et des douanes du Royaume-Uni.

La liste des ventes de l'Union européenne ne fonctionne que pour les pays de l'UE. Par exemple, elle n'inclut pas la TVA sur les ventes aux pays comme la Chine ou les États-Unis.

Pour déclarer la TVA à une administration par voie électronique, vous devez connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] au service Web de l'administration fiscale. Cela suppose que vous configuriez un compte avec votre administration fiscale. Lorsque vous avez un compte, vous pouvez activer une connexion de service que nous fournissons dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, au Royaume-Uni vous pouvez utiliser la connexion de service **GovTalk**.

La déclaration comprend une ligne pour chaque type de transaction avec le client, et affiche le montant total pour chaque type de transaction. La déclaration peut inclure trois types de transactions :  
  
* Marchandises B2B  
* Services B2B  
* Marchandises triangulées B2B  
  
Les biens et des services B2B indiquent si vous avez vendu un bien ou un service, et sont contrôlés par le paramètre **Service UE** des paramètres validation TVA. Les marchandises triangulées B2B indiquent si vous vous êtes engagé dans des transactions avec un tiers, et sont contrôlées par le paramètre **Trans. tripartite UE** sur les documents vente, comme des commandes vente, des factures, des avoirs, etc.  
  
Une fois que vous envoyez la déclaration, [!INCLUDE[d365fin](includes/d365fin_md.md)] surveille le service et conserve un enregistrement de vos communications. Le champ **Statut** indique l'état de la déclaration en cours. Par exemple, lorsque l'administration traite votre déclaration, le statut de celle-ci passe à **Réussie**. Si l'administration fiscale trouve des erreurs dans la déclaration que vous avez envoyée, le statut de celle-ci est **Échec**. Vous pouvez afficher les erreurs sous **Erreurs et avertissements**, corrigez-les, puis envoyez la déclaration. Pour visualiser une liste de toutes vos déclarations de liste des ventes UE, consultez la page **États de liste des ventes UE**.  
  
> [!NOTE]  
>   Si vous utilisez une autre méthode pour envoyer l'état, par exemple en exportant le XML et en le téléchargeant sur le site Web d'une administration fiscale, vous pouvez ensuite choisir **Marquer comme Soumis** pour clôturer la période de référence. Lorsque vous signalez un état comme lancé, vous ne pouvez plus le modifier. Si vous devez modifier l'état après l'avoir signalé comme lancé, vous devez le rouvrir. 
  
Une fois que l'administration fiscale aura examiné votre état, elle devra envoyer un e-mail au contact de votre société. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le contact est spécifié sur la page **Informations société**. Avant de soumettre l'état, assurez-vous qu'un contact est sélectionné.

<!--> [!NOTE]  
>   L'état Liste des ventes UE peut contenir 1 000 lignes aux maximum. Si vous avez davantage de lignes, vous devez envoyer un autre état. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Pour vous connecter au service Web de votre administration fiscale
[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des connexions de service qui se connectent à des sites Web d'administrations fiscales. Par exemple, au Royaume-Uni, vous devez activer la connexion de service **GovTalk**.  

1. Dans le champ **Rechercher des pages ou des états**, entrez **Connexions au service**, puis sélectionnez le lien associé. <!-- remember to get the updated text for this-->  
2. Renseignez les champs requis.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Pour configurer l'état Liste des ventes UE
1. Dans le champ **Rechercher des pages ou des états**, entrez **Paramétrage déclaration TVA**, puis sélectionnez le lien associé.  
2. Si vous souhaitez laisser des utilisateurs modifier et retourner cet état, sélectionnez la case à cocher **Modifier les états soumis**.  
3. Spécifiez la souche de numéros à utiliser pour les états de liste des ventes UE.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Pour préparer et envoyer l'état Liste des ventes UE
1. Dans le champ **Rechercher des pages ou des états**, entrez **Liste des ventes UE**, puis sélectionnez le lien associé.  
2. Sélectionnez **Nouveau**, puis renseignez les champs requis.  
3. Pour générer le contenu de l'état, sélectionnez l'action **Proposer lignes**.  

    > [!NOTE]  
>   Vous pouvez consulter les transactions incluses dans la ligne avant d'envoyer l'état. Pour cela, sélectionnez la ligne, puis cliquez sur l'action **Afficher écritures TVA**.  
4. Pour préparer l'état pour la soumission, choisissez l'action **Emettre**.  
5. Pour envoyer l'état, sélectionnez l'action **Soumettre**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] confirme que l'état est configuré correctement. Si la validation échoue, les erreurs sont affichées sous **Erreurs et avertissements**, de sorte que vous puissiez apporter les modifications appropriées.

## <a name="viewing-communications-with-your-tax-authority"></a>Affichage de l’historique des communications avec votre administration fiscale
Dans certains pays, vous échangez des messages avec l'administration fiscale lorsque vous envoyez des états. Vous pouvez afficher le premier et le dernier message que vous avez envoyés ou reçus en choisissant **Télécharger le message d’envoi** et les actions **Télécharger le message de réponse**.  

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

> [!NOTE]  
>   Lorsque vous créez des codeunits pour l'état, faites attention à la valeur du champ **Version de la déclaration TVA**. Ce champ doit refléter la version de l'état qui est ou a été requis par l'administration fiscale. Par exemple, vous pouvez saisir **2017** dans le champ pour indiquer que l'état remplit les conditions qui étaient en place cette année. Pour trouver la version en cours, contactez votre administration fiscale.  

## <a name="see-also"></a>Voir aussi .
[Configuration de la TVA](finance-setup-vat.md)  
[Configuration des ventes](sales-setup-sales.md)  
[Procédure : facturer des ventes](sales-setup-sales.md)  

