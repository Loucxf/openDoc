# 🪵 Chmod

La commande "chmod" (change mode) est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour modifier les permissions d'accès sur les fichiers et les répertoires. Elle permet de spécifier les droits d'accès pour le propriétaire du fichier, le groupe auquel il appartient et les autres utilisateurs. Voici une explication détaillée de la commande "chmod" :

Syntaxe de base :&#x20;

```bash
chmod [options] permissions fichier(s)
```

Principales options :

* `-c` ou `--changes` : Affiche uniquement les fichiers dont les permissions ont été modifiées.
* `-R` ou `--recursive` : Applique les modifications de manière récursive à tous les fichiers et répertoires contenus dans un répertoire.
* `-v` ou `--verbose` : Affiche des informations détaillées sur les modifications effectuées.

Permissions :

Les permissions sont spécifiées en utilisant une notation alphabétique ou numérique.

* Notation alphabétique : Les permissions sont représentées par les lettres "r" (lecture), "w" (écriture) et "x" (exécution). Par exemple, "rwx" représente les permissions de lecture, écriture et exécution.
* Notation numérique : Chaque permission est représentée par un chiffre. La lecture est représentée par 4, l'écriture par 2 et l'exécution par 1. Les différentes permissions sont ensuite ajoutées pour obtenir un chiffre de 3 chiffres. Par exemple, 755 représente les permissions rwxr-xr-x, où le propriétaire a toutes les permissions (7), le groupe et les autres ont des permissions de lecture et d'exécution (5).

Exemples d'utilisation :

1. Modifier les permissions d'un fichier :&#x20;

```bash
chmod 644 fichier.txt
```

Cela donne les permissions rw-r--r-- au propriétaire, et les permissions r--r--r-- au groupe et aux autres utilisateurs pour le fichier "fichier.txt".

2. Modifier les permissions de manière récursive pour un répertoire et son contenu :

```bash
chmod -R 755 dossier/
```

Cela donne les permissions rwxr-xr-x au propriétaire, et les permissions r-xr-xr-x au groupe et aux autres utilisateurs pour le répertoire "dossier" et tous ses fichiers et sous-répertoires.

3. Modifier les permissions en utilisant la notation alphabétique :

```bash
chmod u=rw,g=r,o=r fichier.txt
```

Cela donne les permissions rw-r--r-- en utilisant la notation alphabétique pour le propriétaire, le groupe et les autres utilisateurs.

Il est important de noter que la commande "chmod" nécessite des droits suffisants pour modifier les permissions d'un fichier ou d'un répertoire. Seul le propriétaire du fichier ou le superutilisateur (root) peut modifier les permissions.
