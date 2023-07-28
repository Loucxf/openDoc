# 🦐 HAProxy

HAProxy est un logiciel open-source de répartition de charge (load balancing) et de proxy TCP/HTTP. Il est utilisé pour gérer le trafic réseau entrant et sortant, répartir les demandes vers plusieurs serveurs backend, améliorer la disponibilité et les performances des applications. Voici un tutoriel d'installation de HAProxy sous Debian :

Étape 1: Mise à jour du système Avant d'installer HAProxy, assurez-vous que votre système Debian est à jour. Ouvrez un terminal et exécutez les commandes suivantes :

```sql
sudo apt update
sudo apt upgrade
```

Étape 2: Installation de HAProxy

1. Dans le même terminal, exécutez la commande suivante pour installer HAProxy :

```
sudo apt install haproxy
```

2. Vous serez invité à saisir votre mot de passe d'administrateur. Fournissez-le et appuyez sur Entrée pour continuer.
3. L'installation de HAProxy commencera. Une fois terminée, HAProxy sera automatiquement démarré et exécuté sur votre système.

Étape 3: Configuration de HAProxy

1. Le fichier de configuration principal de HAProxy se trouve dans /etc/haproxy/haproxy.cfg. Ouvrez ce fichier avec un éditeur de texte en utilisant la commande suivante :

```bash
sudo nano /etc/haproxy/haproxy.cfg
```

2. Dans le fichier de configuration, vous pouvez définir les paramètres spécifiques à votre environnement. Voici un exemple simple de configuration qui équilibre la charge entre deux serveurs web backend :

```sql
frontend web
    bind *:80
    mode http
    default_backend backend_servers

backend backend_servers
    mode http
    balance roundrobin
    server server1 192.168.0.101:80 check
    server server2 192.168.0.102:80 check
```

3. Dans cet exemple, HAProxy écoute sur le port 80 et redirige le trafic entrant vers les serveurs backend server1 et server2.
4. Personnalisez la configuration en fonction de vos besoins. Vous pouvez ajouter des options supplémentaires telles que la gestion des sessions, l'authentification, le chiffrement SSL, etc.
5. Enregistrez le fichier de configuration.

Étape 4: Redémarrage de HAProxy Après avoir modifié la configuration, redémarrez HAProxy pour que les modifications prennent effet. Utilisez la commande suivante :

```
sudo service haproxy restart
```

Étape 5: Vérification de l'état de HAProxy Pour vérifier si HAProxy fonctionne correctement, vous pouvez accéder à l'interface statistique de HAProxy via un navigateur web. Par défaut, l'interface statistique est disponible à l'adresse [http://localhost:8080/stats](http://localhost:8080/stats).

Pour autoriser l'accès à distance à l'interface statistique, modifiez la configuration de HAProxy en ajoutant les lignes suivantes :

```bash
listen stats
    bind *:8080
    stats enable
    stats uri /stats
    stats refresh 10s
    stats admin if TRUE
```

Étape 6: Utilisation de HAProxy Maintenant que HAProxy est installé et configuré, vous pouvez utiliser l'adresse IP de votre serveur HAProxy comme point d'entrée pour votre application. HAProxy répartira la charge entre les serveurs backend spécifiés dans la configuration.

Assurez-vous de consulter la documentation officielle de HAProxy pour en savoir plus sur les fonctionnalités avancées et les options de configuration disponibles.

Ceci conclut le tutoriel d'installation de HAProxy sous Debian. Vous pouvez maintenant commencer à utiliser HAProxy pour répartir la charge et améliorer les performances de votre application.
