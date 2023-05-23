# 🐞 lsblk

La commande `lsblk` est utilisée sous Linux pour afficher les informations sur les périphériques de bloc, tels que les disques durs, les partitions et les périphériques de stockage amovibles. Elle fournit une vue hiérarchique de la structure des périphériques de stockage, ce qui facilite l'identification et l'analyse de ces périphériques.

Voici quelques utilisations courantes de la commande `lsblk` :

1. Afficher une liste des périphériques de stockage :
   * En exécutant simplement `lsblk` sans aucun argument, la commande affiche une liste des périphériques de bloc connectés à votre système.
   * Les informations incluent les noms des périphériques, les types de périphériques (disque, partition, périphérique amovible), les tailles, les points de montage (s'ils sont montés), etc.
2. Afficher des informations détaillées sur les périphériques :
   * Pour obtenir des informations plus détaillées sur les périphériques, vous pouvez utiliser l'option `-f` (par exemple, `lsblk -f`).
   * Cela affiche des détails supplémentaires tels que les systèmes de fichiers utilisés sur les partitions, les étiquettes de volume, les UUID (identifiants uniques universels), etc.
3. Afficher la hiérarchie des périphériques :
   * L'option `-t` (par exemple, `lsblk -t`) permet d'afficher la hiérarchie des périphériques, montrant les relations entre les périphériques parent et les périphériques enfants.
   * Cela est utile pour visualiser comment les périphériques de stockage sont organisés, tels que les disques, les partitions et les volumes logiques LVM.
4. Afficher les informations de taille :
   * Si vous souhaitez afficher les tailles des périphériques dans un format lisible par l'homme (par exemple, en utilisant des unités telles que kilo, méga, giga), vous pouvez utiliser l'option `-h` (par exemple, `lsblk -h`).
5. Afficher uniquement certains types de périphériques :
   * Vous pouvez utiliser des options telles que `-d` (pour afficher uniquement les disques), `-p` (pour afficher uniquement les partitions), `-r` (pour afficher uniquement les périphériques amovibles) pour filtrer les types de périphériques que vous souhaitez afficher.

La commande `lsblk` est pratique pour obtenir rapidement des informations sur les périphériques de bloc connectés à votre système Linux. Elle peut vous aider à comprendre la structure du stockage, à identifier les périphériques et à vérifier les montages et les configurations des partitions.
