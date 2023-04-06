---
title: Envoyer les déclarations de TVA aux autorités fiscales
description: 'Apprendre à préparer les déclarations qui répertorient la TVA des ventes au cours d’une période, ou à partir des ventes et achats, et envoyer la déclaration à l’administration fiscale.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 01/31/2022
ms.author: bholtorf
---

# Déclarer la TVA aux autorités fiscales

Cette rubrique décrit les états dans [!INCLUDE[prod_short](includes/prod_short.md)] que vous pouvez utiliser pour envoyer des informations sur les montants de la taxe sur la valeur ajoutée (TVA) relatifs aux ventes et achats à l’administration fiscale de votre région. Selon le pays, les déclaration peuvent inclure des informations spécifiques ou vous devrez parfois soumettre des déclarations supplémentaires. Vérifiez les articles pour votre pays dans la section [Fonctionnalité locale](about-localization.md).  

Vous pouvez utiliser les déclarations intégrées suivantes :

* La déclaration**Liste des ventes UE**  

    La déclaration Liste des ventes de l’Union européenne (EU) répertorie les montants de la taxe sur la valeur ajoutée (TVA) que vous avez collectés pour les ventes aux clients enregistrés dans les pays de l’Union européenne (UE).  
* La déclaration **Retour TVA**  

    La déclaration Retour TVA inclut la TVA pour les ventes et les achats aux clients et auprès des fournisseurs dans tous les pays utilisant la TVA.  

Dans les deux cas (comme dans les états de TVA), la TVA est calculée sur la base des paramètres validation TVA et des groupes comptabilisation TVA que vous avez définis. [!INCLUDE[prod_short](includes/prod_short.md)] affiche les entrées de TVA toujours en fonction de leur **Date de TVA** comme date de déclaration principale.  

> [!NOTE]
> Tous les rapports liés à la TVA sont désormais exécutés à l’aide de **Date de TVA** pour filtrer les enregistrements pertinents. Même si vous configurez **Utilisation de la date de TVA** comme **Ne pas utiliser la fonctionnalité de date de TVA** [!INCLUDE[prod_short](includes/prod_short.md)] masquera toutes les instances de **Date de TVA** à travers l’application. Cependant, la **Date de TVA** est toujours utilisé dans tous les rapports et est automatiquement renseigné avec le **Date d’affichage**.

Si vous souhaitez afficher un historique complet des écritures TVA, chaque validation impliquant la TVA crée une écriture dans la page **Écritures TVA**. Ces écritures sont utilisées pour calculer le montant de votre déclaration TVA, tel que paiement et remboursement, pour une période donnée. Pour afficher les écritures de TVA, sélectionnez l’icône ![Ampoule qui ouvre la fonction Fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures TVA**, puis choisissez le lien associé.

> [!NOTE]
> Chaque environnement [!INCLUDE[prod_short](includes/prod_short.md)] est destiné à gérer les rapports réglementaires dans un seul pays. Par exemple, la version néerlandaise de [!INCLUDE[prod_short](includes/prod_short.md)] gère la déclaration de TVA aux Pays-Bas mais pas dans d’autres pays. De même, la version américaine de [!INCLUDE[prod_short](includes/prod_short.md)] gère la déclaration 1099 aux États-Unis et ne prend pas en charge la déclaration de TVA dans d’autres pays, sauf si elle est apportée par une extension fournie par notre écosystème partenaire ou une modification de code spécifique au client.

## <a name="ecsaleslist"></a>À propos de la déclaration Liste des ventes UE

Dans l’Union européenne (UE) et au Royaume-Uni, toutes les sociétés qui vendent des biens et des services aux clients enregistrés pour la TVA, y compris les clients dans d’autres pays de l’Union européenne (UE), doivent envoyer une version électronique de l’état Liste des ventes de la Communauté européenne (CE) à leurs administrations douanières et fiscales. L’état **Liste des ventes UE** ne fonctionne que pour les pays de l’UE.

La déclaration comprend une ligne pour chaque type de transaction avec le client, et affiche le montant total pour chaque type de transaction. La déclaration peut inclure trois types de transactions :  

* Marchandises B2B  
* Services B2B  
* Marchandises triangulées B2B  

Les biens et des services *B2B* indiquent si vous avez vendu un bien ou un service, et sont contrôlés par le paramètre **Service UE** des Paramètres comptabilisation TVA. Les *marchandises triangulées B2B* indiquent si vous vous êtes engagé dans des transactions avec un tiers, et sont contrôlées par le paramètre **Trans. tripartite UE** sur les documents vente, comme des commandes vente, des factures, des avoirs, etc.  

Une fois que l’administration fiscale aura examiné votre état, elle devra envoyer un e-mail au contact de votre société. Dans [!INCLUDE[prod_short](includes/prod_short.md)], le contact est spécifié sur la page **Informations société**. Avant de soumettre l’état, assurez-vous qu’un contact est sélectionné.  

### Soumettre une déclaration Liste des ventes UE

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="vatreturn"></a>À propos de la déclaration Retour TVA

Utilisez cet état pour envoyer les documents relatifs à la TVA sur les ventes et les achats, tels que les commandes d’achat et de vente, les factures et les avoirs. Les informations contenues dans l’état sont au même format que dans la déclaration de l’administration fiscale et douanière.  

Pour le retour TVA, vous pouvez spécifier les écritures pour :

* Envoyer les transactions ouvertes uniquement, ou ouvertes et clôturées. Par exemple, cela est utile lorsque vous préparez votre retour TVA annuel final.
* Envoyer uniquement les écritures des périodes définies, ou inclure également les écritures des périodes précédentes. Cette fonction est utile pour mettre à jour un retour TVA déjà envoyé, par exemple, si un fournisseur vous envoie une facture échue.    

## Pour vous connecter au service Web de votre administration fiscale
[!INCLUDE[prod_short](includes/prod_short.md)] fournit des connexions de service à des sites Web d’administrations fiscales. Par exemple, si vous vous trouvez au Royaume-uni, vous pouvez activer la connexion de service **GovTalk** pour envoyer la liste des ventes UE et les états de retour TVA par voie électronique. Si vous souhaitez envoyer l’état manuellement, par exemple en saisissant vos données sur le site Web de l’administration fiscale, cela n’est pas nécessaire.   

Pour déclarer la TVA à une administration par voie électronique, vous devez connecter [!INCLUDE[prod_short](includes/prod_short.md)] au service Web de l’administration fiscale. Cela suppose que vous configuriez un compte avec votre administration fiscale. Lorsque vous avez un compte, vous pouvez activer une connexion de service que nous fournissons dans [!INCLUDE[prod_short](includes/prod_short.md)].

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexions au service**, puis choisissez le lien approprié.
2. Renseignez les champs requis. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Il est judicieux de tester votre connexion. Pour cela, cochez la case **Mode Test**, puis préparez et envoyez votre déclaration de TVA comme décrit dans la section [Préparer et envoyer une déclaration de TVA](#to-prepare-and-submit-a-vat-report). En mode Test, le service vérifie si l’administration fiscale peut recevoir votre état, et le statut de l’état indiquera si l’envoi du test a réussi. Il est important de retenir que ce n’est pas un envoi réel. Pour réellement envoyer l’état, vous devez désactiver la case à cocher **Mode test**, puis répéter le processus d’envoi.

## Pour configurer les états TVA dans [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### Pour configurer des périodes retour de TVA

Facultativement, si votre entreprise n’est pas située au Royaume-Uni, utilisez la page **Périodes de retours de TVA** pour configurer les déclarations de TVA planifiées. Si votre entreprise est située au Royaume-Uni, consultez [Numériser les taxes au Royaume-Uni](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Périodes de retour de TVA**, puis choisissez le lien associé.  
2. Sur la page **Périodes de retour de TVA**, remplissez les champs pour paramétrer la première période. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Répétez l’étape 2 pour toutes les périodes supplémentaires que vous souhaitez ajouter.  

Désormais, lorsque le moment est venu de soumettre une déclaration de TVA pour une période de retour de TVA, choisissez la période sur la page **Périodes de retour de TVA**, puis choisissez l’action **Créer un retour VAR**. Puis, sur la fiche **Retour de TVA**, choisissez l’action **Suggérer des lignes** décrite à l’étape 3 de la procédure suivante.  

## Pour préparer et soumettre un état TVA

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Liste des ventes UE** ou **Retour TVA**, puis choisissez le lien associé.  
2. Sélectionnez **Nouveau**, puis renseignez les champs requis. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour générer le contenu de l’état, sélectionnez l’action **Proposer lignes**.  

    > [!NOTE]  
    >  Pour l’état Liste des ventes UE, vous pouvez consulter les transactions incluses dans les lignes de l’état avant d’envoyer l’état. Pour cela, sélectionnez la ligne, puis cliquez sur l’action **Afficher écritures TVA**.  

4. Pour valider et préparer l’état pour l’envoi, choisissez l’action **Emettre**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] confirme que l’état est configuré correctement. Si la validation échoue, les erreurs sont affichées sous **Erreurs et avertissements**, de sorte que vous sachiez quoi corriger. Généralement, si le message concerne un paramètre manquant dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez cliquer sur le message pour ouvrir la page contenant les informations à corriger.  
5. Pour envoyer l’état, sélectionnez l’action **Soumettre**.  

Une fois que vous envoyez la déclaration, [!INCLUDE[prod_short](includes/prod_short.md)] surveille le service et conserve un enregistrement de vos communications. Le champ **Statut** indique l’état de la déclaration en cours. Par exemple, lorsque l’administration traite votre déclaration, le statut de celle-ci passe à **Réussie**. Si l’administration fiscale trouve des erreurs dans la déclaration que vous avez envoyée, le statut de celle-ci est **Échec**. Vous pouvez afficher les erreurs sous **Erreurs et avertissements**, corrigez-les, puis envoyez la déclaration. Pour visualiser une liste de toutes vos déclarations de liste des ventes UE, consultez la page **États de liste des ventes UE**.  

### Statuts du retour TVA

Les retours TVA peuvent avoir différents statuts, comme décrit dans le tableau suivant.

| Statut | Description |
|------------|-------------------------|
| Ouvrir | Quand vous créez une déclaration de TVA. Vous pouvez exécuter l’action **Proposer lignes**. Si vous avez besoin de corriger des valeurs, vous pouvez réexécuter l’action **Suggérer des lignes**. Vous ne pouvez pas soumettre une déclaration de TVA qui a ce statut. |
| Lancé | Le statut sera modifié quand vous utiliserez l’action **Libérer**. [!INCLUDE[prod_short](includes/prod_short.md)] montrera le raccourci **Erreurs et avertissements**. Vous ne pouvez pas apporter de modifications ou utiliser l’action **Suggérer des lignes**. Pour apporter des modifications, vous devez rouvrir la déclaration de TVA. |
| Rejeté | Si votre soumission a échoué (par exemple, si l’authentification a échoué), le statut passera à **Rejeté**. Vous ne pouvez pas rouvrir un retour TVA avec ce statut. |
| Soumis | Le retour TVA est déposé à l’aide de l’action **Soumettre**, ou elle est marquée comme soumise à l’aide de l’action **Marquer comme soumis**. |
| Accepté | Le retour TVA a ce statut si le rapport est marqué comme accepté en utilisant l’action **Marquer comme accepté**. Si la déclaration **retour TVA** est marqué comme **Accepté**, vous pouvez exécuter l’action **Calculer et comptabiliser le règlement de la TVA**. |

## Affichage de l’historique des communications avec votre administration fiscale

Dans certains pays, vous échangez des messages avec l’administration fiscale lorsque vous envoyez des états. Vous pouvez afficher le premier et le dernier message que vous avez envoyés ou reçus en choisissant **Télécharger le message d’envoi** et les actions **Télécharger le message de réponse**.  

## Envoi manuel des états TVA
Si vous utilisez une autre méthode pour envoyer l’état, par exemple en exportant le XML et en le téléchargeant sur le site Web d’une administration fiscale, vous pouvez ensuite choisir **Marquer comme Soumis** pour clôturer la période de référence. Lorsque vous signalez un état comme lancé, vous ne pouvez plus le modifier. Si vous devez modifier l’état après l’avoir signalé comme lancé, vous devez le rouvrir.

## Déclaration de TVA
Périodiquement, vous devez régler la TVA nette aux autorités fiscales. Si vous devez effectuer des déclarations de TVA fréquemment, vous pouvez exécuter le traitement par lots **Calculer et valider décl. TVA** pour clôturer les écritures TVA ouvertes et transférer les montants TVA achat et vente dans le compte de déclaration TVA.

Lors du transfert des montants TVA vers le compte de déclaration, le compte TVA achat est crédité et le compte TVA vente est débité sur la base des montants calculés pour la période spécifiée. Le montant net est crédité ou débité, si le montant achat TVA est supérieur, sur le compte de déclaration TVA. Vous pouvez valider la déclaration immédiatement ou imprimer d’abord une impression test.  

> [!Note]
> Lorsque vous utilisez le traitement par lots **Calculer et valider décl. TVA**, si vous ne spécifiez pas **Groupe compta. marché TVA** ni **Groupe compta. produit TVA**, les écritures contenant les codes des groupes comptabilisation marché et des groupes comptabilisation produit sont incluses.

## Configuration de vos propres états de TVA

Vous pouvez utiliser l’état **Liste des ventes UE** prêt à l’emploi. Cependant, vous pouvez également créer vos propres rapports, si vous disposez d’une licence de développement afin de pouvoir créer des unités de code. Si vous avez besoin d’aide, contactez un partenaire certifié Microsoft.  

Le tableau suivant décrit les codeunits que vous devez créer pour votre état.  

| Codeunit | Ce qu’il doit effectuer |
|----|-----|
|Proposer lignes| Extraire les informations de la table **Écritures TVA**, et les afficher sur les lignes de la déclaration de TVA.|
|Contenu | Contrôler le format de l’état. Par exemple, si c’est un fichier XML ou JSON. Le format à utiliser dépend des besoins du service Web de votre administration fiscale. |
|Soumission | Contrôler comment et quand vous envoyez l’état selon les besoins de votre administration fiscale. |
|Gestionnaire de réponse | Gérer le retour de l’administration fiscale. Par exemple, elle peut envoyer un message e-mail au contact de votre société. |
|Annuler | Envoyer une annulation d’un état de TVA qui a été envoyé précédemment à votre administration fiscale. |  

> [!Note]
> Lorsque vous créez des codeunits pour la déclaration, faites attention à la valeur du champ **Version de la déclaration TVA**. Ce champ doit refléter la version de l’état qui est ou a été requis par l’administration fiscale. Par exemple, vous pouvez saisir **2021** dans le champ pour indiquer que l’état remplit les conditions qui étaient en place cette année. Pour trouver la version en cours, contactez votre administration fiscale.  

## Voir la [formation Microsoft](/training/paths/process-vat-dynamics-365-business-central/) associée

## Voir aussi

[Configurer des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Configuration des ventes](sales-setup-sales.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
