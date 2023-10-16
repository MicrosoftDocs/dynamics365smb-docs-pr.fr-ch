---
title: Importer les transactions de paie
description: 'Pour gérer les paies, vous importez et validez des transactions financières de votre fournisseur de paie dans la comptabilité, en utilisant une extension de paie telle que Ceridian.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Importation des transactions de paie

Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité. Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie sur la page **Feuille comptabilité**. Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés. Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.

> [!NOTE]  
> Pour utiliser cette fonctionnalité, une extension pour l’importation de la paie doit être installée et activée. Les extensions Salaire de Ceridian et Importer le fichier de paie de Quickbooks sont préinstallées dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md).

## Pour importer un fichier de paie

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilité**, puis choisissez le lien associé.
2. Dans le nom feuille comptabilité pertinent, sélectionnez l’action **Importer les transactions de paie**. Un guide d’installation assisté s’ouvre.
3. Suivez les étapes de la page **Importer les transactions de paie**.

    > [!TIP]  
    >   Dans l’étape à propos du mappage des enregistrements de paie externes dans les comptes généraux, les mappages que vous effectuez seront reconnus la prochaine fois que les mêmes enregistrements seront importés. Cela vous permettra d’économiser du temps car vous n’avez pas à remplir manuellement le champ **N° compte** dans la feuille comptabilité à chaque importation de transactions de paie récurrentes.   

    Lorsque vous cliquez sur le bouton **OK** dans le guide de configuration assistée, la page **Feuille comptabilité** est complétée par des lignes représentant les transactions contenues dans le fichier de paie et par les comptes appropriés des champs **Compte général** en fonction des mappages effectués dans le guide.
4. Modifiez ou validez les lignes feuille comme pour toute autre transaction comptable générale. Pour plus d’informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).   

## Voir aussi

[Finances](finance.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]