# 🐒 mkfs

La commande `mkfs` (Make File System) est utilisée sous Linux pour créer un système de fichiers sur une partition ou un périphérique de stockage. Elle est utilisée après la création d'une partition avec la commande `fdisk` ou un outil similaire. La commande `mkfs` formate la partition avec un système de fichiers spécifié, permettant ainsi au système d'exploitation de gérer et d'organiser les données sur cette partition.

Voici comment utiliser la commande `mkfs` :

1. Syntaxe de base :
   * La syntaxe générale de la commande `mkfs` est la suivante : `mkfs -t type_de_systeme_de_fichiers périphérique`
   * `type_de_systeme_de_fichiers` correspond au type de système de fichiers à créer (par exemple, ext4, ext3, ntfs, xfs, etc.).
   * `périphérique` représente le nom ou le chemin d'accès du périphérique de stockage sur lequel vous souhaitez créer le système de fichiers (par exemple, `/dev/sda1`, `/dev/nvme0n1p2`).
2. Options courantes :
   * `-t type_de_systeme_de_fichiers` : Spécifie le type de système de fichiers à créer.
   * `-L étiquette` : Ajoute une étiquette au système de fichiers.
   * `-m nombre` : Définit le pourcentage de réservation d'espace réservé à l'administrateur du système.
   * `-b taille_bloc` : Spécifie la taille des blocs du système de fichiers.
   * `-v` : Affiche des informations détaillées pendant le processus de création du système de fichiers.
   * `-F` : Force la création du système de fichiers même si des avertissements sont émis.
3. Exemples d'utilisation :
   * `sudo mkfs -t ext4 /dev/sda1` : Crée un système de fichiers de type ext4 sur la partition `/dev/sda1`.
   * `sudo mkfs -t ntfs -L "MonDisque" /dev/sdb1` : Crée un système de fichiers de type NTFS avec l'étiquette "MonDisque" sur la partition `/dev/sdb1`.
   * `sudo mkfs -t xfs -m 5 -b 4096 /dev/nvme0n1p2` : Crée un système de fichiers XFS sur la partition `/dev/nvme0n1p2` avec une réservation de 5% et une taille de bloc de 4096 octets.
4. Attention :
   * L'utilisation de la commande `mkfs` entraîne la suppression de toutes les données présentes sur la partition. Assurez-vous de sauvegarder vos données importantes avant de créer le système de fichiers.
   * Soyez prudent lorsque vous spécifiez le périphérique pour éviter d'effacer accidentellement des données sur le mauvais périphérique.

La commande `mkfs` est un outil essentiel pour créer des systèmes de fichiers sur des partitions ou des périphériques de stockage sous Linux. Elle permet de préparer les partitions pour le stockage des données et facilite la gestion des données sur le système d'exploitation.
