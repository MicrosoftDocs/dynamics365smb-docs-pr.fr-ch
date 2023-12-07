---
title: FAQ sur l’assistant de rapprochement de compte bancaire (version préliminaire) avec Copilot
description: "Cette FAQ fournit des informations sur la technologie d’IA utilisée pour rapprocher les comptes bancaires et les relevés Business\_Central. Elle comprend également des éléments à prendre en compte et des détails clés sur la façon dont l’IA est utilisée, comment elle a été testée et évaluée, et toutes les limitations spécifiques."
ms.date: 11/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
---

# <a name="faq-for-bank-account-reconciliation-assist-preview-with-copilot"></a>FAQ sur l’assistant de rapprochement de compte bancaire (version préliminaire) avec Copilot

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Cette foire aux questions (FAQ) décrit l’impact de l’IA sur l’assistance Copilot pour le rapprochement des comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-bank-reconciliation-assist"></a>Qu’est-ce que l’assistant de rapprochement bancaire ?

Le rapprochement bancaire est une tâche comptable courante dans laquelle les organisations examinent leurs relevés de compte bancaire pour identifier les transactions qui doivent être enregistrées dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, cette tâche est utilisée pour identifier les frais bancaires périodiques ou les petites dépenses des employés. Cette tâche est généralement un processus en plusieurs étapes, commençant par l’importation des relevés bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)], puis la mise en correspondance des transactions avec les écritures comptables et la validation de nouvelles écritures comptables pour refléter toutes les transactions résiduelles qui n’étaient pas connues auparavant de vos livres comptables. Copilot dans [!INCLUDE[prod_short](includes/prod_short.md)] réduit les efforts manuels en faisant correspondre davantage de transactions et en suggérant des comptes du grand livre dans lesquels vous pouvez effectuer une validation. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Quelles sont les capacités de l’aide au rapprochement bancaire ?

Copilot fournit une assistance basée sur l’IA avec deux tâches distinctes : 

- Amélioration de la correspondance des transactions avec les écritures comptables 

   [!INCLUDE[prod_short](includes/prod_short.md)] propose des règles automatisées qui font automatiquement correspondre de nombreuses transactions bancaires avec les écritures du grand livre. Cependant, ces règles sont rigides et aboutissent souvent à de nombreuses transactions sans correspondance qui nécessitent chacune un contrôle manuel et une comparaison associée. Copilot utilise la technologie d’IA pour inspecter les transactions restantes et identifier davantage de correspondances, en fonction des dates, des montants et des descriptions. Par exemple, si plusieurs factures ont été payées en une seule fois par un client, Copilot rapproche la ligne de relevé bancaire unique avec les multiples écritures comptables des factures. 
 
- Comptes généraux suggérés 

   Pour les transactions bancaires résiduelles qui n’ont pu être mises en correspondance avec aucune écriture du grand livre, Copilot utilise la technologie d’IA pour comparer la description de la transaction avec les noms des comptes généraux, suggérant le compte général le plus probable pour effectuer la validation. Par exemple, Copilot pourrait suggérer que la transaction avec le descriptif « Fuel Stop24 » soit validée dans le compte « Transport ». 

Copilot ne se connecte pas à votre banque pour récupérer ou envoyer des transactions. Cette tâche reste entièrement sous votre contrôle et constitue une condition préalable pour commencer à utiliser l’assistance de Copilot, que ces transactions soient ajoutées à [!INCLUDE[prod_short](includes/prod_short.md)] via une connexion bancaire numérique, importée depuis un fichier de relevé bancaire ou saisie manuellement. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Quelle est l’utilisation prévue de l’assistance au rapprochement bancaire ?

L’assistance au rapprochement des comptes bancaires est conçue pour aider à identifier les nouvelles transactions que les clients doivent comptabiliser dans [!INCLUDE[prod_short](includes/prod_short.md)], pour améliorer la précision de leurs grands livres. Cette activité n’est pas destinée à détecter les fraudes ou à déterminer si les clients ont payé à temps.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Comment l’aide au rapprochement bancaire a-t-elle été évaluée ? Quelles mesures sont utilisées pour évaluer les performances ?

Cette fonctionnalité a été testée en utilisant des combinaisons de données de transactions bancaires synthétiques et de comptes généraux et d’écritures de grand livre similaires qui couvrent les variations typiques et les limites de données pour chaque champ et dans différentes langues. Les données de test représentent à la fois une utilisation typique et une utilisation par des acteurs malveillants. Les performances ont été mesurées par rapport au rapprochement manuel des mêmes données. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Quelles sont les limites de l’assistance au rapprochement bancaire ? Comment les utilisateurs peuvent-ils minimiser l’impact des limitations du rapprochement bancaire lors de l’utilisation du système ?

L’assistance au rapprochement des comptes bancaires fonctionne mieux lorsque les noms de comptes généraux, les descriptions d’écritures comptables et les descriptions de transactions bancaires sont tous dans la même langue. Les langues mixtes des descriptions de transactions entraînent souvent moins de correspondances et de suggestions. 

Les comptes du grand livre suggérés fonctionnent mieux en anglais. Bien que cette fonctionnalité puisse être utilisée dans toutes les langues [!INCLUDE[prod_short](includes/prod_short.md)] disponibles, les utilisateurs peuvent rencontrer moins de correspondances de transactions et moins de comptes généraux suggérés dans d’autres langues. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>Dans quelles zones géographiques et langues l’assistance au rapprochement bancaire est-elle disponible ?

Cette fonctionnalité est disponible dans n’importe quelle localisation de pays/région d’environnement et dans n’importe quelle langue d’utilisateur. Pour les environnements client situés dans des pays/régions où Azure OpenAI Service n’est pas déployé, les administrateurs doivent d’abord consentir à autoriser le déplacement des données au-delà des frontières pour que [!INCLUDE[prod_short](includes/prod_short.md)] se connecte à Azure OpenAI Service et que cette fonctionnalité soit disponible. 

Pour plus d’informations sur la langue, consultez la question précédente sur les limitations.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Qu’attend-on des utilisateurs finaux lors de l’exploitation d’une assistance au rapprochement des comptes bancaires ?

### <a name="while-using-bank-account-reconciliation"></a>Lors de l’utilisation du rapprochement bancaire

Les correspondances et suggestions basées sur l’IA peuvent parfois être incorrectes ou incomplètes. Les utilisateurs de l’assistance au rapprochement des comptes bancaires doivent vérifier l’exactitude des correspondances et des suggestions fournies par Copilot avant de choisir de les conserver. Les correspondances et suggestions de Copilot ne sont pas enregistrées dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)] tant que vous n’avez pas cliqué sur le bouton Conserver et quitté la fenêtre Copilot. Vous pouvez également modifier et corriger toute correspondance ou suggestion avant de choisir de la conserver. 

### <a name="after-completing-bank-account-reconciliation"></a>Après l’utilisation du rapprochement bancaire

Il est recommandé aux utilisateurs de vérifier également l’exactitude et de corriger toute divergence après avoir quitté la fenêtre Copilot, y compris les activités suivantes : 

- Consulter le rapport du test de rapprochement. 
- S’assurer que votre organisation dispose des processus d’examen et d’audit appropriés. 
- Rouvrir tous les rapprochements validés via la fonction Annuler. 
- Corriger toute écriture comptable erronée grâce à l’inversion de validation des écritures. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Qu’attend-on des administrateurs et utilisateurs finaux lors de l’exploitation d’une assistance au rapprochement des comptes bancaires ?

Les utilisateurs finaux, tels que les comptables, les trésoriers ou autres personnes travaillant sur la comptabilité d’entreprise, doivent toujours vérifier l’exactitude des correspondances et des suggestions fournies par Copilot avant de choisir de les conserver. Après le rapprochement avec Copilot, nous vous recommandons de consulter le rapport de test de rapprochement pour vérifier l’exactitude et identifier toute divergence. 

Les administrateurs doivent s’assurer que les utilisateurs comptables appropriés ont accès à cette fonctionnalité. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Copilot est-il le seul moyen de réaliser le rapprochement des comptes bancaires ?

Non – l’utilisation de Copilot est facultative. [!INCLUDE[prod_short](includes/prod_short.md)] offre des moyens traditionnels, non basés sur l’IA, d’importer des relevés bancaires, d’exécuter des règles de correspondance prédéfinies et d’appliquer manuellement les correspondances et la comptabilisation sur les comptes généraux appropriés. L’approche traditionnelle et Copilot peuvent être utilisées simultanément au sein d’une organisation. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Comment puis-je donner mon avis sur le contenu généré par l’IA ?

Chaque fois que Copilot propose des correspondances ou des suggestions, vous pouvez fournir des commentaires à Microsoft directement à partir de la fenêtre Copilot, en utilisant les commandes J’aime et Je n’aime pas. Vos commentaires restent anonymes et nous utilisons ces données afin d’évaluer et d’améliorer la qualité du service.


## <a name="see-also"></a>Voir aussi

[Rapprocher les comptes bancaires à l’aide de l’assistant de rapprochement bancaire (version préliminaire)](bank-reconciliation-with-copilot.md)
