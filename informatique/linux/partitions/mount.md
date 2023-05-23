# 🐁 mount

La commande `mount` est utilisée sous Linux pour monter un système de fichiers sur un répertoire existant dans la hiérarchie du système de fichiers. Lorsqu'un système de fichiers est monté, il devient accessible et utilisable dans l'arborescence des répertoires du système d'exploitation. La commande `mount` nécessite des privilèges de superutilisateur (root) ou l'utilisation de la commande `sudo`.

Voici comment utiliser la commande `mount` :

1. Syntaxe de base :
   * La syntaxe générale de la commande `mount` est la suivante : `mount périphérique point_de_montage`
   * `périphérique` fait référence au périphérique ou à la partition contenant le système de fichiers à monter. Par exemple, `/dev/sda1`, `/dev/nvme0n1p2`, ou le chemin d'accès vers un périphérique réseau.
   * `point_de_montage` représente le répertoire de destination (point de montage) existant où le système de fichiers sera monté. Par exemple, `/mnt/data`, `/media/usb`, etc.
2. Options courantes :
   * `-t type_de_systeme_de_fichiers` : Spécifie le type de système de fichiers du périphérique. Si le type n'est pas spécifié, le système de fichiers sera automatiquement détecté.
   * `-o options` : Permet de spécifier des options de montage supplémentaires. Par exemple, `rw` pour le montage en lecture-écriture, `ro` pour le montage en lecture seule, `user` pour permettre aux utilisateurs ordinaires de monter/démonter, etc.
   * `-n` : Effectue un montage en mode « noyau » sans mettre à jour le fichier `/etc/mtab`.
3. Exemples d'utilisation :
   * `sudo mount /dev/sda1 /mnt/data` : Monte le système de fichiers de la partition `/dev/sda1` sur le répertoire `/mnt/data`.
   * `sudo mount -t ntfs /dev/sdb1 /media/usb` : Monte un système de fichiers de type NTFS à partir de la partition `/dev/sdb1` sur le répertoire `/media/usb`.
   * `sudo mount -o remount,rw /dev/sda1` : Remonte la partition `/dev/sda1` en lecture-écriture, en mettant à jour les options de montage.
4. Démontage d'un système de fichiers :
   * Pour démonter un système de fichiers monté, utilisez la commande `umount` suivie du point de montage ou du périphérique. Par exemple, `sudo umount /mnt/data` ou `sudo umount /dev/sda1`.
5. Configuration permanente :
   * Pour rendre le montage permanent après le redémarrage du système, vous devez ajouter une entrée correspondante dans le fichier `/etc/fstab`. Cela permettra au système de monter automatiquement le périphérique au démarrage.
   * Modifiez le fichier `/etc/fstab` en utilisant un éditeur de texte et ajoutez une ligne avec les informations appropriées pour le périphérique et le point de montage.

La commande `mount` est un outil essentiel pour monter et accéder aux systèmes de fichiers sous Linux. Elle permet de connecter des périphériques de stockage ou des partitions au système d'exploitation, offrant ainsi un accès transparent aux données.
