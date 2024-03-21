---
title: Rapprochement des comptes bancaires et lettrage des paiements
description: 'Décrit les tâches de rapprochement de vos comptes bancaires, client, et fournisseur, valider des règlements ou des frais, et lettrer des paiements automatiquement.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Lettrage automatique des paiements et rapprochement des comptes bancaires
Vous devez régulièrement rapprocher vos comptes bancaires, créances client et créances fournisseur en lettrant les paiements enregistrés au niveau de la banque à leurs factures impayées et avoirs associés ou à d’autres écritures ouvertes dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Vous pouvez effectuer cette tâche sur la page **Feuille rapprochement bancaire**, par exemple, en important un fichier ou un flux de relevé bancaire pour enregistrer rapidement les paiements. Les paiements sont lettrés pour ouvrir des écritures client ou fournisseur selon les correspondances entre le texte de paiement et les informations d’écriture. Vous pouvez réviser et modifier les lettrages automatiques avant de valider la feuille. Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille. Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.

La logique qui gère la correspondance automatique du texte de paiement avec les informations d’écriture est configurée sur la page **Règles lettrage paiement** comme une série de règles hiérarchisées que vous pouvez modifier.

Vous pouvez également rapprocher des comptes bancaires sans rapprocher simultanément des paiements. Vous effectuez ce travail sur la page **Rapprochement bancaire**. Pour plus d’informations, voir [Rapprocher des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).   

Pour importer des relevés bancaires en tant que flux bancaire, vous devez d’abord configurer et activer le service Envestnet Yodlee Bank Feeds, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Vous pouvez également importer des fichiers de relevés bancaires au format délimité par des virgules ou des points-virgules (.CSV). Utilisez la configuration assistée **Configurer un format de fichier de relevé bancaire** pour définir les formats d’importation des relevés bancaires et attacher le format à un compte bancaire. Vous pouvez ensuite utiliser ces formats lorsque vous importez des relevés bancaires dans la page **Rapprochement des comptes bancaires**.

Vous pouvez également utiliser l’extension AMC Banking 365 Fundamentals pour convertir un fichier de relevé bancaire, à partir de n’importe quel format, en flux de données que vous pouvez importer dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

| Pour | Voir |
| --- | --- |
| Lettrer des paiements aux écritures comptables client ou fournisseur ouvertes en important un relevé bancaire, et rapprocher le compte bancaire lorsque tous les paiements sont lettrés. |[Rapprocher les paiements à l’aide de l’application automatique](receivables-how-reconcile-payments-auto-application.md) |
| Appliquer manuellement les paiements en affichant les informations détaillées sur les données de correspondance et des suggestions d’écritures ouvertes candidates à l’application des paiements. |[Réviser ou lettrer les paiements après un lettrage automatique](receivables-how-review-apply-payments-auto-application.md) |
| Résoudre les paiements qui ne peuvent pas être lettrés automatiquement à leurs écritures comptables ouvertes associées. Par exemple si les montants sont différents ou si une écriture comptable associée n’existe pas. |[Rapprocher les paiements qui ne peuvent pas être lettrés automatiquement](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Lier le texte des paiements à un client spécifique, fournisseur ou comptes généraux pour toujours valider les réceptions récurrentes en liquide ou les dépenses vers ces comptes quand ils ne peuvent être appliqués à aucun document. |[Mapper du texte sur des paiements récurrents avec des comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Configurez les règles pour définir comment les paiements/transactions bancaires doivent être automatiquement lettrés avec leurs écritures comptables ouvertes associées lorsque vous utilisez la fonction **Lettrer automatiquement** sur la page **Feuille rapprochement bancaire**.|[Définition des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md)|

## Voir aussi
[Rapprochement des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
