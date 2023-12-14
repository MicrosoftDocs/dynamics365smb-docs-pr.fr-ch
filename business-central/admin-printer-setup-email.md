---
title: Paramétrer des imprimantes par e-mail
description: Description pratique
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# Paramétrer des imprimantes par e-mail

Cet article explique comment configurer des imprimantes compatibles avec les e-mails dans [!INCLUDE[prod_short](includes/prod_short.md)]. Avec ces imprimantes, [!INCLUDE[prod_short](includes/prod_short.md)] envoie les travaux d′impression à l’imprimante à l′aide de l′adresse e-mail de l′imprimante.

> [!TIP]
> Pour en savoir plus sur les autres possibilités d’impression, consultez [Vue d’ensemble de la gestion des imprimantes](admin-printer-setup-overview.md). 

## Conditions préalables

- 1re vague de lancement 2020 de [!INCLUDE[prod_short](includes/prod_short.md)] ou ultérieure
- L′extension **Envoyer à une imprimante par e-mail** est installée

    Cette extension est installée par défaut. Pour plus d’informations sur l’installation d’extensions, consultez [Installation et désinstallation d’extensions dans Business Central](ui-extensions-install-uninstall.md).
- La fonctionnalité de messagerie est configurée.

   En savoir plus sur [Configurer les e-mails](admin-how-setup-email.md).

## Ajouter une imprimante par e-mail

La page **Gestion des imprimantes**affiche les imprimantes configurées actuellement. La page vous donne également accès à la page **Paramètres** pour chaque imprimante pour modifier une configuration existante ou configurer une nouvelle imprimante.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionner **Imprimer par e-mail**, puis choisissez **Ajouter une imprimante e-mail**.
3. Sur la page **Paramètres de l′imprimante par e-mail**, renseignez les champs nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Vous devez sélectionner manuellement le format de papier approprié pour une imprimante, car aucune imprimante locale ni aucun paramètre utilisateur ne peuvent être stockés.
    >
    > Sachez que l’extension Imprimante par e-mail est définie par défaut sur le format de papier **A4**, qui n’est pas adapté en Amérique du Nord, par exemple.

## Déclaration de confidentialité

Si vous utilisez l’extension Imprimante par e-mail, tout ou partie des travaux d’impression sont envoyés à l’adresse e-mail configurée pour l’imprimante. Nous vous recommandons vivement d’associer un ID e-mail unique à un périphérique d’impression en utilisant uniquement les services officiels fournis par le fabricant du matériel, tels que HP ePrint, KonicaMinolta EveryonePrint ou Epson Email Print.

Prenez toutes les précautions de confidentialité nécessaires, notamment en veillant à configurer correctement les autorisations, les paramètres de confidentialité et les stratégies de conservation de la solution d’impression d’e-mails. Il est de votre responsabilité de fournir une adresse e-mail correcte, vérifiée et opérationnelle. En savoir plus sur la [déclaration de confidentialité Microsoft](https://privacy.microsoft.com/privacystatement).

## Étapes suivantes

[Paramétrer des imprimantes par défaut](ui-specify-printer-selection-reports.md)

## Voir aussi

[Vue d’ensemble de la gestion des imprimantes](admin-printer-setup-overview.md)  
[Configuration d’imprimantes à impression universelle](admin-printer-setup-universal-print.md)
[Imprimer un état](ui-work-report.md#PrintReport)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exécuter des traitements par lots](ui-how-run-batch-jobs.md)  
