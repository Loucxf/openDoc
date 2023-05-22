# 🐉 Df

La commande "df" (disk free) est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour afficher l'utilisation de l'espace disque sur les systèmes de fichiers montés. Elle fournit des informations sur l'espace total disponible, l'espace utilisé, l'espace libre et le pourcentage d'utilisation pour chaque système de fichiers. Voici une explication détaillée de la commande "df" :

Syntaxe de base :

```bash
df [options] [répertoire(s)]
```

Principales options :

* `-h` ou `--human-readable` : Affiche les tailles des systèmes de fichiers dans un format lisible par l'homme (par exemple, 1K, 234M, 2G).
* `-t <type>` ou `--type=<type>` : Affiche uniquement les systèmes de fichiers du type spécifié (par exemple, ext4, nfs, tmpfs).
* `-i` ou `--inodes` : Affiche les informations sur les inodes plutôt que sur l'espace disque.

Exemples d'utilisation :

1. Afficher l'utilisation de l'espace disque de tous les systèmes de fichiers montés :

```bash
df
```

Cela affiche l'utilisation de l'espace disque de tous les systèmes de fichiers montés, y compris l'espace total, l'espace utilisé, l'espace libre et le pourcentage d'utilisation.

2. Afficher l'utilisation de l'espace disque en format lisible par l'homme :

```bash
df -h
```

Cela affiche l'utilisation de l'espace disque en utilisant un format lisible par l'homme, comme "1K", "234M" ou "2G".

3. Afficher uniquement les systèmes de fichiers d'un type spécifique :

```bash
df -t ext4
```

Cela affiche uniquement les systèmes de fichiers de type "ext4" et leur utilisation de l'espace disque.

4. Afficher les informations sur les inodes plutôt que sur l'espace disque :

```bash
df -i
```

Cela affiche les informations sur les inodes, qui sont des structures de données utilisées pour stocker les métadonnées des fichiers, plutôt que sur l'utilisation de l'espace disque.

La commande "df" est utile pour surveiller l'utilisation de l'espace disque sur un système, vérifier la disponibilité de l'espace sur les systèmes de fichiers montés et prendre des décisions en matière de gestion des ressources de stockage.
