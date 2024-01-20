# SQL

Le langage de requête structuré (SQL : Structured Query Language) est un langage de programmation normalisé permettant de stocker et de traiter des informations dans une base de données relationnelle. Vous pouvez utiliser des instructions SQL pour stocker, mettre à jour, supprimer, rechercher et récupérer des informations de la base de données. Vous pouvez également utiliser le langage SQL pour maintenir et optimiser les performances de la base de données.

# Base de données

Une base de données est un ensemble d’informations stockées, accessibles et gérées à l’aide d’un système de gestion de base de données (SGBD).

Un **SGBD** est un système de gestion de base de données qui permet de stocker, d’organiser et de gérer des données dans une base de données. Les SGBD sont utilisés pour stocker des données dans des tables, qui peuvent être accessibles et reconstruites[^1] de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes.

Un **SGBDR** (système de gestion de base de données relationnelle) est un type de SGBD qui gère les relations entre les tables, c’est-à-dire qu’on peut définir des contraintes qui garantissent l’intégrité référentielle[^2] et fonctionnelle[^3] des données. Les SGBDR sont basés sur une théorie, qu’on appelle le modèle relationnel, qui consiste à stocker toutes les données dans des tables structurées (en colonnes), avec des relations qui lient les tables entre elles.

[^1]: Reconstruites de différentes manières, signifie que les données peuvent être organisées et présentées de différentes manières en fonction des besoins de l’utilisateur.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez reconstruire ces données de différentes manières pour répondre à différentes questions. Vous pouvez regrouper les données par client pour voir toutes les commandes qu’un client a passées, ou vous pouvez regrouper les données par commande pour voir tous les clients qui ont passé une commande particulière.

[^2]: L’intégrité référentielle est une situation dans laquelle pour chaque information d’une table A qui fait référence à une information d’une table B, l’information référencée existe dans la table B. En d’autres termes, elle garantit que les relations entre les tables sont cohérentes et que les données ne sont pas corrompues.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez définir une relation entre les deux tables en utilisant une clé étrangère. La clé étrangère ou FOREIGN KEY est une colonne dans la table des commandes qui fait référence à la table des clients. L’intégrité référentielle garantit que chaque commande est associée à un client existant dans la table des clients. Si un client est supprimé de la table des clients, toutes les commandes associées à ce client seront également supprimées ou mises à jour en conséquence.

[^3]: L’intégrité fonctionnelle est une contrainte qui garantit que les données stockées dans une base de données sont valides et conformes aux règles définies.  
Par exemple, si vous avez une table de clients, vous pouvez définir une contrainte qui garantit que chaque client a un identifiant unique. Si un utilisateur essaie d’insérer un client avec un identifiant qui existe déjà, la contrainte d’intégrité fonctionnelle empêchera l’insertion.

Il existe plusieurs types de bases de données, chacun ayant ses propres avantages et inconvénients. 
Les bases de données le plus couramment utilisées de nos jours :

| Type de base de données             |	Utilisation	                                                                                                    | Comment sont stockées les données                                                | Pour quel type d’usage                                                                          |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Bases de données relationnelles	    | - Stockage de données structurées <br> - transactions complexes <br> - requêtes ad hoc                          |	Les données sont stockées dans des tables                                        | Applications qui nécessitent une structure de données complexe et des requêtes complexes        |
| Bases de données orientées objet    |	- Stockage de données complexes et hiérarchiques <br> - relations complexes entre les données                   | Les données sont stockées sous forme d’objets et de classes                      | Applications qui nécessitent des données complexes et des relations complexes entre les données |
| Bases de données non relationnelles |	- Stockage de données non structurées et semi-structurées <br> - grande évolutivité <br> - grande disponibilité |	Les données sont stockées sous forme de documents, de graphes, de colonnes, etc. | Applications qui nécessitent une grande quantité de données et une évolutivité horizontale      |

La principale différence entre les types de bases de données réside dans la manière dont les données sont stockées. 

## Bases de données relationnelles

- Elles sont plus courantes, les données sont stockées dans des tables qui peuvent être accessibles et reconstruites de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes représentant différents attributs de données et les diverses relations entre les valeurs de données.  
- Elles sont adaptées pour stocker des données structurées[^4], telles que les données financières, les données de vente, les données de production, etc. Elles sont également très utiles pour stocker des données qui ont des relations complexes entre elles, telles que les données de commande et les données de facturation.  
- Elles offrent une flexibilité et aident à analyser les données.

[^4]: Les données structurées sont des données organisées selon un format prédéfini, telles que les données stockées dans une base de données relationnelle.

## Bases de données objet

- Elles sont plus récentes, elles regroupent des paquets de données très proches pour former un objet. Les données sont interrogeables par ensemble, ce qui permet d’avoir toutes les informations immédiatement disponibles. Les objets peuvent inclure des méthodes et exécuter des actions spécifiques. Les objets sont regroupés en classes, qui engendrent une hiérarchie entre classes et sous-classes. Les sous-classes adoptent les propriétés des classes du niveau supérieur et les complètent avec leurs propres attributs. Les objets d’une classe peuvent aussi être liés simultanément à une autre classe. Cette hiérarchie forte s’en retrouve affaiblie au profit de la création d’une interconnexion. Les objets simples se regroupent en objets complexes.  
- Elles sont adaptées pour stocker des données complexes et hiérarchiques, telles que les données de configuration, les données de modélisation, les données de simulation, etc.  
- Également très utiles pour stocker des données géospatiales, telles que les cartes, les images satellites, les données topographiques, etc.

## Bases de données non relationnelles (NoSQL)

- Elles stockent les données au format clé-valeur, dans des documents, en colonnes, en graphiques ou autres. Elles sont davantage utilisées dans un contexte de quantité croissante de données, car elles permettent de stocker des données volumineuses et de les regrouper sur plusieurs machines afin de réduire les coûts de maintenance.  
- Elles sont adaptées pour stocker des données non structurées[^5] et semi-structurées[^6], telles que les données multimédias, les données géospatiales, les données de Big Data, etc. Elles sont également très utiles pour les applications qui nécessitent une grande quantité de données et une évolutivité horizontale[^7] et une grande disponibilité.

[^5]: Les données non structurées, en revanche, sont des données qui ne sont pas organisées selon un format prédéfini, telles que les e-mails, les posts sur les réseaux sociaux, les présentations, les chats, etc. Les données non structurées représentent la majorité des données dans le monde aujourd’hui.
[^6]: Les données semi-structurées sont un mélange de données structurées et non structurées. Elles ont une structure définie, mais ne sont pas conformes à un schéma de données rigide. Les données semi-structurées sont souvent utilisées pour stocker des données complexes, telles que les données XML et JSON.
[^7]: L’évolutivité horizontale est un concept informatique qui se réfère à la capacité d’un système à s’adapter à des charges de travail et des demandes utilisateur qui évoluent rapidement.  
Par exemple, dans le contexte d’une base de données non relationnelle, l’évolutivité horizontale consiste à augmenter la capacité de performance du système en lui ajoutant des ressources du même type que celles qu’il possède déjà, comme des serveurs ou des instances. Cela permet une croissance quasi infinie, car il n’y a pratiquement aucune limite au nombre de machines pouvant être ajoutées.

## Quelles bases de données utiliser dans un projet

Les bases de données relationnelles, objet et non relationnelles ont chacune leurs avantages et inconvénients :

| Type de base de données              | Avantages                                                                                     | Inconvénients                                                                     |
| ------------------------------------ | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Bases de données relationnelles      | - Stockage de données structurées <br> - Transactions complexes <br> - Requêtes ad hoc[^8]    | - Difficiles à mettre à l’échelle <br> - Pas adaptées aux données non structurées |
| Bases de données orientées objet     | - Stockage de données complexes et hiérarchiques <br> - Relations complexes entre les données | - Pas adaptées aux données non structurées <br> - Peu courantes                   |
| Bases de données non relationnelles  | - Grande évolutivité <br> - Grande disponibilité <br> - Adaptées aux données non structurées  | - Peu adaptées aux transactions complexes <br> - Peu adaptées aux requêtes ad hoc |

[^8]: Une requête ad hoc est une requête SQL qui est écrite pour une utilisation unique.  
Elle est généralement utilisée pour extraire des données spécifiques d’une base de données qui ne sont pas incluses dans les rapports standard. Les requêtes ad hoc sont souvent utilisées pour répondre à des questions spécifiques ou pour résoudre des problèmes spécifiques. Par exemple, si vous voulez savoir combien de clients ont acheté un produit spécifique au cours des 30 derniers jours, vous pouvez écrire une requête ad hoc pour extraire ces informations de la base de données.

### Performances

Les performances d’écriture et de lecture diffèrent en fonction de leur structure de stockage de données :
- Les bases de données **relationnelles** stockent les données dans des tables, ce qui peut ralentir les performances d’écriture et de lecture pour les applications qui nécessitent une grande quantité de données. 
- Les bases de données **orientées objet** stockent les données sous forme d’objets et de classes, ce qui peut améliorer les performances d’écriture et de lecture pour les applications qui nécessitent des données complexes et hiérarchiques.
- Les bases de données **non relationnelles** stockent les données sous forme de documents, de graphes, de colonnes, etc., ce qui peut améliorer les performances d’écriture et de lecture pour les applications qui nécessitent une grande évolutivité et une grande disponibilité.
  
> [!IMPORTANT]
> La vitesse de lecture et d’écriture dépend de nombreux facteurs, tels que la taille de la base de données, le nombre de requêtes simultanées, la complexité des requêtes, etc.
