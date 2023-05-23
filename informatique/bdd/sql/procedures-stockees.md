# Procédures stockées

Les procédures stockées sont des blocs de code SQL qui sont enregistrés dans la base de données et peuvent être appelés et exécutés ultérieurement. Elles permettent de regrouper et de réutiliser des instructions SQL complexes, offrant ainsi une meilleure modularité et une plus grande efficacité dans le développement d'applications. Les procédures stockées sont prises en charge par la plupart des systèmes de gestion de bases de données relationnelles, tels que MySQL, SQL Server, Oracle, PostgreSQL, etc.

Avantages des procédures stockées :

* Réutilisabilité : Les procédures stockées peuvent être appelées à partir de différentes parties d'une application ou d'autres procédures stockées, ce qui évite la duplication de code.
* Performance : Les procédures stockées sont compilées et stockées dans la base de données, ce qui permet d'exécuter rapidement des opérations complexes sans envoyer de nombreuses requêtes au serveur.
* Sécurité : Les procédures stockées permettent de gérer les autorisations et les privilèges d'accès aux données, offrant ainsi un contrôle plus granulaire sur les opérations exécutées par les utilisateurs.

Syntaxe de base des procédures stockées : Voici la syntaxe générale pour créer une procédure stockée en SQL :

```sql
CREATE PROCEDURE nom_de_la_procedure ([param1 type1], [param2 type2], ...)
BEGIN
    -- Déclarations et instructions SQL
END;
```

* `nom_de_la_procedure` : Le nom donné à la procédure stockée.
* `param1, param2, ...` : Les paramètres facultatifs de la procédure stockée.
* `type1, type2, ...` : Les types de données des paramètres.

Exemple de procédure stockée simple : Voici un exemple de procédure stockée qui récupère les employés dont le salaire est supérieur à un seuil donné :

```sql
CREATE PROCEDURE GetEmployeesBySalaryThreshold(IN salary_threshold DECIMAL(10,2))
BEGIN
    SELECT * FROM employees WHERE salary > salary_threshold;
END;
```

* `IN salary_threshold` : Le paramètre d'entrée de la procédure stockée.

Appel et exécution d'une procédure stockée : Pour appeler et exécuter une procédure stockée, utilisez la commande `CALL` :

```sql
CALL nom_de_la_procedure([arg1], [arg2], ...);
```

* `nom_de_la_procedure` : Le nom de la procédure stockée.
* `arg1, arg2, ...` : Les arguments passés à la procédure stockée (si des paramètres sont définis).

Exemple d'appel de procédure stockée :

```sql
CALL GetEmployeesBySalaryThreshold(5000);
```

Ce cours vous donne une introduction de base aux procédures stockées en SQL. Vous pouvez utiliser des blocs de code plus complexes, des variables, des boucles et des conditions dans les procédures stockées pour accomplir des tâches plus avancées. Les procédures stockées sont un outil puissant pour améliorer la modularité, la performance et la sécurité de vos applications basées sur une base de données relationnelle.
