# 🦊 fstab

La commande `fstab` (File System Table) est utilisée sous Linux pour configurer les systèmes de fichiers qui doivent être montés automatiquement lors du démarrage du système. Le fichier `/etc/fstab` contient les informations de configuration des systèmes de fichiers et définit les options de montage pour chaque partition ou périphérique de stockage.

Voici comment fonctionne la commande `fstab` :

1. Structure du fichier `/etc/fstab` :
   * Le fichier `/etc/fstab` est un fichier texte qui contient une ligne de configuration pour chaque système de fichiers que vous souhaitez monter automatiquement.
   * Chaque ligne dans le fichier `fstab` suit un format spécifique avec différents champs séparés par des espaces ou des tabulations.
   * Les champs courants sont le périphérique/source, le point de montage, le type de système de fichiers, les options de montage, le dump et le pass.
2. Périphérique/Source :
   * Le premier champ indique le périphérique ou la source de données à monter.
   * Cela peut être le nom du périphérique (par exemple, `/dev/sda1`, `/dev/nvme0n1p2`), l'UUID (identifiant unique universel) du périphérique ou le chemin d'accès à un périphérique réseau.
3. Point de montage :
   * Le deuxième champ spécifie le répertoire de destination (point de montage) où le système de fichiers sera monté.
   * Il s'agit généralement d'un répertoire existant dans la hiérarchie du système de fichiers, tel que `/mnt/data`, `/media/usb`, etc.
4. Type de système de fichiers :
   * Le troisième champ indique le type de système de fichiers du périphérique, par exemple, ext4, ntfs, vfat, nfs, etc.
5. Options de montage :
   * Le quatrième champ spécifie les options de montage pour le système de fichiers.
   * Les options courantes incluent `defaults` (options par défaut), `noauto` (ne pas monter automatiquement lors du démarrage), `ro` (montage en lecture seule), `rw` (montage en lecture-écriture), `user` (autorise les utilisateurs ordinaires à monter/démonter), etc.
6. Dump et Pass :
   * Les cinquième et sixième champs (`dump` et `pass`) sont généralement définis à `0` pour ignorer la sauvegarde et l'ordre de vérification du système de fichiers.
7. Modifier le fichier `/etc/fstab` :
   * Pour modifier le fichier `fstab`, vous devez utiliser un éditeur de texte en mode superutilisateur (par exemple, `sudo nano /etc/fstab`).
   * Ajoutez ou modifiez une ligne de configuration pour chaque système de fichiers que vous souhaitez monter automatiquement.
   * Assurez-vous d'utiliser la syntaxe correcte et de respecter l'ordre des champs.
8. Vérification des erreurs de configuration :
   * Une fois que vous avez modifié le fichier `fstab`, vous pouvez utiliser la commande `mount -a` pour vérifier si les systèmes de fichiers sont montés correctement.
   * Si des erreurs de configuration existent dans le fichier `fstab`, la commande `mount -a` affichera des messages d'erreur.

La commande `fstab` est utilisée pour automatiser le processus de montage des systèmes de fichiers lors du démarrage du système Linux. Elle offre une flexibilité pour définir des options de montage spécifiques à chaque système de fichiers.
