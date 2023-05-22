# 🗣 Head

La commande "head" est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour afficher les premières lignes d'un fichier ou la sortie des commandes. Elle permet d'afficher un aperçu rapide du contenu d'un fichier ou d'une sortie de commande sans avoir à afficher l'intégralité du contenu. Voici une explication détaillée de la commande "head" :

Syntaxe de base :

```bash
head [options] fichier(s)
```

Principales options :

* `-n <nombre>` ou `--lines=<nombre>` : Spécifie le nombre de lignes à afficher. Par défaut, il affiche les 10 premières lignes.
* `-c <nombre>` ou `--bytes=<nombre>` : Spécifie le nombre de bytes à afficher au lieu de lignes.
* `-v` ou `--verbose` : Affiche le nom du fichier avant chaque ensemble de lignes.

Exemples d'utilisation :

1. Afficher les 10 premières lignes d'un fichier :

```bash
head fichier.txt
```

Cela affiche les 10 premières lignes du fichier "fichier.txt".

2. Afficher un nombre spécifique de lignes d'un fichier :

```bash
head -n 5 fichier.txt
```

Cela affiche les 5 premières lignes du fichier "fichier.txt".

3. Afficher les premiers n bytes d'un fichier :

```bash
head -c 100 fichier.txt
```

Cela affiche les 100 premiers bytes du fichier "fichier.txt".

4. Afficher les premières lignes de la sortie d'une commande :

```bash
ls -l | head
```

Cela affiche les premières lignes de la sortie de la commande "ls -l", c'est-à-dire les premières lignes du listing des fichiers et répertoires.

La commande "head" est utile pour obtenir rapidement un aperçu du contenu d'un fichier, vérifier les premières lignes d'un fichier de log ou extraire un sous-ensemble de lignes ou de bytes à partir d'un fichier.
