# 🌏 HTTP Server

Script pour l'installation d'un serveur apache : [https://github.com/Loucxf/install\_apache2](https://github.com/Loucxf/install\_apache2)

1. Exécutez la commande suivante pour installer le serveur Apache :

```
sudo apt install apache2
```

2. Vous serez invité à saisir votre mot de passe d'administrateur. Fournissez-le et appuyez sur Entrée pour continuer.
3. L'installation d'Apache commencera. Une fois terminée, Apache sera automatiquement démarré et exécuté sur votre système.

Étape 3: Vérification de l'installation

1. Pour vérifier si Apache est correctement installé et en cours d'exécution, ouvrez un navigateur Web sur votre ordinateur et entrez l'adresse suivante :

```arduino
http://localhost/
```

Vous devriez voir une page d'accueil Apache indiquant que le serveur fonctionne correctement.

2. Si vous souhaitez accéder à la page d'accueil Apache depuis un autre ordinateur sur le même réseau local, utilisez l'adresse IP de votre serveur Debian. Pour trouver l'adresse IP, exécutez la commande suivante dans le terminal :

```sql
ip addr show
```

Repérez l'adresse IP associée à votre interface réseau (généralement eth0 ou enp0s3). Utilisez cette adresse IP dans votre navigateur Web pour accéder à la page d'accueil Apache.

Étape 4: Configuration d'Apache Le fichier de configuration principal d'Apache se trouve dans le répertoire /etc/apache2/. Vous pouvez modifier ce fichier pour personnaliser la configuration d'Apache selon vos besoins.

Par exemple, pour ajouter un nouvel hôte virtuel, vous pouvez créer un fichier de configuration dans /etc/apache2/sites-available/ avec les directives appropriées, puis activer le site à l'aide de la commande a2ensite.

## Utilisation d'Apache :&#x20;

1. Structure des fichiers d'Apache :

* Les fichiers de configuration principaux d'Apache se trouvent généralement dans le répertoire /etc/apache2/.
* Le fichier de configuration principal est apache2.conf.
* Le répertoire des sites disponibles se trouve dans /etc/apache2/sites-available/, où vous pouvez créer des fichiers de configuration pour chaque site web.
* Le répertoire des sites activés se trouve dans /etc/apache2/sites-enabled/, où vous pouvez activer les sites en créant des liens symboliques vers les fichiers de configuration des sites disponibles.

2. Configuration d'un nouveau site web :

* Créez un nouveau fichier de configuration dans /etc/apache2/sites-available/ avec une structure similaire à ceci :
*   ```less
    <VirtualHost *:80>
        ServerName monsite.com
        ServerAlias www.monsite.com
        DocumentRoot /var/www/monsite
        <Directory /var/www/monsite>
            AllowOverride All
            Require all granted
        </Directory>
    </VirtualHost>
    ```

    Remplacez "monsite.com" par le nom de domaine de votre site et "/var/www/monsite" par le répertoire racine de votre site.
* Enregistrez le fichier de configuration et activez-le en créant un lien symbolique vers le répertoire des sites activés :
* ```bash
  sudo ln -s /etc/apache2/sites-available/monsite.conf /etc/apache2/sites-enabled/
  ```
* Redémarrez Apache pour prendre en compte les modifications :

```bash
sudo service apache2 restart
```

3. Gestion des fichiers d'index :

* Apache recherche par défaut des fichiers d'index tels que index.html, index.php, etc., dans l'ordre spécifié dans la directive "DirectoryIndex" du fichier de configuration principal.
* Vous pouvez personnaliser les fichiers d'index en modifiant cette directive. Par exemple, pour ajouter index.php avant index.html, vous pouvez ajouter la ligne suivante dans le fichier apache2.conf :&#x20;
* ```
  DirectoryIndex index.php index.html
  ```
* Assurez-vous que le fichier d'index souhaité est présent dans le répertoire racine de votre site web.

4. Gestion des autorisations et des accès :

* Les autorisations de fichiers et les directives d'accès sont définies dans les blocs \<Directory> du fichier de configuration d'Apache.
* Vous pouvez spécifier des autorisations spécifiques pour les répertoires, tels que "AllowOverride" pour autoriser les fichiers .htaccess, et utiliser les directives "Require all granted" ou "Require valid-user" pour contrôler l'accès.
* N'oubliez pas de restreindre l'accès aux fichiers sensibles ou aux scripts exécutables pour éviter les problèmes de sécurité.

5. Gestion des journaux d'erreurs et d'accès :

* Les journaux d'erreurs et d'accès d'Apache se trouvent généralement dans /var/log/apache2/.
* Le journal d'erreurs principal est error.log, tandis que le journal d'accès principal est access.log.
* Vous pouvez surveiller ces journaux pour identifier les problèmes et les activités de votre site web.
