---
title: Déplacement des données Copilot entre les zones géographiques
description: Découvrez comment les données utilisées dans les fonctionnalités de copilote dans Dynamics 365 Business Central se déplacent dans les zones géographiques où le service Azure OpenAI n’est pas disponible par défaut.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: null
ms.date: 11/30/2023
ms.custom: bap-template
---

# Déplacement des données Copilot entre des zones géographiques 

Copilot est disponible dans tous les supports pris en charge [Pays/régions Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Cependant, Copilot utilise le service Microsoft Azure OpenAI, actuellement disponible pour Business Central dans certaines régions géographiques uniquement. Cela signifie que si votre environnement est basé ailleurs, les données issues de Copilot et des fonctionnalités de l’IA générative doivent être transmises en dehors de votre région géographique et pourraient être traitées et stockées en dehors de votre limite de conformité. Parmi les données figurent les invites de l’IA et les données de votre entreprise utilisées ou générées par Copilot. Dans ce cas, vous devez vous autoriser le mouvement des données vers un compte Azure OpenAI Service dans une autre région. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Si votre environnement se trouve dans la même région Azure en tant que Service OpenAI Azure, il se connecte automatiquement à Azure OpenAI Service, il n’y a aucune option et aucune configuration unique n’est requise.

> [!NOTE]
> Les fonctionnalités individuelles de Copilot et de l’IA générative pourraient ne pas être disponibles dans toutes les pays/régions de l’environnement Business Central. Consultez l’éditeur de chaque fonctionnalité pour comprendre la disponibilité.
> 
> Les fonctionnalités de Copilot et de l’IA générative des éditeurs non Microsoft, telles que celles issues de personnalisations ou des applications AppSource que vous installez, définissent leurs propres régions Azure OpenAI Service desservies. Consultez l’éditeur de l’extension pour comprendre quels services Azure régionaux sont utilisés par l’extension. 

### Zones géographiques desservant Azure OpenAI Service

Le tableau suivant affiche la région Azure OpenAI Service utilisée par Copilot, selon le pays/région d’un environnement Business Central. Ces informations sont importantes pour décider d’accepter ou non le mouvement des données entre zones géographiques. Vous pouvez identifier le pays/région Azure de votre environnement dans le centre d’administration Business Central (voir [Gestion des environnements dans le centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Région Azure d’environnement| Zone géographique desservant Azure OpenAI Service|Action d’administrateur requise pour déverrouiller Copilot| 
| - | - | - |
|Asie (Est, Sud-Est) |États-Unis|Oui|
|Australie (Sud-Est)| États-Unis |Oui |
|Brésil (Sud) |États-Unis|Oui|
|Canada (Centre, Est)|États-Unis|Oui|
|Europe (Ouest, Nord)| Suède ou Suisse |Oui|
|France (Centre, Sud)| Suède ou Suisse |Oui|
|Allemagne (Nord, Centre-Ouest)| Suède ou Suisse |Oui|
|Inde (Centre, Sud)|États-Unis|Oui|
|Japon (Est, Ouest)|États-Unis|Oui|
|Corée (Centre, Sud)|États-Unis|Oui|
|Norvège (Est, Ouest)|Suède ou Suisse |Oui|
|Afrique du Sud (Nord, Ouest)|États-Unis|Oui|
|Suisse (Nord, Ouest) |Suède ou Suisse |Oui|
|Émirats arabes unis (Nord, Ouest)|États-Unis|Oui|
|Royaume-Uni (Sud, Ouest)|Royaume-Uni|Oui|
|États-Unis (Centre, Est, Centre-Nord, Centre-Sud, Ouest) |États-Unis|Non|

> [!NOTE]
> Une fois un Azure OpenAI Service disponible dans votre région Business Central, votre environnement passe automatiquement à l’utilisation d’Azure OpenAI Service et l’activation n’est pas requise, voire possible.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## Étapes suivantes

Vous choisissez d’autoriser le mouvement des données entre les régions à partir de la page [Capacités de Copilot et de l’IA](https://businesscentral.dynamics.com/?page=7775). Pour en savoir plus, consultez [Autoriser le déplacement des données entre régions](enable-ai.md#allow-data-movement-across-geographies).
