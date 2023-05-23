# 🐸 fdisk

La commande `fdisk` est un outil puissant et largement utilisé sous Linux pour gérer les partitions des disques durs. Elle permet de créer, supprimer, redimensionner et modifier les partitions sur un disque. Voici une explication détaillée de la commande `fdisk` :

**Remarque importante : L'utilisation de `fdisk` peut modifier les partitions de votre disque dur, ce qui peut entraîner la perte de données. Assurez-vous de sauvegarder vos données importantes avant d'utiliser cette commande. Soyez prudent lors de son utilisation.**

1. Syntaxe de base :
   * La commande `fdisk` est généralement utilisée avec le nom du périphérique sur lequel vous souhaitez effectuer des opérations de partitionnement (par exemple, `/dev/sda`, `/dev/nvme0n1`).
   * Par exemple, pour utiliser `fdisk` sur le disque `/dev/sda`, vous exécutez `sudo fdisk /dev/sda`.
2. Commandes principales de `fdisk` :
   * `m` : Affiche l'aide sur les commandes disponibles.
   * `p` : Affiche les informations sur les partitions existantes sur le disque.
   * `n` : Crée une nouvelle partition.
   * `d` : Supprime une partition existante.
   * `t` : Modifie le type de partition.
   * `l` : Affiche la liste des codes de types de partition.
   * `w` : Enregistre les modifications effectuées et écrit les nouvelles informations de partition sur le disque.
   * `q` : Quitte `fdisk` sans enregistrer les modifications.
3. Création d'une nouvelle partition :
   * Après avoir exécuté `fdisk` sur le périphérique souhaité, utilisez la commande `n` pour créer une nouvelle partition.
   * Suivez les instructions pour spécifier le type de partition (primaire, étendue), le numéro de partition, le point de départ et la taille de la partition.
   * Une fois que vous avez terminé, enregistrez les modifications en utilisant la commande `w`.
4. Suppression d'une partition existante :
   * Utilisez la commande `p` pour afficher les partitions existantes et identifiez le numéro de la partition que vous souhaitez supprimer.
   * Ensuite, utilisez la commande `d` suivie du numéro de partition pour supprimer la partition spécifiée.
   * N'oubliez pas d'enregistrer les modifications en utilisant la commande `w`.
5. Modification du type de partition :
   * La commande `t` permet de modifier le type de partition. Elle vous demande le numéro de partition sur lequel vous souhaitez apporter des modifications.
   * Ensuite, vous pouvez sélectionner le code de type de partition approprié à partir de la liste affichée en utilisant la commande `l`.
6. Affichage des informations de partition :
   * Utilisez la commande `p` pour afficher les informations sur les partitions existantes sur le disque.
   * Cela affiche les numéros de partition, les tailles, les types, les points de départ, etc.
7. Quitter `fdisk` :
   * Pour quitter `fdisk` sans enregistrer les modifications, utilisez la commande `q`.
   * Si vous avez apporté des modifications que vous souhaitez conserver, n'oubliez pas d'utiliser la commande `w` pour enregistrer les modifications avant de quitter.

La commande `fdisk` est un outil puissant pour gérer les partitions sous Linux. Cependant, elle nécessite une bonne compréhension des concepts de partitionnement et une prudence lors de son utilisation. Veillez à toujours sauvegarder vos données importantes avant de manipuler les partitions.
