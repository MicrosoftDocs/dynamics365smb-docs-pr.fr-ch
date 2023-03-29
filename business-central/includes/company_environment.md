---
author: edupont04
ms.topic: include
ms.date: 04/01/2022
ms.author: edupont
---
Les utilisateurs [!INCLUDE[prod_short](prod_short.md)] prennent parfois en charge plusieurs services ou sous-organisations au sein d’une unité commerciale. Par exemple, une entreprise peut avoir des bureaux de vente dans différentes villes et plusieurs pays. Elle a donc créé un centre de profit pour chaque bureau. Les bureaux situés dans le même pays sont constitués en *sociétés* distinctes dans un *environnement* partagé. D’autres bureaux sont créés en tant que sociétés dans des environnements distincts car ils sont géographiquement basés dans d’autres pays.

- Qu’est-ce qu’une société ?

  Considérez une *société* en tant que conteneur contenant des informations sur une entité juridique. En utilisant l’exemple ci-dessus, l’entreprise a un bureau de vente à Seattle et un autre à New York, donc elle crée une société à [!INCLUDE[prod_short](prod_short.md)] pour chaque bureau afin qu’elle puisse gérer les opérations pour chaque bureau séparément.

- Qu’est-ce qu’un environnement ?

  Les sociétés dans [!INCLUDE[prod_short](prod_short.md)] Online existent dans ce que l’on appelle des *environnements*. Il existe deux types d’environnements, **Production** et **Sandbox**. En bref, les environnements de production contiennent des données métier en direct et les environnements sandbox sont utilisés comme un endroit sûr pour tester des choses comme de nouveaux processus ou fonctionnalités métier. Pour plus d’informations, voir [Types d’environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (en anglais uniquement). Si vous avez accès à une société, vous avez accès à l’environnement dans lequel elle se trouve. Si vous avez accès à plusieurs sociétés et que celles-ci se trouvent dans des environnements différents, lorsque vous vous connectez à [!INCLUDE[prod_short](prod_short.md)] vous devez spécifier l’environnement dans lequel vous souhaitez travailler. Les environnements sont particuliers à un pays donné, donc si votre organisation travaille dans plusieurs pays, vous avez besoin d’environnements distincts pour chaque pays. Pour plus d’informations, voir [Environnements et sociétés](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (en anglais uniquement).
