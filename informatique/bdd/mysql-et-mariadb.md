# 📄 Mysql et MariaDB

MySQL est un système de gestion de base de données relationnelle open-source très populaire. MariaDB est un fork de MySQL qui offre une compatibilité ascendante avec MySQL tout en ajoutant de nouvelles fonctionnalités et améliorations. MariaDB peut être utilisé comme alternative à MySQL, offrant une expérience similaire avec des améliorations supplémentaires.

Téléchargement :

```bash
sudo apt install mariadb-server
```

Installation :&#x20;

```bash
sudo mysql_secure_installation
```

Se connecter :&#x20;

```bash
mysql -u root -p
```

Créer une base de donnée :&#x20;

```sql
CREATE DATABASE nom_de_la_base_de_donnees;
```

Selectionner une base de donnée :&#x20;

```sql
USE nom_de_la_base_de_donnees;
```

Créer un utilisateur et lui donner des privilèges :&#x20;

```sql
CREATE USER 'utilisateur'@'localhost' IDENTIFIED BY 'mot_de_passe';
GRANT ALL PRIVILEGES ON nom_de_la_base_de_donnees.* TO 'utilisateur'@'localhost';
FLUSH PRIVILEGES;
```

