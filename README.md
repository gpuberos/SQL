# SQL

Le langage de requête structuré (SQL : Structured Query Language) est un langage de programmation normalisé permettant de stocker et de traiter des informations dans une base de données relationnelle. Vous pouvez utiliser des instructions SQL pour stocker, mettre à jour, supprimer, rechercher et récupérer des informations de la base de données. Vous pouvez également utiliser le langage SQL pour maintenir et optimiser les performances de la base de données.

# Base de données

## Qu'est-ce que c'est ?

Une base de données est un ensemble organisé de données stockées de manière structurée, permettant de stocker, gérer et récupérer facilement des informations. Les bases de données sont utilisées pour stocker des données de manière à ce qu'elles puissent être rapidement et facilement accessibles, gérées et mises à jour à l’aide d’un système de gestion de base de données (SGBD). Les bases de données sont largement utilisées dans les applications informatiques, les sites web et de nombreux autres domaines pour stocker et gérer efficacement les informations.

## Dans quels buts ?

1. **Stockage de données structurées** : Les bases de données permettent de stocker des données de manière structurée, ce qui facilite l'organisation et la récupération des informations. Par exemple, une entreprise peut utiliser une base de données pour stocker les informations des clients, telles que les noms, adresses et historiques d'achats.
2. **Manipulation efficace des données** : Les bases de données facilitent la recherche, la mise à jour et la suppression rapides des données. Par exemple, un site de commerce électronique peut utiliser une base de données pour gérer son inventaire, permettant aux utilisateurs de rechercher des produits, d'ajouter des articles à leur panier, et de passer des commandes de manière efficace.
3. **Conservation de l'intégrité des données** : Les bases de données offrent des mécanismes pour garantir l'intégrité des données, évitant ainsi les incohérences. Par exemple, une banque peut utiliser une base de données pour stocker les informations des comptes clients et s'assurer que les transactions financières sont effectuées de manière précise et sans erreurs.

## Système de gestion de base de données (SGBD)

Un **SGBD** est un système de gestion de base de données qui permet de stocker, d’organiser et de gérer des données dans une base de données. Les SGBD sont utilisés pour stocker des données dans des tables, qui peuvent être accessibles et reconstruites[^1] de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes.

Un **SGBDR** (système de gestion de base de données relationnelle) est un type de SGBD qui gère les relations entre les tables, c’est-à-dire qu’on peut définir des contraintes qui garantissent l’intégrité référentielle[^2] et fonctionnelle[^3] des données. Les SGBDR sont basés sur une théorie, qu’on appelle le modèle relationnel, qui consiste à stocker toutes les données dans des tables structurées (en colonnes), avec des relations qui lient les tables entre elles.

[^1]: Reconstruites de différentes manières, signifie que les données peuvent être organisées et présentées de différentes manières en fonction des besoins de l’utilisateur.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez reconstruire ces données de différentes manières pour répondre à différentes questions. Vous pouvez regrouper les données par client pour voir toutes les commandes qu’un client a passées, ou vous pouvez regrouper les données par commande pour voir tous les clients qui ont passé une commande particulière.

[^2]: L’intégrité référentielle est une situation dans laquelle pour chaque information d’une table A qui fait référence à une information d’une table B, l’information référencée existe dans la table B. En d’autres termes, elle garantit que les relations entre les tables sont cohérentes et que les données ne sont pas corrompues.  
Par exemple, si vous avez une table de clients et une table de commandes, vous pouvez définir une relation entre les deux tables en utilisant une clé étrangère. La clé étrangère ou FOREIGN KEY est une colonne dans la table des commandes qui fait référence à la table des clients. L’intégrité référentielle garantit que chaque commande est associée à un client existant dans la table des clients. Si un client est supprimé de la table des clients, toutes les commandes associées à ce client seront également supprimées ou mises à jour en conséquence.

[^3]: L’intégrité fonctionnelle est une contrainte qui garantit que les données stockées dans une base de données sont valides et conformes aux règles définies.  
Par exemple, si vous avez une table de clients, vous pouvez définir une contrainte qui garantit que chaque client a un identifiant unique. Si un utilisateur essaie d’insérer un client avec un identifiant qui existe déjà, la contrainte d’intégrité fonctionnelle empêchera l’insertion.

## Les types de bases de données les plus couramment utilisées

Il existe plusieurs types de bases de données, chacun ayant ses propres avantages et inconvénients.  
La principale différence entre les types de bases de données réside dans la manière dont les données sont stockées. 

| Type de base de données             |	Utilisation	                                                                                                    | Comment sont stockées les données                                                | Pour quel type d’usage                                                                          |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Bases de données relationnelles	    | - Stockage de données structurées <br> - transactions complexes <br> - requêtes ad hoc                          |	Les données sont stockées dans des tables                                        | Applications qui nécessitent une structure de données complexe et des requêtes complexes        |
| Bases de données orientées objet    |	- Stockage de données complexes et hiérarchiques <br> - relations complexes entre les données                   | Les données sont stockées sous forme d’objets et de classes                      | Applications qui nécessitent des données complexes et des relations complexes entre les données |
| Bases de données non relationnelles |	- Stockage de données non structurées et semi-structurées <br> - grande évolutivité <br> - grande disponibilité |	Les données sont stockées sous forme de documents, de graphes, de colonnes, etc. | Applications qui nécessitent une grande quantité de données et une évolutivité horizontale      |

### Bases de données relationnelles

- Elles sont plus courantes, les données sont stockées dans des tables qui peuvent être accessibles et reconstruites de différentes manières, et qui sont elles-mêmes composées de lignes et de colonnes représentant différents attributs de données et les diverses relations entre les valeurs de données.  
- Elles sont adaptées pour stocker des données structurées[^4], telles que les données financières, les données de vente, les données de production, etc. Elles sont également très utiles pour stocker des données qui ont des relations complexes entre elles, telles que les données de commande et les données de facturation.  
- Elles offrent une flexibilité et aident à analyser les données.

[^4]: Les données structurées sont des données organisées selon un format prédéfini, telles que les données stockées dans une base de données relationnelle.

### Bases de données objet

- Elles sont plus récentes, elles regroupent des paquets de données très proches pour former un objet. Les données sont interrogeables par ensemble, ce qui permet d’avoir toutes les informations immédiatement disponibles. Les objets peuvent inclure des méthodes et exécuter des actions spécifiques. Les objets sont regroupés en classes, qui engendrent une hiérarchie entre classes et sous-classes. Les sous-classes adoptent les propriétés des classes du niveau supérieur et les complètent avec leurs propres attributs. Les objets d’une classe peuvent aussi être liés simultanément à une autre classe. Cette hiérarchie forte s’en retrouve affaiblie au profit de la création d’une interconnexion. Les objets simples se regroupent en objets complexes.  
- Elles sont adaptées pour stocker des données complexes et hiérarchiques, telles que les données de configuration, les données de modélisation, les données de simulation, etc.  
- Également très utiles pour stocker des données géospatiales, telles que les cartes, les images satellites, les données topographiques, etc.

### Bases de données non relationnelles (NoSQL)

- Elles stockent les données au format clé-valeur, dans des documents, en colonnes, en graphiques ou autres. Elles sont davantage utilisées dans un contexte de quantité croissante de données, car elles permettent de stocker des données volumineuses et de les regrouper sur plusieurs machines afin de réduire les coûts de maintenance.  
- Elles sont adaptées pour stocker des données non structurées[^5] et semi-structurées[^6], telles que les données multimédias, les données géospatiales, les données de Big Data, etc. Elles sont également très utiles pour les applications qui nécessitent une grande quantité de données et une évolutivité horizontale[^7] et une grande disponibilité.

[^5]: Les données non structurées, en revanche, sont des données qui ne sont pas organisées selon un format prédéfini, telles que les e-mails, les posts sur les réseaux sociaux, les présentations, les chats, etc. Les données non structurées représentent la majorité des données dans le monde aujourd’hui.
[^6]: Les données semi-structurées sont un mélange de données structurées et non structurées. Elles ont une structure définie, mais ne sont pas conformes à un schéma de données rigide. Les données semi-structurées sont souvent utilisées pour stocker des données complexes, telles que les données XML et JSON.
[^7]: L’évolutivité horizontale est un concept informatique qui se réfère à la capacité d’un système à s’adapter à des charges de travail et des demandes utilisateur qui évoluent rapidement.  
Par exemple, dans le contexte d’une base de données non relationnelle, l’évolutivité horizontale consiste à augmenter la capacité de performance du système en lui ajoutant des ressources du même type que celles qu’il possède déjà, comme des serveurs ou des instances. Cela permet une croissance quasi infinie, car il n’y a pratiquement aucune limite au nombre de machines pouvant être ajoutées.

## Quelles bases de données utiliser dans un projet ?

Les bases de données relationnelles, objet et non relationnelles ont chacune leurs avantages et inconvénients :

| Type de base de données              | Avantages                                                                                     | Inconvénients                                                                     |
| ------------------------------------ | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Bases de données relationnelles      | - Stockage de données structurées <br> - Transactions complexes <br> - Requêtes ad hoc[^8]    | - Difficiles à mettre à l’échelle <br> - Pas adaptées aux données non structurées |
| Bases de données orientées objet     | - Stockage de données complexes et hiérarchiques <br> - Relations complexes entre les données | - Pas adaptées aux données non structurées <br> - Peu courantes                   |
| Bases de données non relationnelles  | - Grande évolutivité <br> - Grande disponibilité <br> - Adaptées aux données non structurées  | - Peu adaptées aux transactions complexes <br> - Peu adaptées aux requêtes ad hoc |

[^8]: Une requête ad hoc est une requête SQL qui est écrite pour une utilisation unique.  
Elle est généralement utilisée pour extraire des données spécifiques d’une base de données qui ne sont pas incluses dans les rapports standard. Les requêtes ad hoc sont souvent utilisées pour répondre à des questions spécifiques ou pour résoudre des problèmes spécifiques.  
Par exemple, si vous voulez savoir combien de clients ont acheté un produit spécifique au cours des 30 derniers jours, vous pouvez écrire une requête ad hoc pour extraire ces informations de la base de données.

### Performances

Les performances d’écriture et de lecture diffèrent en fonction de leur structure de stockage de données :
- Les bases de données **relationnelles** stockent les données dans des tables, ce qui peut ralentir les performances d’écriture et de lecture pour les applications qui nécessitent une grande quantité de données. 
- Les bases de données **orientées objet** stockent les données sous forme d’objets et de classes, ce qui peut améliorer les performances d’écriture et de lecture pour les applications qui nécessitent des données complexes et hiérarchiques.
- Les bases de données **non relationnelles** stockent les données sous forme de documents, de graphes, de colonnes, etc., ce qui peut améliorer les performances d’écriture et de lecture pour les applications qui nécessitent une grande évolutivité et une grande disponibilité.
  
> [!IMPORTANT]
> La vitesse de lecture et d’écriture dépend de nombreux facteurs, tels que la taille de la base de données, le nombre de requêtes simultanées, la complexité des requêtes, etc.

## Les types de données

Liste exhaustive des types de données les plus couramment utilisés :  

1. `VARCHAR(size)` : Utilisé pour stocker des chaînes de caractères de longueur variable.  
*Exemple : VARCHAR(50) peut stocker une chaîne de caractères jusqu'à 50 caractères, comme un nom.*
3. `CHAR(size)` : Similaire à VARCHAR, mais avec une longueur fixe.  
*Exemple : CHAR(10) peut stocker une chaîne de caractères de 10 caractères, et si la chaîne est plus courte, elle est remplie d'espaces.*
5. `INT` : Utilisé pour stocker des nombres entiers.  
*Exemple : INT peut stocker des nombres entiers tels que 1, 100, -500.*
6. `DECIMAL(size, d)` : Utilisé pour stocker des nombres décimaux avec une précision spécifique.  
*Exemple : DECIMAL(5, 2) peut stocker un nombre comme 123.45 avec une précision de deux décimales.*
7. `FLOAT` : Utilisé pour stocker des nombres décimaux (à virgule flottante).  
*Exemple : FLOAT peut stocker des nombres décimaux comme 3.14, -0.005.*
8. `BOOLEAN` : Utilisé pour stocker des valeurs de vérité (TRUE/FALSE ou 1/0).  
*Exemple : BOOLEAN peut être utilisé pour indiquer si un utilisateur est connecté (TRUE) ou déconnecté (FALSE).*
9. `DATE` : Utilisé pour stocker des dates.  
*Exemple : DATE peut stocker une date telle que '2024-01-20', 'AAAA-MM-JJ'.*

> [!IMPORTANT]
> La longueur d’une chaîne de caractères dans MySQL est définie en octets. Pour un type de données `VARCHAR`, vous pouvez définir la longueur de la chaîne en utilisant le paramètre `n`.
> La longueur de la chaîne de caractères **“Découverte de SQL”** est de 18 caractères.  
> Si vous utilisez l’encodage UTF-8, chaque caractère peut compter pour plus d’un octet.  
> Par exemple, le caractère `é` peut compter pour deux octets.

> [!TIP]
> Si vous souhaitez plus de types de données, n'hésitez pas à consulter le site [developpement-informatique.com](https://developpement-informatique.com/article/282/types-de-donnees-sql).

## Prérequis environnement de travail MySQL

### Modification des variables d'environnement système de Windows 11

1. Dans rechercher saisissez `Modifier les variables d'environnement`
2. Dans la fenêtre Propiétés système, cliquez sur le bouton `Variables d'environnement...`
3. Dans la fenêtre Variables d'environnement, double cliquez sur `Path`
4. Dans la fenêtre Modifier la variable d'environnement, cliquez sur nouveau et collez le chemin suivant `C:\wamp64\bin\mysql\mysql8.2.0\bin` puis cliquez sur `OK`
5. Redémarrez votre micro-ordinateur.

![Modifier les variables d'environnement](/assets/img/variables-environnement.webp)

### Vérification de l'état des services
Si vous êtes sous Windows 11 et que vous utilisez **[WampServer](https://wampserver.aviatechno.net/)** :

Pour vérifier que le service wampmysql64 est bien lancé : 
1. Clic droit sur l'icône de wampserver dans la barre d'état système.
2. Cliquez sur Outils > Vérifier l'état des services.
3. La fenêtre Administrateur : State of services doit afficher `The service 'wampmysqld64' is started`.

![WampServer MySQL Service Status](/assets/img/wampserver-mysqlservice.webp)

### Activation de l'UTF-8 de manière globale sur le serveur MySQL

> [!WARNING]
> **Correctif** pour la limitation du nombre de caractères au niveau de VARCHAR() sous Windows 11. Nécessite la version MySQL 8.2.0.  
> Modifier votre fichier à l'aide de l'application Bloc-notes `my.ini` en ajoutant à la suite de `port=3306` (en fin de fichier), les lignes `character_set_server=utf8` et `collation_server=utf8_general_ci`.  
> Par défaut le chemin d'accès est : `C:\wamp64\bin\mysql\mysql8.2.0\my.ini`.
> ```
> [mysqld]
> port=3306
> character_set_server=utf8
> collation_server=utf8_general_ci
> ```

> [!NOTE]
> Les lignes suivantes dans WampServer définissent le jeu de caractères et la collation pour le serveur MySQL. Le jeu de caractères définit l’ensemble de caractères utilisé pour stocker les données, tandis que la collation définit les règles de tri et de comparaison des données. Dans ce cas, le jeu de caractères est défini sur `utf8`, qui est un jeu de caractères Unicode qui prend en charge la plupart des langues du monde, et la collation est définie sur `utf8_general_ci `, qui est une collation qui prend en charge la comparaison insensible à la casse pour les caractères Unicode.

## Connexion au serveur MySQL

Le système de gestion de bases de données pour SQL s'appelle mysql.

1. Ouvrez un terminal (cmd)
```
Microsoft Windows [version 10.0.22631.3007]
(c) Microsoft Corporation. Tous droits réservés.

C:\>
```
2. Pour connaître notre version de mysql :

```
C:\>mysql --version
mysql  Ver 8.2.0 for Win64 on x86_64 (MySQL Community Server - GPL)
```

3. Connectez-vous au serveur MySQL via la commande suivante :

```
C:\>mysql -u root -p
```
Les paramètres suivants correspondent à :
- `-u` : User (Utilisateur)
- `-p` : Password (Mot de passe)

Saisissez votre mot de passe pour pouvoir vous connecter :
```
Enter password:
```

Une fois connecté, votre terminal devrait afficher :
```
C:\>mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 8.2.0 MySQL Community Server - GPL

Copyright (c) 2000, 2023, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```
**Nous sommes prêts à taper du code SQL.**

> [!NOTE]
> Par défaut, il n'y a pas de mot de passe pour se connecter au serveur MySQL de WampServer.

> [!TIP] 
> Effacer l’écran dans l’invite de commande de mysql :
> ```
> system cls;
> ```

## Création de notre première base de données

### 1. Créer une base de données `firstdatabase`

```
CREATE DATABASE firstdatabase;
```
En SQL, les instructions sont généralement écrites en majuscules, car ce sont des mots réservés mysql, bien que le langage soit insensible à la casse. Le nom de la base de données est généralement écrit en minuscules. Chaque instruction doit être terminée par un point-virgule `;`.

Pour afficher toutes les bases de données, vous pouvez utiliser l’instruction `SHOW DATABASES` comme ceci :

```
SHOW DATABASES;
```
```
+--------------------+
| Database           |
+--------------------+
| dbmovie_utopia     |
| firstdatabase      |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| vehicule_base      |
+--------------------+
```

Utiliser la commande `USE` pour sélectionner la base de données `firstdatabase`. Après avoir exécuté cette commande, toutes les opérations SQL que vous effectuez seront appliquées à `firstdatabase` jusqu’à ce que vous changiez de base de données ou que vous fermiez la connexion.

```
USE firstdatabase;
```
```
Database changed
```
Cela signifie que vous travaillez maintenant avec la base de données `firstdatabase`. Toutes les tables que vous créez, les requêtes que vous exécutez, etc., seront dans le contexte de `firstdatabase`.

### 2. Créer une table `users` avec les champs `id`, `name`, `age` et `email`

```
CREATE TABLE users(
    id INTEGER NOT NULL AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(110),
    age INTEGER,
    email VARCHAR(255) NOT NULL UNIQUE
);
```
Cette table contient les colonnes suivantes :

- `id` : un identifiant unique pour chaque utilisateur, qui s’auto-incrémente à chaque nouvel enregistrement.
- `name` : le nom de l’utilisateur, qui est une chaîne de caractères pouvant contenir jusqu’à 110 caractères.
- `age` : l’âge de l’utilisateur, qui est un nombre entier.
- `email` : l’adresse e-mail de l’utilisateur, qui est une chaîne de caractères unique et obligatoire pouvant contenir jusqu’à 255 caractères.

Description de la propriété et des contraintes appliquées aux champs :

- `AUTO_INCREMENT` : Cette propriété est généralement utilisée sur une colonne d’identifiant pour générer automatiquement une valeur unique à chaque fois qu’une nouvelle ligne est insérée dans la table.
- `NOT NULL` : Cette contrainte garantit qu’une colonne ne peut pas avoir de valeur NULL. En d’autres termes, la colonne doit toujours avoir une valeur.
- `PRIMARY KEY` : Cette contrainte combine les contraintes NOT NULL et UNIQUE pour garantir qu’une colonne (ou un ensemble de colonnes) a une valeur unique et qu’elle ne contient jamais de NULL. Une table ne peut avoir qu’une seule clé primaire.
- `UNIQUE` : Cette contrainte garantit que toutes les valeurs d’une colonne sont différentes.

### 3. Décrire la structure de la table `users` avec la commande `DESC`

```
DESC users;
```
```
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(110) | YES  |     | NULL    |                |
| age   | int          | YES  |     | NULL    |                |
| email | varchar(255) | NO   | UNI | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
```
Cette commande affichera la structure de la table `users`, y compris les noms des colonnes, les types de données, etc.

### 4. Créer 3 utilisateurs

```
INSERT INTO users (name, email)
VALUES ('John Doe', 'johndoe@gmail.com'), ('Sam Doe', 'samdoe@gmail.com'), ('Will Doe', 'willdoe@gmail.com');
```
```
Query OK, 3 rows affected (0.01 sec)
Enregistrements: 3  Doublons: 0  Avertissements: 0
```
Cette requête est une instruction `INSERT INTO` en SQL, qui est utilisée pour insérer de nouvelles lignes dans une table :

- `INSERT INTO users` : Cette partie de la requête spécifie la table dans laquelle vous voulez insérer des données. Dans ce cas, il s’agit de la table users.
- `(name, email)` : Ces sont les colonnes de la table users dans lesquelles vous voulez insérer des données. Ici, vous insérez des données dans les colonnes name et email.
- `VALUES ('John Doe', 'johndoe@gmail.com'), ('Sam Doe', 'samdoe@gmail.com'), ('Will Doe', 'willdoe@gmail.com')` :  
Cette partie de la requête spécifie les données que vous voulez insérer. Chaque ensemble de parenthèses représente une nouvelle ligne à insérer dans la table. Ici, vous insérez trois nouvelles lignes dans la table. Chaque ligne contient un name et un email.

### 5. Supprimer l'utilisateur avec l'`id` 1

Cette requête sélectionne toutes les données de toutes les colonnes de la table users. Le symbole `*` signifie “toutes les colonnes” :
```
SELECT * FROM users;
```
```
+----+----------+------+-------------------+
| id | name     | age  | email             |
+----+----------+------+-------------------+
|  1 | John Doe | NULL | johndoe@gmail.com |
|  2 | Sam Doe  | NULL | samdoe@gmail.com  |
|  3 | Will Doe | NULL | willdoe@gmail.com |
+----+----------+------+-------------------+
```

Cette requête supprime la ligne de la table users où la colonne `id` est égale à 1 :
```
DELETE FROM users WHERE id = 1;
```

### 6. Supprimer la table `users`

Une fois que vous exécutez cette commande, toutes les données stockées dans la table users seront définitivement supprimées.
```
DROP TABLE users;
```

### 7. Créer une table `users` avec `id`, `name` et `email`

```
CREATE TABLE users (
id INTEGER NOT NULL AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
email VARCHAR(255) NOT NULL UNIQUE
);
```
```
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(100) | YES  |     | NULL    |                |
| email | varchar(255) | NO   | UNI | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
```

### 8. Ajouter une nouvelle colonne `status` à la table `users`

Cette requête ajoute une nouvelle colonne status à la table users. Cette colonne est de type BOOLEAN et ne peut pas être NULL.
```
ALTER TABLE users ADD status BOOLEAN NOT NULL;
```
```
+--------+--------------+------+-----+---------+----------------+
| Field  | Type         | Null | Key | Default | Extra          |
+--------+--------------+------+-----+---------+----------------+
| id     | int          | NO   | PRI | NULL    | auto_increment |
| name   | varchar(100) | YES  |     | NULL    |                |
| email  | varchar(255) | NO   | UNI | NULL    |                |
| status | tinyint(1)   | NO   |     | NULL    |                |
+--------+--------------+------+-----+---------+----------------+
```

Cette requête insère une nouvelle ligne dans la table users avec la valeur 1 pour la colonne status.
```
INSERT INTO users (status) VALUES (1);
```
Cette requête sélectionne toutes les données de la table users où la colonne status est égale à 1.
```
SELECT * FROM users WHERE status = 1;
```
```
+----+------+-------+--------+
| id | name | email | status |
+----+------+-------+--------+
|  1 | NULL |       |      1 |
+----+------+-------+--------+
```

## Les opérations fondamentales en SQL

### Sélection de données (SELECT)

C'est l'opération la plus courante. Elle permet de récupérer des données spécifiques depuis une table.

`SELECT` : Sélectionne des données d’une ou plusieurs tables.  
`FROM` :  Spécifie la table à partir de laquelle vous souhaitez récupérer les données.  

1. Sélectionner une colonne spécifique :
```
SELECT nom_du_champ FROM nom_du_tableau;
```
Cette requête SQL sélectionne le champ nom_du_champ de la table nom_du_tableau.  

2. Sélectionner plusieurs colonnes :
```
SELECT prenom, nom FROM client;
```
Cette requête retourne les prénoms et les noms des clients.  

3. Sélectionner toutes les colonnes :
```
SELECT * FROM client;
```
Cette requête retourne toutes les colonnes de la table client. 

### Insertion de données (INSERT)

Permets d'ajouter de nouvelles lignes de données à une table.

`INSERT INTO` : insérer de nouvelles données dans une table.  
`VALUES` : fourni les données que vous souhaitez insérer dans une table.

1. Insérer une ligne en spécifiant toutes les colonnes :
```
INSERT INTO table VALUES ('valeur 1', 'valeur 2', ...);
```
Cette syntaxe oblige à remplir toutes les données, tout en respectant l’ordre des colonnes.

2. Insérer une ligne en spécifiant seulement les colonnes souhaitées :
```
INSERT INTO table (nom_colonne_1, nom_colonne_2, ...) VALUES ('valeur 1', 'valeur 2', ...);
```
Il est possible de ne pas renseigner toutes les colonnes. De plus, l’ordre des colonnes n’est pas important.

3. Insérer plusieurs lignes à la fois :
```
INSERT INTO client (prenom, nom, ville, age)  
VALUES  
('John', 'Doe', 'San Francisco', 28),  
('Will', 'Doe', 'New York', 38);  
```

### Mise à jour de données (UPDATE) :

Modifie les valeurs existantes dans une table.
```
UPDATE users SET age = 26 WHERE name = 'Doe';
```

### Suppression de données (DELETE) :

Supprime des lignes de données d'une table.
```
DELETE FROM users WHERE name = 'Doe';
```

### Les clauses

#### WHERE

La clause WHERE est utilisée pour filtrer les résultats des requêtes. Elle permet de spécifier des conditions pour restreindre les données renvoyées.

```
SELECT * FROM produits WHERE prix > 50;
```
Cette requête renverra tous les produits dont le prix est supérieur à 50.

#### ORDER BY

Utilisée pour trier les résultats d'une requête.
```
SELECT * FROM users ORDER BY name ASC;
```
Cette requête trie les utilisateurs par ordre croissant de nom.

#### LIMIT

Limite le nombre de résultats renvoyés par une requête.
```
SELECT * FROM users LIMIT 10;
```
Cette requête renverra les 10 premières lignes de la table `users`.

#### AS

Renommer temporairement une colonne ou une table dans le résultat d'une requête. Cela rend les résultats plus lisibles.
```
SELECT name AS NomUtilisateur FROM users;
```
Cette requête renomme la colonne `name` en `NomUtilisateur`.

#### GROUP BY

Regrouper les résultats d'une requête en fonction des valeurs d'une ou de plusieurs colonnes.
````
SELECT ville, COUNT(*) as NombreUtilisateurs FROM utilisateurs GROUP BY ville;
````
Cette requête renverra le nombre d'utilisateurs pour chaque ville.

### Les opérateurs

#### NOT

L'opérateur NOT est utilisé pour nier une condition dans une clause WHERE
```
SELECT * FROM produits WHERE NOT prix > 50;
```
Cette requête renverra tous les produits dont le prix n'est pas supérieur à 50.

#### AND

L'opérateur AND est utilisé pour combiner plusieurs conditions dans une clause WHERE.
```
SELECT * FROM users WHERE age > 30 AND ville = 'Marseille';
```
Cette requête renverra tous les utilisateurs dont l'âge est supérieur à 30 et qui habitent à Marseille.

### Les commandes

#### ALTER TABLE

La commande `ALTER TABLE` en SQL est utilisée pour modifier la structure d’une table existante (altérer).

Utilisations courantes de cette commande :

1. Ajouter une colonne :
```
ALTER TABLE nom_table ADD nom_colonne type_donnees;
```
2. Supprimer une colonne :
```
ALTER TABLE nom_table DROP COLUMN nom_colonne;
```
3. Modifier une colonne :
```
ALTER TABLE nom_table MODIFY nom_colonne type_donnees;
```
4. Renommer une colonne :
```
ALTER TABLE nom_table CHANGE colonne_ancien_nom colonne_nouveau_nom type_donnees;
```

## Les jointures

Les jointures permettent de combiner les données de plusieurs tables en fonction de certaines conditions. Par exemple, si vous avez une table pour les utilisateurs et une autre pour les commandes, une jointure pourrait vous montrer les utilisateurs qui ont passé des commandes.

```
SELECT users.name, commandes.produit
FROM users
JOIN commandes ON users.id = commandes.user_id;
```

> [!NOTE]
> L'utilisation du point `.` dans la clause `SELECT`, comme dans `users.name`, indique que la colonne `name` provient de la table `users`. En SQL, cela est utilisé pour spécifier de quelle table provient une colonne lorsque les colonnes partagent le même nom dans différentes tables. Le point sert à se déplacer dans l'objet.

### PRIMARY KEY et FOREIGN KEY

Les concepts de PRIMARY KEY et FOREIGN KEY sont cruciaux en SQL pour établir des relations entre les tables d'une base de données relationnelle.

#### PRIMARY KEY (clé primaire)

La clé primaire (PRIMARY KEY) assure l’unicité et l’intégrité des données dans une table.

- Une table ne peut avoir qu’une seule clé primaire.
- Elle ne peut pas contenir de valeurs NULL.
- Elle identifie de manière unique chaque enregistrement dans une table.

#### FOREIGN KEY (clé étrangère)

La clé étrangère (FOREIGN KEY) maintient l’intégrité référentielle entre deux tables.

- Une table peut avoir plusieurs clés étrangères.
- Elle peut contenir des valeurs NULL.
- C'est une clé utilisée pour lier deux tables ensemble.
- Elle doit correspondre à une valeur existante de la PRIMARY KEY dans une autre table.
