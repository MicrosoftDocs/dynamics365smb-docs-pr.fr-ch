---
title: "Mise à jour d'une présentation d'état | Microsoft Docs"
description: "Vous pouvez être amené à mettre à jour une présentation d'état personnalisée qui est utilisée dans un état. Cela est nécessaire si une modification de conception a été apportée à l'ensemble de données de l'état, par exemple, si un champ utilisé dans la présentation a été supprimé de l'ensemble de données de l'état."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 681540708d9807aafebcf5701232a282a189e47b
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="updating-report-or-document-layouts"></a>Mise à jour des présentations de rapport ou de document
À l'occasion, vous pouvez être amené à mettre à jour une présentation d'état personnalisée qui est utilisée dans un état. Cela est nécessaire si une modification de conception a été apportée à l'ensemble de données de l'état, par exemple, si un champ utilisé dans la présentation a été supprimé de l'ensemble de données de l'état. Si une présentation de rapport requiert une mise à jour, vous obtiendrez un message d'erreur lorsque vous tentez de visualiser, d'imprimer ou d'enregistrer le rapport.  
  
Vous pouvez mettre à jour automatiquement une présentation d'état à partir du message d'erreur qui s'affiche lorsque vous lancez l'état en cliquant sur le bouton **Oui** du message d'erreur. Ou, avant l'exécution d'états, vous pouvez mettre à jour des présentations d'état spécifiques ou toutes les présentations d'état personnalisées susceptibles d'être affectées par les modifications de l'ensemble de données.  
  
Vous pouvez aussi tester des mises à jour sans appliquer les modifications nécessaires aux présentations d'état personnalisées. Vous pouvez ainsi visualiser les modifications qui seront appliquées à la présentation d'état et identifier des problèmes éventuels pendant cette opération. À partir des résultats du test, vous pouvez ouvrir les présentations d'état personnalisées directement pour résoudre les problèmes. Il est recommandé de tester les mises à jour de présentations d'état avant d'appliquer les mises à jour.  
  
Certaines modifications de l'ensemble de données d'état peuvent être automatiquement mises à jour dans les présentations d'état. Certaines modifications nécessiteront de modifier manuellement la présentation d'état. Pour plus d'informations, consultez [Limitations de la mise à jour d'une présentation d'état personnalisée](ui-update-report-layouts.md#UpdateLimitations).  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a>Pour mettre à jour une ou plusieurs présentations d'état personnalisées  
  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Présentations état**, puis sélectionnez le lien associé.  
  
2.  Dans la fenêtre **Présentations état**, si vous souhaitez mettre à jour un état spécifique, sélectionnez la présentation dans la liste, puis choisissez l'action **Mettre à jour présentation**. Ou, si vous souhaitez mettre à jour toutes les présentations d'état personnalisées pour la société, choisissez l'action **Mettre à jour toutes les présentations**.  

Si aucune erreur ne se produit, la mise à jour est appliquée aux présentations d'état. Si des erreurs se produisent, un message contenant les erreurs s'affiche. Vous devez modifier manuellement la présentation d'état personnalisée pour corriger l'erreur. Pour plus d'informations, consultez [Résolution des erreurs](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Pour tester les mises à jour de présentations d'état personnalisées  
  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sélection présentation état**, puis sélectionnez le lien associé.  
  
2.  Dans la fenêtre **Sélection présentation état**, choisissez l'action **Mises à jour présentation test**.  
  
 Les modifications des présentations d'état sont testées mais pas appliquées aux présentations d'état réelles. La fenêtre **Journal mise à jour présentation état** s'affiche pour indiquer le statut des mises à jour potentielles pour chaque présentation d'état. Si une présentation d'état contient des erreurs, vous pouvez y accéder directement à partir du message pour résoudre les problèmes. Pour plus d'informations, consultez [Résolution des erreurs](ui-update-report-layouts.md#FixErrors).  
  
##  <a name="UpdateLimitations"></a> Limitations de la mise à jour d'une présentation d'état personnalisée  
 Il existe plusieurs types de modifications que la mise à jour automatique peut appliquer à des présentations d'état personnalisées, par exemple, un champ utilisé dans la présentation a été supprimé de l'ensemble de données d'état. Toutefois, la mise à jour automatique ne peut pas gérer les modifications ci-après apportées à un ensemble de données d'état.  
  
1.  Champs, étiquettes ou éléments de données supprimés.  
  
2.  Noms de champ en double dans la présentation d'état lorsqu'un champ a été renommé dans l'ensemble de données. Ceci doit être traité comme une erreur de conception.  
  
3.  Scénarios de mise à niveau où plusieurs itérations d'une présentation d'état engendrent plusieurs actions d'attribution d'un nouveau nom sur les mêmes champs, étiquettes ou éléments de données.  
  
 Si le processus de mise à jour détecte l'un de ces problèmes, la mise à jour ne peut pas être appliquée. Vous devez résoudre les problèmes manuellement, par exemple en modifiant la présentation d'état dans Word, ou par programme à l'aide de codeunits de mise à niveau.  
  
##  <a name="FixErrors"></a> Correction des erreurs  
 Si vous obtenez un message d'erreur lorsque vous mettez à jour ou testez des mises à jour de présentation d'état, vous devez généralement modifier la présentation d'état pour résoudre le problème. Lisez le message d'erreur pour déterminer la cause du problème.  
  
 Le problème le plus courant se pose lorsqu'un champ utilisé sur la présentation a été supprimé de l'ensemble des données de l'état. Dans ce cas, vous pouvez visualiser une ligne du message d'erreur indiquant qu'un article a été supprimé. Pour résoudre ce problème, vous devez modifier la présentation et supprimer le champ en question.  
  
 Pour plus d'informations, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  
  
 Une fois que vous avez modifié la présentation, essayez de mettre de nouveau à jour la présentation.  
  
## <a name="see-also"></a>Voir aussi  
 [Gestion des présentations de rapport](ui-manage-report-layouts.md)  
 [Utilisation des états](ui-work-report.md)  
