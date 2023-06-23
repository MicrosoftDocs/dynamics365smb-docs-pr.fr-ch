---
title: Détails de conception- Structure de la table | Microsoft Docs
description: 'Pour comprendre comment le stockage et la validation d’écriture de dimension sont conçus, il est important de comprendre la structure de tableau.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-table-structure" />Détails de conception : structure de la table
Pour comprendre comment les écritures analytiques sont stockées et validées, il est important de comprendre la structure de la table.  

## <a name="table-480-dimension-set-entry" />Table 480 : Écriture ensemble de dimensions
Vous ne pouvez pas modifier cette table. Une fois les données écrites dans la table, vous ne pouvez plus les supprimer ou les modifier.

|N° champ|Nom de champ|Type de données|Commentaire|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Entier|>0,0 est réservé à l’ensemble de dimensions vide. Champ de références 3 dans la table 481.|  
|2|**Code axe analytique**|Code 20|Relation de table avec la table 348.|  
|3|**Code section**|Code 20|Relation de table avec la table 349.|  
|4|**ID section analytique**|Entier|Champ de références 12 dans la table 349. Ce champ est la clé secondaire utilisée en parcourant la table 481.|  
|5|**Nom axe analytique**|Texte 30|CalcField. Rechercher dans la table 348.|  
|6|**Nom de la section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  

## <a name="table-481-dimension-set-tree-node" />Table 481 : Nœud d’arbre ensemble de dimensions
Vous ne pouvez pas modifier cette table. Elle est utilisée pour trouver un ensemble de dimensions. Si l’ensemble de dimensions est introuvable, un nouvel ensemble est créé.  

|N° champ|Nom du champ|Type de données|Commentaires|  
|---------------|----------------|---------------|-------------|  
|1|**ID ensemble de dimensions parent**|Entier|0 pour le nœud de niveau supérieur.|  
|2|**ID section analytique**|Entier|Relation de la table avec le champ 12 de la table 349.|  
|3|**ID ensemble de dimensions**|Entier|Incrémentez automatiquement. Utilisé dans le champ 1 du tableau 480.|  
|4|**Utilisé**|Booléen|Faux si non utilisé.|  

## <a name="table-482-reclas-dimension-set-buffer" />Table 482 : Tampon ensemble de dimensions reclass.
Cette table est utilisée lorsque vous modifiez un code section analytique, par exemple, pour une écriture comptable article en utilisant la page **Feuille reclassement article**.  

|N° champ|Nom de champ|Type de données|Commentaire|  
|---------------|----------------|---------------|-------------|  
|1|**Code axe analytique**|Code 20|Relation de table avec la table 348.|  
|2|**Code section**|Code 20|Relation de table avec la table 349.|  
|3|**ID section analytique**|Entier|Champ de références 12 dans la table 349.|  
|4|**Nouveau code section**|Code 20|Relation de table avec la table 349.|  
|5|**ID nouvelle section analytique**|Entier|Champ de références 12 dans la table 349.|  
|6|**Nom axe analytique**|Texte 30|CalcField. Rechercher dans la table 348.|  
|7|**Nom de la section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  
|8|**Nom nouvelle section analytique**|Texte 30|CalcField. Rechercher dans la table 349.|  

## <a name="transaction-and-budget-tables" />Transaction et tableaux de budget
En plus des autres champs d’axe dans la table, ce champ est important :  

|N° champ|Nom de champ|Type de données|Commentaire|  
|---------------|----------------|---------------|-------------|  
|480|**ID ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  

### <a name="table-83-item-journal-line" />Table 83 : Ligne feuille article
En plus des autres champs d’axe dans la table, ces champs sont importants :  

|N° champ|Nom de champ|Type de données|Commentaire|  
|---------------|----------------|---------------|-------------|  
|480|**ID ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  
|481|**ID du nouvel ensemble de dimensions**|Entier|Champ de références 1 dans la table 480.|  

### <a name="table-349-dimension-value" />Table 349 : section analytique
En plus des autres champs d’axe dans la table, ces champs sont importants :  

|N° champ|Nom de champ|Type de données|Commentaire|  
|---------------|----------------|---------------|-------------|  
|12|**ID section analytique**|Entier|Incrémentez automatiquement. Utilisé pour références dans le tableau 480 et le tableau 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field" />Tables qui contiennent le champ ID d’ensemble de dimensions
 Le champ **ID d’ensembles de dimensions** (480) existe dans les tables suivantes. Pour les tables qui stockent des données validées, le champ fournit seulement un affichage non modifiable des axes analytiques, marqué comme vue détaillée. Pour les tables qui stockent des documents de travail, le champ peut être modifié. Les tables tampon qui sont utilisées en interne n’ont pas besoin de fonctionnalités modifiables ou non modifiables.  

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
|304|**En-tête fact. d’intérêts émise**|  
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
|302|**En-tête facture d’intérêts**|  
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

Le champ 480 existe dans les tables suivantes.  

|Numéro table|Nom de la table|  
|---------------|----------------|  
|49|**Tampon valid. facture**|  
|212|**Tampon validation projet**|  
|372|**Tampon paiement**|  
|382|**Tampon écriture comptable CF**|  
|461|**Tampon ligne fact. acompte**|  
|5637|**Tampon écriture compta. immo.**|  
|7136|**Tampon budget article**|  

## <a name="see-also" />Voir aussi

[Aperçu des écritures de l’ensemble de dimensions](design-details-dimension-set-entries-overview.md)  
[Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md)   
