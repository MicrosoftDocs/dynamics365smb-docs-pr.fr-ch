---
title: Configurer les documents entrants| Microsoft Docs
description: "Utilisez la fonctionnalité Documents entrants pour créer des documents électroniques, gérer des tâches OCR, importer des factures, et convertir des fichiers images."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6381fc0949c3f6789a6b3387d119051403bcbb4a
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-incoming-documents"></a>Configurer des documents entrants
Si vous créez des lignes feuille comptabilité à partir des enregistrements de documents entrants, vous devez spécifier dans la fenêtre **Paramètres des documents entrants** quels modèle et nom de feuille utiliser.

Si vous ne souhaitez pas que les utilisateurs créent des factures ou des lignes feuille comptabilité à partir d'enregistrements de documents entrants, sauf si les documents ont été préalablement approuvés, vous devez paramétrer des approbateurs dans la fenêtre **Approbateurs de document entrant**.

Pour convertir les fichiers PDF et image en documents électroniques que vous pouvez convertir, par exemple, en factures achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord configurer la fonctionnalité OCR et activer le service.

Une fois que la fonctionnalité Documents entrants est configurée, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés. Les fichiers externes peuvent être joints à n'importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables. Pour plus d'informations, voir la section [Traitement des documents entrants](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Configurer la fonctionnalité Documents entrants
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres des documents entrants**, puis sélectionnez le lien connexe.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Configurer des approbateurs d'enregistrements document entrant
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres des documents entrants**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Paramètres des documents entrants**, sélectionnez l'action **Approbateurs**.

    La fenêtre **Approbateurs de document entrant** affiche tous les utilisateurs configurés dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Sélectionnez un ou plusieurs utilisateurs pouvant approuver un document entrant pour qu'un document ou une ligne feuille connexe puisse être créée.

Lorsque des approbateurs ont été configurés dans la fenêtre **Approbateurs de document entrant**, seuls ces utilisateurs peuvent approuver un document entrant si la case **Exiger une approbation pour créer** est cochée dans la fenêtre **Paramètres des documents entrants**.

> [!NOTE]  
>   Ce paramétrage d'approbation n'est pas lié aux flux d'approbation. Pour plus d'informations, reportez-vous à [Utilisation des flux d'approbation](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Configurer un service ROC
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres service OCR**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Chiffrer les informations de connexion
Il est recommandé de protéger les informations de connexion que vous saisissez dans la fenêtre **Paramètres service OCR**. Vous pouvez chiffrer des données sur le serveur en générant de nouvelles clés de chiffrement ou en important des clés existantes que vous activez sur l'instance de serveur qui est connectée à la base de données.

1. Dans la fenêtre **Paramètres service OCR**, sélectionnez l'action **Gestion du chiffrement**.
2. Dans la fenêtre **Gestion du chiffrement des données**, activez le chiffrement de vos données.

## <a name="see-also"></a>Voir aussi
[Traiter les documents entrants](across-process-income-documents.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

