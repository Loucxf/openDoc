# 🐌 Tail

La commande "tail" est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour afficher les dernières lignes d'un fichier ou la fin de la sortie des commandes. Elle permet d'afficher rapidement les dernières parties d'un fichier ou d'une sortie sans avoir à afficher l'intégralité du contenu. Voici une explication détaillée de la commande "tail" :

Syntaxe de base :

```scss
tail [options] fichier(s)
```

Principales options :

* `-n <nombre>` ou `--lines=<nombre>` : Spécifie le nombre de lignes à afficher. Par défaut, il affiche les 10 dernières lignes.
* `-c <nombre>` ou `--bytes=<nombre>` : Spécifie le nombre de bytes à afficher au lieu de lignes.
* `-f` ou `--follow` : Reste en attente des nouvelles lignes ajoutées à un fichier en temps réel.

Exemples d'utilisation :

1. Afficher les 10 dernières lignes d'un fichier :

```bash
tail fichier.txt
```

Cela affiche les 10 dernières lignes du fichier "fichier.txt".

2. Afficher un nombre spécifique de lignes à partir de la fin d'un fichier :

```bash
tail -n 5 fichier.txt
```

Cela affiche les 5 dernières lignes du fichier "fichier.txt".

3. Afficher les derniers n bytes d'un fichier :

```bash
tail -c 100 fichier.txt
```

Cela affiche les 100 derniers bytes du fichier "fichier.txt".

4. Afficher les dernières lignes de la sortie d'une commande en temps réel :

```bash
tail -f fichier.log
```

Cela affiche les dernières lignes du fichier "fichier.log" et reste en attente des nouvelles lignes ajoutées au fichier. Utile pour surveiller les fichiers de log en temps réel.

La commande "tail" est couramment utilisée pour vérifier les nouvelles lignes ajoutées à des fichiers de log, surveiller l'évolution des fichiers en temps réel, ou extraire un sous-ensemble de lignes ou de bytes à partir de la fin d'un fichier.
