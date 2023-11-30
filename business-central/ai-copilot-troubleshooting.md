---
title: Résoudre les problèmes des fonctionnalités de Copilot et d’IA
description: Découvrez comment résoudre les problèmes courants que vous pourriez rencontrer lorsque vous travaillez avec les fonctionnalités Copilot et IA dans Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection: null
ms.date: 11/15/2023
ms.custom: bap-template
---
# Résoudre les problèmes des fonctionnalités de Copilot et d’IA

Copilot est une fonctionnalité basée sur l’IA de Business Central qui aide à diverses tâches telles que la rédaction de textes marketing et le rapprochement des comptes bancaires. Si vous rencontrez des problèmes avec Copilot ou d’autres fonctionnalités d’IA, cet article peut vous aider à identifier et à résoudre les problèmes courants.

## Copilot n’apparaît pas sur les pages

Si la fonctionnalité Copilot, telle que l’action **Rédiger avec Copilot** pour les suggestions de textes marketing ou l’action **Réconcilier avec Copilot** pour l’aide au rapprochement des comptes bancaires n’apparaît pas sur une page comme prévu, vérifiez les points suivants :

- Si la fonctionnalité est contrôlée sous Gestion des fonctionnalités, assurez-vous qu’elle est activée. [En savoir plus sur la gestion des fonctionnalités](admin-feature-management.md).

- Assurez-vous que la fonctionnalité n’est pas masquée par la personnalisation. [En savoir plus sur la personnalisation](ui-personalization-user.md).

## Copilot apparaît sur les pages, mais vous obtenez une erreur indiquant qu’il n’est pas activé

Lorsque vous essayez d’utiliser Copilot et que vous obtenez une erreur similaire à **Désolé, Copilot n’est pas activé pour \[fonctionnalité\]**, il y a quelques points à vérifier. :

- D'abord, vérifiez que la fonctionnalité est activée sur la page **Capacités de Copilot et de l’IA**. [En savoir plus sur l’activation des fonctionnalités Copilot et IA](enable-ai.md#activate-features). 
- Ensuite, assurez-vous que la déclaration de confidentialité pour l’intégration Azure OpenAI n’est pas définie sur **Je ne suis pas d’accord pour tout le monde**. Si tel est le cas, remplacez-le par **D’accord pour tout le monde**. [En savoir plus sur les avis de confidentialité](privacy-notices-status.md).

## Voir aussi

[Configurer les capacités Copilot et IA](enable-ai.md)  
[Suggestions de textes marketing avec Copilot](ai-overview.md)  
[Rapprocher les comptes bancaires avec Copilot](bank-reconciliation-with-copilot.md)  
