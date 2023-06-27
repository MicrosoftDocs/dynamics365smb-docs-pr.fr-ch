---
title: Configurer des documents entrants
description: 'Configurez la fonctionnalité Documents entrants pour créer des documents électroniques, gérer des tâches OCR, importer des factures, et convertir des fichiers images.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents"></a>Configurer des documents entrants

Si vous créez des lignes feuille comptabilité à partir des enregistrements de documents entrants, vous devez spécifier sur la page **Paramètres des documents entrants** quels modèle et nom de feuille utiliser.

Une fois que la fonctionnalité **Documents entrants** est configurée, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés. Les fichiers externes peuvent être joints à n’importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables. Pour plus d’informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Configurer la fonctionnalité Documents entrants

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration document entrant**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Dans le cadre de la configuration, vous devez décider si vous souhaitez exiger l’approbation des documents entrants. Pour demander une approbation, vous devez [configurer des approbateurs et des flux de travail approbation](#to-set-up-approvers-of-incoming-document-records). Si votre organisation n’a pas l’intention d’exiger l’approbation, vous pouvez ignorer la section suivante.

Enfin, si vous utilisez un service OCR pour convertir des fichiers PDF ou image représentant des documents entrants, [vous devez le configurer](#to-set-up-an-ocr-service). Sinon, vous pouvez également ignorer cette section.

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Configurer des approbateurs d’enregistrements document entrant

Si vous ne souhaitez pas que les utilisateurs créent des factures ou des lignes feuille comptabilité à partir d’enregistrements de documents entrants, sauf si les documents ont été préalablement approuvés, configurez un processus d’approbation pour les documents entrants. Les approbateurs de documents entrants doivent être paramétrés comme des utilisateurs de flux de travail approbation.

Avant de pouvoir créer des workflows qui impliquent des étapes d’approbation, vous devez configurer les utilisateurs du workflow qui sont impliqués dans les processus d’approbation. Sur la page **Paramètres utilisateur d’approbation**, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d’approbation sont déléguées lorsque l’approbateur initial est absent. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Configurer un service ROC

Pour transformer des fichiers PDF et image en documents électroniques que vous pouvez convertir en factures, avoirs ou lignes feuille, configurez la fonction OCR. Vous pouvez également créer des écritures manuellement pour représenter les documents externes.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres services OCR**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Vos données de connexion sont automatiquement chiffrées.

Pour en savoir plus, voir [Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
