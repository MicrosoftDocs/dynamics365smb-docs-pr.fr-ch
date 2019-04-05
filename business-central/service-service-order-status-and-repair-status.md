---
title: Statut commande service et statut réparation | Microsoft Docs
description: Le champ Statut de la page Commande service et le statut réparation de l'article de service, qui est représenté par le champ Code du statut de réparation sur la page Commande service ont une certaine relation dans le module Service management. Le statut commande service reflète l'état réparation de tous les articles de service de la commande service.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a7ef1f214bda9c78113b320ddbd331b5a3e7de33
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820564"
---
# <a name="service-order-status-and-repair-status"></a>Statut commande service et statut réparation
Le champ **Statut** de la page **Commande service** et le statut réparation de l'article de service, qui est représenté par le champ **Code du statut de réparation** sur la page **Commande service** ont une certaine relation dans le module Service management. Le statut commande service reflète l'état réparation de tous les articles de service de la commande service.  

> [!NOTE]  
>  Ces deux champs de statut ne sont pas liés au champ **Statut de lancement** de l'en\-tête de commande de service, qui détermine la gestion des articles de service au niveau de l'entrepôt.  

 Chaque fois que le statut réparation d'un article de service d'une commande service est modifié, le programme met à jour le statut de la commande. Pour afficher l'état réparation général des articles de service, vous devez préciser les informations suivantes :  

* Le statut commande service auquel chaque état réparation est lié. Pour plus d'informations, voir Statut commande service.  
* Le niveau de priorité de chaque option statut commande service. Pour plus d'informations, voir Priorité.  

 Lorsque vous convertissez un devis service en commande service, l'état réparation de chaque article de service de la commande est modifié à **Initial** et le statut de la commande service passe à **Suspendu**.  

## <a name="specifying-service-order-status-for-repair-status"></a>Spécification du statut commande service pour l'état réparation  
Chaque état réparation est lié à un statut commande service précis. Les options de ce statut commande service sont **Suspendu**, **En cours**, **En attente** et **Terminé**. Neuf options d'état réparation sont disponibles : **Initial**, **En cours**, **Expertisé**, **Service en partie réalisé**, **Devis terminé**, **Attente réponse client**, **Pièce de rechange commandée**, **Pièce de rechange reçue** et **Terminé**.  

### <a name="pending"></a>Suspendu  
Le statut commande service **Suspendu** indique que le service peut démarrer ou continuer à n'importe quel moment. Pour cette raison, les quatre options d'état réparation **Initial**, **Expertisé**, **Service en partie réalisé** et **Pièce de rechange reçue** peuvent toutes être liées à ce statut commande service.  

### <a name="in-process"></a>En cours  
Le statut commande service **En cours** indique que le service est en cours. Par conséquent, les deux options d'état de réparation **En cours** et **Pièce de rechange commandée** peuvent être liées à ce statut commande service. Si vous liez le statut **Pièce de rechange commandée** au statut commande service **En cours,** vous devez aussi lier le statut **Pièce de rechange reçue** à ce statut commande service.  

### <a name="on-hold"></a>En attente  
Le statut commande service **En attente** indique que le service est momentanément en attente, parce que vous attendez une réponse du client ou des pièces de rechange pour que le service puisse commencer. Pour cette raison, les trois options d'état réparation **Devis terminé**, **Pièce de rechange commandée** et **Attente réponse client** peuvent toutes être liées à ce statut commande service.  

### <a name="finished"></a>Terminé  
Le statut commande service **Terminé** indique que la maintenance est terminée. Pour cette raison, l'état réparation **Terminé** est lié à ce statut.  

## <a name="assigning-priority-to-service-order-status"></a>Affectation de priorité à des statuts commande service  
Lorsque l'état réparation d'un article de service est modifié, les options statut commande service liées aux différentes options d'état réparation de tous les articles service de la commande sont identifiés. Si les articles de service sont liés à plusieurs options de statut commande service, l'option de statut commande service dont la priorité est la plus élevée est sélectionnée.  

Choisissez le statut commande service comportant les informations les plus importantes et affectez à ce statut la priorité la plus élevée, etc.  

### <a name="example"></a>Exemple :  
Voici ci-après un exemple d'affectation de niveau de priorité :  

* En cours - Très haute  
* Suspendu - Haute  
* En attente - Moyenne  
* Terminé - Basse  

Par exemple, si un article de service présente l'état réparation **Initial** (lié au statut commande service **Suspendu**), qu'un autre présente le statut **En cours** (lié au statut commande service **En cours**) et que le troisième présente le statut **Pièce de rechange commandée** (lié au statut commande service **En attente**), le statut commande service est **En cours** car il correspond au niveau de priorité le plus élevé.  

## <a name="see-also"></a>Voir aussi  
[Paramétrer les statuts des commandes service et des réparations](service-order-repair-status.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  
