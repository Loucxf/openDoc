# 🦁 ln

La commande "ln" (lien) est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour créer des liens entre les fichiers ou répertoires. Elle permet de créer des références à des fichiers ou répertoires existants, ce qui permet d'accéder à ces fichiers ou répertoires via différents noms ou emplacements. Voici une explication détaillée de la commande "ln" :

Syntaxe de base :

```bash
ln [options] cible lien
```

Principales options :

* `-s` ou `--symbolic` : Crée un lien symbolique plutôt qu'un lien dur (par défaut).
* `-f` ou `--force` : Remplace le lien existant s'il existe déjà.
* `-v` ou `--verbose` : Affiche des informations détaillées sur les opérations effectuées.

Types de liens :

1. Lien symbolique (symbolic link) : Un lien symbolique, également appelé lien mou ou lien souple, est un type de lien qui crée une référence symbolique vers un fichier ou un répertoire existant. Lorsqu'un lien symbolique est accédé, le système d'exploitation suit la référence pour atteindre le fichier ou le répertoire cible.
2. Lien dur (hard link) : Un lien dur crée une autre entrée dans le système de fichiers qui pointe vers le même fichier ou répertoire cible. Les liens durs sont des références directes vers le même contenu, et les modifications apportées à l'un des liens sont reflétées dans tous les autres liens.

Exemples d'utilisation :

1. Créer un lien symbolique vers un fichier :

```bash
ln -s /chemin/vers/fichier cible
```

Cela crée un lien symbolique nommé "cible" qui pointe vers le fichier spécifié.

2. Créer un lien dur vers un fichier :

```bash
ln /chemin/vers/fichier cible
```

Cela crée un lien dur nommé "cible" qui pointe vers le fichier spécifié.

3. Créer un lien symbolique vers un répertoire :

```bash
ln -s /chemin/vers/répertoire cible
```

Cela crée un lien symbolique nommé "cible" qui pointe vers le répertoire spécifié.

4. Créer un lien dur vers un répertoire (non recommandé) :

```bash
ln -d /chemin/vers/répertoire cible
```

Cela crée un lien dur nommé "cible" qui pointe vers le répertoire spécifié.

Il est important de noter que lorsqu'un fichier ou un répertoire cible est déplacé ou supprimé, les liens qui y font référence peuvent devenir inutilisables ou pointer vers des emplacements incorrects. Par conséquent, il est recommandé d'utiliser les liens symboliques plutôt que les liens durs dans la plupart des cas, car ils offrent plus de flexibilité.
