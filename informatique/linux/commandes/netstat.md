# 👂 Netstat

La commande `netstat` est une commande utilisée dans les systèmes d'exploitation, tels que Linux, macOS et Windows, pour afficher des informations sur les connexions réseau, les interfaces réseau, les statistiques réseau et les tables de routage. Elle fournit une vue détaillée de l'état du réseau sur une machine.

La syntaxe générale de la commande `netstat` est la suivante :

```sh
netstat [options]
```

Voici quelques-unes des options couramment utilisées avec la commande `netstat` :

* `-a` : Affiche toutes les connexions actives et les ports en écoute, tant TCP que UDP.
* `-t` : Affiche les connexions TCP.
* `-u` : Affiche les connexions UDP.
* `-n` : Affiche les adresses IP et les numéros de port sous forme numérique plutôt que de résoudre les noms d'hôtes.
* `-p` : Affiche le nom ou l'identifiant du processus qui utilise le port.
* `-r` : Affiche la table de routage du système.
* `-s` : Affiche les statistiques réseau, telles que les compteurs de paquets et d'erreurs.
* `-l` : Permet de filtrer les résultats pour afficher uniquement les ports qui sont en écoute (listening).

La commande `netstat` est souvent utilisée pour :

* Vérifier les connexions réseau actives.
* Vérifier les ports en écoute sur la machine.
* Identifier les programmes ou processus qui utilisent certains ports.
* Vérifier les statistiques réseau, comme le nombre de paquets reçus ou envoyés.
* Afficher la table de routage du système pour voir les routes configurées.

Il convient de noter que certaines options peuvent varier légèrement selon le système d'exploitation utilisé. Il est recommandé de consulter la documentation spécifique à votre système d'exploitation pour obtenir des informations détaillées sur les options et les fonctionnalités spécifiques de la commande `netstat`.
