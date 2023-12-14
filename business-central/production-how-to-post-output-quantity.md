---
title: Validation par lots de la production et des temps d’exécution
description: La quantité de sortie représente l’avancement du travail sous la forme de la quantité finie et de la capacité utilisée du travail ou du poste de charge.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: bholtorf
---
# <a name="batch-post-output-and-run-times"></a>Valider par lots la production et les temps d’exécution

La quantité de sortie représente l’avancement du travail sous la forme de la quantité finie et de la capacité utilisée du travail ou du poste de charge.

Vous pouvez utiliser la feuille production pour :

* Ajustez le stock en fonction de la production des articles finis émanant de la production.
* Enregistrez les quantités et les rebuts pour chaque opération dans la gamme de production.
* Enregistrez la configuration et le temps d’exécution pour les centres de travail et les postes de charge.

> [!NOTE]
> Si le routage de production est utilisé, le stock est mis à jour uniquement lorsque vous validez la quantité produite durant la dernière opération.

La page **Feuille production** vous permet d’effectuer les mêmes tâches que sur la page **Journal production**, et exécuter en même temps les tâches connexes de validation de la consommation. Pour plus d’informations, voir [Enregistrer la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Pour valider les quantités produites et/ou enregistrer les temps d’exécution pour une ou plusieurs lignes ordre de fabrication

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille production**, puis choisissez le lien associé.  
2. Renseignez les champs en indiquant les données relatives à la fabrication et/ou les temps d’exécution. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Vous pouvez utiliser la fonction **Éclater gamme** pour générer des lignes feuille à partir des ordres de fabrication.
  
3. Si l’opération est achevée, sélectionnez le champ **Terminé**.  
4. Choisissez l’action **Valider** pour valider les opérations.

    Les écritures comptables de capacité sont mises à jour pour les postes de charge ou centres de travail utilisés avec des informations sur le temps et la quantité de production et de rebut. Si vous avez validé la dernière opération, l’article sera ajouté au stock.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a>Voir aussi

[Valider le rebut manuellement](production-how-to-post-scrap.md)
[Contrepasser la validation de production](production-how-to-reverse-output-posting.md)
[Production](production-manage-manufacturing.md)
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
