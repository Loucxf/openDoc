# 🎉 Partitions

1. Comprendre les partitions :
   * Une partition est une section logique d'un disque dur qui est délimitée et utilisée pour stocker des données.
   * Les partitions peuvent être utilisées pour organiser et gérer efficacement l'espace de stockage sur un disque dur.
   * Sous Linux, les partitions sont généralement identifiées par des noms tels que /dev/sda1, /dev/sdb2, etc.
2. Vérifier les partitions existantes :
   * Utilisez la commande `lsblk` pour afficher la liste des périphériques de bloc, y compris les partitions.
   * La commande `fdisk -l` peut également être utilisée pour afficher les informations détaillées sur les partitions existantes.
3. Créer une nouvelle partition :
   * Utilisez la commande `fdisk` pour créer une nouvelle partition sur un disque.
   * Exécutez `sudo fdisk /dev/<device>` pour ouvrir l'outil fdisk pour le périphérique spécifié.
   * Utilisez les commandes fdisk (nouvelle partition), d (supprimer une partition), p (afficher les partitions), w (enregistrer les modifications), etc.
   * Une fois la partition créée, vous pouvez formater la partition à l'aide de la commande `mkfs` (par exemple, `mkfs.ext4 /dev/sda1` pour formater en système de fichiers ext4).
4. Monter et démonter des partitions :
   * Utilisez la commande `mount` pour monter une partition sur un répertoire spécifique.
   * Par exemple, `sudo mount /dev/sda1 /mnt` monte la partition /dev/sda1 sur le répertoire /mnt.
   * Utilisez la commande `umount` pour démonter une partition montée.
5. Gestion des partitions avec GParted :
   * GParted est une interface graphique conviviale pour gérer les partitions sous Linux.
   * Vous pouvez l'installer à l'aide de la commande `sudo apt-get install gparted` sur les distributions basées sur Debian/Ubuntu.
   * Lorsque vous exécutez GParted, sélectionnez le périphérique de stockage souhaité et utilisez l'interface graphique pour créer, redimensionner, déplacer, formater ou supprimer des partitions.
6. Modifier la taille des partitions existantes :
   * Utilisez la commande `resize2fs` pour redimensionner un système de fichiers ext2/ext3/ext4.
   * Avant de redimensionner une partition, vous devez d'abord la démonter (utilisez la commande `umount`).
   * Après avoir redimensionné la partition, vous pouvez la remonter sur le point de montage approprié.
7. Gestion des partitions avec LVM (Logical Volume Manager) :
   * LVM permet de créer des volumes logiques qui facilitent la gestion de l'espace de stockage.
   * Les partitions sont regroupées en groupes de volumes, à partir desquels vous pouvez créer des volumes logiques et les étendre au besoin.
   * Vous pouvez utiliser les commandes `pvcreate`, `vgcreate`, `lvcreate`, `lvextend`, etc. pour créer et gérer des volumes logiques à l'aide de LVM.

Il est essentiel de faire preuve de prudence lors de la gestion des partitions, car des erreurs peuvent entraîner une perte de données. Assurez-vous de sauvegarder vos données importantes avant de procéder à des opérations de partitionnement.
