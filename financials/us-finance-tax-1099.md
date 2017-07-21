---
title: "Report de transactions 1099 aux États-Unis | Microsoft Docs"
description: "L'IRS requiert le formulaire de déclaration d'honoraires 1099 pour les paiements aux fournisseurs et vous pouvez spécifier un document achat est soumis à la 1099 et indiquer le code 1099 du fournisseur."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a>Génération d'états de transactions soumis à la 1099 aux États-Unis

L'Internal Revenue Service (IRS) requiert une ou plusieurs versions du formulaire de déclaration d'honoraires 1099 pour les paiements aux fournisseurs. Les copies de ces formulaires doivent être adressées aux fournisseurs annuellement avant le dernier jour de janvier. Sur les documents achat, vous pouvez spécifier que le document est soumis à la 1099, et vous pouvez spécifier le code 1099 pour le fournisseur.  

## <a name="1099-codes"></a>Codes 1099
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les codes 1099 les plus courants sont déjà définis, ainsi vous êtes prêt à générer des états obligatoires. Les codes sont définis dans la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099** dans laquelle vous pouvez également ajouter de nouveaux codes 1099. Pour chaque fournisseur soumis à recouvrement, vous pouvez spécifier le code 1099 approprié dans le raccourci **Paiements** sur la fiche Fournisseur.  

L'état **Fournisseur 1099 Information** vous permet d'examiner les transactions 1099 payées au cours d'une période donnée. À la fin de l'exercice, vous pouvez imprimer les transactions 1099 sur les formulaires pré-imprimés.  

## <a name="printing-1099-tax-forms"></a>Impression des formulaires de déclaration d'honoraires 1099
Dans la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099**, vous pouvez accéder aux formulaires de déclaration d'honoraires suivantes :  

* Fournisseur 1099 Div  

  Imprime le formulaire fédéral 1099-DIV pour les dividendes et la distribution. Vous pouvez imprimer l'ensemble des formulaires 1099-DIV ou ceux spécifiques. L'état utilise les codes qui s'appliquent aux zones d'honoraires du formulaire DIV de la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099**.  
* Fournisseur 1099 Int  

  Imprime le formulaire fédéral 1099-INT pour les produits financiers. Vous pouvez imprimer l'ensemble des formulaires 1099-INT ou ceux spécifiques. L'état utilise les codes qui s'appliquent aux zones d'honoraires du formulaire INT de la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099**.  
* Fournisseur 1099 Div - Revenus divers  

  Imprime le formulaire fédéral 1099-MISC pour les revenus divers. Vous pouvez imprimer l'ensemble des formulaires 1099-MISC ou ceux spécifiques. L'état utilise les codes qui s'appliquent aux zones d'honoraires du formulaire MISC de la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099**.  

Les modifications réglementaires affectant cet état et les données de la table sont généralement gérés lors de mises à jour de fin d'exercice.
Il peut être utile d'exécuter l'état **Fournisseur 1099 Information** pour vérifier les données avant l'impression sur les formulaires.

## <a name="submitting-1099-tax-forms-electronically"></a>Soumission électronique des formulaires de déclaration d'honoraires 1099
Pour envoyer des formulaires de déclaration d'honoraires 1099 par voie électronique, utilisez l'état **Fournisseur 1099 Support magnétique**. Spécifie les formulaires 1099 qui peuvent être exportés. Les informations de formulaire exportées par cet état sont les mêmes que les états qui impriment les formulaires 1099 décrits dans la section précédente.  

L'état utilise les codes qui s'appliquent aux zones d'honoraires du formulaire de la fenêtre **Formulaire de déclaration d'honoraires de l'administration fiscale 1099**. Les codes sont mappés aux zones d'honoraires dans les présentations de fichier de cet état. Les données de la table et la version de l'état pour un exercice fiscal particulier doivent donc concorder. Si des codes personnalisés sont ajoutés à la table, ces derniers doivent être mappés aux zones d'honoraires au sein de cet objet.  

Les modifications réglementaires affectant cet état et les données de la table sont généralement gérés lors de mises à jour de fin d'exercice.
Il peut être utile d'exécuter l'état **Fournisseur 1099 Information** pour vérifier les données avant de générer le fichier électronique.  

## <a name="see-also"></a>Voir aussi
[Procédure : enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md)  
[Procédure : enregistrer des achats](purchasing-how-record-purchases.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

