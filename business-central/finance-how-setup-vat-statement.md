---
title: Configurer une déclaration de TVA
description: Cette rubrique vous explique comment configurer un modèle de déclaration de TVA et des noms de déclaration de TVA pour répondre aux exigences en pleine évolution de l’administration fiscale.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a><a name="set-up-vat-statement-templates-and-vat-statement-names"></a>Paramétrer des modèles de déclaration de TVA et des noms de déclaration de TVA

Les autorités fiscales peuvent modifier et modifient leurs exigences de validation de la TVA. Les modèles de déclaration de TVA et les noms de déclaration de TVA peuvent vous aider à vous préparer aux changements à venir et à vous conformer en douceur aux nouvelles exigences. Vous pouvez utiliser des modèles de déclaration de TVA pour configurer différents rapports lorsque vous choisissez d’imprimer la déclaration. Chaque modèle de déclaration de TVA peut avoir plusieurs noms de déclaration de TVA qui, en retour, définissent les calculs, et vous pouvez créer un nouveau nom de déclaration de TVA lorsque les exigences changent. Par exemple, un nom peut calculer la TVA pour cette année en fonction des exigences actuelles, et un autre modèle peut calculer la TVA en fonction des exigences de l’année suivante. Les noms permettent également de conserver un historique des formats de déclaration de TVA, par exemple pour vous permettre de déterminer comment la TVA a été calculée dans les années précédentes.

## <a name="to-define-a-vat-statement"></a><a name="to-define-a-vat-statement"></a>Pour définir une déclaration de TVA

Les déclarations de TVA vous permettent de calculer le montant de la déclaration de TVA pour une période donnée, par exemple, un trimestre.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Déclarations TVA**, puis choisissez le lien associé.  
2. Choisissez le champ **Nom**, puis choisissez **Nouveau** dans la page **Noms déclarations TVA**.
3. Renseignez les champs requis. Généralement, vous souhaitez avoir un paramètre pour chaque association Groupe compta. marché TVA/Groupe compta. produit TVA. Pour les numéros de ligne, il est logique d’utiliser des numéros ou des codes équivalents comme dans votre déclaration TVA officielle [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Vous pouvez filtrer les informations de la déclaration, selon votre sélection dans le champ **Type**. L’option **Totalisation comptes** est utile lorsque vous souhaitez calculer la TVA à partir d’un compte spécifique.
L’option **TVA** permet d’obtenir la TVA pour les comptes affectés aux sélections dans les champs **Type compta. TVA**, **Groupe compta. marché TVA** et/ou **Groupe compta. produit TVA**. L’option **Total de lignes** permet de saisir une valeur ou des critères de filtre rapide dans le champ **Total de lignes**. Pour plus d’informations, voir [Recherche, filtrage et tri des données](ui-enter-criteria-filters.md). L’option **Description** est souvent utilisée pour ajouter une note à la déclaration. Par exemple, vous pouvez l’utiliser comme en-tête si vous avez utilisé Total de lignes.

## <a name="to-preview-the-vat-statement"></a><a name="to-preview-the-vat-statement"></a>Afficher la déclaration de TVA

Après avoir défini une déclaration de TVA, vous pouvez en afficher un aperçu pour vérifier qu’elle répond à vos besoins.
> [!Tip]
> Il est préférable d’avoir une section de la déclaration TVA en utilisant **Type** **TVA** et une autre section ci-dessous en utilisant **Type** **Totalisation comptes** pour rapprocher les montants en fonction de la table **TVA** par rapport au montant des **Comptes généraux**. Vous pouvez également utiliser le rapport **CPT - Rapprochement TVA** à cet effet.

1. Choisissez **Aperçu**.
2. Entrez un filtre de date pour limiter la déclaration à une période spécifique. Pour plus d’informations sur la personnalisation de la page pour afficher le filtre de date, voir [Recherche, filtrage et tri des données](ui-enter-criteria-filters.md).
3. Vous pouvez sélectionner diverses options pour indiquer le type des écritures TVA à inclure dans la déclaration.
4. Sur les lignes où le champ **Type** indique la valeur **TVA**, vous pouvez afficher la liste des écritures TVA en choisissant le montant figurant dans le champ **Montant colonne**.
5. Vous pouvez utiliser la personnalisation pour afficher plus de champs dans les lignes. Par exemple, le montant de base sur encaissement prévu et le montant de TVA sur encaissement prévu, si vous utilisez la TVA sur encaissement.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/process-vat-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Configuration de la TVA](finance-setup-vat.md)  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)  
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
