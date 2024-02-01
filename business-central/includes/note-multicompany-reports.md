---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Il était possible d’obtenir les données de diverses entreprises dans un seul rapport avec les services Web OData. Mais depuis la 2e vague de lancement 2021 de [!INCLUDE [prod_short](prod_short.md)], seul ODataV4 est pris en charge, ce qui ne permet pas n’exporter les données de plusieurs entreprises. La fonction **$expand** dans Power BI que vous pourriez considérer comme un autre moyen de créer un rapport multi-sociétés, ne peut pas non plus être utilisée. Elle créera une colonne avec le nom de l’entreprise, mais ne la remplira pas avec les données de l’entreprise après une actualisation.