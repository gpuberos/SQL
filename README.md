# SQL

Le langage de requête structuré (SQL : Structured Query Language) est un langage de programmation normalisé permettant de stocker et de traiter des informations dans une base de données relationnelle. Vous pouvez utiliser des instructions SQL pour stocker, mettre à jour, supprimer, rechercher et récupérer des informations de la base de données. Vous pouvez également utiliser le langage SQL pour maintenir et optimiser les performances de la base de données.

# Base de données

Une base de données est un ensemble d’informations stockées, accessibles et gérées à l’aide d’un système de gestion de base de données (SGBD).

Un **SGBD** est un système de gestion de base de données qui permet de stocker, d’organiser et de gérer des données dans une base de données. Les SGBD sont utilisés pour stocker des données dans des tables, qui peuvent être accessibles et reconstruites[^1] de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes.

Un **SGBDR** (système de gestion de base de données relationnelle) est un type de SGBD qui gère les relations entre les tables, c’est-à-dire qu’on peut définir des contraintes qui garantissent l’intégrité référentielle[^2] et fonctionnelle[^3] des données. Les SGBDR sont basés sur une théorie, qu’on appelle le modèle relationnel, qui consiste à stocker toutes les données dans des tables structurées (en colonnes), avec des relations qui lient les tables entre elles.

[^1]: Reconstruites de différentes manières, signifie que les données peuvent être organisées et présentées de différentes manières en fonction des besoins de l’utilisateur.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez reconstruire ces données de différentes manières pour répondre à différentes questions. Vous pouvez regrouper les données par client pour voir toutes les commandes qu’un client a passées, ou vous pouvez regrouper les données par commande pour voir tous les clients qui ont passé une commande particulière.

[^2]: L’intégrité référentielle est une situation dans laquelle pour chaque information d’une table A qui fait référence à une information d’une table B, l’information référencée existe dans la table B. En d’autres termes, elle garantit que les relations entre les tables sont cohérentes et que les données ne sont pas corrompues.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez définir une relation entre les deux tables en utilisant une clé étrangère. La clé étrangère ou FOREIGN KEY est une colonne dans la table des commandes qui fait référence à la table des clients. L’intégrité référentielle garantit que chaque commande est associée à un client existant dans la table des clients. Si un client est supprimé de la table des clients, toutes les commandes associées à ce client seront également supprimées ou mises à jour en conséquence 

[^3]: L’intégrité fonctionnelle est une contrainte qui garantit que les données stockées dans une base de données sont valides et conformes aux règles définies.  
Par exemple, si vous avez une table de clients, vous pouvez définir une contrainte qui garantit que chaque client a un identifiant unique. Si un utilisateur essaie d’insérer un client avec un identifiant qui existe déjà, la contrainte d’intégrité fonctionnelle empêchera l’insertion.

Il existe deux types de bases de données :
- les bases de données **relationnelles**.
- les bases de données **non relationnelles**, également appelées **NoSQL**.

La principale différence entre les deux types de bases de données réside dans la manière dont les données sont stockées. 

## Base de données relationnelle

Elles stockent les données dans des tables, qui peuvent être accessibles et reconstruites de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes représentant différents attributs de données et les diverses relations entre les valeurs de données.

## Bases de données non relationnelles (NoSQL)

Elles stockent les données au format clé-valeur, dans des documents, en colonnes, en graphiques ou autres. Elles sont davantage utilisées dans un contexte de quantité croissante de données, car elles permettent de stocker des données volumineuses et de les regrouper sur plusieurs machines afin de réduire les coûts de maintenance.

## Quelles bases de données utiliser dans un projet

Les bases de données relationnelles et non relationnelles ont chacune leurs avantages et inconvénients :

- Les **bases de données relationnelles** sont plus adaptées aux applications qui nécessitent une structure de données complexe et des requêtes complexes. Elles offrent une flexibilité et aident à analyser les données. 
- Les **bases de données non relationnelles**, en revanche, sont plus adaptées aux applications qui nécessitent une grande quantité de données et une évolutivité horizontale. Elles permettent de stocker des données volumineuses et de les regrouper sur plusieurs machines afin de réduire les coûts de maintenance.

Le choix entre les deux types de bases de données dépend des besoins de l’application. Si l’application nécessite une structure de données complexe et des requêtes complexes, une base de données relationnelle est plus adaptée. Si l’application nécessite une grande quantité de données et une évolutivité horizontale[^4], une base de données non relationnelle est plus adaptée.

[^4]: L’évolutivité horizontale est un concept informatique qui se réfère à la capacité d’un système à s’adapter à des charges de travail et des demandes utilisateur qui évoluent rapidement.  Par exemple, dans le contexte d’une base de données non relationnelle, l’évolutivité horizontale consiste à augmenter la capacité de performance du système en lui ajoutant des ressources du même type que celles qu’il possède déjà, comme des serveurs ou des instances. Cela permet une croissance quasi infinie, car il n’y a pratiquement aucune limite au nombre de machines pouvant être ajoutées 

### Performances

En ce qui concerne la vitesse de lecture et d’écriture, il est vrai que les bases de données NoSQL sont généralement plus rapides en lecture que les bases de données relationnelles, tandis que les bases de données relationnelles sont généralement plus rapides en écriture. Cependant, il est important de noter que la vitesse de lecture et d’écriture dépend de nombreux facteurs, tels que la taille de la base de données, le nombre de requêtes simultanées, la complexité des requêtes, etc.
