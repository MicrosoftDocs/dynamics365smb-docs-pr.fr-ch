---
title: Procédure pas à pas sur les contrats de service pour les articles de service
description: Cet article vous guide à travers différents scénarios impliquant des articles et des contrats de service.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Procédure pas à pas sur les contrats de service pour les articles de service

Cette procédure détaillée illustre plusieurs processus principaux :

- Création d’articles de service via les ventes
- Création et facturation d’un contrat de service
- Création d’une commande service pour un contrat de service
- Affecter une ressource en fonction de la compétence et de la zone
- Terminer la saisie de temps pour la commande service
- Valider et facturer la commande service du contrat

## <a name="creation-of-service-items"></a>Création d’articles de service

### <a name="scenario"></a>Scénario

Susan, la préparatrice de commandes, valide une commande client en vendant un article configuré pour générer un article de service.  

### <a name="steps"></a>Étapes

1. Vérifiez que l’**Article** a **Groupe articles de service** sélectionné.
   
    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis choisissez le lien associé.  
    2. Sélectionnez l’article *S-100* et ouvrez-le.
    3. Vérifiez la valeur dans le champ **Groupe articles service**.
       
2. Validez la **Commande client** pour créer l’article de service pour le client.  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.  
    2. Sélectionnez la commande pour le client 10000. Le N° de commandes externes est *SVC-1*.
    3. Choisissez l’action **Valider** pour expédier l’article au client.

### <a name="results"></a>Résultats

- Un article de service est créé pour le client 10000

## <a name="invoicing-a-service-contract"></a>Facturation d’un contrat de service

### <a name="scenario-1"></a>Scénario

Charles, le responsable de service, crée ensuite un contrat de service pour facturer les visites de maintenance normales.

3. Créer le **Contrat de service** pour le nouvel article de service
    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Contrats de service**, puis sélectionnez le lien associé.
    2. Sélectionnez l’action **Nouveau**.  
    3. Dans la boîte de dialogue de confirmation, choisissez **Oui** pour créer un contrat à l’aide d’un modèle. 
    4. Sélectionnez *Contrat non prépayé – Mensuel*.
    5. Dans le récapitulatif Service, dans le champ **Type commande service**, saisissez **MAINTEN**.
    6. Dans les lignes, entrez les informations suivantes :

    |N° article de service|Valeur ligne|  
    |----------------|----------|  
    |SV000001|6000|

    7. Choisissez l’action **Signer le contrat** et confirmez la signature.
    8. Choisissez **Oui** pour confirmer la création d’une facture de service. Vous recevrez un message de confirmation avec le numéro de facture service.

3. Valider la facture service
   1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures service**, puis sélectionnez le lien associé.
   2. Localisez la facture service et choisissez l’action **Valider**.

### <a name="results-1"></a>Résultats

- Un contrat de service signé est créé, avec des écritures comptables
- Une facture service validée est créée

## <a name="creating-a-service-order-for-a-service-contract-and-assign-resources"></a>Création d’une commande service pour un contrat de service et affectation de ressources

### <a name="scenario-2"></a>Scénario

Charles, le responsable de service, crée les commandes service pour les ordres de maintenance normaux dans le cadre du contrat de service, puis examine le tableau d’affectation pour les affecter.

### <a name="steps-1"></a>Étapes

1. Exécutez les commandes service qui respectent les obligations des contrats de service actifs.
   1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Créer des commandes de service de contrat**, puis sélectionnez le lien associé.
   2. Entrez les dates de début et de fin du mois dans les champs Date de début et Date de fin du raccourci Options
   3. Choisissez **OK** pour confirmer la création des commandes service. Vous recevrez un message de confirmation avec le numéro des commandes service créées.

2. Examiner les commandes en attente d’affectation via le tableau d’affectation
   1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Tableau d’affectation**, puis sélectionnez le lien associé.
   2. Le tableau d’affectation affiche toutes les commandes service ouvertes, ainsi que le **Nbre affectations** pour indiquer si les commandes service ont été affectées à une ressource.
   3. Choisissez l’action **Afficher documents** pour ouvrir une commande service.  Vous verrez que le raccourci Lignes articles de service indique quelles ressources sont compétentes pour travailler avec cet article.

3. Affecter une ressource à la commande service
   1. À partir de la commande service, choisissez l’action de ligne **Affectations ressources**
   2. Saisissez les informations suivantes pour l’affectation de ressources

    |N° article de service|N° ressource|Date affectation|Heures affectées|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|a|0|

    3. Le statut de l’affectation passe à Actif.
    4. L’actualisation du tableau d’affectation affiche le **Nbre d’affectations** qui est passé de 0 à 1 pour la commande service.

### <a name="results-2"></a>Résultats

- Les commandes service sont créées pour les contrats de service
- Les commandes service sont affectées à une ressource pour terminer le travail

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Terminer la saisie de temps pour la commande service et enregistrer la commande service

### <a name="scenario-3"></a>Scénario

Le technicien de service enregistre son temps directement dans la commande service, puis marque la commande comme terminée.

> [!NOTE]
> La saisie de temps pour les commandes service peut être effectuée via les feuilles de temps. Pour plus d’informations, voir [lien vers la feuille de temps si cette note a du sens].

### <a name="steps-2"></a>Étapes

1. Localiser la commande service et saisir le temps dans la ligne service
   1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Commandes service**, puis choisissez le lien associé.
   2. Localisez la commande service pour laquelle vous souhaitez saisir le temps.
   3. Choisissez l’action de ligne **Ligne service**.
   4. Entrez les informations suivantes

    |Type|N°|Quantité|Qté à consommer|
    |----|---|--------|--------|   
    |Ressource|RESOURCE1|2|2|

2. Dans la commande service, validez la consommation
   1. Choisissez l’action **Valider** pour terminer la commande service, sélectionnez l’action **Expédier et consommer**, puis choisissez le bouton **OK**.

### <a name="results-3"></a>Résultats

- Des écritures comptables service sont créées et associées à l’article de service, au contrat de service et à la ressource

## <a name="see-also"></a>Voir aussi
