---
title: "Procédure de configuration de nouvelles sociétés à l'aide d'une applet de commande | Microsoft Docs"
description: "Dans un certain nombre de scénarios, vous pouvez vouloir facturer et importer un package configuration sans impliquer vos utilisateurs ni utiliser l'interface utilisateur RapidStart Services. Vous pouvez le faire à l'aide d'une applet de commande Windows PowerShell."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Configurer les nouvelles sociétés à l'aide d'une applet de commande
Dans un certain nombre de scénarios, vous pouvez vouloir facturer et importer un package configuration sans impliquer vos utilisateurs ni utiliser l'interface utilisateur RapidStart Services. Vous pouvez le faire à l'aide d'une applet de commande Windows PowerShell. Les scénarios où cela peut être utile sont les suivants :  

- Importer des données dans plusieurs installations de [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Configurer des domaines d'application supplémentaires pour plusieurs clients.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Pour déployer un package configuration à l'aide d'une applet de commande  

1. Préparez un package RapidStart Services. Par exemple, vous pouvez créer un package pour importer certaines valeurs et les noms de la table et des champs pour insérer ces valeurs dedans.  
2. Placez le package sur un ordinateur où vous allez lancer l'applet de commande.  
3. Ouvrez l'interpréteur de commandes d'administration de [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4. Saisissez **Invoke-NAVCodeUnit** et spécifiez des informations similaires à l'exemple suivant.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
L'applet de commande importe le package dans chaque société. Les utilisateurs peuvent commencer à utiliser la nouvelle fonctionnalité immédiatement.  

## <a name="see-also"></a>Voir aussi  
[Configurer de nouvelles sociétés](admin-how-to-configure-new-companies.md)  
[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  
[Applets de commande Windows PowerShell Microsoft Dynamics NAV](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

