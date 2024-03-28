---
title: Configurer des codes pour les pistes d’audit
description: Découvrez les tâches de configuration des codes source et des codes motif que vous pouvez utiliser pour suivre les pistes d’audit.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Configuration des codes source et des codes de motif pour les pistes d’audit

Un code journal est affecté automatiquement à toutes les écritures validées, de sorte que les transactions puissent être suivies jusqu’à leur origine. Pour attribuer un autre code journal aux écritures, vous pouvez utiliser les codes motif. Ces derniers permettent d'indiquer le motif de création d'une écriture. Lorsque vous les configurez, vous pouvez les affecter à des modèles ou des noms de feuilles, ainsi qu’à des lignes feuille et documents spécifiques.  

Pour les codes source et les codes motif, utilisez des codes faciles à mémoriser et descriptifs. Le code doit être unique et vous pouvez configurer autant de codes que vous le souhaitez.

## <a name="define-source-codes"></a>Définir des codes journaux

Parfois, vous souhaitez savoir comment une écriture particulière a été créée, par exemple si elle vient de la validation d’une feuille ou d’une facture achat. Un code journal indique l’emplacement de création d’une écriture. Les écritures sont créées lors de la validation des feuilles et des factures et lors de l’exécution de certains traitements par lots. Un code journal spécifique existe pour chaque type compta. et est affecté lors de la création d’écritures individuelles.  

La validation de feuilles, de commandes, de factures ou d’avoirs, et l’exécution de divers traitement par lots, crée des écritures dans les états financiers. La page **Paramètres codes journaux** comporte plusieurs raccourcis, un pour chaque domaine d’application. Chaque raccourci indique les codes journaux applicables pour ce module.

Lorsque vous validez ou exécutez un traitement par lots, le bon code journal est relié automatiquement à l’écriture. Par exemple, lorsque vous validez à partir de la feuille, l’écriture est codifiée en tant que *JNLCOMPTA*. Vous pouvez ensuite filtrer la page **Écritures comptables** pour afficher les écritures qui ont été publiées à partir de la feuille comptabilité ou des documents de vente, par exemple

### <a name="to-define-source-codes"></a>Pour définir des codes journaux

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") saisissez **Paramètres codes journaux**, puis choisissez le lien associé.  

2. Dans la fenêtre **Paramètres codes journaux**, pour chaque type de validation et travail par lots, spécifiez le code source approprié.  

Vous pouvez modifier le contenu d’un champ ultérieurement, et cette modification aura alors un impact sur les publications futures.

## <a name="change-source-codes"></a>Modifier les codes journaux

Vous pouvez modifier un code journal. Par exemple, vous pouvez remplacer le code journal *GENJNL* par *GNJ*.

### <a name="to-change-source-codes"></a>Pour modifier des codes journaux

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Codes journal.**, puis choisissez le lien associé.

2. Sur la ligne du code à modifier, sélectionnez le code dans le champ **Code**.

3. Saisissez le nouveau code, puis cliquez sur le bouton **OK**. Vous pouvez également modifier la valeur du champ **Description**.

Toutes les nouvelles écritures qui sont validées à partir de la feuille comptabilité, se verront attribuer un nouveau code journal.

## <a name="define-reason-codes"></a>Définir des codes motif

Les codes de motif complètent les codes source et sont utilisés pour indiquer la raison pour laquelle une écriture a été créée. Vous pouvez affecter des codes motif à chaque écriture, et vous pouvez affecter des codes permanents à des modèles feuille et à des feuilles spécifiques. Lorsqu’un code motif est lié à une ligne feuille ou à un en-tête vente ou achat, toutes les écritures sont marquées avec le code motif lorsqu’elles sont enregistrées.  

### <a name="to-set-up-reason-codes"></a>Pour configurer des codes motif

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche")  entrez **Codes de motif**, puis choisissez le lien associé.

2. Dans la fenêtre **Codes motif**, saisissez le premier code dans le champ **Code**. Dans le champ **Désignation**, saisissez un texte explicatif.

Répétez cette procédure pour chaque code à utiliser. Vous pouvez configurer autant de codes que vous le souhaitez.

La procédure suivante décrit comment ajouter un code motif à un modèle feuille, mais des étapes similaires s’appliquent à l’ajout d’un code motif à une ligne feuille ou à une feuille.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Pour affecter des codes motif à des modèles feuille

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche")  entrez **Modèles feuille comptabilité**, puis sélectionnez le lien associé.

2. Sur la ligne du modèle feuille sélectionné, renseignez le champ **Code motif** avec le code souhaité.

3. Fermez le modèle feuille.

Le code motif sélectionné est copié dans les nouvelles feuilles créées sous le modèle feuille. Pour affecter des codes motif à des modèles feuille dans les autres modules, procédez de la même manière.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Pour utiliser des codes motif dans les documents achat et vente

1. Ouvrez le document achat ou vente approprié.

2. Dans l’en-tête achat ou vente, entrez le code dans le champ **Code motif**.

Lors de la validation de la facture, le code motif est copié dans chaque écriture comptable, client et fournisseur. Vous ne pouvez pas affecter un code motif différent à chacune des lignes achat et vente, car toutes les lignes sont validées sous la forme d'une écriture unique.

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
