---
title: Configurer et publier des services Web de KPI basés sur des états financiers
description: Cet article décrit comment afficher les données de KPI d’état financier basées sur des états financiers spécifiques.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a><a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a>Configurer et publier des services Web de KPI basés sur des états financiers

La page **État financier - Paramètres du service web KPI** vous permet de configurer la manière dont les données des KPI (indicateurs de performances clés) des états financiers sont affichées, et sur quels états financiers spécifiques baser les KPI. Lorsque vous sélectionnez **Publier le service Web**, les données de KPI de l’état financier spécifié sont ajoutées à la liste des services Web publiés sur la page **Services web**.

> [!NOTE]
> Si vous utilisez ce service Web, les dates de clôture ne sont pas incluses dans votre ensemble de données. Vous pouvez utiliser des filtres dans Power BI pour analyser différentes périodes.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a><a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a>Configurer et publier des services Web de KPI basés sur des états financiers
  
1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration du service web de KPI des états financiers**, puis choisissez le lien associé.
2. Renseignez les champs du raccourci **Général**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sur le raccourci **Définitions de ligne**, renseignez les champs.
4. Répétez l’étape 3 pour tous les états financiers sur lesquels vous souhaitez baser le service Web de KPI des états financiers.  
5. Pour visualiser ou modifier l’état financier sélectionné, sur le raccourci **Définitions de ligne**, choisissez l’action **Modifier la définition de ligne**.
6. Pour afficher les données de KPI de l’état financier que vous avez défini, choisissez l’action **Service web de KPI des états financiers**.
7. Pour publier le service Web de KPI de l’état financier, choisissez l’action **Publier le service web**.

Vous pouvez désormais créer des états financiers dans Power BI basés sur le ou les services Web que vous avez créés.

> [!NOTE]  
> Vous pouvez également publier le service Web de KPI en pointant vers l’objet de page **Configuration du service web de KPI des états financiers** à partir de la page **Services web**. Pour plus d’informations, consultez [Publier un service Web](across-how-publish-web-service.md).

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Décisionnel pour le secteur de la finance](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
