---
title: Résoudre les problèmes des fonctionnalités de Copilot et d’IA
description: Découvrez comment résoudre les problèmes courants que vous pourriez rencontrer lorsque vous travaillez avec les fonctionnalités Copilot et IA dans Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Résoudre les problèmes des fonctionnalités de Copilot et d’IA

Copilot est une fonctionnalité basée sur l’IA de Business Central qui aide à diverses tâches telles que la rédaction de textes marketing et le rapprochement des comptes bancaires. Si vous rencontrez des problèmes avec Copilot ou d’autres fonctionnalités d’IA, cet article peut vous aider à identifier et à résoudre les problèmes courants.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot n’apparaît pas sur les pages

Si la fonctionnalité Copilot, telle que l’action **Rédiger avec Copilot** pour les suggestions de textes marketing ou l’action **Réconcilier avec Copilot** pour l’aide au rapprochement des comptes bancaires n’apparaît pas sur une page comme prévu, vérifiez les points suivants :

- Si la fonctionnalité est contrôlée sous Gestion des fonctionnalités, assurez-vous qu’elle est activée. [En savoir plus sur la gestion des fonctionnalités](admin-feature-management.md).

- Assurez-vous que la fonctionnalité n’est pas masquée par la personnalisation. [En savoir plus sur la personnalisation](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot apparaît sur les pages, mais vous obtenez une erreur indiquant qu’il n’est pas activé

Lorsque vous essayez d’utiliser Copilot et que vous obtenez une erreur similaire à **Désolé, Copilot n’est pas activé pour \[fonctionnalité\]**, il y a quelques points à vérifier. :

- D'abord, vérifiez que la fonctionnalité est activée sur la page **Capacités de Copilot et de l’IA**. [En savoir plus sur l’activation des fonctionnalités Copilot et IA](enable-ai.md#activate-features). 
- Ensuite, assurez-vous que la déclaration de confidentialité pour l’intégration Azure OpenAI n’est pas définie sur **Je ne suis pas d’accord pour tout le monde**. Si tel est le cas, remplacez-le par **D’accord pour tout le monde**. [En savoir plus sur les avis de confidentialité](privacy-notices-status.md).

## <a name="copilot-capabilities-from-microsoft-not-listed-on-copilot--ai-capabilities-page"></a>Les capacités de Copilot de Microsoft ne sont pas répertoriées sur la page Fonctionnalités de Copilot et de l’IA

Si aucune des fonctions d’IA de Microsoft n’apparaît dans la page **Fonctionnalités de Copilot et de l’IA**, c’est probablement parce qu’une ou plusieurs applications intégrées sont installées dans votre environnement. Les applications intégrées peuvent offrir leurs propres fonctionnalités Copilot, mais les fonctionnalités publiées par Microsoft ne sont pas compatibles avec les environnements dotés d’applications intégrées.

## <a name="see-also"></a>Voir aussi

[Configuration des fonctionnalités de Copilot et d’IA](enable-ai.md)  
[Suggestions de textes marketing avec Copilot](ai-overview.md)  
[Rapprocher les comptes bancaires avec Copilot](bank-reconciliation-with-copilot.md)  
