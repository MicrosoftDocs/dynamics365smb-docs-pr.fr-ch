---
title: Lignes achat récurrentes standard
description: Définissez des lignes achat que vous utilisez fréquemment pour les insérer dans des documents achat pour remplir rapidement les lignes avec des informations standard.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Créer des lignes achat récurrentes

Si vous devez souvent créer des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents achat, par exemple, pour les commandes de réapprovisionnement récurrentes.

## Configurer des lignes achat récurrentes

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Lignes achat récurrentes**, puis sélectionnez le lien associé.
2. Sur la page **Lignes achat récurrentes**, cliquez sur l’action **Nouveau**.
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Dans le raccourci **Lignes**, renseignez les champs qui répercutent les lignes standard que vous prévoyez d’utiliser comme lignes récurrentes sur les documents achat.

> [!NOTE]
> Vous ne pouvez pas définir des prix sur les lignes achat récurrentes, car les prix, les remises, etc. sont calculés sur les documents achat réels après avoir inséré les lignes achat récurrentes.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Affecter des lignes d’achat récurrentes à un fournisseur

Affectez une ou plusieurs lignes achat récurrentes à un fournisseur afin qu’elles soient disponibles pour être insérées sur les documents achat pour ce fournisseur.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche pour un fournisseur concerné.
3. Choisissez l’action **Lignes achat récurrentes**.
4. Sur la page **Lignes achat récurrentes**, sélectionnez les codes des lignes achat récurrentes que vous souhaitez pouvoir insérer sur les documents achat du fournisseur.
5. Renseignez les autres champs pour définir quand, comment et où les lignes achat récurrentes doivent être utilisées.
6. Dans les quatre champs où vous sélectionnez la façon dont les lignes sont insérées sur chaque type de document, sélectionnez l’une des options suivantes :

|Option|Désignation|
|------|-----------|
|**Manuel**|Vous devez rechercher et insérer manuellement une ligne achat récurrente existante pour le fournisseur.|
|**Automatique**|Si plusieurs lignes achat récurrentes existent pour le fournisseur, vous recevrez une notification pour vous permettre de sélectionner la ligne à insérer. Si une seule ligne achat récurrente existe, elle sera insérée automatiquement.<br /><br />Cela ne fonctionne que si le nouveau document a été créé à partir d’une liste de documents, par exemple en sélectionnant l’action **Nouveau** sur la page **Commandes achat**. Cela ne fonctionne pas si le document a été créé à partir d’une fiche fournisseur, par exemple.|
|**Toujours demander**|Une notification s’affiche et toutes les lignes achat récurrentes existantes sont affichées afin que vous puissiez en sélectionner une.

## Insérer des lignes achat récurrentes dans une facture achat

Si des lignes achat récurrentes existent pour le fournisseur, vous pouvez les insérer ou demander à les ajouter sur tous les types de documents achat, par exemple une facture achat. Si vous avez activé les options **Toujours demander** tout en affectant des lignes achat récurrentes aux fournisseurs, vous serez informé si des lignes achat récurrentes existent.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Ouvrez la facture achat que vous souhaitez pour insérer une ou plusieurs lignes achat standard.
3. Choisissez l’action **Extraire les lignes achat récurrentes**.
4. Sur la page **Lignes achat récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes achat standard.
5. Cliquez sur le bouton **OK** pour insérer les lignes achat standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.

## Voir aussi

[Achats](purchasing-manage-purchasing.md)  
[Configurer les procédures achat](purchasing-setup-purchasing.md)  
[Créer des factures vente](sales-how-work-standard-lines.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]