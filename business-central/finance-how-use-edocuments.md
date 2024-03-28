---
title: Utiliser des documents électroniques dans les ventes et achats
description: Découvrez comment utiliser la fonctionnalité de documents électroniques liée aux factures de vente et d’achat.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Utiliser des documents électroniques dans les ventes et achats

Vous pouvez utiliser des documents électroniques configurés (documents électroniques) avec les documents de vente et d’achat.

Vous pouvez utiliser les documents suivants avec la fonctionnalité des documents électroniques :  

- Ventes : 
    - Factures vente
    - Commandes vente
    - Avoirs vente
    - Factures service
    - Avoirs service
    - Factures d’intérêts
    - Relances
- Achats : 
    - Factures achat
    - Commandes achat (créer uniquement un document)
    - Avoirs achat
    - Feuilles comptabilité

> [!NOTE]
> Actuellement, une commande fournisseur ne peut être utilisée que lorsque vous créez le document à partir du document électronique de votre fournisseur. Cependant, vous ne pouvez pas mettre à jour le document existant avec les lignes que vous avez obtenues de votre fournisseur.  

## Documents électroniques vente

Pour créer et envoyer une facture électronique à un client, vous devez créer et valider la facture vente. Pour en savoir plus sur le processus standard, voir [Facture des ventes](sales-how-invoice-sales.md).

Après avoir validé le document vente, ouvrez la page **Facture vente validée** pour accéder à la page **Document électronique** associée.

### Afficher les documents électroniques

Pour afficher les documents électroniques existants, procédez comme suit.

1. Sur la page **Facture vente validée**, sélectionnez **Document électronique** \> **Ouvrir document électronique**.
2. Sur la page **Document électronique**, dans l’en-tête, vous pouvez afficher les informations de base sur la facture validée.
3. Le champ **Enregistrement** affiche le numéro de document de la facture vente validée. Sélectionnez le lien pour ouvrir le document.
4. Dans le champ **Statut du document électronique**, vous pouvez afficher le statut en temps réel du document et son emplacement dans le pipeline de processus. Si le document est validé, le statut est défini sur **Traité**.

### Journaux et statuts des documents électroniques

Pour plus de détails sur le niveau d’état de service de votre document électronique, consultez le récapitulatif **Statut du service du document électronique**. Sur les lignes, le système affiche un ou plusieurs services utilisés par le document. Dans le scénario le plus courant, chaque document utilise un seul service. Cependant, un document peut utiliser plusieurs services.

- Cochez la case **Code service document électronique** pour déterminer quel service a été utilisé.
- Cochez la case **Statut du document électronique** pour déterminer le statut de service actuel de ce document.
- Si vous souhaitez plus de détails, sélectionnez le champ **Journaux** pour le service sur la page **Journaux de documents électroniques**. Un aperçu chronologique des différents statuts du document est affiché.
- Vérifiez les champs **Numéro d’entrée** et **Création le** et d’autres informations sur la page **Journaux de documents électroniques**. Dans le champ **Statut du document électronique**, le premier statut est défini sur **Exporté**, ce qui indique que le fichier de document électronique a été créé. Le statut suivant est **Envoyé**, qui indique que le document a été envoyé au fournisseur de services, s’il est configuré.

Pour plus d’informations, sélectionnez l’entrée qui possède le statut **Exporté**, puis exécutez l’une des actions suivantes :

- **Ouvrir les journaux de mappage** : obtenez un aperçu de tous les champs exportés à partir des tables sourcées dans le champ **Valeur d’origine**. Si vous avez utilisé des règles de transformation lors du processus d’exportation, vous pouvez également obtenir la valeur finale dans le champ **Nouvelle valeur**.
- **Exporter le fichier** : exportez le fichier XML pour une révision manuelle.

Pour visualiser la communication entre vous et le service auquel vous envoyez votre document, utilisez le champ **Journaux de communications**. Ouvrez la page **Journaux de communication de documents électroniques** pour afficher les détails de la demande et le message de motifs avec ce service.

S’il y a un problème avec le fournisseur de services et que le document ne peut pas être envoyé, recherchez les indicateurs suivants sur la page **Document électronique** :

- Le champ **Statut du document électronique** sur l’en-tête montre le statut **Erreur**.
- Le champ **Statut du document électronique** sur le récapitulatif **Statut du service de document électronique** affiche le statut **Erreur d’envoi**.
- Le récapitulatif **Erreur et avertissements** contient un ou plusieurs messages indiquant la cause du problème.

Une fois le problème résolu, exécutez manuellement les actions **Envoyer le document**. Si vous avez besoin de différentes actions, telles que **Document recréé**, **Annuler le document**, ou **Obtenir l’approbation**, vous pouvez les exécuter.

## Documents électroniques achat

La réception des factures électroniques achat dans Dynamics 365 Business Central peut être effectuée par lots ou manuellement.

### Exécuter le traitement par lots

> [!NOTE]
> Ce traitement par lots est destiné à la collecte automatisée de vos factures entrantes. Cela ne peut fonctionner que dans un pays ou une région où la fonctionnalité existe.

Chaque fois qu’une file d’attente de tâches est exécutée, si le service externe reçoit des factures envoyées par votre fournisseur, le système collecte et importe ces factures. Pour terminer le processus, procédez comme suit.

1. Une fois le traitement par lots terminé, les factures récemment importées sont répertoriées dans la liste sur la page **Documents électroniques**, ainsi que leurs informations détaillées de base.
2. Pour afficher plus de détails, ouvrez un document électronique spécifique.
3. S’il n’y a eu aucune erreur ou problème dans le document électronique et dans son mappage, le champ **Enregistrement** affiche le numéro de document de la facture achat créée automatiquement par le système. Sélectionnez le lien pour ouvrir le document. Ce document créé par le système n’est pas le document validé.
4. Pour accéder directement au document achat, sélectionnez le champ **Enregistrement**. Après avoir ouvert la page **Facture achat**, vérifiez le document. Ensuite, si tout est correct, validez le document.
5. Lorsque vous validez le document d’achat, le champ **Enregistrement** du **document électronique** est mis à jour de **Facture** à **Facture achat** et le numéro du document achat validé est disponible. Vous pouvez sélectionner le numéro pour ouvrir la facture achat validée.

Les détails des journaux sont les mêmes que ceux du processus de vente des documents électroniques.

Étant donné que les erreurs dans le processus de vente sont principalement liées à la disponibilité du service, le document entrant peut contenir plusieurs raisons. La raison la plus courante d’une erreur est que le système ne peut pas reconnaître les lignes du document électronique que vous avez reçu de votre fournisseur. Il ne peut donc pas saisir de lignes dans votre facture achat.

Il existe deux erreurs courantes :

- Si vous souhaitez utiliser cette ligne spécifique de votre facture fournisseur qui a été directement imputée au compte du grand livre (G/L), vous devez avoir correctement configuré la valeur du **Texte de mappage**. Pour contourner cette erreur si vous souhaitez utiliser des comptes généraux, sélectionnez **Mapper le texte au compte** pour créer un mappage spécifique de la valeur **Texte de mappage** avec la valeur **N° cpte débit** que vous souhaitez utiliser.
- Si vous souhaitez suivre l’inventaire et utiliser les lignes de votre facture fournisseur pour renseigner les articles sur vos lignes de document, vous devez avoir correctement configuré le **N° référence article** . Pour contourner cette erreur, mappez l’élément externe avec vos numéros d’article à l’aide de la liste de référence d’article. Pour plus d’informations, voir [Utiliser les références article](inventory-how-use-item-cross-refs.md).

Après avoir corrigé les erreurs et les avertissements, vous pouvez spécifier manuellement quand le système doit créer une facture achat en fonction de votre configuration en sélectionnant **Créer un document**.

### Importer manuellement les factures

Pour importer manuellement des documents électroniques externes, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Service de document électronique**, puis sélectionnez le lien associé.
2. Sur la page **Service de document électronique** , sélectionnez le service actif. 
3. Sélectionnez **Recevoir** et téléchargez le fichier de document électronique que vous avez reçu du fournisseur.
4. Si un message d’erreur apparaît, ouvrez le document électronique pour résoudre les problèmes.
5. Lorsque vous avez fini de résoudre les problèmes, dans le groupe **Importer manuellement**, sélectionnez **Créer un document**.
6. Une fois le document créé dans Business Central, vous pouvez l’afficher comme si vous utilisiez un traitement par lots.

## Vue d’ensemble des statuts des documents électroniques

Pour obtenir un meilleur aperçu de tous les documents électroniques de l’entreprise, vous pouvez sélectionner le centre de rôles **Comptable** où existent les statuts des documents électroniques. Vous y trouverez des activités de documents électroniques qui ont les statuts suivants :

- **Documents électroniques sortants**

    - Traité
    - En cours
    - Erreur

- **Documents électroniques entrants :**

    - Traité
    - En cours
    - Erreur

## Voir aussi

[Comment configurer des documents électroniques dans Business Central](finance-how-setup-edocuments.md)  
[Comment étendre des documents électroniques dans Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestion financière](finance.md)  
[Facturation des ventes](sales-how-invoice-sales.md)  
[Enregistrer les achats avec les factures achat et les commandes](purchasing-how-record-purchases.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
