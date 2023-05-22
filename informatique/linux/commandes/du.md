# 🦆 Du

La commande "du" (disk usage) est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour afficher l'utilisation de l'espace disque par les fichiers et répertoires d'un système de fichiers. Elle permet de connaître la taille des fichiers et répertoires, ce qui est utile pour identifier les fichiers volumineux ou les répertoires consommant beaucoup d'espace disque. Voici une explication détaillée de la commande "du" :

Syntaxe de base :

```bash
du [options] répertoire(s)
```

Principales options :

* `-h` ou `--human-readable` : Affiche les tailles des fichiers et répertoires dans un format lisible par l'homme (par exemple, 1K, 234M, 2G).
* `-s` ou `--summarize` : Affiche uniquement le total de l'utilisation de l'espace disque plutôt que les détails par fichier et répertoire.
* `-c` ou `--total` : Affiche le total cumulatif de l'utilisation de l'espace disque pour chaque répertoire, en incluant les sous-répertoires.
* `-h` ou `--max-depth=<niveau>` : Spécifie la profondeur maximale pour laquelle les informations doivent être affichées.

Exemples d'utilisation :

1. Afficher l'utilisation de l'espace disque d'un répertoire :

```bash
du répertoire
```

Cela affiche la taille totale utilisée par les fichiers et sous-répertoires du répertoire spécifié.

2. Afficher l'utilisation de l'espace disque en format lisible par l'homme :

```bash
du -h répertoire
```

Cela affiche la taille totale utilisée en utilisant un format lisible par l'homme, comme "1K", "234M" ou "2G".

3. Afficher uniquement le total de l'utilisation de l'espace disque d'un répertoire :

```bash
du -s répertoire
```

Cela affiche uniquement le total de l'utilisation de l'espace disque pour le répertoire spécifié, sans les détails par fichier et sous-répertoire.

4. Afficher le total cumulatif de l'utilisation de l'espace disque pour chaque répertoire, en incluant les sous-répertoires :

```bash
du -c répertoire
```

Cela affiche le total cumulatif de l'utilisation de l'espace disque pour chaque répertoire, ainsi que le total général.

La commande "du" est utile pour surveiller l'utilisation de l'espace disque sur un système, identifier les fichiers ou répertoires consommant le plus d'espace et prendre des décisions éclairées sur la gestion des ressources de stockage.
