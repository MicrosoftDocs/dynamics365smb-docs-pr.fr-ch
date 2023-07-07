---
title: Modifier l’aspect d’un état en sélectionnant une disposition différente
description: 'Vous pouvez utiliser différentes présentations d’un état, et passer d’une présentation à l’autre pour modifier l’aspect d’un état.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# <a name="legacy-set-the-layout-used-by-a-report"></a>(Hérité) Définir la présentation utilisée par un état

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Un rapport peut être créé avec plus d’une présentation de rapport, que vous pouvez ensuite changer au besoin.

Selon les présentations qui sont disponibles pour un rapport, vous pouvez choisir d’utiliser une présentation de rapport RDLC intégrée, une présentation de rapport Word, ou une présentation personnalisée. Pour plus d’informations sur les présentations de rapport RDLC et Word, les présentations intégrées et personnalisées, et plus encore, reportez-vous à [Gérer la présentation des états](ui-manage-report-layouts.md).

Lorsque des présentations de rapport personnalisées sont définies, vous pouvez les sélectionner à partir des fiches client et fournisseur pour spécifier que les présentations sélectionnées sont utilisées pour les documents que vous créez pour le client ou le fournisseur en question. Pour plus d’informations, voir [Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Les états de document (pas les listes) qui utilisent une mise en page d’état Word sont généralement plus rapides que ceux qui utilisent une mise en page d’état RDLC. Ainsi, si vous avez la possibilité de choisir entre une mise en page d’état Word ou RDLC pour un état de document, utilisez la mise en page d’état Word pour de meilleures performances.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Pour modifier la présentation de rapport à utiliser pour un rapport ou un document

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection présentation état**, puis sélectionnez le lien associé.
  
   La page **Sélection présentation état** répertorie tous les états disponibles pour la société spécifiée dans le champ **Société** en haut de la page. Le champ **Description présentation** <!-- **Selected Layout** -->spécifie la présentation qui est actuellement utilisée sur l’état.
2. Définissez le champ **Société** en haut de la page sur la société qui inclut l’état.

   Ce champ vous permet de définir différentes présentations pour le même état dans différentes entreprises.

3. Pour modifier la présentation utilisée par un état, sur la ligne correspondant à l’état, définissez le champ **Présentation sélectionnée** sur l’une des options suivantes :
   * **RDLC (intégré)**, utilise la présentation d’état RDLC intégrée sur l’état.
   * **Word (intégré)**, utilise la présentation état Word intégrée sur l’état.
   * **Personnalisée**, utilise une présentation personnalisée sur l’état.  

> [!NOTE]
> Si vous choisissez une présentation de rapport de type **RDLC (intégré)** ou **Word (intégré)** et si vous recevez un message d’erreur indiquant que le rapport n’a pas de présentation du type spécifié, alors vous devez choisir une autre option de présentation ou créer une présentation de rapport personnalisée du type que vous souhaitez utiliser. Consultez la procédure suivante.

Si vous avez sélectionné une présentation de rapport RDLC ou Word intégrée, aucune action supplémentaire n’est requise, et la présentation sera utilisée la prochaine fois que le rapport sera exécuté.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Pour modifier la présentation personnalisée à utiliser pour une présentation de rapport

Vous pouvez également modifier la présentation personnalisée actuellement utilisée. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

Toutes les présentations de rapport personnalisées qui existent pour les présentations de rapport dans une société sont répertoriées sur la page **Présentations état personnalisées**. Sur la page **Sélection présentation état**, il est possible de savoir quelles sont les présentations personnalisées disponibles pour chaque rapport dans le récapitulatif **Présentations personnalisées**.

1. Sur la page **Sélection présentation état**, sur la ligne de la présentation de rapport que vous souhaitez modifier, cliquez sur le bouton de recherche dans le champ **Description présentation personnalisée**.
2. Sur la page **Présentations état personnalisées**, sélectionnez la ligne de la présentation personnalisée que vous souhaitez utiliser, puis cliquez sur le bouton **OK**.

Le nom de la présentation personnalisée sélectionnée s’affiche maintenant dans le champ **Description présentation personnalisée**, et sera utilisé la prochaine fois que le rapport ou le document sera prévisualisé, imprimé ou envoyé.

Vous pouvez maintenant accéder à vos fiches client et fournisseur pour spécifier les présentations à utiliser pour différents documents que vous créez pour le client ou le fournisseur en question, comme les confirmations de commande ou les relances de paiement. Pour plus d’informations, voir [Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) associée

## <a name="see-also"></a>Voir aussi
[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
