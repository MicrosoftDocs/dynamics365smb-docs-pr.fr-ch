---
title: "Business\_Central pour les organisations multisites et internationales | Microsoft Docs"
description: "Business\_Central fournit des fonctions qui prennent en charge un modèle d′entreprise en étoile."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# <a name="business-central-for-multi-site-and-international-organizations"></a><a name="business-central-for-multi-site-and-international-organizations"></a><a name="business-central-for-multi-site-and-international-organizations"></a>Business Central pour les organisations multisites et internationales
Les organisations qui ont plusieurs sites utilisent souvent un modèle commercial en étoile dans lequel une société mère, ou siège social, gère les opérations globales de l′entreprise tandis que chaque site fonctionne comme une entité unique et autonome. Les sites sont souvent répartis géographiquement et ont des besoins différents en matière de partage d′informations avec le siège social. De plus, les sites n′ont généralement pas besoin du même niveau de complexité et manquent souvent des ressources nécessaires pour conserver un système volumineux.

[!INCLUDE[prod_short](includes/prod_short.md)] offre aux petites et moyennes entreprises une solution de gestion d′entreprise facile à utiliser et à entretenir à un faible coût de possession.

Cet article présente certaines façons où [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge un modèle d′entreprise en étoile.

## <a name="integrating-the-headquarter-company-and-the-sites"></a><a name="integrating-the-headquarter-company-and-the-sites"></a><a name="integrating-the-headquarter-company-and-the-sites"></a>Intégration du siège social et des sites

[!INCLUDE[prod_short](includes/prod_short.md)] peut s′intégrer au système comptable du siège social tout en répondant aux besoins variés des différents sites, quels que soient la taille, l′emplacement ou le type d′activité.

Le schéma suivant est un exemple de différents sites intégrés à un siège social.

![Description du diagramme générée automatiquement.](media/multisite-headquarter-sites.png)

## <a name="meet-the-needs-of-domestic-and-international-sites"></a><a name="meet-the-needs-of-domestic-and-international-sites"></a><a name="meet-the-needs-of-domestic-and-international-sites"></a>Répondre aux besoins des sites nationaux et internationaux

Les besoins commerciaux des sites diffèrent souvent selon le secteur, les méthodes commerciales ou les relations avec le siège social. [!INCLUDE[prod_short](includes/prod_short.md)] peut être facilement adapté et étendu pour différents types d′entreprises et de paramètres régionaux. Microsoft AppSource offre une multitude d′applications Microsoft et partenaires, et les partenaires peuvent déployer rapidement [!INCLUDE[prod_short](includes/prod_short.md)] avec une perturbation minimale des opérations quotidiennes.

Pour les organisations multinationales, [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les exigences légales et les pratiques commerciales locales.

* Pour les versions en ligne, il existe plus de [40 versions nationales localisées](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) que vous pouvez installer en tant qu′extensions à partir de Microsoft AppSource.  
* Pour les versions sur site, des [versions nationales](/azure/architecture/solution-ideas/articles/business-central) sont disponibles sous forme de versions localisées par Microsoft ou de localisations complémentaires dirigées par des partenaires.

Un réseau de plus de 4 000 partenaires Microsoft dans le monde fournit une expertise locale.

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Adaptez le système à l′entreprise. | Profitez d′un système conçu dès le départ pour les entreprises moyennes. | [Aperçu](https://dynamics.microsoft.com/business-central/overview/) |
| Respectez les pratiques réglementaires et locales. | Conformez-vous aux exigences légales et aux pratiques commerciales locales. | [Fonctionnalités locales](about-localization.md) |
| Accédez à plusieurs entreprises à partir d′une seule page. | Accédez rapidement à n′importe quelle entreprise Business Central de votre organisation. | [Hub Entreprise](ui-extensions-company-hub.md) |
| Gérez plusieurs langues et devises. | La prise en charge de plusieurs langues et devises permet de répondre aux besoins locaux. | [Fonctions multilingues](about-locale-language.md)<br></br>[Fonctions multi-devises](finance-how-setup-additional-currencies.md) |


## <a name="consolidate-financial-data"></a><a name="consolidate-financial-data"></a><a name="consolidate-financial-data"></a>Consolidation des données financières

Une facette fondamentale du modèle commercial en étoile est la capacité pour le siège social et les sites d′échanger des données financières, même lorsque le siège social et les sites utilisent des systèmes, des structures comptables, des langues et des devises différents.

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Consolidez les données financières des sites. | Consolidez les états financiers des sites, qu′ils exécutent Business Central ou une autre application, en une seule entité commerciale (société). | [Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md) |
| Intégrez les structures comptables. | Transférez les données de consolidation de différentes structures comptables vers les vôtres. Format de fichier intégré pour F&O (disponible avec la deuxième vague de publication 2020) | [Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)<br></br>[Préparer les comptes généraux pour la consolidation](finance-consolidated-company-reporting-setup.md#glacc) |
| Effectuez des transactions dans plusieurs devises. | Assurez-vous que les états financiers dans différentes devises sont exacts et utilisent des taux de change corrects. | [Mettre à jour des taux de change devise](finance-how-update-currencies.md) |

## <a name="share-business-insight-with-integrated-analytics"></a><a name="share-business-insight-with-integrated-analytics"></a><a name="share-business-insight-with-integrated-analytics"></a>Partage de Business Insight avec Integrated Analytics

Alignez l′organisation avec vos objectifs commerciaux en offrant une compréhension commune de la réalité actuelle. L′analyse intégrée peut aider les gens à fonder leurs décisions sur le même ensemble de faits.

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Partagez des informations avec les sites sans support informatique étendu. | Créez des KPI et des tableaux de bord Business Intelligence dans Power BI basés sur vos données. | [Utiliser des données Business Central dans Power BI](across-working-with-business-central-in-powerbi.md) |
| Développez des états financiers personnalisés. | Générez des états financiers basés sur des paramètres. | [Veille économique](bi.md) |
| Alignez-vous sur les faits. | Générez, visualisez et partagez des états avec les parties prenantes internes et externes. | [États financiers](finance-reports.md) |
| Analysez les données dans Excel. | Recherchez des faits, dépannez et effectuer des analyses ad hoc dans Microsoft Excel. | [Analyser les états financiers dans Excel](finance-analyze-excel.md) |


## <a name="exchange-data-using-apis-and-xmlports"></a><a name="exchange-data-using-apis-and-xmlports"></a><a name="exchange-data-using-apis-and-xmlports"></a>Échange de données à l′aide des API et des XMLports

Les API et les XMLports simplifient le processus de connexion des instances de [!INCLUDE[prod_short](includes/prod_short.md)], y compris celles qui ont été personnalisées pour chaque site.

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Connectez les versions personnalisées entre les sites et le siège social. | Les pages API peuvent exposer n′importe quelle représentation d′une entité, y compris ses personnalisations. | [Activation des API pour Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Gestion des versions et sécurité. | Les API utilisent ODataV4, qui fournit la gestion des versions, les webhooks et le suivi des modifications. | [Sécurité et protection](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Validez et importez des documents XML. | Les codeunits peuvent être exposés en tant qu′actions indépendantes pour prendre en charge la validation et l′ingestion de documents XML. Pour traiter des documents XML, des XMLports peuvent être appliqués. Les actions indépendantes sont également capables de générer un document XML ou JSON. | [Objets XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Facilitez la maintenance grâce à l′échange de données électroniques. | Une solution d′échange de données électroniques peut être ajoutée pour servir de couche d′intégration entre le siège social et les sites. | [Data Exchange Framework](across-about-the-data-exchange-framework.md) |
| Échangez des données entre différents systèmes. | Utilisez des XMLports pour créer des documents XML, qui peuvent ensuite être échangés entre un siège social qui utilise un système et des sites qui utilisent Business Central. | [Vue d’ensemble de XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Administrez des échanges de données complexes. | Utilisez une combinaison de XMLports avec Business Central et le serveur Microsoft BizTalk pour répondre aux besoins uniques de vos sites.</br>Pour les besoins complexes, utilisez une solution d′échange de données électroniques basée sur le serveur BizTalk et Commerce Gateway dans Business Central en association avec les XMLports. | [Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md) |
| Connectez-vous aux services et solutions tiers<sup></sup>. | Les API établissent une connexion point à point entre Business Central et les services et solutions tiers<sup></sup>. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## <a name="promote-an-efficient-intercompany-supply-chain"></a><a name="promote-an-efficient-intercompany-supply-chain"></a><a name="promote-an-efficient-intercompany-supply-chain"></a>Promotion d′une chaîne d′approvisionnement intersociétés efficace

Les sites ont souvent besoin d′un accès à la chaîne d′approvisionnement et des fonctions pour en gérer certains aspects. Par exemple, les sites peuvent utiliser le même fournisseur, mais gérer leurs actifs et leurs emplacements physiques séparément.

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Traitez les transactions inter-divisions comme des transactions de vente et d′achat normales. | Utilisez les validations intersociétés pour créer des documents de vente et d′achat et des écritures comptables pour des flux entiers et pour plusieurs sociétés à la fois afin d′éliminer l′écriture de données en double. | [Gestion des transactions intersociétés](intercompany-manage.md) |
| Utilisez des processus sans papier. | Évitez les frais d′envoi, de réception et d′impression des documents. | [Documents entrants](across-income-documents.md)<br><br> [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md) |

## <a name="respond-quickly-to-new-business-conditions"></a><a name="respond-quickly-to-new-business-conditions"></a><a name="respond-quickly-to-new-business-conditions"></a>Réaction rapide aux nouvelles conditions commerciales

Le siège social doit être en mesure de réagir rapidement face aux changements commerciaux sur chaque site. En combinaison avec Power Automate, [!INCLUDE[prod_short](includes/prod_short.md)] peut servir de mécanisme d’alerte précoce.

![Capture d′écran d′une description de publication sur les réseaux sociaux générée automatiquement.](media/multisite-apps.png)

| **Exigence commerciale** | **Comment Business Central la prend en charge** | **En savoir plus** |
|-------------------------|-------------------------|-------------------------|
| Générez automatiquement des alertes par e-mail. | Configurez des alertes dans Power Automate qui envoie des e-mails pour vous informer des conditions métier critiques sur les sites ou chez les partenaires de la chaîne d′approvisionnement. | [Business Central et Power BI](admin-powerbi.md) |
| Utilisez des alertes standard ou personnalisées. | Utilisez 12 modèles différents inclus pour Business Central ou configurez vos propres alertes en fonction de votre entreprise. | [Utiliser Business Central dans un flux automatisé](across-how-use-financials-data-source-flow.md) |

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
