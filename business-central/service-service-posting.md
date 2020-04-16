---
title: Validation de service | Microsoft Docs
description: La fonctionnalité de validation de service vous permet de traiter vos documents efficacement et de maintenir une stratégie de service client fructueuse. Vous pouvez créer et mettre à jour des documents validés, et créer des écritures comptables dans le module Service et dans d'autres modules pour garantir une mise à jour correcte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6ecf6b203b7dd3264c3499f8b60bbdb29698e647
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192474"
---
# <a name="service-posting"></a>Validation de service
La fonctionnalité de validation de service vous permet de traiter vos documents efficacement et de maintenir une stratégie de service client fructueuse. Vous pouvez créer et mettre à jour des documents validés, et créer des écritures comptables dans le module Service et dans d'autres modules pour garantir une mise à jour correcte.  

> [!NOTE]  
>  La section suivante décrit la validation de service indépendamment de la façon dont les articles sont gérés physiquement dans l'entrepôt.  
>   
>  Dans un magasin qui n'est pas configuré pour appeler une gestion d'entrepôt, vous effectuez des actions de validation directement sur la page **Lignes service**. Dans les magasins qui impliquent une gestion d'entrepôt, les actions de validation décrites, à l'exception des actions Expédier et Consommer, sont effectuées indirectement au moyen de différentes fonctions d'expédition de l'entrepôt, selon la configuration. Pour plus d'informations, voir [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Expédition  
La fonction Expédition vous permet d'enregistrer les articles et le temps appropriés entrés dans les lignes d'une commande service après que vous ayez exécuté le service. Une expédition enregistrée est crée et des mises à jour interviennent dans le module Stock, ainsi que d'autres modules dans [!INCLUDE[d365fin](includes/d365fin_md.md)] afin d'indiquer que les articles ont été prélevés sur le stock et envoyés au client. Plus particulièrement, des écritures comptables article, des écritures comptables valeur, des écritures comptables service sont générés ainsi que des écritures comptables garantie.  

Si le magasin est configuré pour exiger la gestion d'entrepôt, l'expédition et le déplacement d'articles de ligne service s'exécutent de la même manière que pour d'autres documents origine. La seule différence est que les articles de la ligne service peuvent être consommés en externe ou en interne et qui nécessitent deux fonctions de lancement différentes.

## <a name="invoice"></a>Facturer  
Vous devez utiliser l'option de facturation pour émettre une facture à l'adresse du client auquel vous voulez facturer le service. Généralement, il s'agit de la différence entre la quantité expédiée enregistrée par la fonction de **validation de l'expédition** et la quantité consommée enregistrée par la fonction de **validation de la consommation** sujette à facturation. Vous ne pouvez pas facturer ce qui n'a pas été expédié. Lors de l'exécution de la fonction de **validation de la facture**, une facture service validée est crée et les documents validés sont mis à jour avant de les rendre cohérents avec les quantités qui sont contenues dans la facture émise. Comme pour les autres procédures de validation, es écritures comptables appropriées, qui incluent les écritures comptables, sont générées.  

## <a name="ship-and-invoice"></a>Expédition et facturation  
L'option d'expédition et de facturation vous permet d'émettre une expédition de service et une facture en même temps.  

## <a name="ship-and-consume"></a>Livrer et consommer  
L'option expédier et consommer vous permet d'enregistrer et de valider des articles, des coûts ou des heures de maintenance, mais qui ne peuvent pas figurer dans la facture adressée au client. Une facture n'est pas émise mais vous pouvez émettre simultanément une expédition service et une consommation service afin de refléter le fait que certains articles ou des heures ont été donnés au client gratuitement. Les écritures comptables correspondantes sont également créées pour enregistrer la consommation.  

> [!NOTE]  
>  La procédure de validation de service vous permet d'effectuer une validation partielle. Vous pouvez créer une expédition ou une facture partielle en renseignant les champs **Qté à expédier** et **Qté à facturer** sur des lignes service de commandes de service avant la validation. Notez que vous ne pouvez pas créer de facture pour quelque chose qui n'a pas été expédié. Cela signifie que, avant de pouvoir facturer, vous devez avoir enregistré une expédition ou choisir d'expédier et de facturer en même temps.  

Une fois la validation terminée, vous pouvez visualiser les documents service validés depuis les pages correspondantes (**Expédition service enreg.** et **Facture service enreg.**). Vous pouvez visualiser les écritures validées créées sur diverses pages contenant des écritures validées (**Écritures comptables**, **Écritures comptables article**, **Écritures entrepôt**, **Écritures comptables service**, **Écritures comptables projet**, **Écritures comptables garantie**, etc.).  

## <a name="to-view-information-about-a-posted-service-document"></a>Pour visualiser les informations relatives aux documents service validés  
Lorsque vous validez une facture service, une expédition service ou un avoir service, les informations du document sont transférées respectivement sur les pages **Facture service enreg.**, **Expédition service enreg.** ou **Avoir service enreg.** Vous ne pouvez rien entrer, modifier ni supprimer sur ces pages. Vous pouvez imprimer un bon de livraison, une facture ou un avoir à partir de ces pages.  

La procédure suivante utilise un exemple de facture service enregistrée ; cette même procédure est applicable aux expéditions de service et aux avoirs enregistrés.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Facture service enreg.**, puis sélectionnez le lien associé.  
2. Ouvrez la facture service enregistrée que vous souhaitez afficher.  
3. Pour obtenir un aperçu de la facture validée, choisissez l'action **Statistiques**.  

    La page **Statistiques commande service** s'ouvre. La page affiche des informations telles que la quantité, le montant, la TVA, le coût, la marge et le crédit autorisé du client pour le document validé.

## <a name="see-also"></a>Voir aussi  
[Valider des commandes de service](service-how-to-post-service-orders.md)   
[Créer commande service](service-how-to-create-service-orders.md)
