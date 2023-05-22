# 🐢 Top

La commande "top" est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour afficher en temps réel les informations sur les processus en cours d'exécution sur le système. Elle fournit un aperçu détaillé de l'utilisation des ressources système telles que le CPU, la mémoire, les processus actifs et bien plus encore. Voici une explication détaillée de la commande "top" :

Syntaxe de base :

```bash
top
```

Une fois que vous exécutez la commande "top", une interface interactive est affichée avec plusieurs sections d'informations. Voici les sections principales :

1. Ligne d'en-tête (Header) : Cette ligne affiche des informations globales telles que l'heure actuelle, la durée depuis le démarrage du système, le nombre total de processus, les statistiques de charge, etc.
2. Rangée des tâches (Task row) : Chaque ligne de cette section représente un processus individuel en cours d'exécution. Les informations fournies incluent l'identifiant du processus (PID), le propriétaire, l'utilisation du CPU, l'utilisation de la mémoire, l'état du processus, le temps d'exécution, etc.
3. Résumé des ressources système (System resource summary) : Cette section affiche les informations sur l'utilisation globale des ressources système, notamment l'utilisation du CPU, la mémoire physique et virtuelle, les statistiques de swap (si disponible), etc.
4. Affichage des ressources spécifiques au CPU (CPU-specific resource breakdown) : Cette section montre la répartition détaillée de l'utilisation du CPU par chaque processus individuel. Il affiche les pourcentages d'utilisation du CPU par les processus en temps réel.
5. Commandes interactives : En bas de l'interface, vous pouvez utiliser des commandes interactives pour interagir avec les processus, trier les colonnes, modifier les paramètres d'affichage, etc.

Quelques commandes interactives couramment utilisées :

* `k` : Permet de tuer (arrêter) un processus spécifique en fournissant son PID.
* `r` : Permet de renice (modifier la priorité) d'un processus spécifique en fournissant son PID.
* `1` : Affiche la répartition détaillée de l'utilisation du CPU par chaque cœur du processeur.
* `m` : Permet de basculer entre l'affichage de l'utilisation de la mémoire en termes de kilo-octets (K), méga-octets (M) ou gigaoctets (G).

La commande "top" est un outil puissant pour surveiller l'état du système en temps réel, diagnostiquer les problèmes de performances, identifier les processus consommant des ressources excessives et suivre les changements d'utilisation du CPU et de la mémoire.
