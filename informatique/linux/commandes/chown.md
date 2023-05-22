# 👑 Chown

La commande "chown" (change owner) est utilisée sous Linux et d'autres systèmes d'exploitation de type Unix pour modifier le propriétaire et le groupe propriétaire d'un fichier ou d'un répertoire. Elle permet de changer les attributs de propriété d'un fichier. Voici une explication détaillée de la commande "chown" :

Syntaxe de base :&#x20;

```bash
chown [options] propriétaire:fichier(s) 
```

ou

```bash
chown [options] propriétaire:group fichier(s)
```

Principales options :

* `-R` ou `--recursive` : Applique les modifications de manière récursive à tous les fichiers et répertoires contenus dans un répertoire.
* `-v` ou `--verbose` : Affiche des informations détaillées sur les modifications effectuées.

Exemples d'utilisation :

1. Changer le propriétaire d'un fichier :

```bash
chown utilisateur fichier.txt
```

Cela attribue le fichier "fichier.txt" à l'utilisateur spécifié en tant que propriétaire.

2. Changer le propriétaire et le groupe propriétaire d'un fichier :

```bash
chown utilisateur:group fichier.txt
```

Cela attribue le fichier "fichier.txt" à l'utilisateur spécifié en tant que propriétaire et au groupe spécifié en tant que groupe propriétaire.

3. Changer de manière récursive le propriétaire et le groupe propriétaire d'un répertoire et de son contenu :

```bash
chown -R utilisateur:group dossier/
```

Cela attribue le répertoire "dossier" et tous ses fichiers et sous-répertoires à l'utilisateur spécifié en tant que propriétaire et au groupe spécifié en tant que groupe propriétaire.

Il est important de noter que seuls le propriétaire du fichier et le superutilisateur (root) ont la permission de changer le propriétaire d'un fichier ou d'un répertoire. La commande "chown" nécessite des droits suffisants pour effectuer ces modifications.
