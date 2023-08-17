---
title: Plusieurs contrats | Microsoft Docs
description: 'Selon les accords de votre niveau de service avec un client, vous pouvez avoir à gérer un article de service sous plusieurs contrats de service.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="multiple-contracts"></a>Plusieurs contrats
Selon les accords de votre niveau de service avec un client, vous pouvez avoir à gérer un article de service sous plusieurs contrats de service.  
  
En gérant un article de service sous plusieurs contrats, vous pouvez effectuer les opérations suivantes :  
  
* Émettre différents contrats pour un même article de service.  
* Assurer la maintenance des composants séparément.  
* Envisager les différentes compétences qui sont requises pour assurer la maintenance de différents aspects d’un article de service, comme les composants mécaniques et les logiciels.  
* Spécifier des délais de réponse et fréquences de maintenance différents pour les composants d’un article de service.  
* Indiquer différents types d’activité à exécuter sur un article de service si celui-ci demande différents types de maintenance à des moments différents.  
* Sélectionner et affecter un numéro contrat adéquat à une ligne article de service lorsque vous créez une commande service.  
* Gérer les informations financières pertinentes portant sur les articles de service et les accords de niveau de service.  
  
Vous pouvez vous inspirer des exemples suivants d’utilisation de la fonctionnalité de contrats multiples.  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Création de plusieurs contrats par article de service
Vous pouvez créer manuellement un contrat de service ou un devis contrat pour des articles de service déjà enregistrés dans des contrats non annulés appartenant à un même client. Pour cela, utilisez la procédure standard de création de contrats de service et de devis contrat de service. Pour plus d’informations, voir [Utiliser des contrats de service et des devis contrat de service](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Lorsque vous ajoutez un article de service à une ligne contrat déjà enregistrée dans d’autres contrats de service ou devis contrat, un message d’avertissement est affiché indiquant que l’article de service appartient déjà à un ou plusieurs contrats de service ou devis contrat. Si vous confirmez ce message, toutes les informations pertinentes de l’article de service sont copiées dans une ligne contrat nouvellement créée.  
  
## <a name="copying-documents"></a>Copie de documents
Vous pouvez créer automatiquement un contrat service ou un devis contrat pour des articles de service déjà enregistrés dans d’autres contrats de service ou devis contrat à l’aide de l’action **Copier à partir du document**.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Création de commandes service pour plusieurs contrats
Vous pouvez manuellement créer une commande service pour un article de service qui est enregistré dans plusieurs contrats actifs. Un contrat service est actif lorsqu’il est signé et non expiré.  
  
## <a name="see-also"></a>Voir aussi
[Exécution des contrats de service](service-fulfill-service-contracts.md)  
[Créer commande service](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
