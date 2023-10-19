---
title: Procédure pas à pas sur les projets de base
description: Cet article vous guide à travers plusieurs processus principaux dans la gestion des projets.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---
# <a name="walkthrough-of-basic-jobs"></a>Procédure pas à pas sur les projets de base

Cette procédure détaillée illustre plusieurs processus principaux :

- Ajout de tâches aux projets
- Enregistrement du temps et des dépenses de matériel pour un projet
- Facturation d’un projet

## <a name="adding-a-job-task-to-a-job"></a>Ajout d’une tâche à un projet

### <a name="scenario"></a>Scénario

Simon, le chef de projet, souhaite enregistrer le temps consacré à former le client sur l’utilisation d’une machine expresso dans une tâche distincte du projet d’installation d’une machine commerciale sur site.

### <a name="steps"></a>Étapes

1. Créer la tâche de projet  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis choisissez le lien associé.  
    2. Sélectionnez le projet *J00010*.
    3. Dans la zone **Tâches**, choisissez l’action **Nouvelle ligne**.  Saisissez les valeurs suivantes :
 
    |N° tâche projet|Désignation|Type tâche projet|
    |------------|-----------|-------------|  
    |220|Formation du client|Validation|

2. Indenter les tâches de projet
   1. Dans la zone Tâches, localisez l’action **Indenter tâches projet**
   2. Confirmez que vous souhaitez indenter les tâches en sélectionnant **Oui**.

### <a name="results"></a>Résultats

 - Maintenant, le temps et les dépenses peuvent être enregistrés dans la nouvelle tâche de projet

## <a name="record-time-and-material-expenses-to-a-job"></a>Enregistrer le temps et les dépenses de matériel pour un projet

### <a name="scenario-1"></a>Scénario

Edgin, le technicien qui installe la machine, doit enregistrer son temps et les matériels utilisés lors de l’installation dans le projet pour la facturation.  Il a déjà ajouté les déplacements et les matériels, et doit maintenant ajouter le temps pour apprendre au personnel comment utiliser la machine.

### <a name="steps-1"></a>Étapes

1. Créer des lignes feuille projet supplémentaires

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles projet**, puis choisissez le lien associé.  
    2. Sélectionnez le lot *CONTOSO*.  Vous verrez plusieurs lignes de type Ressource et Article, qui reflètent le temps (pour le technicien et le véhicule) et les matériels (la machine et les fournitures) utilisés.
    3. Créez une ligne. Saisissez les valeurs suivantes :
 
    |N° projet|N° tâche projet|Type|N°|Désignation|Quantité|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressource|EDGIN|Formation du client|0|

2. Valider le temps et les dépenses
   1. Choisissez l’action **Valider**
   2. Confirmez que vous souhaitez valider les lignes en sélectionnant **Oui**.

### <a name="results-1"></a>Résultats

 - Des écritures comptables projet et des écritures comptables ressource de type *Utilisation* sont créées
 - Des écritures comptables article sont créées pour ajuster négativement l’inventaire
 - Sur la fiche projet, les coûts et les prix dans la zone Tâches reflètent les nouveaux soldes en attente de facturation
 - Sur la fiche projet, le récaptitulatif Détails du projet reflète les totaux des prix

## <a name="creating-a-sales-invoice-for-a-job"></a>Création d’une facture vente pour un projet

### <a name="scenario-2"></a>Scénario
Simon doit créer et valider une facture à envoyer au client avec le temps et les dépenses du projet.

### <a name="steps-2"></a>Étapes
1. Créer la facture vente

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis choisissez le lien associé.  
    2. Dans la liste des projets, choisissez l’action **Créer une facture vente projet**.
    3. Définissez le filtre **N° projet** sur *J00010*.
    4. Choisissez **OK** pour générer la facture vente.  Vous recevrez une confirmation du nombre de factures générées

2. Valider la facture du temps et des dépenses
   1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures vente**, puis sélectionnez le lien associé.  
   2. Sélectionnez la dernière facture pour l’ouvrir pour révision.
   3. Sélectionnez l’action **Valider**.

### <a name="results-2"></a>Résultats

 - Des écritures comptables projet et des écritures comptables ressource de type *Vente* sont créées
 - Sur la fiche projet, les coûts et les prix dans la zone Tâches reflètent les nouveaux soldes facturés
 - Sur la fiche projet, le récaptitulatif Détails du projet reflète les totaux des prix dans la section Prix facturé
