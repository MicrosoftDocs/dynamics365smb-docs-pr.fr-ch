---
title: "Détails de conception- Structure de la table | Microsoft Docs"
description: "Pour comprendre comment le stockage et la validation d'écriture de dimension sont conçus, il est important de comprendre la structure de tableau."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 900605cd276698e3e6146d18e36ed18363b6c99c
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-table-structure"></a>Détails de conception : structure de la table
Pour comprendre comment le stockage et la validation d'écriture de dimension sont conçus, il est important de comprendre la structure de tableau.  

## <a name="new-tables"></a>Nouvelles tables  
 Trois nouveaux tableaux ont été conçus pour gérer les écritures d'ensemble de dimensions.  

### <a name="table-480-dimension-set-entry"></a>Table 480 : Écriture de l'ensemble de dimensions  
 La table 480 **Écriture de l'ensemble de dimensions** est une nouvelle table. Vous ne pouvez pas modifier cette table. Une fois les données écrites dans la table, vous ne pouvez plus les supprimer ou les modifier. La suppression de données requiert de vérifier toutes les occurrences de l'ID de l'ensemble de dimensions dans la totalité de la base de données, y compris des solutions partenaire.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Entier|>0,0 est réservé à l'ensemble de dimensions vide. Champ de références 3 dans la table 481.|  
|2|**Code axe analytique**|Code 20|Relation de table avec la table 348.|  
|3|**Code section**|Code 20|Relation de table avec la table 349.|  
|4|**ID section analytique**|Entier|Champ de références 12 dans la table 349. Ce champ est la clé secondaire utilisée en parcourant la table 481.|  
|5|**Nom axe analytique**|Texte 30|CalcField. Rechercher dans la table 348.|  
|6|**Nom de la section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  

#### <a name="table-481-dimension-set-tree-node"></a>Table 481 : Nœud d'arbre ensemble de dimensions  
 La table 481 **Nœud d'arbre ensemble de dimensions** est une nouvelle table. Vous ne pouvez pas modifier cette table. Elle est utilisée pour trouver un ensemble de dimensions. Si l'ensemble de dimensions est introuvable, un nouvel ensemble est créé.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|1|**ID ensemble de dimensions parent**|Entier|0 pour le nœud de niveau supérieur.|  
|2|**ID section analytique**|Entier|Relation de la table avec le champ 12 de la table 349.|  
|3|**ID ensemble de dimensions**|Entier|Incrémentez automatiquement. Utilisé dans le champ 1 du tableau 480.|  
|4|**Utilisé**|Booléen|Faux si non utilisé.|  

##### <a name="table-482-reclas-dimension-set-buffer"></a>Table 482 : Tampon ensemble de dimensions reclass.  
 La table 482 **Tampon ensemble de dimensions reclass.** est une nouvelle table. Le tableau est utilisé pour modifier un ID d'ensemble de dimensions. Il est nécessaire lorsque vous modifiez un code section analytique et un nouveau code section analytique, par exemple, dans la table **Feuille reclassement article**.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|1|**Code axe analytique**|Code 20|Relation de table avec la table 348.|  
|2|**Code section**|Code 20|Relation de table avec la table 349.|  
|3|**ID section analytique**|Entier|Champ de références 12 dans la table 349.|  
|4|**Nouveau code section**|Code 20|Relation de table avec la table 349.|  
|5|**ID nouvelle section analytique**|Entier|Champ de références 12 dans la table 349.|  
|6|**Nom axe analytique**|Texte 30|CalcField. Rechercher dans la table 348.|  
|7|**Nom de la section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  
|8|**Nom nouvelle section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  

## <a name="modified-tables"></a>Tables modifiées  
 Toutes les tables de transactions et de budget ont été modifiées pour gérer les écritures de l'ensemble de dimensions.  

### <a name="changes-to-transaction-and-budget-tables"></a>Modifications de la transaction et des Tableaux de budget  
 Un nouveau champ a été ajouté à toutes les tables de transactions et de budget.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|480|**ID ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  

#### <a name="changes-to-table-83-item-journal-line"></a>Modifications de la ligne feuille article de la table 83  
 Deux nouveaux champs ont été ajoutés au tableau 83 **Ligne feuille article**.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|480|**ID ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  
|481|**ID du nouvel ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  

##### <a name="changes-to-table-349-dimension-value"></a>Modifications de la section analytique de la table 349  
 Un nouveau champ a été ajouté à la table 349 **Section analytique**.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|12|**ID section analytique**|Entier|Incrémentez automatiquement. Utilisé pour références dans le tableau 480 et le tableau 481.|  

###### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Tables qui obtiennent l'ID d'ensemble de dimensions du nouveau champ 480  
 Un nouveau champ, 480, **ID ensemble de dimensions** a été ajouté aux tables suivantes. Pour les tables qui stockent des données validées, le champ fournit seulement un affichage non modifiable des axes analytiques, marqué comme vue détaillée. Pour les tables qui stockent des documents de travail, le champ peut être modifié. Les tables tampon qui sont utilisées en interne n'ont pas besoin de fonctionnalités modifiables ou non modifiables.  

 Le champ 480 ne peut pas être modifié dans les tables suivantes.  

|Numéro table|Nom de la table|  
|---------------|----------------|  
|17|**Écriture comptable**|  
|21|**Écriture comptable client**|  
|25|**Écriture comptable fournisseur**|  
|32|**Écriture comptable article**|  
|110|**En-tête expédition vente**|  
|111|**Ligne expédition vente**|  
|112|**En-tête facture vente**|  
|113|**Ligne facture vente**|  
|114|**En-tête avoir vente**|  
|115|**Ligne avoir vente**|  
|120|**En-tête réception achat**|  
|121|**Ligne réception achat**|  
|122|**En-tête facture achat**|  
|123|**Ligne facture achat**|  
|124|**En-tête avoir achat**|  
|125|**Ligne avoir achat**|  
|169|**Écriture comptable projet**|  
|203|**Écriture comptable ressource**|  
|271|**Écriture comptable compte bancaire**|  
|281|**Écriture comptable inventaire**|  
|297|**En-tête relance émise**|  
|304|**En-tête fact. d'intérêts émise**|  
|5 107|**Archives en-tête vente**|  
|5 108|**Archives ligne vente**|  
|5 109|**Archives en-tête achat**|  
|5 110|**Archives ligne achat**|  
|5 601|**Écriture comptable immobilisation**|  
|5 625|**Écriture comptable maintenance**|  
|5 629|**Écriture comptable couverture assurance**|  
|5 744|**En-tête expédition transfert**|  
|5 745|**Ligne expédition transfert**|  
|5 746|**En-tête réception transfert**|  
|5 747|**Ligne réception transfert**|  
|5 802|**Écriture valeur**|  
|5 832|**Écriture comptable capacité**|  
|5 907|**Écriture comptable service**|  
|5 908|**En-tête service**|  
|5 933|**Tampon valid. cde service**|  
|5 970|**En-tête contrat serv. archivé**|  
|5 990|**En-tête expédition service**|  
|5 991|**Ligne expédition service**|  
|5 992|**En-tête facture service**|  
|5 993|**Ligne facture service**|  
|5 994|**En-tête avoir service**|  
|5 995|**Ligne avoir service**|  
|6 650|**En-tête expédition retour**|  
|6 651|**Ligne expédition retour**|  
|6 660|**En-tête réception retour**|  
|6 661|**Ligne réception retour**|  

 Le champ 480 peut être modifié dans les tables suivantes.  

|Numéro table|Nom de la table|  
|---------------|----------------|  
|36|**En-tête vente**|  
|37|**Ligne vente**|  
|38|**En-tête achat**|  
|39|**Ligne achat**|  
|81|**Ligne feuille comptabilité**|  
|83|**Ligne feuille article**|  
|89|**Ligne feuille nomenclature**|  
|96|**Écriture budget**|  
|207|**Ligne feuille ressource**|  
|210|**Ligne feuille projet**|  
|221|**Ventilation feuille compta**|  
|246|**Ligne proposition achat**|  
|295|**En-tête relance**|  
|302|**En-tête facture d'intérêts**|  
|5 405|**Ordre de fabrication**|  
|5 406|**Ligne O.F.**|  
|5 407|**Composant O.F.**|  
|5 615|**Ventilation immo**|  
|5 621|**Ligne feuille immo.**|  
|5 635|**Ligne feuille assurance**|  
|5 740|**En-tête transfert**|  
|5 741|**Ligne transfert**|  
|5 900|**En-tête service**|  
|5 901|**Ligne article de service**|  
|5 902|**Ligne service**|  
|5 965|**En-tête contrat service**|  
|5 997|**Ligne service standard**|  
|7 134|**Écriture budget article**|  
|99 000 829|**Composant planning**|  

 Le champ 480 a été ajouté aux tables tampon suivantes.  

|Numéro table|Nom de la table|  
|---------------|----------------|  
|49|**Tampon valid. facture**|  
|212|**Tampon validation projet**|  
|372|**Tampon paiement**|  
|382|**Tampon écriture comptable CF**|  
|461|**Tampon ligne fact. acompte**|  
|5637|**Tampon écriture compta. immo.**|  
|7136|**Tampon budget article**|  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : écritures d'ensemble de dimensions](design-details-dimension-set-entries.md)   
 [Aperçu des écritures de l'ensemble de dimensions](design-details-dimension-set-entries-overview.md)   
 [Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md)   
 [Détails de conception : Codeunit 408 Gestion des axes analytiques](design-details-codeunit-408-dimension-management.md)   
 [Détails de conception : exemples de code de motifs modifiés dans les modifications](design-details-code-examples-of-changed-patterns-in-modifications.md)

