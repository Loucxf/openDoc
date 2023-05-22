# 🎞 Dmesg

Elle permet d'afficher les informations de démarrage du système, les messages du noyau liés aux périphériques, aux pilotes et à d'autres composants système.

Lorsque le système démarre, le noyau du système d'exploitation effectue diverses opérations d'initialisation, détecte les périphériques matériels, charge les pilotes nécessaires et effectue d'autres tâches. Ces actions génèrent des messages qui sont stockés dans un tampon de messages du noyau. La commande "dmesg" permet d'accéder à ces messages et de les afficher dans la console.

Syntaxe de base :

```css
dmesg [options]
```

Principales options :

* `-c` ou `--clear` : Efface le tampon de messages du noyau après l'affichage.
* `-H` ou `--human` : Affiche les tailles en utilisant un format lisible par l'homme (par exemple, 1K, 234M, 2G).
* `-l` ou `--level <niveau>` : Affiche uniquement les messages ayant un niveau de priorité spécifique (par exemple, emerg, alert, crit, err, warning, notice, info, debug).

Exemples d'utilisation :

1. Afficher les messages du noyau :

```
dmesg
```

Cela affiche tous les messages du noyau depuis le dernier démarrage du système.

2. Effacer le tampon de messages du noyau après l'affichage :

```r
dmesg -c
```

Cela affiche tous les messages du noyau et efface ensuite le tampon de messages.

3. Afficher uniquement les messages d'erreur et d'avertissement :

```perl
dmesg -l err,warn
```

Cela affiche uniquement les messages du noyau ayant un niveau de priorité d'erreur (err) et d'avertissement (warn).

La commande "dmesg" est utile pour diagnostiquer les problèmes système, surveiller les événements du noyau et obtenir des informations sur les périphériques détectés par le système d'exploitation.
