---
title: Définition et répartition des coûts
description: 'Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d’affectations que nécessaire.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Définition et répartition des coûts

Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d’affectations que nécessaire. Chaque affectation comporte les éléments suivants :  

- Une source affectation.  
- Une ou plusieurs cibles d’affectation.  

La source d’affectation détermine les coûts à affecter, tandis que les cibles d’affectation déterminent l’emplacement des coûts à affecter. Par exemple, les coûts pour le type de coût Fournitures non stockables représentent une source de ventilation. Vous affectez tous les coûts de fournitures non stockables à trois centres de coûts : Atelier, Production, et Vente. Ces centres de coûts sont les cibles d’affectation.  

Pour chaque source d’affectation, vous définissez un niveau d’affectation, une période de validité et une variante comme identifiant de regroupement. Vous pouvez utiliser un traitement par lots pour définir des filtres afin de sélectionner les définitions d’affectation, puis exécuter les affectations des coûts automatiquement.  

Pour chaque cible d’affectation, vous définissez une base de ventilation. La base de ventilation peut être statique ou dynamique.  

- Les bases de ventilation statique dépendent d’une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.  
- Les bases de ventilation dynamique dépendent de valeurs variables, telles que le nombre de salariés dans un centre de coût ou les revenus de vente d’un coût associé pour une période donnée.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

## Configuration de la source et des cibles d’affectation

Chaque affectation comporte une source et au moins une cible. La source d’affectation définit les coûts à affecter. Les cibles d’affectation déterminent où affecter ces coûts.  

### Pour configurer les affectations de coûts

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectation des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l’action **Modifier**.  
3. Dans le champ **ID**, entrez un ID pour la source d’affectation.  
4. Définissez un niveau compris entre les chiffres 1 et 99 dans le champ **Niveau**. La validation d’affectation suit l’ordre des niveaux.  
5. Entrez un type de coût pour définir les types de coût à affecter dans le champ **Plage type de coûts**. Si tous les coûts pour un type donné sont affectés, aucune plage n’est définie.  
6. Entrez un centre de coûts avec des coûts à affecter dans le champ **Code centre de coûts**.  
7. Entrez un coût associé avec des coûts à affecter dans le champ **Code coûts associés**. Ce champ reste vide la plupart du temps car les coûts associés sont rarement affectés à d’autres coûts associés.  
8. Entrez un type de coût dans le champ **Type de crédit/coût**. Les coûts affectés sont crédités dans le type de coût d’origine. La validation des crédits est validée sur le type de coût spécifié ici.  
9. Sur le raccourci **Lignes**, définissez les cibles d’affectation. Sur la première ligne, entrez un type de coût dans le champ **Type coût cible**. Il définit le type de coût à partir duquel l’affectation est débitée.  
10. Sur la première ligne, saisissez la première cible d’affectation dans le champ **Centre de coûts cible** ou **Objet de coûts cible**. Ces deux champs définissent le centre de coûts ou les coût associés à partir desquels l’affectation est débitée. Vous pouvez renseigner uniquement l’un de ces champs, mais pas les deux.  
11. Répétez les mêmes étapes sur la deuxième ligne pour configurer les cibles d’affectation supplémentaires.  
12. Après avoir paramétré la cible et les sources d’affectation, sélectionnez **Calculer la clé de ventilation** pour calculer le total des valeurs de part.  

> [!NOTE]  
> Cochez la case **Bloqué** pour désactiver la configuration de l’affectation.

## Définition de filtres pour les bases de ventilation dynamique

Le mode de ventilation dynamique dépend des valeurs modifiables. Par exemple, le nombre de salariés dans un centre de coûts ou le nombre d’articles vendus d’un coût associé pour une période donnée. Il existe neuf bases de ventilation prédéfinies et douze plages de dates dynamiques. Vous définissez plusieurs filtres en fonction de la base de ventilation.  

### Définition des filtres

Le tableau suivant affiche les filtres applicables aux diverses bases de ventilation et les valeurs valides dans les champs **Filtre n°** et **Filtre groupe**. Sélectionnez <kbd>F1</kbd> dans le champ **Code filtre date** pour lire les descriptions détaillées.  

|**Base**|**Filtre n°**|**Code filtre date**|**Filtre centre de coûts**|**Filtre coûts associés**|**Filtre groupe**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Écritures comptables|Compte général|Oui|Oui|Oui|N/A|  
|Écritures budget|Compte général|Oui|Oui|Oui|Nom budget comptable|  
|Écritures du type de coût|Type coût|Oui|Oui|Oui|N/A|  
|Écritures budget des coûts|Type coût|Oui|Oui|Oui|Nom du budget|  
|Nombre de salariés|N/A|Oui|Oui|Oui|N/A|  
|Articles vendus (qté)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles achetés (qté)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles vendus (montant)|N° article|Oui|Oui|Oui|Groupe compta. stock|  
|Articles achetés (montant)|Nombre d’articles|Oui|Oui|Oui|Groupe compta. stock|

## Scénario 1 : Définition des ventilations statiques en fonction du ratio d’affectation

Le mode de ventilation statique dépend d’une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.  

Cette rubrique décrit comment définir trois nouveaux coûts associés pour la cibles d’affectation pour le centre de coûts PROD de la source d’affectation à l’aide d’un ratio de ventilation prédéfini, comme 5:2:4. Les trois coûts associés cibles sont ACCESSO, PEINTURE et ACCESSOIRES.  

> [!NOTE]  
> L’exemple utilise les données de démonstration dans [!INCLUDE[prod_short](includes/prod_short.md)].  

### Pour définir le centre de coûts PROD de la source d’affectation sur le raccourci Général  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectation des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l’action **Nouveau**.  
3. Dans le champ **ID**, sélectionnez <kbd>Entrée</kbd> ou entrez un ID.  
4. Dans le champ **Niveau**, saisissez **1**.  
5. Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6. Dans le champ **Code centre de coûts**, entrez **PROD**.  
7. Dans le champ **Type de crédit/coût**, entrez le type de coût **9903**.  

### Pour définir les coûts associés de la cible d’affectation sur le raccourci Lignes  

1. Sur la première ligne facture, dans le champ **Type coût cible**, saisissez **9903**.  
2. Sur la première ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSO**.  
3. Sur la première ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d’affectation de tous les coûts cumulés.  
4. Sur la première ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
5. Sur la première ligne, dans le champ **Part**, saisissez le ratio d’affectation **5**.  
6. Sur la deuxième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
7. Sur la deuxième ligne, dans le champ **Coûts associés cibles**, saisissez **PEINTURE**.  
8. Sur la deuxième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d’affectation de tous les coûts cumulés.  
9. Sur la deuxième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
10. Sur la deuxième ligne, dans le champ **Part**, saisissez le ratio d’affectation **2**.  
11. Sur la troisième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
12. Sur la troisième ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSOIRES**.  
13. Sur la troisième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d’affectation de tous les coûts cumulés.  
14. Sur la troisième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
15. Sur la troisième ligne, dans le champ **Part**, saisissez le ratio d’affectation **4**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement le champ **Pour cent** à l’aide d’un pourcentage qui dépend de ces trois ratios d’affectation saisis dans le champ **Part** pour chacune des trois lignes.

## Scénario 2 : Définition des ventilations dynamique sur la base des articles vendus

Cette rubrique explique comment définir les affectations à l’aide du mode de ventilation dynamique. Dans l’exemple, vous modifiez la ventilation dynamique des coûts pour que le centre de coûts VENTES prenne en charge le nouveau ÉQUIPEMENT IT de coûts associés. Les packages ÉQUIPEMENT IT ont des numéros d’articles dont la plage s’échelonne entre 8904-W et 8924-W. Vous pouvez utiliser les chiffres de ventes de l’exercice précédent pour en calculer la part. La ventilation est validée en fonction du type de coût 9903.  

> [!NOTE]  
> L’exemple utilise les données de démonstration dans [!INCLUDE[prod_short](includes/prod_short.md)].  

### Pour définir les ventilations dynamique en fonction des articles vendus de l’exercice précédent  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectation des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l’action **Nouveau**.  
3. Dans le champ **ID**, sélectionnez <kbd>Entrée</kbd> ou entrez un ID.  
4. Dans le champ **Niveau**, saisissez **1**.  
5. Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6. Dans le champ **Code centre de coûts**, entrez **VENTES**.  
7. Dans le champ **Type de crédit/coût**, entrez le type de coût **9903**.  
8. Dans le champ **Type coût cible**, entrez le type de coût **9903**.  
9. Dans le champ **Objet de coûts cible**, sélectionnez **Nouveau** pour créer un nouvel objet de coût ÉQUIPEMENT IT et renseigner les champs, le cas échéant. Sélectionnez **ÉQUIPEMENT IT**. Laissez le champ **Centre de coûts cible** vide.  
10. Dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d’affectation de tous les coûts cumulés.  
11. Dans le champ **Base**, sélectionnez la base de ventilation **Articles vendus (Montant)**.  
12. Dans le champ **Filtre n°**, entrez **8904-W..8924-W**.  
13. Dans le champ **Code filtre date**, entrez **Année précédente**.  
14. Choisissez l’action **Calculer la clé de ventilation** pour calculer la part.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] utilise les chiffres de ventes des exercices précédents pour calculer une part de 1596,50 DS avec 100 % alloués pour les packages ÉQUIPEMENT IT. Cela signifie que tous les articles vendus au cours de l’exercice précédent seront affectés au ÉQUIPEMENT IT des coûts associés.

## Voir la [formation Microsoft](/training/modules/allocate-costs-dynamics-365-business-central/) associée

## Voir aussi

 [Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)  
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)  
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
 [Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)  
 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
